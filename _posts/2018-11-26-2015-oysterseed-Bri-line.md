---
layout: post
title: Start new DIA analysis using Walnut, EncyclopeDIA, and Bri-line
date: '2018-11-26'
category: 2015Oysterseed
tags: [DIA, Bri-line, EncyclopeDIA, Walnut, Skyline]
---
Today I tried doing the ```mprophet``` model in Skyline Daily. It wasn't super great and I got stuck, but Emma reminded me that a lot of people who do DIA analysis prefer a new method using Walnut, EncyclopeDIA, and Bri-line. I started this new protocol today and am currently letting Walnut make the new chromatogram library, which will take a while. I'll move on to the next phase for this tomorrow when the library is done.

## mprophet
```mprophet``` is part of the [Advanced Peak Picking Tutorial](https://skyline.ms/_webdav/home/software/Skyline/@files/tutorials/PeakPicking_2-5.pdf). I finished the model, but didn't go into checking the error rates because Emma reminded me that the Walnut, EncyclopeDIA, "Bri-line" method is what others have been preferring.

20181126-2015-Cgseed.sky.zip is too large to add to OWL... but it's on Woodpecker (FTR 209)

## New method in a nutshell
1. Convert .raw to .mzML using MSConvert (Check)
2. Walnut --> make .elib file using the .mzML files made in Step 1. "Save Chromatogram Library" (in progress - will be done tomorrow)
3. EncyclopeDIA --> Search wide-window data with library from Step 2.
4. Bri-line --> ELIB browser: look at peaks; RAW file browser: look at RAW files

This method is pretty straight forward and seemingly easy to follow - will report back on that in tomorrow's notebook post.

## Goals for the week:
Tuesday      
1. Finish new DIA analysis method

Wednesday       
1. Extraction plan for Crab samples - get input from Steven and Sam
2. Start extractions (?)

Thursday      
I have a million classes (3), so I won't have time to fit in extractions, but:    
1. Work on R script for adding new Qubit data

Friday     
1. Extractions
2. Anything from my previous goals that I couldn't finish


