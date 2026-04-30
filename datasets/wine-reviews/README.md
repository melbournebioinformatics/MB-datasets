# Data: Wine Reviews

130k wine reviews with variety, location, winery, price, and description

## File

| File | Size | Description |
|------|------|-------------|
| `winemag-data-130k-v2.csv` | 50 MB | — |
| `winemag-data-130k-v2.json` | 76 MB | — |
| `winemag-data_first150k.csv` | 47 MB | — |

## Download

> **Note:** These files (50–76 MB each) exceed the 1 MB repository limit and are not committed to this repo. Download directly from the source:
>
> https://www.kaggle.com/datasets/zynicide/wine-reviews

After downloading and unzipping:

```python
# Python / pandas
import pandas as pd
df = pd.read_csv("winemag-data-130k-v2.csv", index_col=0)
```

```r
# R
df <- read.csv("winemag-data-130k-v2.csv")
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/zynicide/wine-reviews

Original source: zynicide (Kaggle)

**Citation:**
> Thoutt, Z. (2017). *Wine Reviews*. Kaggle. Scraped from WineEnthusiast (winemag.com), June and November 2017. https://www.kaggle.com/datasets/zynicide/wine-reviews

## License

CC-BY-NC-SA-4.0

## Columns

### `winemag-data-130k-v2.csv`

| Column | Description |
|--------|-------------|
| `country` | Country of origin |
| `description` | Taster's review text |
| `designation` | Vineyard within the winery where grapes were sourced |
| `points` | Rating score (80–100) |
| `price` | Cost per bottle (USD) |
| `province` | Province or state of origin |
| `region_1` | Specific wine-growing area within province |
| `region_2` | More specific sub-region (not always present) |
| `taster_name` | Name of the wine reviewer |
| `taster_twitter_handle` | Reviewer's Twitter handle |
| `title` | Review title (typically includes vintage year) |
| `variety` | Grape variety |
| `winery` | Winery that made the wine |
### `winemag-data-130k-v2.json`

JSON-format wine review data (6,919 records). Top-level keys are string integers; each value is a review object.

| Field | Description |
|-------|-------------|
| `country` | Country of origin |
| `description` | Taster's review text |
| `designation` | Vineyard within the winery where grapes were sourced |
| `points` | Rating score (80–100) |
| `price` | Cost per bottle (USD) |
| `province` | Province or state of origin |
| `region_1` | Specific wine-growing area within province |
| `region_2` | More specific sub-region (not always present) |
| `variety` | Grape variety |
| `winery` | Winery that made the wine |
### `winemag-data_first150k.csv`

Earlier scrape (June 2017); lacks taster name, Twitter handle, and title columns present in v2.

| Column | Description |
|--------|-------------|
| `country` | Country of origin |
| `description` | Taster's review text |
| `designation` | Vineyard within the winery where grapes were sourced |
| `points` | Rating score (80–100) |
| `price` | Cost per bottle (USD) |
| `province` | Province or state of origin |
| `region_1` | Specific wine-growing area within province |
| `region_2` | More specific sub-region (not always present) |
| `variety` | Grape variety |
| `winery` | Winery that made the wine |

## Why this dataset?

Rich real-world NLP dataset pairing free text (sommelier reviews) with structured attributes (variety, country, price, points). Good for text preprocessing, TF-IDF, and sentiment/rating prediction; the price-vs-points scatter plot is a classic EDA exercise. The points distribution also illustrates grade inflation in human-assigned scores, motivating discussion of label quality in ML datasets.

---

## Source description (from Kaggle)

### Context

After watching [Somm](http://www.imdb.com/title/tt2204371/) (a documentary on master sommeliers) I wondered how I could create a predictive model to identify wines through blind tasting like a master sommelier would. The first step in this journey was gathering some data to train a model. I plan to use deep learning to predict the wine variety using words in the description/review. The model still won't be able to taste the wine, but theoretically it could identify the wine based on a description that a sommelier could give. If anyone has any ideas on how to accomplish this, please post them!

### Content


This dataset contains three files:

- **winemag-data-130k-v2.csv** contains 10 columns and 130k rows of wine reviews. 

- **winemag-data_first150k.csv** contains 10 columns and 150k rows of wine reviews.  

- **winemag-data-130k-v2.json** contains 6919 nodes of wine reviews. 

Click on the data tab to see individual file descriptions, column-level metadata and summary statistics.


### Acknowledgements

The data was scraped from [WineEnthusiast](http://www.winemag.com/?s=&drink_type=wine) during the week of June 15th, 2017. The code for the scraper can be found [here](https://github.com/zackthoutt/wine-deep-learning) if you have any more specific questions about data collection that I didn't address.

**UPDATE 11/24/2017**
After feedback from users of the dataset I scraped the reviews again on November 22nd, 2017. This time around I collected the title of each review, which you can parse the year out of, the tasters name, and the taster's Twitter handle. This should also fix the duplicate entry issue.


### Inspiration

I think that this dataset offers some great opportunities for sentiment analysis and other text related predictive models. My overall goal is to create a model that can identify the variety, winery, and location of a wine based on a description. If anyone has any ideas, breakthroughs, or other interesting insights/models please post them.
