# ECG Arrhythmia Classification Project

## Overview

This project detects cardiac arrhythmias from ECG signals using multiple deep learning architectures. Pretrained models are included so you can directly run inference without retraining.

Supported architectures:

* 1D CNN
* GRU (Recurrent Neural Network)
* ResNet1D
* Autoencoder (feature extractor / anomaly detection)

---

## Project Structure

```
ECG-Arrhythmia-Classification-main/
│
├── ECG_arrhythmia.ipynb      # Training + evaluation notebook
├── ecg_arrhythmia.py         # Main inference script
│
├── best_model.keras          # Final best performing model
├── CNN1D_best.keras          # CNN model
├── GRU1D_best.keras          # GRU model
├── ResNet1D_best.keras       # ResNet model
├── ae_best_weights.h5        # Autoencoder weights
├── ae_best_weights.keras     # Autoencoder model
```

---

## Requirements

Install dependencies first:

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn wfdb
```

Python version recommended: **3.9 – 3.11**
TensorFlow recommended: **2.12+**

---

## How To Run (Quick Start)

### 1) Clone / Download Project

```bash
git clone <your-repo-url>
cd ECG-Arrhythmia-Classification-main
```

### 2) Run Inference

```bash
python ecg_arrhythmia.py
```

The script will:

* Load pretrained model
* Process ECG signal
* Predict arrhythmia class

---

## Using a Specific Model

Inside `ecg_arrhythmia.py`, change model path:

```python
model_path = "CNN1D_best.keras"
# model_path = "GRU1D_best.keras"
# model_path = "ResNet1D_best.keras"
# model_path = "best_model.keras"
```

---

## Running Notebook (Training / Visualization)

```bash
jupyter notebook ECG_arrhythmia.ipynb
```

Use this only if you want to retrain or understand preprocessing.

---

## Output Classes (Example)

Typical MIT-BIH classes:

* N : Normal beat
* S : Supraventricular ectopic beat
* V : Ventricular ectopic beat
* F : Fusion beat
* Q : Unknown beat

---

## Notes

* Models are already trained — no GPU required for inference
* CPU inference time ≈ < 1 second per signal
* For new datasets, ensure same preprocessing pipeline

---

## Future Improvements

* Real-time ECG streaming prediction
* Web dashboard (Flask/React)
* Mobile integration
* Patient risk scoring

---

## Author Purpose

This repository is archived to preserve trained models and enable fast reuse for experiments, demos, and deployment without retraining.
