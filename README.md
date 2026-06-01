# Alzheimer's Disease Progression Prediction
Predicting conversion from Mild Cognitive Impairment (MCI) to 
Alzheimer's Disease using longitudinal brain MRI scans.

## Overview
Built a hybrid 3D CNN-LSTM deep learning architecture on real 
clinical data from the ADNI dataset to classify whether a patient's 
MCI will remain stable or convert to Alzheimer's Disease over time.

## Architecture
- 3D CNN — extracts spatial features from each MRI volume
- LSTM — models how those features evolve across timepoints
- Grad-CAM — highlights high-risk brain regions driving predictions

## Dataset
- Source: ADNI (Alzheimer's Disease Neuroimaging Initiative)
- 218 subjects (109 Stable MCI, 109 Converting to AD)
- Format: NIfTI (.nii.gz) longitudinal MRI scans

## Results
| Metric | Score |
|--------|-------|
| Test AUC-ROC | 0.73 |
| Test Accuracy (tuned) | 0.73 |
| Trainable Parameters | 649,154 |

## Tech Stack
Python · PyTorch · Scikit-learn · NiBabel · NumPy · Matplotlib

## How to Run
1. Open `alzheimers_cnn_lstm.ipynb` in Google Colab
2. Set runtime to GPU (Runtime → Change runtime type → T4 GPU)
3. Mount Google Drive and update dataset file paths
4. Run all cells sequentially
