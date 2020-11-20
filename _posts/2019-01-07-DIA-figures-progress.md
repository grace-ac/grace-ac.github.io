---
layout: post
title: 2015 Oysterseed DIA MSStats Figures Progress
date: '2019-01-07'
category: 2015Oysterseed
tags: [MSStats, DIA]
---
Today I went through my [R script](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/R/Skyline-to-MSstats-format-and-plots.R) for the [RobertsLab/project-pacific.oyster-larvae](https://github.com/RobertsLab/project-pacific.oyster-larvae) project. I have a Volcano Plot and a Comparison Plot. I also did some data process plots: Profile Plots and QC Plots. I am working on updating the MS Stats protocol, and will include all the resources I used to create those plots. Additionally, I am beginning to read through the [Oyster-Larval-Proteomics-2015](https://docs.google.com/document/d/1OaYNzlOJr5QibCYt8--GMNGvXlzHPR9_daCkNUVkj-U/edit) paper and am working on finding some new relevant citations. My goal for the month is to finish this project and paper!

### MS Stats protocol and plots
[GitHub Issue #516](https://github.com/RobertsLab/resources/issues/516)     
R Script: [Skyline-to-MSstats-format-and-plots.R](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/R/Skyline-to-MSstats-format-and-plots.R)  

Work-in-progress MSStats protocol: [03-MSStats-protocol.md](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/protocol/03-MSStats-protocol.md)

Resources used to create R Script:    
- [MS Stats R Package Manual](https://bioconductor.org/packages/release/bioc/manuals/MSstats/man/MSstats.pdf)
- [MS Stats Manual](http://msstats.org/wp-content/uploads/2017/01/MSstats_v3.7.3_manual.pdf)
- [Yaamini's R Script](https://github.com/RobertsLab/project-oyster-oa/blob/master/analyses/DNR_Skyline_20170524/2017-06-22-MSstats/2017-06-22-MSstats.R)
- Help from Meena Choi regarding my needing to add a column labeled "Fraction" with all cells containing "1"

#### Plots:   
- [QC Plot](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/QCPlot.pdf)   
- [Profile Plots](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/ProfilePlot.pdf)
- [Profile Plots with summarizations](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/ProfilePlot_wSummarization.pdf)
- [Volcano Plot](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/VolcanoPlot-3.pdf)
- [Comparison Plots](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/ComparisonPlot-3.pdf)


### Goals for this week regarding this project:
- Understand what plots are and figure out what's important
- Figure out if other plots should be made (to be created next week)
- Figure out if other analyses should be done (to be performed next week)
- Work on organizing all the information 
