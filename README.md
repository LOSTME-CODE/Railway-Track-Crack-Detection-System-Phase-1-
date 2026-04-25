# Affordable-Intelligent-Robot-for-Surveillance-of-Railway-Track
This repository contains the design, implementation, and deployment details of a low-cost, AI-powered robotic system built for real-time railway track crack detection. The system leverages YOLOv8n, Raspberry Pi 5, and dual Pi cameras to automate the inspection process and improve safety by identifying structural defects in tracks early.
Key Features
Real-time crack detection using YOLOv8n deep learning model.

GPS-enabled location tagging of detected defects.

Live video feed with GUI for human validation and logging.

Lightweight and affordable robotic platform designed for Indian railway conditions.

Custom dataset of over 24,000 images (crack & null) for robust training.

🛠 Hardware Components
Raspberry Pi 5 (8GB RAM)

2 × Raspberry Pi Camera Module v3

Arduino Nano (motor control)

GPS Module (Neo-8M)

L298N Motor Driver

4 × BO Motors

3D Printed Chassis

Power Bank + 9V Batteries

💻 Software Stack
YOLOv8n (Ultralytics) trained on custom + Roboflow datasets

Python with OpenCV for real-time video processing

PyTorch for model training

Raspberry Pi OS

Arduino IDE for motor control

Custom GUI for monitoring and data logging

📈 Model Performance
Precision: 0.988

Recall: 0.997

mAP@0.5: 0.995

mAP@0.5:0.95: 0.892

Trained for up to 130 epochs using AdamW optimizer with augmentation


For dataset download:
https://drive.google.com/file/d/1oSOizswm1wyWbeE7UcHu-PehY1hpmq3O/view?usp=sharing

