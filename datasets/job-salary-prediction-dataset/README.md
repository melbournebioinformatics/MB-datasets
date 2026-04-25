# Data: Job Salary Prediction Dataset

A large-scale dataset for analyzing job roles, experience, skills, and salary.

## File

| File | Size | Description |
|------|------|-------------|
| `job_salary_prediction_dataset.csv` | 16 MB | — |

## Download

```bash
kaggle datasets download -d nalisha/job-salary-prediction-dataset -p data --unzip
```

```python
from kaggle.api.kaggle_api_extended import KaggleApi
api = KaggleApi(); api.authenticate()
api.dataset_download_files("nalisha/job-salary-prediction-dataset", path="data", unzip=True)
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/nalisha/job-salary-prediction-dataset

Original source: nalisha (Kaggle)

**Citation:**
> Nalisha (2024). *Job Salary Prediction Dataset* [Synthetic dataset]. Kaggle. https://www.kaggle.com/datasets/nalisha/job-salary-prediction-dataset
> Note: Synthetically generated for ML practice.

## License

CC0-1.0

## Columns

### `job_salary_prediction_dataset.csv`

| Column | Description |
|--------|-------------|
| `job_title` | Job role or position (e.g., Data Analyst, AI Engineer) |
| `experience_years` | Number of years of professional experience |
| `education_level` | Highest education level completed |
| `skills_count` | Number of technical or professional skills listed |
| `industry` | Industry sector |
| `company_size` | Size of the company: small, medium, or large |
| `location` | Job location or region |
| `remote_work` | Whether the role allows remote work |
| `certifications` | Number of professional certifications held |
| `salary` | Annual salary in USD (target variable) |

## Why this dataset?

Large regression dataset (250,000 rows, 10 features) with a mix of categorical, binary, and numeric inputs. Good for feature engineering, encoding strategies, and benchmarking regression models. The range of salary-influencing features supports discussion of confounders and multicollinearity; the synthetic origin means no privacy concerns when used in classroom settings.

---

## Source description (from Kaggle)

This dataset contains 250,000 job records designed for salary prediction, data analysis, and machine learning projects.

It includes information about job titles, experience level, education background, skills, industry type, company size, and work location. The dataset helps researchers and data scientists explore how different factors influence salary.

#### It can be used for:
- Salary prediction models
- Exploratory data analysis (EDA)
- Machine learning practice
- Data visualization projects
- Career and industry salary insights

| Column               | Description                                                |
| -------------------- | ---------------------------------------------------------- |
| **job_title**        | The job role or position (e.g., Data Analyst, AI Engineer) |
| **experience_years** | Number of years of professional experience                 |
| **education_level**  | Highest level of education completed                       |
| **skills_count**     | Number of technical or professional skills                 |
| **industry**         | Industry sector where the job belongs                      |
| **company_size**     | Size of the company (small, medium, large)                 |
| **location**         | Job location or region                                     |
| **remote_work**      | Whether the job allows remote work                         |
| **certifications**   | Number of professional certifications                      |
| **salary**           | Annual salary of the employee                              |
