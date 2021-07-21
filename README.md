# Mild and severe SARS-CoV-2 infection induces respiratory and intestinal microbiome changes in the K18-hACE2 transgenic mouse model

These scripts are purely intended as a description for the methods used in the publication:

Seibert, Caceres, Cardenas-Garcia, Carnaccini, Geiger, Rajao, Otesen, Perez, 2021, Mild and severe SARS-CoV-2 infection induces respiratory and intestinal microbiome changes in the K18-hACE2 transgenic mouse model. Microbiology Spectrum. Accepted 2021

Code related to the analyses performed at the ASV level is reported.

## Work-flow 

### Decontam 

The exported R script will show the analysis and use of program decontam (Nicole Davis et al. publication https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-018-0605-2) using the files that are created from dada2. This corresponds to results in Supplemental Table 1.

### SampleProcessingandSetup

This exported R script will show the proccess of using the exported decontam files to remove any variants with unknown phylas, are classified as Eukaryotes, Chloroplasts or Mitochondria (since the purpose of the paper was to analyze Bacteria), and remove any samples with a coverage of less 10,000 reads/sample (low coverage). The script also produces a boxplot that compares the sequencing coverage among negative controls and samples (lung and ceca). This will correspond to Figure 1B. 

### AlphaDiversity_Analysis

This exported R script will show the script used to rarify the data at a depth of 12,000, analysis of different alpha diversity measures (Observed ASVs, Shannon index, and Inverse Simpson index) of the different groups within the ceca and the lungs. This will correspond to Figures 2A-D, 5A-C, 5F-H, 5A-D, and Supplemental Figures S1-4.

### BetaDiversity_Analysis

This exported R script will show the script used to produce the graphs used to show the beta diversity comparisons of groups within the ceca and the lungs including Bray-Curtis distances, NMDS plot, and the hierarchal cluster analysis. This will correspond to Figures 2E-G, 5D and H, 6E-G. 

### Taxonomic_Analysis 

This exported R script will show the scripts used to analyze taxonomy relative abundance differences among groups in the cecum and lung. The phylum boxplots are analyzed using the relative abundance of each ASV. The family boxplots are analyzed using the relative abundance of ASVs that are >1% and >2% in the cecum and the lung, respectively. This was performed this way since we wanted to look for overall trends in the more abundant phyla and to account for those ASVS that have very low relative abundances that could potentially be PCR artifacts or contamination. This same analysis was also used to create the taxonomic barplots. This document also includes the script used to produce the correlation heatmap. This will correspond to Figures 3,4, 7, 8 and 5S. 
