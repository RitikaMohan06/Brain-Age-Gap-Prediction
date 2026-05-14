# Brain Age Prediction from Structural MRI Using Deep Learning for Early Neurodegenerative Risk Assessment

##  Project Overview

This project focuses on predicting brain age from structural MRI scans using Deep Learning techniques. The main objective is to estimate a subject’s biological brain age and analyze the Brain Age Gap (difference between predicted age and actual chronological age), which can act as a biomarker for early neurodegenerative diseases such as Alzheimer’s disease and dementia.

The project uses publicly available MRI datasets and implements a Transfer Learning-based Convolutional Neural Network (CNN) using the ResNet50 architecture in Python.

---

# Objectives

- Predict brain age from MRI scans using Deep Learning
- Analyze structural brain aging patterns
- Perform MRI preprocessing and feature extraction
- Evaluate prediction performance using regression and classification metrics
- Generate visualizations for research and journal publication
- Study Brain Age Gap for neurodegenerative risk assessment

---

# Problem Statement

Chronological age does not always reflect the actual biological condition of the brain. Structural changes in the brain may indicate accelerated aging caused by neurodegenerative diseases. Manual analysis of MRI scans is time-consuming and dependent on expert interpretation.

This project aims to automate brain age prediction using Deep Learning to provide:
- early neurodegenerative risk assessment
- scalable MRI analysis
- AI-assisted clinical support

---

# Dataset Used

The project uses publicly available structural MRI datasets:

## Recommended Datasets
1. IXI Dataset  
https://brain-development.org/ixi-dataset/

2. OASIS Dataset  
https://www.oasis-brains.org/

3. NKI-RS Dataset  
https://fcon_1000.projects.nitrc.org/indi/pro/nki.html

---

# Dataset Structure

BrainAgeProject/
│
├── data/
│   ├── subject1.nii
│   ├── subject2.nii
│   ├── ...
│
├── metadata.csv
├── BrainAgePrediction.ipynb
└── README.md

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| PyTorch | Deep Learning Framework |
| NumPy | Numerical Operations |
| Pandas | Data Handling |
| Matplotlib | Visualization |
| Seaborn | Statistical Graphs |
| Scikit-learn | Metrics & Evaluation |
| NiBabel | MRI File Processing |
| ResNet50 | Transfer Learning CNN |

---

#  Methodology

## 1. MRI Data Collection
Structural MRI scans are collected from public neuroimaging repositories.

## 2. Preprocessing
The MRI scans are:
- normalized
- resized
- converted into 2D slices
- transformed into 3-channel images

## 3. Feature Extraction
Transfer learning is performed using pretrained ResNet50 architecture.

## 4. Model Training
The model learns the mapping between MRI features and chronological age.

## 5. Prediction
The trained model predicts the brain age for unseen MRI scans.

## 6. Evaluation
Performance is evaluated using:
- Mean Absolute Error (MAE)
- Accuracy
- F1 Score
- Confusion Matrix
- Heatmaps and Statistical Graphs

---

# Why MRI Slices Were Converted to 3 Channels

MRI images are grayscale (single-channel), but pretrained CNN models like ResNet50 are trained on RGB images with 3 channels.

To utilize transfer learning effectively, the grayscale MRI slice is duplicated across 3 channels so that it matches the expected input shape of the pretrained model.

---

# Proposed Model Architecture

MRI Slice
     ↓
Preprocessing
     ↓
ResNet50 Convolution Layers
     ↓
Residual Blocks
     ↓
Feature Extraction
     ↓
Fully Connected Regression Layer
     ↓
Predicted Brain Age

---

# Evaluation Metrics

## Mean Absolute Error (MAE)

MAE = (1/N) Σ |y - ŷ|

Measures average prediction error in years.

## Accuracy

Used after converting age into age-group classes.

## F1 Score

Balances precision and recall for classification evaluation.

---

# 📈 Visualizations Included

The project generates:
- Training Loss Curve
- Actual vs Predicted Scatter Plot
- Error Distribution Plot
- Brain Age Gap Histogram
- Confusion Matrix
- Correlation Heatmap
- Performance Metrics Bar Chart

---

#  How to Run the Project

## Step 1: Install Dependencies

pip install torch torchvision nibabel pandas numpy matplotlib seaborn scikit-learn

---

## Step 2: Open Jupyter Notebook

Using Anaconda Navigator:
- Launch Jupyter Notebook
- Open project folder
- Open BrainAgePrediction.ipynb

---

## Step 3: Run All Cells

Run notebook cells sequentially.

---

#  Sample Output

Actual Age: 65 | Predicted Age: 67
Actual Age: 40 | Predicted Age: 42

---

# Expected Performance

| Metric | Expected Range |
|---|---|
| MAE | 5–12 years |
| Accuracy | 70–85% |
| F1 Score | 0.70–0.85 |

---

#  Brain Age Gap

Brain Age Gap = Predicted Age - Actual Age

A higher positive gap may indicate accelerated brain aging and possible neurodegenerative risk.

---

#  Future Improvements

- Use 3D CNN architectures
- Integrate multimodal MRI data
- Apply Explainable AI (Grad-CAM)
- Train on larger datasets
- Hyperparameter optimization
- Clinical disease classification

---

#  References

1. Cole JH et al., “Predicting brain age with deep learning from raw imaging data,” NeuroImage, 2017.  
https://doi.org/10.1016/j.neuroimage.2017.07.059

2. He K et al., “Deep Residual Learning for Image Recognition,” CVPR, 2016.  
https://arxiv.org/abs/1512.03385

3. Franke K et al., “BrainAGE biomarker,” NeuroImage, 2010.  
https://doi.org/10.1016/j.neuroimage.2010.01.088

---

# Author

Project Title:
Brain Age Prediction from Structural MRI Using Deep Learning for Early Neurodegenerative Risk Assessment

Developed using Deep Learning and MRI-based Neuroimaging Analysis.
Ritika Mohan
