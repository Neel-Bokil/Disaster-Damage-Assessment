# 🏚️ Disaster Damage Assessment using Deep Learning

## 📌 Project Overview

This project presents a Deep Learning-based Disaster Damage Assessment System that automatically detects and classifies affected regions from satellite imagery after natural disasters such as floods, earthquakes, wildfires, and tsunamis.

A U-Net semantic segmentation model with a ResNet34 encoder is trained on the xBD (xView2) disaster dataset to identify and classify damage severity at the pixel level.

The system is deployed through a Streamlit web application, allowing users to upload pre-disaster and post-disaster satellite images and obtain:

- Damage segmentation masks
- Damage overlays
- Damage severity assessment
- Pixel-wise damage statistics

---

## 🎯 Problem Statement

Develop a deep learning-based image segmentation model to detect and classify affected regions from satellite imagery after natural disasters, enabling faster disaster response and damage assessment.

---

## 📂 Dataset

### xBD (xView2) Disaster Dataset

The project uses the xBD dataset, one of the largest publicly available disaster damage assessment datasets.

Dataset contains imagery from:

- Floods
- Wildfires
- Earthquakes
- Tsunamis
- Volcanic Eruptions

Damage Classes:

| Class ID | Class Name |
|-----------|------------|
| 0 | Background |
| 1 | No Damage |
| 2 | Minor Damage |
| 3 | Major Damage |
| 4 | Destroyed |

---

## 🛠️ Project Pipeline

### Notebook 1
Data Preparation and Dataset Exploration

### Notebook 2
Pre/Post Disaster Image Pair Generation

### Notebook 3
Segmentation Mask Generation and Pixel Distribution Analysis

### Notebook 4
U-Net Model Training and Evaluation

### Notebook 5
Inference, Visualization, and Streamlit Asset Preparation

---

## 🧠 Model Architecture

### U-Net

Encoder:
- ResNet34

Input:
- Pre-Disaster Image
- Post-Disaster Image

Input Shape:

```text
6 × 256 × 256
```

Output Shape:

```text
5 × 256 × 256
```

Loss Function:
- Weighted Cross Entropy Loss

Optimizer:
- Adam

---

## 📊 Dataset Statistics

Pixel Distribution:

| Class | Percentage |
|---------|-----------|
| Background | 98.34% |
| No Damage | 1.33% |
| Minor Damage | 0.13% |
| Major Damage | 0.08% |
| Destroyed | 0.11% |

The dataset exhibits severe class imbalance, making damage-region segmentation a challenging task.

---

## 📈 Model Performance

### Test Results

| Metric | Score |
|----------|---------|
| Loss | 0.6411 |
| Mean IoU | 0.2743 |
| Mean Dice | 0.3292 |

### Class-wise IoU

| Class | IoU |
|---------|---------|
| Background | 0.9432 |
| No Damage | 0.2711 |
| Minor Damage | 0.0642 |
| Major Damage | 0.0340 |
| Destroyed | 0.0258 |

### Class-wise Dice

| Class | Dice |
|---------|---------|
| Background | 0.9704 |
| No Damage | 0.4183 |
| Minor Damage | 0.1135 |
| Major Damage | 0.0623 |
| Destroyed | 0.0479 |

---

## 🖥️ Streamlit Application Features

The deployed application allows users to:

- Upload pre-disaster imagery
- Upload post-disaster imagery
- Generate damage segmentation masks
- Visualize damage overlays
- View pixel-wise damage reports
- Obtain overall damage severity assessment

---

## 📸 Sample Output

The application generates:

- Pre-Disaster Image
- Post-Disaster Image
- Predicted Segmentation Mask
- Damage Overlay
- Damage Assessment Report

---

## 🚀 Installation

Clone the repository:

```bash
git clone <your_repo_url>
cd Disaster-Damage-Assessment
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app.py
```

---

## 📦 Requirements

Main Libraries:

- Python 3.11
- PyTorch
- Torchvision
- Segmentation Models PyTorch
- OpenCV
- NumPy
- Pandas
- Pillow
- Streamlit

---

## 🌐 Deployment

### GitHub Repository

Source code and notebooks are hosted on GitHub.

### Hugging Face

The trained model weights are hosted on Hugging Face due to GitHub file-size limitations.

### Streamlit Cloud

The application is deployed using Streamlit Community Cloud.

---

## 🔮 Future Improvements

- Train using post-disaster imagery only
- Increase training epochs
- Incorporate Dice + Focal Loss
- Use stronger encoders (ResNet50 / EfficientNet)
- Improve performance on minority damage classes
- Add batch inference support

---

## 👨‍💻 Author

Neel Bokil

M.Tech (Artificial Intelligence)


---

## 📜 License

This project is developed for academic and research purposes.
