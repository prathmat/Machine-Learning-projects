
# Capstone Project: Noise vs Speech Classification

## 📌 Objective

This project builds upon the initial classical ML-based analysis to classify audio segments as either **speech** or **noise** using the MS-SNSD dataset. We explored both traditional machine learning and deep learning models to determine which approach yields the best performance.

---

## 🧠 Dataset Overview

- **Source**: [Microsoft MS-SNSD Dataset](https://github.com/microsoft/MS-SNSD)
- **Content**:
  - `CleanSpeech_training`: Clean speech WAV files.
  - `NoisySpeech_training`: Speech files mixed with environmental noise at varying SNR levels.
  - train_data.csv is the CSV  created by pairing features from NoisySpeech_training with labels generated from CleanSpeech_training.This data is similar to what was used in [GitHub - Capstone Initial Analysis](https://github.com/prathmat/Machine-Learning-projects/blob/main/Capstone%20Initial%20Analysis%20Data%20Exploration/Capstone_20_1.ipynb)



---

## 🛠️ Data Preprocessing

1. Extracted **MFCC features** from each noisy WAV file.
2. Assigned labels:
   - `1` for speech segments
   - `0` for noise segments (based on clean-to-noisy alignment)
3. Framed data into sequences of 32 frames.
4. Normalized and reshaped for LSTM input.

---

## 📊 Exploratory Data Analysis

- Frame-wise energy analysis
- Class distribution
- Correlation heatmap of features
- Visualizations of MFCC distributions

(🔽 Included in Jupyter Notebook)

---

## 🧪 Model Architectures

### 1️⃣ Baseline ML Models

| Model                 | Accuracy |
|----------------------|----------|
| Decision Tree        | 89.85%   |
| Random Forest        | 94.08%   |
| K-Nearest Neighbors  | 94.73%   |
| Support Vector Machine | 91.65% |
| Logistic Regression  | 85.58%   |
| Naive Bayes          | 78.81%   |

🔍 **Observation**: Ensemble models (RF, KNN) perform better due to better generalization and less overfitting.

---

### 2️⃣ Deep Learning Models

#### Bi-directional LSTM
- Handles **temporal context** from both past and future frames.
- Reached ~86.84% accuracy.

#### CNN + BiLSTM Hybrid (Model 2)
- CNN captures **local spectral patterns** in MFCCs.
- LSTM captures **sequential temporal dynamics**.
- Reached **93.42% test accuracy**, matching and even outperforming ML models.

🧠 **Why better?**
- Learns both **spectral structure** (via convolution) and **temporal structure** (via LSTM).
- Robust to SNR variations due to context windowing.

---

## 📈 Evaluation Metrics

### Model 2 (CNN + BiLSTM)

- **Accuracy**: 93.42%
- **Precision** (Speech): 95%
- **Recall** (Speech): 94%
- **F1-Score**: 0.93

#### Confusion Matrix

|           | Pred Noise | Pred Speech |
|-----------|------------|-------------|
| **Noise** | 240        | 21          |
| **Speech**| 26         | 427         |

✅ **High true positives**, low false positives.

---

## 📌 Future Improvements

- Use attention mechanisms (e.g., self-attention or transformer blocks).
- Try CRNN (Convolutional Recurrent Neural Network) structure.
- Augment training with dynamic SNR ranges and reverberation.
- Use audio spectrograms instead of MFCCs for richer features.
- Test models on unseen real-world noise datasets.

---

## 📁 Files in This Package

- `Capstone_Improved_CNN_LSTM_vs_ML.ipynb`: Final end-to-end notebook
- `README_Improved_Model.md`: This documentation
- `conf_matrix_cnn_lstm.png`, `conf_matrix_rf.png`: Evaluation plots
- `model_comparison_metrics.csv`: Accuracy scores for all models

---

## 🔗 Original Version

Initial ML-only version: [GitHub - Capstone Initial Analysis](https://github.com/prathmat/Machine-Learning-projects/blob/main/Capstone%20Initial%20Analysis%20Data%20Exploration/Capstone_20_1.ipynb)

This project significantly improves upon the original by integrating deep learning and offering robust, high-accuracy predictions.

