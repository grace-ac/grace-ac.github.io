---
layout: post
title: Heatmap Practice
date: '2020-05-19'
category: bairdi
---
Today I've been playing with heatmaps and have been able to make quite a few. Now, I'm just going to keep making a bunch from the individual crab RNAseq data to see if there are any interesting patterns. However, I am struggling to get the Trinity ID counts from the 2020 Genewiz samples (individual crabs) annotated with transcriptome v. 1.5 `blast` output and Uniprot-SP-GO annotation... which means that I'm kind of just mapping random genes... 

### Trying to annotate 2020 Genewiz count matrix

Individual crab sample counts: [sam/20200430_cbai_deg_multiple_conditions/data/salmon.gene.counts.matrix](https://raw.githubusercontent.com/RobertsLab/code/master/r_projects/sam/20200430_cbai_deg_multiple_conditions/data/salmon.gene.counts.matrix)

Rmd to try to annotate list: [scripts/annotate-indiv_crab-genecounts.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/annotate-indiv_crab-genecounts.Rmd)

Tried to do the same thing as what I did when annotated the list of DEGs:    
1. `join` the transcriptome v. 1.5 `blast` output with uniprot-SP-GO.sorted
2. `join` the above created table with the Trinity IDs of the count matrix.

Problem --> NONE of the individual crab samples Trinity IDs match with that of the `blast` transcriptome and uniprot-SP-GO... which doesn't make sense. 

I'm pretty sure that the 2020 Genewiz count matrix is from the transcriptome v. 1.5...?     
[Sam's noteboook post where he makes the count matrix](https://robertslab.github.io/sams-notebook/2020/04/29/Transcript-Abundance-C.bairdi-Alignment-free-with-Salmon-Using-2020-GW-Data-on-Mox.html) 

The reason why I want to annotate this is so that I can map interesting genes in heatmaps, even if they aren't differentiallyexpressed. For example, I have lsits of stress response genes, so I could pick out some that I know match with certain stress response or immune response functions and plot them over time within crabs and compare between crabs... 

### Heat map practice
[Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/deg-heatmaps.Rmd)    

HTML preview of above linked Rmd: [here](https://htmlpreview.github.io/?https://raw.githubusercontent.com/RobertsLab/paper-crab/master/scripts/deg-heatmaps.html)

Pretty easy to make heatmaps!!! 

I also made some of the DEG lists for temperature comparison and infection status comparisons.   

Used this Rmd [here](https://github.com/RobertsLab/paper-crab/blob/master/scripts/join-tempDEG_genecounts.Rmd) to get a list of the 423 [temperature comparison DEGs with gene counts](https://github.com/RobertsLab/paper-crab/blob/master/analyses/temp_DEGlist-counts.tab).

### Plan for before Thursday meeting with SR at 3pm: 
1. add some general notes about the list of enriched DEGs from the temperature comparison (DAVID output: [here](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DAVID-enrich-temp.txt))
2.  Watch the tutorial on making heatmaps to see if there's anything else that would be useful to try: [video](https://www.youtube.com/watch?v=HySAnHTrNnM&list=PLzfP3sCXUnxEu5S9oXni1zmc1sjYmT1L9&index=36)
3.  Make a TON of heatmaps of individual crab data
- Compare crabs across time; can plot specific genes of interest (need to get GO info for the Trinity IDs FIRST!) 



