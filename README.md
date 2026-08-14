# CNN Transfer Learning Image Classification

## Overview

This project implements binary image classification to distinguish between
**REAL** and **AI-generated (FAKE)** images.

The implementation is based on the research paper:

> **A Comparative Study of MobileNetV2 and ResNet50 for Multi-Class
> AI-Generated and Real Image Classification**

The project uses a custom CNN, MobileNetV2 transfer learning, and
MobileNetV2 fine-tuning.

## Dataset

**CIFAKE – Real and AI-Generated Images**

- Training images: 100,000
- Test images: 20,000
- Classes: REAL, FAKE

## Models

### Custom CNN

A CNN was designed and trained from scratch for REAL/FAKE classification.

### MobileNetV2

A pretrained MobileNetV2 model was used through transfer learning.

### Fine-Tuned MobileNetV2

The upper layers of MobileNetV2 were fine-tuned to adapt the model to the
target dataset.

## Results

| Model | Test Accuracy |
|---|---:|
| Custom CNN | **95.62%** |
| MobileNetV2 | 88.84% |
| Fine-Tuned MobileNetV2 | **94.80%** |

Fine-tuning improved MobileNetV2 from **88.84% to 94.80%**.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Training/Validation Curves
- Error Analysis

The final fine-tuned MobileNetV2 achieved:

- Correct predictions: **18,960 / 20,000**
- Error rate: **5.20%**

## Research Paper

The original paper compares **MobileNetV2 and ResNet50** using a larger
multi-class dataset and additional techniques such as data augmentation and
5-fold cross-validation.

This project implements an **adapted version of the research problem** using
the CIFAKE binary REAL/FAKE dataset.

## Technologies

Python, TensorFlow, Keras, NumPy, Pandas, Matplotlib, Scikit-learn,
Google Colab

## Repository

```text
CNN-Transfer-Learning-Image-Classification/
├── README.md
└── Gayatri_Gaikwad_CNN_TransferLearning_Assignment.ipynb
