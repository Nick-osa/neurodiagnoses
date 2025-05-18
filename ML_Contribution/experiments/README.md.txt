## 🧪 General Experiment Overview

This repository presents a series of machine learning experiments for the **early prediction of Alzheimer's Disease (AD)** using **non-invasive features**. The aim is to identify scalable biomarkers and high-performing models that minimize reliance on invasive or subjective measures such as CSF tests or clinical scores.

### 🎯 Objectives
- Classify cognitive stages (CN, MCI, Dementia) using non-invasive data  
- Benchmark shallow ANNs and classical ML models  
- Ensure clinical relevance and interpretability (via SHAP)

### 🔁 Experiment Roadmap

| Experiment | Description           | Features Used                             |
|-----------:|------------------------|--------------------------------------------|
| 1          | Baseline ANN           | Age, APOE4, MMSE, CDRSB, Hippocampus/ICV   |
| 2          | Non-invasive only      | Age, APOE4, MRI biomarkers only            |
| 3          | Expanded MRI features  | Cortical thickness, ventricular volume, etc. |
| 4+         | Model comparisons      | Classical ML models (RF, SVM, etc.)        |

### 📊 Evaluation
- Accuracy, confusion matrix, class-wise performance  
- Feature importance via SHAP for explainability



# 🧠 ANN Model – Experiment 1

Baseline experiment using a shallow Artificial Neural Network (ANN) to classify Alzheimer's stages (CN, MCI, Dementia) from the cleaned ADNIMERGE dataset.

## 🔍 Features Used
- **Age** (Demographic)
- **APOE4** status (Genetic risk factor)
- **MMSE**, **CDRSB** (Clinical scores)
- **Hippocampus/ICV** (MRI biomarker)

## 🧱 Model Architecture
- Shallow ANN with 2 hidden layers
- Output: 3-class softmax
- Loss: Categorical crossentropy
- Optimizer: Adam

## 📊 Results
- **Accuracy**: ~91%
- **Key drivers** (via SHAP): MMSE, Hippocampal volume
- Establishes baseline for future experiments with expanded features and model depth

# 🧠 ANN Model – Experiment 2
