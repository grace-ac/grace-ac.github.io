---
layout: post
title: Worked more on R script for adding Qubit data; Started using Mox
date: '2018-10-23'
category: bairdi
tags: [R, Mox]
---
Today I worked more on my R script for adding new Qubit files. Everything works great up until the actual joining of files. After joining, there are extra columns that have the extensions ".x" and ".y"... I think it has something to do with the fact that some columns are factors, some are characters, and some are numeric... I also started using Mox today, but am unsure how to upload the .fastq files from the C bairdi transcriptome data. Waiting to hear back on that in a GitHub issue.

# R Script
Script [here](https://github.com/RobertsLab/project-crab/blob/master/scripts/all-hemo-fixing.R)

Issue with the final joining. 

# Mox
Steven showed me some examples of how to run Trinity on Mox. 
```#!/bin/bash
## Job Name
#SBATCH --job-name=trinity
## Allocation Definition
#SBATCH --account=srlab
#SBATCH --partition=srlab
## Resources
## Nodes (We only get 1, so this is fixed)
#SBATCH --nodes=1
## Walltime (days-hours:minutes:seconds format)
#SBATCH --time=10-100:00:00
## Memory per node
#SBATCH --mem=100G
#SBATCH --mail-type=ALL
#SBATCH --mail-user=sr320@uw.edu
## Specify the working directory for this job
#SBATCH --workdir=/gscratch/srlab/sr320/analyses/0624b





source /gscratch/srlab/programs/scripts/paths.sh


/gscratch/srlab/programs/trinity/Trinity \
--seqType fq \
--max_memory 100G \
--left /gscratch/srlab/sr320/data/geoduck-RNA-seq/NR012_S1_L001_R1_001.fastq,\
/gscratch/srlab/sr320/data/geoduck-RNA-seq/NR012_S1_L002_R1_001.fastq \
--right /gscratch/srlab/sr320/data/geoduck-RNA-seq/NR012_S1_L001_R2_001.fastq,\
/gscratch/srlab/sr320/data/geoduck-RNA-seq/NR012_S1_L002_R2_001.fastq \
--trimmomatic \
--CPU 28
```

[hyak_mox Wiki](https://github.com/RobertsLab/hyak_mox/wiki)

To upload files:    
[File transfers](https://github.com/RobertsLab/hyak_mox/wiki/File-Transfers)



```ssh: connect to host 205.175.107.122 port 22: Connection timed out
rsync: connection unexpectedly closed (0 bytes received so far) [Receiver]
rsync error: unexplained error (code 255) at io.c(605) [Receiver=3.0.9]
[graceac9@mox1 ~]$ 
