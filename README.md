# 🧘‍♂️ Yoga Posture Correction with MediaPipe + IMU Sensor Fusion

This project presents a **real-time yoga posture detection and correction system** that integrates **computer vision** (MediaPipe) and **motion sensors** (MPU6050 IMU) to deliver **instant feedback** for safer, more accurate yoga practice.

By combining 2D pose estimation and 3D orientation data, the system enables a more holistic, intelligent, and responsive yoga assistant—suitable for beginners and experienced practitioners alike.

---

## 🚀 Project Highlights

- 📷 **MediaPipe Pose Estimation** – Detects human joints from webcam video input  
- 🎯 **MPU6050 Sensor Fusion** – Captures angular motion (pitch, roll, yaw) from the lumbar region  
- 💡 **CNN-based Classification** – Classifies 7 different yoga poses using EfficientNet-B2  
- 🔄 **Real-Time Feedback** – Guides users with live corrections like “Bent forward” or “Align spine”  
- 🔍 **High Accuracy** – Achieved **96% validation accuracy**, minimal overfitting  
- 🧩 **Data Augmentation** – Tackled class imbalance, improved generalization  

---

## 🧪 Pose Classes Recognized

The system currently supports detection and correction for the following 7 yoga postures:

1. Vrikshasana (Tree Pose)  
2. Trikonasana (Triangle Pose)  
3. Sukhasana (Sitting Pose)  
4. Marjariasana (Cat Pose)  
5. Malasana (Garland Pose)  
6. Vasisthasana (Side Plank Pose)  
7. Virabhadrasana II (Warrior Pose II)  

---

## 📊 Dataset Collection

- 📹 **Camera Feed**: Front-facing RGB webcam for keypoint extraction  
- 📡 **Sensor Input**: MPU6050 mounted at the **lumbar region**  
- 🧍‍♀️ **Multiple Volunteers** performed poses under supervision  
- 📏 Sensor values averaged and calibrated for stability  

---

## 🧱 System Architecture

flowchart TD

    A[Camera Input] --> B[MediaPipe Pose Detection]
    B --> C[Keypoint Angle Calculation]
    A2[MPU6050 Sensor] --> D[IMU Angle Extraction]
    C --> E[Fusion Module]
    D --> E
    E --> F[Posture Classification (CNN)]
    F --> G[Real-time Feedback Generation]
