# IMDB Sentiment Analysis using 1D CNN

---

## Overview

This project implements a 1D Convolutional Neural Network (CNN) to perform binary sentiment classification on the IMDB movie reviews dataset. The goal is to classify reviews as either positive or negative.

The model was trained using text preprocessing techniques, sequence tokenization, and padding. Regularization and optimization strategies such as dropout, early stopping, and learning rate scheduling were applied to improve generalization and prevent overfitting.

---

## 1. 1D Convolutional Neural Network (CNN)

**Architecture:**  
- Embedding Layer (vocabulary size: 10,000, embedding dimension: 128)  
- Conv1D Layer (filters: 64, kernel size: 5, ReLU activation)  
- Conv1D Layer (filters: 64, kernel size: 5, ReLU activation)  
- Global Max Pooling Layer  
- Dense Layer (ReLU activation)  
- Dropout (0.5)  
- Output Layer (Sigmoid activation)  

---

## Techniques Applied

- Text cleaning (lowercasing, removing HTML tags and special characters)  
- Tokenization with OOV handling  
- Sequence padding (max length: 300)  
- Train / validation / test split with stratification  
- Dropout for regularization  
- EarlyStopping to prevent overfitting  
- ReduceLROnPlateau for adaptive learning rate  

---

## Training Configuration

- Optimizer: Adam (learning rate: 0.0005)  
- Loss Function: Binary Crossentropy  
- Batch Size: 64  
- Epochs: up to 10 (with early stopping)  

---

## Performance

- Training Accuracy: ~0.94–0.96  
- Validation Accuracy: ~0.88–0.89  
- Best Epoch: 2  
- Test Accuracy: ~0.88  

---

## Files

- `cnn_model.ipynb` → Full implementation  
- `results/loss_curve.png` → Training vs validation loss  
- `results/accuracy_curve.png` → Training vs validation accuracy  
- `results/confusion_matrix.png` → Confusion matrix

---

## Curves

![Loss Curve](results/loss_curve.png)  
![Accuracy Curve](results/accuracy_curve.png)  

---

## Summary

The 1D CNN model demonstrated strong performance for sentiment classification, achieving high accuracy with efficient training time. Proper regularization techniques ensured good generalization while preventing excessive overfitting. I tried to improve the results but couldn't do better than this one.
