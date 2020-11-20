---
layout: post
title: "Tried some more GO-MWU stuff - not great - switching gears"
date: '2020-04-21'
category: bairdi
tags: GO-MWU
---

Today I tried some more `GO-MWU` stuff, but it didn't really do much. After input at lab meeting, I tried using DAVID first, then GO-MWU... got 1 enriched biological process. Meeting with Steven --> new plan of things to focus on for now (writing, results we have). Details in post. 

### Earlier this morning
Before lab meeting, I tried GO-MWU, modelled after [Zostera-GO_MWU.R](https://github.com/eimd-2019/project-EWD-transcriptomics/blob/master/analyses/GO-MWU/Zostera-GO_MWU.R) from the EIMD FHL 2019 class. Separates the GO enrichemnt into the different categories: biological process (BP), cellular component (CC), and molecular function (MF). 

I also tried it with different input files (`DESeq` 2019 crab data file (all genes, not just DEGs) with continuous measure of significance):      
- log2fc --> [analyses/GO-MWU/2019-crab-ALL-geneID-log2fc.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/GO-MWU/2019-crab-ALL-geneID-log2fc.csv)    
- padj --> [analyses/GO-MWU/2019-crab-ALL-geneID-padj.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/GO-MWU/2019-crab-ALL-geneID-padj.csv)    
- pvalue --> [analyses/GO-MWU/2019-crab-ALL-geneID-pval.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/GO-MWU/2019-crab-ALL-geneID-pval.csv)    

I tested each one by changed the `input` in this script: [analyses/GO-MWU/2019-crab-infection-ALL-GO_MWU.R](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-infection-ALL-GO_MWU.R)    

The results in terms of the identified number of GO terms at 10% FDR differed depending on the significance value used:      
**Molecular Function**     
Using log2fc → 15 GO terms at 10% FDR     
Using padj → 4 GO terms at 10% FDR      
Using pvalue → 8 GO terms at 10% FDR      
**Cellular Component**      
Using lof2fc → 10 GO terms at 10% FDR     
Using padf → 5 GO terms at 10% FDR    
Using pvalue → 4 GO terms at 10% FDR    
**Biological Process**     
Using log2fc → 7 GO terms at 10% FDR     
Using padj → 12 GO terms at 10% FDR    
Using pvalue → 4 GO terms at 10% FDR     

Then, I saved what the results were from using the [analyses/GO-MWU/2019-crab-ALL-geneID-log2fc.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/GO-MWU/2019-crab-ALL-geneID-log2fc.csv) as the input:      
**Result files**     
- Biological process: [analyses/GO-MWU/2019-crab-ALL-GOBP-results.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-ALL-GOBP-results.csv)      
- Cellular component: [analyses/GO-MWU/2019-crab-ALL-GOCC-results.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-ALL-GOCC-results.csv)      
- Molecular function: [analyses/GO-MWU/2019-crab-ALL-GOMF-results.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-ALL-GOMF-results.csv)     

**Trees**     
- Biological procces: [analyses/GO-MWU/2019-crab-infection-GOBP.pdf](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-infection-GOBP.pdf)      
- Cellular component: [analyses/GO-MWU/2019-crab-infection-GOCC.pdf](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-infection-GOCC.pdf)     
- Molecular function: [analyses/GO-MWU/2019-crab-infection-GOMF.pdf](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-infection-GOMF.pdf) 

When I tried with the [analyses/GO-MWU/2019-crab-ALL-geneID-padj.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/analyses/GO-MWU/2019-crab-ALL-geneID-padj.csv) file, which is the continuous measure of significance used by EIMD and the GO-MWU example script, it gave essentially no results, even though it found a few GO terms that were at 10% FDR:    
Result tree: [analyses/GO-MWU/2019-crab-infection-GOBP-padj.pdf](https://github.com/RobertsLab/project-crab/blob/master/analyses/GO-MWU/2019-crab-infection-GOBP-padj.pdf)    
The red and blue colors are missing, and it says that the ratios are zeros... 

### After lab meeting
During lab meeting, a plan for the afternoon was identified:     
1. Put the Uniprot Accession IDs in DAVID to look for enrichment     
2. If enrichment --> go back to `GO-MWU` and use BP     
3. If no enrichment --> try something else... possibly TopGO 

I focused on trying out DAVID.      

Script for creating lsits of uniprot Accession IDs here: [scripts/042120-2019crab-infection-for-DAVID.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/042120-2019crab-infection-for-DAVID.Rmd)    
Basically, I got 2 lists:     
1. Background --> Uniprot Accession IDs from the BLAST output from the entire crab transcriptome    
2. gene list --> Uniprot Accession IDs from the list of 772 DEGs (made by SR) by `join`-ing the DEG list with the crab transcriptome BLAST output to get the Uniprot Acccession IDs.      

I put the gene list Uniprot Accession IDs in DAVID, then the background Uniprot Accession ID list.     

Resulting file for GO_BP_ALL from DAVID --> [analyses/2019-crab-infection-DAVID-output.txt](https://github.com/RobertsLab/project-crab/blob/master/analyses/2019-crab-infection-DAVID-output.txt)    

I then tried `GO-MWU` again, using the padjusted values, and the same thing described above happened. 

Then Steven and I met to discuss next steps. 

### SR crab chat
Steven did the same thing in DAVID as I did, but saved the GOTERM_BP_DIRECT list, which I guess is shorter:     
[/analyses/chart_12EFD.txt ](https://github.com/RobertsLab/project-crab/blob/master/analyses/chart_12EFD.txt)    

Either way, the top line, which is the enriched, is GO:0044351~macropinocytosis, and the only result. 

I'm going to stop playing around with `GO-MWU` for the next few days and instead focus on writing.      

## NEXT STEPS

Tasks for the next couple of days:       
**METHODS**    
- what I can for differential expression, enrichment

**RESULTS**      
- transcriptome results (we have annotated crab transcriptome: maybe may a GOslim plot, list number of genes, etc.) 
- `DESEq` results (SR performed analysis, but I can write results) 
- enrichement result (GO:0044351~macropinocytosis --> look at the genes involved in this, find some resources on what it is)
- mortality (have mort. data! make a visual or something - blurb, whatever for now)

**DISCUSSION**     
- transcriptome results
- enrichment result --> little blurb
- mortality blurb 

