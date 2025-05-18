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

---------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🧠 ANN Model – Experiment 2

Follow-up experiment focused on addressing class imbalance and improving interpretability. SMOTE was applied to improve classification of underrepresented classes (e.g., Dementia), and SHAP was introduced to explain model predictions. A Logistic Regression baseline was added for comparison.

## 🔍 Features Used
- **Age** (Demographic)
- **APOE4** status (Genetic risk factor)
- **MMSE**, **CDRSB** (Clinical scores)
- **Hippocampus/ICV** (MRI biomarker)

## 🧱 Model Architecture
- Shallow ANN with 2 hidden layers + dropout
- Output: 3-class softmax
- Loss: Categorical crossentropy
- Optimizer: Adam
- Compared with Logistic Regression

## ⚖️ Class Imbalance Handling
- Applied **SMOTE** to oversample Dementia cases
- Improved recall and precision for minority class, though still room for improvement

## 📊 Results
- **ANN Accuracy**: ~91%
- **Logistic Regression**: Comparable accuracy but lower performance in non-linear class boundaries
- **Key drivers** (via SHAP): CDRSB, MMSE, Hippocampus/ICV
- **APOE4**: Least impactful feature

## 🧠 Interpretability
- Applied **SHAP** for feature attribution
- Validated clinical relevance of top features
- Helped build trust in model decisions

## 🔄 Next Steps
- Expand MRI biomarkers (e.g., Cortical Thickness, Ventricular Volume)
- Test more complex ANN architectures and classical models (e.g., Random Forest)
- Apply cross-validation for robustness

