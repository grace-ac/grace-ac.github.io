---
layout: post
title: More RNA extracted from Day 9 - RNA in all
date: '2019-11-15'
category: bairdi
tags: [Zymo, Qubit, RNAisolation]
---
I extracted RNA from the same tubes that I worked with a lot the past couple of weeks on the bioanalyzer and Nanodrop and qubit because there ended up being not much left. RNA was in all samples. Details of extraction and next steps in post. 

### Samples: 

Because I used so much of the eluted RNA from the samples that I tried to get DNA free ([post](https://grace-ac.github.io/bairdi-nanodrop-bioanalyzer-kallisto/)), I re-did those samples. 

| FRP  | trtmnt_tank | day | infection_status | maturity | tube_number |
|------|-------------|-----|------------------|----------|-------------|
| 6157 | NA          | 9   | 0                | M        | 169         |
| 6143 | NA          | 9   | 0                | M        | 10          |
| 6228 | NA          | 9   | 0                | I        | 29          |
| 6150 | NA          | 9   | 0                | M        | 119         |
| 6277 | NA          | 9   | 0                | I        | 177         |
| 6156 | NA          | 9   | 0                | I        | 24          |
| 6272 | NA          | 9   | 0                | I        | 111         |
| 6178 | NA          | 9   | 0                | M        | 124         |
| 6161 | NA          | 9   | 0                | M        | 53          |
| 6136 | NA          | 9   | 0                | M        | 91          |
| 6137 | NA          | 9   | 1                | I        | 81          |
| 6112 | MA          | 9   | 0                | I        | 28          | 

### RNA isolation
Used the same process to isolate as [previous posts](https://grace-ac.github.io/rna-extractions-day12-qubitresults/) with the Zymo RNA Microprep kit. No obvious, glaring mistakes were made as far as I'm aware. 

### Results: 

I acciddentally didn't make enough of the Qubit RNA HS working solution for all 12 samples plus the two standards, so I ran 10 samples, and then the remaining two separately. 

[Google sheets](https://grace-ac.github.io/rna-extractions-day12-qubitresults/)       
[Raw qubit (10 samples)](https://github.com/RobertsLab/project-crab/blob/master/data/Qubit_data/QubitData_2019-11-15_14-57-49.csv)       
[Raw qubit (2 sampels)](https://github.com/RobertsLab/project-crab/blob/master/data/Qubit_data/QubitData_2019-11-15_15-04-58.csv)

| test_date      | qubit_tube_conc_ng.ml | original_sample_conc_ng.ul | sample_vol_ul | dilution_factor | tube_number | extraction_method | ul_sample-used | elution_vol_ul | total-yield_ng |
|----------------|-----------------------|----------------------------|---------------|-----------------|-------------|-------------------|----------------|----------------|----------------|
| 11/15/19 14:57 | 157                   | 15.7                       | 2             | 100             | 91          | Zymo_microprep    | 35             | 15             | 204.1          |
| 11/15/19 14:57 | 312                   | 31.2                       | 2             | 100             | 53          | Zymo_microprep    | 35             | 15             | 405.6          |
| 11/15/19 14:57 | 228                   | 22.8                       | 2             | 100             | 124         | Zymo_microprep    | 35             | 15             | 296.4          |
| 11/15/19 14:57 | 399                   | 39.9                       | 2             | 100             | 111         | Zymo_microprep    | 35             | 15             | 518.7          |
| 11/15/19 14:56 | 282                   | 28.2                       | 2             | 100             | 24          | Zymo_microprep    | 35             | 15             | 366.6          |
| 11/15/19 14:56 | 630                   | 63                         | 2             | 100             | 177         | Zymo_microprep    | 35             | 15             | 819            |
| 11/15/19 14:56 | 323                   | 32.3                       | 2             | 100             | 119         | Zymo_microprep    | 35             | 15             | 419.9          |
| 11/15/19 14:56 | 331                   | 33.1                       | 2             | 100             | 29          | Zymo_microprep    | 35             | 15             | 430.3          |
| 11/15/19 14:56 | 229                   | 22.9                       | 2             | 100             | 10          | Zymo_microprep    | 35             | 15             | 297.7          |
| 11/15/19 14:56 | 281                   | 28.1                       | 2             | 100             | 169         | Zymo_microprep    | 35             | 15             | 365.3          |
| 11/15/19 15:04 | 221                   | 22.1                       | 2             | 100             | 28          | Zymo_microprep    | 35             | 15             | 287.3          |
| 11/15/19 15:04 | 510                   | 51                         | 2             | 100             | 81          | Zymo_microprep    | 35             | 15             | 663            |

RNA in all!!

### Next steps: 
Come up with pooling plan for the next 6 libraries:     

| Infection status | Day | Temp trtmnt |
|------------------|-----|-------------|
| Infected         | 9   | NA          |
| Uninfected       | 9   | NA          |
| Infected         | 12  | cold        |
| Uninfected       | 12  | cold        |
| Infected         | 12  | warm        |
| Uninfected       | 12  | warm        |

Pool them next week, and hopefully by then we'll have a quote from NWGC, so that we can submit them next week for library prep and seq. 
