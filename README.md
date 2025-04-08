# README

# Acute Myeloid Leukemia Heatmap Analysis

A bioinformatics analysis pipeline for generating heatmaps from RNA-seq data of acute myeloid leukemia samples. This repository adapts the refine.bio-examples notebook for analyzing gene expression patterns in AML model mice.

## Project Details

| Information | Details |
|-------------|---------|
| Original Source | [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html) |
| Dataset | Shih et al., 2017 (19 AML model mice samples) |
| Processing | Quantile normalized via refine.bio |
| Analysis Type | RNA-seq clustering heatmap |
| Last Updated | October 2021 |

## Requirements

* R environment
* Required packages:
  * pheatmap
  * magrittr
  * readr
  * dplyr
  * tibble
  * sessionInfo

## Directory Structure

```markdown
project_root/
├── data/
│   ├── SRP070849/
│   │   ├── SRP070849.tsv      # Gene expression matrix
│   │   └── metadata_SRP070849.tsv # Sample metadata
├── plots/
│   └── aml_heatmap.png        # Generated heatmap
└── results/
    └── top_90_var_genes.tsv   # Filtered gene expression data
```

## Analysis Overview

This pipeline performs RNA-seq analysis on AML samples from Shih et al., 2017, focusing on mice with IDH2 and TET2 mutations under different treatment conditions. The analysis includes:

1. Data preprocessing and organization
2. Gene expression matrix loading
3. Sample ordering synchronization
4. Variance-based gene filtering
5. Heatmap generation with annotations

## Key Features

* Automated folder structure creation
* Sample metadata integration
* Treatment condition tracking
* Mutation status annotation
* Variance-based gene selection
* Reproducible analysis (seed: 12345)

## Getting Started

1. Clone this repository
2. Install required R packages:
   ```r
   if (!("pheatmap" %in% installed.packages())) {
     install.packages("pheatmap", update = FALSE)
   }
   ```
3. Execute the R Markdown file to generate the analysis

## Output Files

* `aml_heatmap.png`: Generated heatmap visualization
* `top_90_var_genes.tsv`: Filtered gene expression data
* Session information report

## Dataset Citation

[Shih et al., 2017](https://pubmed.ncbi.nlm.nih.gov/28193779/)

## Original Source

This analysis adapts the refine.bio-examples notebook available at:
[https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html)

Note: This README file describes the analysis pipeline and requirements. For detailed methodology and implementation details, refer to the R Markdown file in the repository. 