# Data: Pima Indians Diabetes Database

Predict the onset of diabetes based on diagnostic measures

## File

| File | Size | Description |
|------|------|-------------|
| `diabetes.csv` | 23 KB | — |

## Download

```bash
kaggle datasets download -d uciml/pima-indians-diabetes-database -p data --unzip
```

```python
from kaggle.api.kaggle_api_extended import KaggleApi
api = KaggleApi(); api.authenticate()
api.dataset_download_files("uciml/pima-indians-diabetes-database", path="data", unzip=True)
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database

Original source: uciml (Kaggle)

**Citation:**
> Smith, J.W., Everhart, J.E., Dickson, W.C., Knowler, W.C., & Johannes, R.S. (1988). Using the ADAP learning algorithm to forecast the onset of diabetes mellitus. *In Proceedings of the Symposium on Computer Applications and Medical Care* (pp. 261–265). IEEE Computer Society Press.

## License

CC0-1.0

## Columns

### `diabetes.csv`

| Column | Description |
|--------|-------------|
| `Pregnancies` | Number of times pregnant |
| `Glucose` | Plasma glucose concentration (2-hour oral glucose tolerance test) |
| `BloodPressure` | Diastolic blood pressure (mm Hg) |
| `SkinThickness` | Triceps skinfold thickness (mm) |
| `Insulin` | 2-hour serum insulin (µU/mL) |
| `BMI` | Body mass index (weight kg / height m²) |
| `DiabetesPedigreeFunction` | Diabetes pedigree function (genetic risk score) |
| `Age` | Age in years |
| `Outcome` | Class label: 1 = diabetic, 0 = non-diabetic |

## Why this dataset?

Classic binary classification benchmark (768 samples, 8 features, ~35% positive class). Small enough to iterate quickly; imbalanced enough to motivate precision/recall over accuracy. Good entry point for supervised ML, feature selection, and threshold tuning in a biomedical context.

---

## Source description (from Kaggle)

## Context

This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage.

## Content

The datasets consists of several medical predictor variables and one target variable, `Outcome`. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

## Acknowledgements

Smith, J.W., Everhart, J.E., Dickson, W.C., Knowler, W.C., & Johannes, R.S. (1988). [Using the ADAP learning algorithm to forecast the onset of diabetes mellitus][1]. *In Proceedings of the Symposium on Computer Applications and Medical Care* (pp. 261--265). IEEE Computer Society Press.

## Inspiration

Can you build a machine learning model to accurately predict whether or not the patients in the dataset have diabetes or not?

  [1]: http://rexa.info/paper/04587c10a7c92baa01948f71f2513d5928fe8e81
