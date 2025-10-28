# GlobalDietaryDiversity
Repo for all code related to the paper 'Increasing plant diversity of global diets' by Neubert et al. 2025

## System requirements
### Hardware requirements
Designed to run on a standard laptop or desktop computer capable of typical data-analysis workflows. No special hardware is required.

### Software requirements
#### OS Requirements
The notebooks should work on most modern operating systems. This repo has been tested specifically on macOS 15.1.

#### Tools needed
1) R (4.1.x recommended; validated on 4.1.1)
2) An IDE such as RStudio (or any equivalent R IDE/editor)

#### R package dependencies
Install the following packages before running the notebooks:
- Biostrings 2.62.0
- dunn.test 1.3.5
- ggpubfigs 0.0.1
- ggpubr 0.5.0
- ggridges 0.5.4
- ggtree 3.2.1
- lmtest 0.9-40
- microbiome 1.16.0
- multcompView 0.1-8
- patchwork 1.3.0
- phyloseq 1.38.0
- RColorBrewer 1.1-3
- reshape2 1.4.4
- tidyverse 1.3.2
- vegan 2.6-4


## Installation guide
Typical install time for all tools and dependencies is <30 minutes on a normal desktop computer.

1) Get the repository: Download the ZIP or git clone the repo and open it in your R IDE (e.g., RStudio).

2) Install required R packages: Install the packages listed in the R package dependencies section (e.g., via install.packages() in R).

3) Run the notebooks: Open any Code/*.Rmd file and run in RStudio. The Rmd files are organized by figure and can be used to generate all results and figures. Restart the R session and clear objects from workspace between each notebook to ensure proper package and variable loading. Note that the economic data that support the findings of this study are available from the International Comparison Program (ICP) of The World Bank but access to unpublished ICP data is restricted under a confidentiality agreement and cannot be shared or disseminated by the authors, and so are not publicly available. Therefore, the Figure 5A code will not be able to be run. Data may be available from the ICP Global Office upon request and subject to their data access and confidentiality policies.


## Demo & Instructions for use
### Instructions to run on the included data
1) Open the repo in your R IDE (e.g., RStudio).
2) Install the packages listed in System Requirements.
3) Open each notebook under Code/ and run all code chunks (top to bottom). Restart R session and clear objects from workspace between each notebook to ensure proper package and variable loading.

### Expected output
- Figure PDFs are written to Figures/ (e.g., Figure1a_withLabels.pdf, Fig2a.pdf, etc. as indicated in each notebook).
- Some notebooks write intermediate R objects (e.g., *_withPCs.rds, CLR/RA variants) to Data/.

### Expected run time 
All notebooks (sequentially): ~5 minutes, depending on machine.

### Instructions for use on your own data 
1) Provide a compatible FoodSeq phyloseq object with otu_table, tax_table, and sample_data columns used in the notebooks. Save it in Data/ (e.g., Data/my_cohort_ps_glommed.rds) and update any file-name/path references in the code chunks.
2) Adjust cohort-specific variables as needed. Some notebooks reference fields and logic tailored to the study cohorts (e.g., country labels, covariates, inclusion filters). You may need to rename columns, relevel factors, or edit model formulas to reflect your dataset.
3) Run all code chunks in the relevant notebooks to generate figures for your dataset.

This codebase is designed to reproduce analyses for the specific cohorts in the paper; it is not a fully general-purpose package. While you can adapt it to other FoodSeq datasets by supplying a compatible phyloseq object and updating paths/variables, expect to adjust column names, factor levels, and some model formulas to match your context.


### Reproduction instructions (paper results)
1) Using the included precomputed objects and mapping files in Data/, open each Code/*.Rmd and run all code chunks in order.
2) The PDFs written to Figures/ will correspond to the figures reported in the manuscript. (The manuscript versions were spaced and lightly formatted in Illustrator; underlying data and results are identical.)
