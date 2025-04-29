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
- `clean_data.py` - Removes missing values
- `normalize.py` - Scales numerical features

## Usage
```bash
python clean_data.py input.csv output_clean.csv
```

## Requirements
- Python 3.8+
- pandas library
