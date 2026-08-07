# YOLOv8 Structured Pruning for Mobile Food Detection

> Optimization of YOLOv8 Using Structured Pruning Based on Dependency Graph for Food Detection and Nutritional Information on Mobile Devices.

This repository contains the implementation of my undergraduate thesis, which focuses on optimizing the YOLOv8 object detection model using structured pruning based on a dependency graph. The optimized model is deployed on Android devices using TensorFlow Lite to perform food detection and display nutritional information.

---

## 🚀 Project Highlights

- 📱 Successfully deployed on Android using TensorFlow Lite
- 🧠 YOLOv8s optimized with Structured Pruning (Dependency Graph)
- 📦 Model size reduced by **45.5%**
- ⚡ Lower memory usage compared to the original YOLOv8s model
- 🍽️ Detects Indonesian food and displays nutritional information
- 📊 Trained and evaluated on a custom dataset consisting of **682 annotated images**

---

## 📸 Mobile Application Demo

<p align="center">
  <img src="docs/images/demo-1.png" width="45%">
</p>

---

## ✨ Features

- Real-time food detection using YOLOv8
- Structured pruning based on Dependency Graph
- TensorFlow Lite deployment for Android
- Nutritional information display for detected food
- Bounding box visualization with confidence scores
- Configurable confidence threshold
- Multi-thread inference support
- Lightweight model suitable for mobile deployment

---

## 📈 Performance Summary

### Model Optimization

| Model | Parameters | Model Size | mAP@0.5 | FPS (GPU) |
|-------|-----------:|-----------:|---------:|----------:|
| YOLOv8s | 11.13 M | 21.49 MB | 85.11% | 63.1 |
| YOLOv8s-Pruned20 | 7.54 M | 14.65 MB | 78.17% | 55.7 |
| **YOLOv8s-Pruned30** | **6.05 M** | **11.80 MB** | **80.64%** | **58.0** |
| YOLOv8s-Pruned50 | 3.60 M | 7.13 MB | 73.75% | 70.8 |

The **30% pruned model** was selected for Android deployment because it provides the best balance between detection accuracy, model size, and mobile inference performance.

---

### Android Deployment Performance

| Device | Average Inference | FPS | Memory Usage |
|---------|-----------------:|----:|-------------:|
| Samsung Galaxy S24 Ultra | 354.8 ms | 2.88 | 104.8 MB |
| Xiaomi 13T | 641.3 ms | 1.56 | 119.3 MB |

The deployed TensorFlow Lite model achieved:

- **45.5% smaller model size**
- **Lower memory consumption**
- Successful deployment on Android devices
- Stable food detection and nutritional information display

Although the application does not yet achieve real-time performance (20–30 FPS), it is suitable for informational and nutritional assistance applications where immediate frame rates are not a strict requirement.
