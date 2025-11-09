# Wafer Map Classification - Project README

## 1. Overview

This project automates **wafer defect pattern recognition** using
machine learning and deep learning models.\
It leverages the **WM811K dataset**, which contains wafer maps annotated
with failure pattern labels.\
The goal is to classify each wafer image into predefined defect
categories such as *Center, Donut, Edge-Loc, Edge-Ring, Random,
Scratch,* and *Near-Full.*

------------------------------------------------------------------------

## 2. Dataset

The **WM811K dataset** includes over **800,000 wafer maps** from real
semiconductor manufacturing data.\
Each map represents bin-level pass/fail data, reshaped into 2D wafer
images.\
The dataset provides 9 labels, including normal wafers and 8 distinct
defect types.

------------------------------------------------------------------------

## 3. Methodology / Pipeline

1.  **Data Preprocessing** -- Convert raw bin data into grayscale wafer
    images and normalize pixel values.\
    Handle class imbalance via SMOTE or data augmentation.\
2.  **Model Architecture** -- Use a pre-trained CNN (e.g., ResNet50) for
    feature extraction, followed by a classifier layer.\
    Alternatively, extract embeddings and train a traditional ML model
    (e.g., SVM).\
3.  **Evaluation** -- Metrics: accuracy, precision, recall, F1-score,
    and confusion matrix.\
    Visualize model attention using **Grad-CAM** for interpretability.

------------------------------------------------------------------------

## 4. Results Summary

The **ResNet50 + SVM hybrid model** achieved strong accuracy across
major defect classes while reducing overfitting.\
- CNN captured spatial defect textures effectively.\
- SVM provided robust class separation in high-dimensional space.\
- Grad-CAM highlighted relevant wafer defect regions, enhancing
explainability.

------------------------------------------------------------------------

## 5. Future Work

-   Integrate **attention mechanisms** and **self-supervised
    pretraining**.\
-   Use temporal process data for early fault detection.\
-   Build a **manufacturing dashboard** for real-time yield monitoring
    and RCA visualization.

------------------------------------------------------------------------

## 6. References

1.  WM811K Dataset: [Kaggle - WM811K Wafer
    Map](https://www.kaggle.com/datasets/qingyi/wm811k-wafer-map)\
2.  Liu et al., *"WM811K: A Public Wafer Map Dataset for Defect Pattern
    Recognition"*, IEEE DataPort, 2018.\
3.  He et al., *"Deep Residual Learning for Image Recognition"*, CVPR,
    2016.
