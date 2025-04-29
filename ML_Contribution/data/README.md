-- For datasets or CSVs used --

Goals

Our immediade goals include using Artificial Neural Networks to create a model that cam predict clinical scores of neurodegenerative diseases. This is in tandem with the already deployed RandomForestClassifier model.
  
Our dataset would also include genetic information as an improvement to the previouse RandomForestClassifier model.

To acheieve this the data set must:

Contain clinical labels (e.g., cognitive scores like MMSE)

Include neuroimaging data (MRI, PET, fMRI, etc.)

Include fluid biomarkers (blood, plasma, CSF)

Include genetic information (like APOE4, SNPs)


Datasets
1. ADNI (Alzheimer’s Disease Neuroimaging Initiative)
Rationale: - ADNI is specifically designed for Alzheimer's diagnosis/progression research
           - Consists of the ground truth of our proposed ANN model and includes clinical scores like MMSE/CDR.

2. TADPOLE Challenge Dataset
Rationale  - Augment the ADNI datasets and used for futher model benchmaking and tunning of hyperparametes

3. OASIS (Open Access Series of Imaging Studies)
Rationale - Additional Imaging Data

CSVs would be dounloaded once access is approved.

ADNI.

At first we are going to concentrate on the ADNI dataset specifically the ADNIMERGE dataset.
ADNIMERGE - The ADNIMERGE dataset is a curated, standardized collection of data from the Alzheimer’s Disease Neuroimaging Initiative (ADNI), designed to facilitate research on Alzheimer’s disease (AD). 

Key Features of ADNIMERGE:
Data Integration:

Combines clinical, cognitive, MRI, PET, and biomarker data (e.g., CSF Aβ/tau) from ADNI phases (1, GO, 2, 3).

Harmonized variables across different ADNI cohorts for consistency.

Common Variables:

Diagnosis: Labels like CN (Cognitively Normal), MCI (Mild Cognitive Impairment), and AD.

Demographics: Age, sex, education, APOE genotype.

Cognitive Scores: MMSE, ADAS-Cog, CDR-SB.

MRI/PET Biomarkers: Hippocampal volume, amyloid PET (AV45/Florbetapir), FDG-PET.

Format:

Structured as an R data frame (.rda file), widely used in statistical analysis.

Includes longitudinal data (multiple time points per subject).

Purpose:

Simplifies data access for researchers studying AD progression, predictive modeling, or biomarker validation.

-- Then we proceed to Pre-process and clean the ADNIMERGE Dataset and clean the dataset.--
