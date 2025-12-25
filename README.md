## Project Title
NOA_RNAseq_Gene_Filtration_Pipeline

## Description
An end-to-end, reproducible bioinformatics pipeline for RNA-seq analysis and candidate gene prioritization in non-obstructive azoospermia

## Background
- Non-obstructive azoospermia (NOA) is a severe form of male infertility characterized by impaired spermatogenesis. 
RNA-seq studies of testicular tissue have revealed extensive transcriptional dysregulation; however, translating 
differential expression results into biologically meaningful and novel candidate genes remains challenging.

## Objective
- To identify and prioritize biologically plausible candidate genes associated with non-obstructive azoospermia by 
combining RNA-seq differential expression analysis with systematic, biologically driven gene filtration.

## Pipeline Overview
The pipeline consists of the following stages:

- RNA-seq data preprocessing and quality control  
-  Differential gene expression analysis between NOA and control samples
-  Gene filtration based on testis-specific expression and disease association  
-  Functional enrichment and biological interpretation of prioritized genes

## Key Methodology
To reduce false-positive candidates and improve biological relevance, differentially expressed genes are filtered by:

- Expression in normal human testis tissue (GTEx)
- Known association with obstructive azoospermia or unrelated infertility phenotypes
- Prior established involvement in non-obstructive azoospermia

The remaining genes represent prioritized candidates for further functional investigation.
## Data Sources
- NCBI GEO – public RNA-seq datasets of human testicular tissue  
- GTEx – tissue-specific gene expression reference  
- ClinVar – variant–disease associations  
- OMIM – curated gene–phenotype relationships  
- DisGeNET – gene–disease associations

## Reproducibility
- Modular scripts written in R and Python  
- Environment management via Conda  
- Workflow automation using Snakemake (planned)  
- Clear input/output structure for reuse with alternative datasets

## Repository Structure
data/        # Raw and processed input data  
scripts/     # Analysis and filtration scripts  
notebooks/   # Exploratory and QC notebooks  
results/     # Tables and figures  
envs/        # Conda environment specifications

## Limitations
- Dependence on publicly available datasets
- Sample size varies by selected GEO dataset
- Results are hypothesis-generating and not intended for clinical diagnosis
- 
## Future Work
- Integration of WES variant data
- Candidate gene scoring system
- Containerization using Docker

