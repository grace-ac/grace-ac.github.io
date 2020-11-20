---
layout: post
title: BLAST really running on Mox, 2015 Oysterseed new plan
date: '2018-11-08'
category: [bairdi, 2015Oysterseed]
tags: [Mox, BLAST, DIA]
---
Today I officially ran BLAST on Mox. It kept failing the past couple days, and Steven pointed out I didn't actually make the directory I was telling Mox to put the output in, and that I was saying to use ```blastn``` when it should have been ```blastx```. I also met with Emma yesterday and spoke with Nick from Skyline to come up with a new plan for the 2015Oysterseed DIA analysis. Also, at lab meeting and Crab Meeting last week, Steven gave me some things to try with the BLAST output and assembled transcriptome for GSS next week. Also, I posted DecaPod S1E12 - Crab Meeting 6. Steven mentioned some things that I should go back and change, so I'll work on that in my spare time. 

## BLAST on Mox
I was messing up the script to run BLAST on Mox. Here's what the script looks like now, and the job officially started running today (11/08/18) at 10:38am. (script lives on Mox ```/gscratch/srlab/graceac9/jobs/20181108-Cb-sprot_blast.sh```).      
```
#!/bin/bash
## Job Name
#SBATCH --job-name=bairdiblast_01
## Allocation Definition
#SBATCH --account=srlab
#SBATCH --partition=srlab
## Resources
## Nodes
#SBATCH --nodes=1
## Walltime (days-hours:minutes:seconds format)
#SBATCH --time=3-20:30:00
## Memory per node
#SBATCH --mem=100G
##turn on e-mail notification
#SBATCH --mail-type=ALL
#SBATCH --mail-user=graceac9@uw.edu
## Specify the working directory for this job
#SBATCH --workdir=/gscratch/srlab/graceac9/analyses/1108Cbspblast



# Load Python Mox module for Python module availability

module load intel-python3_2017



/gscratch/srlab/programs/ncbi-blast-2.6.0+/bin/blastx \
-query /gscratch/srlab/graceac9/query/library01/query.fa \
-db /gscratch/srlab/graceac9/blastdb/uniprot_sprot/blastdb/uniprot_sprot \
-max_target_seqs 1 \
-outfmt 6 \
-num_threads 28 \
-out 1108-cbairdiblast-sprot.tab
```
I was saying ```blastn```... but I'm blasting with uniprot-sprot, which is proteins, so I had to do blastx. 

## Plan for Transcriptome and BLAST output once it's done
I'm presenting a poster at GSS next Thursday. Steven mentioned at lab meeting today that I could have some basic transcriptome and BLAST results added to my poster. 

Specifically:   
% _Hematodinium_      
Do a ```blastn``` with all the _Hematodinium_ in NCBI (need to download) and turn my transcriptome into the database    
Do a taxonomy sort (figure out how to do this...)    
Create pie charts      
Ven diagriam comparing homologs between my transcriptome, Laura's, and maybe another one    
Basic stats    

I also want to run the transcriptome through ```Transrate``` in my [jupyter notebook that I started](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/notebooks/Cbairdi_01_transrate.ipynb). 

## 2015 Oysterseed Project
Emma came by yesterday to look at the Skyline document to see if we could figure out why I was still having high (~50%) error rates. She also shared with me that people who have been using Skyline for DIA analysis don't like it, so she sent me the newer method of doing so using Bryline.   

We walked over to Foege to talk to Nick from Skyline regarding this project. He said that basically we weren't doing the correct things to properly analyze our files... don't fully understand what this all means yet, but Nick has been emailing with updates on what doesn't work as he goes through the process himself with the oyster files. 

I guess in the meantime I'll keep reading up on whatever he suggests (when he suggests trying something different), and I'll take a closer look at how to use this other program. 

## DecaPod
DecaPod is available on iTunes, but apparently the author is listed as "unknown". I didn't realize this, so I'll go back and change that. 

Additionally, I just remembered that I think episode 2 still isn't up there. I think it's because it was uploaded differently than the other ones, because that was the one that Steven made. So I guess I'll re-upload it and see if it shows up. Also, I think that episode is missing the intro and outro (was made before S1E1, so it was before I had made the intro and outro), so I'll add those.
