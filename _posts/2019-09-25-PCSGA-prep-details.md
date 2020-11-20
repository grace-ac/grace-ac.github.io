---
layout: post
title: Crab Project - What I did for PCSGA 2019
date: '2019-09-25'
category: bairdi
tags: PCSGA
---
In this post I will detail what I did for PCSGA 2019. I did some new analyses
and found some new results from our first assembled transcriptome.

### New BLAST
Steven made a BLAST database from the Dinophyceae proteins (Dinophyceae is class under which dinoflagellates are), and did a `BLASTx` against the first assembled transcriptome (Day 26, infected and uninfected, cold and ambient).

I used this script to separate the transcriptome into putative crab and putative _Hematodiniium_ genes: [sep_crab-hemat-genes.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/sep_crab-hemat-genes.Rmd)

That script resulted in the following files:
- [crab-blastx-sp.tab](https://github.com/RobertsLab/project-crab/blob/master/analyses/crab-blastx-sp.tab)
- [hemat-blastx-sp.tab](https://github.com/RobertsLab/project-crab/blob/master/analyses/hemat-blastx-sp.tab)

### Annotating BLAST outputs
In jupyter notebooks, I annotated the two blastx outputs (crab and _Hematodinium_) with GOslim terms.

- [091419-crab-BLAST-to-slim.ipynb](https://github.com/RobertsLab/project-crab/blob/master/notebooks/091419-crab-BLAST-to-slim.ipynb)
- [091419-hemat-BLAST-to-slim.ipynb](https://github.com/RobertsLab/project-crab/blob/master/notebooks/091419-hemat-BLAST-to-slim.ipynb)

I then used the following R script to create files for creating pie charts for biological process GO slim terms:     
[091519-crab-hemat-GOslim.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/091519-crab-hemat-GOslim.Rmd)

The script resulted in the following files:    
- [crab-GOslim-count.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/crab-GOslim-count.csv) 
- [hemat-GOslim-count.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/hemat-GOslim-count.csv)

### Creating pie charts
I used the count.csv files to create pie charts in google sheets: 
- [crab-GOslim-pie](https://docs.google.com/spreadsheets/d/19KVnNG6F3dFFhexe2TuVgkLw_bHXOdu3OsY2bU4Wb3Y/edit#gid=0) 
- [hemat-GOslim-pie](https://docs.google.com/spreadsheets/d/1lNeKlqT5q57WgtVkARp-Afhr9FAchR7OsH9lzNBx6TU/edit#gid=0)

For the talk, I went more in-depth into the "stress response" slice in the crab GOslim pie. I made a table of some crab genes with notes on their names and functions, and links to the uniprot database on those genes:
- [crab-genes](https://docs.google.com/spreadsheets/d/1DZkk1CsFzcEWR-D6mhrH1T9mrXE2SUR8NN9d4MqWhfg/edit#gid=0)

The ones highlighted are the ones I chose to talk about in the talk.

### The talk and slides
Link to final google slides: [Crandall_Wed_1645](https://docs.google.com/presentation/d/1H3Eoh2EdC10Qbc2q7r2oEtThnFbpn0Mq0RFer2WqUyQ/edit)

Link to slidedeck on figshare:
[Effects_of_Bitter_Crab_Disease_on_the_gene_expression_of_Alaskan_Tanner_Crabs](https://figshare.com/articles/Effects_of_Bitter_Crab_Disease_on_the_gene_expression_of_Alaskan_Tanner_Crabs/9898916)

### Thoughts on talk
It was supposed to be 12 minutes, with 3 minutes for questions. I have no idea how much time I took, but I did get 2 clarifying questions at the end of the talk.

It was my first time presenting at a conference, and my slot was on day 2 (Wednesday) at 4:45pm. It was a struggle to stay energized and it was also a struggle to stay calm - I was really nervous!

I think I had good background information and that I explained things fairly well, but I wish I had gone a little more in depth into the genes that we found. I also think that for next time, I need to find ways to combat the nerves because they got a bit in the way of my ability to speak at the beginning - I collected myself well-enough after the third slide or so... but I want to improve! 
