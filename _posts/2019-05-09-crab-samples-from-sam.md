---
layout: post
title: Closer to having some pooled libraries!
date: '2019-05-09'
category: bairdi
---
Sam extracted RNA using the Quick DNA/RNA Microprep Plus Kit (ZymoResearch) ([post](https://robertslab.github.io/sams-notebook/2019/04/30/RNA-Isolation-and-Quantification-C.bairdi-Hemolymph-Pellet-in-RNAlater.html)). I don't think there is currently enough RNA in the libraries to reach the requiremets for NWGC... details in post. 


Today I quickly joined his [qubit result file](https://docs.google.com/spreadsheets/d/1EMhrPAYvMkduAQWxO_TS3MB2P_8dk9S7JWv5vtUDCDQ/edit?usp=sharing) with the hemolymph sampling data ([hemo_table.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/hemo_table.csv)) in [R](https://github.com/RobertsLab/project-crab/blob/master/scripts/0509-samples-for-libs.R). 

The resulting file: [hemo_qub-for-libs.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/hemo_qub-for-libs.csv)

The goal is to have 12 libraries accounting for each infection status and temperature treatment. Each pooled library needs to have at least 1000 ng of RNA in a sample of ~50ul. ([GitHub Issue #184](https://github.com/RobertsLab/resources/issues/184))

Pooled libraries to create: 

| Library Number | Sample Day | Infection status | Temp trtmnt |
|----------------|------------|------------------|-------------|
| 1              | 9          | 0                | NA          |
| 2              | 9          | 1                | NA          |
| 3              | 12         | 0                | Amb         |
| 4              | 12         | 1                | Amb         |
| 5              | 12         | 0                | Cold        |
| 6              | 12         | 1                | Cold        |
| 7              | 12         | 0                | Warm        |
| 8              | 12         | 1                | Warm        |
| 9              | 26         | 0                | Amb         |
| 10             | 26         | 1                | Amb         |
| 11             | 26         | 0                | Cold        |
| 12             | 26         | 1                | Cold        |


*Note: the temperature treatments didn't start until after the Day 9 sampling day.

As of now, I don't think the pooled samples would have enough RNA to meet the requirements... for example, the samples that fall under Library 1 add up to 79.9 ng/ul. 

I may need to check this again when I'm not sick.
