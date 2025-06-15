# Data 


# 🧪 PPMI Preprocessing

This folder contains notebooks used to prepare the PPMI dataset for Parkinson’s disease (PD) prediction tasks.

We processed and cleaned MRI, clinical scores, and genotype data to build datasets for two main objectives:

1. **PD Diagnosis Prediction** (MRI + clinical + genotype)
2. **UPDRS Score Prediction** (MRI + DAT-SPECT + APOE4)

---

## 🔄 Workflow Overview

### `PPMI_Preprocessing_1_Baseline.ipynb`
- Merged raw PPMI tables (MRI, clinical, genetic).
- Created subject-level baseline dataset.

### `PPMI_Preprocessing_2_UPDRS.ipynb`
- Cleaned data (removed rows/columns with >40% missing).
- Applied KNN imputation.
- Normalized brain volumes (e.g., `Putamen_Total_norm`).
- Selected relevant features and standardized data.

### `PPMI_Preprocessing_3_ClinicalOnly.ipynb`
- Built dataset using only clinical variables for baseline modeling.

### `PPMI_Preprocessing_4_Imputation_MICE.ipynb`
- Compared imputation strategies (KNN, MICE, mean).
- Chose MICE for complex missingness.

### `PPMI_Preprocessing_5_Feature_Analysis.ipynb`
- Analyzed feature correlations and reduced redundancy.

---

## 📁 Output

Cleaned datasets are saved for modeling tasks (classification/regression) in `experiments/` and `models/`.

---

## 📌 Notes

- Based on data from the Parkinson’s Progression Markers Initiative (PPMI).

