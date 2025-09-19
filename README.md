# Medical Image Classification – PathMNIST

This repository contains a **comparative study of machine learning and deep learning algorithms** applied to the [PathMNIST dataset](https://www.nature.com/articles/s41597-022-01721-8), a benchmark dataset of histopathology tissue images.  
The study was conducted as part of my **Master’s in Data Science coursework**, with the goal of evaluating traditional vs. modern approaches for **multi-class image classification**.

---

## 🎯 Project Aim
The objective is to:
- Build and evaluate **Random Forest, Multi-Layer Perceptron (MLP), and Convolutional Neural Networks (CNN)** on tissue image data.
- Investigate challenges such as **class imbalance, inter-class similarity, noise, and low resolution (28×28 RGB images)**.
- Compare models across **accuracy, runtime, robustness, and complexity**.
- Provide insights into trade-offs between traditional ML and deep learning in medical imaging.

---

## 🧠 Key Findings
- **CNN achieved the highest accuracy (77.04%)** with reasonable runtime, proving most effective for image classification.
- **Random Forest** performed surprisingly well (65.5%) on flattened image data, though computationally expensive.
- **MLP** struggled due to lack of spatial awareness, achieving only ~34% accuracy.
- CNN provided the best trade-off between **accuracy, efficiency, and generalization**.

---

## 📊 Dataset
- Subset of the **PathMNIST – TissueNets** dataset.  
- **28×28 RGB images** representing 9 tissue classes.  
- **32,000 training** and **8,000 testing** images.  
- Challenges: **imbalanced classes, inter-class similarity, blurred/noisy images**.

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Normalization (pixel scaling to [0,1])
   - Flattening for RF and MLP (1D vector of 2352 features)
   - One-hot encoding for neural networks
2. **Models Implemented**
   - Random Forest (with hyperparameter tuning)
   - Multi-Layer Perceptron (fully connected ANN)
   - Convolutional Neural Network (2 Conv2D + MaxPooling + Dense layers with Dropout)
3. **Evaluation Metrics**
   - Test Accuracy
   - Training Runtime
   - Comparative trade-offs

---

## 📈 Results

| Model                  | Accuracy | Training Time |
|-------------------------|----------|---------------|
| Random Forest           | 65.5%    | 115.5 sec     |
| Multi-Layer Perceptron  | 34.4%    | 13.3 sec      |
| Convolutional Neural Net| **77.0%**| 22.7 sec      |

✅ **CNN is the best choice** for medical image classification tasks, balancing speed and accuracy. 
