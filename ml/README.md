**ML pipelines for stratifying neurological biomarkers and predicting disease progression using multi-modal data from ADNI and PPMI cohorts.**

## Project Overview
This research initiative as part of a Master thesis with Fundació de Neurosciences, develops non-invasive diagnostic tools for Alzheimer's and Parkinson's diseases. Our work focuses on:

1. **CSF Biomarker Stratification**  
   Predicting ABETA, pTau, and tTau positivity using:
   - MRI imaging features
   - Cognitive assessments
   - Demographic data
   - Genotypic markers  
   *(ADNI cohort)*

2. **Motor Score Prediction (UPDRS III)**
   Forecasting Parkinson's disease progression(UPDRS III motor scores) using:
   - DAT-SPECT imaging
   - MRI features
   - Genotypic data  
   *(PPMI cohort)*

4. **AD prediction with shallow ANNs**
   Exploring the masking by clinical data of other features predicting AD:
   - MRI imaging features
   - Cognitive assessments
   - Demographic data
   - Genotypic markers  
   *(ADNI cohort)*

## Key Features
- Multi-modal data integration (imaging + clinical + genetic)
- Biomarker ratio analysis for clinical trial triage
- Predictive modeling of disease progression

## Project Structure

- **data/**
  - ADNI/ - Alzheimer's data
    - processed/ - Processed datasets
  - PPMI/ - Parkinson's data
    - processed/ - Processed datasets
  - README.md - Data documentation
  
- **docs/**
  - clinical_background/ - Clinical context
  - methods/ - Research methodologies
  - results/ - Experimental findings
  - README.md - Documentation overview

- **notebooks/**
  - data_processing/ - Transformation notebooks
  - demos/ - Demonstration notebooks
  - exploratory/ - EDA notebooks
  - README.md - Notebooks guide

- **src/**
  - data_processing/ - Data pipelines
    - ADNI/ - ADNI processing scripts
    - PPMI/ - PPMI processing scripts
  - evaluation/ - Model evaluation
  - modelling/ - ML models
    - adni_csf_prediction.py - CSF biomarker prediction
    - adni_ad_diagnosis.py - Alzheimer's diagnosis
    - ppmi_regression.py - UPDRS III regression

- **Files**
  - .gitignore - Untracked files
  - Dockerfile - Container config
  - Makefile - Automation
  - README.md - Project overview
  - requirements.txt - Dependencies

