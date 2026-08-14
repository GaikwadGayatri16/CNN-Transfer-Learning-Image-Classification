# CNN Transfer Learning Image Classification

## Research Paper Based Image Classification Project

This project implements an image classification pipeline for distinguishing
between **AI-generated (FAKE)** and **REAL** images using Convolutional Neural
Networks.

The implementation is based on the research paper:

> **A Comparative Study of MobileNetV2 and ResNet50 for Multi-Class
> AI-Generated and Real Image Classification**

The original research paper compares MobileNetV2 and ResNet50 for AI-generated
and real image classification. This project implements an **adapted version of
the research problem** using a binary REAL/FAKE classification dataset and
compares a custom CNN with MobileNetV2 before and after fine-tuning.

---

## 1. Project Objective

The main objectives of this project are:

- To implement a CNN image classification model from scratch.
- To implement transfer learning using a pretrained MobileNetV2 model.
- To fine-tune the pretrained MobileNetV2 model for the target dataset.
- To evaluate the models using multiple classification metrics.
- To compare the performance of the models on the same test dataset.
- To perform error analysis using incorrect predictions.
- To compare the implementation with the selected research paper.

---

## 2. Problem Statement

AI-generated images have become increasingly realistic and can be difficult
to distinguish from real images using visual inspection alone.

The objective of this project is to develop deep learning models capable of
classifying images into two categories:

- **REAL** — authentic/real images
- **FAKE** — AI-generated images

The project investigates both a custom CNN and a pretrained MobileNetV2 model
to determine their effectiveness for this binary image classification task.

---

## 3. Research Paper

### Selected Paper

**Title:**  
*A Comparative Study of MobileNetV2 and ResNet50 for Multi-Class AI-Generated
and Real Image Classification*

**Journal:**  
Sinkron: Jurnal dan Penelitian Teknik Informatika

**Volume:** 10, Issue 1, January 2026

**DOI:**  
https://doi.org/10.33395/sinkron.v10i1.15682

### Research Paper Summary

The research paper investigates AI-generated and real image classification
using two CNN architectures:

- MobileNetV2
- ResNet50

The paper uses a dataset of **23,941 images**, organized into REAL and FAKE
classes along with five visual subclasses:

- Human
- Animal
- View
- Art
- Vehicle

The research methodology includes preprocessing, data augmentation,
5-fold cross-validation, transfer learning, fine-tuning, and evaluation using
accuracy, precision, recall, F1-score, and confusion matrices.

The paper reported that MobileNetV2 achieved its best accuracy of approximately
**89% at 10 epochs**, while ResNet50 achieved its best accuracy of
approximately **93% at 30 epochs**.

---

## 4. Adaptation of the Research Paper

This project does not reproduce every experiment from the original paper.

Instead, it implements an **adapted version of the research problem** suitable
for the practical assignment.

### Original Research Paper

- MobileNetV2
- ResNet50
- 23,941 images
- REAL/FAKE with five visual subclasses
- Data augmentation
- 5-fold cross-validation
- Fine-tuning
- Multiple evaluation metrics

### This Implementation

- Custom CNN trained from scratch
- MobileNetV2 transfer learning
- Fine-tuned MobileNetV2
- CIFAKE dataset
- Binary REAL/FAKE classification
- Standard train/validation/test workflow
- Accuracy, precision, recall and F1-score
- Confusion matrices
- Training/validation curves
- Error analysis
- Final model comparison

This adaptation allows the core research idea to be implemented while
maintaining a practical and reproducible workflow.

---

## 5. Dataset

### Dataset Used

**CIFAKE — Real and AI-Generated Images**

The dataset contains two classes:

- REAL
- FAKE

### Dataset Size

| Dataset | Number of Images |
|---|---:|
| Training | 100,000 |
| Testing | 20,000 |
| Total | 120,000 |

The training dataset is balanced between the REAL and FAKE classes.

### Classification Type

This implementation performs:

**Binary Image Classification**

```text
REAL
FAKE
