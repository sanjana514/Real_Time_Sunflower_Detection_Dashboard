# 🌻 SSL, Semi-Supervised & Self-Supervised Sunflower Detection — Results & Dashboard

This repository contains the **result files, configuration files, SSL model outputs, ablation studies, and a Streamlit-based dashboard** for visualizing and comparing supervised, semi-supervised, and self-supervised sunflower detection experiments.

⚠️ **This repo contains scripts and results**  
All folders store outputs generated from YOLO/SSL experiments on a COCO-formatted sunflower dataset.


## 🧪 What This Repository Contains

### **1️⃣ Baseline Supervised Model Outputs**
Located in:

BaseLine Models/ ---> .ipynb files of baseline supervised models

  - YOLOv10s
  - YOLO11s
  - YOLO12s
  - RF-DETR nano

### **2️⃣ Dataset Configuration**
Data Configuration/data_Sunflower.yaml ---> contains the transformed yaml file after transformation from COCO to YOLO

data_Sunflower.yaml
```yaml
  names:
  - Sunflower
  - Sunflower
  nc: 2
  path: /kaggle/working/New_Converted_Dataset
  test: test/images
  train: train/images
  val: valid/images
```


### **3️⃣ SSL Model Results**
Stored inside:
```lua
SSL Models/
│── Ablation Study/ ---> Contains different hyperparameter based best SSL performence
│── BYOL/ ---> Contains YOLO backbone based model file
│── DINO/ ---> Contains YOLO backbone based model file
└── PSEUDO_STAC/ ---> Contains best YOLO backbone based model file for different label ratio
```

### **4️⃣ Streamlit Dashboard**
Found in:
```lua
Streamlit App/
│ ├── runs_ssl/ # model output folders for dashboard
│ ├── app.py # Streamlit dashboard
│ ├── requirements.txt # dependencies
│ ├── packages.txt
│ ├── run_ssl_dashboard.bat # one-click run script (Windows)
│ └── .gitignore
```
This is a **fully interactive visualization dashboard** for comparing:

- Semi-Supervised and SSL performace through best.pt files
- Per-model mAP/P/R curves  
- Train/Val loss plots  
- Prediction example galleries that is image, video and live camera feed
