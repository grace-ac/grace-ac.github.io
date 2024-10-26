---
layout: post
title: Pycno Paper 1 Updates
date: '2024-10-25'
categories: [pycno]
---
Updates on paper methods and results. Updates on goals.

# notes:
Met with Steven to go through paper methods --> streamlining, simplifying, and organizing.

Things to add to paper:
- alignment rates for libraries I'm talking about


# Annotating DEG Lists with GO BP terms:
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/code/23-annotating-deg-lists.Rmd


### Summer 2021
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2021_exposedVcontrol_annotated.tab

### Summer 2022
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2022_exposedVcontrol_annotated.tab

https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2022_exposedVcontrol_withAge_annotated.tab

https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2022_exposedVcontrol_withAgeContrast_annotated.tab

## Comparing 2021 and 2022
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/code/25-compare-2021-2022.Rmd

### Unique 2021
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_unique_2021.tab

### Unique 2022
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_unique_2022.tab

### Shared 2021 and 2022
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_same_2021-2022.tab

# Get list of genes from shared DAVID output

shared DEG list DAVID enrichment output: https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/24-2021-2022-enrichment/2021-2022-same-DAVID.txt

Want the genes that are associated with the top 9 processes (<0.05 Benjamini-Hochberg corrected p-values).

| Term                                                                         | Count | %          | PValue   | List Total | Pop Hits | Pop Total | Fold Enrichment | Bonferroni | Benjamini  | FDR        |
|------------------------------------------------------------------------------|-------|------------|----------|------------|----------|-----------|-----------------|------------|------------|------------|
| GO:0043161~proteasome-mediated ubiquitin-dependent protein catabolic process | 80    | 2.67558528 | 1.86E-08 | 2807       | 173      | 10742     | 1.7696469       | 1.11E-04   | 1.11E-04   | 1.11E-04   |
| GO:0002181~cytoplasmic translation                                           | 28    | 0.93645485 | 4.77E-08 | 2807       | 40       | 10742     | 2.67880299      | 2.84E-04   | 1.42E-04   | 1.42E-04   |
| GO:0006508~proteolysis                                                       | 144   | 4.81605351 | 5.96E-07 | 2807       | 383      | 10742     | 1.43881996      | 0.00354188 | 9.63E-04   | 9.61E-04   |
| GO:0006511~ubiquitin-dependent protein catabolic process                     | 70    | 2.34113712 | 6.47E-07 | 2807       | 156      | 10742     | 1.71718141      | 0.00384429 | 9.63E-04   | 9.61E-04   |
| GO:0007229~integrin-mediated signaling pathway                               | 26    | 0.86956522 | 1.52E-05 | 2807       | 44       | 10742     | 2.2613272       | 0.08674616 | 0.01814814 | 0.01811463 |
| GO:0033209~tumor necrosis factor-mediated signaling pathway                  | 17    | 0.56856187 | 3.58E-05 | 2807       | 24       | 10742     | 2.7106935       | 0.19197353 | 0.03508708 | 0.03502229 |
| GO:0042742~defense response to bacterium                                     | 31    | 1.0367893  | 4.12E-05 | 2807       | 59       | 10742     | 2.0107238       | 0.2177764  | 0.03508708 | 0.03502229 |
| GO:0006412~translation                                                       | 73    | 2.44147157 | 6.75E-05 | 2807       | 184      | 10742     | 1.51826567      | 0.33111824 | 0.04711885 | 0.04703184 |
| GO:0097352~autophagosome maturation                                          | 20    | 0.66889632 | 7.12E-05 | 2807       | 32       | 10742     | 2.39178839      | 0.34563155 | 0.04711885 | 0.04703184 |

Use the uniprot accession ID list to get the genes... but how. Is it literally going to be the same as if I were to use the GO ID and get all those genes?

GitHub Issue: [1996](https://github.com/RobertsLab/resources/issues/1996). Saw that there's been a response but didn't get around to it today, will give it a look soon!
