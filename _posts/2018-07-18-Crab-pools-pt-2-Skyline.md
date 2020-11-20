---
layout: post
title: Crab Pools and Skyline Update
date: '2018-07-18'
categories: [bairdi, 2015Oysterseed]
tags: RNASeq, Skyline
---
Today Sam speed vac-ed the pools and put them on ice. We mixed the samples and ran Qubit. The readings were way too low. Sam got out hte Nanodrop and we ran them on that... and the readings were bad. Since I am out of town the rest of this week and half of next, Sam is going to try to fix some things, detailed below. In terms of Skyline, Emma has been in contact with Nick today and others from the Skyline crew. She is working on figuring out what the issue is with my super high error rates. At the end of today's post, I also outline rest of July goals and summer goals. 

## Crab Sample Pools (GitHub issue [#311](https://github.com/RobertsLab/resources/issues/311))
So when Sam got in around 7am, he put the crab pool sample tubes back in the speed vac on medium. After four hours, he collected them and put them on ice. (**Combined with yesterday, the samples starting at 270ul volume got down to 26-34ul volume after 6 hours in the speed vac on medium heat**) I then vortexed them to try to mix the precipitate in the samples. Sam pipetted them to mix and then spun them down. I then ran Qubit on the pool tubes, making sure to avoid the pellets on the bottom (so as to not misleadingly inflate the results). The results were bad- way too low.       
![img](../notebook-images/20180718-qubit-pool-res.png)

The UW Core facility needs the pool sample tubes to have at least 20ng/ul of RNA in a 50ul tube.      
Some potential reasons for this could be that the original samples Qubit readings were inaccurate or that the RNA has degraded and since the Qubit dye only binds to non-degraded RNA, a Nanodrop could potentially tell us if there is RNA in the samples.

We ran the samples on Nanodrop. The results were not good. There was noise and no peak at 260 nm (wavelength). Here is the output file screenshot from those results. pool_master had to be run a second time because the first time didn't work.      
![img](../notebook-images/Nanodrop20180718.PNG)

### Next steps on Crab sample pools
Since I'm going to be out of town until next Thursday and we want to get these pools to the CORe to be sequenced ASAP (the turnaround time will be 3-4 months) Sam will thaw all my samples that were used to make the pools (as can be seen on the pool tabs in this spreadsheet: [20180702-crab-sampling-file.csv](https://github.com/RobertsLab/project-crab/blob/master/data/20180702-crab-sampling-file.xls)) and vortex them to mix, then re-run the Qubit on all of them to see if my original Qubit readings were innaccurate. If they were, then he would re-work the pooling volumes from each sample such that we hit at least the minimum amount of 20ng/ul RNA in a 50ul sample. 

## Skyline DIA
Emma and I talked a bit today in person and she said that she'll work with and talk to the people from Skyline about my issue. She asked for the raw files from the 2015 Oysterseed experiment (owl link: [here](http://owl.fish.washington.edu/phainopepla/C_gigas/2015-12-30/)) and I think she's going through it again with them. Hopefully by the end of next week I'll have some real results I can work with to get this 2015 oysterseed DIA paper done and out by the end of summer. Steven made a good point that once school starts up late September, balancing all of these things will get harder, so I'd much rather get this done before then. 

## July goals
- Send pools to core facility (3-4 month turnaround time)
- Have data to work with for 2015Oysterseed project
- Crab project master spreadsheet done

## Summer goals
- Have a good start on a Trinity and RNASeq analysis workflow for when I do get the crab data back
- Work on and finish the 2015 Oysterseed paper (hopefully a chapter in my thesis as well) 


