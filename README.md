# ML4Sci_DeepLense_2026
## 📊 Model Comparison

| Model | Type | Backbone | Description | FID ↓ |
|------|------|----------|-------------|------|
| DDPM | Diffusion | U-Net | Baseline diffusion model | 19.5 |
| Rectified Flow | Flow Matching | ConvNeXt | Faster flow-based generation | 28.34 |
| Rectified Flow | Flow Matching | DiT (Transformer) | High-quality transformer-based model | **4.6** |

---

## 🧠 Key Observations

- Transformer-based models (DiT) significantly outperform CNN-based models  
- Rectified Flow improves generation efficiency and quality  
- ConvNeXt backbone underperforms compared to DiT in this task  
- Best performance achieved with **Rectified Flow + DiT**
