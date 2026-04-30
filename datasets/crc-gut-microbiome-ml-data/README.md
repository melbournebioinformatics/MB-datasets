# Data: CRC Gut Microbiome ML Data

Microbiome data for colorectal cancer ML classification (60 samples)

## File

| File | Size | Description |
|------|------|-------------|
| `README.md` | 2 KB | — |
| `metadata.csv` | 3 KB | — |
| `seqtab_nochim_export.xlsx` | 1 MB | — |
| `taxa_species_export.xlsx` | 511 KB | — |

## Download

```bash
BASE=https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/crc-gut-microbiome-ml-data

# wget
wget "$BASE/metadata.csv"
wget "$BASE/seqtab_nochim_export.xlsx"
wget "$BASE/taxa_species_export.xlsx"

# curl
curl -O "$BASE/metadata.csv"
curl -O "$BASE/seqtab_nochim_export.xlsx"
curl -O "$BASE/taxa_species_export.xlsx"
```

```python
# Python / pandas — metadata only (CSV)
import pandas as pd
base = "https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/crc-gut-microbiome-ml-data"
meta = pd.read_csv(f"{base}/metadata.csv")
seqtab = pd.read_excel(f"{base}/seqtab_nochim_export.xlsx", index_col=0)
taxa = pd.read_excel(f"{base}/taxa_species_export.xlsx", index_col=0)
```

```r
# R
base <- "https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/crc-gut-microbiome-ml-data"
meta <- read.csv(paste0(base, "/metadata.csv"))
# xlsx files require readxl or openxlsx:
# library(readxl); seqtab <- read_excel(tempfile_from_url(...))
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/aramelheni/crc-gut-microbiome-ml-data

Original source: aramelheni (Kaggle)

**Citation:**
> Armelʼheni, A. (2023). *CRC Gut Microbiome ML Data*. Kaggle. Derived from DADA2-processed 16S rRNA sequencing data; original code at https://github.com/aramelheni/ColorectalCancer-Detection. https://www.kaggle.com/datasets/aramelheni/crc-gut-microbiome-ml-data

## License

apache-2.0

## Columns

### `README.md`

Documentation file — not a data file; no column table applicable.
### `metadata.csv`

| Column | Description |
|--------|-------------|
| `SampleID` | Unique sample identifier |
| `host_disease` | Disease status label |
| `SampleName` | Human-readable sample name |
| `DiseaseStatus` | `Colorectal cancer`, `Healthy`, or `Adenomatous Polyps` |
| `Sex` | Patient sex |
| `Age` | Patient age in years |
### `seqtab_nochim_export.xlsx`

ASV abundance matrix. Rows = 60 patient samples; columns = ASV DNA sequences (one per amplicon sequence variant); cell values = read counts (bacterial abundance).

| Dimension | Description |
|-----------|-------------|
| Rows | One row per patient sample (60 total) |
| Columns | One column per ASV DNA sequence (thousands of features) |
| Values | Integer read counts representing bacterial abundance |
### `taxa_species_export.xlsx`

Taxonomic classification of each ASV. One row per ASV; columns are taxonomic ranks.

| Column | Description |
|--------|-------------|
| `Kingdom` | Taxonomic kingdom |
| `Phylum` | Taxonomic phylum |
| `Class` | Taxonomic class |
| `Order` | Taxonomic order |
| `Family` | Taxonomic family |
| `Genus` | Taxonomic genus |
| `Species` | Taxonomic species |

## Why this dataset?

Small (60 samples), well-curated 16S rRNA amplicon dataset with ground-truth disease labels (CRC, healthy, adenomatous polyps). Illustrates the full amplicon analysis pipeline — ASV table → taxonomic assignment → abundance matrix → ML classification — at a scale students can explore interactively. Small size makes iteration fast; the three-class labels and high-dimensional feature space motivate dimensionality reduction and feature selection discussions.

---

## Source description (from Kaggle)

## About Dataset

This dataset contains **processed gut microbiome data** from 60 samples for **Colorectal Cancer (CRC) detection** using machine learning. The data is derived from 16S rRNA gene sequencing and has been preprocessed using the DADA2 pipeline.

## Files Description

### seqtab_nochim_export.xlsx (1.4 MB)
- ASV (Amplicon Sequence Variant) abundance table
- **Rows:** Patient samples (60 samples)
- **Columns:** DNA sequences (ASVs) representing different bacterial species
- **Values:** Read counts (bacterial abundance)

### taxa_species_export.xlsx (511 KB)
- Taxonomic classification table mapping each ASV to its taxonomy
- **Includes:** Kingdom, Phylum, Class, Order, Family, Genus, Species

### metadata.csv (2.8 KB)
- Patient information and disease status
- **Columns:** SampleID, host_disease, SampleName, DiseaseStatus, Sex, Age
- **Categories:** Colorectal cancer | Healthy | Adenomatous Polyps

## Usage

This dataset is ready for machine learning tasks:
- Train classification models to predict CRC from gut microbiome composition
- Identify bacterial genera associated with colorectal cancer
- Compare microbial diversity between healthy and CRC patients
- Feature engineering from microbiome sequencing data

## Acknowledgments

Data processed using DADA2 pipeline. Original repository: [ColorectalCancer-Detection](https://github.com/aramelheni/ColorectalCancer-Detection)
