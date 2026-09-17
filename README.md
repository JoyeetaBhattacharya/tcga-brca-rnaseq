# Breast cancer molecular subtypes from RNA-seq: reproducing the TCGA landmark analysis

This project reproduces the RNA-seq components of the Cancer Genome
Atlas Network's landmark breast cancer paper (Nature 490, 61-70,
2012), which defined the molecular landscape of human breast tumours
using multi-platform genomic data across 825 patients.

## The question

Breast cancer is not one disease — it is at least five molecularly
distinct diseases that happen to originate in the same tissue. Patients
with Luminal A tumours have a fundamentally different prognosis and
treatment response than patients with Basal-like tumours. The question
this paper answered was: can genome-scale expression profiling define
these subtypes precisely enough to guide clinical decisions?

## Data

All data comes from the GDC Data Portal (project: TCGA-BRCA).

## What I reproduce

1. Subtype classification using the PAM50 gene set
2. PCA and UMAP of the expression landscape
3. Differential expression: tumour vs. normal
4. Differential expression: Basal-like vs. Luminal A
5. Survival analysis by subtype (Kaplan-Meier curves)


## How to reproduce

git clone https://github.com/YOUR-USERNAME/tcga-brca-rnaseq.git
cd tcga-brca-rnaseq
conda env create -f environment.yml
conda activate tcga-brca

## Tools

DESeq2, pyDESeq2, TCGAbiolinks, clusterProfiler, survival/survminer,
lifelines, scikit-learn

## References

- Cancer Genome Atlas Network. "Comprehensive molecular portraits of
  human breast tumours." Nature 490, 61-70 (2012).
- Love MI, Huber W, Anders S. "Moderated estimation of fold change and
  dispersion for RNA-seq data with DESeq2." Genome Biology 15, 2014.
