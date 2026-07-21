## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#demo">Demo</a>
- <a href="#problem-statement">Problem Statement</a>
- <a href="#patent">Patent</a>
- <a href="#hardware-used">Hardware Used</a>
- <a href="#software-tools">Software & Tools</a>
- <a href="#result">Result</a>
- <a href="#deployment">Deployment</a>
- <a href="#future-work">Future Work</a>
- <a href="#system-architecture">System Architecture</a>
- <a href="#key-features">Key Features</a>

- <a href="#methodology">Methodology</a>

# 🚆 Affordable Intelligent Robot for Surveillance of Railway Track

**A Low-Cost AI-Powered Robotic System for Real-Time Railway Track Crack Detection using YOLOv8, Raspberry Pi 5 & GPS**

This project presents an intelligent and affordable robotic inspection system developed to automate railway track monitoring. The robot uses **YOLOv8n**, **Raspberry Pi 5**, **dual Raspberry Pi Camera Modules**, and **GPS-based location tagging** to detect track cracks in real time, reducing manual inspection effort while improving railway safety.

The system captures live video, performs AI inference onboard, records GPS coordinates of detected defects, and provides a GUI for visualization and logging.

---

<h3 id="demo">Demo</h3>

### System Overview

<p align="center">
<img src="https://github.com/user-attachments/assets/4759c2e5-f74b-4d98-b9cf-80791af31b0f" width="900">
</p>

### Project Contribution

Detailed implementation and contribution can be found here:

📄 **My Contribution**

https://github.com/user-attachments/files/27088280/my_contribution.pdf

---

<h3 id="overview">Overview</h3>

Railway tracks continuously undergo stress due to heavy loads, weather conditions, corrosion, and fatigue, making periodic inspection essential for passenger safety.

Traditional inspection methods rely heavily on manual labor, making the process:

- Time-consuming
- Costly
- Prone to human error
- Difficult to perform frequently

This project introduces a **low-cost autonomous robotic inspection platform** capable of:

- Detecting railway track cracks in real time
- Capturing live video
- Recording GPS coordinates
- Displaying detection status through a GUI
- Logging inspection data for future analysis

The solution is designed to be lightweight, affordable, and suitable for deployment in Indian railway environments.

---

<h3 id="problem-statement">Problem Statement</h3>

Railway track failures caused by undetected cracks can lead to severe accidents and costly maintenance. Existing inspection techniques often require specialized equipment and extensive manpower.

The objective of this project is to develop an intelligent robotic system capable of:

- Automating railway track inspection
- Detecting structural cracks using deep learning
- Recording precise GPS locations of defects
- Providing real-time monitoring through a graphical interface
- Reducing inspection time and operational costs

---
  <h3 id="patent">📜 Patent</h3>


This project has been published as an Indian patent, recognizing the novel approach for automated railway track crack detection using deep learning and an intelligent robotic inspection system.

Patent Details	

Patent Number	202521121451
Title	Computer-Implemented System and Method for Automated Railway Track Crack Detection Using Deep Learning
Status	Published (Indian Patent)


---

<h3 id="hardware-used">🔧 Hardware Used</h3>

| Component | Purpose |
|-----------|---------|
| Raspberry Pi 5 (8GB) | Main processing and AI inference |
| Raspberry Pi Camera Module v3 (×2) | Crack detection input |
| Arduino Uno/Nano | GPS communication and motor control |
| GPS NEO-M8N | Real-time location tracking |
| L298N Motor Driver | Motor control |
| 4 × BO Motors | Robot movement |
| 3D Printed Chassis | Lightweight robotic body |
| Power Bank + 9V Batteries | Power supply |
| Miscellaneous Wiring | Hardware integration |

---

<h3 id="software-tools">💻 Software & Tools</h3>

| Tool | Usage |
|------|-------|
| YOLOv8n | Railway crack detection model |
| Python (OpenCV, NumPy, Pandas) | Detection pipeline |
| PyTorch | Model training |
| ONNX Runtime | Edge inference on Raspberry Pi |
| Tkinter / CustomTkinter | GUI |
| Arduino IDE | GPS and motor control |
| VS Code | Development |
| Roboflow | Dataset creation and augmentation |

---

<h3 id="result">Result</h3>

### Model Performance

| Metric | Score |
|---------|-------|
| Precision | **0.988** |
| Recall | **0.997** |
| mAP@0.5 | **0.822** |
| mAP@0.5:0.95 | **0.62** |

### Dataset

- Original Dataset: **2,505 Images**

- Final Augmented Dataset: **9000+ Images**
- Classes:
  - Crack
  - Null

### Training Details

- Model: YOLOv8n
- Image Size: 640 × 640
- Epochs: 50–130
- Batch Size: 32
- Optimizer: AdamW (Best Performance)

### Key Outcomes

- High crack detection accuracy
- Stable deployment on Raspberry Pi 5
- Real-time inference using ONNX Runtime
- GPS-based defect localization
- GUI-assisted inspection and logging
- Lightweight robotic platform suitable for low-cost deployment

---

<h3 id="deployment">Deployment</h3>

### Install Dependencies

```bash
pip install ultralytics
pip install opencv-python
pip install numpy
pip install pandas
pip install onnxruntime
```

### Additional Setup

- Connect Raspberry Pi Camera Module v3 (Dual Cameras)
- Connect Neo-8M GPS Module
- Connect Arduino Nano via Serial
- Connect L298N Motor Driver with BO Motors
- Power Raspberry Pi and robot platform

### Run Project

```bash
python gps.py
```

```bash
python crack_detection.py
```

```bash
python gui_display.py
```

---

### Dataset

The complete training dataset used for this project can be downloaded from:

**Google Drive**

[Download Dataset](https://drive.google.com/file/d/1oSOizswm1wyWbeE7UcHu-PehY1hpmq3O/view?usp=sharing)
---

<h3 id="future-work">Future Work</h3>

- Thermal camera integration for enhanced crack detection
- LiDAR-based railway defect mapping
- Night-time inspection capability
- Cloud-based monitoring dashboard
- Automatic SMS/Email alert system
- Fully autonomous railway navigation
- Multi-defect detection beyond surface cracks


---

<h3 id="system-architecture">🏗 System Architecture</h3>

```text
Dual Raspberry Pi Cameras
            │
            ▼
     Raspberry Pi 5
            │
            ▼
   YOLOv8n Crack Detection
            │
      ┌─────┴─────┐
      ▼           ▼
 Live GUI     CSV Logging
      │
      ▼
 Detection Status

Arduino Nano ─────► GPS Module
       │
       └────────────► Raspberry Pi (Serial Communication)
```

---

<h3 id="methodology">Methodology</h3>

```text

Railway Track
      │
      ▼
Dual Raspberry Pi Cameras
      │
      ▼
Image Acquisition
      │
      ▼
Image Preprocessing
      │
      ▼
YOLOv8n Crack Detection Model
      │
      ├───────────────► Crack Detected?
      │                     │
      │                     ▼
      │             GPS Coordinate Capture
      │                     │
      ▼                     ▼
 Live GUI Display      CSV Data Logging
      │
      ▼
Real-Time Railway Track Monitoring
```

### 1️⃣ Hardware Integration

- Connect dual Raspberry Pi cameras to Raspberry Pi 5
- Connect GPS module to Arduino
- Establish Raspberry Pi ↔ Arduino serial communication
- Control robot movement using L298N motor driver

### 2️⃣ Data Collection

The dataset contains railway track images captured under various real-world conditions, including:

- Color images
- Black & White images
- Different lighting conditions
- Multiple railway track textures
- Crack and non-crack samples

### 3️⃣ Data Augmentation

The following augmentation techniques were applied to improve model robustness:

- Horizontal & Vertical Flip
- Rotation (±9°)
- Random Crop (0–9%)
- Brightness Adjustment
- Contrast Enhancement
- Noise Addition
- Grayscale Conversion

### 4️⃣ Model Training

**Model:** YOLOv8n

**Training Configuration**

- Epochs: **50–130**
- Image Size: **640 × 640**
- Batch Size: **32**

**Optimizers Evaluated**

- SGD
- AdamW (**Best Performing Optimizer**)

---

<h3 id="key-features">⭐ Key Features</h3>

- Real-time crack detection using **YOLOv8n**
- Dual camera system for improved detection accuracy
- Live GPS tracking using **NEO-M8N GPS Module**
- Instant crack detection alerts
- GUI with live camera feed
- Automatic CSV logging of:
  - Latitude
  - Longitude
  - Timestamp
  - Crack Status
- Raspberry Pi 5 deployment using **ONNX Runtime** for fast edge inference
- Custom dataset training


## 👥 Team

- **Protima Basak**
- **Namrata Todkar**
- **Samradny Ware**
- **Saachi Sharma**
  
### Project Guide

- **Dr. Priya Jadhav**
