# Data Preprocessing

This folder contains scripts for cleaning and preparing raw data.

The ADNIMERGE has characteristic missingness of data. our plan is to progressively create models around the most available dataset.

Clinical Data
Low missingness (<3%): PTID, VISCODE, AGE, APOE4 

Moderate missingness (~30%): DX, MMSE, CDRSB 

MRI Data
High missingness (40-50%): Hippocampus/Entorhinal volumes 

PET/CSF Biomarkers
Very high missingness (75-85%): AV45, ABETA, TAU 

# Plan
Implemet the models in phases based around data availability

1. Use clinical + genetic data (AGE, APOE4, MMSE, CDRSB) with diagnosis-stratified imputation.

2. Add MRI data for reduced but richer dataset.

3. Exclude PET/CSF unless doing targeted biomarker studies.

# Workflow

## Scripts
- `ADNIMERGE_PREPROCESSING.py` - Examine data for missingness to select features
- `Visualize_neurodegenerative_biomakers.py` - Visualize how key biomakers affect AD progression and outcomes
- `ADNI_baseline_clean_csv.py` - Outputs a clean df with sime selected MRI and genetic features for initial test ML model


*ADNI_baseline_clean_csv.py*


Data Cleaning for ADNI
This script prepares a clean subset of the ADNIMERGE dataset (from the Alzheimer's Disease Neuroimaging Initiative) for machine learning tasks. It focuses on extracting baseline data (VISCODE == 'bl') and selecting biologically relevant features including demographics, clinical scores, imaging biomarkers, and genotype data.


Key Steps:

Selects relevant features: AGE, APOE4, Hippocampus, ICV, MMSE, CDRSB, DX.

Normalizes hippocampal volume using intracranial volume (Hippocampus_ICV).

Stratified median imputation for MMSE and CDRSB by diagnosis (DX).

Encodes missing APOE4 values using the most frequent value per diagnosis group.

Removes rows missing critical features (DX, APOE4, Hippocampus_ICV).

Verifies missing values and retains a clean, analysis-ready dataset.

Exports a final .csv file for downstream ML modeling.

Output:

ADNI_baseline_clean.csv: Cleaned and preprocessed baseline data.



## Usage
```bash
python clean_data.py input.csv output_clean.csv
```

## Requirements
- Python 3.8+
- pandas library
