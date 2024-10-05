# Stage-4
# LGG Glioma Biomarker Identification

## Overview
This repository contains R code for analyzing RNA-seq data from the TCGA-LGG project to identify potential biomarkers in gliomas based on IDH status (Wildtype vs Mutant). The analysis includes preprocessing steps, differential expression analysis (DEA), and visualization of the results.

## Requirements

### R Requirements
- **R (version 4.0 or later)**
- **Required R packages**:
  - `TCGAbiolinks`
  - `SummarizedExperiment`
  - `DESeq2`

## Installation

### Installing R Packages
Install the necessary R packages using the following commands:
install.packages("BiocManager")
BiocManager::install(c("TCGAbiolinks", "SummarizedExperiment", "DESeq2"))

## Usage
### Load the Data
The script downloads RNA-seq data from the GDC (TCGA-LGG project) and processes it to ensure it is ready for analysis.

### Preprocess the Data
1. The script filters genes with more than 25 zero values across samples to maintain data quality.
2. Samples with missing IDH status are removed, and only those with valid IDH status are used.
3. Genes with low counts (less than 10 reads across all samples) are filtered out.

## Differential Expression Analysis
The script conducts differential expression analysis using DESeq2, identifying significant differentially expressed genes (DEGs) based on adjusted p-values (padj < 0.05) and log2 fold changes (log2FC > 1).

## Visualization
MA Plot: The script generates an MA plot to visualize the differential expression results for IDH Wildtype vs Mutant gliomas.

## Files
DESeq2_results_TCGA_LGG.csv: CSV file containing results from the differential expression analysis.

