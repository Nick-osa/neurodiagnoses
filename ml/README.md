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

### Alternative Format Using Icons (More Visual)
```markdown
## 📁 Project Structure

| Directory | Description |
|-----------|-------------|
| **📂 data/** | Datasets and processed data |
| &nbsp;&nbsp;&nbsp;📂 ADNI/ | Alzheimer's Disease Neuroimaging Initiative data |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 processed/ | Cleaned and processed ADNI datasets |
| &nbsp;&nbsp;&nbsp;📂 PPMI/ | Parkinson's Progression Markers Initiative data |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 processed/ | Cleaned and processed PPMI datasets |
| &nbsp;&nbsp;&nbsp;📄 README.md | Data documentation |
| **📂 docs/** | Project documentation |
| &nbsp;&nbsp;&nbsp;📂 clinical_background/ | Clinical context |
| &nbsp;&nbsp;&nbsp;📂 methods/ | Research methodologies |
| &nbsp;&nbsp;&nbsp;📂 results/ | Experimental findings |
| &nbsp;&nbsp;&nbsp;📄 README.md | Documentation overview |
| **📂 notebooks/** | Jupyter notebooks |
| &nbsp;&nbsp;&nbsp;📂 data_processing/ | Data transformation notebooks |
| &nbsp;&nbsp;&nbsp;📂 demos/ | Demonstration notebooks |
| &nbsp;&nbsp;&nbsp;📂 exploratory/ | Exploratory data analysis |
| &nbsp;&nbsp;&nbsp;📄 README.md | Notebooks guide |
| **📂 src/** | Production source code |
| &nbsp;&nbsp;&nbsp;📂 data_processing/ | Data pipelines |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ADNI/ | ADNI processing scripts |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 PPMI/ | PPMI processing scripts |
| &nbsp;&nbsp;&nbsp;📂 evaluation/ | Model evaluation |
| &nbsp;&nbsp;&nbsp;📂 modelling/ | ML models |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📄 adni_csf_prediction.py | CSF biomarker prediction |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📄 adni_ad_diagnosis.py | Alzheimer's diagnosis |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📄 ppmi_regression.py | UPDRS III regression |
| **📄 .gitignore** | Specifies untracked files |
| **📄 Dockerfile** | Container configuration |
| **📄 Makefile** | Automation commands |
| **📄 README.md** | Project overview |
| **📄 requirements.txt** | Python dependencies |
