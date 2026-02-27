# Steel Plates Faults Classification Project

## Overview

This project focuses on classifying defects in steel plates using machine learning and deep learning techniques. It compares the performance of:

- K-Nearest Neighbors (K-NN)
- Support Vector Machines (SVM)
- Multi-Layer Perceptron (Deep Learning)

The goal is to determine the most effective method for industrial quality control.

---

## Dataset Characteristics

The project utilizes the **"Steel Faults"** dataset, which includes specialized features for industrial classification:

- **Features:** 27 distinct variables representing geometric and luminosity properties of the steel surface.
- **Target Classes:** 7 types of faults:
  - Pastry
  - Z_Scratch
  - K_Scratch
  - Stains
  - Dirtiness
  - Bumps
  - Other Faults

---

## Algorithms & Implementation

### 1. K-Nearest Neighbors (K-NN)

- **Scaling:** Standardized using `StandardScaler` to ensure mean = 0 and standard deviation = 1 (distance metrics are sensitive to feature scales).
- **Distance Metric:** Euclidean distance.
- **Hyperparameter Tuning:** Tested K values from 1 to 20.
  - Optimal value: **K = 1**
- **Accuracy:** ~72.42%

---

### 2. Support Vector Machine (SVM)

- **Kernel:** RBF (Radial Basis Function) kernel to handle non-linear data.
- **Margin:** Soft Margin implemented to allow some misclassifications in noisy real-world data.
- **Validation:** 10-fold cross-validation to ensure generalization.
- **Accuracy:** 76%

---

### 3. Deep Learning (Multi-Layer Perceptron)

- **Architecture:** Feed-forward neural network with:
  - Hidden Layer 1: 64 neurons
  - Hidden Layer 2: 32 neurons
- **Activation Functions:**
  - ReLU for hidden layers
  - Softmax for final output layer (7-class classification)
- **Regularization:** 20% Dropout layers to reduce overfitting
