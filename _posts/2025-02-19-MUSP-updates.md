---
layout: post
title: MultiSpecies - MultiQC, Trimming, Short-term Goals
date: '2025-02-19'
categories: [MultiSpecies]
---
Updates and short-term goals for the multi-species analyses

# Goals for the multispecies RNAseq data I currently have
Get functional enrichment for each species.

We don't currently have controls sequenced, so we can't currently do any differential expression analyses.

So for now, I will be focusing on aligning RNAseq data for each species to each species' respective genomes.

Then, I'll do two levels of things to start:    
1. Within each species: start with all genes that are expressed and run functional enrichment on each species (each species has n=6 sea star libraries)      
2. I still need a bit more guidance on this next one, but something where within each species, I normalize based on a gene that doesn't change, and convert all numbers based on some ratio of that gene. Then plot the data, and come up with a threshold, and then functional enrichment within each species. Also... something with z-scores possible? TBD.

# Short Term Goals

**NOTE** The GitHub repository for this project is private, so the links to the code won't work for anyone who does not have collaborative access to the private repository.

## General:
Create a budget request for funding for sequencing controls from Day 12 of the multi-species project.

## Multi-species Data Analyses:
1. ![status](https://img.shields.io/badge/status-in%20progress-orange.svg) --> Create a "Key Files" wikipage in my GitHub repository for this multispecies work (note: this repository will be kept private, as it will contain data files that belong to collaborators that are currently unpublished)       
2. ![status](https://img.shields.io/badge/status-completed-green.svg) 2/12/2025 --> Run FASTQC and get a MultiQC report for the untrimmed RNAseq data     
- [10-FastQC-pre-trim.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/10-FastQC-pre-trim.Rmd)      
- Report: [gcrandall/multispeciesSSWD/QCreports/multiqc_report_untrimmedRNAseqData.html](http://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/multiqc_report_untrimmedRNAseqData.html)
3. ![status](https://img.shields.io/badge/status-completed-green.svg)  2/18/2025 --> Trim the RNAseq data using `bash` chunks on Raven Rstudio server and get MultiQC report. **RIP Mox**   
- [11-multispecies-RNAseq-trimming.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/11-multispecies-RNAseq-trimming.Rmd)     
Trimmed files live: `/home/shared/8TB_HDD_02/graceac9/GitHub/project-pycno-multispecies-2023/output/11-multi-fastp`  note: they are not pushed to the GitHub repository, so are on Raven for analysis.
- FastQC report [multiqc_report_trimmedRNAseqData.html](http://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/multiqc_report_trimmedRNAseqData.html)   
- GitHub Issue asking for input on pre- and post-trim multiqc report: [#2097](https://github.com/RobertsLab/resources/issues/2097)
4. ![status](https://img.shields.io/badge/status-in%20progress-orange.svg) --> Index genomes and run `hisat2` and `stringtie` to align RNAseq data to each species' respective genomes [12-hisat2.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/12-hisat2.Rmd)
