# IMDB Sentiment Analysis — GRU Model

---

## Overview

This part of the project implements a GRU neural network for binary sentiment classification on the IMDB movie reviews dataset

---

## Model Architecture

- Embedding Layer (vocabulary size: 10,000, embedding dimension: 128)
- GRU Layer (64 units, dropout: 0.3, recurrent dropout: 0.3)
- Dense Layer (ReLU activation)
- Dropout (0.6)
- Output Layer (Sigmoid activation)

---

## Techniques Applied

- Text cleaning and preprocessing
- Tokenization with out-of-vocabulary handling
- Sequence padding
- Stratified train/validation/test split
- Dropout and recurrent dropout for regularization
- Early stopping to prevent overfitting
- Learning rate reduction on plateau

---

## Training Configuration

- Optimizer: Adam
- Learning Rate: 0.0005
- Loss Function: Binary Cross-Entropy
- Batch Size: 64
- Epochs: up to 5 with early stopping

---

## Performance

- Training Accuracy: 0.68–0.90
- Test Accuracy: 0.86

---

## Files

Attached under the GRU folder

---

## Conclusion

The GRU model provides an efficient recurrent alternative to LSTM for sentiment classification. It is generally faster and simpler while still achieving strong performance, making it a useful model for comparison against CNN and LSTM approaches.
