# A Lightweight MobileNetV2-Based Framework for Underwater Image Classification Using a Balanced Dataset and Quantized Image Representations 

<p align="center">
  <b>Hardware-Oriented Preprocessing + Lightweight Deep Learning for Underwater Image Classification</b>
</p>

---

## 📌 Overview

Underwater images often suffer from poor visibility, low contrast, color distortion, noise, and complex backgrounds. These characteristics make underwater object classification challenging, particularly for resource-constrained edge devices such as autonomous underwater vehicles (AUVs) and remotely operated vehicles (ROVs).

This project proposes a preprocessing and classification pipeline that combines underwater image enhancement, adaptive foreground segmentation, low-bit image representation, and lightweight deep learning.

The main objective is to investigate the effect of reducing image precision from conventional 8-bit representation to **1-bit, 2-bit, and 3-bit representations** while maintaining classification performance using **MobileNetV2**.

The preprocessing pipeline is designed with future FPGA/ASIC implementation in mind by using an optimized integer-based Otsu thresholding approach and shift-based quantization.

---

# 🎯 Project Objective

The primary objective is to develop and evaluate a memory-efficient underwater image classification pipeline.

The project investigates:

- Underwater image enhancement using WGN and CLAHE
- Foreground segmentation using optimized Otsu thresholding
- Reduction of image precision using MSB-preserving bit-shift quantization
- Classification using MobileNetV2
- The effect of 1-bit, 2-bit, and 3-bit image representations on classification accuracy
- Class-wise classification performance
- Image-quality improvement using UIQM and UCIQE
- Hardware-oriented preprocessing suitable for future FPGA/ASIC implementation

The central research question is:

> **How much can the image representation be reduced while maintaining acceptable underwater image classification performance?**

---

# 🧠 Overall Methodology

```text
                    DUO Dataset
                         │
                         ▼
                Object Cropping
                         │
                         ▼
                Dataset Balancing
                         │
                         ▼
                 Image Resizing
                    256 × 256
                         │
                         ▼
                  Data Augmentation
                         │
                         ▼
              White Gaussian Noise
                         │
                         ▼
                       CLAHE
                         │
                         ▼
              Optimized Otsu Threshold
                         │
                         ▼
                Binary Mask Generation
                         │
                         ▼
               Foreground Segmentation
                         │
                         ▼
             MSB-Preserving Quantization
                   /       |       \
                  /        |        \
               1-bit     2-bit     3-bit
                  \        |        /
                   \       |       /
                         ▼
                     MobileNetV2
                         │
                         ▼
                 4-Class Prediction
                         │
                         ▼
       Accuracy / Precision / Recall / F1
                         │
                         ▼
                  Experimental Analysis
