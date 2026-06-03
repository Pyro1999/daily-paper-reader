---
title: "BaRISTA: Brain Scale Informed Spatiotemporal Representation of Human Intracranial Neural Activity"
title_zh: BaRISTA：脑尺度信息引导的人脑颅内神经活动时空表示
authors: "Lucine L Oganesian, Saba Hashemi, Maryam M. Shanechi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=LDjBDk3Czb"
tags: ["query:pbci-load"]
score: 4.0
evidence: 颅内记录的基础模型，与脑电基础模型相关
tldr: 颅内脑电记录呈现复杂时空交互，现有基础模型泛化不足。本文提出BaRISTA，一种基于Transformer的神经基础模型，通过多尺度空间编码和自监督学习捕捉脑网络模式。实验表明其在下游解码任务中表现优异。虽非头皮EEG，但其方法论对EEG基础模型构建具有启发意义。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1433, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1429, \"height\": 564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 816, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1347, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1316, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1318, \"height\": 717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1284, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1311, \"height\": 631, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1196, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1358, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1243, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1270, \"height\": 1289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1357, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1344, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1420, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1074, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1355, \"height\": 356, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1333, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1332, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1446, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1204, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1277, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1109, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1371, \"height\": 608, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1438, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 937, \"height\": 467, \"label\": \"Table\"}]"
motivation: 颅内记录存在复杂时空交互，现有方法难以有效编码空间信息和学习脑网络模式。
method: 设计Transformer架构，融合多尺度空间编码和自监督任务。
result: 在多个颅内数据集上提升了跨主体和解码性能。
conclusion: 所提方法有效利用了颅内信号的时空结构。
---

## Abstract
Intracranial recordings have opened a unique opportunity to simultaneously measure activity across multiregional networks in the human brain. Recent works have focused on developing transformer-based neurofoundation models of such recordings that can generalize across subjects and datasets. However, these recordings exhibit highly complex spatiotemporal interactions across diverse spatial scales, from the single-channel scale to the scale of brain regions. As such, there remain critical open questions regarding how best to encode spatial information and how to design self-supervision tasks that enable the learning of brain network patterns and enhance downstream decoding performance using such high-dimensional, multiregional recordings. To allow for exploring these questions, we propose a new spatiotemporal transformer model of multiregional neural activity and a corresponding self-supervised masked latent reconstruction task, designed to enable flexibility in the spatial scale used for token encoding and masking. Applying this model on publicly available multiregional intracranial electrophysiology (iEEG) data, we demonstrate that adjusting the spatial scale for both token encoding and masked reconstruction significantly impacts downstream decoding. Further, we find that spatial encoding at larger scales than channel-level encoding, which is commonly used in existing iEEG transformer models, improves downstream decoding performance. Finally, we demonstrate that our method allows for region-level token encoding while also maintaining accurate channel-level neural reconstruction. Taken together, our modeling framework enables exploration of the spatial scales used for token encoding and masking, reveals their importance towards self-supervised pretraining of neurofoundation models of multiregional human brain activity, and enhances downstream decoding performance.

---

## 论文详细总结（自动生成）

# 论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：颅内脑电图（iEEG）能够同时记录人类大脑多个区域的神经活动，具有复杂的跨空间尺度（从单通道到脑区网络）的时空交互。现有基于Transformer的神经基础模型大多采用通道级空间编码和随机掩码策略，未能充分利用脑区层次的空间信息，导致跨被试、跨数据集的泛化能力受限。
- **整体含义**：本文旨在探索如何更好地编码空间信息以及如何设计自监督预训练任务，从而学习脑网络模式并提升下游解码性能。作者提出一个灵活的框架BaRISTA，允许独立调整令牌编码和掩码的空间尺度，以揭示空间尺度对自监督预训练的影响，并最终提升多区域iEEG数据的解码表现。

## 2. 方法论

### 核心思想
- 提出一个**时空Transformer模型**，将神经信号按通道分片后通过共享的时间编码器（扩张卷积CNN）生成令牌，然后加入**可学习空间编码**（依据不同空间尺度：通道坐标、脑图谱分块、脑叶），并将所有令牌按（时间×通道）交错排列输入单一编码器Transformer，实现空间和时间的联合关注。
- 设计**自监督掩码潜在重构任务**：根据空间元信息（如脑区或脑叶）选择候选掩码目标，而非随机掩码；使用在线编码器（原始令牌）和通过指数移动平均（EMA）更新的目标编码器，将掩码令牌替换为共享的可学习掩码令牌，然后通过预测器网络（MLP）重构目标令牌；损失为掩码令牌预测与目标令牌之间的均方误差。

### 关键技术细节
- **令牌化**：每个通道的每个时间片段（长度L=512，对应250ms）通过共享的扩张卷积CNN（5层，隐藏维5，核宽3，膨胀因子2^i）和线性投影得到维度d=64的令牌。
- **空间编码**：根据所选空间尺度（通道LPI坐标、Destrieux图谱脑区、脑叶），使用可学习嵌入表；多维空间则对各维度嵌入求和。
- **掩码策略**：随机选择一定比例的空间类别（如某些脑区）的所有通道的所有时间片作为目标令牌，其余为观测令牌；掩码令牌替换为可学习掩码令牌，但保留其空间编码。
- **训练**：同时优化令牌器和编码器Transformer，目标编码器通过EMA更新；训练损失为掩码令牌的MSE重构损失。
- **下游任务**：使用预训练模型（EMA目标令牌器+编码器）进行微调；分类任务在平均嵌入上训练线性分类器；重构任务增加线性层将预测令牌映射回原始时间序列。

## 3. 实验设计

### 数据集
- **Brain Treebank**：10名癫痫患者的26个会话的iEEG数据（2048Hz采样），记录期间观看好莱坞电影，提供对齐的转录。总共29.2小时用于预训练（17个会话），2个会话作为验证，7个会话作为测试。下游任务使用3秒无重叠片段（主要评估）和有重叠但按时间顺序切分的片段（第二次评估）。

### Benchmark与对比方法
- **baseline**：PopT（Population Transformer）和Brant，以及随机初始化的BaRISTA。
- **下游任务**（主要）：句子起始检测和语音/非语音分类（ROC-AUC指标）。额外任务（第二次评估）：音量高低分类、全局光流大小分类。

### 对比设置
- 固定掩码比例为30%，预训练70个epoch。
- 在不同空间编码/掩码组合（3×3=9种）下分别预训练模型，评估在下游任务上的微调性能。

### 资源与算力
- 文中明确提及：BaRISTA模型参数约**1M**（比PopT 20M、Brant 500M小得多）。
- 预训练使用**4×NVIDIA RTX 6000 Ada或4×NVIDIA RTX A6000 GPU**，约**<4小时**（70个epoch，约19500步）。PopT预训练约22小时（4×A6000），Brant约2.8天（4×A100）。

## 4. 实验数量与充分性

- **主实验**：在9种空间编码/掩码组合下分别预训练模型（每种组合至少1个预训练种子），并在7个测试会话上进行微调（每个会话5个随机种子），报告平均AUC和标准误。共收集35个（7会话×5种子）数据点。
- **额外实验**：
  - 跨被试泛化实验：逐次将测试被试的数据完全排除在预训练外，进行微调。
  - 数据规模缩放实验：使用5%、10%、25%、50%、75%预训练数据，观察下游性能变化。
  - 通道重构任务：评估不同组合下的重构MSE和R²。
  - 消融实验：比较不同时间编码器（线性投影、单层CNN vs. 扩张CNN）以及混合注意力与分离注意力模块。
  - 第二次评估（时间顺序切分）重复了上述主要实验，结果一致。
  - 可解释性分析：使用投影权重显示高权重的脑区与语言相关区域一致。
- **充分性**：实验覆盖了空间尺度、预训练数据量、跨被试泛化、重构能力、架构选择等多个维度，统计显著性检验（Wilcoxon signed-rank、双因素ANOVA）支撑结论。对比基线（PopT、Brant）经过复现验证。实验设计较为充分、公平。

## 5. 主要结论与发现

1. **空间尺度至关重要**：相比通道级编码，使用更大的空间尺度（如脑图谱分区或脑叶）进行令牌编码能显著提升下游分类性能（AUC提高约0.08~0.10，p<1e-5）。
2. **空间编码比空间掩码影响更大**：双因素ANOVA显示，空间编码对下游性能的影响更显著，而空间掩码的作用较小且仅在通道级编码时有明显差异。
3. **大尺度编码仍能保持通道级重构能力**：在重构任务中，脑区级编码的模型在通道级重构上的MSE和R²与通道级编码相当，说明并不损失精细信息。
4. **跨被试泛化与数据缩放**：即使将目标被试完全排除在预训练外，性能仍高于基线；随着预训练数据量增加，下游性能持续提升。

## 6. 优点

- **灵活的空间尺度设计**：首次系统地分离并探究了空间编码和掩码尺度对自监督预训练的影响，提供了可调节的框架。
- **端到端潜在空间重构**：联合训练令牌器和编码器，使用EMA目标网络和掩码重构，无需监督信号，提升了表示质量。
- **计算效率高**：仅1M参数，预训练仅需<4小时，远小于基线模型（PopT 20M/22小时，Brant 500M/2.8天），同时达到更优性能。
- **全面的实验验证**：多个下游任务、多种空间尺度组合、跨被试、数据缩放、消融、重构验证，结果一致且统计显著。

## 7. 不足与局限

- **空间定义依赖解剖学**：当前仅使用了基于解剖学的空间类别（通道坐标、Destrieux图谱、脑叶），未探索基于功能连接或其他数据驱动的空间划分，可能限制了最优性能。
- **掩码策略仅限空间**：未引入时间维度的掩码，未来可结合时空掩码以学习更丰富的表示。
- **重构任务中高频成分恢复较差**：频谱分析显示高频（40-150Hz）重构误差显著高于低频，可能限制了在需要对高频特征敏感的任务上的表现。
- **数据集单一**：仅使用Brain Treebank（自然语言刺激），未在其他iEEG数据集（如静息态、运动任务等）上验证，泛化性有待进一步考察。
- **计算资源报告**：虽然提供了硬件和训练时间，但未详细说明完整项目总计算量（包括消融实验等）。
- **基线比较的公平性**：本文模型参数量远小于基线，但性能更高，这本身是优点；但未深入分析原因（如架构、训练技巧的差异），可能存在其他因素影响。

## 8. 总结

BaRISTA通过引入多尺度空间编码和相应的掩码重构自监督任务，显著提升了颅内神经活动基础模型的跨被试泛化能力和下游解码性能。其关键贡献在于揭示了空间尺度选择的重要性，并为未来神经基础模型的空间信息处理提供了新思路。

（完）
