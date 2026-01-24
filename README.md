# EnBa
# English to Bangla Machine Translation  
### A Comparative Study of Seq2Seq, Transformers, and LLMs

📌 **Author:** Suraiya Mahmuda  
📅 **Date:** January 2026  

---

## 📖 Project Overview

This project implements an **English-to-Bangla Machine Translation system** using three different approaches:

1. **Seq2Seq LSTM (Encoder–Decoder)**
2. **Transformer-based Model (NLLB-200)**
3. **Large Language Model (Qwen2.5-3B-Instruct)**

The goal is to **compare translation quality and performance** across traditional NMT, modern Transformers, and Large Language Models using **BLEU score evaluation**.

---

## 🎯 Objectives

- Implement a **custom Seq2Seq LSTM** model for English–Bangla translation  
- Use a **pre-trained Transformer (NLLB-200)** for high-quality translation  
- Evaluate a **Large Language Model (LLM)** in a zero-shot translation setting  
- Compare all models using **BLEU scores**  
- Provide an **offline-capable translation framework**

---

## 🧠 Models Used

### 1️⃣ Seq2Seq LSTM
- Encoder–Decoder architecture  
- Word embeddings + LSTM layers  
- Suitable for simple and short sentences  

### 2️⃣ Transformer (NLLB-200)
- Model: `facebook/nllb-200-1.3B`
- Beam search decoding (num_beams = 10)
- Forced BOS token for Bangla (`ben_Beng`)
- High accuracy, fully offline

### 3️⃣ LLM (Qwen2.5-3B-Instruct)
- Zero-shot translation via prompting
- Float16 precision
- Greedy decoding (`do_sample=False`)
- Produces the most fluent translations

---

## 📊 Dataset

- **Type:** Parallel English–Bangla dataset  
- **Format:** CSV  
- **Columns:**
  - `en_text` – English sentence  
  - `bn_text` – Bangla sentence  

Data cleaning includes:
- Removing empty or very short sentences  
- Normalizing whitespace  
- Tokenization and padding (for LSTM)

---

## 🛠️ Tools & Technologies

| Category | Tools |
|--------|------|
| Programming | Python |
| Deep Learning | TensorFlow / Keras, PyTorch |
| NLP Libraries | Hugging Face Transformers, NLTK |
| Evaluation | sacreBLEU |
| Environment | Kaggle Notebook (NVIDIA Tesla T4 GPU) |

---

## 🏗️ System Architecture

![System Architecture](images/architecture.png)


