---
layout: post
title: DNA-free, Qubit, and Bioanalyzer Plan; Kallisto work
date: '2019-11-07'
category: bairdi
tags: [Qubit, DNA-free, CrabMtg, Kallisto, Bioanalyzer]
---
Today we came up with a plan to address the issues that came up with the weird bioanalyzer results from yesterday (GitHub Issue #[792](https://github.com/RobertsLab/resources/issues/792)). I also got some help with kallisto and am working on getting some analysis done for looking at differential expression (hopefully have some new results for GSS talk next week). 

### Weird Bioanalyzer results from yesterday
#### Yesterday's post: [here](https://grace-ac.github.io/bairdi-nanodrop-bioanalyzer-kallisto/)

#### What could be happening?   
- We know reagents work becaue I ran a plate with just the reagents, and all looked good
- We know there's RNA in my samples because I have detectable RNA from the Qubit RNA HS Kit (only will show RNA results)
- The NanoDrop results also looked good
- The elution substance for all samples was RNase-free water (0.1% DEPC-treated water), so it's likely not the elution substance

It could be that there is DNA in the samples that is screwing up the Bioanalyzer's ability to read the RNA. A way to figure out if that's the case was come up with during today's meeting:    
1. Run 4 of the samples that I ran on the Bioanalyzer yesterday on the Qubit using the dsDNA HS Kit 
2. Use the Turbo DNA-free Kit on those same four samples to get rid of DNA
3. Run those same four samples on the Bioanalyzer (hoping to see JUST the RNA at that point)
4. Re-run those samples on the Qubit using the dsDNA HS Kit to see if there's still any DNA

### I ran 2ul of 4 samples on Qubit using dsDNA HS Kit
#### Results:    

| Run ID            | Assay Name             | Test Name             | Test Date     | QubitÆ tube conc. | Units | Original sample conc. | Units | Sample Volume (µL) | Dilution Factor | tube_number |
|-------------------|------------------------|-----------------------|---------------|-------------------|-------|-----------------------|-------|--------------------|-----------------|-------------|
| 2019-11-07_164551 | dsDNA High sensitivity | Sample_#191107-164649 | 11/7/19 16:46 | 23.4              | ng/mL | 2.34                  | ng/µL | 2                  | 100             | 53          |
| 2019-11-07_164551 | dsDNA High sensitivity | Sample_#191107-164640 | 11/7/19 16:46 | 93.2              | ng/mL | 9.32                  | ng/µL | 2                  | 100             | 24          |
| 2019-11-07_164551 | dsDNA High sensitivity | Sample_#191107-164630 | 11/7/19 16:46 | 220               | ng/mL | 22                    | ng/µL | 2                  | 100             | 29          |
| 2019-11-07_164551 | dsDNA High sensitivity | Sample_#191107-164616 | 11/7/19 16:46 | 155               | ng/mL | 15.5                  | ng/µL | 2                  | 100             | 10          |

#### Next steps:   
- Use the [Turbo DNA-free Kit](https://assets.thermofisher.com/TFS-Assets/LSG/manuals/1907M_turbodnafree_UG.pdf) on those 4 samples 

Will do that tomorrow. Then will follow with the Bioanalyzer, and re-run on Qubit with dsDNA HS Kit. 

I'm hoping there's enough of the samples left to do all of this! 

Here's how much volume I think is in those 4 samples:   
- Started with 15ul of eluted RNA in RNase-free water
- Used 2ul of each sample on Qubit with RNA HS Kit (now 13 ul)
- Used 1ul **3 separate times** to run on the Bioanalyzer (now 10ul) 
- Used 1ul of each on the NanoDrop (now 9ul) 
- Used 2ul of each on the Qubit with the dsDNA HS Kit (now 7ul) 

I will use 1ul of each on the Bioanalyzer after using the DNA-free kit, then will use 2ul of each sample on the Qubit with the dsDNA HS Kit. I will end up with ~4ul... I will definitely have to re-extract RNA from those samples. LUCKILY I have plenty of hemolymph in the freezer for those samples left :) . 

### Kallisto
I showed my notebook for using kallisto and the error that I was getting. It kept saying something about how it needs to have an even number of files to work with, but that I was giving it an odd number... 

Turns out the ACTUAL problem was that I had wrote "-out" in the code, where I should have written "-o" OR "-output"... 

Anyway, it works now ([2019-11-06-bairdi-kallisto.ipynb](https://github.com/RobertsLab/project-crab/blob/master/notebooks/2019-11-06-bairdi-kallisto.ipynb)), but I'll have to run this on a more powerful computer, because my laptop will not be able to handle it. And the way I have my notebook now, it'd be using the samples from owl, which would require wifi connection, and would further decrease the speed. 

I'm trying to figure out which computer I should use, or if I should just try to figure out how to make an .sh script (which I wouldn't really know how to start) and run it on Mox. 

I need to make decisions soon because my talk for GSS is next Thursday at 1:30pm! 


