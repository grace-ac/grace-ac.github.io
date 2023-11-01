---
layout: post
title: Start QC and Trimming of Summer 2022 _Pycnopodia helianthoides_ Coelomocyte RNAseq Data
date: '2023-11-01'
categories: [pycnopodia]
---
Starting the process of working with summer 2022 _Pycnopodia helianthoides_ coelomocyte RNAseq data. This will be part of my talk for SICB in January, and for WSN I'll be focusing on presenting the work I have already done from summer 2021.

## Summer 2022 Raw Data
The raw RNAseq data lives on owl: [https://owl.fish.washington.edu/nightingales/P_helianthoides/](https://owl.fish.washington.edu/nightingales/P_helianthoides/)

The data for summer 2022 are the files with the prefix "PSC-0". Here's a link to the google sheet with sample info (will put into github repo soon): [here](https://docs.google.com/spreadsheets/d/1XOYU03o2HtDA0IaUfHTlZp3fKLAaWsZ2r-2IdVDefek/edit#gid=248611810)

## Pre-trimming QC:
Following my protocol here: [RNAseq-pipeline.md](https://github.com/grace-ac/project-pycno-sswd-2021/blob/main/protocols/RNAseq-pipeline.md#2-quality-check-and-trimming)

Some adjustments to that specific protocol for summer 2022 data are:

### 2. Quality Check and Trimming
#### 1. Untrimmed Data Quality Check Part I: FASTQC

Summer 2022 .fastq.gz files from Owl are on Raven in: `/home/shared/8TB_HDD_02/graceac9/pycnornaseq2022`

Multiqc report for untrimmed data on owl:
[owl.fish.washington.edu/scaphapoda/grace/pycno_2022/multiqc/mutliqc_report.html](http://owl.fish.washington.edu/scaphapoda/grace/pycno_2022/multiqc/multiqc_report.html)


### 3. Trim RNAseq data: Run `fastp` on Mox, then `multiqc`
#### A. `rsync` RNAseq data (fastq.gz) from `nightingales` to `/gscratch/srlab/graceac9/data/pycno/RNAseq/summer2022`

#### B. Script for summer 2022 will be in:
`/gscratch/scrubbed/graceac9/jobs/20231101_pycno2022_fastp.sh`

Trimmed data on Mox is: `/gscratch/srlab/graceac9/analyses/pycno/20231101_PSC2022_trimming`

Moved the trimmed data's multiqc report to owl:
[owl.fish.washington.edu/scaphapoda/grace/pycno_2022/multiqc/trimmed/multiqc_report.html](http://owl.fish.washington.edu/scaphapoda/grace/pycno_2022/multiqc/trimmed/multiqc_report.html)
