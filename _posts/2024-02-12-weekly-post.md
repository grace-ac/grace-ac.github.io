---
layout: post
title: Summer 2021 and Summer 2023 Sea Star Wasting Disease Work Updates
date: '2024-02-12'
categories: [WeeklyBits, pycnopodia, sswd_multispecies_2023]
---
Post with little updates on what I did last week!

# Summer 2021 Work
Did some more PCAs, and `DESeq2` analyses - nothing is annotated yet, though, so this is just looking into differences between treatment groups and disease sign groups preliminarily.

Note:

For summer 2021 work, we did a bunch of experiments, but I was only able to get enough RNA for sequencing for some samples.

I have RNAseq data for samples that are part of Experiment A and Experiment B. Datasheet for all library metadata from Summer 2021: [grace-ac/paper-pycno-sswd-2021/data/sample_metadata.csv](https://github.com/grace-ac/paper-pycno-sswd-2021/blob/main/data/sample_metadata.csv).

**Experiment A** began on 9/23/2021. Stars were injected with either 0.45micron filtered live tissue homogenate from a wasting star (microbial group), heat-killed tissue homogenate from a wasting star (control group), or unfiltered live tissue homogenate from a wasting star (exposed group). Stars were observed 2x daily and sampled at disease sign along with control pair. The RNAseq data timeline control and exposed groups are not balanced due to lack of sufficient RNA for sequencing for some samples. Comparisons made for those libraries are shared below under the title "Experiment A".

**Experiment B** began on 10/05/2021. Stars were injected with heat-killed tissue homogenate from a wasting star (control group) or unfiltered live tissue homogenate from a wasting star (exposed group). Some of the control stars in this experiment were previously injected with the 0.45micron filtered live tissue homogenate in Experiment A but never showed any disease signs, and so they became part of the control group. They continued to remain disease-sign free throughout the remainder of Experiment B. Comparisons made between libraries from Experiment B are shared below under the title "Experiment B".

## Experiment A:

| library_ID | star_ID | previous_exposure | treatment      | sample_date | experiment_day | disease_sign |
|------------|---------|-------------------|----------------|-------------|----------------|--------------|
| PSC.19     | H16     | tank_exposure     | na             | 9/23/21     | na             | armdrop      |
| PSC.23     | H15     | tank_exposure     | control        | 9/26/21     | 3              | armdrop      |
| PSC.24     | E13     | tank_exposure     | 0.45live       | 9/27/21     | 4              | armdrop      |
| PSC.34     | H12     | tank_exposure     | 0.45live       | 10/2/21     | 9              | armtwist     |
| PSC.35     | E05     | na                | unfilteredlive | 10/2/21     | 9              | armdrop      |
| PSC.36     | E04     | na                | unfilteredlive | 10/2/21     | 9              | armdrop      |
| PSC.37     | E01     | na                | unfilteredlive | 10/2/21     | 9              | armdrop      |
| PSC.38     | E12     | na                | 0.45live       | 10/2/21     | 9              | na           |
| PSC.39     | H05     | na                | control        | 10/2/21     | 9              | na           |
| PSC.40     | H04     | na                | control        | 10/2/21     | 9              | na           |
| PSC.42     | H03     | na                | control        | 10/3/21     | 9              | na           |
| PSC.43     | E02     | na                | unfilteredlive | 10/3/21     | 10             | armdrop      |
| PSC.48     | E14     | na                | 0.45live       | 10/7/21     | 12             | na           |
| PSC.49     | E16     | na                | 0.45live       | 10/7/21     | 12             | na           |

### Armdrop Vs. Healthy
Library PSC.19 is from a star that had a shared exposure in a co-housing tank situation with PSC.23, PSc.24, and PSC.34... it did not survive to make it to Experiment A, but because it has the same exposure history as those three libraries that WERE included in Experiment A... I perhaps weirdly decided to include this library in the below preliminary comparison.


![img](../notebook-images/2024-02-12/expA_armdrop_v_healthy_PCA.png)    

PERMANOVA: 0.001.
PCA showing significant difference in RNAseq data between stars that were sampled at arm drop disease sign compared to stars that were healthy at sampling.

Note: PERMANOVA performed in R code: [grace-ac/paper-pycno-sswd-2021/code/04-PCAplots.Rmd](https://github.com/grace-ac/paper-pycno-sswd-2021/blob/main/code/04-PCAplots.Rmd), lines 240-274.

![img](../notebook-image/2024-02-12/expA_DEGs_armdropexposed_V_healthycontrol_volcano.png)      

Volcano plot of the 4,093 DEGs found using `DESeq2` when comparing the libraries shown above in the PCA.

### Control Vs. Unfiltered Live

![img](../notebook-images/2024-02-12/expA_unfiltered_V_control_PCA.png)      

PERMANOVA:







# Summer 2023 Multi-Species Planning
I'll be extracting RNA from samples from the 6 exposed bins, each with a wild juvenile _Pycnopodia helianthoides_, wild _Pisaster ochraceus_ and wild _Dermasterias imbricata_, from Day 12 of the multi-species experiment. That will be n=18 samples that will (provided there's enough RNA) be sent of for total RNA-sequencing.

This time point was selected because it will be a good starting point that will capture a lot of information that will help answer multiple questions.

# Summer 2023 Image Organization
I finally finished uploading, labelling, and organizing all the photos I took of the stars from Summer 2023 experiments! Woo!

# Other
Starting the process of re-vamping my website/notebook! Making it pretty, updating project details, links, etc.
