## Qwen Image Edit Model & GPU Compatibility Chart

This document summarizes the optimal combinations of **Qwen-Image-Edit-2509** based models and **RTX A4500, RTX 4000 Ada, RTX 4090** GPUs.

---

## 🚀 1. GPU Key Specifications Summary

| Item / GPU | RTX A4500 | RTX 4000 Ada | RTX 4090 |
|:-----------|:----------|:-------------|:----------|
| **Architecture** | Ampere | Ada Lovelace | Ada Lovelace |
| **VRAM**    | 20 GB GDDR6 | 20 GB GDDR6 | **24 GB GDDR6X** |
| **CUDA Cores** | 7168 | 6144 | **16384** |
| **BF16 Support** | Partial | High | **Full Support** |
| **TDP**     | 200W | **130W** | 450W |

---

## 🧠 2. Qwen Image Edit Model Characteristics

Comparison of key features and VRAM requirements for Qwen-Image-Edit-2509 derivative models.

| Model Name | Precision | Steps | Est. VRAM Req. | Summary | Quality | Speed |
|:-----------|:----------|:------|:---------------|:--------|:--------|:------|
| `Qwen-Image-Edit-2509_bf16` | bf16 | Free | ≥ 16~20GB | Original, highest quality | ⭐⭐⭐⭐⭐ | ⭐ |
| `svdq-int4_r128-lightningv2.0-4steps` | int4 | 4 | 10~14GB | Quality/speed balance | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| `svdq-fp4_r32-lightningv2.0-8steps` | fp4 | 8 | 6~10GB | Ultra-light, ultra-fast | ⭐⭐½ | ⭐⭐⭐⭐⭐ |

<sub>**[Qwen Image Edit Model hugginface](https://huggingface.co/nunchaku-tech/nunchaku-qwen-image-edit-2509/tree/main)**</sub>

---

## 🎯 3. Optimal Model Recommendations per GPU

| GPU Model | **Recommended Model** | **Key Recommendation Reason** |
|:----------|:----------------------|:------------------------------|
| **RTX A4500 (20GB)** | `svdq-int4_r128-lightningv2.0-4steps` | 20GB VRAM, **quality-speed balance** |
| **RTX 4000 Ada (20GB)** | `svdq-fp4_r32-lightningv2.0-8steps` | Ada optimized, **ultra-fast/light** |
| **RTX 4090 (24GB)** | `Qwen-Image-Edit-2509_bf16` | **24GB VRAM + Full BF16** = **highest quality** |

---

## 📝 Conclusion

-   **RTX A4500**: `svdq-int4_r128 Lightning` → **Balanced quality/speed**
-   **RTX 4000 Ada**: `svdq-fp4_r32 Lightning` → **Ultra-fast/light, Ada optimized**
-   **RTX 4090**: `BF16 Full` → **Highest quality**

---

<sub>*📄 Date: 2025-10-21* <br> *Sources: Hugging Face, NVIDIA Official Specs, Nunchaku-Tech Qwen Image Edit Model Repository*</sub>
