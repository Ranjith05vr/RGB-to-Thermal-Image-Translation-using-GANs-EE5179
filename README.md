# RGB-to-Thermal Image Translation using GANs

Deep learning project developed for the **RGB-to-Thermal Transfer Kaggle Competition**, focused on generating thermal images from RGB images using image-to-image translation models.

## Competition

**Kaggle Competition:** [RGB-to-Thermal Transfer](https://www.kaggle.com/competitions/rgb_2_thermal)

## Project Overview

Thermal cameras provide information that is fundamentally different from conventional RGB cameras and can be useful in applications such as surveillance, autonomous systems, low-light imaging, and object detection.

This project investigates whether thermal images can be generated from corresponding RGB images using **Generative Adversarial Networks (GANs)** and encoder-decoder architectures.

Multiple image-to-image translation architectures were implemented and evaluated:

- **Pix2Pix**
- **CycleGAN**
- **ResNet-based U-Net / U-Net++**
- **Dual-Attention GAN (DAGAN)**

Different loss functions, data augmentation strategies, and training hyperparameters were explored to improve the quality of the generated thermal images.

The best-performing approach was **Pix2Pix Conditional GAN (cGAN)**.

---

## Approach

The overall workflow was:

```text
RGB Images
    │
    ▼
Data Preprocessing
    │
    ├── Image Normalization
    ├── Random Cropping
    └── Horizontal / Vertical Flipping
    │
    ▼
RGB → Thermal Image Translation
    │
    ├── Pix2Pix
    ├── CycleGAN
    ├── ResNet U-Net / U-Net++
    └── DAGAN
    │
    ▼
Loss Optimization
    │
    ▼
Generated Thermal Image
    │
    ▼
PSNR Evaluation
    │
    ▼
Kaggle Submission
