---
layout: post
title: Annotated Protein List from MS Stats with set thresholds... in progress
date: '2019-04-05'
category: 2015Oysterseed
---
Yesterday and today I got some more 2015 DIA paper-related tasks done, including making a table that includes the proteins detected above a log2FC of 3.00 and below -3.00, and one that was annotated... 

### Tasks completed
1. Uploaded the skyline daily .zip file to the Roberts Lab PanoramaWeb in a new folder entitled "2015-DIA-Cgigas-seed". 
2. Updated links in the GitHub [paper-pacific.oyster-larvae/protocols](https://github.com/grace-ac/paper-pacific.oyster-larvae/tree/master/protocols)

### Threshold protein lists
[R script](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/scripts/03-Cgseed-diff-exp.R)      

Yesterday I made one without annotation. [20190403-2015Cgseed-protcomp.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/20190403-2015Cgseed-protcomp.csv) 26 proteins.       
[proteins_comp.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/proteins_comp.csv)

Today I made one with [Steven's annotated protein list](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/Cgseed-protcomp-annotation.tab). 20 proteins.     
[proteins_comp_annot.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/proteins_comp_annot.csv)

We cross-referenced the [20190403-2015Cgseed-protcomp.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/20190403-2015Cgseed-protcomp.csv) with Steven's [pivot table](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/0403-DIA-Cgseed.xlsx) created from [0403-DIA-Cgseed.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/data/0403-DIA-Cgseed.csv) and determined that if the log2FC number is negative, it's 23C, and if the log2FC is positive, it's 29C. 

### Weekend and next week tasks
1. Keep working on paper (intro, methods, discussion)
2. Get results for the paper figured out- do I include the phenotype data even though the 29C data is pooled from 7 silos...?
3. Get repository to the point where it only has the important information. I still think I have too much stuff in there. But once everything is finished, it'll be easier to ID what needs to stay and what needs to go. 
