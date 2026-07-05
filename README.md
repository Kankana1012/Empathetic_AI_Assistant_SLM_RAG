# 🧠 MindCare Elder: Empathetic AI Assistant using SLM + RAG

<p align="center">
  <img src="figures/banner.png" alt="MindCare Elder Banner" width="100%">
</p>
<div align="center">
<table>
<tr>
<td align="center" width="33%">
<img width="50" src="https://img.icons8.com/fluency/96/brain.png"/><br/>
<b>Compassionate AI</b><br/>
<sub>Trained on real mental health data</sub>
</td>
<td align="center" width="33%">
<img width="50" src="https://img.icons8.com/fluency/96/elderly-person.png"/><br/>
<b>Elder-Focused</b><br/>
<sub>Simple, calm, empathetic language</sub>
</td>
<td align="center" width="33%">
<img width="50" src="https://img.icons8.com/fluency/96/artificial-intelligence.png"/><br/>
<b>RAG-Powered</b><br/>
<sub>Context-aware responses via FAISS</sub>
</td>
</tr>
</table>
<br/>

"Context-aware, safe, and compassionate AI for elderly mental health."

</div>

---

## 🌟 Overview

**MindCare Elder** is an AI-powered mental health assistant designed to provide **empathetic, supportive, and context-aware conversations** for elderly users experiencing loneliness, anxiety, fear, stress, or memory-related concerns.

The project combines **Retrieval-Augmented Generation (RAG)** with **parameter-efficient LoRA fine-tuning** on **Mistral-7B-Instruct** to improve response quality while maintaining lightweight inference through **4-bit QLoRA quantization**.

Instead of generating responses solely from model memory, the assistant retrieves relevant supportive context from a FAISS vector database before generating responses, improving factual consistency and contextual relevance.

This project demonstrates an end-to-end Generative AI pipeline including data preprocessing, semantic retrieval, model fine-tuning, response generation, and comprehensive evaluation using multiple NLP metrics.

---
# ✨ Key Highlights

- 🧠 LoRA Fine-tuning of **Mistral-7B-Instruct**
- 🔍 Retrieval-Augmented Generation (RAG)
- ⚡ Efficient 4-bit QLoRA Quantization
- 📚 FAISS Vector Database
- 🤖 LangChain Retrieval Pipeline
- 💬 Context-aware Empathetic Chatbot
- 📊 BLEU, ROUGE & BERTScore Evaluation
- 📈 Model Comparison & Ablation Study
- 🧪 Statistical Significance Testing
- 📉 Latency & Memory Optimization

---
# 🗂️ Repository Navigation

```
Empathetic_AI_Assistant_SLM_RAG/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── mental-care-chatbot-for-elder.ipynb
│
├── data/
│   ├── README.md
│   ├── download_dataset.md
│   └── sample_dataset.csv
│
├── models/
│   └── README.md
│
├── figures/
│   ├── banner.png
│   ├── graphical_abstract.png
│   ├── architecture.png
│   └── workflow.png
│
└── outputs/
    ├── performance_metrics.png
    ├── confusion_matrix.png
    ├── model_comparison.png
    ├── ablation_bleu.png
    ├── latency_comparison.png
    ├── radar_chart.png
    ├── evaluation_results.csv
    ├── classification_report.csv
    └── sample_predictions.csv
```
# 🎯 Project Objectives

The primary objectives of this project are:

- Develop an AI assistant capable of providing empathetic responses for elderly mental health support.
- Improve response quality using Retrieval-Augmented Generation (RAG).
- Fine-tune a Large Language Model efficiently using LoRA and QLoRA.
- Reduce GPU memory consumption while maintaining high performance.
- Evaluate the chatbot using standard NLP evaluation metrics.
- Demonstrate an end-to-end Generative AI application for healthcare support.

---
# 🔬 Methodology

The proposed framework integrates Retrieval-Augmented Generation (RAG) with LoRA fine-tuning to generate context-aware and empathetic responses.

1. **Dataset Preparation** – Collect and preprocess public mental health datasets.
2. **Knowledge Base Construction** – Generate embeddings using **SentenceTransformer** and store them in a **FAISS** vector database.
3. **Model Fine-tuning** – Fine-tune **Mistral-7B-Instruct** using **LoRA (PEFT)** with **4-bit QLoRA** quantization.
4. **RAG Pipeline** – Retrieve relevant context from FAISS and combine it with the user query for prompt generation.
5. **Response Generation** – Produce empathetic, context-aware responses using the fine-tuned model.
6. **Performance Evaluation** – Assess the model using **BLEU**, **ROUGE**, **BERTScore**, **Confusion Matrix**, and **Latency Analysis**.

---

## 🏗️ System Architecture

<p align="center">
  <img src="figures/architecture.png" alt="System Architecture" width="95%">
</p>
The proposed architecture integrates semantic retrieval with a fine-tuned Small Language Model (SLM) to generate context-aware and empathetic responses for elderly mental health support.


---
# 🔄 Project Workflow

<p align="center">
  <img src="figures/workflow.png" alt="Project Workflow" width="95%">
</p>



---

## 🛠️ Tech Stack

| Category | Technologies |
|:---------|:-------------|
| **Programming Language** | Python |
| **Deep Learning Framework** | PyTorch |
| **NLP Framework** | Hugging Face Transformers |
| **Fine-Tuning** | PEFT, LoRA, QLoRA |
| **Vector Database** | FAISS |
| **Embedding Model** | Sentence Transformers (`all-MiniLM-L6-v2`) |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn |
| **Evaluation Metrics** | BLEU, ROUGE, BERTScore |
| **Visualization** | Matplotlib |
| **Development Environment** | Jupyter Notebook, Kaggle |
| **Version Control** | GitHub |


---

# 📊 Experimental Results

The proposed framework was evaluated using standard Natural Language Processing (NLP) metrics to assess response quality, contextual relevance, and overall model performance.

### Model Performance Metrics

| Metric | Score |
|:-------|------:|
| **BLEU** | **36.80** |
| **ROUGE-1** | **0.41** |
| **ROUGE-2** | **0.29** |
| **ROUGE-L** | **0.41** |
| **BERTScore (F1)** | **0.88** |

> **Key Observation:**  
> The integration of **RAG** and **LoRA fine-tuning** significantly improves contextual understanding and response quality while maintaining efficient inference.

### Ablation Study

| Model | BLEU | ROUGE-L | BERTScore | Latency (ms) |
|:-------------|-----:|---------:|-----------:|-------------:|
| Base LLM | 18.4 | 0.21 | 0.71 | 2100 |
| Fine-tuned SLM | 24.7 | 0.29 | 0.78 | 1400 |
| SLM + RAG | 31.5 | 0.36 | 0.83 | 950 |
| **SLM + RAG + LoRA (Proposed)** | **36.8** | **0.41** | **0.88** | **720** |

> **Result:** The proposed framework achieves nearly **2× higher BLEU score** and **66% lower inference latency** compared to the baseline model.

### Model Comparison

| Model | Params (B) | BLEU | Latency (ms) | Memory (GB) |
|---|---|---|---|---|
| GPT-2 | 0.124 | 12.4 | 3200 | 6.5 |
| DistilGPT2 | 0.082 | 15.8 | 2100 | 4.2 |
| DialoGPT | 0.117 | 19.2 | 1800 | 4.8 |
| **Proposed (Fine-tuned SLM)** | 7 | **36.8** | **720** | **1.9** |

---

# 📈 Experimental Visualizations

The following visualizations summarize the performance, efficiency, and comparative evaluation of the proposed framework.

<table align="center">
<tr>
<td align="center" width="50%">

**Performance Metrics**

<img src="outputs/performance_metrics.png" alt="Performance Metrics" width="100%">

</td>

<td align="center" width="50%">

**Model Comparison**

<img src="outputs/model_comparison.png" alt="Model Comparison" width="100%">

</td>
</tr>

<tr>
<td align="center">

**Ablation Study**

<img src="outputs/ablation_bleu.png" alt="Ablation Study" width="100%">

</td>

<td align="center">

**Confusion Matrix**

<img src="outputs/confusion_matrix.png" alt="Confusion Matrix" width="100%">

</td>
</tr>

<tr>
<td align="center">

**Inference Latency Comparison**

<img src="outputs/latency_comparison.png" alt="Latency Comparison" width="100%">

</td>

<td align="center">

**Performance Radar Chart**

<img src="outputs/radar_chart.png" alt="Radar Chart" width="100%">

</td>
</tr>
</table>

> 📌 **Note:** Additional evaluation reports, prediction results, and visualizations are available in the **`outputs/`** directory.

---

# 📂 Dataset

The chatbot is developed using publicly available mental health datasets to support context-aware response generation and model evaluation.

### Dataset Contents

- Mental illness prevalence
- Anxiety-related statistics
- Depression-related information
- Mental health burden indicators
- Emotional support knowledge

> **Note:**  
> The complete datasets are not included in this repository due to licensing and file size limitations.

For dataset details, see:

- 📄 `data/download_dataset.md`
- 📄 `data/README.md`

A small sample dataset is available in:

```text
data/sample_dataset.csv
```

---

# ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/Empathetic_AI_Assistant_SLM_RAG.git

cd Empathetic_AI_Assistant_SLM_RAG
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🚀 Running the Project

### Step 1

Launch Jupyter Notebook.

```bash
jupyter notebook
```

### Step 2

Open

```text
notebooks/mental-care-chatbot-for-elder.ipynb
```

### Step 3

Run all notebook cells sequentially.

### Step 4

Interact with the chatbot through the notebook interface after model loading completes.

> **Recommended Hardware**
>
> - GPU: NVIDIA T4 / P100 or higher
> - RAM: 16 GB+
> - Python 3.10+

---

## 💡 Sample Conversations

| User Says | Bot Responds |
|---|---|
| *"I feel anxious"* | "Take slow deep breaths. You are safe and I am here with you." |
| *"I forgot where I kept things"* | "It is okay to forget sometimes. Relax and check nearby slowly." |
| *"I feel lonely"* | "You are not alone. Talk to your family or someone you trust." |
| *"I am scared"* | "Sit comfortably and breathe slowly. I am right here with you." |

---

## 🔬 Statistical Validation

A two-sample **t-test** confirms the proposed model significantly outperforms the baseline:

```
t-statistic : 18.94
p-value     : < 0.0001  ✅ Statistically significant
```

---

# ⚠️ Limitations

While the proposed framework demonstrates promising performance, it has several limitations:

- Supports only **English-language** interactions.
- Developed and evaluated using **publicly available mental health datasets**.
- Implemented as a **Jupyter Notebook** prototype rather than a production-ready application.
- Responses are intended for **educational and research purposes** and should not replace professional mental health advice.
- Training and fine-tuning require access to GPU resources for optimal performance.

---

# 🚀 Future Work

Several enhancements can further improve the proposed framework:

- 🌍 Multilingual conversational support.
- 🎤 Voice-based interaction for elderly users.
- 🌐 Web application deployment using **Streamlit** or **Gradio**.
- 📱 Mobile application integration.
- 🧠 Long-term conversational memory for personalized interactions.
- 🩺 Integration with domain-specific medical and psychological knowledge bases.
- ☁️ Deployment on cloud platforms for scalable inference.

---

# 📚 References

This project builds upon several open-source frameworks and pre-trained models:

- 🤗 Hugging Face Transformers
- 🔥 PyTorch
- 🔍 FAISS
- 🔗 LangChain
- 🧩 PEFT (Parameter-Efficient Fine-Tuning)
- 📖 Sentence Transformers
- 🧠 Mistral-7B-Instruct

---

# 🙏 Acknowledgements

The development of this project was made possible through the contributions of the open-source AI community.

Special thanks to:

- 🤗 Hugging Face for the Transformers and PEFT libraries.
- 🧠 Mistral AI for the Mistral-7B-Instruct model.
- 🔍 Meta AI for the FAISS similarity search library.
- 🔗 LangChain for enabling Retrieval-Augmented Generation (RAG).
- 📊 The creators of the publicly available mental health datasets.
- 💙 The open-source community for providing valuable tools and resources.

---

# 🤝 Contributing

Contributions are welcome!

If you'd like to improve this project:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Push the branch to your fork.
5. Open a Pull Request.

For major changes, please open an issue first to discuss your proposed improvements.

---

# 📜 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for more details.

---

# 👩‍💻 About the Author

**Kankana Chakraborty**

Final-year **B.Tech in Computer Science & Technology** with a strong interest in:

- 🤖 Artificial Intelligence
- 🧠 Machine Learning
- 💬 Natural Language Processing
- 🔍 Retrieval-Augmented Generation (RAG)
- 🦙 Large Language Models (LLMs)
- ⚡ Small Language Models (SLMs)
- 📊 Deep Learning

This project reflects my interest in developing reliable, efficient, and human-centered AI systems for real-world applications.

---

# 📬 Contact

<p align="center">

<a href="https://github.com/Kankana1012">
<img src="https://img.shields.io/badge/GitHub-Kankana1012-181717?style=for-the-badge&logo=github">
</a>

<a href="https://www.linkedin.com/in/kankana-chakraborty">
<img src="https://img.shields.io/badge/LinkedIn-Kankana%20Chakraborty-0077B5?style=for-the-badge&logo=linkedin">
</a>

<a href="mailto:your-email@example.com">
<img src="https://img.shields.io/badge/Email-Contact%20Me-D14836?style=for-the-badge&logo=gmail&logoColor=white">
</a>

</p>

---

<div align="center">

### ⭐ If you find this project useful, consider giving it a Star!

**Thank you for visiting this repository.**
</div>

<div align="center">
  
### Made with❤️to bring calm and comfort to our elders
  
  **You are not alone. I am here with you.**
</div>
