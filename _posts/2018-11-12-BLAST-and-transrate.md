---
layout: post
title: BLAST on Hummingbird and Transrate 
date: '2018-11-12'
category: bairdi
tags: [BLAST, Transrate]
---
Today I attempted to take my BLAST output on Hummingbird and work through this [blast-2-slim](https://github.com/sr320/nb-2018/blob/master/C_virginica/83-blast-2-slim.ipynb) notebook of Steven's. I had gone through this before using [Cgigas](https://github.com/grace-ac/Practicing-with-Blast/blob/master/notebooks/blast-to-slim.ipynb). I got stuck today at the part where you ```!join``` ```_blast-GO-unfolded.sorted``` with ```GO-GOslim.sorted```. Will ask tomorrow. Additionally, today I worked on using ```transrate``` to look at my _C. bairdi_ assembly using [Laura's notebook](https://github.com/fish546-2018/laura-quantseq/blob/master/notebooks/transcriptome-assess-annotate.ipynb) as a guide. 

### BLAST to GO slim
The notebook is in the Downloads on Hummingbird in ```grace-Cbairdi-transcriptome/notebooks/20181105-blast-Cbairdi_swiss-prot.ipynb```. I couldn't figure out how to ```commit``` and ```push``` it successfully to my [GitHub repo notebook](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/notebooks/20181025-blast-Cbairdi_swiss-prot.ipynb)...
but I ```rsync```-ed the notebook to Owl from Hummingbird: [/scaphapoda/grace/Crab-project/20181025-blast-Cbairdi_swiss-prot.ipynb](http://owl.fish.washington.edu/scaphapoda/grace/Crab-project/20181025-blast-Cbairdi_swiss-prot.ipynb). 

Anyway, I got stuck where you have to ```!join``` the ```_blast-GO-unfolded.sorted```with ```GO-GOslim.sorted```. I checked the two files in TextWrangler on Hummingbird, and they both looked good. Additionally, I looked at the files using ```!head``` and ```!tail```. The one thing that I noticed, which I'm not sure is typical, is that in the ```_blast-GO-unfolded.sorted``` file, there were a lot more rows of the "TRINITY_DN#..." column, than there where of the "GO...." column. Maybe that is the problem? 

Will ask Steven or Sam tomorrow morning.

### ```Transrate```
I used ```Transrate``` today and followed [Laura's notebook](https://github.com/fish546-2018/laura-quantseq/blob/master/notebooks/transcriptome-assess-annotate.ipynb). Here's my notebook post: [Cbairdi_01_tranrate.ipynb](https://github.com/fish546-2018/grace-Cbairdi-transcriptome/blob/master/notebooks/Cbairdi_01_transrate.ipynb). I'm not sure what else I should do with this, so I'll ask tomororw. 

### GSS
This Thursday is GSS. I'm hoping to have some basic assembly data to share on my poster, and I'll have some stuff after I get the above issues sorted out.

