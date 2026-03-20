---
layout: post
title: Submitting Raw RNAseq Files to NCBI From Ch. 1
date: '2026-03-19'
categories: [RNAseq, NCBI, Chapter1]
---
Details about submitting the raw RNAseq files to NCBI for my first chapter. 

### Create an NCBI Account
I logged in through my ORCID account. Started a submission for SRA. 

Added the metadata information, project info, etc, according to the NCBI specifications.  

### SFTP To Transfer files 
Followed instructions on NCBI and also got help from Sam (GitHub Issue [#2407](https://github.com/RobertsLab/resources/issues/2407)), and looked at [this notebook post](https://robertslab.github.io/sams-notebook/posts/2017/2017-07-06-data-management-sra-submission-olympia-oyster-uw-pacbio-data-from-20170323/index.html) of Sam's. 

Used `ssh` to get into Owl where the data files are. I first copied all the files for this specific project into a new folder so that I could easily transfer them all and not any extra ones. 

Owl folder: `web/nightingales/P_helianthoides/Grace_Crandall_Chapter1_Files_copy` 

Then I established an `sftp` connection: 

`sftp subftp@sftp-private.ncbi.nlm.nih.gov` where `subftp` is the username. It then prompted me to put in the password given to me by NCBI (will not share). 

Then I followed the remaining instructions from NCBI:   
1. navigate to my account folder using: `cd uploads/grace[more info that I won't share]`    
2. Create a subfolder using: `mkdir`   
3. Navigate into that newly created subfolder using `cd`   
4. Copy files into the subfolder using: `mput *fastq.gz` 

Files started transferring around 7:40pm. Completed around 8:33 pm. Takes 10+ minutes for all the files to officially transfer to the folder on the NCBI thing. 

"After upload, select your preload folder from the Files step of your submission.
Note: it takes at least 10 minutes for uploaded files to become available for selection within a submission." 

Submitted 23:47. 

## NCBI Info 
Will post once official: 

Project: [PRJNA1440140](https://www.ncbi.nlm.nih.gov/sra/PRJNA1440140)    
Officially published 2026-03-20. 

  


