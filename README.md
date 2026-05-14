# 🎬 Sentiment Analysis with DistilBERT

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Framework-orange.svg)]()
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-Transformers-yellow.svg)]()

## 📌 项目概述 (Project Overview)
本项目旨在利用深度学习与迁移学习范式，构建一个高效的情感分析系统。我们以 **DistilBERT** 作为基座模型，在 IMDB 电影评论数据集上进行微调（Fine-tuning），实现对自然语言文本情感极性（正面/负面）的自动识别。

本项目的核心不仅在于实现 93% 的高准确率，更在于深入的**错误分析 (Error Analysis)**，通过定量分析（混淆矩阵）与定性分析（错误案例剖析），探索了预训练模型在实际应用中的局限性与潜在的数据质量问题。

## 🚀 核心功能 (Key Features)
*   **迁移学习实现**：基于 Hugging Face 生态，将轻量级预训练模型 DistilBERT 应用于下游二分类任务。
*   **端到端流程**：涵盖数据探索 (EDA)、文本分词、模型微调、性能评估及 Web 可视化演示。
*   **批判性评估**：不仅仅关注 Accuracy，还通过混淆矩阵和人工案例剖析，揭示了模型对“反讽”理解的局限及数据集中的“标签噪音”。
*   **交互式 UI**：基于 Gradio 构建实时推理 Web 界面，支持用户输入文本进行即时情感检测。

## 📊 实验结果 (Performance)
模型在 IMDB 测试集（25,000 条数据）上的最终表现如下：

| Metric | Score |
| :--- | :--- |
| **Accuracy** | **93.03%** |
| **F1-Score** | **0.9305** |

*注：模型经过 2 轮微调（Fine-tuning）达到收敛，表现优异。*

## 🛠️ 技术栈 (Tech Stack)
*   **Language**: Python
*   **Framework**: PyTorch, Hugging Face Transformers, Datasets
*   **Web UI**: Gradio
*   **Analysis**: Pandas, Matplotlib, Seaborn, Scikit-learn
*   **Platform**: Google Colab (GPU Acceleration)

## 📂 项目结构 (Project Structure)
```text
.
├── notebooks/
│   ├── 01_Data_Exploration.ipynb    # 数据加载与 EDA
│   ├── 02_Fine_tuning.ipynb         # 模型训练与微调
│   └── 03_Evaluation_and_UI.ipynb   # 评估、分析与 Gradio 部署
├── results/                         # 训练日志与模型 Checkpoints
├── images/                          # 混淆矩阵、Loss 曲线等图表
├── app.py                           # 最终演示的 Web 应用代码
└── README.md                        # 项目说明
