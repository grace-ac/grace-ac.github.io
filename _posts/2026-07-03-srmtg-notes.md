---
layout: post
title: Post-Steven Meeting Notes and Current To-Dos
date: '2026-07-03'
categories: [SRMtg]
---
Post with post-meeting notes and to-dos before I meet with Steven again next Wednesday. 

# Meeting notes: 
I showed him the figures I made of the orthogroup GOslims for each species proportional to the orthogroups shared by all three (post [here](https://grace-ac.github.io/OrthoFinder_results/)) and the orthogroup GOSlims for Day 12 DEGs for each species proportional to the orthogroups shared by all three (post [here](https://grace-ac.github.io/Musp_degs-orthogroups/)). 

We looked at the _P. helianthoides_ figures side-by-side and didn't see any huge differences, except that there was programmed cell death in the figure for Day 12 DEGs that didn't show up in the orthogroup GOSlims figure. 

# Next step: 
_Enrichment_       
Use DAVID to get enrichment for each species. The background will be the uniprot accession IDs for the list of shared orthogroups across all species, and the gene lists will be the uniprot accession IDs for the orthogroups that are unique to each species and associated with the Day 12 DEGs. 

Using the shared orthogroups as a background allows for the comparison across species since we can't run `DESeq2` on the three species together due to their having different genomes that they are aligned to. 

_Combined figure_    
Also, would be helpful to combine the figures mentioned above into one figure. 


