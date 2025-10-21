## Qwen Image Edit Model & GPU Compatibility Chart

This document summarizes the optimal combinations of **Qwen-Image-Edit-2509** based models and **RTX A4500, RTX 4000 Ada, RTX 4090** GPUs.

---

## 🚀 1. GPU Key Specifications Summary

| Item / GPU | RTX A4500 | RTX 4000 Ada | RTX 4090 |
|:------------|:-----------:|:-------------:|:-----------:|
| **Architecture** | Ampere | Ada Lovelace | Ada Lovelace |
| **VRAM** | 20 GB GDDR6 | 20 GB GDDR6 | **24 GB GDDR6X** |
| **CUDA Cores** | 7,168 | 6,144 | **16,384** |
| **BF16 Support** | Partial | High | **Full Support** |
| **TDP** | 200 W | **130 W** | 450 W |

<sub>※ Optimized for GitHub Markdown — uniform width & compact layout</sub>

---

## 🧠 2. Qwen Image Edit Model Characteristics

Comparison of key features and VRAM requirements for Qwen-Image-Edit-2509 derivative models.

| Model Name | Precision | Steps | Est. VRAM Req. | Summary | Quality | Speed |
|:------------|:----------:|:------:|:---------------:|:--------|:--------:|:------:|
| `Qwen-Image-Edit-2509_bf16` | bf16 | Free | ≥ 16–20 GB | Original, highest quality | ⭐⭐⭐⭐⭐ | ⭐ |
| `svdq-int4_r128-lightningv2.0-4steps` | int4 | 4 | 10–14 GB | Quality / speed balance | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| `svdq-fp4_r32-lightningv2.0-8steps` | fp4 | 8 | 6–10 GB | Ultra-light, ultra-fast | ⭐⭐½ | ⭐⭐⭐⭐⭐ |

<sub>**Qwen Image Edit Model — Hugging Face Repository**</sub>

---

## 🎯 3. Optimal Model Recommendations per GPU

| GPU Model | **Recommended Model** | **Key Reason** |
|:-----------|:----------------------|:------------------------------|
| **RTX A4500 (20 GB)** | `svdq-int4_r128-lightningv2.0-4steps` | 20 GB VRAM — balanced quality/speed |
| **RTX 4000 Ada (20 GB)** | `svdq-fp4_r32-lightningv2.0-8steps` | Ada optimized — ultra-fast / lightweight |
| **RTX 4090 (24 GB)** | `Qwen-Image-Edit-2509_bf16` | 24 GB VRAM + BF16 full support = highest quality |

---

## 📝 Conclusion

- **RTX A4500** → `svdq-int4_r128 Lightning` → **Balanced quality/speed**  
- **RTX 4000 Ada** → `svdq-fp4_r32 Lightning` → **Ultra-fast/light + Ada optimized**  
- **RTX 4090** → `BF16 Full` → **Highest quality**

---

<sub>*📄 Date: 2025-10-21*  
*Sources: Hugging Face, NVIDIA Official Specs, Nunchaku-Tech Qwen Image Edit Model Repository*</sub>
