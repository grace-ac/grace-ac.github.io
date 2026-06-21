---
layout: post
title: Mutispecies `DESeq2` Results - Links to DEG and Annotated DEG Lists
date: '2026-06-20'
categories: [MutiSpecies]
---
Post detailing the Multi-Species results from `DESeq2` --> DEG lists and annotations.    

# Summary
This post links out all the key results files as of now for differential expression analyses. The count matrices for each species, the `DESeq2` results for all the different comparisons, and the annotated DEG lists from those differential gene expression analyses. 

### Some overall notes: 
- all results are based off of the transcript matrices for each species     
- the different `DESeq2` analyses within each species section are as follows:       

1. Combing time points (day 6 and 12) and just comparing exposed to control within each species: Design = ~ condition (SSWD-exposed vs control)         
2. Design = **~ day + condition**  --> comparing condition (SSWD-exposed or not) while controlling for day (day 6 or 12)      
3. Contrast on the comparison from 2 above --> is the same as the DEG list in 4 below: compares time points (day 6 vs day 12) while controlling for condition (SSWD-exposed vs not). From the `DESeq2` manual: "A **contrast** is a linear combination of estimated log2 fold changes. Can be used to test if differences between groups are equal to zero." To get the contrast, you do: `deseq2.resday <- results(ddsDay, contrast = c("day", "6",  "12"))`, which, again, is the SAME THING as `Design = ~ condition + day` below.                 
4. Design = **~ condition + day** --> a different way to get the same results as 3 above --> comparing time points (day 6 vs day 12) while controlling for condition (SSWD-exposed or not)        
5. Design = **~ condition + day + condition:day** --> interaction. Looks to see if the effect of SSWD-exposure depends on day (6 vs 12) by adding an interaction term (condition:day). Both condition (SSWD-exposure or not) and day (6 vs 12) are main effects, and to see if they depend on each other to result in a gene expression outcome, you need the interaction term of the two (condition:day).       
6. Comparing control to exposed from JUST day 6: Design = ~ condition (JUST for the libraries from day 6 -- comparing SSWD-exposed to control)        
7. Comparing control to exposed from JUST day 12: Design = ~ condition (JUST for the libraries from day 12 -- comparing SSWD-exposed to control)         

# Key Links: 

## Project Repository:        
[project-pycno-multispecies-2023](https://github.com/grace-ac/project-pycno-multispecies-2023) 

**(NOTE: repository is PRIVATE until collaborators publish their genomic data - links in this notebook post will ONLY work for current collaborators)**

## Count Matrices:   
### _P. helianthoides_     
Code: [code/16-hisat2-pycno-d6-d12.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/16-hisat2-pycno-d6-d12.Rmd)        
Gene count matrix (days 6 and 12):[data/pycno_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_gene_count_matrix_2023.csv)       
Transcript count matrix (days 6 and 12): [data/pycno_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_transcript_count_matrix_2023.csv)

### _Pisaster ochraceus_    
Code: [code/17-hisat2-pisaster-d6-d12.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/17-hisat2-pisaster-d6-d12.Rmd)      
Gene count matrix (days 6 and 12): [data/pisaster_gene_count_matrix_2023_all.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_gene_count_matrix_2023_all.csv)      
Transcript count matrix (days 6 and 12): [data/pisaster_transcript_count_matrix_2023_all.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_transcript_count_matrix_2023_all.csv)    

### _Dermasterias imbricata_    
Code: [code/18-hisat2-derm-d6-d12.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/18-hisat2-derm-d6-d12.Rmd)     
Gene count matrix (days 6 and 12): [data/derm_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_gene_count_matrix_2023.csv)     
Transcript count matrix (days 6 and 12): [data/derm_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_transcript_count_matrix_2023.csv)    

## `DESeq2` Results:    
### _P. helianthoides_     

#### All results are from transcript count matrices   
**`DESeq2`**       
Code: [project-pycno-multispecies-2023/code/19-deseq2-pycno.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/19-deseq2-pycno.Rmd)     
1. DEGs combining Day 6 and Day 12: [project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed.tab)     
Design = ~ condition    
1893 DEGs (<0.05 padj)         

2. DEGs controlling for time points (Day 6 vs Day 12) and comparing condition (SSWD exposure or not): [project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_CvEwithDay.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_CvEwithDay.tab)       
Design = ~ day + condition    
2252 DEGs (<0.05 padj)    
```
summary(ddsDay.res)
out of 23353 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 1930, 8.3%
LFC < 0 (down)     : 1367, 5.9%
outliers [1]       : 439, 1.9%
low counts [2]     : 5970, 26%
(mean count < 15)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

3. Contrast on day from above:    
Now need to perform a contrast to see if there is a difference between these groups as it relates to day 
[project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_CvEwithDay_contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_CvEwithDay_contrast.tab)   
791 DEGs (<0.05 padj)     
To get the contrast:   
```
deseq2.resday <- results(ddsDay,
                          contrast = c("day", "6",  "12"))
```

**Files 3 and 4 are the exact same... just two different methods of getting the same file.** 


4. DEGs comparing time points (Day 6 vs Day 12) and controlling for condition (SSWD-exposure or not):    
[project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlforcondition-compare-timepoints.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlforcondition-compare-timepoints.tab)     
Design = ~ condition + day  
791 DEGs (<0.05 padj)     
```
summary(ddsDayCon.res)
out of 23353 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 723, 3.1%
LFC < 0 (down)     : 840, 3.6%
outliers [1]       : 439, 1.9%
low counts [2]     : 7294, 31%
(mean count < 30)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

5. DEGs with an interaction term --> seeing if effects of SSWD-exposure and/or time change over time:    
[project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_interaction.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_interaction.tab)     
Design = ~ condition + day + condition:day     
4003 DEGs (<0.05 padj)            
```
summary(ddsDayInteract.res)
out of 23353 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 2641, 11%
LFC < 0 (down)     : 2539, 11%
outliers [1]       : 268, 1.1%
low counts [2]     : 4793, 21%
(mean count < 7)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

6. DEGs Day 6 alone - exposed vs control : [project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed_DAY6.tab)  
Design = ~ condition    
109 DEGs (<0.05 padj)     

7. DEGs Day 12 alone - exposed vs control: [project-pycno-multispecies-2023/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed_DAY12.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-deseq2-pycno/DEGlist_transcripts_pycno_controlVexposed_DAY12.tab)     
Design = ~ condition     
5359 DEGs (<0.05 padj)   

**Annotating**    
Code: [project-pycno-multispecies-2023/code/22-annot-DEGlists.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/22-annot-DEGlists.Rmd)     

_Annotated lists correspond to the seven DEGlists listed above for Pycnopodia helianthoides_        

1. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot.tab)   
2. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlforday_comparecondition_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlforday_comparecondition_annot.tab)        
3. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_day-contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_day-contrast.tab)     
4. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlforcondition_compareday_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlforcondition_compareday_annot.tab)      
5. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_interaction_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_interaction_annot.tab)      
6. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_DAY6.tab)      
7. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_DAY12.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pycno_controlVexposed_annot_DAY12.tab)     

### _P. ochraceus_      
**`DESeq2`**       
Code: [project-pycno-multispecies-2023/code/20-deseq2-pisaster.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/20-deseq2-pisaster.Rmd)     

1. DEGs combining Day 6 and Day 12: [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_pisaster_controlVexposed.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_pisaster_controlVexposed.tab)     
Design = ~ condition          
2262 DEGs (<0.05 padj)  

2. DEGs controlling for time points (Day 6 vs Day 12) and comparing condition (SSWD exposure or not): [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_CvEwithDay.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_CvEwithDay.tab)    
Design = ~ day + condition    
3054 DEGs (<0.05 padj)   
```
summary(ddsDay.res)
out of 31263 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 3491, 11%
LFC < 0 (down)     : 1197, 3.8%
outliers [1]       : 1702, 5.4%
low counts [2]     : 6590, 21%
(mean count < 2)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

3. Contrast on day from above: [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_CvEwithDay_contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_CvEwithDay_contrast.tab)    
333 DEGs (<0.05 padj)  
To get the contrast:   
```
deseq2.resday <- results(ddsDay,
                          contrast = c("day", "6",  "12"))
```

**Files 3 and 4 are the exact same... just two different methods of getting the same file.** 

4. DEGs comparing time points (Day 6 vs Day 12) and controlling for condition (SSWD-exposed or not): [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlforcondition-compare-timepoints.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlforcondition-compare-timepoints.tab)    
Design = ~ condition + day     
333 DEGs (<0.05 padj)     
```
summary(ddsDayCon.res)
out of 31263 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 256, 0.82%
LFC < 0 (down)     : 493, 1.6%
outliers [1]       : 1702, 5.4%
low counts [2]     : 10905, 35%
(mean count < 13)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

5. DEGs with an interaction term --> seeing if effects of SSWD-exposure and/or time change over time: [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_interaction.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_interaction.tab)        
Design = ~ condition + day + condition:day        
818 DEGs (<0.05 padj)      
```
summary(ddsDayInteract.res)
out of 31263 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 311, 0.99%
LFC < 0 (down)     : 931, 3%
outliers [1]       : 1227, 3.9%
low counts [2]     : 8503, 27%
(mean count < 4)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

6. DEGs Day 6 alone - exposed vs control: [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlVexposed_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlVexposed_DAY6.tab)        
Design = ~ condition     
80 DEGs (<0.05 padj)     

7. DEGs Day 12 alone - exposed vs control: [project-pycno-multispecies-2023/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlVexposed_DAY12.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-deseq2-pisaster/DEGlist_transcripts_pisaster_controlVexposed_DAY12.tab)          
Design = ~ condition    
4558 DEGs (<0.05 padj)   

**Annotating**    
Code: [project-pycno-multispecies-2023/code/22-annot-DEGlists.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/22-annot-DEGlists.Rmd)      

_Annotated lists correspond to the seven DEGlists listed above for Pisaster ochraceus_ 

1. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot.tab)      
2. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlforday_comparecondition.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlforday_comparecondition.tab)        
3. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_annot_day-contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_annot_day-contrast.tab)      
4. [project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlforcondition_comparetime_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlforcondition_comparetime_annot.tab)      
5. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_interaction_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_interaction_annot.tab)      
6. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot_DAY6.tab)    
7. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot_DAY12.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_pisaster_controlVexposed_annot_DAY12.tab)     

### _D. imbricata_      
**`DESeq2`**       
Code: [project-pycno-multispecies-2023/code/21-deseq2-derm.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/21-deseq2-derm.Rmd)     

1. DEGs combining Day 6 and Day 12: [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_derm_controlVexposed.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_derm_controlVexposed.tab)        
Design = ~ condition     
375 DEGs (<0.05 padj)      

2. DEGs controlling for time points (Day 6 vs Day 12) and comparing condition (SSWD exposure or not): [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_CvEwithDay.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_CvEwithDay.tab)              
Design = ~ day + condition      
708 DEGs (<0.05 padj)     
```
summary(ddsDay.res)
out of 23164 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 675, 2.9%
LFC < 0 (down)     : 640, 2.8%
outliers [1]       : 1059, 4.6%
low counts [2]     : 3580, 15%
(mean count < 6)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

3. Contrast on day from above: [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_CvEwithDay_contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_CvEwithDay_contrast.tab)          
1775 DEGs (<0.05 padj)     
To get the contrast:   
```
deseq2.resday <- results(ddsDay,
                          contrast = c("day", "6",  "12"))
```

**Files 3 and 4 are the exact same... just two different methods of getting the same file.** 

4. DEGs comparing time points (Day 6 vs Day 12) and controlling for condition (SSWD-exposed or not): [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_controlforcondition-compare-timepoints.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_controlforcondition-compare-timepoints.tab)         
Design = ~ condition + day    
1775 DEGs (<0.05 padj)    
```
summary(ddsDayCon.res)
out of 23164 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 1695, 7.3%
LFC < 0 (down)     : 1138, 4.9%
outliers [1]       : 1059, 4.6%
low counts [2]     : 6002, 26%
(mean count < 34)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

5. DEGs with an interaction term --> seeing if effects of SSWD-exposure and/or time change over time: [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_interaction.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_interaction.tab)      
Design = ~ condition + day + condition:day      
547 DEGs (<0.05 padj)    
```
summary(ddsInteract.res)
out of 23164 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)       : 321, 1.4%
LFC < 0 (down)     : 424, 1.8%
outliers [1]       : 806, 3.5%
low counts [2]     : 3744, 16%
(mean count < 6)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

6. DEGs Day 6 alone - exposed vs control:  [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_controlVexposed_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_controlVexposed_DAY6.tab)           
Design = ~ condition    
38 DEGs (<0.05 padj)       

7. DEGs Day 12 alone - exposed vs control: [project-pycno-multispecies-2023/output/21-deseq2-derm/DEGlist_transcripts_derm_controlVexposed_DAY12.ta](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/21-deseq2-derm/DEGlist_transcripts_derm_controlVexposed_DAY12.tab)      
Design = ~condition     
2787 DEGs (<0.05 padj)      


**Annotating**    
Code: [project-pycno-multispecies-2023/code/22-annot-DEGlists.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/22-annot-DEGlists.Rmd)         

_Annotated lists correspond to the seven DEGlists listed above for Dermasterias imbricata_ 

1. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot.tab)       
2. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlforday_comparecondition_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlforday_comparecondition_annot.tab)     
3. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_annot_day-contrast.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_annot_day-contrast.tab)    
4. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlforcondition_comparetime_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlforcondition_comparetime_annot.tab)      
5. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_interaction_annot.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_interaction_annot.tab)        
6. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot_DAY6.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot_DAY6.tab)       
7. [project-pycno-multispecies-2023/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot_DAY12.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/22-annot-DEGlists/DEGlist_transcripts_derm_controlVexposed_annot_DAY12.tab)    





