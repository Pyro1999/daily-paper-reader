---
title: "CSBrain: A Cross-scale Spatiotemporal Brain Foundation Model for EEG Decoding"
title_zh: "CSBrain: 用于脑电解码的跨尺度时空脑基础模型"
authors: "Yuchen Zhou, Jiamin Wu, Zichen Ren, Zhouheng Yao, Weiheng Lu, Kunyu Peng, Qihao Zheng, Chunfeng Song, Wanli Ouyang, Chao Gou"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=agcXjEHmyW"
tags: ["query:pbci-load"]
score: 10.0
evidence: 用于EEG解码的基础模型
tldr: 现有EEG基础模型忽略了神经活动的跨尺度时空结构，导致解码能力受限。CSBrain提出了跨尺度时空脑基础模型，通过显式建模不同尺度的时空模式，在多个EEG解码任务上取得了领先性能。该模型有望推动被动脑机接口中认知负荷等心理状态的精确评估。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1365, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1365, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1430, \"height\": 246, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1373, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1375, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1187, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1002, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1435, \"height\": 408, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1439, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1380, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 648, \"height\": 325, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1386, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1007, \"height\": 669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1017, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1435, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1435, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1404, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 882, \"height\": 887, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 882, \"height\": 887, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 1006, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 750, \"height\": 956, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 822, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1310, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1313, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1309, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1308, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1311, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1312, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1312, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1348, \"height\": 521, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1312, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1313, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1313, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1312, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1311, \"height\": 517, \"label\": \"Table\"}]"
motivation: 现有EEG基础模型采用尺度无关的密集建模，忽略了神经活动的跨尺度时空特性，限制了解码性能。
method: 提出跨尺度时空架构，分别捕获EEG信号中不同时间尺度和空间位置的模式，并通过注意力融合实现多尺度表征。
result: 在多个EEG解码基准数据集上，CSBrain超越了现有基础模型和专用方法，验证了跨尺度建模的有效性。
conclusion: CSBrain作为EEG基础模型，为被动脑机接口中的认知负荷评估等任务提供了强大的通用表征。
---

## Abstract
Understanding and decoding human brain activity from electroencephalography (EEG) signals is a fundamental problem in neuroscience and artificial intelligence, with applications ranging from cognition and emotion recognition to clinical diagnosis and brain–computer interfaces. While recent EEG foundation models have made progress in generalized brain decoding by leveraging unified architectures and large-scale pretraining, they inherit a scale-agnostic dense modeling paradigm from NLP and vision. This design overlooks an intrinsic property of neural activity—cross-scale spatiotemporal structure. Different EEG task patterns span a broad range of temporal and spatial scales, from brief neural activations to slow-varying rhythms, and from localized cortical activations to large-scale distributed interactions. Ignoring this diversity may lead to suboptimal representations and weakened generalization ability. To address these limitations, we propose CSBrain, a Cross-scale Spatiotemporal Brain foundation model for generalized EEG decoding. CSBrain introduces two key components: (i) Cross-scale Spatiotemporal Tokenization (CST), which aggregates multi-scale features within localized temporal windows and anatomical brain regions into compact scale-aware token representations; and (ii) Structured Sparse Attention (SSA), which models cross-window and cross-region dependencies for diverse decoding tasks, further enriching scale diversities while eliminating the spurious dependencies. CST and SSA are alternately stacked to progressively integrate cross-scale spatiotemporal dependencies. Extensive experiments across 11 representative EEG tasks and 16 datasets demonstrate that CSBrain consistently outperforms both task-specific models and strong foundation baselines. These results establish cross-scale modeling as a key inductive bias for generalized EEG decoding and highlight CSBrain as a robust backbone for future brain–AI research.

---

## 论文详细总结（自动生成）

# 论文详细总结：CSBrain: 跨尺度时空脑基础模型用于脑电解码

## 1. 核心问题与整体含义（研究动机与背景）
- **现有范式缺陷**：当前的EEG基础模型（如BIOT、LaBraM、CBraMod）大多直接移植自NLP和视觉领域的尺度无关密集建模范式（scale-agnostic dense modeling）。它们将EEG信号分割成固定尺度的token，然后对所有token施加全局稠密注意力。
- **本质矛盾**：神经活动具有固有的**跨尺度时空结构**——不同EEG解码任务在时间尺度（从短暂的神经爆发到缓慢变化的节律）和空间尺度（从局部皮层激活到大范围分布式交互）上差异巨大。忽略这种多样性导致表征次优、泛化能力弱。
- **本文目标**：提出CSBrain，一种显式建模跨尺度时空结构的脑基础模型，旨在实现通用的、可泛化的EEG解码。

## 2. 方法论：核心思想与技术细节
### 2.1 整体架构
- **输入**：原始EEG信号 \( \mathbf{E} \in \mathbb{R}^{C \times T} \)（C为电极数，T为时间点）。
- **预处理**：带通滤波（0.3–75 Hz）、陷波滤波（60 Hz）、重采样至200 Hz、归一化至±100 μV；然后切分成非重叠的段（segment），每段长度t；提取时域和频域特征融合，加位置编码得到初始表示 \( \mathbf{x}^{(0)} \in \mathbb{R}^{C \times n \times d} \)。
- **核心模块**：**Cross-scale Spatiotemporal Tokenization (CST)** 与 **Structured Sparse Attention (SSA)** 交替堆叠L层（L=12）。

### 2.2 Cross-scale Spatiotemporal Tokenization (CST)
- **目的**：在局部时间窗口和大脑解剖区域内聚合多尺度特征，生成紧凑的尺度感知token。
- **Temporal Tokenization**：对每个位置(i,j)，使用K个不同核大小的1D卷积（\( \{\text{Conv}_t^{(k)}\}_{k=1}^K \)）在局部窗口上提取多尺度时间模式，拼接并加残差投影。
- **Spatial Tokenization**：类似地，根据10-20系统将电极划分为脑区，在每个脑区内使用多尺度空间卷积聚合邻近电极信息，输出跨尺度token \( \tilde{\mathbf{x}}^{(l)}_{i,j} \)。
- **维度分配**：采用指数衰减方案（\( d_k \propto \frac{1}{2^k} \)），小核分配更高维度保留细粒度特征，大核分配低维度汇总粗略上下文。

### 2.3 Structured Sparse Attention (SSA)
- **目的**：在CST提供的结构化token基础上，高效捕捉跨窗口和跨区域的长期依赖，同时避免虚假依赖并降低计算量。
- **Inter-window Attention**：将token按时间窗口分组（每组对应同一相对位置），组内自注意力。
- **Inter-region Attention**：从每个脑区采样一个代表token（顺序采样），结合该脑区的平均特征构成区域描述子，组装成空间组，组内自注意力。
- **复杂度**：线性复杂度 \( O(N \cdot k) \)，其中 \( k \ll \sqrt{N} \)，远低于稠密注意力的 \( O(N^2) \)。

### 2.4 预训练策略
- **目标**：掩码自编码（Masked Autoencoding）
- **掩码策略**：以比例r=0.5随机掩码时间段，被掩码段用可学习向量代替。
- **重建损失**：均方误差（MSE）\( \mathcal{L}_{\text{rec}} = \|\hat{\mathbf{E}}_m - \mathbf{E}_m\|^2 \)。

## 3. 实验设计
### 3.1 数据集与评估场景
- **预训练数据**：Temple University Hospital EEG Corpus (TUEG)，约9000小时，110万+样本。
- **下游任务（11个任务，16个数据集）**：
  - 运动想象分类：BCIC-IV-2a、PhysioNet-MI、SHU-MI
  - 情绪识别：FACED、SEED-V
  - 癫痫检测：CHB-MIT、Siena
  - 睡眠分期：ISRUC、HMC
  - 想象语音分类：BCIC2020-3
  - 警觉估计：SEED-VIG（回归）
  - 精神压力检测：MentalArithmetic
  - 精神障碍诊断：Mumtaz2016
  - 事件类型分类：TUEV
  - 异常检测：TUAB
  - 慢波事件分类：TUSL

### 3.2 Benchmark与对比方法
- **任务特定模型（7个）**：EEGNet、EEGConformer (Conformer)、SPaRCNet、ContraWR、CNN-Transformer (C-Trans)、FFCL、ST-Transformer
- **基础模型（3个）**：BIOT、LaBraM、CBraMod
- **指标**：多分类用Balanced Accuracy (B-Acc)、Cohen's Kappa、Weighted F1；二分类加AUROC、AUC-PR；回归用Pearson相关系数、R²、RMSE。所有结果5次重复均值±标准差。

## 4. 资源与算力
- **硬件**：4块NVIDIA A100 GPU（预训练），CUDA 12.4
- **训练时长**：约101小时（40 epoch，batch size 128）
- **模型参数量**：约4.9M（12层，隐层200，注意力头8）
- **优化器**：AdamW，lr=5e-4，weight decay=5e-2，余弦退火调度
- **注**：下游微调算力未详细给出，但可在单GPU上较快完成。

## 5. 实验数量与充分性
- **总量**：覆盖11个任务、16个数据集、10个对比方法，在主表中报告平均性能。
- **消融实验**：
  - Tokenization尺度对比（单尺度 vs. 双尺度 vs. 三尺度 vs. 堆叠）
  - 注意力机制对比（稠密、Criss-cross、SSA）
  - 预训练有效性（w/ vs. w/o pretrain）
  - 缩放分析（数据量、模型容量）
  - 区域描述符设计消融（Token only, Mean only, Random, Ours）
- **可视化**：Grad-CAM地形图、t-SNE表示、注意力图、通道相似性
- **公平性**：严格遵循官方划分或随机种子划分，统一数据预处理流程，指标覆盖全面，多次重复报告标准差。实验设计客观、全面、充分。

## 6. 主要结论与发现
- **性能全面领先**：CSBrain在几乎所有16个数据集上取得最佳或次佳结果，宏平均B-Acc达0.7095，比CBraMod高3.35%，比LaBraM高3.98%，比BIOT高7.73%。
- **跨尺度建模是关键**：堆叠的多尺度tokenization和结构化稀疏注意力显著优于单尺度或仅一次跨尺度处理。
- **任务特异性激活模式**：Grad-CAM可视化表明，不同任务激活不同脑区和尺度（如运动想象激活对侧运动皮层，情绪识别激活额叶和枕叶），验证了跨尺度建模的必要性。
- **预训练有效**：在数据有限时（如BCIC-IV-2a）增益巨大，在大数据时也有提升。
- **缩放趋势**：增加预训练数据量和模型容量均可提升性能，符合神经缩放定律。

## 7. 优点
- **创新性强**：首次将跨尺度时空结构作为归纳偏置引入EEG基础模型，突破了现有尺度无关的密集建模范式。
- **设计精巧**：CST通过多尺度卷积在局部时空窗口生成紧凑token，SSA通过分组注意力实现线性复杂度，两者交替堆叠渐进融合多尺度依赖。
- **实验极为全面**：16个数据集覆盖主流BCI任务，对比了10个强基线，消融实验和可视化分析丰富。
- **可解释性**：通过Grad-CAM、t-SNE和注意力可视化展示了模型捕获的生理相关模式。
- **代码开源**：提供代码和模型权重，可复现。

## 8. 不足与局限
- **计算资源限制**：当前探索的模型和数据缩放规模有限，未达到视觉/语言模型级别的性能上限；最优预训练数据量仍是开放问题。
- **跨模态缺失**：仅使用EEG，未扩展至MEG、fMRI等其他神经成像模态。
- **噪声鲁棒性**：在处理极低信噪比的EEG时，结构化注意力是否能完全消除虚假依赖仍需进一步验证。
- **部分任务指标**：在CHB-MIT数据集上平衡准确率略低于CBraMod（0.7262 vs. 0.7398），但AUROC更高（0.8915 vs. 0.8892），说明指标选择对排名有影响。
- **数据集同质性**：预训练数据TUEG为临床长时记录，下游任务包含多种范式，但部分罕见病数据集（如TUSL仅245样本）统计稳定性有限。
- **未考虑在线/实时场景**：模型延迟和计算效率在实时BCI应用中需进一步优化。

（完）
