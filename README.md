# RGB-to-Thermal Image Translation using GANs

Deep learning project for the **RGB-to-Thermal Transfer** Kaggle competition, focused on generating thermal images from corresponding RGB images using **Generative Adversarial Networks (GANs)**.

The project investigates multiple image-to-image translation architectures and compares their ability to learn the mapping from visible-spectrum RGB images to thermal images.

Our best-performing approach was a **Pix2Pix Conditional GAN (cGAN)**, which achieved a **PSNR of 26.05** and a **12th-place leaderboard position**.

---

## Project Overview

Thermal cameras provide information that is not directly available in conventional RGB images, particularly under challenging illumination conditions. The objective of this project was to investigate whether a deep generative model could learn the transformation:

```text
RGB Image  →  Thermal Image
