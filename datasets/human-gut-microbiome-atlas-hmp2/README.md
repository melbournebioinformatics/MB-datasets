# Data: Human Gut Microbiome Atlas (HMP2)

Deep Metagenomics of Crohn's Disease & Ulcerative Colitis

## File

| File | Size | Description |
|------|------|-------------|
| `hmp2_ibd_metagenomics_atlas_20260219_121629.csv` | 8 MB | — |

## Download

> **Note:** This file is ~8 MB; download may take a moment.

```bash
# wget
wget https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/human-gut-microbiome-atlas-hmp2/hmp2_ibd_metagenomics_atlas_20260219_121629.csv

# curl
curl -O https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/human-gut-microbiome-atlas-hmp2/hmp2_ibd_metagenomics_atlas_20260219_121629.csv
```

```python
# Python / pandas
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/human-gut-microbiome-atlas-hmp2/hmp2_ibd_metagenomics_atlas_20260219_121629.csv")
```

```r
# R
df <- read.csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/human-gut-microbiome-atlas-hmp2/hmp2_ibd_metagenomics_atlas_20260219_121629.csv")
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/qasimhu/human-gut-microbiome-atlas-hmp2

Original source: qasimhu (Kaggle)

**Citation:**
> Lloyd-Price, J., Arze, C., Ananthakrishnan, A.N., et al. (2019). Multi-omics of the gut microbial ecosystem in inflammatory bowel diseases. *Nature*, 569, 655–662. https://doi.org/10.1038/s41586-019-1237-9
>
> Dataset curated by: qasimhu (2024). *Human Gut Microbiome Atlas (HMP2)*. Kaggle. https://www.kaggle.com/datasets/qasimhu/human-gut-microbiome-atlas-hmp2

## License

Attribution 4.0 International (CC BY 4.0)

## Columns

### `hmp2_ibd_metagenomics_atlas_20260219_121629.csv`

| Column | Description |
|--------|-------------|
| `External ID` | Unique stool sample identifier |
| `Participant ID` | Patient identifier (use for time-series grouping) |
| `week_num` | Study week of sample collection (0–52) |
| `diagnosis` | Clinical label: `Crohns Disease`, `Ulcerative Colitis`, or `Healthy` |
| `fecalcal` | Fecal Calprotectin (µg/g); gold-standard inflammation biomarker (<100 = remission, >250 = active) |
| `dysbiosis_score` | Deviation of microbiome composition from healthy reference |
| `antibiotics` | Whether patient was on antibiotics at time of collection (True/False) |
| `s__[species]` | ~500 columns of relative bacterial species abundance profiled by MetaPhlAn 3.0 |

## Why this dataset?

Longitudinal metagenomics dataset (1,638 samples, 132 subjects, 52 weeks) from a landmark IBD study. Introduces the challenges of high-dimensional compositional data — relative abundances must sum to 1, requiring CLR or log-ratio transforms before standard ML. The time-series structure motivates mixed-effects models; the clinical endpoints (Crohn's vs. UC vs. healthy) make the classification task medically concrete.

---

## Source description (from Kaggle)

# Context
This dataset is a curated, Machine Learning-ready version of the **Integrative Human Microbiome Project (iHMP)**, specifically the Inflammatory Bowel Disease Multi-omics Database (IBDMDB).

Unlike standard microbiome datasets that offer only a single snapshot per patient, this atlas is **Longitudinal**. It follows 132 individuals (Crohn's Disease, Ulcerative Colitis, and Healthy Controls) over the course of one year, capturing the dynamic fluctuations of the gut ecosystem during disease flares and remission.

# Content
The dataset contains **1,638 metagenomic samples** from 132 unique subjects.
* **Sequencing:** Whole Genome Shotgun (WGS).
* **Profiling:** Species-level taxonomy assigned using **MetaPhlAn 3.0**.
* **Metadata:** Matched clinical phenotypes including inflammation markers.

# Key Variables
* **`External ID`**: Unique identifier for the stool sample.
* **`Participant ID`**: Unique patient identifier (allows for Time-Series grouping).
* **`week_num`**: The study week (0 to 52) when the sample was collected.
* **`diagnosis`**: The clinical label (`Crohns Disease`, `Ulcerative Colitis`, or `Healthy`).
* **`fecalcal`**: Fecal Calprotectin ($\mu g/g$). The **Gold Standard** biomarker for intestinal inflammation.
    * *&lt; 100:* Remission/Healthy.
    * *&gt; 250:* Active Inflammation.
* **`dysbiosis_score`**: A calculated metric indicating how "deviant" the microbiome is from a healthy reference.
* **`antibiotics`**: Binary flag (True/False) if the patient was on antibiotics at the time.
* **`[Bacteria Columns]`**: ~500 columns representing the Relative Abundance of specific bacterial species (e.g., *s__Faecalibacterium_prausnitzii*).

# Acknowledgements
Data derived from the [IBDMDB](https://ibdmdb.org/) project (HMP2).
* *Lloyd-Price, J., et al. Multi-omics of the gut microbial ecosystem in inflammatory bowel diseases. Nature (2019).*

# Inspiration
1.  **Ecological Forecasting:** Can you predict a "Flare-Up" (high Fecal Calprotectin) 2 weeks before it happens based on microbial shifts?
2.  **Biomarker Discovery:** Which specific species are the strongest predictors of Crohn's Disease? (Hint: Check *E. coli* vs *F. prausnitzii*).
3.  **Compositional Data Analysis:** Apply CLR (Centered Log-Ratio) transformations to handle the relative abundance constraints.
