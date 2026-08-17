# CNN Transfer Learning Image Classification

## Overview

This project implements binary image classification to distinguish between
**REAL** and **AI-generated (FAKE)** images.

The implementation is based on the research paper:

> **A Comparative Study of MobileNetV2 and ResNet50 for Multi-Class
> AI-Generated and Real Image Classification**

The project compares three CNN architectures:

- Custom CNN trained from scratch
- MobileNetV2 using transfer learning and fine-tuning
- ResNet50 using transfer learning and fine-tuning

## Dataset

**CIFAKE – Real and AI-Generated Images**

- Training images: 100,000
- Test images: 20,000
- Classes: REAL, FAKE

The dataset is balanced between the two classes.

## Models

### Custom CNN

A Convolutional Neural Network was designed and trained from scratch for
REAL/FAKE classification.

### MobileNetV2

A pretrained MobileNetV2 model was used through transfer learning. Its upper
layers were then fine-tuned using a smaller learning rate.

### ResNet50

A pretrained ResNet50 model was used through transfer learning. Its upper
layers were also fine-tuned using a smaller learning rate.

## Results

### Final Model Comparison

| Model | Test Accuracy |
|---|---:|
| Custom CNN | **95.62%** |
| Fine-Tuned MobileNetV2 | **94.80%** |
| Fine-Tuned ResNet50 | **89.81%** |

The custom CNN achieved the highest test accuracy of **95.62%**.

### Effect of Fine-Tuning

| Model | Before Fine-Tuning | After Fine-Tuning | Improvement |
|---|---:|---:|---:|
| MobileNetV2 | 88.84% | 94.80% | +5.96 pp |
| ResNet50 | 76.64% | 89.81% | +13.17 pp |

Fine-tuning significantly improved both pretrained models.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Training/Validation Curves
- Error Analysis

For the fine-tuned MobileNetV2, the model correctly classified:

- **18,960 / 20,000 test images**
- **Error rate: 5.20%**

## Research Paper Comparison

The selected research paper compares **MobileNetV2 and ResNet50** for
AI-generated and real image classification using a more extensive
experimental setup.

The paper uses techniques such as:

- Transfer learning
- Fine-tuning
- Data augmentation
- 5-fold cross-validation
- Multiple evaluation metrics

This project implements an **adapted version of the research problem** using
the CIFAKE binary REAL/FAKE dataset.

Unlike the paper, this implementation also includes a **custom CNN baseline**
and focuses on binary REAL/FAKE classification.

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab
- GitHub

## Repository Structure

```text
CNN-Transfer-Learning-Image-Classification/
├── README.md
└── Gayatri_Gaikwad_CNN_TransferLearning_Assignment.ipynb
