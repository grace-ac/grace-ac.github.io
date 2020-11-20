---
layout: post
title: 6 pooled Crab RNA samples - unsuccessful concentration with Zymo RNA Clean and Concentrator Kit -5
date: '2020-01-10'
category: bairdi
tags: [RNA, concentration, qubit]
---
Today I tried to concentrate the 6 pooled crab RNA samples. Long story short, a lot of RNA was lost in the process and the "concetrated" samples are now well below the requirements for NWGC for RNAseq. Details in post. Next steps, I'm going to extract more RNA from samples from Day 9 so we can bulk those pools up if we want to try to send them to NWGC still. Then I'll extract more RNA from samples that will bulk up the other pools, too. 

## 6 pooled samples
The initial RNA concentrations for the 6 pooled samples are: (post: [here](https://grace-ac.github.io/pooled-6-new-samples/))     

| trtmnt_tank | day | infection_status | total-yield_ng | elution_vol | vol_for_pool | total_vol_ul | qubit_vol_ul | qubit_sample_ng | total_ng_RNA_pool | final_sample_vol |
|-------------|-----|------------------|----------------|-------------|--------------|--------------|--------------|-----------------|-------------------|------------------|
| NA          | 9   | 0                | 287.3          | 13          | 4.977375566  | 52.65550411  | 2            | 21              | 1063.765586       | 50.65550411      |
| NA          | 9   | 1                | 305.5          | 13          | 4.680851064  | 57.13842355  | 2            | 21.5            | 1185.476106       | 55.13842355      |
| cold        | 12  | 0                | 412.1          | 13          | 3.470031546  | 51.61757335  | 2            | 23.6            | 1170.974731       | 49.61757335      |
| cold        | 12  | 1                | 280.8          | 13          | 5.092592593  | 39.22471819  | 2            | 27.2            | 1012.512335       | 37.22471819      |
| warm        | 12  | 0                | 380.9          | 13          | 3.754266212  | 40.86453844  | 2            | 26.9            | 1045.456084       | 38.86453844      |
| warm        | 12  | 1                | 230.1          | 13          | 6.214689266  | 41.00446376  | 2            | 26.3            | 1025.817397       | 39.00446376      |

## NWGC requirements
They require normalized at least 1.5 micrograms (15000 ng) of RNA. Each sample should be concentrated to 50ng/ul of RNA. Each sample should be eluted (normalized) in at least 30ul of TE. 

# Attempt at concentrating
Earlier in the week I tried concentrating two test pools that I made. Post: [here](https://grace-ac.github.io/concentrate-test-pools/). I made a mistake because I diluted the test pools before running 2ul on the qubit, so I didn't have a baseline idea of how much RNA was in the samples. 

### Today's attempt
I know the conenctration and volume of all the samples (in table above). 

Because there was a sample that had 55.14ul in it, I decided to normalize them all to 60ul by adding RNAse-free water. 

Then I went through the protocol as described.     
1. Add 100ul of RNA Binding Buffer to each sample. Mix by pipet. (Current volume now 160ul).    
2. Add 1 volume (160ul) of 100% ethanol. Mix by pipet. Transfer to a Zymo-Spin IC Column (provided). Centrifuge at 10,000 g for 30s. Discard flow-through.    
3. Add 400ul of RNA Prep Buffer to the column. Centrifuge 10,000g for 30s. Discard flow-through.     
4. Add 700ul of RNA Wash Buffer to the column. Centrifuge 10,000g for **2 minutes**. Discard flow-through. Transfer column to labeled RNAse-free microcentrifuge tube.     
5. Add 35ul of TE to the column. Centrifuge 10,000g for 2 minutes. RNA is now eluted in the TE.      

#### Qubit results
I ran 2ul of each sample on the qubit using RNA HS Kit.     
The concentrations were wayyyy too far below the required 50ng/ul. And each sample lost RNA, some more than others. :(

| Day | Infection status | Temperature | RNA ng/ul in 2ul | Total RNA in sample ng (33ul of sample remaining) |
|-----|------------------|-------------|------------------|---------------------------------------------------|
| 9   | 0                | NA          | 15.7             | 518.1                                             |
| 9   | 1                | NA          | 17.6             | 580.8                                             |
| 12  | 0                | cold        | 24.9             | 821.7                                             |
| 12  | 1                | cold        | 26.0             | 858                                               |
| 12  | 0                | warm        | 26.0             | 858                                               |
| 12  | 1                | warm        | 24.4             | 805.2                                             |

# Next steps
On Tuesday, January 14th I'll extract RNA from another set of 24. I'll focus on Day 9 infected and uninfected again, so that if we want to bulk up those 6 pooled samples with more RNA to send to NWGC, we can. 
