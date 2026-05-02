# 🎯 Video Stability Analysis using Optical Flow and 3D CNN

### Extracting Motion Patterns from Video Sequences

---

## 📌 Overview

This project analyzes motion patterns in video data and classifies stability using a combination of classical computer vision and deep learning techniques.

The system computes motion-based stability scores using optical flow, generates labels automatically, and trains a 3D Convolutional Neural Network (3D CNN) to classify videos into stable and unstable categories.

---

## ❓ Problem Statement

Raw video data is unstructured and does not directly provide information about motion stability.

The objective of this project is to:

* Extract meaningful motion information from video sequences
* Quantify motion stability using feature engineering
* Classify videos into stable and unstable categories

---

## 🚀 Key Features

* 🎥 Video preprocessing and frame extraction
* 🌊 Optical Flow-based motion analysis
* 📊 Stability score computation
* 🏷️ Automatic dataset labeling (heuristic-based)
* 🗂️ Dataset organization (stable vs unstable)
* 🧠 3D CNN model for classification
* 📈 Model training and evaluation

---

## 🧠 Project Pipeline

```plaintext
Raw Video Data
        ↓
Optical Flow Analysis (main.py)
        ↓
Motion Features + Stability Score
        ↓
Auto Label Generation (sort_dataset.py)
        ↓
Structured Dataset
   ├── stable/
   └── unstable/
        ↓
3D CNN Training (train.py)
        ↓
Classification Accuracy
```

---

## 📁 Project Structure

```plaintext
video-stability-analysis-3dcnn/
│
├── src/
│   ├── main.py              # Optical flow + feature extraction
│   ├── sort_dataset.py     # Label generation + sorting
│   ├── train.py            # Model training
│   ├── data_loader.py      # Dataset loading
│   ├── model_3dcnn.py      # 3D CNN model
│   ├── preprocessing.py
│   ├── optical_flow.py
│   ├── feature_extraction.py
│   ├── stability_index.py
│   ├── visualization.py
│
├── dataset/
│   ├── stable/
│   └── unstable/
│
├── Data/
│   └── labels.xlsx
│
├── Results/
│   └── final_results.xlsx
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
git clone https://github.com/CodeVoyager7777/video-stability-analysis-3dcnn.git
cd video-stability-analysis-3dcnn
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

---

## ▶️ Usage

### 1️⃣ Run Optical Flow + Feature Extraction

```bash
python src/main.py
```

### 2️⃣ Generate Labels & Organize Dataset

```bash
python src/sort_dataset.py
```

### 3️⃣ Train the Model

```bash
python src/train.py
```

---

## 🧪 Model Details

* Model: **3D Convolutional Neural Network (3D CNN)**
* Input: Video clips
* Frame size: `64 × 64`
* Frames per video: `8`
* Classes:

  * Stable Motion
  * Unstable Motion

---

## 🧠 Core Idea

Instead of relying on manual labeling, this project:

> Automatically generates labels using motion-based stability scores derived from optical flow.

This enables scalable dataset creation for supervised learning.

---

## 📊 Results

* Achieved ~79% accuracy on test dataset
* Model learns motion-based stability patterns from video sequences

---

## ⚠️ Limitations

* **Heuristic Labeling:** Labels are generated using a mean-based threshold instead of ground-truth annotations.
* **Threshold Sensitivity:** The threshold may not generalize well across different datasets.
* **Limited Evaluation Metrics:** Performance is evaluated mainly using accuracy.
* **No Model Comparison:** The model is not benchmarked against alternative approaches.

---

## 🚀 Future Scope

* Improve labeling using annotated or semi-supervised data
* Compare with alternative models (2D CNN, LSTM, classical ML)
* Add advanced evaluation metrics (precision, recall, F1-score)
* Improve model generalization and robustness

---

## 🛠️ Tech Stack

* Python
* OpenCV
* NumPy & Pandas
* PyTorch
* Matplotlib

---

## 👨‍💻 Author

Laksh Makkar
GitHub: https://github.com/CodeVoyager7777
