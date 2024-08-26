# tcga_colorectal
Data analysis of open access colo-rectal patient data from the TCGA database.

The initial focus is on the Differential Expression analysis of \
the RNAseq data from the TCGA Database and the aim is to identify all statistically significant differences
between the two groups highlighted below. The samples are Human \
from the colo-rectal patients of the TCGA database with two locations; Rectum and Left Colon. 

This repository contains code to analyse colon and rectum cancer datasets from the TCGA database. The STAR \
Counts were downloaded and the analysis was performed using the packages cited in the script. The analysis includes pre-processing of the TCGA data, Principal Component Analysis (PCA), Differential Gene Expression Analysis, and data visualization of results.

**Sample info:**  \
the READ (rectum) cohort: 172 unique case submitter IDs  \
the COAD (colon) cohort: 461 unique case submitter IDs further stratified into sub-localizations\
localization 'descending colon',  \
localization 'sigmoid colon',  \
localization 'splenic flexure'  \
 <br />


## Data Preparation
### Data Download
From the TCGA database; the READ (rectum) cohort and the COAD (colon) cohorts were stratified. The \
"rectum" group was compared to with the "left colon" group which includes the followinig localizations \
'descending colon', 'sigmoid colon', and 'splenic flexure'. The data included gene expression \
quantification with STAR counts.

### Data Preprocessing
The data underwent pre-processing to prepare the data for downstream analysis, inluding data \
wrangling, and data normalization. This step included variance stabilizing transformation (vst) \
and Deseq2 package normalization to ensure data comparability across samples.


## Visualization

### PCA plot

Several PCA plots were generated to visualize the variation in the data. Samples that are similar \
to each other will cluster together in the PCA plot. PCA transforms a large set of variables into a \
smaller one that still contains most of the information in the large set. It does this by identifying \
the directions (principal components) in which the data varies the most. The data was first normalized (vst) \
so that the variance becomes independent of the mean. The axes of a PCA plot represent the principal \
components. Typically, the first two principal components (PC1 and PC2) are plotted, as they capture the \
most variance. Additionally, a 3D PCA plot was also produced to visualize the data with the \
third Principal Component.

### Volcano Plot
A volcano plot was generated to visualize the differential expression results. This plot displays
-> Log2 Fold Change (x-axis): Indicates the magnitude of expression change between colon and rectum samples.
-> -Log10 Adjusted p-value (y-axis): Represents the statistical significance of the expression change.
-> Significance Thresholds: Horizontal and vertical lines on the plot indicate thresholds for significance \
and fold change, helping to highlight the most differentially expressed genes.

### Heatmap
A heatmap was created to show the expression levels of the top differentially expressed genes. Key features \
of the heatmap include
-> Expression Patterns: It visualizes the expression patterns of these genes across samples, facilitating the \
identification of clusters or patterns in gene expression.
-> Clustering: Both genes and samples are clustered to reveal similarities and differences in expression profiles.

# Code Release Statement

This R Markdown file contains code for analyzing TCGA data and to perform PCA analysis, \
Differential Gene Expression Analysis, and other bioinformatics visualization. The code provided is released \
under the MIT License and is intended for use in research and educational projects.

**MIT License**

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and \
associated documentation files (the "Software"), to deal in the Software without restriction, including \
without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell \
copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the \
following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial \
portions of the Software.

**Disclaimer:**  
The software is provided "as is", without warranty of any kind, express or implied, including \
but not limited to the warranties of merchantability, fitness for a particular purpose, and \
non-infringement. In no event shall the authors or copyright holders be liable for any claim, \
damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, \
or in connection with the software or the use or other dealings in the software.

**Publication Policy**

As part of our commitment to transparency and scientific collaboration, our bioinformatics services core \
releases code and methods upon project completion. For generated code, we maintain a private GitHub \
repository during project execution where investigators and collaborating students can contribute. \
Methods are written throughout the project lifecycle and are part of our core's deliverables. Upon \
publication, the repository becomes public and is released under an open-source license, \
ensuring that others can build upon and benefit from our work, with the exception of code handling sensitive data.

Our core adheres to strict data security practices. Any code handling sensitive or confidential data undergoes \
rigorous review to ensure compliance with privacy regulations and may or may not be publicly \
released according to VCU's data security and privacy policies.

We require that any results obtained from code generated during our collaboration include a citation to the \
GitHub repository, acknowledging the contributions of our analysts. Additionally, the BISR and its source of \
funding, the CCSG grant, must be included in the acknowledgment and funding sections of manuscripts.