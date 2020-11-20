---
layout: post
title: Create list of Trinity_IDs associated with GOslim "Stress response" from annotated crab transcriptome
date: '2020-02-27'
category: bairdi
---
Today I made a list of Trinity_IDs that are associated with the GOslim term "stress response" from the annotated crab transcriptome. I also clean up a few things in the project-crab/analyses repo... kind of. 

## Getting list:

Used this Rmd: [042720-get_crab-stress_response-genelist.Rmd](https://github.com/RobertsLab/project-crab/blob/master/scripts/042720-get_crab-stress_response-genelist.Rmd)

"stress response" Trinity ID list: [crab_stress-response-genes.tab](https://github.com/RobertsLab/project-crab/blob/master/analyses/crab_stress-response-genes.tab)    
Not sure if I should `join` the above list with other information to make it more useful. Will ask in lab meeting tomorrow. 

## cleaning up a `project-crab` repo a little:
Move some files around, made a new directory in `analyses` for `BLAST` files: [analyses/BLAST_to_GOslim](https://github.com/RobertsLab/project-crab/tree/master/analyses/BLAST_to_GOslim) 

## other crab project related things:
- still looking up more about macropinocytosis and what it could mean that it's enriched in infected crabs
- editing and adding more to the [crab paper](https://docs.google.com/document/d/1xZjT_2ix39jhFGhPjUqjOIubCEZfnl9yDddIjR3nY38/edit)
