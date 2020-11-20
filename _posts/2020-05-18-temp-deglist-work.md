---
layout: post
title: New DEG list comparing temperature - annotation, enrichment; annotation of oyster differentially abundant protein list
date: '2020-05-18'
categories: [Oyster; bairdi]
---
Today I worked with the new DEG list from `DESeq2` - comparing elevated (10˚C) and decreased (4˚C) temperature treatments. Annotated with uniprot-SP-GO and used DAVID to get enriched biological processes. Additionally, since it could be interesting to compare between oyster and crab projects, I annotated the list of differentially abundant proteins from the oyster project. 

### NEW DEG list
Analysis in `DESeq2` performed by SR. Then I went through script. 

Comparison --> libraries 8+10 to libraries 9+11 ([new crab paper](https://docs.google.com/document/d/1L2Iil705Qu-GeZOtdV5STjDevfpHHHWcrgMiqw1Wn7Y/edit#) table 1)      
USED SAME TRANSCRIPTOME AS THE ONE USED FOR THE INFECTED STATUS DEG COMPARISON (transcriptome v. 1.5)


In new repo for paper: [RobertsLab/paper-crab](https://github.com/RobertsLab/paper-crab)

Rmd for `DESeq2` --> [scripts/02-DeSeq-Temperature.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/02-DeSeq-Temperature.Rmd) 

List of 423 differentially expressed genes: [analyses/DEG-temperature.tab](https://raw.githubusercontent.com/RobertsLab/paper-crab/master/analyses/DEG-temperature.tab)

#### Annotation 
I did the same process  that I did for the previous DEG list comparing infection statuses. However the .tab DEGlist output from `DESeq2` has the Trinity IDs as row names, not as a column, so in order to name the Trinity IDs column as "Trinity_ID" for `join`-ing purposes, I opend file up in excel and named the first column ([analyses/DEG-temperature.txt](https://raw.githubusercontent.com/RobertsLab/paper-crab/master/analyses/DEG-temperature.txt)).    

1. Annotated the 423 DEG list with [uniprot-SP-GO.sorted](http://owl.fish.washington.edu/halfshell/bu-alanine-wd/17-07-20/uniprot-SP-GO.sorted) and [`blast` output from the transcriptome (v. 1.5)](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/BLAST_to_GOslim/_blast-sep.tab): [scripts/annotate-temp-DEGlist.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/annotate-temp-DEGlist.Rmd)   
2. Resulting file: [analyses/pool_temp-annot_DEGlist.tab](https://raw.githubusercontent.com/RobertsLab/paper-crab/master/analyses/pool_temp-annot_DEGlist.tab)   

The same thing happened here as with the infection status annotation --> the annotated list has more rows that the original list of 423 DEGs... likely because the transcriptome `blast` output has duplicate Trinity IDs listed. Therefore, the number of annotated DEGs (339) is likely not a true number. Still need to figure out how to fix this. 

(also need to fix that in the infections status DEG list annotation: [RobertsLab/project-crab/blob/master/scripts/annotate-2019infection_status-DEGs.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/annotate-2019infection_status-DEGs.Rmd))

### Oyster: annotated list of differentially abundant proteins
I had a list of differentially abundant proteins already, but it wasn't annotated with GO or the _C. gigas_ `blat` output. So I did that:    
R script: [scripts/03-join-annotate-diffexp-prot.R](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/scripts/03-join-annotate-diffexp-prot.R)     
Annotated list: [analyses/diff_abundant-prot-annotated.tab](https://raw.githubusercontent.com/grace-ac/paper-pacific.oyster-larvae/master/analyses/diff_abundant-prot-annotated.tab)    

There were 69 differentially abundant proteins. The number was gotten by using a cut-off of >2 log2 fold change and <-2 log2 fold change from the [list of 2,808 detected proteins](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/20190403-2015Cgseed-protcomp.csv) in the samples. 

### Next steps for thesis work: 
this week:    
- analyses for more crab results - differential expression analsyes for temperature, probably some heat maps, look at variation of certain DEGs across all libraries, ...     
- practice talk Friday: working on flow of information - will be a very rough run-through. Defense date June 2nd.    

Before defense:     
- maybe do some comparisons between oyster and crab differentially abundant/expressed lists...? 

before turn in thesis (due by June 26th at latest):    
- write introduction to thesis tying two projects together (maybe also a conclusion tying the results together?) 



