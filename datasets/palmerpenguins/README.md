# Data: Palmer Archipelago (Antarctica) Penguin Dataset

## File

| File | Rows | Description |
|------|------|-------------|
| `penguins_lter.csv` | 344 | Full LTER dataset — all three species, all measurement and isotope columns |

## Download

```bash
# wget
wget https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv

# curl
curl -O https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv
```

```python
# Python / pandas
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv")
```

```r
# R
df <- read.csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv")
```

## Provenance

Downloaded from Kaggle:
**https://www.kaggle.com/datasets/parulpandey/palmer-archipelago-antarctica-penguin-data**

Original data collected by Dr. Kristen Gorman and the Palmer Station, Antarctica Long Term Ecological Research (LTER) Network.

**Citation:**
> Gorman KB, Williams TD, Fraser WR (2014). Ecological Sexual Dimorphism and Environmental Variability within a Community of Antarctic Penguins (Genus *Pygoscelis*). *PLoS ONE* 9(3): e90081. https://doi.org/10.1371/journal.pone.0090081

## License

CC-0 (Public Domain), in accordance with the Palmer Station LTER Data Policy and LTER Data Access Policy for Type I data.

## Columns

| Column | Description |
|--------|-------------|
| `studyName` | Study identifier (e.g. `PAL0708` = Palmer station, 2007–08 season) |
| `Sample Number` | Individual sample number within a study |
| `Species` | Penguin species: *Pygoscelis adeliae* (Adélie), *Pygoscelis antarctica* (Chinstrap), *Pygoscelis papua* (Gentoo) |
| `Region` | Geographic region (all records: Anvers) |
| `Island` | Island within the Palmer Archipelago: Torgersen, Dream, or Biscoe |
| `Stage` | Reproductive stage at time of sampling (e.g. "Adult, 1 Egg Stage") |
| `Individual ID` | Unique nest identifier |
| `Clutch Completion` | Whether the nest had a full clutch (Yes/No) |
| `Date Egg` | Date the first egg was observed |
| `Culmen Length (mm)` | Length of the upper ridge of the beak, in millimetres |
| `Culmen Depth (mm)` | Depth (height) of the culmen at its base, in millimetres |
| `Flipper Length (mm)` | Flipper length in millimetres |
| `Body Mass (g)` | Body mass in grams |
| `Sex` | Sex of the individual (MALE / FEMALE) |
| `Delta 15 N (o/oo)` | Stable isotope ratio δ¹⁵N (per mille) — proxy for trophic level |
| `Delta 13 C (o/oo)` | Stable isotope ratio δ¹³C (per mille) — proxy for foraging habitat |
| `Comments` | Free-text notes (e.g. missing measurements, field observations) |

## Why this dataset?

The Palmer penguin dataset is a modern, biologically meaningful alternative to the classic Iris dataset widely used in data science teaching. It contains:

- **Three species** on **three islands**, enabling species- and habitat-level comparisons
- **Morphological measurements** (bill, flipper, body mass) that reflect real ecological questions about sexual dimorphism and species differentiation
- **Stable isotope data** (δ¹⁵N, δ¹³C) that connect the dataset to diet and foraging ecology — topics directly relevant to bioinformatics and computational biology students
- **Missing data** and **inconsistent formatting** that mirror real-world data quality issues

Key references for teaching context:
- Kaggle notebook: https://www.kaggle.com/code/parulpandey/penguin-dataset-the-new-iris
- Kaggle notebook: https://www.kaggle.com/code/jessemostipak/dive-into-dplyr-tutorial-1
