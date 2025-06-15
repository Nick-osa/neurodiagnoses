-- For datasets or CSVs used --

# Neurodegenerative Disease Prediction with ANNs

## Goals
Develop an **Artificial Neural Network (ANN)** to predict clinical scores of neurodegenerative diseases, improving upon our existing RandomForestClassifier model by incorporating:
- Clinical cognitive scores (MMSE, CDRSB)
- Neuroimaging data (MRI, PET)
- Fluid biomarkers (CSF, plasma)
- Genetic risk factors (APOE4)

## Dataset Strategy

### Primary Dataset: ADNIMERGE
**Rationale**: Curated Alzheimer's Disease Neuroimaging Initiative (ADNI) data with harmonized variables across phases.

#### Key Features:
| Category          | Variables                          |
|-------------------|-----------------------------------|
| Clinical          | DX (CN/MCI/AD), MMSE, CDR-SOB     |
| Demographics      | Age, Sex, Education               |
| Genetics          | APOE4 genotype                    |
| MRI               | Hippocampal volume, ICV           |
| PET               | Amyloid (AV45), FDG-PET           |
| CSF Biomarkers    | Aβ42, p-Tau, t-Tau                |

### Supplementary Datasets
- **TADPOLE**: For hyperparameter tuning
- **OASIS**: Additional imaging validation

## Data Availability Report

### Missingness Summary
1. **Clinical (N=~1,500)**:
   - `DX`/`MMSE`/`CDRSB`: 30% missing  
   *Action: Impute using diagnosis-stratified medians*
   
2. **MRI (N=~800)**:
   - Hippocampal volume: 46% missing  
   *Action: Baseline-carried-forward imputation*

3. **PET/CSF (N=~200)**:
   - Amyloid PET: 81% missing  
   - CSF Aβ42: 86% missing  
   *Action: Exclude from initial model*

4. **Genetics**:
   - APOE4: 2% missing  
   *Action: Forward-fill longitudinal data*

