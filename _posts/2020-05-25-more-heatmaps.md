---
layout: post
title: More Crab results - DESeq ABC v GHI; more heatmaps
date: '2020-05-25'
category: bairdi
---
Today I did another `DESeq2` analysis comparing crabs A, B, C to crabs G, H, I at Day 2 in order to get any DEGs for temperature on infection. 
I also tried making some more heatmaps, and I think there may be some cool ones... 

# `DESeq2` Crabs ABC vs GHI at Day
Rmd: [scripts/DESeq-ABC-GHI.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-ABC-GHI.Rmd)

Results: 5 DEGs: [analyses/DEG-ABCGHI.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEG-ABCGHI.tab) 

4 of the 5 DEGs were able to `join` with transcriptome v. 1.5 `blast` output and uniprot_sp_go: [annot_DEGlist-ABCGHI.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/annot_DEGlist-ABCGHI.tab)

Was `join`-ed in this Rmd: [annoate-ABCGHI-DEGlist.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/annoate-ABCGHI-DEGlist.Rmd)

# Heatmaps!!

In all of the following, I used the `DESeq2` to get variance stabilized transformed data. Scroll to the end for plots.  

- [scripts/02-DeSeq-Temperature.html](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/02-DeSeq-Temperature.html 
)

- [scripts/DESeq-infection.html](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-infection.html)

- [scripts/DESeq-ABC-GHI.html](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-ABC-GHI.html)

Then, I tried really hard to figure out if it was possible to get variance stabilized transformed lists for all 2020 Genewiz samples, but I couldn't figure it out.     
So I tried using `DESeq2` on the individual crab samples to make some more heatmaps using the DEG lists from the above scripts: [scripts/heatmaps.html](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/heatmaps.html)

I also include heatmaps (red) with the normalized counts... and they look like nothing. The range of the normalized counts is WAY too big... so you can't see anything. That's why I decided to try the `DESeq2` method for the individual crab comparisons heatmaps.

#### Resources I used to figure those things out:     

https://colauttilab.github.io/RNA-Seq_Tutorial.html  

https://www.rdocumentation.org/packages/DESeq2/versions/1.12.3/topics/varianceStabilizingTransformation    

https://rdrr.io/bioc/DESeq2/man/varianceStabilizingTransformation.html 

# Next steps before lab meeting tomorrow:
- Think of some other ways to make heatmaps
- Try `DESeq2` with time as factor
