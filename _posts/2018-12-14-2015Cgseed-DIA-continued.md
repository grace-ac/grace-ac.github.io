---
layout: post
title: DIA analysis 2015 Cg seed continued
date: '2018-12-14'
category: 2015Oysterseed
tags: [DIA, MSstats]
---
Today I am continuing my work in MS stats and working with the exported Skyline report. I updated the protocol to document what I have been doing to get where I am. I am in contact with Meena from MS stats, who is helping me with an error that keeps coming up in the R code. Once that is fixed, I'll be able to analyze the data and make some figures/tables. 

## Updated protocol
I updated the [02-SkylineDaily-protocol.md](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/protocol/02-SkylineDaily-protocol.md) to share how to include all the information needed in the Skyline exported report to use in MS Stats. 

## MS stats
**I'll make a third protocol.md for using MS stats once it's all sorted out.**
[Skyline-to-MSstats-format.R](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/R/Skyline-to-MSstats-format.R)

I'm still stuck at the point where I'm trying to get my converted Skyline report to work with MS stats. I have successfully changed the column names, but am stuck at the ```dataProcess``` command. I have a [GitHub Issue](https://github.com/RobertsLab/resources/issues/516) open and Emma has been giving suggestions, but recommended I join the MS Stats google group. 

I joined the group and got a response from Meena Choi from the MS Stats team, and am awaiting on her next response. 

In the meantime, I'm still looking through:   
- [Yaamini's notebook posts](https://yaaminiv.github.io/Selecting-SRM-Targets-Part3/) and [R script](https://github.com/RobertsLab/project-oyster-oa/blob/master/analyses/DNR_Skyline_20170524/2017-06-22-MSstats/2017-06-22-MSstats.R)

- [MS Stats Manual](http://msstats.org/wp-content/uploads/2017/01/MSstats_v3.7.3_manual.pdf)

- [MS Stats R package manual](https://bioconductor.org/packages/release/bioc/manuals/MSstats/man/MSstats.pdf)

I'm looking forward to moving past this ```dataProcess``` error so that I can finally compare the 23C _C. gigas_ seed with the 29C _C. gigas_ seed. 
