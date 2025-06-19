---
layout: post
title: MultiSpecies - Current Status and Summer Goals
date: '2025-06-18'
categories: [MultiSpecies]
---
See post for details on where the multi-species work lies, and what my goals are for this work for the summer.

# Current Analysis Status as of end-of-day June 18
Last thing I did related to this project was aligning the Day 12 exposed RNAseq data for the _P. helianthoides_ and _P. ochraceus_ (see post: [here](https://grace-ac.github.io/MUsp-updates-2/))

There's a bit more that I did since then... namely I attempted to align the _D. imbricata_ RNAseq to the _D. imbricata_ genome. This I cannot share publicly as our collaborators who are letting us have access to their _D. imbricata_ genome have not published the genome yet. It's currently still in a status of being an issue because the matrix is empty (all 0s), but the steps previously show that there are gene and transcript counts. Working to figure this out.

Current status:

- [x] _P. helianthoides_ RNAseq libraries aligned to genome with count matrices     
- [ ] _P. ochraceus_ RNAseq libraries aligned to genome with count matrices*     
- [ ] _D. imbricata_ RNAseq libraries aligned to genome with count matrices*     

* For both _P. ochraceus_ and _D. imbricata_, the final matrices are empty, all 0s... but the previous steps show that there are gene counts, and the alignment rates are good for both species (83.7% - 86.5% for _P. ochraceus_; 83.6% - 88.1% for _D. imbricata_)

## Here's what I did today:
### MUSP-related work:
- Re-familiarized with where I'm at and what next steps are

### Other:
Put together some slides for my guest lecture for the EIMD Short-Course. I'll be zooming in next Monday, June 23rd  at 1pm, and presenting about 30mins of sea star immune stuff to the students. I'll share slides after I present!

# Goals leading up to Wildlife Disease Association Conference (July 27-Aug 1)
- [ ] Extract more RNA and send of for sequencing (see post with timeline: [here](https://grace-ac.github.io/RNA-extractions-multispecies/))      
    i. Note: This RNA data will not  be available in time for analysis for WDA       
- [ ] Fix alignment issue for _P. ochraceus_       
- [ ] Fix alignment issue for _D. imbricata_        
- [ ] Characertize transcriptomes for each species at this time point and this disease stage     
- [ ] Make some cool figures:      
    - [ ] Disease sign progression over time (already made, but see if I want to change anything)      
    - [ ] Days to mortality across the different species      
    - [ ] Any cool gene ontology things (can't be enrichment, because can't do `DESeq2` with no controls yet, but see what my options are)       
    - [ ] Experimental design figure that's cool and pretty    

# Broader Summer Goals for Multi-Species Work
- [ ] Write a draft of the multi-species work    
- [ ] Process new RNAseq data (will receive likely in August)
- [ ] Run differential expression analyses on new data; both time points --> August - September
