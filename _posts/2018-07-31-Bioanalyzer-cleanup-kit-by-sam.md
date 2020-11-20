---
layout: post
title: My Bioanalyzer and Sam's RNA Clean-up Kit and RNeasy Plus Mini Kit results
date: '2018-07-31'
category: bairdi
tags: RNAisolation, Bioanalyzer
---
Today I ran the Bioanalyzer on the samples Sam isolated RNA from months ago using RNAzol RT as well as some of the RNA isolated from samples that I have done. The results were not good - no dye showed up, so maybe I did it wrong. TBD. Also, Sam used a kit to clean up the RNA that I have isolated and then ran Qubit and Nanodrop1000, as well as used RNeasy Plus Mini Kit to isolate RNA from untouched hemolymph samples. Low concentrations of RNA, but at least there is RNA. The results from the RNeasy Plus Mini Kit isolations are clean and the RNA on Qubit and Nanodrop1000 are good. 

# Bioanalyzer (GitHub Issue [#328](https://github.com/RobertsLab/resources/issues/328))
Used RNA Pico Chip. I ran the three samples that Sam isolated RNA from in [November 2017](http://onsnetwork.org/kubu4/2017/11/07/rna-isolation-quantification-tanner-crab-hemolymph/). I also ran the following 8 samples from what I previously isolated RNA from:     
360      
214      
287      
358       
469      
434      
463             
457       
![img](../notebook-images/tubes-for-bioanalyzer.JPG)

I loaded the RNA pico chip according to the [protocol](https://github.com/grace-ac/grace-ac.github.io/blob/master/notebook-images/pico-chip-protocol.JPG). Vortex the chip (first time through, it didn't click in to the tension bar very well and popped out. I ran it anyway, but this error popped up:)      
![img](../notebook-images/Error.PNG)

Use 2100 Expert software on the desktop. 

Assay selection: RNA --> Eukaryote Total RNA Pico series II     
Save --> Custom --> Desktop\data\RobertsLab     
After the chip is loaded, name the samples      
![img](../notebook-images/bioanalyzer-software-image.JPG)    
Click START

Results:    
### Electropherogram:    
![img](../notebook-images/electropherogram.PNG)    

### Gel:     
![img](../notebook-images/Gel.PNG)

Results aren't great. Sam noted that:      
`A couple of things:      
No marker is showing up in any of the wells. Expect a tall, narrow, defined peak at ~20 - 23 seconds.    
These have not been DNased, so it may not be surprising that these look crazy?`   

# Sam Cleans up Tanner Crab RNA (GitHub Issue [#330](https://github.com/RobertsLab/resources/issues/330))
## Link to his notebook post: [here](http://onsnetwork.org/kubu4/2018/07/31/rna-cleanup-tanner-crab-rna/)

Samples used:    
![img](../notebook-images/tubes-for-sam.JPG)

Essential results:    
- All concentrations were too low for detection via NanoDrop.
- Qubit quantification indicate yields ranging from ~25ng to ~192.5ng.
- New Qubit results are much lower (except for tubes 409 and 355) 
### Here's how his new cleaned results compare to my previous Qubit results:    
My previous results (column highlighted in pink compares to the blue highlighted column in Sam's Qubit results:)    
![img](../notebook-images/20180731-cleanup-master-pool-original-qubit.png)

Sam's results       
![img](../notebook-images/20180731-sam-rna-cleanup-qubit.png)

# Sam isolates RNA from hemolymph samples using RNeasy Plus Mini Kit (GitHub Issue [#327](https://github.com/RobertsLab/resources/issues/327))
## Link to his notebook post: [here](http://onsnetwork.org/kubu4/2018/07/31/rna-isolation-tanner-crab-hemolymph-using-rneasy-plus-mini-kit/)

I gave Sam four samples from Day 26 (samples were taken in triplicates) from the following crabs:    
451 (infected, cold, immature)    
478 (infected, ambient, immature)     
506 (uninfected, ambient, immature)    
432 (uninfected, cold, mature)   

Essential results:   
- NanoDrop results look good (purity is good)
- Qubit yields are decent (range from ~37ng to ~350ng)

Sam notes that the important thing is that this procedure produced clean RNA, which renders the Qubit results believable. He thinks the RNAzol RT isolations I did had too much contamination carried over causing incorrect Qubit measurements. 

I'm not sure if that means I wasn't careful enough with not carrying contamination between samples or if RNAzol RT didn't work well with the salts and other junk in the crab hemolymph...

**Regardless, we'll try using TriReagent out as soon as some arrives and ponder the idea of getting some kind of isolation kit (Sam's suggestion).** 



