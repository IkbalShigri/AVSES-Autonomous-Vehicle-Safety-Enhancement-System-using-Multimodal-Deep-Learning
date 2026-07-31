# AVSES-Autonomous-Vehicle-Safety-Enhancement-System-using-Multimodal-Deep-Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLO-v8-6A0DAD?style=for-the-badge)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv)
![Deep Learning](https://img.shields.io/badge/Deep-Learning-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

### 🚘 A Multimodal Deep Learning Framework for Autonomous Vehicle Safety Enhancement Through Vehicle Rear Signal Recognition and Motorcyclist Hand Gesture Understanding

</div>

---

# 📌 Overview

**AVSES (Autonomous Vehicle Safety Enhancement System)** is a multimodal deep learning framework developed to improve autonomous vehicle perception by simultaneously recognizing:

- 🚗 Vehicle Rear Signals
- 🏍️ Motorcyclist Hand Gestures

Unlike conventional vision systems that rely on a single source of information, AVSES fuses temporal visual information from two independent perception modules to enhance driving awareness and decision-making.

The system combines:

- YOLOv8 Object Detection
- CNN Feature Extraction
- LSTM Temporal Modeling
- Multimodal Fusion
- Real-time Video Processing

---

# 🎯 Motivation

Current autonomous driving systems often fail to recognize:

- Motorcyclists' manual turning intentions
- Rear vehicle signal states
- Temporal behavioral patterns

These limitations reduce situational awareness and can increase collision risk.

AVSES addresses this challenge by integrating multiple visual cues into a unified AI framework capable of robust real-time understanding.

---

# 🧠 System Architecture

```text
                     Video Stream
                           │
            ┌──────────────┴──────────────┐
            │                             │
     Vehicle Detection             Gesture Detection
          (YOLOv8)                    (YOLOv8)
            │                             │
       ROI Extraction               ROI Extraction
            │                             │
     CNN Feature Encoder         CNN Feature Encoder
            │                             │
         LSTM Model                 LSTM Model
            │                             │
            └──────────────┬──────────────┘
                           │
                 Multimodal Feature Fusion
                           │
                    Final Classification
                           │
              Driving Decision Support
```

---

# 📂 Project Structure

```text
AVSES/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── src/
│   ├── train.py
│   ├── inference.py
│   ├── models.py
│   ├── dataset.py
│   ├── utils.py
│   └── config.py
│
├── notebooks/
│
├── outputs/
│   ├── checkpoints/
│   ├── figures/
│   ├── confusion_matrix.png
│   ├── training_curve.png
│   └── best_model.pt
│
├── docs/
│   ├── architecture.png
│   ├── pipeline.png
│   └── thesis.pdf
│
└── data/
    └── README.md
```

---

# 📊 Dataset

The project uses two complementary datasets.

## 🚗 Vehicle Rear Signal Dataset

Classes

| Label | Meaning |
|--------|----------|
| BOO | Brake ON |
| OLO | Left Indicator |
| OOR | Right Indicator |
| OOO | No Signal |

---

## 🏍️ Hand Gesture Dataset

| Label | Meaning |
|--------|-----------|
| bike_left_hand | Left Turn |
| bike_right_hand | Right Turn |
| OOO_bike | Normal Riding |

---

# ⚙️ Methodology

## 1️⃣ Object Detection

YOLOv8 detects

- Rear vehicle region
- Motorcyclist

---

## 2️⃣ ROI Extraction

Relevant image regions are cropped for further processing.

---

## 3️⃣ Feature Extraction

CNN learns spatial representations.

---

## 4️⃣ Temporal Learning

LSTM learns sequential information from video clips.

---

## 5️⃣ Feature Fusion

Outputs from both modalities are combined to produce the final prediction.

---

# 🚀 Technologies

- Python
- PyTorch
- YOLOv8
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- CUDA

---

# 📈 Training Configuration

| Parameter | Value |
|------------|--------|
| Image Size | 224×224 |
| Frames per Clip | 16 |
| Optimizer | AdamW |
| Scheduler | Cosine Annealing |
| Learning Rate | 3e-4 |
| Batch Size | 8 |
| Epochs | 50 |

---

# 📊 Results

## Performance Metrics

✔ Accuracy

✔ Precision

✔ Recall

✔ F1 Score

✔ Confusion Matrix

✔ Training Curves

---

## Sample Results

```
outputs/

├── confusion_matrix.png

├── training_curve.png

├── per_class_f1.png

├── augmentation_preview.png

└── best_model.pt
```

---

# 📦 Installation

```bash
git clone https://github.com/yourusername/AVSES.git

cd AVSES

pip install -r requirements.txt
```

---

# ▶️ Training

```bash
python src/train.py
```

---

# ▶️ Inference

```bash
python src/inference.py
```

---

# 📁 Dataset Preparation

```
data/

├── Vehicle_Dataset/

│   ├── Training/

│   └── Testing/

│

└── HandGesture_Dataset/

    ├── Training/

    └── Testing/
```

---

# 📚 Research Contributions

✅ Multimodal Deep Learning

✅ Vehicle Signal Recognition

✅ Motorcyclist Gesture Recognition

✅ Temporal Sequence Learning

✅ Feature Fusion

✅ Real-time Autonomous Driving Support

---

# 🔮 Future Work

- Transformer-based temporal learning
- Vision Transformers (ViT)
- Real-time deployment on NVIDIA Jetson
- Sensor fusion with LiDAR
- Weather robustness
- Explainable AI (XAI)

---

# 📖 Citation

```bibtex
@software{AVSES2026,
  title={AVSES: Autonomous Vehicle Safety Enhancement System},
  author={Muhammad Iqbal},
  year={2026},
  url={https://github.com/IkbalShigri/AVSES}
}
```

---

# 👨‍💻 Author

**Muhammad Iqbal**

Software Engineer

Artificial Intelligence Researcher

Deep Learning | Computer Vision | Autonomous Systems

GitHub: https://github.com/IkbalShigri

LinkedIn: https://linkedin.com/in/iqbalshigri

---

# ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub.

---

## 📜 License

This project is licensed under the MIT License.
