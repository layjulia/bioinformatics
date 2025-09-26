# Bioinformatics R Project
This repository contains R scripts and analyses for exploring gene expression, growth data, and biological sequence diversity across selected organisms. The project forms part of a beginner student's exploration of using R Studio with git to review bioinformatics workflows.

## Key Project Files
- [R Markdown](https://github.com/layjulia/bioinformatics/blob/main/AT4.Rmd)
- [HTML output](https://github.com/layjulia/bioinformatics/blob/main/AT4.html)

## Summary of Project Structure
- [Part 1: Gene expression analysis and growth data analysis](https://github.com/layjulia/bioinformatics?tab=readme-ov-file#part-1-importing-files-data-wrangling-mathematical-operations-plots-and-saving-code-on-github)
- [Part 2: Examining biological sequence diversity](https://github.com/layjulia/bioinformatics?tab=readme-ov-file#part-2-examining-biological-sequence-diversity)

### Part 1: Gene expression analysis and growth data analysis

Part 1 files were downloaded from: https://github.com/ghazkha/Assessment4

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

_A. aceti_ (GCA_002005445) is the allocated organism of interest and is compared to the _E. coli_ (GCA_000005845) genome throughout.

- [Acetobacter aceti (GCA_002005445)](https://bacteria.ensembl.org/Acetobacter_aceti_gca_002005445/Info/Index)
- [Escherichia coli str. K-12 substr. MG1655 str. K12 (GCA_000005845)](https://bacteria.ensembl.org/Escherichia_coli_str_k_12_substr_mg1655_gca_000005845/Info/Index/)

The below describes the purpose of each script in this section and their inputs and outputs.

- **Input**: Complete coding DNA sequences (CDS) for *E. coli* and *A. aceti*.  
- **Scripts include**:
  1. **Coding Sequence Counts**
     - Count the number of CDS for each organism.
     - Present results in a comparison table.
  2. **Total Coding DNA**
     - Sum of coding DNA length per organism.
     - Output as a table with comparison.
  3. **Coding Sequence Length**
     - Distribution of CDS lengths (boxplot).
     - Mean and median CDS length comparison.
  4. **Base Composition & Amino Acid Frequencies**
     - Nucleotide composition across CDS.
     - Amino acid frequencies in protein translations.
     - Bar plots for DNA bases and protein residues.
  5. **Codon Usage Bias**
     - Codon usage tables (RSCU values).
     - Visualisation of codon bias (barplots and heatmap).
     - Per-amino-acid codon breakdown.
  6. **K-mer Analysis**
     - Identify 10 most over- and under-represented protein sequence k-mers (lengths 3–5) in *A. aceti*.
     - Compare representation of these k-mers in *E. coli*.
     - Barplots of k-mer frequencies.
     - Fold-change tables highlighting over/under-representation.
- **Output**:
  - Tables comparing sequence features across organisms.
  - Boxplots and barplots (CDS length, codon usage, base frequencies).
  - Heatmap and barplots for codon usage bias.
  - K-mer frequency plots and summary tables.
  
## Requirements
- **R**
- Packages required:
  - `seqinr`
  - `ggplot2`
  - `dplyr`
  - `patchwork`
  - `forcats`