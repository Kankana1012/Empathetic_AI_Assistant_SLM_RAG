# 🤖 Trained Models

This directory is reserved for storing the trained model checkpoints and LoRA adapter weights used in the **MindCare Elder** project.

## 🧠 Model Information

- **Base Model:** Mistral-7B-Instruct-v0.1
- **Architecture:** Decoder-only Transformer
- **Fine-tuning Method:** PEFT + LoRA with 4-bit QLoRA (NF4)
- **Embedding Model:** SentenceTransformers (`all-MiniLM-L6-v2`)
- **Retrieval Method:** FAISS-based Retrieval-Augmented Generation (RAG)

---

## ❓ Why are the model files not included?

The trained model weights are **not included** in this repository because:

- GitHub imposes file size limitations for repositories.
- Fine-tuned LoRA adapter weights and model checkpoints are too large to host directly.
- This repository is intended to share the implementation, methodology, and experimental results while enabling reproducibility.

---

## 🚀 Reproducing the Model

The complete training, retrieval, and inference pipeline is available in:

```text
notebooks/mental-care-chatbot-for-elder.ipynb
```

Running the notebook will allow you to:

- 📂 Load and preprocess the mental health dataset.
- 🧹 Prepare instruction-response training data.
- 🤖 Fine-tune **Mistral-7B-Instruct** using **LoRA** and **QLoRA**.
- 🔍 Build the **FAISS** vector database for Retrieval-Augmented Generation.
- 💬 Generate context-aware and empathetic responses.
- 📊 Evaluate the model using BLEU, ROUGE, BERTScore, Confusion Matrix, and Latency Analysis.

---

## 🔮 Future Work

Future versions of this repository may include:

- 🤗 LoRA adapter weights
- 📦 Quantized GGUF/GGML models
- 🌐 Hugging Face model repository
- ☁️ Pretrained checkpoints
- 🚀 Streamlit deployment with downloadable models

---

## 📄 Note

This repository is intended for **educational, research, and reproducibility purposes**. Users can reproduce the complete model by following the training pipeline provided in the notebook.
