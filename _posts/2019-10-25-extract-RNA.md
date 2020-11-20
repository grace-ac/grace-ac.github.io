---
layout: post
title: Crab RNA extractions with Qubit results
date: '2019-10-25'
category: bairdi
tags: [Zymo, RNAisolation, Qubit]
---
Today I ran 2ul of the 24 samples I extracted yesterday. 20 out of 24 had RNA. Details in post. 

### Prep
Labeled tubes
- 24 RNase-free snap cap tubes (for preparing the 35ul sample)
- 24 RNase-free snap cap tubes (with C. bairdi RNA, tube number, and date)
- 24 yellow zymo spin column lids (**Next time also label collection tube**)
- 24 clear zymo spin column lids

Grabbed 100% ethanol in a 15ml tube, and RNase-free water in a 15ml tube. 

P1000, P200, P20 and tips

### Sample prep
Tubes I grabbed:    

| status     | tube number |
|------------|-------------|
| infected   | 15          |
| infected   | 133         |
| infected   | 144         |
| infected   | 81          |
| infected   | 101         |
| infected   | 27          |
| infected   | 163         |
| infected   | 109         |
| infected   | 103         |
| infected   | 62          |
| infected   | 8           |
| infected   | 19          |
|            |             |
| uninfected | 91          |
| uninfected | 10          |
| uninfected | 119         |
| uninfected | 32          |
| uninfected | 53          |
| uninfected | 48          |
| uninfected | 34          |
| uninfected | 121         |
| uninfected | 108         |
| uninfected | 111         |
| uninfected | 50          |
| uninfected | 41          |


1. Let pelleted hemolymph thaw, then vortexed for a second.
2. Transfered 35ul of the slurry to a labeled snap cap tube (some tubes (27, 62, 19) only contained ~35ul, whereas other tubes still had a lot left). 
3. Added 35ul of RNase free water
4. Added 280 ul Lysis buffer 
5. Mixed all 350ul of liquid by vortexing. 

### Purification
1. Transfered 350ul of sample into yellow spin column.
2. Spun 10,000 g 30s. 
3. Saved DNA on the column for later. (Put in -20C on labeled tube rack in FTR 209)
4. Saved flowthrough with RNA and continued
5. Added 350ul 100% ethanol and pipet to mix.
6. Transfer all 700ul to clear spin column. 
7. Spun 10,000 g 30 s. 
Discard flow-through

At the end of Step 7, there was white crystal-y stuff in tubes 144, 8. 

8. Added 400ul DNA/RNA prep buffer. Spun 10,000g 30 s

At end of Step 8, tubes 15, 10, 53, 121 still had some liquid on the column

9. Add 700 ul DNA/RNA wash buffer. Spin 10,000 g 30s 

At end of step 9, 163, 10, 121, still had liquid on column. Spun these again at 10,000 g 30 s. Then they were fine. 

10. Added 400 ul DNA/RNA wash buffer. Spin 10,000 g 2 minutes. Transfered column to fully labeled RNase-free snap caps.
11. Added 15ul RNase-free water to column matrix and let sit for 5 minutes. Spun to elute 10,000 g 2 minutes.

Put samples in -80C over night becuase I left. 

### Qubit
Ran 2ul of each sample on Qubit. 

20/24 samples had RNA. 

[Link to data](https://docs.google.com/spreadsheets/d/16zarY-NZnyrlKN69chKfSraMnVi3OFzlwDytWGx5NZ0/edit?usp=sharing) 

| qubit_tube_conc_ng.ml | original_sample_conc_ng.ul | sample_vol_ul | dilution_factor | tube_number | extraction_method | ul_sample-used | elution_vol_ul | total-yield_ng |
|-----------------------|----------------------------|---------------|-----------------|-------------|-------------------|----------------|----------------|----------------|
| 39.5                  | 3.95                       | 2             | 100             | 41          | Zymo_microprep    | 35             | 15             | 51.35          |
| 126                   | 12.6                       | 2             | 100             | 50          | Zymo_microprep    | 35             | 15             | 163.8          |
| 200                   | 20                         | 2             | 100             | 111         | Zymo_microprep    | 35             | 15             | 260            |
| 136                   | 13.6                       | 2             | 100             | 108         | Zymo_microprep    | 35             | 15             | 176.8          |
| 62.3                  | 6.23                       | 2             | 100             | 121         | Zymo_microprep    | 35             | 15             | 80.99          |
| 78.4                  | 7.84                       | 2             | 100             | 34          | Zymo_microprep    | 35             | 15             | 101.92         |
| 31                    | 3.1                        | 2             | 100             | 48          | Zymo_microprep    | 35             | 15             | 40.3           |
| 155                   | 15.5                       | 2             | 100             | 53          | Zymo_microprep    | 35             | 15             | 201.5          |
| Out of range          | Out of range               | 2             | 100             | 32          | Zymo_microprep    | 35             | 15             | #VALUE!        |
| 249                   | 24.9                       | 2             | 100             | 119         | Zymo_microprep    | 35             | 15             | 323.7          |
| 293                   | 29.3                       | 2             | 100             | 10          | Zymo_microprep    | 35             | 15             | 380.9          |
| 148                   | 14.8                       | 2             | 100             | 91          | Zymo_microprep    | 35             | 15             | 192.4          |
| 54.5                  | 5.45                       | 2             | 100             | 19          | Zymo_microprep    | 35             | 15             | 70.85          |
| 160                   | 16                         | 2             | 100             | 8           | Zymo_microprep    | 35             | 15             | 208            |
| Out of range          | Out of range               | 2             | 100             | 62          | Zymo_microprep    | 35             | 15             | #VALUE!        |
| 160                   | 16                         | 2             | 100             | 103         | Zymo_microprep    | 35             | 15             | 208            |
| 37.6                  | 3.76                       | 2             | 100             | 109         | Zymo_microprep    | 35             | 15             | 48.88          |
| 163                   | 16.3                       | 2             | 100             | 163         | Zymo_microprep    | 35             | 15             | 211.9          |
| Out of range          | Out of range               | 2             | 100             | 27          | Zymo_microprep    | 35             | 15             | #VALUE!        |
| 41.8                  | 4.18                       | 2             | 100             | 101         | Zymo_microprep    | 35             | 15             | 54.34          |
| 310                   | 31                         | 2             | 100             | 81          | Zymo_microprep    | 35             | 15             | 403            |
| 143                   | 14.3                       | 2             | 100             | 144         | Zymo_microprep    | 35             | 15             | 185.9          |
| 235                   | 23.5                       | 2             | 100             | 133         | Zymo_microprep    | 35             | 15             | 305.5          |
| Out of range          | Out of range               | 2             | 100             | 15          | Zymo_microprep    | 35             | 15             | #VALUE!        |


**Extracted RNA is in [-80, Rack 7, col 3, row 4](https://docs.google.com/spreadsheets/d/1Qsvz3QTURlPF_hX05BQxjom3484WuMfqQ1ILl9LEljU/edit#gid=2006985773)**

(Put remaining hemolymph pellet tubes in Rack 8, column 3, row 5 in -80 (the nearly empty box from first day sampling tubes)).
