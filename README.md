# 🌱 Plant Recognition Model Comparison

## 🔎 Overview
This project compares **YOLO (object detection)** and **ResNet-9 (classification)** models for plant species recognition. The study evaluates them against a traditional ANN-based approach using the **PlantifyDr dataset**, focusing on **accuracy, inference speed, and memory usage**.  

---

## 🏗️ System Architecture
- **YOLO:** Detects and classifies plants in a single pass — optimized for real-time performance.  
- **ResNet-9:** Deep residual network — optimized for accuracy and feature extraction.  

<p align="center">
  <img src="images/yolo_arch.png" alt="YOLO Architecture" width="500"/>
</p>

<p align="center">
  <img src="images/resnet_arch.png" alt="ResNet Architecture" width="500"/>
</p>

---

## ⚙️ Models & Training
- **Dataset:** PlantifyDr plant image dataset.  
- **Preprocessing:** resizing, normalization, augmentation.  
- **Training:** Python (PyTorch, OpenCV); evaluated with standard metrics.  
- **Deployment:** backend (Flask, Python), frontend (Android app in Kotlin).  

---

## 📊 Results (Reported)
- **YOLO:** 90.21% accuracy, fastest inference.  
- **ResNet-9:** 87.74% accuracy, higher detail extraction, slower inference.  
- **Reference ANN-based approach:** 92.48% accuracy (reported in literature).  

---

## 📱 App Demo
A lightweight **Android app** was developed for real-time recognition.  

<p align="center">
  <img src="images/app_screenshot_1.png" alt="App Home Screen" width="250"/>
  <img src="images/app_screenshot_2.png" alt="App Results" width="250"/>
</p>

**Usage:** capture/upload plant image → model inference → species prediction + confidence score.  
