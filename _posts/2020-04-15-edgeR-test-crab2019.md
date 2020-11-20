---
layout: post
title: "edgeR practice: crab 2019 data"
date: '2020-04-15'
categories: [bairdi, Analyses, edgeR]
---
Haven't posted in a long long time... so in today's post I'll detail what I've been up to with the crab project: paper progress and trying out edgeR for differential gene expression analyses. 

## Testing out `edgeR`
### Non-crab test
We used `edgeR` in the Ecology of Infectious Marine Disease course at FHL in summer 2019 to find differentially expressed genes in eelgrass with and without exposure to a pathogen, _Labyrinthula zostera_. Very convenient timing that I took that class becuase it was before any analyses were being performed for the crab project.

I went back thorugh the github repo we had from the class and tested out `edgeR` by reproducing this script: https://github.com/eimd-2019/project-EWD-transcriptomics/blob/master/analyses/EdgeR/GRASS_START_GENE_MEE_Contrasts_CAB_7_10_nonZostera_at.R 

Things went smoothly and I was able to reproduce everything after I got the 'targets.txt' file from Colleen. 

### Trying with crab data: 2019 dataset
The 2019 RNAseq data was a combination of temperature treatments, but there were four main groupings:      
- Day 26 Uninfected
- Day 26 Infected
- Day 12 Uninfected
- Day 12 Infected

Steven and Sam helped with getting a file of gene counts for each sample (link: [here](https://raw.githubusercontent.com/sr320/nb-2019/master/C_bairdi/analyses/Abundance-merge.txt))

And I made a 'targets' file that lists out the samples and their treatments (link: [targets_2019.txt](https://github.com/RobertsLab/project-crab/blob/master/analyses/targets_2019.txt)). I originally had the sample treatments listed as "26_Uninf", etc., but there's a part in the script where contrasts between different groupings need to be made, and having numbers in the treatment descriptions was messing things up, so I changed it to:     
- "E" = day 12 (stands for 'earlier')
- "L" = day 26 (stands for 'later')
- "U" = uninfected
- "I" = infected     
After that was fixed, the code worked well. 

Link to the Rmd file of testing out `edgeR` with the crab 2019 dataset: 
- markdown with figures: [here](https://github.com/RobertsLab/project-crab/blob/master/scripts/041420-crab-edgeR-test.md) 
- script: [here](https://github.com/RobertsLab/project-crab/blob/master/scripts/041420-crab-edgeR-test.Rmd)

It worked, but I need to go through more slowly and with the manual at hand to make sure all the steps make sense for the crab data. (Manual for `edgeR`: [here](https://www.bioconductor.org/packages/release/bioc/vignettes/edgeR/inst/doc/edgeRUsersGuide.pdf)

## Crab project updates
Paper draft: [here](https://docs.google.com/document/d/1xZjT_2ix39jhFGhPjUqjOIubCEZfnl9yDddIjR3nY38/edit)

methods:    
- have written methods for RNA extraction for each data set
- have written what I can for methods of crab collection and experimental set-up

Results:     
- starting to get some differential gene expression progress in that I'm testing out `edgeR` and working on comparisons
- will work on making a mortality figure

Other:
We got the data back from NWGC that I sent out a while back (Sam's working with it) - notebook post detailing what the samples are: [here](https://grace-ac.github.io/submitted-6-pools-to-NWGC/)


General timeline:     
This week (4/13) - focusing on crab results     
Next week (4/20) - working on discussion      
week after (4/27) - working on intro

Goal to have draft of full thesis done by somewhere around May 4th to send to committee. 
