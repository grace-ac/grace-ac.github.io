---
layout: post
title: Summer 2022 Data Entry, Summer 2021-2022 Work, Multi-Species RNAseq Update
date: '2024-10-02'
categories: [pycno]
---
Updates on data entry for 2022; summer 2021-2022 analyses, and Multi-species RNA sequencing.

# Data Entry
I finished my share of data entry for 2022!!! Feels really good to have that finally off my task list. Melanie and Alyssa are finishing up their share soon.

# Summer 2021 - 2022 Analyses
Converting the .sam files to .sorted.bam files... It said it was complete, so I checked:

```
ls ../analyses/20-hisat2/*sorted.bam | wc -l
```
And got 20 returned... it should be 32!

I double checked there were 32 .sam files.

So I'm re-running the .sam to .sorted.bam file code chunk.

## Writing retreat
Myself, Melanie, and Alyssa will be going on a writing retreat to Quadra to stay at the Hakai station up there! We'll be up there Oct 20-24, and will be focusing on writing. Byt then, my goal is to at the VERY LEAST have my analyses for this first paper completed and results figured out.


# Summer 2023 - Multi-Species RNA Sequencing Update
I got an email that sequencing has been completed! The data is being uploaded to their server and I'll get a notification once that is complete, and I'll transfer it over to us!

They did provide one note for one of the samples:   

"Sample PSC-0559 did not meet our internal specifications and is undergoing additional review and sequencing."

Sample PSC-0559 is from a leather star. This is interesting and I wonder what their internal specifications are because that sample was not listed as being one of the low-RNA potential-problem samples... and that star had ~118ng RNA/ul of sample... which is a lot... totaling ~1,652 ng of RNA in the whole sample.

I hope that all goes well and I'm curious what their specifications are.
