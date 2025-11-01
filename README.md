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
**Predefined YOLOv8n**
<img width="1670" height="122" alt="image" src="https://github.com/user-attachments/assets/d66bd0ed-5fb8-47b3-97a1-894782145ba5" />

**Custom YOLOv8n**
<img width="1685" height="133" alt="image" src="https://github.com/user-attachments/assets/03ab5ac6-617c-4c4c-9a88-d3030ec14fc9" />

**Precision**
<img width="1183" height="687" alt="image" src="https://github.com/user-attachments/assets/52c6f230-ead0-4d1d-a39f-a111e7c110d6" />

**Recall**
<img width="1178" height="697" alt="image" src="https://github.com/user-attachments/assets/344a178c-d80a-4bb5-8e4c-6bcefe06aae7" />

**F1 Score**
<img width="1105" height="641" alt="image" src="https://github.com/user-attachments/assets/60bd7a2c-1187-47b8-bde7-4258a991f957" />

**mAP@50**
<img width="1052" height="615" alt="image" src="https://github.com/user-attachments/assets/a59ef505-6ebc-439d-984b-51103190f5b2" />


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
