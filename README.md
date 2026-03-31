# 🚗 Driver Drowsiness Detection System using OpenCV

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]()
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg)]()

---

## 📌 Overview

This project implements a **Driver Drowsiness Detection System** using **Computer Vision**.
It monitors the driver's eye movements in real-time and detects fatigue using the **Eye Aspect Ratio (EAR)**.
If drowsiness is detected, an **alarm is triggered** to alert the driver and prevent accidents.

---

## 🎯 Applications

- 🚗 Long-distance drivers
- 🚛 Truck and transport monitoring
- 🚌 Public transport safety
- 🏍️ Riders prone to fatigue

---

## 🧠 Key Features

- Real-time face detection
- Facial landmark detection (eyes tracking)
- Eye Aspect Ratio (EAR) calculation
- Drowsiness detection based on blink duration
- Alarm alert system

---

## 🛠️ Code Requirements

- Python 3.x (2.7+ supported)
- Webcam

---

## 📦 Dependencies

Install all dependencies using:

```bash
pip install opencv-python imutils dlib scipy playsound
```

Libraries used:

```python
import cv2
import imutils
import dlib
import scipy
import playsound
import queue
import time
import sys
```

---

## 📝 Description

This system uses OpenCV and Dlib to detect driver drowsiness in real-time. It captures video from a webcam, detects facial landmarks, extracts eye regions, and calculates EAR. If the eyes remain closed beyond a threshold duration, the system identifies drowsiness and triggers an alert.

---

## ⚙️ Algorithm

### 1️⃣ Face Detection

- Uses Dlib's HOG + Linear SVM based face detector

<img src="https://github.com/omsingh031/Driver-Drowsiness-Detection-System/blob/main/face.PNG" width="400"/>

### 2️⃣ Facial Landmark Detection

- Detects 68 facial landmarks
- Extracts eye coordinates

### 3️⃣ Eye Detection

<img src="https://github.com/omsingh031/Driver-Drowsiness-Detection-System/blob/main/eye.PNG" width="400"/>

### 4️⃣ Eye Aspect Ratio (EAR)

- Determines whether eyes are open or closed
- Threshold ≈ 0.3

<img src="https://github.com/omsingh031/Driver-Drowsiness-Detection-System/blob/main/eye_aspect_ratio.png" width="400"/>

### 5️⃣ Drowsiness Logic

- Normal blink: 200–300 ms
- Drowsy blink: 800–900 ms
- If EAR < threshold for long → Drowsiness Detected

---

## ▶️ Execution

Run the following command:

```bash
python blinkDetect.py
```

---

## 📂 Project Structure

```
Driver-Drowsiness-Detection/
│
├── blinkDetect.py
├── alarm.wav
├── shape_predictor.dat
├── eye.png
├── face.png
├── eye_aspect_ratio.png
└── README.md
```

---

## 📊 Results

- Detects eye closure in real-time
- Differentiates normal vs drowsy blinking
- Triggers alert instantly

---

## ⚠️ Limitations

- Sensitive to lighting conditions
- Requires proper camera angle
- Accuracy depends on hardware

---

## 🔮 Future Improvements

- Deep learning models (YOLO, CNN)
- Head pose detection
- Yawning detection
- Mobile app integration

---

## 🧑‍💻 Author

**Om Kumar Singh**
B.Tech CSE (AI), VIT Bhopal

---

## ⭐ Acknowledgment

Inspired by real-world driver safety challenges and open-source CV implementations.
