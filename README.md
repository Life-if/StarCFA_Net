# StarCFA-Net: Severity-Aware Lightweight Road Damage Detection

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)


> **StarCFA-Net** is a novel, lightweight, and severity-aware framework for real-time road damage detection, designed for efficient deployment on edge devices. Accompanied by the newly introduced **MLHR-RDD** dataset, it enables fine-grained classification of both damage types *and* severity levels—addressing a critical gap in existing road inspection systems.

![中文版本](https://pytorch.org/)

## 📌 Overview

Road damage detection is essential for infrastructure maintenance, cost reduction, and transportation safety. However, most current methods only classify damage *types*, ignoring their *severity*—limiting practical utility in real-world maintenance planning.

To bridge this gap, we propose:
- **StarCFA-Net**: A lightweight YOLOv8-based detector featuring:
  - **StarNet backbone** for reduced redundancy and enhanced feature extraction.
  - **Cross-stage Feature Aggregation (CFA)** module to align multi-scale features.
  - **Efficient Channel Attention (ECA)** to optimize channel-wise feature weighting.
- **MLHR-RDD Dataset**: A high-resolution top-down road damage dataset containing:
  - **6,689 images**
  - **8,890 annotated instances**
  - **9 damage categories**, each labeled with **severity levels** (e.g., minor, moderate, severe).

Experiments show that StarCFA-Net achieves state-of-the-art accuracy while reducing parameters and FLOPs by **30–50%** compared to representative models—making it ideal for real-time edge deployment.

---

## 🚀 Features

- ✅ Joint prediction of **damage type + severity level**
- ✅ Real-time inference speed (>30 FPS on mid-tier GPUs)
- ✅ Lightweight architecture (<3M parameters)
- ✅ Compatible with YOLOv8 ecosystem (training, export, inference)
- ✅ Public release of **MLHR-RDD** dataset (link below)

---

## 📥 Dataset: MLHR-RDD
The MLHR-RDD dataset will be publicly released upon paper acceptance.

📊 Includes:
- High-resolution (≥2048×2048) top-down road images
- COCO-style JSON annotations with `category_id` and `severity` fields

---

## 📄 Citation
If you find StarCFA-Net or the MLHR-RDD dataset useful in your research, please cite our work:
```
@article{yourname2025starcfa,

  title={StarCFA-Net: Severity-Aware Lightweight Network for Real-Time Road Damage Detection},

  author={Your Name and Co-authors},

  journal={Under Review},

  year={2025}

}
```
