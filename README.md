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
Part 1 explores gene expression and long-term tree growth data. The table below summarises the inputs, analyses and outputs.

Part 1 input files from: https://github.com/ghazkha/Assessment4

| Analysis | Key Steps | Outputs |
|----------|-----------|---------|
| **Gene Expression Analysis** <br> (`gene_expression.tsv` – RNA-seq counts) | - Import data<br>- Compute mean expression per gene<br>- Identify top 10 highly expressed genes<br>- Count genes with mean < 10<br>- Generate histogram of mean gene expression | Summary tables, top 10 gene list, histogram plot |
| **Growth Data Analysis** <br> (`growth_data.csv` – Tree circumference) | - Import and explore dataset<br>- Calculate mean & SD at start/end of study<br>- Visualise distributions with boxplots by site/time<br>- Compute mean growth over last 10 years<br>- Perform `t.test` for site differences | Summary statistics (mean ± SD), box plots of growth trends, p-values |

**Key Findings:**  
- **Gene Expression**: Top 10 highly expressed genes were identified; many genes had low mean expression (<10); overall expression distribution is skewed toward low counts.  
- **Growth Data**: Mean growth differed between sites over the 20-year period; t-tests indicate differences are not statistically significant.

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

**Key Findings:**  
- *E. coli* has more coding sequences than *A. aceti* and slightly lower GC content.  
- *A. aceti* shows higher GC bias, which may influence codon usage and protein composition.  
- Codon usage differs between organisms, reflecting organism-specific preferences.  
- K-mer analysis highlights over- and under-represented motifs, suggesting differences in genome sequence patterns.

## Requirements

- **R**
- R packages required:

| Package     | Purpose                                           |
|------------|--------------------------------------------------|
| `seqinr`   | Sequence analysis and codon usage calculations  |
| `R.utils`  | General utility functions                        |
| `ggplot2`  | Plotting and data visualisation                  |
| `dplyr`    | Data manipulation                                |
| `patchwork`| Combining multiple plots                          |
| `forcats`  | Factor manipulation and ordering                 |
| `knitr`    | Rendering HTML table                             |

## Quick Start Guide

1. Clone the repository: `git clone https://github.com/layjulia/bioinformatics.git`
2. Open `AT4.Rmd` in RStudio.
3. Install required packages: `install.packages(c("seqinr","R.utils","ggplot2","dplyr","patchwork","forcats","knitr"))`
4. Knit the R Markdown to HTML to reproduce the analyses

## Citations

Citation Style Language (CSL): [Harvard (Deakin University)](https://www.zotero.org/styles?q=id%3Aharvard-deakin-university&format=author-date)