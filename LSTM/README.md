# IMDB Sentiment Analysis — LSTM Model

---

## Overview

In this part of the project, we implemented an LSTM neural network for binary sentiment classification on the same dataset. The objective is to classify reviews as positive or negative.

---

## Model Architecture

- Embedding Layer (vocabulary size: 10,000, embedding dimension: 128)
- LSTM Layer (64 units, dropout: 0.3, recurrent dropout: 0.3)
- Dense Layer (ReLU activation)
- Dropout (0.6)
- Output Layer (Sigmoid activation)

---

## Techniques Applied

- Text preprocessing (cleaning HTML tags, punctuation, lowercasing)
- Tokenization and sequence padding
- Train/validation/test split with stratification
- Dropout for regularization
- Recurrent dropout in LSTM to reduce overfitting

---

## Training Configuration

- Optimizer: Adam
- Loss: Binary Crossentropy
- Batch Size: 64
- Epochs: 5

---

## Performance

- Training Accuracy: ~0.94–0.96
- Validation Accuracy: ~0.87–0.88
- Best Epoch: 3
- Test Accuracy: ~0.86

---

## Remarks

The model exhibits good learning behavior, with validation loss decreasing until epoch 3, after which it increases, indicating the onset of overfitting. Regularization techniques such as dropout and recurrent dropout helped improve generalization.

---

## Files

Attached under the LSTM folder

---
