---
layout: post
title: More tables for 2015 _C. gigas_ seed
date: '2019-04-09'
category: 2015Oysterseed
---
Today I spoke with Steven about what the results are for the 2015 _C. gigas_ seed paper. I made a new annotated table for the 69 differentially abundant (though not significantly) proteins. Edits to paper.

### Annotated table of 60 diff. expressed proteins
I used the [proteins_comp_annot_threshold.csv](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/proteins_comp_annot_threshold.csv) which was made a few days ago from Steven's annotated list, with a set threshold of 2.00 and -2.00 log-2 fold changes. 

I did this in jupyter and R:    
[01-blastp-to-GOslim.ipynb](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/notebooks/01-blastp-to-GOslim.ipynb) (to get GOslim terms for the BLASTp results from Steven)       
[02-detected-prots-annotate-GOslim.ipynb](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/notebooks/02-detected-prots-annotate-GOslim.ipynb) (to get the protein list into a good format with just the columns we want)      
[04-join-annotate-diffexp-prot.R](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/scripts/04-join-annotate-diffexp-prot.R) (to join the GOslim with the protein list)      

The final file: [diffexp-prot-annotated.tab](https://github.com/grace-ac/paper-pacific.oyster-larvae/blob/master/analyses/diffexp-prot-annotated.tab)     
Not super sure why there are so many proteins... I was only expecting to annotate the 69 differentially expressed. I'll have to fix that. 

### Paper updates
[paper](https://docs.google.com/document/d/1OaYNzlOJr5QibCYt8--GMNGvXlzHPR9_daCkNUVkj-U/edit)    
Worked more on edits and clarifications.    

Results that I'll aim to have:     
Phenotype: 
- condense to a few sentences (no graphs)        

Proteomics:     
- MS Stats (not sure if should have as supplemental, or if I should include some in paper)    
- Protein list from MS stats (annotated - GO)
- Protein list of the 69 diff abundant (annotated - GO)
- Maybe a visual (REVIGO?)

