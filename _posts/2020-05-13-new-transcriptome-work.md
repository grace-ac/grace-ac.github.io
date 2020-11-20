---
layout: post
title: Submitted Thesis Chapters to Committee; Start working with New transcriptome
date: '2020-05-13'
category: bairdi
---
Today I submitted my two thesis chapters to my committee, and between now and June 2nd (my defense date), I'll be doing more differential expression analyses with the new transcriptome (not filtered based on taxonomy). Plan for the work and what I've done so far detailed in post.

### Submitted chapters
Submitted:     
Chapter 1 --> [Oyster paper](https://docs.google.com/document/d/1OaYNzlOJr5QibCYt8--GMNGvXlzHPR9_daCkNUVkj-U/edit)        
Chapter 2 --> [Crab paper](https://docs.google.com/document/d/1xZjT_2ix39jhFGhPjUqjOIubCEZfnl9yDddIjR3nY38/edit)      

I'll also write up a thesis introduction that ties the two chapters together. 

Thesis is due to the Graduate School by June 26th (all grad students got a two week extension due to pandemic).      
Thesis submission resources:      
[Timeline](https://grad.uw.edu/for-students-and-post-docs/degree-requirements/dates-and-deadlines/#Spring)       
[Electronic thesis formatting guidelines](https://grad.washington.edu/for-students-and-post-docs/thesisdissertation/etd-formatting-guidelines/)     

### New transcriptome work so far:    
I started a new crab paper ([here](https://docs.google.com/document/d/1L2Iil705Qu-GeZOtdV5STjDevfpHHHWcrgMiqw1Wn7Y/edit)) and added link to the [pubathon page](https://github.com/RobertsLab/resources/wiki/Pubathon). 

I copied over the methods and results from the first crab paper (the one I sent to my committee), and am replacing the statistics, numbers, etc. with those from the new transcriptome. I also made a new stress response gene list and a new transcriptome GOslinm pie chart:      
- [stress-response-genes.tab](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/stress-response-genes.tab) ([Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/051320-NEW-get-stress-response-gene-list.Rmd))
- [excel file where I make pie](https://github.com/RobertsLab/project-crab/blob/master/analyses/make-new-GOslim-pie.xlsx) (can be seen in paper in results)  

Jupyter notebook where I took the new `blast` results to GOslim: [here](https://github.com/RobertsLab/project-crab/blob/master/notebooks/051320-bairdi_new-transcript_Blast-toGOslim.ipynb)

New transcriptome `blast` results: [here](https://gannet.fish.washington.edu/Atumefaciens/20200508_cbai_diamond_blastx_transcriptome-v2.0/20200507.C_bairdi.Trinity.blastx.outfmt6) 

New transcriptome [Blastquery-GOslim.tab](https://github.com/RobertsLab/project-crab/blob/master/analyses/BLAST_to_GOslim/new_transcriptome/Blastquery-GOslim.tab)

I also made a table of all the samples that we have RNAseq data for (in paper). I made it based on [this google sheet](https://docs.google.com/spreadsheets/d/1d17yg5F5gKKC66O8QkTIlPxljJeuX7ZsG46pkBr1lNQ/edit#gid=445629834) (tab labeled "table-for-paper"). I also used this google sheet ([here](https://docs.google.com/spreadsheets/d/1hXMY1rg5qYNTsqvO7PXbRgM7LF06ntEp27N2Efc9gSo/edit#gid=0)) to figure out the individual crabs and come up with a crab ID scheme. Currently am using letters A through I (9 crabs, 6 have 3 time points of RNAseq data, 3 have 2 time points (the warm crabs that didn't survive the experiment)). 

### New plan between now and June 2nd
- Next week --> differential expression analyses (details will be discussed 05/14 on specific comparisons)
- Week after --> modify paper (intro, discussion) based on new results

I'll also be doing a practice "talk" on May 22nd... won't be a full on talk, will just be getting feedback on flow of presentation and ideas on what is important and isn't to include in defense. 
