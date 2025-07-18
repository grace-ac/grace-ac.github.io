---
layout: post
title: SR Meeting - Agenda, Takeaways, ands How I Did On Last Week's Goals
date: '2025-07-18'
categories: [SRMeet]
---
See post for proposed agenda, how I did from last week's goals, and the new goals for this upcoming week.

# Did I do What I said I would?
Yes.

See post where I listed my goals: [July 8, 2025](https://grace-ac.github.io/SRmeeting-post-notes/)

Aaaaand... yes I did do what I intended to do! See today's earlier post where I link out all the files (note: you will only be able to access the GitHub repository and files if you are a collaborator, as it is currently set to private). Link to post: [July 18, 2025](https://grace-ac.github.io/MUSP-analyses/).

# Agenda for today:
1. Go over the annotations I did    
2. Come up with next steps for results to share at WDA          
3. Come up with target journal to submit Aspen's paper that's currently on biorxiv: [Uncovering Host-Parasite Dynamics: Gene Expression Shifts in Hematodinium-infected Chionoecetes bairdi in Response to Temperature Change](https://www.biorxiv.org/content/10.1101/2025.06.05.658092v2)    

# Meeting Notes:
_Will be placed here after the meeting occurs at 12-12:30pm today_

Question: Why does each count matrix have some instances where the gene counts are "0"s across all 6 libraries? Need to figure that out.

- Look at just BPs
- Or go to GO Slim and pick categories to compare
- Pull out every row that has immune in it “grep”      
Create smaller tables of just “immune” processes

Next step:
- Just pull out rows that have “immune” in them       
Calculation on counts         
Give sum of all 6 columns (stars)        
Another column that does mean       
Another column that does std error       
Could pick 4 genes (house-keeping - or one gene)        
What people use (NADPH or ribosomal gene)      
Could normalize based on that           
- Following step:           
Find common genes      
Find them based on shared names       
Swissprot IDs         
- Could in a separate effort:       
Do a join on that for all three species        
Join based on swissprot ID        
How many are shared        


## To Do:
### Multispecies
1. For each count matrix of each species:      
- pull out all genes that are annotated with "immune"     
- get sum of counts across all 6 libraries
- get mean of counts    
- get std error

2. Compare across all three species:    
- `join` each annotated count matrix by the uniprot accession ID column and see what is shared
- can also see what is unique to each species
- can then filter down smaller to just "immune" processes

3. Get GO Slim terms for each species annotated count matrix.

### Crab Paper:
Find some journal options to think about.
