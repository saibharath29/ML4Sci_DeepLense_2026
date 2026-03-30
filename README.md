# ML4Sci_DeepLense_2026
# 📌 Diffusion Models for Gravitational Lensing

## 🚀 Overview
This project explores diffusion and flow-based models for generating strong gravitational lensing images. Multiple architectures are implemented and compared based on image quality using FID score.

---

## 📊 Model Comparison

| Rank | Model | Type | Backbone | Description | FID ↓ |
|------|------|------|----------|-------------|------|
|  1 | Rectified Flow + DiT | Flow Matching | Transformer (DiT) | Best performing model with high-quality generation | **4.6**  |
|  2 | DDPM | Diffusion | U-Net | Baseline diffusion model | 19.5 |
|  3 | Rectified Flow + ConvNeXt | Flow Matching | ConvNeXt | Faster flow-based model but lower quality | 28.34 |

---

## 🧠 Key Insights

- Transformer-based models (DiT) significantly outperform CNN-based architectures  
- Rectified Flow improves generation efficiency and quality  
- ConvNeXt backbone struggles to capture fine lensing structures  
- Best performance achieved with **Rectified Flow + DiT**  

---

## ⚙️ Setup

```bash
pip install torch torchvision numpy matplotlib
