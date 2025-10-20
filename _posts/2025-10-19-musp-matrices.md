---
layout: post
title: MultiSpecies - Matrices for each species 
date: '2025-10-19'
categories: [MultiSpecies]
---
See post for details on the multispecies count matrices developed using `hisat2` and `stringtie`. 

# Overview
*REMINDER: GitHub repo is private due to use of data from collaborators that are not published yet, so the links to code and data files will only work for current project collaborators*

For each species,  I have 24 libraries: controls, n=6 Day 6, n=6 Day 12; exposed, n=6 Day 6, n=6 Day 12. 

Each one has a genome ( _P. helianthoides_ genome is [publicly available (Schiebelhut et al., 2023)](https://datadryad.org/dataset/doi:10.5061/dryad.51c59zwfd); _P. ochraceus_ and _D. imbricata_ are not).       

The libraries were first trimmed (see post: [Multi-Species - Day 6 and Day 12 RNAseq data FastQC and Trimming](https://grace-ac.github.io/MUSP-d6d12-data-processing/)). 

Then, the trimmed RNAseq libraries were aligned to their genomes using `hisat2` and `stringtie` and then count matrices were created (both for genes and transcripts). 

# _P. helianthoides_ 

Code: [project-pycno-multispecies-2023/code/26-hisat2-pycno-d6-d12.Rmd)](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/26-hisat2-pycno-d6-d12.Rmd)     

Aligment MultiQC Report on OWL: [gcrandall/multispeciesSSWD/QCreports/pycno_2023_alignment_ALL_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/pycno_2023_alignment_ALL_multiqc_report.html) 

Gene count matrix:    
[project-pycno-multispecies-2023/data/pycno_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_gene_count_matrix_2023.csv)

Transcript count matrix:      
[project-pycno-multispecies-2023/data/pycno_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_transcript_count_matrix_2023.csv)

# _P. ochraceus_   

Code: [project-pycno-multispecies-2023/code/27-hisat2-pisaster-d6-d12.Rmd)](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/27-hisat2-pisaster-d6-d12.Rmd)   

Alignment MultiQC Report on OWL:     
[gcrandall/multispeciesSSWD/QCreports/pisaster_2023_alignment_ALL_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/pisaster_2023_alignment_ALL_multiqc_report.html)

Gene count matrix:    
[project-pycno-multispecies-2023/data/pisaster_gene_count_matrix_2023_all.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_gene_count_matrix_2023_all.csv)

Transcript count matrix:    
[project-pycno-multispecies-2023/data/pisaster_transcript_count_matrix_2023_all.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_transcript_count_matrix_2023_all.csv)

# _D. imbricata_ 

Code: [project-pycno-multispecies-2023/code/28-hisat2-derm-d6-d12.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/28-hisat2-derm-d6-d12.Rmd)

Alignment MultiQC Report on OWL:     
[gcrandall/multispeciesSSWD/QCreports/derm_2023_alignment_ALL_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/derm_2023_alignment_ALL_multiqc_report.html)

Gene count matrix:    
[project-pycno-multispecies-2023/data/derm_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_gene_count_matrix_2023.csv)

Transcript count matrix:   
[project-pycno-multispecies-2023/data/derm_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_transcript_count_matrix_2023.csv)
