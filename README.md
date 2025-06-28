# 🧬 Protein Sequence Classification: RNN vs LSTM vs Transformer

This repository contains the complete code and trained models for the thesis:  
**“A Comparative Study on Deep Learning Methods for Protein Sequence Classification.”**

This project benchmarks **Recurrent Neural Networks (RNN)**, **Long Short-Term Memory networks (LSTM)**, and **Transformer** architectures on classifying protein sequences using amino acid embeddings from the [UniProt](https://www.uniprot.org/) database.

---

## 📌 Overview

Protein sequences are vital in bioinformatics but require automated, accurate classification to understand function and taxonomy.  
This project compares how well different deep learning methods can classify protein sequences based solely on **sequence embeddings**.

---

## 📚 Dataset

- **Source:** UniProt Protein Embeddings
- **Species Used:**  
  - *Caenorhabditis elegans*
  - *Homo sapiens*
  - *Mus musculus*
- **Features:**  
  - 1024-dimensional embedding vectors
  - 5,000 samples per species
  - Split: 60% Train / 20% Validation / 20% Test

---

## ⚗️ Experimental Setup

- Models implemented and trained in Python (**Tensorflow**) using Google Colab with GPU acceleration.
- Identical hyperparameters used across RNN, LSTM, and Transformer for fair comparison.
- Early stopping applied based on validation loss.

---

## 📊 Key Results

| Model       | Test Loss | Test Accuracy |
|-------------|-----------|----------------|
| RNN         | 0.5653    | 68.9%          |
| LSTM        | 0.5513    | 68.7%          |
| Transformer | 0.5953    | 64.2%          |

**Findings:**  
- Sequential models (RNN, LSTM) showed better performance and stability than the Transformer for this specific dataset.
- Attention-based Transformers may require larger or differently structured biological data to outperform recurrent models on sequence classification.

---

## 💡 Contribution & Future Work

- Confirms the effectiveness of simple recurrent architectures for **order-sensitive biological sequence tasks**.
- Suggests possible extensions:
  - Scaling experiments to larger protein databases
  - Hybrid models combining RNNs with Attention mechanisms for improved long-range dependencies
