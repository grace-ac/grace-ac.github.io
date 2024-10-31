---
layout: post
title: Multi-Species Data - Transfer and Repository Updates
date: '2024-10-31'
categories: [pycno]
---
Transferred data from conference room computer (genefish) to Owl. See post for details.

# Downloaded from Azenta
I originally downloaded the data from Azenta via CyberDuck (See post: [MUSP RNAseq Data Received](https://grace-ac.github.io/MUSP-RNAseq-data-received/)), and then I left for a writing retreat with Melanie and Alyssa to Quadra Island, BC, Canada!

# Check md5 before transferring to OWL
md5 checksums are unique number codes that are used to confirm the integrity of files after downloading. I followed what we did in this GitHub Issue: [1460](https://github.com/RobertsLab/resources/issues/1460). There's a lot of information in there, so here's exactly what needs to be done:

On genefish, open terminal and navigate to the folder where the data lives.

Then run:

```
for checksum_file in *.md5
do
# Gets filename without any suffixes
filename=$(basename -s .fastq.gz.md5 ${checksum_file})
# Generates MD5 checksum and compares to provided checksum in MD5 file
diff <(md5 "${filename}.fastq.gz" | awk '{print $4}') <(awk '{print $1}' ${checksum_file})
done
```

This will take some time, so go and do something else and come back!

Checked at 4:45pm and it showed no errors, so all is good!

Now I'm `rsync`-ing the files to Owl:

```
rsync --archive --progress --verbose PSC*.fastq.gz grace@128.95.149.83:/volume1/web/nightingales/P_helianthoides/
```

# Check md5 checksums after `rsync`-ing to OWL       

Confirm that it all went well. Navigate in command line to the `grace@Owl:/var/services/web/nightingales/P_helianthoides` directory and run:

```
for fastq in PSC*.fastq.gz
do
  md5sum "${fastq}" >> checksums.md5
  echo "Generated checksum for ${file}."
  echo ""
done
```
