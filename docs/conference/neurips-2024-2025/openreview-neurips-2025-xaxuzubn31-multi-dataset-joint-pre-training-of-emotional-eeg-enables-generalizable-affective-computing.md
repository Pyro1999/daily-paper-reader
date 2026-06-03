---
title: Multi-dataset Joint Pre-training of Emotional EEG Enables Generalizable Affective Computing
title_zh: 多数据集联合预训练的情感脑电图实现可泛化的情感计算
authors: "Qingzhu Zhang, Jiani Zhong, Li ZongSheng, Xinke Shen, Quanying Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=xaxuzubN31"
tags: ["query:pbci-load"]
score: 6.0
evidence: 基于EEG的预训练框架，可迁移至认知负荷评估
tldr: 针对情绪识别中跨数据集泛化困难的问题，提出多数据集联合预训练框架，通过协方差对齐损失对齐二阶统计特性。实验证明该方法能鲁棒泛化，无需大量微调。该预训练策略可迁移至认知负荷评估等领域，为EEG任务特定预训练提供新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 689, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 1093, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1125, \"height\": 741, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1464, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1482, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1147, \"height\": 1829, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 948, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1459, \"height\": 1191, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 385, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1539, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1469, \"height\": 1459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1187, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 455, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1306, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1308, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 594, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1184, \"height\": 656, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1437, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1437, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1475, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1422, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 739, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1609, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 499, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 495, \"height\": 256, \"label\": \"Table\"}]"
motivation: 现有EEG预训练模型难以处理情绪识别等复杂任务，需要任务特定预训练。
method: 提出跨数据集协方差对齐损失，联合预训练多个情感EEG数据集。
result: 在多个情感数据集上实现了鲁棒的跨数据集泛化。
conclusion: 任务特定的多数据集预训练可有效提升EEG情感识别泛化能力。
---

## Abstract
Task-specific pre-training is essential when task representations diverge from generic pre-training features. Existing task-general pre-training EEG models struggle with complex tasks like emotion recognition due to mismatches between task-specific features and broad pre-training approaches. This work aims to develop a task-specific multi-dataset joint pre-training framework for cross-dataset emotion recognition, tackling problems of large inter-dataset distribution shifts, inconsistent emotion category definitions, and substantial inter-subject variability. We introduce a cross-dataset covariance alignment loss to align second-order statistical properties across datasets, enabling robust generalization without the need for extensive labels or per-subject calibration. To capture the long-term dependency and complex dynamics of EEG, we propose a hybrid encoder combining a Mamba-like linear attention channel encoder and a spatiotemporal dynamics model. Our method outperforms state-of-the-art large-scale EEG models by an average of 4.57% in AUROC for few-shot emotion recognition and 11.92% in accuracy for zero-shot generalization to a new dataset. Performance scales with the increase of datasets used in pre-training. Multi-dataset joint pre-training achieves a performance gain of 8.55\% over single-dataset training. This work provides a scalable framework for task-specific pre-training and highlights its benefit in generalizable affective computing. Our code is available at https://github.com/ncclab-sustech/mdJPT_nips2025.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

现有通用的EEG大规模预训练模型（如LaBraM、EEGPT）通常针对多任务（睡眠分期、异常检测等）进行预训练，但在情绪识别这类复杂、动态、跨数据集差异大的任务上表现不佳。主要原因是：  
- **任务表示不匹配**：通用预训练学习的特征与情绪相关的神经表征存在偏差。  
- **跨数据集分布偏移**：不同情感数据集在电极布局、采样率、情绪类别定义、被试间差异等方面存在显著差异。  
- **现有方法依赖一对一的域适应或逐被试微调**，难以泛化到未见数据集或新情绪类别。

本文提出**任务特定的多数据集联合预训练（mdJPT）**，专门针对情感识别任务，通过跨数据集协方差对齐（CDA）和跨被试对比对齐（ISA），实现鲁棒的跨数据集泛化，无需大量标注或被试校准。

### 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：  
利用多个情感EEG数据集联合预训练一个编码器，使其学习到数据集无关、被试无关但情绪相关的表征。预训练目标包含两个无监督损失：  
- **CDA损失**：对齐不同数据集/被试在隐空间中的协方差结构（二阶统计量），消除分布偏移。  
- **ISA损失**：基于时间对齐的对比学习，拉近同一情绪刺激下不同被试的表征，推远不同刺激的表征。

**模型架构**（混合编码器）：  
1. **MLLA通道编码器**（Mamba-like Linear Attention）：  
   - 将每个通道的EEG信号切分为重叠的滑动窗口补丁（patch）。  
   - 每个通道独立通过MLLA编码器（含输入门、线性注意力、遗忘门），捕获长期时序依赖。  
   - 输出维度为 \(C \times N_1 \times K_1\)。  
2. **时空动态模型**：  
   - 线性空间投影 \(W_s\) 将多通道嵌入映射到隐空间用于协方差对齐。  
   - 空间迁移卷积（不同扩张率）捕获多尺度空间变化模式。  
   - 局部注意力机制动态加权时空表征。  
3. **投影器**（用于ISA损失）：两个时序卷积层，将编码器输出映射到对比空间。

**关键公式**（文字描述）：  
- CDA损失：对每个维度 \(d\) 计算被试协方差矩阵 \(\Sigma_{s,v}^{(d)}\)，然后求被试中心 \(\Gamma_s^{(d)}\)，再计算所有被试中心两两间的Frobenius距离之和 \(L_d\)，最终取对数得到 \(L_{CDA} = \log(\sum_d L_d + 1)\)。  
- ISA损失：基于NT-Xent损失，正样本对来自同一刺激且时间对齐的两个被试的片段，负样本为其他所有片段。总损失 \(L = L_{ISA} + \lambda L_{CDA}\)。

### 3. 实验设计

**数据集**：  
- SEED、SEED-IV、SEED-V、SEED-VII（62通道，1000Hz，3/4/5/7类）  
- FACED（32通道，250/1000Hz，9类，使用前20名被试）  
- DEAP（32通道，512Hz，二分类：效价/唤醒/优势）  
- EmoEEG-MC（额外泛化测试，想象诱发情绪）

**评估场景**：  
1. **跨数据集被试独立（少样本）分类**：留一数据集法，用目标数据集1/4的被试微调MLP分类器，剩余3/4测试，报告5次随机划分的均值±标准差。  
2. **零样本泛化**：预训练后直接对未见数据集进行最近邻分类（余弦相似度）。  
3. **数据集数量扩展实验**：以SEED-V为目标，逐步增加预训练数据集数量。  
4. **消融实验**：CDA权重、ISA损失、MLLA vs Transformer、时空动态模型 vs Transformer。  
5. **额外**：从DEAP到其他数据集的迁移、二分/四分类任务、随机种子稳定性。

**对比方法**：  
- DE基线（差分熵特征）  
- MMM、LaBraM、EEGPT（使用公开预训练权重）

### 4. 资源与算力

论文在第3.2节提到：“All experiments are implemented in Python 3.12.3 using the PyTorch 2.3.1 framework and are executed on an NVIDIA GeForce RTX 3090 GPU.”  
**但未明确说明GPU数量、训练时长、总计算量等细节**。仅提及使用了一块RTX 3090，未提供具体时长或迭代时间。

### 5. 实验数量与充分性

- **主要实验**：在6个数据集上进行了少样本和零样本评估，覆盖不同类别数、电极数、采样率。  
- **数据集扩展实验**：验证了随着预训练数据集增多性能持续提升（从单数据集到5个数据集，相对提升15.14%）。  
- **消融实验**：CDA权重扫描、ISA损失移除、MLLA vs Transformer、时空动态模型 vs Transformer、对比学习框架对比（监督CL vs ISA）、时间对齐策略对比。  
- **额外分析**：t-SNE可视化、轮廓分数、混淆矩阵、特征重要性跨数据集一致性（Pearson相关）、模型参数量比较。  
- **随机种子稳定性**：5次重复实验，标准偏差<0.85%。  
- **泛化至想象情境**（EmoEEG-MC），但性能仍较低。

**充分性评价**：实验设计较为全面，涵盖了主要变体、消融、扩展和泛化分析，对比方法为当前主流EEG预训练模型，公平性较好（均使用相同预处理和微调流程）。但零样本实验仅使用最近邻，可能对表示空间要求较高；未与领域自适应方法（如对抗训练）对比；算力描述不够详细。

### 6. 论文的主要结论与发现

1. **任务特定多数据集预训练显著优于通用预训练**：在少样本设定下，AUROC平均提升4.57%；零样本设定下准确率平均提升11.92%。  
2. **CDA和ISA损失有效**：CDA对齐二阶统计量，ISA促进跨被试对比学习，两者结合提升泛化。  
3. **MLLA通道编码器优于标准Transformer**，时空动态模型优于Transformer层。  
4. **预训练数据集越多，性能越好**：5个数据集联合训练相比单数据集提升8.55%准确率。  
5. **模型高效**：仅1.0M参数，远小于LaBraM（5.8M）和EEGPT（4.7M）。  
6. **零样本能力突出**：在DEAP上零样本准确率73.3%，甚至超过微调后的模型（可能得益于避免过拟合）。  
7. **特征可视化显示跨数据集对齐和情绪区分能力增强**。

### 7. 优点

- **创新性**：首次提出针对情感EEG的任务特定多数据集联合预训练框架，引入协方差对齐这一无监督对齐方式，避免标注依赖。  
- **方法设计**：MLLA+时空动态模型结合，兼顾长期依赖和空间动态，参数效率高。  
- **实验全面**：覆盖多种分类设定、多数据集、零样本、消融、泛化、可解释性分析。  
- **性能优异**：在多个数据集上超越通用预训练模型，尤其在零样本设置下大幅领先。  
- **可扩展性**：框架可推广至其他脑机接口任务。

### 8. 不足与局限

- **9类细粒度情绪识别性能仍不佳**（FACED数据集准确率仅23.46%），存在残差分布偏移。  
- **主要基于视频诱发情绪**，对想象诱发（EmoEEG-MC）的泛化效果有限（准确率20.56%）。  
- **未建模个体差异**（如主观情绪体验），未来可引入软对比学习调节。  
- **数据集人口多样性有限**（年龄、文化、健康状态）。  
- **缺乏与更多领域自适应方法的对比**（如对抗域适应）。  
- **算力资源描述不足**，仅提及单块RTX 3090，未报告训练时长。  
- **潜在伦理风险**（情感监控、隐私），论文虽提及但未给出具体缓解方案。

（完）
