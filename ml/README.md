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
├── data/ # Datasets and processed data
│ ├── ADNI/ # Alzheimer's Disease Neuroimaging Initiative data
│ │ └── processed/ # Cleaned and processed ADNI datasets
│ ├── PPMI/ # Parkinson's Progression Markers Initiative data
│ │ └── processed/ # Cleaned and processed PPMI datasets
│ └── README.md # Data documentation and descriptions
│
├── docs/ # Comprehensive project documentation
│ ├── clinical_background/ # Clinical context and disease background
│ ├── methods/ # Research methodologies and protocols
│ ├── results/ # Experimental findings and visualizations
│ └── README.md # Documentation overview
│
├── notebooks/ # Jupyter notebooks for exploration
│ ├── exploratory/ # Exploratory data analysis (EDA)
│ └── README.md # Notebooks guide
│
├── src/ # **Main**
│ ├── data_processing/ # Data processing pipelines
│ │ ├── ADNI/ # ADNI-specific processing scripts
│ │ └── PPMI/ # PPMI-specific processing scripts
│ ├── evaluation/ # Model evaluation and metrics
│ └── modelling/ # Machine learning models
│ ├── adni_csf_prediction.py # CSF biomarker prediction (ADNI)
│ ├── adni_ad_diagnosis.py # Alzheimer's diagnosis models (ADNI)
│ └── ppmi_regression.py # UPDRS III regression (PPMI)
│
├── .gitignore # Specifies untracked files
├── Dockerfile # Container configuration
├── Makefile # Automation commands
├── README.md # Project overview (this file)
└── requirements.txt # Python dependencies
