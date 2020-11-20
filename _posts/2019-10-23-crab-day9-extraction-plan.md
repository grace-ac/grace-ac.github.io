---
layout: post
title: Notes on protocol and plan for Crab Project extractions - use info from Sam's notebook posts
date: '2019-10-23'
category: bairdi
tags: ZymoRNA
---
This post contains my notes on the [Zymo Research Protocol for Quick-DNA/RNA Microprep kit](https://github.com/RobertsLab/resources/blob/master/protocols/Commercial_Protocols/ZymoResearch_quick-dna-rna_microprep_plus_kit_20190411.pdf), and [Sam's notebook post](https://robertslab.github.io/sams-notebook/2019/04/30/RNA-Isolation-and-Quantification-C.bairdi-Hemolymph-Pellet-in-RNAlater.html) to create a protocol for extracting RNA. I also include my extraction plan for this next week as I try to get enough RNA to get two more libraries (Day 9 infected (1), and Day 9 uninfected (2)). 

## Sample extraction plan:   
Remaining Day 9 sample tubes (reminder: no temperature treatments were happening on Day 9):     
- 39 uninfected (21 are listed as "M" for "mature")         
- 49 infected (all are "I" for "immature")       

I will start out by extracting 12 infected and 12 uninfected samples on my first extraction day (**Thursday, 10/24/19**). I will use the Qubit to keep track of the yields. 

The next day I'll do another 12 infected and 12 uninfected samples (**Friday, 10/25/19**). If there are still not high enough RNA yields, I'll do another round of extractions of 12 infected and 12 uninfected (**Friday, 10/25/19**). 

Hopefully by next week I'll have the ability to create two pooled libraries for Day 9: (1) infected Day 9, and (2) uninfected Day 9. 

## Protocol plan: 
(From [Zymo Research Protocol for Quick-DNA/RNA Microprep kit](https://github.com/RobertsLab/resources/blob/master/protocols/Commercial_Protocols/ZymoResearch_quick-dna-rna_microprep_plus_kit_20190411.pdf) and [Sam's notebook post](https://robertslab.github.io/sams-notebook/2019/04/30/RNA-Isolation-and-Quantification-C.bairdi-Hemolymph-Pellet-in-RNAlater.html))               
My samples are crab hemolymph (and _Hematodinium spp._) cells. The samples were originally stored in RNAlater, then in Winter 2018, I spun them down, and saved the supernatant in other sample tubes. 

### Prepping reagents (Only have to do if I open a new kit) 
1. Add 96 ml 100% ethanol (or 104ml 95% ethanol) to the 24 ml **DNA/RNA Wash Buffer** concentrate
2. Add 275 ul **DNase/RNas-Free Water** per vial to reconstitute the lyophilized **DNase I** at 1 U/ul. Mix by gentle inversion. Store frozen aliquots at -20C. 
3. Add 1040 ul **Proteinase K Storage Buffer** per vial to reconstitute the lyophilized **Proteinase K** at 20 mg/ml. Vortex to dissolve. Store at -20C. 

### Sample preparation: 
Cells are already "pelleted".      
1. Transfer 35 ul of slurry to a microcentrifuge tube (vortex first).    
2. Add 35 ul of RNase-free water.
3. Add 140 ul of **DNA/RNA Lysis Buffer** and mix.     
In total, tube contains 210 ul of liquid

### Purification: 
1. Transfer sample to a **Zymo-Spin IC-XM Column** in a **Collection Tube** and centrifuge (10,000 g for 30 sec). **SAVE FLOW-THROUGH**
2. Add an equal volume (210 ul) of ethanol (95% or 100%) to the flow through and mix well. Transfer to a **Zymo-Spin IC Column** in a **Collection Tube** and centrigure (10,000 g for 30 sec). _Discard flowthrough_.
3. Add 400 ul **DNA/RNA Prep Buffer** to the column and centrifuge (10,000 g 30 sec). _Discard the flowthrough_. 
4. Add 700 ul **DNA/RNA Wash Buffer** and centrifuge (10,000 g 30 sec). _Discard flowthrough_. 
5. Add 400 ul **DNA/RNA Wash Buffer** and centrifuge 10,000 g for 2 minutes to ensure the removal of the wash buffer. Carefully transfer column into a clean microcentrifuge tube. 
6. Add 15 ul **DNase/RNase-Free Water** directly to the column matrix. Let stand for 5 minutes, then centrifuge (10,000 g 30 sec) to elute RNA from column. 

### RNA quantification:
Use 1 ul on the Qubit to quantify RNA.   
Place remainder of sample into -80 C.

### Spreadsheet:   
Save Qubit results, input sample tube numbers, add date to [master-qubit.xlsx](https://github.com/RobertsLab/project-crab/blob/master/analyses/master-qubit.xlsx), then `join` [sample_table.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/sample_table.csv) using this R script ([081919-sample-qubit-master.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/081919-sample-qubit-master.Rmd)). This will update the master qubit sample spreadsheet: [master-qubit-sample.csv](https://github.com/RobertsLab/project-crab/blob/master/analyses/master-qubit-sample.csv).
