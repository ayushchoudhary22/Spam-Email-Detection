# 📧 Spam Email Detection using Hybrid ML and CNN-based DL Models

This repository implements a powerful email spam detection system using both traditional **Machine Learning** and **Deep Learning (CNN)** models. The goal is to accurately classify email messages as **Spam** or **Ham (Not Spam)**.

---

## 📑 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Models Used](#models-used)
- [Results](#results)
- [How to Run](#how-to-run)
- [Folder Structure](#folder-structure)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## 📌 Overview

Spam emails are not just annoying—they're often dangerous. From phishing scams to malicious links, spam emails cost billions each year in damages and lost time. In this project:

- We apply **two models**:
  - A **Hybrid ML model** using Naive Bayes, SVM, and Random Forest
  - A **CNN-based Deep Learning model**
- We compare performance and discuss results
- Built for accuracy, speed, and real-world readiness

---

## 📊 Dataset

- Source: [UCI SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- ~5,500 SMS text messages
- Labels: `ham` (0), `spam` (1)

---

## 🧠 Models Used

### 🔹 Hybrid Machine Learning Model
- Feature extraction: **TF-IDF with bigrams**
- Classifiers:  
  - Naive Bayes (`alpha=0.1`)  
  - Linear SVM (`C=10`)  
  - Random Forest (`n_estimators=200`)
- Combined using `VotingClassifier`

### 🔹 CNN Deep Learning Model
- Preprocessing: **Tokenization + Padding**
- Layers:
  - Embedding → Conv1D → GlobalMaxPooling → Dense + Dropout → Sigmoid
- Training:
  - 30 epochs, batch size 64
  - Binary crossentropy, class weights

---

## 📈 Results

| Metric        | Hybrid ML | CNN DL |
|---------------|-----------|--------|
| Accuracy      | 97.66%    | 98.83% |
| Spam Recall   | 0.83      | High   |
| Spam Precision| 1.00      | High   |

- ✅ CNN performed slightly better in recall and generalization  
- ✅ Hybrid model was faster and simpler to train

---

## 🚀 How to Run

### Clone the repository
```bash
git clone https://github.com/ayushchoudhary22/Spam-Email-Detection.git
cd Spam-Email-Detection
