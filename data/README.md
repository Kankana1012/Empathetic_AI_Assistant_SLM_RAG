# 📂 Dataset Information

This directory contains documentation and a sample dataset used in the **MindCare Elder** project.

The chatbot is developed using publicly available mental health datasets to support Retrieval-Augmented Generation (RAG), model fine-tuning, and performance evaluation.

---

## 📊 Dataset Overview

The project utilizes mental health datasets containing information related to:

- Mental illness prevalence
- Anxiety disorders
- Depressive disorders
- Mental health burden indicators
- Emotional well-being statistics

These datasets are used to:

- Prepare instruction-response training data
- Build the FAISS knowledge base
- Support context-aware response generation
- Evaluate the proposed framework

---

## 📁 Directory Contents

```text
data/
├── README.md
├── download_dataset.md
└── sample_dataset.csv
```

| File | Description |
|------|-------------|
| **README.md** | Dataset documentation |
| **download_dataset.md** | Instructions for obtaining the original datasets |
| **sample_dataset.csv** | A small sample dataset for demonstration purposes |

---

## 📄 Sample Dataset

The included **sample_dataset.csv** provides a small subset of the original data structure to help users understand the dataset format without distributing the complete datasets.

---

## ⚠️ Why are the original datasets not included?

The complete datasets are not included in this repository because:

- They originate from publicly available third-party sources.
- Redistribution may be subject to licensing or usage restrictions.
- Some datasets exceed GitHub's recommended file size limits.

Instead, this repository provides download instructions and a sample dataset for reproducibility.

---

## 🚀 Getting Started

1. Read **download_dataset.md**.
2. Download the original datasets from the referenced sources.
3. Place the datasets in the appropriate directory.
4. Run the notebook to preprocess the data and train the model.

---

## 📌 Note

This project is intended for **educational, research, and reproducibility purposes**. Please comply with the licensing terms of the original dataset providers when downloading or using the datasets.
