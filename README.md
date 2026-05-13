# Bulk RNA-seq Analysis of GSE310456

**Adipose tissue-derived microRNAs as epigenetic modulators of type 2 diabetes**

## Overview

Reproducible bulk RNA-seq analysis of GEO dataset [GSE310456](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE310456), comparing gonadal white adipose tissue from diabetes-resistant (DR) and diabetes-prone (DP) female NZO mice.

## Methods

- **Preprocessing**: edgeR TMM normalization
- **DE analysis**: edgeR (QLF test) and limma-voom
- **Consensus DEGs**: Genes significant in both methods (FDR < 0.05, |logFC| ≥ 1)
- **Enrichment**: GO (Biological Process) and KEGG pathways

## Key Results

- 9,295 DEGs identified by both methods
- Strong enrichment of immune and inflammatory pathways
- Adipose tissue inflammation linked to diabetes susceptibility

## Files

- `Bulk RNA-seq Analysis Using GEO Dataset GSE310456.Rmd` — R Markdown source (reproducible)
- `Bulk RNA-seq Analysis Using GEO Dataset GSE310456.html` — Rendered report ([view online](https://github.com/dIcarusb/RNA-seq-Analysis-of-GSE310456/blob/main/Bulk-RNA-seq-Analysis-Using-GEO-Dataset-GSE310456.html))

## How to Reproduce

1. Clone this repository
2. Open `analysis.Rmd` in RStudio
3. Install required packages (listed in Session Info)
4. Knit the document

Data is downloaded automatically from GEO via `GEOquery`.

## Requirements

R ≥ 4.4.1 with packages: edgeR, limma, GEOquery, ggplot2, pheatmap, EnhancedVolcano, org.Mm.eg.db, pander, readxl

## Author

Pavel Baykalov — 2026-05-07
