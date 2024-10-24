---
layout: post
title: Writing Retreat Day 2 and 3
date: '2024-10-23'
categories: [pycno]
---
Writing Retreat Days 2 and 3. Chatted with Steven - new goals for results section to focus on, and goals for blocking out chunks for the paper. Writing in notebook post and will include which ones have been done, and will provide updates on progress in Friday's notebook post.

# Goals

Overall:        
This week --> methods      
Next Week --> results      
Following Week --> discussion       

Draft complete by --> Nov 8 (or Nov 11/12... because WSN is Nov 7-10).

Specific:   
1. Finish methods section of paper. Will discuss with Steven this Friday.
2. Results: Shared DEG list between 2021 and 2022 ([4,114 DEGs](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_same_2021-2022.tab)) - enrichment - look at processes with Benjamini <0.05... and get genes related to them (using uniprot accession IDs). Here's some information about what Bejamini is - the Benjamini-Hochberg Procedure: [Multiple Tests, Multiple Comparisons](https://stats.libretexts.org/Bookshelves/Applied_Statistics/Biological_Statistics_(McDonald)/06%3A_Multiple_Tests/6.01%3A_Multiple_Comparisons)
3. Annotations: re-do using uniprot table downloaded from uniprot.org with the GO BP terms... I currently only have a table with GO IDs... but terms would be more helpful to get at bigger categories. Also, get my annotations `join`-ed with the interproscan.tsv annotation from the published genome from [dryad](https://datadryad.org/stash/dataset/doi:10.5061/dryad.51c59zwfd).
4. GitHub Issue to ask for getting GO Slim terms from the 4,114 DEGs. GitHub Issue: [#1989](https://github.com/RobertsLab/resources/issues/1989)
5. GitHub Issue: assign to Steven - ask for annotation of reads that don't map to sea star from libraries from 2021 - include link to 8 control and 8 exposed libraries.

## More info on results section goals:
Because there's no difference between adults and juveniles immune response, focusing in on the list of [4,114 DEGs](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_same_2021-2022.tab) that are shared between the two years.

[DAVID enrichment](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/24-2021-2022-enrichment/2021-2022-same-DAVID.txt) --> terms with Benjamini <0.05.          
Get genes related to those terms using uniprot accession IDs.     

Also, annotate DEG list with GO BP terms to get bigger umbrella terms for genes - look for immune related things.     

Flow of results for this:   
1. DEGs (4,114) annotated
- use GO Term (GO Slim?) to get bigger categories of genes... and pick some cool ones to talk about
2. DAVID enrichment (211 terms); 9 terms with Benjamini <0.05   
3. Get genes for those 9 terms (use uniprot accession ID) from the DEG list


# October 23, 2024 - Finding Cool Genes
Old stuff... won't be used but writing in notebook because I did it yesterday. Will not be keeping these files or using them... but they exist so here's what they are:

## Summer 2021
https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/24-2021-2022-enrichment/2021-bonferroni-genes-immune-only.txt

Genes from https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/24-2021-2022-enrichment/2021-Bonferroni_genes_from_1_significant.txt that have functions related to immune response. Found by searching genes in uniprot.org and reading descriptions.
