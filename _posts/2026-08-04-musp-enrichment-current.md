---
layout: post
title: MultiSpecies - Preliminary Enrichment Results Part II
date: '2026-08-04'
categories: [MultiSpecies]
---
See post for details on current enrichment results from MultiSpecies work part II. 

# Code and Result Files: 
GitHub Repo: [project-pycno-multispecies-2023](https://github.com/grace-ac/project-pycno-multispecies-2023/tree/main) 

## Code:
Current results are from taking the annotated DEG lists per species at Day 6, Day 12, and the interaction of day and treatment with the background being each species' respective annotated gene matrix info. Orthogroups are currently not invovled in these results. This is just looking at each species alone. 

These results are also currently just for Biological Processes (BP). 

### Enrichment 
Code:[39-topGO-enrichment.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/39-topGO-enrichment.Rmd) 

Results Directory: [39-topGO-enrichment](https://github.com/grace-ac/project-pycno-multispecies-2023/tree/main/output/39-topGO-enrichment)

Result Stats so Far:   

|                                                                                          | Dermasterias | Pisaster | Pycnopodia |
|------------------------------------------------------------------------------------------|--------------|----------|------------|
| Total Genes                                                                              | 27002        | 49439    | 26538      |
| DEGs at Day 6                                                                            | 107          | 388      | 160        |
| Proportion of Total Genes that are DEGs at Day 6                                         | 0.004        | 0.008    | 0.006      |
| Number of Significantly Enriched Processes (Fisher’s p-value < 0.05) for Day 6           | 56           | 123      | 85         |
| DEGs at Day 12                                                                           | 3406         | 6759     | 6158       |
| Proportion of Total Genes that are DEGs at Day 12                                        | 0.13         | 0.14     | 0.23       |
| Number of Significantly Enriched Processes (Fisher’s p-value < 0.05) for Day 12          | 347          | 684      | 322        |
| DEGs: Interaction of Day and SSWD-Exposure                                               | 733          | 1432     | 4558       |
| Proportion of Total Genes that are DEGs for the Interaction                              | 0.03         | 0.03     | 0.17       |
| Number of Significantly Enriched Processes (Fisher’s p-value < 0.05) for the Interaction | 185          | 274      | 434        |

Results Files:     

_P. helianthiodes_    
- [pycno.Day6.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pycno.Day6.topGO_ALL_BP_results.csv)        
Day 6 enrichment all BP results for _P. helianthiodes_.     
- [pycno.D12.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pycno.D12.topGO_ALL_BP_results.csv)     
Day 12 enrichment all BP results for _P. helianthoides_        
- [pycno.INTERACTION.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pycno.INTERACTION.topGO_ALL_BP_results.csv)     
Interaction of day and treatment enrichment all BP results for _P. helianthoides_.     

_P. ochraceus_    
- [pisa.Day6.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pisa.Day6.topGO_ALL_BP_results.csv)     
Day 6 enrichment all BP results for _P. ochraceus_.      
- [pisa.D12.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pisa.D12.topGO_ALL_BP_results.csv)     
Day 12 enrichment all BP results for _P. ochraceus_.      
- [pisa.INTERACTION.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/pisa.INTERACTION.topGO_ALL_BP_results.csv)     
Interaction of day and treatment enrichment all BP results for _P. ochraceus_.     

_D. imbricata_ 
- [derm.Day6.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/derm.Day6.topGO_ALL_BP_results.csv)     
Day 6 enrichment all BP results for _D. imbricata_.     
- [derm.D12.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/derm.D12.topGO_ALL_BP_results.csv)    
Day 12 enrichment all BP results for _D. imbricata_.    
- [derm.INTERACTION.topGO_ALL_BP_results.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/39-topGO-enrichment/derm.INTERACTION.topGO_ALL_BP_results.csv)    
Interaction of day and treatment enrichment all BP results for _D. imbricata_.    

Result Figures:      
R code: [40-enrichment-figs.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/40-enrichment-figs.Rmd) 

Output directory: [/output/40-enrichment-figs](https://github.com/grace-ac/project-pycno-multispecies-2023/tree/main/output/40-enrichment-figs) 

All are of the top 10 enriched biological processes per species. No orthogroups are incorporated in these results. 

### Day 6 Enrichment Per Species
Top 10 Biological Processes 

![img](../notebook-images/2026-08-04/allspecies_top10_GO_dotplot_day6.pdf)

### Day 12 Enrichment Per Species
Top 10 Biological Processes 

![img](../notebook-images/2026-08-04/allspecies_top10_GO_dotplot-2.pdf)    

### Interaction of Day and Treatment Enrichment Per Species
Top 10 Biological Processes 

![img](../notebook-images/2026-08-04/allspecies_top10_GO_dotplot_INTERACTION.pdf)

### Interpretations
Basically... I haven't looked into the processes yet. But my next steps are to confirm that these are true... double check my code and see what Steven thinks... then go into the literature. 

I do need to also do enrichment or at least try with orthogroup stuff... but when I tried with DAVID there wasn't any. 

# Multi-Species Next Step Thoughts:   
1. Try some stuff with enrichment and orthogroups   
2. Try making a PCA of gene expression that ties genes to shared orthogroups so the PCA can compare expression of all three species, both time points, and both treatments....? Is this possible? Orhtogroups are tricky because many genes can be part of one orthogroup. 

