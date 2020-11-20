---
layout: post
title: Crab RNA-Seq thoughts; Merging columns in R
date: '2018-08-16'
categories: bairdi
tags: Crabproject, RNASeq, R
---
Yesterday I shared some preliminary thoughts (in a GitHub issue and detailed below) on what we can do for our first Crab RNA-Seq library. Today I learned - through a whole mess of comments on a GitHub Issue because my stuff isn't organized well - how to merge data in columns that are the same in R, so that you don't have duplicates (example: "Test_Date.x" and "Test_Date.y"). Steven mentioned I should go over with him how to name files... which sounds good to me because I think I'm taking too much time out of my day renaming and replacing files as I update them. Sam also mentioned that my R Project is difficult to work with because it includes files that belong to two different repositories. So I'll work on cleaning that up and making it easier for future collaboration and help. 

## Crab RNA-Seq plan thoughts
GitHub Issue [#346](https://github.com/RobertsLab/resources/issues/346)    
## **For a library using UW CORE, need 1000 ng RNA in 50ul sample.** 

**Gave Sam 40 samples from Day 26. From each of the following groups:**  
uninfected, cold (11)
infected, cold (10)
uninfected, ambient (9)
infected, ambient (10)
(gave uninf. cold instead of uninf. amb. for one sample. not 10 per treatment). 

**Of those 40, 15 had quantifiable RNA (Qubit RNA HS):**
uninfected, cold: 5/11
infected, cold: 5/10
uninfected, ambient: 3/9
infected, ambient: 2/10

**Below is a screenshot of just those 15 samples along with their volume (he resuspended them in 10ul H2O) and their total sample yield (total volume * original sample volume):**
![20180815-samps-from-sam](https://user-images.githubusercontent.com/14934314/44165821-9ae7b500-a07e-11e8-9251-ad50a5d3b7ea.png)

**Total RNA (ng) for each treatment group:** 
![20180815-total-rna-per-trtmnt](https://user-images.githubusercontent.com/14934314/44166757-10ed1b80-a081-11e8-9c8c-7d7006ff91f1.png)

Some preliminary thoughts of mine so far:       
From these 15, we could:     
- combine all 15 samples (1560.8 ng RNA)
- combine the cold treatment together (1200.8 ng RNA)

Combining the infected cold and infected ambient is very close to 1000ng (954 ng RNA).

We can try isolating RNA using the Qiagen Kit from the second tubes taken in triplicate and then hopefully have more than enough

## Merging column data in R
GitHub Issue [#349](https://github.com/RobertsLab/resources/issues/349)    
### **The problem:**    
I added the Qubit RNA HS results from the 40 samples Sam processed. I did this by "left_join" by the tube_number with the [20180813-all-hemo-with-Qubit.csv](https://raw.githubusercontent.com/RobertsLab/project-crab/master/data/20180813-all-hemo-with-Qubit.csv).

However, it added repeat columns (I deleted the ones that aren't important):     
![screen shot 2018-08-16 at 11 55 58 am](https://user-images.githubusercontent.com/14934314/44229016-9fc66a80-a14b-11e8-8c95-a378b2c00082.png)

Is there a way in R to merge information in "Test_Date.x" with "Test_Date.y" and "Original_sample_conc_ng.ul.x" with "Original_sample_conc_ng.ul.y" so that there aren't repeats. I'll have to keep adding more Qubit information as isolations continue. 

### **The solution:**    
```merge(x = hemoqub, y = qSam, by = c("tube_number", "Test_Date", "Original.sample.conc."), all.x = TRUE)```

### Notes from Sam and Steven    
From @kubu4     
```Heads up, this is a bit difficult to work with because your script is traversing multiple repos (e.g. ../project-crab/data ; I don't have a project-crab folder on my computer, so I can't get to those files using your script).```

```Personally, I think you should do all of this work in a single repo - that would eliminate these issues. However, if you want to work with two repos, you should make some changes:```

```Use the download.file() function to download data files from other repos.```    
```Or,```

```Add information to repo README.md files that explain that this repo depends on the other and provide link and/or cloning instructions for that other repo.```

From @sr320    
```We should talk about file naming also- let’s go over this tomorrow```

### Things I need to do:   
- Learn better method of naming files and updating them
- Make collaboration in R projects more user-friendly by either putting everything in one repo, or being very clear about downloading files from other repos
- Make sure everything is ready for collaboration BEFORE I make a GitHub issue asking for help
