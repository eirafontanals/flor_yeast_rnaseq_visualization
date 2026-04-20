# Flor Yeast RNA-seq Visualization

This repository presents an RNA-seq data visualization project focused on two industrial strains of *Saccharomyces cerevisiae* (flor yeasts) involved in sherry wine production. The aim is to explore whether transcriptomic differences between strains may help explain differences in wine characteristics.

## Project overview

Flor yeasts develop a velum on the surface of fortified wine and are essential in the biological aging process that defines the sensory profile of sherry wines. In this project, RNA-seq expression data from two flor yeast strains were analyzed across six stages of velum development, using four replicates per time point.

The analysis applies dimensionality reduction and visualization methods to investigate the global structure of the data, evaluate clustering patterns, and identify potential outlier samples.

## Objectives

- Load and organize RNA-seq count data from four replicate files
- Build sample metadata from file names
- Explore global transcriptomic structure
- Apply dimensionality reduction techniques:
  - PCA
  - t-SNE
  - UMAP
- Assess clustering by strain, time point, and replicate
- Detect potentially atypical samples
- Compare raw and normalized expression patterns

## Methods

The analysis was developed in **R Markdown** and relies on the following main packages:

- `ggplot2`
- `dplyr`
- `tidyr`
- `tibble`
- `RColorBrewer`
- `ggfortify`
- `factoextra`
- `Rtsne`
- `umap`
- `patchwork`
- `htmltools`

## Repository structure

```bash
.
├── README.md
├── flor-yeast-rnaseq-visualization.Rmd
├── data/
│   ├── rep1.csv
│   ├── rep2.csv
│   ├── rep3.csv
│   └── rep4.csv
├── figures/
└── output/
│   ├── flor-yeast-rnaseq-visualization.html
```

## How to run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/flor-yeast-rnaseq-visualization.git
   cd flor-yeast-rnaseq-visualization
   ```

2. Open the `.Rmd` file in **RStudio**.

3. Install the required packages if needed:

   ```r
   install.packages(c(
     "ggplot2", "tidyr", "dplyr", "tibble", "RColorBrewer",
     "ggfortify", "factoextra", "Rtsne", "umap", "patchwork", "htmltools"
   ))
   ```

4. Place the input files inside the `data/` directory.

5. Knit the R Markdown document to HTML.

## Data

This project expects expression count tables stored as CSV files, corresponding to the different biological replicates. File names are used to reconstruct sample metadata such as strain, time point, and replicate.

If the original dataset cannot be shared publicly, this repository can still be used as a reproducible analysis template by following the same input structure.

## Main analyses

The project includes:

- Data import and preprocessing
- Metadata extraction from sample names
- Count matrix assembly
- Exploratory visualization of sample relationships
- PCA on raw and normalized data
- t-SNE projection
- UMAP projection
- Interpretation of clustering patterns and outlier behavior

## Key observations

The visual analyses suggest that transcriptomic variation may reflect both strain-specific and developmental differences. In addition, one sample appears to behave atypically during quality assessment and may represent a potential outlier worth further investigation.

## Authors

- Eira Fontanals Muñoz
- Òscar Contreras Parejo
- Marc J. Torres Valero

## Academic context

This repository was developed as part of an academic data visualization project in bioinformatics.

