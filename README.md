# A Lightweight MobileNetV2-Based Framework for Underwater Image Classification Using a Balanced Dataset and Quantized Image Representations

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow" alt="TensorFlow">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv" alt="OpenCV">
  <img src="https://img.shields.io/badge/Model-MobileNetV2-red" alt="MobileNetV2">
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-yellow?logo=googlecolab" alt="Google Colab">
</p>

---

## 📌 Project Overview

Underwater image classification is challenging because images captured in underwater environments are affected by color distortion, wavelength-dependent attenuation, scattering, turbidity, poor illumination, and reduced contrast. These degradations can significantly affect the performance of computer vision and deep learning models.

This project presents a **lightweight MobileNetV2-based framework for underwater image classification**, with an emphasis on improving image quality while maintaining computational efficiency.

The work starts from the publicly available **DUO underwater dataset**. The original dataset was processed and reorganized into a classification-oriented dataset through data cleaning, class-wise organization, balancing, and image preprocessing.

Multiple underwater image enhancement techniques were investigated:

- White Balance
- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- FUnIE-GAN

The enhanced images are subsequently evaluated using underwater image quality metrics such as **UIQM** and **UCIQE** and are used as inputs to a lightweight **MobileNetV2 classification framework**.

The project also investigates **quantized image representations** with the objective of reducing computational and memory requirements and improving the suitability of the framework for resource-constrained edge platforms.

---

# 🎯 Objectives

The primary objectives of this project are:

- To develop a classification-ready underwater image dataset from the DUO dataset.
- To organize the dataset into class-specific categories.
- To address class imbalance through dataset balancing.
- To investigate conventional underwater image enhancement techniques.
- To investigate deep-learning-based underwater image enhancement.
- To compare image enhancement methods using non-reference underwater image quality metrics.
- To develop a lightweight underwater image classification model using MobileNetV2.
- To investigate quantized image representations for efficient processing.
- To study the effect of image enhancement on classification performance.
- To develop a framework suitable for future deployment on resource-constrained edge and underwater robotic platforms.

---

# 🌊 Problem Statement

Images acquired underwater are significantly different from images captured in conventional terrestrial environments.

The major challenges include:

### Color distortion

Different wavelengths of light are attenuated at different rates underwater, causing a strong blue or green color cast.

### Reduced contrast

Scattering and turbidity reduce the contrast between objects and their surroundings.

### Non-uniform illumination

Artificial and natural underwater lighting can result in uneven illumination across an image.

### Haze and scattering

Suspended particles scatter light and introduce haze-like effects.

### Loss of fine details

The combined effects of attenuation and scattering can cause important visual features to disappear.

These problems can negatively affect image classification models.

Therefore, this project investigates whether suitable image enhancement and lightweight deep learning can improve underwater classification while keeping computational requirements relatively low.

---

# 🗂️ Dataset

## Source Dataset

The project uses the publicly available **DUO underwater dataset** as the source dataset.

The original dataset was obtained for research purposes and subsequently processed to make it suitable for image classification.

The original dataset is **not redistributed in this repository**.

---

## Dataset Preprocessing

The source dataset was transformed into a classification-ready dataset through a preprocessing pipeline.

The preprocessing workflow includes:

```text
Original DUO Dataset
        │
        ▼
Dataset Inspection
        │
        ▼
Data Cleaning
        │
        ▼
Class-wise Organization
        │
        ▼
Class Balancing
        │
        ▼
Image Standardization
        │
        ▼
Classification-ready Dataset
