# MB-datasets

Small datasets for teaching and training at [Melbourne Bioinformatics](https://mdhs.unimelb.edu.au/melbournebioinformatics), The University of Melbourne.

## Purpose

Curated, ready-to-use datasets for workshops, tutorials, and course materials. Each dataset is small enough to be bundled directly in a repo (under 1 MB) and comes with provenance documentation.

## Datasets

| Dataset | Description | Rows | Format |
|---------|-------------|------|--------|
| [palmerpenguins](datasets/palmerpenguins/) | Morphological and isotope measurements for three Antarctic penguin species | 344 | CSV |

## Downloading a dataset

All files are accessible directly via `raw.githubusercontent.com`. The URL pattern is:

```
https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/<dataset-name>/<filename>
```

**wget**
```bash
wget https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv
```

**curl**
```bash
curl -O https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv
```

**Python**
```python
import pandas as pd
url = "https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv"
df = pd.read_csv(url)
```

**R**
```r
url <- "https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/palmerpenguins/penguins_lter.csv"
df <- read.csv(url)
```

For gzipped files (`.csv.gz`), both `wget`/`curl` download as-is; pandas and R's `read.csv` decompress automatically.

---

## Contributing

1. Create a new directory under `datasets/` using a short, lowercase, hyphenated name (e.g. `datasets/my-dataset/`).
2. Add a `README.md` — see [`datasets/palmerpenguins/README.md`](datasets/palmerpenguins/README.md) for the expected format. At minimum it must include:
   - A URL to the original source (ideally one with full metadata/provenance)
   - A table of columns with descriptions
   - License information
3. Keep dataset files under **1 MB**. Gzip (`.gz`) is fine if needed.
4. Add a row to the table above.

### README template

```markdown
# Data: <Dataset Name>

## File

| File | Rows | Description |
|------|------|-------------|
| `data.csv` | N | Brief description |

## Download

```bash
# wget
wget https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/<dataset-name>/<filename>

# curl
curl -O https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/<dataset-name>/<filename>
```

```python
# Python / pandas
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/<dataset-name>/<filename>")
```

```r
# R
df <- read.csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/<dataset-name>/<filename>")
```

## Provenance

Downloaded from: <URL>

Original source: <institution / author / study>

**Citation:**
> Author et al. (Year). Title. *Journal* vol(issue): pages. https://doi.org/...

## License

<License name and any conditions>

## Columns

| Column | Description |
|--------|-------------|
| `col_name` | What it contains |

## Why this dataset?

<One paragraph: what makes it useful for teaching?>
```

## License

Individual datasets carry their own licenses — see the `README.md` in each subdirectory. Repository infrastructure (this file, templates) is released under [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
