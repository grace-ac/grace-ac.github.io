---
layout: post
title: New Hemolymp sample and Qubit file; New RNA-seq short-term plan
date: '2018-08-20'
category: bairdi
tags: [R, RNASeq]
---
Today Sam, Steven, and I met and decided to pool the 15 samples that had quantifiable RNA (Qubit RNA HS results) from the 40 samples that Sam processed using the Qiagen RNEasy Mini Plus Kit into one sample to be sequenced. Also, they both helped me learn more about data management and creating a better file that contains the crab hemolymph sampling data and the Qubit results data.

## Pool Plan
Today I combined these tubes from the [40 that Sam processed](http://onsnetwork.org/kubu4/2018/08/09/rna-isolation-quantificaiton-tanner-crab-hemolymph/) into one tube (-80 rack 2, Column 3, row 4).   
![img](https://user-images.githubusercontent.com/14934314/44165821-9ae7b500-a07e-11e8-9251-ad50a5d3b7ea.png)


Sam sent me the information of sending this off to get sequenced. Will read this evening and make a plan to do it tomorrow.

## Data organization and management
I am now going to be keeping all the data files (relatively untouched and manipulated) in [project-crab/data](https://github.com/RobertsLab/project-crab/tree/master/data) and will be working in R on scripts kept in [project-crab/scripts](https://github.com/RobertsLab/project-crab/tree/master/scripts) and the new joined files will be kept in [project-crab/analyses](https://github.com/RobertsLab/project-crab/tree/master/analyses). 

Today, Steven and Sam helped me clean up the hemolymph sampling data file so that it is more accurate and also just the information we really care about. The ["sample_table.csv"](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/sample_table.csv) now contains many extra rows. Steven created new tube numbers for Day 26 samples, because those were taken in triplicate (except for the three crabs in the warm treatment, for which there were 6 samples taken). So now, there are tube numbers like so: 401_1, 401_2, 401_3, etc. This is more truly accurate so that we can keep better track of what samples have been touched and how many of Day 26 we have left.

We also joined the improved ["sample_table.csv"](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/sample_table.csv) with qubit results, for which I have sample volume (ul) and total yield (ng) columns. Steven made sure to add the _1 to the Day 26 tube numbers. The new [sample_qubit_table.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/sample_qubit_table.csv) has rows for every tube we have in the freezer, as well as the important information from the qubit results (Test_Date, tube_number, Original_sample_conc_ng.ul, sample_vol_ul, total_yield_ng). 

There are some tubes that are not accounted for because there are some that I have processed, but haven't run on the Qubit, so it currently looks like those samples are still untouched and in the freezer. I will go back through my notebook posts and find the tube numbers for the ones that I have done that with. I would be very surprised if there were more than a dozen tubes that that has happened with (4 crabs - three samples per crab). 

Also, it would be nice to add a column that would include the method of RNA isolation. I used RNAzol RT protocol, whereas the ones that Sam has processed were done with Qiagen RNeasy Mini Plus Kit. We are currently waiting on the lyophilizer to be fixed, after which we will try a new method using Tri-Reagent. 

## Next steps
### - Send pool to be sequenced
### - Once lyophilizer is fixed, give Sam the samples I've picked out for him to try the Tri-Reagent
### - Work through the data sheets more to account for all tubes
