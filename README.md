# ML4Sci_DeepLense_2026




# 📌Test 1: ResNet50 Classification – Gravitational Lensing

## 🚀 Overview
Multi-class classification of strong gravitational lensing images into:

- no (no substructure)
- sphere (subhalo)
- vort (vortex)

---

## 🧠 Model

- Backbone: ResNet50 (ImageNet pretrained)
- Type: Transfer Learning
- Custom Head: Fully Connected (51200 → 128 → 64 → 3)

---

## ⚙️ Training

- Epochs: 50  
- Optimizer: Adam (1e-4)  
- Scheduler: ReduceLROnPlateau  
- Batch Size: 256  
- Multi-GPU: Yes  

---

## 🔄 Augmentation

- Rotation (±180°)  
- Translation (±20%)  
- Scaling (0.8–1.2)  
- Horizontal & Vertical Flip  

---

## 📊 Results

| Metric | Value |
|------|------|
| Accuracy | **94.49%** |
| Macro AUC | **0.9917** |
| AUC (no) | 0.9918 |
| AUC (sphere) | 0.9864 |
| AUC (vort) | 0.9969 |




# 📌Test 8: Diffusion Models for Gravitational Lensing

## 🚀 Overview
This project explores diffusion and flow-based models for generating strong gravitational lensing images. Multiple architectures are implemented and compared based on image quality using FID score.

---

## 📊 Model Comparison

| Rank | Model | Type | Backbone | Description | FID ↓ |
|------|------|------|----------|-------------|------|
|  1 | Rectified Flow + DiT | Flow Matching | Transformer (DiT) | Best performing model with high-quality generation | **4.6**  |
|  2 | DDPM | Diffusion | Transformer (DiT) | Baseline diffusion model | 19.5 |
|  3 | Rectified Flow + ConvNeXt | Flow Matching | ConvNeXt | Faster flow-based model but lower quality | 28.34 |

---

## 🧠 Key Insights

- Transformer-based models (DiT) significantly outperform CNN-based architectures  
- Rectified Flow improves generation efficiency and quality  
- ConvNeXt backbone struggles to capture fine lensing structures  
- Best performance achieved with **Rectified Flow + DiT**

# 📌 Test 7:PINN Classification – Gravitational Lensing

## 🚀 Overview
Physics-Informed Neural Network (PINN) for multi-class classification:

- no (no substructure)
- sphere (subhalo)
- vort (vortex)

---

## 🧠 Model

- Backbone: ResNet50 (ImageNet pretrained)
- Type: Physics-Informed Learning
- Added Components:
  - Lensing Kernel Layer (physics-based conv)
  - Physics Bottleneck (κ, γ prediction)

---

## ⚙️ Training

- Total Epochs: 43  
  - Phase 1: Warmup (5 epochs)  
  - Phase 2: Fine-tune (25 epochs)  
  - Phase 3: Physics Loss (13 epochs)  

- Optimizer: AdamW  
- Scheduler: Cosine Annealing  
- Batch Size: 16  

---

## 🔬 Physics Integration

- κ (convergence) ∈ [0,1]  
- γ (shear) ∈ [-1,1]  
- Physics Loss:
  - Enforces lensing equation consistency  
  - Added in final phase  

---

## 🔄 Augmentation

- Rotation (±180°)  
- Translation (±20%)  
- Scaling (0.8–1.2)  
- Flip (H + V)  

---

## 📊 Results

| Metric | Value |
|------|------|
| Accuracy | **93.28%** |
| Macro AUC | **0.9890** |
| AUC (no) | 0.9904 |
| AUC (sphere) | 0.9825 |
| AUC (vort) | 0.9942 |

---

## 🧠 Insights

- Physics + DL gives strong performance  
- κ and γ improve interpretability  
- Similar accuracy to ResNet50 baseline  


---
