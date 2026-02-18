# 🏭 Industrial Anomaly Detection on MILAN Eraser Dataset

## 📌 Overview

Industrial anomaly detection plays a crucial role in automated quality control for manufactured products.  
This project focuses on automating the inspection process of erasers produced by MILAN Stationery Company.

Each product package contains 15 erasers, and images are captured using a fixed-angle camera system.  
The system provides six-channel image data:

- AM  
- GRAY  
- G  
- R  
- W  
- NORMAL  

The objective is to determine whether the printed logo on each eraser is clear and defect-free.  
This is formulated as a **binary classification problem**.

---

## 🎯 Problem Statement

Given a multi-channel image of an eraser, classify it as:

- **Normal (No Defect)**
- **Defective Logo**

The dataset contains **1,381 multi-channel images**, with noticeable class imbalance.

---

## 🧠 Methodology

We trained and evaluated multiple pretrained CNN architectures:

- ResNet-18  
- ResNet-34  
- ResNet-50  
- ResNet-101  
- ResNet-152  

All models were fine-tuned on the MILAN eraser dataset using transfer learning.

---

## 🔬 Best Performing Model

The fine-tuned **ResNet-50** achieved the best overall performance:

- **AUC-PR:** 0.7236  
- **F1-score:** 0.6376  

It outperformed other ResNet backbone variants.

---

## 🚀 Key Contributions

### 1️⃣ Dataset Label Correction
- Identified inconsistencies in binary annotations.
- Manually inspected and corrected incorrect labels.
- Reduced noise and improved training quality.
- Helped mitigate class imbalance.

### 2️⃣ Transfer Learning with ResNet-50
- Fine-tuned pretrained ResNet-50 on corrected dataset.
- Leveraged transfer learning for better feature extraction.
- Achieved superior performance compared to deeper and shallower variants.

### 3️⃣ Handling Class Imbalance
To address dataset imbalance, we combined:

- Class-weighted loss
- Weighted random sampling

This strategy reduced bias toward the majority class and improved minority defect detection.

---

## 📊 Evaluation Metrics

Since the dataset is imbalanced, we used:

- Area Under Precision-Recall Curve (AUC-PR)
- F1-score
- Precision
- Recall

---

## 📁 Dataset Details

- Total samples: 1,381  
- Multi-channel images (6 channels)  
- Binary labels: Normal vs Defective  

---

## 🛠️ Tech Stack

- Python  
- PyTorch  
- Pretrained ResNet architectures  
- Transfer Learning  
- Weighted Loss Functions  
- Weighted Random Sampling  

---
