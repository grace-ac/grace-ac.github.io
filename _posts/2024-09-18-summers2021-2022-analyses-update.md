---
layout: post
title: Summer 2021 and Summer 2022 Analyses Status
date: '2024-09-18'
categories: [pycno]
---
Here's where things stand for Summer 2021 and Summer 2022 analyses.

# Notes:
Per Steven's suggestion, I made a wiki in my GitHub repo describing the key data files and providing information about where they live:   

GitHub repo: [grace-ac/paper-pycno-sswd-2021-2022](https://github.com/grace-ac/paper-pycno-sswd-2021-2022)    
Wiki Page in repo: [here](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/wiki/Key-Files)

# `BLAST` the _P. helianthoides_ genome gene list (actually transcripts) to get annotation

Goal --> annotate the genome with BLAST annotation to later annotate the DEG lists.

Code:
[paper-pycno-sswd-2021-2022/code/16-blast-annotation.Rmd](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/code/16-blast-annotation.Rmd)  

BLAST output:    
[paper-pycno-sswd-2021-2022/analyses/16-blast-annotation/blast_out.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/16-blast-annotation/blast_out.tab)

# `kallisto` alignment
[paper-pycno-sswd-2021-2022/code/17-kallisto-2021-2022.Rmd](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/code/17-kallisto-2021-2022.Rmd)

Count matrix:   
[paper-pycno-sswd-2021-2022/data/2021-2022_kallisto_count_matrix_rounded_20240918.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/2021-2022_kallisto_count_matrix_rounded_20240918.tab)


# `DESeq2` to get DEG lists:  
[paper-pycno-sswd-2021-2022/code/18-deseq2_2021_2022.Rmd](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/code/18-deseq2_2021_2022.Rmd)

DEG lists:
### Summer 2021  
8 control adults vs 8 exposed adults:     
[paper-pycno-sswd-2021-2022/data/expB_DEG_DET_lists/DEGlist_8v8_2021_exposedVcontrol.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/expB_DEG_DET_lists/DEGlist_8v8_2021_exposedVcontrol.tab)

Annotated DEG list with counts and BLAST
[paper-pycno-sswd-2021-2022/data/expB_DEG_DET_lists/DEGlist_8v8_2021_exposedVcontrol_counts_BLAST.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/expB_DEG_DET_lists/DEGlist_8v8_2021_exposedVcontrol_counts_BLAST.tab)


### Summer 2022
#### Exposed V Control taking age into account:     
DEG list:     
[paper-pycno-sswd-2021-2022/data/2022_DEG_DET_lists/DEGlist_2022_exposed_v_control_no_contrast.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/2022_DEG_DET_lists/DEGlist_2022_exposed_v_control_no_contrast.tab)

Annotated DEG list with counts and BLAST:  
[paper-pycno-sswd-2021-2022/data/2022_DEG_DET_lists/DEGlist_2022_noage_contrast_counts_BLAST.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/2022_DEG_DET_lists/DEGlist_2022_noage_contrast_counts_BLAST.tab)


#### Exposed V Control taking age into account, contrasting age to get the DEGs that are different by age group:   
DEG list:     
[paper-pycno-sswd-2021-2022/data/2022_DEG_DET_lists/DEGlist_2022-contrast_age.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/2022_DEG_DET_lists/DEGlist_2022-contrast_age.tab)

Annotated DEG list with counts and BLAST:     
[paper-pycno-sswd-2021-2022/data/2022_DEG_DET_lists/DEGlist_2022_agecontrast_counts_BLAST.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/2022_DEG_DET_lists/DEGlist_2022_agecontrast_counts_BLAST.tab)
