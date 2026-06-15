# 💳 Bank Transaction NLP Categorizer

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.2+-ee4c2c.svg)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/Hugging%20Face-Transformers-orange.svg)](https://huggingface.co/transformers/)
[![Streamlit](https://img.shields.io/badge/Streamlit-App-ff4b4b.svg)](https://streamlit.io/)

---

## 🌍 English Version

An automated Personal Finance Management (PFM) system designed to categorize "dirty" bank transaction strings using Deep Learning.

### 🛠️ Tech Stack
* **Deep Learning:** PyTorch, Hugging Face `transformers`, `datasets`
* **Model:** `distilbert-base-multilingual-cased` (Fine-Tuned)
* **Frontend UI:** Streamlit
* **Data:** Synthetic dataset of raw bank receipts generated with realistic terminal noise.

### ⚙️ Key Features
* **Transformer Fine-Tuning:** A baseline multilingual DistilBERT model was fine-tuned for Sequence Classification to accurately recognize key spending categories.
* **Robustness to Noise:** The model effectively handles typos, mixed scripts (Cyrillic/Latin), abbreviations, and random terminal metadata (IDs, locations), extracting the true semantic context.
* **Inference UI:** A clean, user-friendly Streamlit web interface that showcases model predictions, top-5 probability distribution, and certainty flags (Confidence Score).

### 🗂️ Repository Structure
```text
├── .gitignore               # Excludes models, data, and cache files
├── README.md                # Project documentation
├── app.py                   # Main Streamlit UI application code
├── requirements.txt         # Project package dependencies
└── src/                     # Core source code directory
    ├── __init__.py          # Makes src a Python package
    └── train_nlp.py         # Pipeline for synthetic data generation & model training
