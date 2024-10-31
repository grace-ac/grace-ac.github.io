---
layout: post
title: Notes from Meeting with Steven; Paper Updates
date: '2024-10-31'
categories: [pycno]
---
See post for details about WSN talk plan; paper results plan.

# WSN Talk
I originally thought there wouldn't be any time to do any analyses in time for the talk, but after talking with Steven, I'll do a quick comparison between just the pycnos and the pisasters using transcriptomes and `kalisto` and emphasize that it's preliminary and that I'll be including derms later.

First step --> need to find transcriptome of pisaster ochraceus (GitHub Issue: [2001](https://github.com/RobertsLab/resources/issues/2001))


# Paper Results

## Alignment rates
Table of RNAseq metadata with alignment rates: [paper-pycno-sswd-2021-2022/data/Sample_Metadata_with_alignment.tsv](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/data/Sample_Metadata_with_alignment.tsv)

Average alignment rate = 76.84%     
Std deviation = 0.07     
Count of Samples = 28     
Std error = stddev*(squareroot(28)) = 0.37    

"[Standard deviation measures how much observations vary from one another, while standard error looks at how accurate the mean of a sample of data is compared to the true population mean.](https://careerfoundry.com/en/blog/data-analytics/standard-error-vs-standard-deviation/#:~:text=Standard%20deviation%20measures%20how%20much,to%20the%20true%20population%20mean.)".

So I think standard error might be the better of the two to report.

## Getting direction for DEG expression
Looked at [DEGlist_2021_exposedVcontrol_annotated.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2021_exposedVcontrol_annotated.tab) and [DEGlist_2022_exposedVcontrol_annotated.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/23-annotating-deg-lists/DEGlist_2022_exposedVcontrol_annotated.tab) and confirmed that positive log 2 fold change values means that the DEG is more highly expressed in exposed stars, and negative log 2 fold change values means that the DEG is less expressed in exposed stars. I did that confirmation by looking at counts.

So, for 2021 (experiment A)- there are 4,004 DEGs more highly expressed in exposed stars (out of a total of 6,938). And for 2022 (experiment B) - there are 3,628 DEGs more highly expressed in exposed stars (out of a total of 6,237).

For the 4,114 DEGs that are shared between the two years (experiments A and B): [DEGlist_same_2021-2022.tab](https://github.com/grace-ac/paper-pycno-sswd-2021-2022/blob/main/analyses/25-compare-2021-2022/DEGlist_same_2021-2022.tab)

I wanted to confirm that the log2fold change values for the 4,114 DEGs were the same direction for both DEG lists. I checked by creating new columns and assigning if the log2foldchange is < 0, put "lower" (because lower expression in exposed for negative log2fc), if not, then put "higher" (because higher expression in exposed for positive log2fc). Then I made another column where if the higher and lower values in the two columns for each experiment matched, it'd put "true", and if not, "false". It was true that the expression directions matched for 4,101 DEGs, meaning that if a DEG was more highly expressed in an exposed star in experiment A (2021), that same DEG was also more highly expressed in exposed for experiment B (2022). There were 13 DEGs that did not match. of those, 9 were more highly expressed in exposed stars for experiment A, and those same 9 were less expressed in exposed stars for experiment B. And the remaining 4 had the opposite, where they were less expressed in exposed stars in experiment A (2021), and those same 4 were more expressed in exposed in experiment B (2022).
