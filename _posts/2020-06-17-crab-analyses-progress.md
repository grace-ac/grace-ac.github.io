---
layout: post
title: Crab Analyses Progress
date: '2020-06-17'
category: bairdi
---
I made some progress in getting new results for the crab part of my thesis. I ran `DESeq2` on libraries 8-11 based on infection, but taking temperature into account. I then took those results and contrasted the two temperature treatments to get an effect of temperature on infection gene expression. I also am trying to do time-series with the individual crab RNAseq... and that's been a bit tricky because in some cases we don't have any replicates, and in ones where we do, there are three time points and I'm struggling to figure out how to analyze them... links to Rmd and results files in post: 

## `DESeq2` on libraries 8-11 based on infection taking temperature into account: 
Rmd: [scripts/DESeq-libraries8-11.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-libraries8-11.Rmd)      
.HTML preview: [/scripts/DESeq-libraries8-11.htm](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-libraries8-11.html)      

**Heatmaps are viewable in the .html linked above^**

Infection comparison taking temperature into account       
DEGlist (.tab)             
[analyses/DEGlist-infection_temp-libs8-11.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-infection_temp-libs8-11.tab)        

DEGlist (.txt with Trinity_ID column):            
[analyses/DEGlist-infection_temp-libs8-11.txt](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-infection_temp-libs8-11.txt)        

With count data:        
[/analyses/DEGlist-inf-temp-libs8-11_counts.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-inf-temp-libs8-11_counts.tab)      
 
Annotated with transcriptome v. 1.5 blast output and uniprot-GO:          
[analyses/DEGlist-infection_temp-annot.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-infection_temp-annot.tab)    

### Contrast temperature treatments from the above results:    
DEGlist (.tab)          
[analyses/DEGlist-contrast_temp-libs8-11.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-contrast_temp-libs8-11.tab)     

DEGlist (.txt)          
[analyses/DEGlist-contrast_temp-libs8-11.txt(https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-contrast_temp-libs8-11.txt)       

With count data:          
[analyses/DEGlist-contrast-temp-libs8-11_counts.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-contrast-temp-libs8-11_counts.tab)      

Annotated with transcriptome v. 1.5 blast output and uniprot-GO:           
[analyses/DEGlist-contrasttemp-annot.tab](https://github.com/RobertsLab/paper-crab/blob/master/analyses/DEGlist-contrasttemp-annot.tab)

**Some** processes present in the list of DEGs that were able to be annotated (43 genes) with uniprot-GO:     
- apoptosis    
- cellular response to decreased oxygen     
- transcription activity    
- defense response to gram-negative bacterium      
- cell proliferation involved in immune response      
- response to glucose starvation    

## Time series with individual crab RNAseq data attempts: 

Rmd: [scripts/DESeq-time-series.Rmd](https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-time-series.Rmd)      

.HTML: [scripts/DESeq-time-series.html](https://htmlpreview.github.io/?https://github.com/RobertsLab/paper-crab/blob/master/scripts/DESeq-time-series.html)

To Do for time series:       
- try to figure out how to plot gene counts of crab ABC over time      
- Gene list for ABC vs GHI (I think I have this... but I think because it's two temperatures at two time points, I have to do what I did above for libraries 8 -11 where I do the initital deseq, and then do a contrast to get the final gene list)





