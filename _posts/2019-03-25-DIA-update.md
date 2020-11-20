---
layout: post
title: 2015 DIA Oysterseed Paper Progress
date: '2019-03-25'
category: 2015Oysterseed
tags: [DIApaper]
---
A little bit of progress has been made with the DIA proteomics paper. I am aiming to have the methods section of the paper solidly done by our meeting this Wednesday at 2 pm. 

### Created a paper repo
[https://github.com/grace-ac/paper-pacific.oyster-larvae](https://github.com/grace-ac/paper-pacific.oyster-larvae)

A lot of work needs to be done to organize both the paper's repo and the [project's repo](https://github.com/RobertsLab/project-pacific.oyster-larvae). 

Work in progress.

### Methods developing
Got some input from Steven and Emma on the methods for the [paper](https://docs.google.com/document/d/1OaYNzlOJr5QibCYt8--GMNGvXlzHPR9_daCkNUVkj-U/edit). I'm working on paring down the methods that Rhonda wrote, as well as adding the methods of what I've done. Still adding to it because I'm currently working towards getting the GO and GOslim terms from the Skyline output file so that I can compare the proteins expressed between the two temperature regimes.

### Started using Galaxy
I'm [using Galaxy right now](https://github.com/RobertsLab/project-pacific.oyster-larvae/blob/master/DIA_2015/protocols/04-Galaxy-protocol.md) to run a BLASTp with the newest version of the uniprot-swprot database and the proteome I used in the DIA analysis. 

From the BLAST output file, I'll join that with the GO terms (probably in R or Jupyter... unless that's also something you can do in Galaxy. I'll play around with it once the BLASTp is complete). Then, I'll create some simple Venn diagrams and other basic plots and stats to show what proteins were expressed in general, as well as to compare the two temperatures. Aiming to have this done by the Wednesday meeting as well. 



