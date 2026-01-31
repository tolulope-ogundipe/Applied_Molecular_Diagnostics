# 16S rRNA Microbiome Analysis Workflow (QIIME 2)

## Overview
This document outlines a standard workflow for 16S rRNA gene-based microbiome analysis using QIIME 2. The pipeline reflects applied research experience in animal health and host–microbiome studies, with emphasis on gastrointestinal samples and parasite-associated microbiota.

The workflow is designed for Illumina amplicon sequencing data and focuses on reproducibility, data quality, and biological interpretation.

## Sample Context
Microbiome analyses have been performed on:
- Gastrointestinal-associated samples
- Fecal material
- Parasitic nematodes isolated from host animals

Host species include livestock and equine systems, supporting investigations into host–parasite–microbiota interactions.

## Target Region and Sequencing Strategy
- 16S rRNA gene: V4 hypervariable region
- Amplicon-based sequencing
- Illumina platform
- Dual-indexing strategy applied during library preparation

## Step 1: Raw Data Import and Quality Assessment
- Demultiplexed paired-end FASTQ files imported into QIIME 2
- Initial quality inspection performed to evaluate read length, quality score distribution, and adapter presence
- Decisions on trimming and truncation guided by per-base quality profiles

## Step 2: Denoising and ASV Inference
- Denoising performed using an error-model–based approach
- Removal of low-quality reads, chimeras, and sequencing artifacts
- Generation of Amplicon Sequence Variants (ASVs) for high-resolution profiling
- Feature table and representative sequences produced

## Step 3: Taxonomic Assignment
- Taxonomic classification performed using a curated reference database
- SILVA database used for bacterial taxonomy assignment
- Taxonomic resolution evaluated across phylum to genus levels

## Step 4: Diversity Analyses - MicrobiomeAnalyst.ca
### Alpha Diversity
- Assessment of within-sample diversity
- Metrics selected based on study design and sequencing depth
- Rarefaction applied where appropriate

### Beta Diversity
- Between-sample diversity evaluated using distance-based metrics
- Ordination methods used to visualize community structure
- Grouping factors include biological and experimental variables
- 
## Step 5: Community Composition Analysis
- Relative abundance analysis at multiple taxonomic levels
- Identification of dominant and low-abundance taxa
- Comparison of microbial profiles across sample types or host conditions

## Step 6: Statistical Analysis and Visualization
- Downstream statistical analyses performed outside QIIME 2
- Feature tables and taxonomy exported for external platforms
- Visualization and comparative analysis conducted using microbiome-focused tools
  
## Data Interpretation
Microbiome outputs are interpreted in relation to:
- Host species and physiological context
- Gastrointestinal niche
- Parasitic or disease-associated conditions
- Experimental factors such as sex or sampling site

## Notes
This workflow represents applied microbiome research practice. Specific command-line syntax, proprietary scripts, and unpublished datasets are intentionally excluded.

