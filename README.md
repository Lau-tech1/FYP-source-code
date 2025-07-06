# ECG Image Enhancement and Noise Reduction Techniques

This repository contains the source code for our Final Year Project (FYP), which focuses on denoising ECG signals using two wavelet-based techniques:
- **Empirical Wavelet Transform (EWT)**
- **Stationary Wavelet Transform (SWT)**

We evaluate the effectiveness of these methods against two types of common ECG noise:
- **Baseline Wander (BW)**
- **Electromyogram (EMG)**

> 📁 Only the `Experimental` folder (source code) is included in this repository. Original datasets are excluded as per project guidelines. Instructions for dataset access and environment setup are provided below.

> 💡 This project is entirely developed and executed using **Jupyter Notebook**.

---

## 📁 Project Structure

```
Experimental/
├── BW_EWT/      # BW noise removal using EWT
├── BW_SWT/      # BW noise removal using SWT
├── EMG_EWT/     # EMG noise removal using EWT
└── EMG_SWT/     # EMG noise removal using SWT
```

Each folder contains:
- Python Notebooks (`.ipynb`) with processing, visualization, and evaluation
- Code for importing signals, adding synthetic noise, applying denoising techniques, and evaluating results (SNR, RMSE, PRD)

---

## 📥 Dataset Instructions

We used all 48 recordings from the MIT-BIH Arrhythmia Dataset. For each recording, only the first 10 seconds of data were extracted and used for evaluation.

This project uses the **MIT-BIH Arrhythmia Database** and **MIT-BIH Noise Stress Test Database**:

### 🔗 Download Links:
- MIT-BIH Arrhythmia Dataset: [https://physionet.org/content/mitdb/1.0.0/](https://physionet.org/content/mitdb/1.0.0/)
- MIT-BIH Noise Stress Test Database: [https://physionet.org/content/nstdb/1.0.0/](https://physionet.org/content/nstdb/1.0.0/)

> ⚠️ Create a local `Dataset/` folder for MIT-BIH signals and a `Noise/` folder for the noise signals as shown in the example structure below:

```
YourProjectRoot/
├── Dataset/           # MIT-BIH Arrhythmia records (e.g., 100.dat, 100.atr, ...)
├── Noise/             # Noise files (e.g., bw, ma)
└── Experimental/      # This repo's folder
```

---

## ⚙️ Requirements

Tested on: `Python 3.10` with **Jupyter Notebook**

You can install the required library packages by entering the following command directly in a Jupyter Notebook cell:

```bash
pip install numpy scipy matplotlib wfdb PyWavelets ewtpy
```

---

## 📊 Evaluation Metrics

We evaluate the effectiveness of the denoising techniques using the following metrics:

- **Signal-to-Noise Ratio (SNR):** Measures the strength of the signal relative to the noise.
- **Root Mean Square Error (RMSE):** Quantifies the differences between predicted and actual values.
- **Percentage Root-mean-square Difference (PRD):** Represents the distortion level between the original and denoised signals.

These metrics provide objective insights into how well each method removes noise without distorting the underlying ECG signal.

---

## ▶️ How to Run

1. Download the datasets as instructed and place them in `Dataset/` and `Noise/` folders.
2. Navigate to any of the 4 folders under `Experimental/`.
3. Open the Jupyter Notebook (e.g., `BW_EWT(100).ipynb`).
4. Run all cells sequentially to:
   - Load ECG signals and noise
   - Add synthetic noise
   - Apply the corresponding denoising technique
   - Visualize results and compute metrics (SNR, RMSE, PRD)

---
