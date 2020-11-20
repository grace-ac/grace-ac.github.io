---
layout: post
title: 2015 Oysterseed Plan and Crab Meeting Notes
date: '2018-12-06'
tags: [bairdi, 2015Oysterseed]
---
Crab Meeting today: shared current status of what we've got (FISH546 [grace-Cbairdi-transcriptome](https://github.com/fish546-2018/grace-Cbairdi-transcriptome)). Additionally, we had a proteomics meeting today and I got some input on next steps for the DIA: set some stringent thresholds, MS Stats, make some tables, etc. I will make a separate post on what I did (protocol) tomorrow as I work with the data. Today's post will just include a general outline of what I have and next steps. 

## Crab Meeting
(Will edit and publish within the next couple of days)

Shared my current status of transcriptome annotation and basic analyses (FISH546 [grace-Cbairdi-transcriptome](https://github.com/fish546-2018/grace-Cbairdi-transcriptome)). 

Steven and Sam were both surprised by the taxonomy pie chart, specifically that there were ~2500 taxonomic groups identified. ([Rscript](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/scripts/taxa_breakdown.R); ([data_set_from_Steven](http://gannet.fish.washington.edu/seashell/bu-mox/analyses/1114b/cg-trinity-nt.tab)). I will go back and investigate which transcriptome was used, and also make clear that there are two different fasta files: one from the practice assembly using the tiny .fastq files; one from the true assembly on Mox. 

I also am going to get some more BLAST jobs running as we wait for the Bioanalyzer to be fixed (after which I can hopefully continue with RNA extractions if results look good). 

## 2015 Oysterseed Proteomics Chat
What I have (finally!): 
I have some *.elib.peptides.text files, which are the quant files from the DIA. 

**(Tomorrow's post will be dedicated to the DIA protocol I used.)** 

What I will do:
I will set a stringent threshold and use MS Stats, take a rough look at the data. Make a table. Emma said she'll be available to help if (when) I get stuck. 

I also need to make sure I can identify the proteome I used. I know where it is, but I'll include it in tomorrow's post with the protocol. 

