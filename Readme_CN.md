# StarCFA-Net：面向严重程度感知的轻量级道路损坏检测

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)

> **StarCFA-Net** 是一种新颖、轻量级且支持严重程度感知的实时道路损坏检测框架，专为边缘设备的高效部署而设计。配合新引入的 **MLHR-RDD** 数据集，它能够对损坏类型和严重程度进行细粒度分类，填补了现有道路检测系统中的关键空白。

![English](./Readme.md)

## 📌 概述

道路损坏检测对于基础设施维护、成本降低和交通安全至关重要。然而，当前大多数方法仅对损坏"类型"进行分类，忽略了其"严重程度"，这限制了其在实际维护规划中的实用性。

为解决这一问题，我们提出：
- **StarCFA-Net**：基于 YOLOv8 的轻量级检测器，具有以下特点：
  - **StarNet 骨干网络**：减少冗余并增强特征提取能力。
  - **跨阶段特征聚合（CFA）模块**：对齐多尺度特征。
  - **高效通道注意力（ECA）**：优化通道级特征加权。
- **MLHR-RDD 数据集**：高分辨率俯视道路损坏数据集，包含：
  - **6,689 张图像**
  - **8,890 个标注实例**
  - **9 种损坏类别**，每种类别均标注**严重程度等级**（如轻微、中等、严重）。

实验表明，StarCFA-Net 达到了最先进的精度，同时与代表性模型相比，参数和计算量（FLOPs）减少了 **30–50%**，非常适合实时边缘部署。

---

## 🚀 特点

- ✅ 联合预测**损坏类型 + 严重程度等级**
- ✅ 实时推理速度（中端 GPU 上 >30 FPS）
- ✅ 轻量级架构（<300 万参数）
- ✅ 兼容 YOLOv8 生态系统（训练、导出、推理）
- ✅ 公开发布**MLHR-RDD**数据集（链接见下文）

---

## 📥 数据集：MLHR-RDD
MLHR-RDD 数据集将在论文接受后公开发布。

📊 包含：
- 高分辨率（≥2048×2048）俯视道路图像
- COCO 格式 JSON 标注，包含 `category_id`（类别 ID）和 `severity`（严重程度）字段

---

## 📄 引用
如果您在研究中使用了 StarCFA-Net 或 MLHR-RDD 数据集，请引用我们的工作：
