---
layout: post
title: MultiSpecies - Analyses - Day 12 Exposed Alignments, Count Matrices, and Annotation
date: '2025-07-18'
categories: [MultiSpecies]
---
See post for details.

# Project Repository Link
NOTE: Private. Contains unpublished data from collaborators, so the link here and in this post will only work for folks who have been granted collaborative status on the repository until it can be made public later.

[grace-ac/project-pycno-multispecies-2023](https://github.com/grace-ac/project-pycno-multispecies-2023/tree/main)

# Alignments

## _P. helianthoides_

Code: [12-hisat2_pycno.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/12-hisat2_pycno.Rmd)   

Output:    
- [data/pycno_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_gene_count_matrix_2023.csv)   
- [data/pycno_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pycno_transcript_count_matrix_2023.csv)   

Alignment MultiQC Report: [pycno_2023_alignment_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/pycno_2023_alignment_multiqc_report.html)

Alignment Rates:   
Exposed, Day 12

| Sample ID | Alignment Rate  | Species            |
|-----------|-----------------|--------------------|
| PSC-0519  | 79.18%          | _P. helianthoides_ |
| PSC-0525  | 79.40%          | _P. helianthoides_ |
| PSC-0531  | 78.52%          | _P. helianthoides_ |
| PSC-0537  | 77.72%          | _P. helianthoides_ |
| PSC-0549  | 80.91%          | _P. helianthoides_ |
| PSC-0561  | 81.66%          | _P. helianthoides_ |

23464 genes; 25831 transcripts.

## _P. ochraceus_

Code: [13-hisat2_pisaster.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/13-hisat2_pisaster.Rmd)   

Output:    
- [data/pisaster_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_gene_count_matrix_2023.csv)   
- [data/pisaster_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/pisaster_transcript_count_matrix_2023.csv)   

Alignment MultiQC Report: [pisaster_2023_alignment_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/pisaster_2023_alignment_multiqc_report.html)

Alignment Rates:   
Exposed, Day 12

| Sample ID | Alignment Rate  | Species        |
|-----------|-----------------|----------------|
| PSC-0518  | 86.49%          | _P. ochraceus_ |
| PSC-0524  | 85.01%          | _P. ochraceus_ |
| PSC-0530  | 85.92%          | _P. ochraceus_ |
| PSC-0536  | 85.03%          | _P. ochraceus_ |
| PSC-0548  | 86.61%          | _P. ochraceus_ |
| PSC-0560  | 83.84%          | _P. ochraceus_ |

32370 genes; 35696 transcripts.

## _D. imbricata_

Code: [14-hisat2_derm.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/14-hisat2_derm.Rmd)

Output:    
- [data/derm_gene_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_gene_count_matrix_2023.csv)   
- [data/derm_transcript_count_matrix_2023.csv](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/data/derm_transcript_count_matrix_2023.csv)  

Alignment MultiQC Report: [dermasterias_2023_alignment_multiqc_report.html](https://owl.fish.washington.edu/gcrandall/multispeciesSSWD/QCreports/dermasterias_2023_alignment_multiqc_report.html)

Alignment Rates:   
Exposed, Day 12

| Sample ID | Alignment Rate  | Species        |
|-----------|-----------------|----------------|
| PSC-0529  | 87.81%          | _D. imbricata_ |
| PSC-0523  | 85.42%          | _D. imbricata_ |
| PSC-0529  | 83.73%          | _D. imbricata_ |
| PSC-0535  | 88.16%          | _D. imbricata_ |
| PSC-0547  | 86.96%          | _D. imbricata_ |
| PSC-0559  | 87.01%          | _D. imbricata_ |

22124 genes; 25030 transcripts.

# Annotations

Each species has a protein annotation of the genome, each one called the same "augustus.hints.aa". I ran `blastp` on each of these files to get uniprot/sprot annotation of the genes/transcripts which can then be `join`-ed with the count matrices for annotation.

## _P. helianthoides_

Code:
- BLAST: [15-BLAST-pycno.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/15-BLAST-pycno.Rmd)  
- Annotation `join`-ing: [18-annot-pycno.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/18-annot-pycno.Rmd)     

Output:
- BLAST: [output/15-BLAST-pycno/Phel_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/15-BLAST-pycno/Phel_aughintcod_blastout_sep.tab)     

Ran `blastp` on the `augustus.hints.aa` file from [https://datadryad.org/dataset/doi:10.5061/dryad.51c59zwfd](https://datadryad.org/dataset/doi:10.5061/dryad.51c59zwfd).   

From the `BLAST` output, the uniprot accession IDs were then put in the ID Mapping feature at [uniprot.org](https://www.uniprot.org/id-mapping), then a big table of GO annotations was downloaded.

That table was `join`-ed with the [Phel_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/15-BLAST-pycno/Phel_aughintcod_blastout_sep.tab)

THEN, I `join`-ed the _P. helianthoides_ transcript count matrix with the big annotation table, resulting in this annotated transcript count matrix:  

[output/18-annot-pycno/Phel_transcript_counts_annotation.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/18-annot-pycno/Phel_transcript_counts_annotation.tab)

## _P. ochraceus_

Code:
- BLAST: [16-BLAST-pisaster.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/16-BLAST-pisaster.Rmd)     
- Annotation: [19-annot-pisaster.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/19-annot-pisaster.Rmd)   

Output:
- BLAST: [output/16-BLAST-pisaster/Pisaster_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/16-BLAST-pisaster/Pisaster_aughintcod_blastout_sep.tab)     

Ran `blastp` on the `augustus.hints.aa` file from Mike Dawson and Lauren Schiebelhut (not publicly available yet).   

From the `BLAST` output, the uniprot accession IDs were then put in the ID Mapping feature at [uniprot.org](https://www.uniprot.org/id-mapping), then a big table of GO annotations was downloaded.

That table was `join`-ed with the [Pisaster_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/16-BLAST-pisaster/Pisaster_aughintcod_blastout_sep.tab).  

THEN, I `join`-ed the _P. ochraceus_ transcript count matrix with the big annotation table, resulting in this annotated transcript count matrix:  

[output/19-annot-pisaster/Pisaster_transcript_counts_annotation.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/19-annot-pisaster/Pisaster_transcript_counts_annotation.tab)

## _D. imbricata_

Code:
- BLAST: [17-BLAST-derm.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/17-BLAST-derm.Rmd)   
- Annotation: [20-annot-derm.Rmd](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/code/20-annot-derm.Rmd)    

Output:
- BLAST: [output/17-BLAST-derm/Dermasterias_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/17-BLAST-derm/Dermasterias_aughintcod_blastout_sep.tab)     

Ran `blastp` on the `augustus.hints.aa` file from from Mike Dawson and Lauren Schiebelhut (not publicly available yet).   

From the `BLAST` output, the uniprot accession IDs were then put in the ID Mapping feature at [uniprot.org](https://www.uniprot.org/id-mapping), then a big table of GO annotations was downloaded.

That table was `join`-ed with the [Dermasterias_aughintcod_blastout_sep.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/17-BLAST-derm/Dermasterias_aughintcod_blastout_sep.tab).

THEN, I `join`-ed the _D. imbricata_ transcript count matrix with the big annotation table, resulting in this annotated transcript count matrix:

[output/20-annot-derm/Derm_transcript_counts_annotation.tab](https://github.com/grace-ac/project-pycno-multispecies-2023/blob/main/output/20-annot-derm/Derm_transcript_counts_annotation.tab)
