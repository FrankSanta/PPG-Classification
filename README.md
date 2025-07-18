# Cardiac Arrhythmia Classification from PPG Signals

_This project was developed as part of the final assignment for the **Biomedical Data Analysis and Modeling** course at Politecnico di Milano._

## 🧠 Overview

This project addresses the detection of cardiac arrhythmias from photoplethysmographic (PPG) signals, focusing on distinguishing:
- Normal pulses,
- Premature Atrial Contractions (PAC),
- Premature Ventricular Contractions (PVC).

Both **binary classification** (Normal vs PAC/PVC) and **ternary classification** (Normal vs PAC vs PVC) problems are explored using traditional Machine Learning and Deep Learning approaches.

A **novel custom F1-score** was proposed to better evaluate model performance under severe class imbalance.

## 📊 Features

- 🩺 **PPG Signal Preprocessing**:
  - Resampling, artifact detection (PSD-based), bandpass filtering.
  - Segmentation with dual strategies based on signal quality.
- 🔍 **Anomaly Detection**:
  - Autoencoder-based detection of corrupted segments.
- 🧬 **Feature Extraction**:
  - Statistical, peak, and peak-to-peak features.
- ⚙️ **Feature Preprocessing**:
  - Z-score normalization, KNN imputation, and min-max scaling.
- 🧹 **Feature Selection**:
  - Correlation- and variance-based filtering (reduced from 40 to 12 features).
- 📈 **Modeling**:
  - ML Models: SVM, LDA, KNN, Random Forest, AdaBoost, Gradient Boosting.
  - DL Models: VGG, ResNet, Wide DenseNet, Wide ResNet + CBAM, LSTM with Multi-Head Attention.
- 🧪 **Custom Evaluation Metric**:
  - Weighted F1-score giving importance to minority classes.
- 📊 **Confidence Analysis**:
  - Prediction confidence tracked for underrepresented classes.

## 🔬 Results

### 🟢 Binary Classification (Normal vs PAC/PVC)

| Model         | Custom F1-Score | Best Precision/Recall         |
|---------------|-----------------|-------------------------------|
| AdaBoost      | 0.92            | High recall & precision       |
| Random Forest | 0.92            |                               |
| KNN           | 0.89            |                               |
| Wide DenseNet | 0.80            | DL-based model, fair results  |

### 🟠 Ternary Classification (Normal, PAC, PVC)

| Model             | Custom F1-Score | Notable Points                        |
|------------------|-----------------|---------------------------------------|
| AdaBoost / RF    | 0.65            | Best among ML models                  |
| VGG              | 0.52            | Most distinguishable among DL models  |
| CBAM / ResNet DL | 0.48 - 0.50     | Slightly better than DenseNet and LSTM|

## 🧰 Tools & Technologies

- **Signal Processing Libraries** – for PSD analysis and Butterworth filtering.
- **NumPy, SciPy, Pandas** – for data handling and statistical analysis.
- **Matplotlib, Seaborn** – for visualization of signals and results.
- **Scikit-learn** – for traditional ML models, preprocessing, and evaluation.
- **TensorFlow/Keras, PyTorch** – for deep learning models including VGG, ResNet, LSTM, CBAM.

## 🧑‍💻 Authors

- **Maurizio Pandocchi** – Biomedical Engineering @ Politecnico di Milano  
- **Francesca Vacca** – Biomedical Engineering @ Politecnico di Milano  
- **Francesco Santambrogio** – Computer Science & Engineering @ Politecnico di Milano  

