---
layout: post
title: Organizing Crab Qubit results and RNA isolation data - in progress 
date: '2019-08-02'
category: bairdi
---
The past three or so days I've been meticulously searching through all of my notebook posts and RNA isolation result files to create a master table of all of the hemolymph tubes that have been processed both by myself and Sam. Additionally, I made a note as to whether all of the sample was used, or if only some of the slurry was used (meaning that there would still be some in the -80). I'm pretty sure that I have a complete list now, but will revisit in a couple days to give my eyes a rest! Details in post.

## Organization of Crab data
In the spirit of hackweek, I've been taking the time to sort through all of my notebook posts for details related to RNA isolation, as well as Sam's notebook posts, since he has processed several dozen samples as well, in order to create a large list of samples that have been isolated, including those that were tossed due to mistakes, and those that had isolations that were so messed up, I didn't quantify them (this happened one day when I accidentally contaminated the elution H20 and didn't realize until after I had eluted all RNA samples). 

I think that in order to not go insane and in order to truly keep track of the samples, I'll have to use an excel spreadsheet and just manually copy and paste the Qubit results with each new extraction. This won't be hard. It will actually make creating a true master spreadsheet easier because I can just join this master qubit file with a master crab sample file. Previously, I was trying to add each individual Qubit file to a master crab and qubit result file... and it was just getting too tedious and complicated. 

Excel file with qubit and isolation samples: [here](https://github.com/RobertsLab/project-crab/blob/master/data/master-qubit.xlsx)

In order to create a master file, I'll just have to convert the excel tab with the qubit and isolation results into a .csv, then join with the crab sampling data based on tube number! Easy peasy. 

### Next steps for organization
#### Spreadsheets: 
- put all Qubit data into 1 directory (currently I have some on Owl, some on my desktop, and some in the GitHub project. There are some overlap, so I just need to make sure I keep them all in the same place, and get rid of repeats)
- make note of which samples were used to create libraries, and which library they are part of
- once qubit and isolation spreadsheet is truly complete (need to fix an issue with ones where RNA was extracted from the same tubes multiple times), `join` it with the crab sampling master spreadsheet (the one that has triplicate tubes labeled ###-1, ###-2, ###-3)

#### GitHub repo: 
- git rid of my old intermediate attempts at creating a master file
- git rid of old scripts that were used to create those old intermediate master files
- update README.md's

### Next steps for Crab Project:
- revisit transcriptome assembly, annotation from first transcriptome
- think about where I'm going to be keeping all the data, scripts, analyses (gannet and GitHub repo)

