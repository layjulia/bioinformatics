# Bioinformatics R Project
This repository contains R scripts and analyses exploring **gene expression, growth data, and biological sequence diversity** across selected organisms. The project also demonstrates how RStudio and Git can be used to implement reproducible **bioinformatics workflows and clear documentation**.

## Key Project Files
| File | Description |
|------|-------------|
| [`AT4.Rmd`](https://github.com/layjulia/bioinformatics/blob/main/AT4.Rmd) | R Markdown file containing code script, outputs and explanations |
| [`AT4.html`](https://github.com/layjulia/bioinformatics/blob/main/AT4.html) | Rendered HTML output of the analysis |

## Summary of Project Structure

- [Part 1: Gene expression analysis and growth data analysis](https://github.com/layjulia/bioinformatics?tab=readme-ov-file#part-1-importing-files-data-wrangling-mathematical-operations-plots-and-saving-code-on-github)
- [Part 2: Examining biological sequence diversity](https://github.com/layjulia/bioinformatics?tab=readme-ov-file#part-2-examining-biological-sequence-diversity)

### Part 1: Gene expression analysis and growth data analysis

Part 1 input files were downloaded from: https://github.com/ghazkha/Assessment4

#### Gene Expression Analysis

- **Input**: RNA-seq count data (`gene_expression.tsv`), containing raw counts for three samples.
- **Scripts include**:
  - Importing data and setting gene identifiers as row names.
  - Calculating mean expression across samples.
  - Listing top 10 highly expressed genes.
  - Counting genes with mean expression < 10.
  - Generating a histogram of mean expression values.  
- **Output**:
  - Summary tables (`head()` of genes, mean values).
  - Ranked list of top 10 genes.
  - Histogram plot of mean expression.
  
#### Growth Data Analysis

- **Input**: Tree circumference measurements at two sites (control vs treatment) over 20 years (`growth_data.csv`)  
- **Scripts include**:
  - Importing CSV data into an R object.
  - Summarising column names and dataset structure.
  - Calculating mean and standard deviation of circumference at start and end.
  - Boxplots of tree circumference distributions by site and timepoint.
  - Mean growth over the last 10 years at each site.
  - Hypothesis testing (`t.test`) for differences in growth.  
- **Output**:
  - Summary statistics (mean ± SD).
  - Boxplot of growth trends.
  - p-value for site comparison.

### Part 2: Examining biological sequence diversity

_A. aceti_ (GCA_002005445) is the allocated organism of interest and is compared to the _E. coli_ (GCA_000005845) genome throughout. Differences in genome organisation, codon usage bias and protein sequence composition are discussed. Input files are complete coding DNA sequences (CDS) for *E. coli* and *A. aceti* available from:  

- [Acetobacter aceti (GCA_002005445)](https://bacteria.ensembl.org/Acetobacter_aceti_gca_002005445/Info/Index)
- [Escherichia coli str. K-12 substr. MG1655 str. K12 (GCA_000005845)](https://bacteria.ensembl.org/Escherichia_coli_str_k_12_substr_mg1655_gca_000005845/Info/Index/)

| Analysis | Key Steps | Outputs |
|----------|-----------|---------|
| **Coding Sequence Counts** | Count CDS entries per organism | Table comparing CDS counts |
| **Total Coding DNA** | Sum total coding length | Comparison table |
| **CDS Length Distribution** | Plot CDS lengths, compute mean & median | Box plot and summary table |
| **Base Composition & Amino Acid Frequencies** | Calculate nucleotide and amino acid proportions | Barplots of bases |
| **Codon Usage Bias** | Compute RSCU values, plot codon usage | Codon usage tables, heatmaps, barplots |
| **K-mer Analysis (k=3–5)** | Identify over- and under-represented k-mers, compare across organisms | Frequency barplots, rank/rank scatterplots with correlation coefficients |


## Requirements

- **R**
- R packages required:
  - `seqinr`
  - `R.utils`
  - `ggplot2`
  - `dplyr`
  - `patchwork`
  - `forcats`
  - `knitr`

## Quick Start Guide

1. Clone the repository: `git clone https://github.com/layjulia/bioinformatics.git`
2. Open `AT4.Rmd` in RStudio.
3. Install required packages: `install.packages(c("seqinr","R.utils","ggplot2","dplyr","patchwork","forcats","knitr"))`
4. Knit the R Markdown to HTML to reproduce the analyses

## Citations

Citation Style Language (CSL): [Harvard (Deakin University)](https://www.zotero.org/styles?q=id%3Aharvard-deakin-university&format=author-date)