-- Saved models and different test runs --

# ANN Model Experiment 1

First in a controlled series testing Alzheimer's classification efficacy using ADNIMERGE data.Evaluates minimal architecture (2 hidden layers) with core MRI/clinical features (hippocampus, MMSE, APOE4).Excludes PET/CSF biomarkers and advanced architectures to isolate foundational performance metrics.Establishes accuracy ceiling for subsequent complexity/feature enhancements in later experiments.

# Alzheimer's Disease Prediction with Shallow Artificial Neural Network

A shallow Artificial Neural Network (ANN) for predicting Alzheimer's Disease progression stages (CN, MCI, Dementia) using MRI biomarkers and clinical data from the ADNI dataset.

## Table of Contents
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Future Improvements](#future-improvements)


## Dataset
The model uses the ** Cleaned ADNIMERGE Dataset** containing baseline measurements from Alzheimer's Disease Neuroimaging Initiative:
- MRI biomarkers (hippocampal volume normalized by intracranial volume)
- Clinical scores (MMSE, CDRSB)
- Demographic data (age)
- Genetic risk factor (APOE4 status)

Preprocessed dataset: `ADNI_baseline_clean.csv` ([ADNI Data Dictionary](https://adni.loni.usc.edu/data-samples/data-dictionary/))

## Features
### Input Features
| Feature          | Description                                | Type    |
|------------------|--------------------------------------------|---------|
| AGE              | Patient age at baseline                    | Numeric |
| MMSE             | Mini-Mental State Examination score       | Numeric |
| CDRSB            | Clinical Dementia Rating Sum of Boxes     | Numeric |
| APOE4            | Apolipoprotein E ε4 allele status         | Binary  |
| Hippocampus_ICV  | Hippocampal volume normalized by ICV      | Numeric |

### Target Variable
| Class | Label | Description          |
|-------|-------|----------------------|
| CN    | 0     | Cognitively Normal   |
| MCI   | 1     | Mild Cognitive Impairment |
| Dementia | 2  | Alzheimer's Dementia |

## Installation
1. Clone repository:
```bash
git clone https://github.com/Nick-osa/alzheimer-prediction-ann.git
cd alzheimer-prediction-ann

## Usage
python train_model.py

# Trained ANN model: models/adni_ann_model.h5
# ANN_model_experiment1.ipynb

# Outputs: ANN_model_experiment1.ipynb , Model: adni_ann_model.h5 (Keras HDF5 format), Scaler: scaler.pkl (Joblib-pickled StandardScaler)

# How to access
  - python file
 
# Load model
  from tensorflow.keras.models import load_model
  loaded_model = load_model("adni_ann_model.h5")

# Load scaler
  import joblib
  loaded_scaler = joblib.load("scaler.pkl")

## Model Architecture

Sequential(
    Dense(32, activation='relu', input_shape=(5,)),  # Input: 5 features
    Dropout(0.2),                                     # Regularization
    Dense(16, activation='relu'),                     # Hidden layer
    Dense(3, activation='softmax')                    # Output: CN/MCI/Dementia
)

## Results

- Accuracy: 92% (414-sample test set)

# Class Performance:

CN (Normal): 0.98 F1-score (157/160 correct)

MCI: 0.84 F1-score (61/68 recall, 78% precision)

Dementia: 0.91 F1-score (164/186 correct)

Limitation: MCI↔Dementia confusion (24 misclassifications)

## Future Improvemets

- Address class imbalance with Resampling techniques and SMOTE 
- Add neuroimaging features (FDG-PET, amyloid PET)
- Improve ANN models i.e  gradient boosting ensembles

