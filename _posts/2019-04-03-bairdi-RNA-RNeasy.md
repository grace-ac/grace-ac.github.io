---
layout: post
title: RNeasy Kit Extraction with 12 samples - RNA in 1/12
date: '2019-04-03'
category: bairdi
tags: [RNeasy, RNAisolation]
---
Today I did the RNeasy Plus Micro Kit protocol (without the vacuum) on 12 samples (taken from the 24 that I did last time). Of the 12, only 1 had detectable RNA. The rest were all "Out of Range: TOO LOW". Details in post below. 

### Preparation
Labeling:    
12 RNase-free snap caps     
12 QIA shredder      
12 gDNA spin columns     
12 RNA MinElute columns (did these right before use because they need to be kept in fridge)     
12 snapcaps for the eluted RNA     

Solutions:    
70% ethanol: 7ml ethanol + 3ml DEPC-treated H20     
80% ethanol: 5.2ml ethanol + 1.3ml DEPC-treated H20     
Buffer RLT + B-ME: 4.5ml Buffer RLT + 45ul B-ME    

### Prepping samples

| Tube number | Sample Day | Infection status | Temp trtmnt |
|-------------|------------|------------------|-------------|
| 135         | 9          | 0                | NA          |
| 90          | 9          | 1                | NA          |
| 317         | 12         | 0                | Amb         |
| 352         | 12         | 1                | Amb         |
| 242         | 12         | 0                | Cold        |
| 234         | 12         | 1                | Cold        |
| 285         | 12         | 0                | Warm        |
| 271         | 12         | 1                | Warm        |
| 499         | 26         | 0                | Amb         |
| 468         | 26         | 1                | Amb         |
| 458         | 26         | 0                | Cold        |
| 438         | 26         | 1                | Cold        |



Let the samples thaw. Vortex for 15s. Sample out 15ul of the slurry into new snap cap labeled tubes.   

These samples are 12 of the ones that I used last time ([March 19, 2019](https://grace-ac.github.io/24sample-RNeasy-extraction/)).

### Protocol
1. Added 350ul of Buffer RLT Plus + B-ME solution to both samples
2. Vortex to mix
3. Transfer lysate to QIA Shredder column with 2ml collection tube. Centrifuge 2min at full speed
4. Transfer flow-through to gDNA Elimninator column with 2ml collection tube. Centrifuge for 30s at 12,00 g. Discard column. Save flow-through. 
5. Add 350ul of 70% ethanol. Pipet to mix. Proceed to step 6. 
6. Transfer sample (including any precipitate that may have formed) to RNeasy MinElute column. Close Lid. Centrifuge 20s at 12,000g. Discard flow-through
7. Add 700ul Buffer RW1 to RNeasy column. Close lid. centrifuge 20s at 12,000g. Discard flow-through.
8. 500ul Buffer RPE to RNeasy column. Close lid. Centrifuge 20s at 12,000g. Discard flow-through.
9. Add 500ul 80% ethanol to RNeasy column. Close lid. Centrifuge 2min at 12,000g. Dsicard collection tube and flow-through.
10. Put RNeasy column in new 2ml collection tube. Cut off RNeasy column lid. Keep tube open and centrifuge at full speed for 5min. Discard flow-through.
11. Put RNeasy column in new 1.5 ml collection tube. Add 14ul RNase-free water to center of membrane. Centrifuge at full speed for 1min with cap on. 

### Qubit Results
[Google sheet](https://docs.google.com/spreadsheets/d/1o_BsLhAC0fkzFJ7VtzgUFediy3KueRXkb27flbaxGs8/edit#gid=0) 

Only 1 tube had RNA: sample 135 (4.60 ng/ul with a 1ul sample used on the Qubit RNA HS)   

I saved the samples in the -80 (Rack 7, col 3, row 1) 

### Two days ago: I ran 10ul of the 24 eluted samples on Qubit to see if there was any RNA
GitHub Issue [#636](https://github.com/RobertsLab/resources/issues/636)         
4/24 had RNA. And all 4 had less than 1 ng/ul of RNA in the 10ul sample.          
[Google sheet](https://docs.google.com/spreadsheets/d/1me8cRniPYfM4AUiFo5oO2cS_7km00uroTeMCktiMTFk/edit#gid=0)  

The sample that had RNA today (tube 135) did not have RNA in it when I ran 10ul of the sample on the Qubit two days ago. 

The samples are pretty much done from that extraction, but I saved the tubes anyway in the -80 (Rack 7, col 3, row 1) 

