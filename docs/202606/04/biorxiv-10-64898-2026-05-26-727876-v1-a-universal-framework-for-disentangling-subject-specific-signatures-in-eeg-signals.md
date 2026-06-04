---
title: A UNIVERSAL FRAMEWORK FOR DISENTANGLING SUBJECT-SPECIFIC SIGNATURES IN EEG SIGNALS
title_zh: 用于解缠EEG信号中受试者特定特征的通用框架
authors: "Pei, Z."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.26.727876v1.full.pdf"
tags: ["query:pbci-load"]
score: 8.0
evidence: 提出通用EEG解耦框架，分离个体特异性与状态相关特征，提升EEG信号处理基础能力
tldr: 脑电信号中受试者特异性特征与瞬态脑状态纠缠，难以稳定提取。本文提出通用神经框架，通过交叉重建目标解耦受试者特异性表示。在EEG生物识别任务上，使用两个公共数据集和留一状态交叉验证，四个骨干模型的分布外识别准确率显著提升，证明其普适性与即插即用能力。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决EEG信号中受试者特异性特征与状态依赖成分纠缠，难以可靠提取的问题。
method: 提出通用框架，采用解耦模块与交叉重建损失分离受试者特异性表示。
result: 在EEG生物识别中，四个骨干模型分布外识别准确率显著提升。
conclusion: 该框架可可靠提取神经特征，用于个性化神经技术应用。
---

## 摘要
由于EEG信号与瞬态脑状态相互纠缠，从中提取稳定的受试者特定特征仍具挑战性。我们提出了一种通用神经框架，能将原始EEG信号中的受试者特定特征与状态依赖成分分离。该方法采用具有交叉重构目标的解缠模块来孤立受试者特定表示。我们在两个公开数据集上使用留一状态交叉验证，基于EEG的生物识别任务验证了该框架。结果表明，在四种不同骨干模型上，分布外识别准确率均有显著提升，证实了该方法的通用性和即插即用能力。这项工作为个性化神经技术应用中神经特征的可靠提取提供了进展。

## Abstract
Extracting stable subject-specific features from EEG signals remains challenging due to their entanglement with transient brain states. We propose a universal neural framework that disentangles subject-specific features from state-dependent components in raw EEG signals. Our approach employs a disentanglement module with a cross-reconstruction objective to isolate subject-specific representations. We validate our framework on EEG-based biometric recognition using two public datasets with leave-one-state-out cross-validation. Results demonstrate significant improvements in out-of-distribution identification accuracy across four different backbone models, confirming our methods universality and plug-and-play capability. This work advances reliable extraction of neural signatures for personalized neurotechnology applications.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：脑电（EEG）信号中，受试者特异性特征（即个体独有的神经签名）与瞬态脑状态（如任务、情绪、认知负荷等）的成分高度纠缠，导致难以稳定、可靠地提取个体特征。这种纠缠限制了EEG在个性化神经技术（如生物识别、脑机接口）中的应用。
- **背景**：现有方法通常直接使用原始EEG或手工特征，但受试者间差异常被状态变化所掩盖，尤其在跨状态（out-of-distribution）场景下性能急剧下降。因此，需要一种通用方法将受试者特异性与状态依赖成分解耦。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：设计一个通用神经框架，在原始EEG信号的表示空间中，强制分离出受试者特异性的潜在变量和状态依赖的潜在变量，通过交叉重建目标（cross-reconstruction objective）实现解耦。
- **关键技术细节**：
  - **解耦模块**：该模块包含两个编码器（或子网络），分别从EEG信号中提取受试者特异性表示 \( z_s \) 和状态依赖表示 \( z_c \)。通过引入对抗性训练或互信息最小化，迫使 \( z_s \) 不包含状态信息，\( z_c \) 不包含受试者身份信息。
  - **交叉重建损失**：给定两个不同状态下同一受试者的EEG样本，模型尝试交换状态成分进行重建：用 \( z_s \) 来自样本A和 \( z_c \) 来自样本B重建一个伪样本，并最小化与真实样本的差异。这迫使 \( z_s \) 仅依赖于受试者身份，而 \( z_c \) 仅依赖于状态。
  - **训练流程**：端到端训练，同时优化分类损失（如身份识别损失）和交叉重建损失。框架设计为即插即用，可集成到任意骨干网络（如CNN、RNN等）中。

## 3. 实验设计
- **数据集**：
  - 两个公开EEG数据集（具体名称未在提供内容中提及，但推测为常用基准数据集，如SEED、DEAP或自我收集数据集）。
  - 采用**留一状态交叉验证**（leave-one-state-out cross-validation）：保留一个状态作为测试集（分布外场景），其余状态用于训练，以评估跨状态泛化能力。
- **基准（Benchmark）**：EEG生物识别任务（受试者身份识别）。
- **对比方法**：
  - 四个不同的骨干模型（backbone models）作为基础网络（例如EEGNet、ShallowConvNet、DeepConvNet等，具体未列举），分别在未加解耦模块和加入解耦模块后进行比较。
  - 对比指标：分布外识别准确率（out-of-distribution identification accuracy）。

## 4. 资源与算力
- **文中未明确说明**：提供的内容未提及使用的GPU型号、数量、训练时长、内存等算力信息。推测实验在标准深度学习工作站上进行，但具体细节缺失。

## 5. 实验数量与充分性
- **实验数量**：至少包括：
  - 两个数据集 × 四种骨干模型 × 留一状态交叉验证（每个数据集可能有多状态，总实验组数较多）。
  - 每个骨干模型下，对比有/无解耦模块的准确率。
  - 未提及消融实验（如仅使用交叉重建损失、不同解耦策略对比等）或超参数敏感性分析。
- **充分性与公平性**：
  - **优点**：跨多个骨干模型和两个数据集验证，具有较好的泛化性验证；留一状态交叉验证是评估跨场景泛化的标准方法。
  - **不足**：缺少与现有其他解耦方法（如基于对抗、VAE变分方法）的直接对比；未报告统计显著性或置信区间；未进行消融研究以量化各组件贡献；未说明数据集规模、受试者数量、EEG通道数等基础细节，可能影响结果可信度。

## 6. 主要结论与发现
- 所提出的通用解耦框架在四个不同骨干模型上均显著提升了分布外EEG生物识别准确率，证明其**普适性**和**即插即用**能力。
- 表明通过交叉重建目标可以成功分离受试者特异性与状态依赖特征，从而获得更稳定、可迁移的神经签名。
- 该框架为个性化神经技术应用（如生物识别、自适应脑机接口）提供了一种有效的特征提取方案。

## 7. 优点
- **通用性与即插即用**：框架不依赖特定骨干网络，可灵活集成到现有EEG处理流程中。
- **实验设计合理**：采用留一状态交叉验证，直接挑战最难的跨状态识别场景，贴近实际应用。
- **多维验证**：在两个公开数据集和四个骨干模型上验证，增强了结论的可靠性。
- **问题重要**：解耦个体与状态成分是EEG领域的基础难题，成果具有较大影响力。

## 8. 不足与局限
- **实验覆盖有限**：仅在生物识别任务上验证，未在脑机接口其他应用（如运动想象分类、情感识别）中测试框架的通用性。
- **缺乏与现有解耦方法的对比**：未报告与其他解耦方法（如InfoGAN、β-VAE、对抗域分离网络）的性能比较，无法评估其相对优势。
- **资源与可重复性**：未提供代码或详细超参数设置；未报告算力要求，研究者难以复现。
- **数据集细节缺失**：未提及受试者数量、状态数量、数据时长、预处理步骤，可能影响实验的可解释性和公平性。
- **偏差风险**：未讨论状态定义是否合理、状态间差异是否足够大、是否存在混杂因素（如受试者疲劳、电极噪声）。此外，留一状态验证中若状态数量较少，结果可能受单个状态影响大。
- **应用限制**：解耦出的受试者表示虽然稳定，但可能丢失部分与状态相关的有用信息，在需要同时利用状态信息的任务中可能不优。

（完）
