---
layout: post
title: Re-do MS Stats; DIA 2015 Cgseed Updates
date: '2019-04-03'
category: 2015Oysterseed
tags: MSStats
---
Today I got some more input from Emma regarding the reports to export from Skyline to analyze. I exported a new MS Stats report (the built-in one from Skyline) and also made the bioreplicates in the file accurate (details in post). Additionally, I exported a new report that includes information that should help us get to the point of comparing 23C and 29C proteins, and identifying the proteins expressed in total. 

### New reports
[New MS Stats report](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/20190403-MSstats-report.csv.zip)      
[New protein list](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/0403-DIA-Cgseed.csv)      

The new protein list integrates the transitions for the each peptide. However, we are still trying to figure out how to integrate the peptides for each protein (GitHub [#666](https://github.com/RobertsLab/resources/issues/666)). 

I also spoke with Yaamini, and she told me that we should only look at proteins that have 3 or more peptides (ones that have 2 or 1 should be discarded). The ones that have more than 3 peptides, the three most abundant peptides should be used. 

### Re-do MS Stats with new report
[New MS Stats script](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/scripts/MSstats-Cgseed-DIA.R)      

Products from new MS Stats: 
- [protein comparison results table](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/20190403-2015Cgseed-protcomp.csv)   
- [Comparison Plot](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/ComparisonPlot.pdf)
- [Profile Plot](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/ProfilePlot.pdf)
- [Profile Plot with Summarization](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/ProfilePlot_wSummarization.pdf)
- [QC Plot](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/QCPlot.pdf)
- [Volcano Plot](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/VolcanoPlot.pdf) 

### Thoughts on new MS Stats
I haven't delved too much into the plots, except for the Volcano Plot.

It is very different from the one I did with the earlier MS Stats report (the one I created by hand). 

The one from before had the bioreplicates wrong. I had:    

| Temp trtmnt | sample day | sample | bioreplicate |
|-------------|------------|--------|--------------|
| 23C         | 9/11/15    | 1      | 1            |
| 29C         | 9/11/15    | 2      | 2            |
| 23C         | 9/14/15    | 13     | 1            |
| 29C         | 9/14/15    | 14     | 2            |

And it showed that there was 1 significantly downregulated ([old volcano plot](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/analyses/VolcanoPlot.pdf)) 

Today, Steven said that bioreplicates should actually be within treatment. So I fixed the bioreplicates for today's MS Stats report and MS Stats analysis in R. The bioreplicates are now:      

| Temp trtmnt | sample day | sample | bioreplicate |
|-------------|------------|--------|--------------|
| 23C         | 9/11/15    | 1      | 1            |
| 29C         | 9/11/15    | 2      | 1            |
| 23C         | 9/14/15    | 13     | 2            |
| 29C         | 9/14/15    | 14     | 2            |

Maybe that's why the new Volcano plot has no significant proteins and the last plot did. 

### Next steps: 
- Compare 23C with 29C using the new report: [0403-DIA-Cgseed.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/0403-DIA-Cgseed.csv) 

>I also spoke with Yaamini, and she told me that we should only look at proteins that have 3 or more peptides (ones that have 2 or 1 should be discarded). The ones that have more than 3 peptides, the three most abundant peptides should be used.

- Get protein lists: total proteins, and (if temp trtmnts are different) proteins for each temp trtmnt

- Clean up repo: readme files; only include important stuff

- Finish paper by April 17th 

