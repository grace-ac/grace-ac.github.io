---
layout: post
title: Crab Project - try RNeasy Kit on some samples; Adding Qubit data to sample file
date: '2018-10-22'
category: bairdi
tags: [RNAisolation, R]
---
Today, Steven, Sam, and I discussed where we're at with the crab samples and RNA extraction. We decided to extract some samples using the RNeasy Mini Plus Kit from Qiagen that Sam has already used and had decent results. In the meantime, I'll be working on creating a little metadata analysis comparing the different methods used so far, the yields, whether the samples were lyophilized, etc. To do this, I had to figure out how to add the new Qubit data to the crab sampling file. I think I've figured out a general work flow in R, and Sam helped me out with some codes to fix some errors I was having.

## Crab RNA Extraction history thus far
The [Tri-reagent method](https://github.com/grace-ac/grace-ac.github.io/blob/master/_posts/2018-10-05-trireagent-extraction-no-lyophilizer.md) hasn't been super great becuase the yields have been so low. The RNAzol method from months ago wasn't good either because the Qubit results at the time of extraction were really good, but after pooling and speed vac-ing, the Qubit yields were [too low](https://grace-ac.github.io/Crab-pools-pt-2-Skyline/) for the sequencing faciliy. I even tried the RNAzol protocol, but with [6x the reagents](https://grace-ac.github.io/RNA-protocol-with-6ml-RNAzol/), but that didn't change things. 

[Sam has used the RNeasy Mini Plus Kit](http://onsnetwork.org/kubu4/2018/07/31/rna-isolation-tanner-crab-hemolymph-using-rneasy-plus-mini-kit/) from Qiagen on some samples that I have given him, and had okay yields that were clean (good bioanalyzer and nanodrop readings). 

Since those looked so good, I [gave Sam some more samples](https://grace-ac.github.io/sample-spreadsheet-samples-for-sam-d26/) to do the RNeasy kit on. Of those 40, [only 15 had quantifiable RNA](http://onsnetwork.org/kubu4/2018/08/09/rna-isolation-quantificaiton-tanner-crab-hemolymph/). Those 15 pooled together are what I sent to be sequenced as our first library. I [speed va-ed](https://grace-ac.github.io/speed-vac-new-pool/) them, and then walked them over to NWGC ([August 23, 2018](https://grace-ac.github.io/Pooled-sample-handed-toNWGC/)). 

We [recieved the sequence data](http://onsnetwork.org/kubu4/2018/10/15/data-received-chionoecetes-bairdi-rnaseq-fastqc-analysis/) on October 15, 2018 ([Owl/nightingales/C_bairdi/](http://owl.fish.washington.edu/nightingales/C_bairdi/)).

By next crab meeting (Next Thurs), I will have this data assembled and annotated. Currently looking into using Trinity. 

## Crab Extraction Plan for this week
Extract RNA from a few more Day 26 samples using the Qiagen RNeasy Kit that Sam used and see what happens with yields and purity. 

### Make a visualization of the Crab RNA extraction metadata
For this, I need to streamline the workflow of adding new Qubit data to the [hemosample_qubit_table.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/hemosample_qubit_table.csv). With Sam's help, I think I have a pretty good idea of how to do this. I just need to clean up the script a little and to **figure out how to add the "total_yield_ng" column, though. I know how to add columns and put in information as long as every row has the same information. With this, though, I need the column contents to be the "Original_sample_conc_ng.ul" multiplied by the "total_sample_vol_ul".**

[R script](https://github.com/RobertsLab/project-crab/blob/master/scripts/all-hemo-fixing.R)
