# Deep Learning-Based Detection of Wooden Pallets Using YOLOv8

---

## Project Overview

> This project presents an AI-based system to **automatically detect and classify wooden pallets** — specifically **EUR** and **non-EUR** pallets — using the **YOLOv8n** deep learning model.  
>  
> The goal is to enhance **Trackmate AB’s logistics automation** by reducing manual labor and improving pallet identification accuracy in real-time.

### Objectives
- Detect and classify **EUR** and **non-EUR** pallets.
- Compare **predefined** and **customized YOLOv8n** models.
- Achieve high detection accuracy with minimal inference time.
- Enable **edge deployment** on low-resource devices (e.g., forklift cameras).

### Dataset Summary
- **Total images:** 202 annotated pallet images  
- **Augmentation:** Each training image augmented 3× per fold  
- **Cross-validation:** 3-fold  
  - ~536 training images  
  - ~54 validation images  
- **Annotation tool:** `labelImg`  
- **Augmentation library:** `Albumentations`

- ### Model Training
- Framework: `Ultralytics YOLOv8`
- Training image size: `640×640`
- Validation strategy: 3-fold cross-validation
- Metrics evaluated: **Precision**, **Recall**, **F1-Score**, **mAP@0.5**

---

## Results
<img width="1670" height="122" alt="image" src="https://github.com/user-attachments/assets/d66bd0ed-5fb8-47b3-97a1-894782145ba5" />

| Model Type         | Precision | Recall | F1-Score | mAP@0.5 |
|--------------------|------------|---------|-----------|----------|
| **Predefined YOLOv8n** | **0.86** | **0.84** | **0.85** | **0.88** |
| Custom YOLOv8n     | 0.90 | 0.62 | 0.73 | 0.74 |

### Interpretation
- The **predefined YOLOv8n** model achieved the **best overall performance**, balancing speed and accuracy.
- It is **lightweight** and suitable for **real-time inference** on edge devices.
- The **custom model**, while having higher precision, suffered from lower recall — missing more true detections.

### Key Observations
- Consistent results across lighting, occlusion, and varied pallet angles.
- Robust generalization in real-world logistics settings.
- Significant improvement in detection automation accuracy compared to manual methods.

### Summary
- **mAP@50:** 88%  
- **Precision:** 86%  
- **Recall:** 84%  
- **F1-Score:** 85%  
- **Inference speed:** Suitable for real-time deployment.
