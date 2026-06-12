# Cancer Dataset UAE — Exploratory Data Analysis

A Python-based exploratory data analysis (EDA) project on a cancer patient dataset from the United Arab Emirates, covering 10,000 patients across multiple emirates, cancer types, and demographic groups.

---

## Dataset Overview

**File:** `_cancer_dataset_uae.csv`  
**Rows:** 10,000 patient records  
**Columns:** 20 features

| Column | Description |
|---|---|
| `Patient_ID` | Unique patient identifier |
| `Age` | Patient age |
| `Gender` | Male / Female |
| `Nationality` | Patient nationality |
| `Emirate` | UAE emirate where treatment occurred |
| `Diagnosis_Date` | Date of cancer diagnosis |
| `Cancer_Type` | Type of cancer diagnosed |
| `Cancer_Stage` | Stage at diagnosis (I–IV) |
| `Treatment_Type` | Treatment modality |
| `Treatment_Start_Date` | Date treatment began |
| `Hospital` | Hospital name |
| `Primary_Physician` | Attending physician |
| `Outcome` | Treatment outcome |
| `Death_Date` | Date of death (if applicable) |
| `Cause_of_Death` | Cause of death (if applicable) |
| `Smoking_Status` | Smoking history |
| `Comorbidities` | Existing comorbid conditions |
| `Ethnicity` | Patient ethnicity |
| `Weight` | Weight (kg) |
| `Height` | Height (cm) |

### Key Value Distributions

- **Cancer Types:** Liver, Leukemia, Lung, Pancreatic, Breast, Ovarian, Prostate, Colorectal
- **Cancer Stages:** I, II, III, IV
- **Treatment Types:** Radiation, Surgery, Chemotherapy, Immunotherapy
- **Outcomes:** Recovered (49.3%), Under Treatment (40.8%), Deceased (9.9%)
- **Missing Data:** `Death_Date` and `Cause_of_Death` are null for non-deceased patients; `Comorbidities` has ~40% missing values

---

## Project Structure

```
cancer-dataset-uae/
│
├── _cancer_dataset_uae.csv      # Raw dataset
├── Pyhton_Project.ipynb         # Main analysis notebook
└── README.md
```

---

## Analysis Performed

### 1. Data Inspection & Cleaning
- Loaded and inspected dataset shape, data types, and missing values
- Checked for duplicate records
- Converted `Diagnosis_Date` and `Treatment_Start_Date` to datetime format

### 2. Feature Engineering
- Created age bins using quartile-based thresholds: `young_adult`, `middle_age`, `older_adult`, `elderlies`

### 3. Exploratory Visualizations

**Categorical distributions (bar charts):**
- Gender, Nationality, Emirate, Cancer Type, Outcome, Smoking Status, Comorbidities, Ethnicity

**Numerical distributions (histograms):**
- Age, Weight, Height

**Relationship analysis:**
- Age category distribution
- Outcome by age category
- Outcome by gender (pie charts)
- Outcome by cancer type
- Outcome by smoking status
- Outcome by comorbidities

**Correlation analysis:**
- Heatmap of numerical features (Age, Weight, Height)

---

## Requirements

```
pandas
numpy
matplotlib
seaborn
```

Install with:

pip install pandas numpy matplotlib seaborn


## Author

Project by Shruti Nair
