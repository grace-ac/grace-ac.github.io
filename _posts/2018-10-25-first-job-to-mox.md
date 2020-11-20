---
layout: post
title: Sent First Trinity Assembly Job to Mox!
date: '2018-10-25'
category: bairdi
tags: [Trinity, Mox, Assembly]
---
Today, with Steven's guidance, I sent the first job to mox! I am not sure if it will work, but I have it set up to get email notification when the job finishes. Below I provide the link to the .sh script to run Trinity as well as the command line code to run Trinity on mox. I also am starting to work on creating a BLAST pipeline ready. I provide the link to what I'm working on. Currently it's in a jupyter notebook, but Steven said that this can also be done on Mox, so I'll work on making it into an .sh script and create GitHub issues to get it checked out by Steven and Sam. 

## Trinity on Mox
[20181024_Cbairdi_trinity_01.sh](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/scripts/20181024_Cbairdi_trinity_01.sh)

Here's what I put in the commandline to make it happen:    
```
/gscratch/srlab/graceac9/data
[graceac9@mox1 data]$ ls
304428_S1_L001_R1_001.fastq  304428_S1_L002_R1_001.fastq
304428_S1_L001_R2_001.fastq  304428_S1_L002_R2_001.fastq
[graceac9@mox1 data]$ cd ../
[graceac9@mox1 graceac9]$ ls
analyses  blastdb  data  jobs
[graceac9@mox1 graceac9]$ cd jobs
[graceac9@mox1 jobs]$ pwd
/gscratch/srlab/graceac9/jobs
[graceac9@mox1 jobs]$ touch 20181025_Cbairdi_trinity.sh
[graceac9@mox1 jobs]$ ls
20181025_Cbairdi_trinity.sh
[graceac9@mox1 jobs]$ nano 20181025_Cbairdi_trinity.sh 
[graceac9@mox1 jobs]$ head 20181025_Cbairdi_trinity.sh 
#!/bin/bash
## Job Name
#SBATCH --job-name=20181024_Cbairdi_trinity_01
## Allocation Definition 
#SBATCH --account=srlab
#SBATCH --partition=srlab
## Resources
## Nodes 
#SBATCH --nodes=1   
## Walltime (days-hours:minutes:seconds format)
[graceac9@mox1 jobs]$ sbatch -p srlab -A 20181025_Cbairdi_trinity.sh 
^C
[graceac9@mox1 jobs]$ sbatch -p srlab -A srlab 20181025_Cbairdi_trinity.sh 
Submitted batch job 401714
[graceac9@mox1 jobs]$ squeue | grep srlab
            401714     srlab 20181024 graceac9 PD       0:00      1 (QOSGrpCpuLimit)
            401715     srlab BismarkA   strigg PD       0:00      1 (QOSGrpCpuLimit)
            401682     srlab 20181012 yaaminiv PD       0:00      1 (QOSGrpCpuLimit)
            359332     srlab  Ae_canu jldimond  R 13-00:30:22      1 n2211
            394229     srlab BismarkA   strigg  R   21:40:22      1 n2203
[graceac9@mox1 jobs]$ 
```

GitHub Issue [#452](https://github.com/RobertsLab/resources/issues/452) outlines some uncertainties Sam has on whether the script will work, but I'll see what happens when the job finishes (if it finishes). 

## Creating BLAST Pipeline
Currently, I have this .ipynb notebook that is based on other BLAST projects I've done: [0181025-blast-Cbairdi_swiss-prot.ipynb](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/notebooks/20181025-blast-Cbairdi_swiss-prot.ipynb)

In class, Steven said that BLAST can be run on Mox as well, so I'm thinking I can make the BLAST script into a .sh. Perhaps something like this... [20181025_bash_BLAST_script.sh](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/scripts/20181025_bash_BLAST_script.sh)..

I don't think either of those scripts would work in their current states, obviously. I'm going to work through them a little more and then make an Issue in GitHub to see what needs to be changed/added for either or both to work. 
