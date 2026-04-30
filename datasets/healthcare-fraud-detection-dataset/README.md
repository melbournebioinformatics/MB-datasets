# Data: Healthcare Fraud Detection Dataset

Realistic medical insurance claims dataset with ICD-10, CPT codes.

## File

| File | Size | Description |
|------|------|-------------|
| `healthcare_fraud_detection.csv` | 1 MB | — |

## Download

```bash
# wget
wget https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/healthcare-fraud-detection-dataset/healthcare_fraud_detection.csv

# curl
curl -O https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/healthcare-fraud-detection-dataset/healthcare_fraud_detection.csv
```

```python
# Python / pandas
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/healthcare-fraud-detection-dataset/healthcare_fraud_detection.csv")
```

```r
# R
df <- read.csv("https://raw.githubusercontent.com/melbournebioinformatics/MB-datasets/main/datasets/healthcare-fraud-detection-dataset/healthcare_fraud_detection.csv")
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/nudratabbas/healthcare-fraud-detection-dataset

Original source: nudratabbas (Kaggle)

**Citation:**
> Abbas, N. (2024). *Healthcare Fraud Detection Dataset* [Synthetic dataset]. Kaggle. https://www.kaggle.com/datasets/nudratabbas/healthcare-fraud-detection-dataset
> Note: Data is synthetically generated to replicate real-world billing and fraud patterns.

## License

CC0-1.0

## Columns

### `healthcare_fraud_detection.csv`

| Column | Description |
|--------|-------------|
| `claim_amount` | Total billed amount for the claim |
| `approved_amount` | Amount approved by the insurer |
| `claim_status` | Claim outcome: approved, rejected, or pending |
| `insurance_type` | Coverage type: private, Medicare, Medicaid, or self-pay |
| `patient_age` | Patient age in years |
| `patient_gender` | Patient gender |
| `state` | US state of the patient |
| `chronic_condition` | Binary flag for presence of a chronic condition |
| `prior_visits` | Number of prior visits in the last 12 months |
| `provider_id` | Unique provider identifier |
| `provider_specialty` | Medical specialty (cardiology, orthopedics, general practice, etc.) |
| `monthly_claim_volume` | Provider's monthly claim submission count |
| `diagnosis_code` | ICD-10 diagnosis code |
| `procedure_code` | CPT procedure code |
| `claim_submission_date` | Date the claim was submitted |
| `days_to_submit` | Days between service date and claim submission |
| `length_of_stay` | Inpatient length of stay in days |
| `visit_type` | Outpatient, inpatient, or emergency |
| `Is_Fraud` | Target variable: 1 = fraudulent claim, 0 = legitimate (~8% positive rate) |

## Why this dataset?

Synthetic tabular dataset (10,000 claims) with realistic class imbalance (~8% fraud rate), intentional missing values, and mixed feature types. Ideal for teaching imbalanced classification (SMOTE, class weighting), threshold selection, and explainability (SHAP). ICD-10 and CPT codes introduce students to medical coding vocabularies without exposing real patient data.

---

## Source description (from Kaggle)

Healthcare fraud is a significant challenge for insurance providers and healthcare systems worldwide, leading to billions in financial losses each year and increasing the cost of care for patients. Detecting fraudulent claims is difficult because fraudulent behavior often mimics legitimate medical activity while exploiting subtle inefficiencies in billing systems.

Studies and industry reports suggest:

- Healthcare fraud accounts for an estimated 3–10 percent of total healthcare spending
- Fraudulent claims are often embedded within large volumes of legitimate transactions
- High-cost claims and abnormal provider behavior are common indicators of fraud
- Early detection can significantly reduce financial losses and operational inefficiencies

Understanding which claims are potentially fraudulent, and why, allows organizations to:

- Improve fraud detection systems using data-driven approaches
- Reduce financial losses and claim leakage
- Enhance auditing and compliance processes
- Allocate investigative resources more effectively
- Strengthen trust in healthcare systems

## Content

This dataset contains 10,000 healthcare insurance claims designed to replicate real-world billing and fraud patterns. It includes a mix of patient, provider, and financial features suitable for classification tasks.

## Claim and Financial Information

- Claim amount and approved amount
- Claim status such as approved, rejected, or pending
- Insurance type including private, Medicare, Medicaid, and self-pay
- Log-normal distribution of claim values to reflect real billing patterns

## Patient Information

- Patient age and gender
- State-level geographic information
- Chronic condition indicator
- Prior visit history within the last 12 months

## Provider Information

- Unique provider identifiers
- Provider specialty such as cardiology, orthopedics, and general practice
- Monthly claim volume per provider

## Medical Coding

- Diagnosis codes based on ICD-10 standards
- Procedure codes based on CPT standards
- Realistic relationships between diagnoses and procedures

## Temporal Features

- Claim submission date
- Days between service and claim submission

## Additional Features

- Length of stay for inpatient cases
- Visit type such as outpatient, inpatient, or emergency

## Target Variable

- Is_Fraud
       0 indicates a legitimate claim
       1 indicates a fraudulent claim
- Fraud rate is approximately 8 percent, reflecting real-world imbalance

## Realism and Data Characteristics

This dataset is designed to include meaningful and realistic fraud patterns:
- Fraudulent claims tend to have higher claim amounts
- Fraud cases are often submitted with shorter delays after service
- Certain providers show higher concentrations of fraudulent activity
- Approved amounts vary and do not directly reveal fraud status
- Non-fraud cases include natural variability and noise

A small percentage of missing values has been introduced in selected columns to simulate real-world data imperfections.

## Inspiration and Use Cases

This dataset enables a wide range of applications for Kaggle users and data practitioners:

- Fraud Detection Modeling
- Imbalanced Learning
- Feature Engineering  
- Explainable AI
- Use SHAP or similar methods to interpret model decisions and understand fraud drivers.
- Analyze provider behavior, claim patterns, and system inefficiencies.

## Ideal For

- Data scientists and machine learning practitioners
- Healthcare analysts and researchers
- Students learning classification and anomaly detection
- Kaggle users building portfolio projects
- Anyone interested in fraud detection using tabular data
