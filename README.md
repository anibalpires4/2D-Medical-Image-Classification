# 2D Medical Image Classification

This repository contains an analysis and implementation of machine learning models to classify 2D medical images into six distinct classes from dermoscopy and blood cell microscopy datasets. The project primarily focuses on developing and evaluating Convolutional Neural Networks (CNNs) but also explores alternative methods such as k-NN, SVM, and Random Forests.

---

## Overview
The classification task involves images with the following six classes:
1. **Nevu (0)**
2. **Melanoma (1)**
3. **Vascular Lesions (2)**
4. **Granulocytes (3)**
5. **Basophils (4)**
6. **Lymphocytes (5)**

The dataset is imbalanced, and data augmentation techniques (e.g., flips, rotations, transpositions, contrast adjustments) were used to balance the class distribution. Models were evaluated using metrics like balanced accuracy and F1-score.

### Methods
1. **Convolutional Neural Networks (CNNs)**:
   - Custom architecture with two convolutional layers, batch normalization, max-pooling, dropout, and dense layers.
   - Achieved a **balanced accuracy of 86%** on the validation set.
2. **k-Nearest Neighbors (k-NN)**:
   - Used Euclidean distance with data augmentation.
3. **Support Vector Machines (SVM)**:
   - Applied RBF kernel with augmented data.
4. **Random Forests**:
   - Trained with 100 estimators on augmented data.

---

## Results

### CNN Architecture
| **Layer**         | **Output Shape**  |
|--------------------|-------------------|
| Conv2D            | (28 × 28 × 32)    |
| Batch Norm.       | (28 × 28 × 32)    |
| MaxPooling        | (14 × 14 × 32)    |
| Conv2D            | (14 × 14 × 64)    |
| Batch Norm.       | (14 × 14 × 64)    |
| MaxPooling        | (7 × 7 × 64)      |
| Flatten           | (7 × 7 × 64)      |
| Dense (128)       | (128)             |
| Dropout (0.5)     | (128)             |
| Dense (6)         | (6)               |

- Total Parameters: **422,150**
- Metrics:
  - **Precision**: Achieved high precision across all classes, with particularly strong results for Nevu (0), Granulocytes (3), and Basophils (4).
  - **Balanced Accuracy**: 86%
  - **F1-Score**: Demonstrated strong performance, with the highest F1-scores for Granulocytes (95%) and Nevu (91%).

---

## Technologies
- **Programming Language**: Python
- **Frameworks and Libraries**:
  - TensorFlow/Keras (CNN Implementation)
  - Scikit-learn (k-NN, SVM, Random Forests)
  - Matplotlib, Seaborn (Data Visualization)
- **Tools**: Jupyter Notebook

---

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/anibalpires4/2D-Medical-Image-Classification.git

