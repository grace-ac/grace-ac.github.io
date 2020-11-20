---
layout: post
title: DIA protocol, and Next Steps
date: '2018-12-07'
category: 2015Oysterseed
tags: DIA
---
Today I worked on documenting what I did (writing up a protocol of sorts) that is in progress. I am re-doing a couple steps just so that I'm ABSOLUTELY certain where files came from, and I'm putting all the new outputs in a brand-new directory so that it's just all more organized. I will upload all of the directory and files into a new folder in OWL, which will be linked out in the new protocol. I also got some input on how to set the thresholds that we talked about in the proteomics meeting yesterday, so I'll try that Monday once my process is fully documented so I can just focus on analysis. 

### DIA protocol (in progress) 
(Based on this DIA outline from MacCoss Lab grad students: [data_analysis](https://docs.google.com/document/d/1Vr3wE7Z8eJVenUWgbxJ3CmXxCoNiba_HYQXh7sNce_k/edit))    

[my new DIA protocol](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/protocol/DIA-protocol.md) 

All of this is being performed on Woodpecker in FTR 209, Roberts' Lab. All of the materials, and output files are in ```/Desktop/grace/Bri-line```    
After all is finished, I'll upload to OWL or GitHub repo... probably GitHub repo is the best... 

### DIA next steps
From Lindsay:   
> The quants exported from Encyclopedia (*.elib.peptides.txt) are all I use. You can view multiple samples using the Multi Elib browser. 

> I don't bother checking chromatograms until I have a reasonably scaled list (e.g. statistically significant, significantly differential, etc). You can't manually curate data at DIA scale, so you gotta have either 
(in order of ascending difficulty from easiest to most laborious:)
(a) willingness to accept that there's gonna be a lot of bad quants; 
(b) a specific hypothesis you want to manually validate a la cherry-picking; <-- this is what I usually do for one-off bio experiments
(c) harsh filters for the quant with thresholds like min 3 quantitative transitions, min 2 peptides, etc; or 
(d) empirically validate quantitative peptides like with a calibration curve. <-- this is probably overkill for almost everyone

We decided on setting stringent thresholds. Bri-line doesn't give you any options to do so, so Lindsay suggested this ([GitHub Issue #507](https://github.com/RobertsLab/resources/issues/507)):   
> There's built in "filters" when running encyclopedia, the parameters include "min quantitative ions" etc. Other filtering is all DIY. I use R or Python to parse the *.elib.peptides.txt and run statistical tests. Then I set up skyline doc to view results of statistical testing 

I'll try that out on Monday (I'm devoting the better part of Monday to this project, or maybe all day if the Bioanalyzer still is out of commission), as well as finish up the protocol.

In the meantime, I'll read up on MS stats ([Yaamini has used this before](https://yaaminiv.github.io/Selecting-SRM-Targets-Part3/)), read up on the [project](https://github.com/RobertsLab/project-pacific.oyster-larvae/wiki/2015-Oyster-Seed-experiment-23C-vs.-29C) more, and revisit the paper: [Oyster-larval-proteomics-2015](https://docs.google.com/document/d/1OaYNzlOJr5QibCYt8--GMNGvXlzHPR9_daCkNUVkj-U/edit) 
