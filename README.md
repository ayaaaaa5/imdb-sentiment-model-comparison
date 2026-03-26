# 📊 IMDB Sentiment Analysis — Deep Learning Models Comparison

## Overview
This project focuses is an enhancement of the previous assignment by using three deep learning architectures:

- **1D Convolutional Neural Network (1D-CNN)**
- **Long Short-Term Memory (LSTM)**
- **Gated Recurrent Unit (GRU)**

The objective is to compare performance, efficiency, and generalization across these models.

---

## Data Preprocessing
All models use the same preprocessing pipeline:

- Text cleaning (lowercasing, removing HTML tags & special characters)
- Tokenization with **OOV handling**
- Sequence padding (max length: **300**)
- **train / validation / test split**

---

## Models:

### 1D-CNN Model:
**Architecture**
- Embedding (128-dim)
- Conv1D (64 filters, kernel size = 5) ×2
- Global Max Pooling
- Dense (ReLU)
- Dropout (0.5)
- Output Layer (Sigmoid)

**Strengths**
- Fast training
- Captures local textual patterns (n-grams)
- Strong generalization

---

### LSTM Model
**Architecture**
- Embedding (128-dim)
- LSTM (64 units, dropout = 0.3, recurrent dropout = 0.3)
- Dense (ReLU)
- Dropout (0.6)
- Output Layer (Sigmoid)

**Strengths**
- Captures long-term dependencies in sequences

**Limitations**
- Slow training
- Slight overfitting after a few epochs

---

### GRU Model
**Architecture**
- Embedding (128-dim)
- GRU (64 units, dropout = 0.3, recurrent dropout = 0.3)
- Dense (ReLU)
- Dropout (0.6)
- Output Layer (Sigmoid)

**Strengths**
- Simpler and faster than LSTM
- Comparable performance with fewer parameters

---

## Training Settings:

| Parameter        | Value                  |
|----------------|------------------------|
| Optimizer       | Adam                  |
| Learning Rate   | 0.0005                |
| Loss Function   | Binary Crossentropy   |
| Batch Size      | 64                    |
| Epochs          | 5–10 (EarlyStopping)  |
---

## Performance Comparison

| Model | Train Accuracy | Validation Accuracy | Test Accuracy | Notes |
|------|---------------|--------------------|--------------|------|
| **CNN** | ~0.94–0.96 | ~0.88–0.89 | **0.88** | Best overall performance |
| **LSTM** | ~0.94–0.96 | ~0.87–0.88 | 0.86 | Slight overfitting |
| **GRU** | ~0.68–0.90 | ~0.86–0.88 | 0.86 | Efficient |

---

## Comments:

I noticed that all your models started to overfit relatively early in the training process, although the exact timing varied between models. This consistent pattern of early overfitting was the primary justification for employing early stopping.

---

## 🧾 Conclusion

- **CNN is the best-performing model** for this task.
- **LSTM and GRU are useful for sequence modeling** but do not outperform CNN here.
- **GRU is preferred over LSTM** when efficiency is important.
