# Mild and severe SARS-CoV-2 infection induces respiratory and intestinal microbiome changes in the K18-hACE2 transgenic mouse model

These scripts are purely intended as a description for the methods used in the publication:

Seibert, Caceres, Cardenas-Garcia, Carnaccini, Geiger, Rajao, Otesen, Perez, 2021, Mild and severe SARS-CoV-2 infection induces respiratory and intestinal microbiome changes in the K18-hACE2 transgenic mouse model. Submitted (2021)

Code related to the analyses performed at the ASV level is reported.

## Work-flow 

### Decontam 

The exported R script will show the analysis and use of program decontam (Nicole Davis et al. publication https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-018-0605-2) using the files that are created from dada2. 

### SampleProcessingandSetup

This exported R script will show the proccess of using the exported decontam files to remove any variants with unknown phylas, are classified as Eukaryotes, Chloroplasts or Mitochondria (since the purpose of the paper was to analyze Bacteria), and remove any samples with a coverage of less 10,000 reads/sample (low coverage). The script also produces a boxplot that compares the sequencing coverage among negative controls and samples (lung and ceca). 

### AlphaDiversity_Analysis

This exported R script will show the script used to rarify the data at a depth of 12,000, analysis of different alpha diversity measures (Observed ASVs, Shannon index, and Inverse Simpson index) of the different groups within the ceca and the lungs. This will correspond to Figures 2A-D, 4A-C, 4F-H, 5A-D, and Supplemental Figures S1-4.

### BetaDiversity_Analysis

This exported R script will show the script used to produce the graphs used to show the beta diversity comparisons of groups within the ceca and the lungs. This will correspond to Figures 2D-G, 4D and 4H, and 5D-G and Supplemental Figures S5.
