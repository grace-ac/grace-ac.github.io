---
layout: post
title: Sent BLAST to Mox, and Plan for rest of Week
date: '2018-11-06'
category: bairdi
tags: [BLAST, Mox]
---
I sent a ```.sh``` to Mox to perform a BLAST with my assembled _C. bairdi_ transcriptome and swiss prot. I am also working on figuring out how to do this on Hummingbird (on ```toaster/grace```). Additionally, I have come up with a list of things I want to accomplish this week!

## BLAST to Mox
Yesterday I wasted a bunch of time trying to figure out how to run Jupyter on Mox in order to perform a BLAST... totally forgot that you can just do: ```sbatch -p srlab -A srlab shell.script``` while logged in to Mox... 

So today, I got some assistance from Steven and Sam to make sure that my 20181106_Cb-sprot_blast.sh will work (GitHub Issue [# 470](https://github.com/RobertsLab/resources/issues/470)). 

Script lives on Mox in ```/gscratch/srlab/graceac9/jobs/``` and also a copy of it is [here](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/scripts/20181106_Cbairdi-sprot_BLAST.sh). 

The job is officially in queue (# 428276).

## Plan for the rest of the week (non-class-related tasks):
### Wednesday:    
- Run Bioanalyzer on what I extracted last week using the Qiagen RNeasy Micro Plus Kit
- Get input from Emma on my error rate determination of her Skyline file (she'll come by between 12:30 and 2:30 pm) 
- Try BLAST on Hummingbird
- Edit and publish Crab Meeting #6 DecaPod episode (at home in evening)

### Thursday: 
- Work on R script for organizing new Qubit data
- Come up with an extraction plan to finish by Dec 21st (when I leave for Holidays)
- Determine how many kits need to order

### Friday:
- Extract RNA using Qiagen RNeasy Micro Plus Kit from a subset of the samples I selected Wednesday
- Check in on BLASTs
- START WORKING ON GSS POSTER!!! GSS is Thurs Nov 15th
