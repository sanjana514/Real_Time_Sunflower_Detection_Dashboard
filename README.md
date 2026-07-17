### 🌻 Sunflower Detection using Supervised, Semi-Supervised & Self-Supervised Learning

A comprehensive implementation and visualization framework for **sunflower detection** using **Supervised Learning, Semi-Supervised Learning (SSL), and Self-Supervised Learning (Self-SL)** based object detection models.

This repository includes model implementations, experiment notebooks, dataset configuration, performance analysis, and a Streamlit dashboard for interactive comparison of different learning approaches.

---

## 📂 Project Structure

### 1. Baseline Models

**Location**

```
BaseLine Models/
```

Contains Jupyter notebooks for fully supervised object detection experiments using:

- YOLOv10s
- YOLO11s
- YOLO12s
- RF-DETR Nano

These notebooks include model training, evaluation, and performance analysis.

---

### 2. Dataset Configuration

**Location**

```
Data Configuration/
```

Contains the dataset configuration file generated after converting the original COCO dataset into YOLO format.

Example:

```yaml
names:
  - Sunflower
  - Sunflower
nc: 2
path: /kaggle/working/New_Converted_Dataset
train: train/images
val: valid/images
test: test/images
```

---

### 3. Self-Supervised Learning Experiments

**Location**

```
SSL Models/
```

This directory contains notebooks and experimental results for different self-supervised learning approaches.

#### 📌 Ablation Study

```
SSL Models/Ablation Study/
```

Contains hyperparameter tuning experiments and comparative analysis for selecting the best-performing SSL configuration.

---

#### 📌 BYOL

```
SSL Models/BYOL/
```

Contains implementation and experiments using the **Bootstrap Your Own Latent (BYOL)** framework integrated with different YOLO backbones.

---

#### 📌 DINO

```
SSL Models/DINO/
```

Contains experiments using **DINO-based self-supervised representation learning** with multiple YOLO variants.

---

#### 📌 Pseudo-STAC

```
SSL Models/PSEUDO_STAC/
```

Contains semi-supervised learning experiments using different labeled-to-unlabeled data ratios.

---

## 📊 Streamlit Dashboard

**Location**

```
Streamlit App/
```

The repository includes an interactive Streamlit dashboard for visualizing model performance and inference results.

Project structure:

```
Streamlit App/
│
├── app.py
├── requirements.txt
├── packages.txt
├── run_ssl_dashboard.bat
├── runs_ssl/
└── .gitignore
```

---

## ✨ Dashboard Features

The dashboard provides an interactive interface for comparing different learning approaches.

### Model Comparison

- Supervised vs Semi-Supervised vs Self-Supervised models
- Comparison across multiple YOLO backbones
- Performance evaluation using best trained models

### Performance Visualization

- Precision
- Recall
- mAP
- Training Loss
- Validation Loss
- Learning Curves

### Prediction Visualization

Supports inference on:

- Images
- Videos
- Webcam / Live Camera Feed

### Result Exploration

Users can browse:

- Prediction examples
- Detection outputs
- Evaluation plots
- Performance summaries

---

## 🛠 Technologies Used

- Python
- PyTorch
- Ultralytics YOLO
- RF-DETR
- BYOL
- DINO
- Streamlit
- OpenCV
- Pandas
- Matplotlib

---

## 🚀 Running the Dashboard

Install the required dependencies

```bash
pip install -r requirements.txt
```

Launch the application

```bash
streamlit run app.py
```

or execute

```
run_ssl_dashboard.bat
```

---

## 📈 Project Highlights

- Supervised object detection experiments
- Semi-supervised learning pipeline
- Self-supervised representation learning
- Ablation study analysis
- Interactive Streamlit dashboard
- Image, video and webcam inference
- Performance comparison across multiple detection models

---

## 📄 License

This repository is intended for research and educational purposes.