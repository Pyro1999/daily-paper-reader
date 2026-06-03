---
title: "REVE: A Foundation Model for EEG - Adapting to Any Setup with Large-Scale Pretraining on 25,000 Subjects"
title_zh: REVE：面向脑电图的基础模型——通过大规模预训练2.5万受试者适应任意设置
authors: "Yassine El Ouahidi, Jonathan Lys, Philipp Thölke, Nicolas Farrugia, Bastien Pasdeloup, Vincent Gripon, Karim Jerbi, Giulia Lioi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ZeFMtRBy4Z"
tags: ["query:pbci-load"]
score: 9.0
evidence: 基于2.5万人的EEG基础模型，可直接用于认知负荷估计
tldr: 现有EEG基础模型因数据集异构难以泛化。本文提出REVE，通过4D位置编码和大规模预训练（2.5万受试者）学习通用EEG表示。实验表明REVE在多个下游任务中线性探测表现优异，可有效迁移至认知负荷估计等场景，为被动BCI提供强大的基础模型。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-zefmtrby4z/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 539, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1419, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 916, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1198, \"height\": 554, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 979, \"height\": 895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 905, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 891, \"height\": 751, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1259, \"height\": 576, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1154, \"height\": 534, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1156, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1453, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1156, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1152, \"height\": 630, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1147, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1157, \"height\": 607, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1157, \"height\": 606, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1276, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 908, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1329, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1399, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 774, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1457, \"height\": 191, \"label\": \"Table\"}]"
motivation: EEG数据集异构性强，现有基础模型泛化能力不足。
method: 提出4D位置编码，在大规模多设置EEG数据上预训练通用表示。
result: 在多种下游任务中线性探测性能大幅超越现有模型。
conclusion: REVE可作为EEG分析的基础骨干，支持认知负荷等应用。
---

## Abstract
Foundation models have transformed AI by reducing reliance on task-specific data through large-scale pretraining. While successful in language and vision, their adoption in EEG has lagged due to the heterogeneity of public datasets, which are collected under varying protocols, devices, and electrode configurations. Existing EEG foundation models struggle to generalize across these variations, often restricting pretraining to a single setup, resulting in suboptimal performance, in particular under linear probing.
We present REVE (Representation for EEG with Versatile Embeddings), a pretrained model explicitly designed to generalize across diverse EEG signals. REVE introduces a novel 4D positional encoding scheme that enables it to process signals of arbitrary length and electrode arrangement. Using a masked autoencoding objective, we pretrain REVE on over 60,000 hours of EEG data from 92 datasets spanning 25,000 subjects, representing the largest EEG pretraining effort to date.
REVE achieves state-of-the-art results on 10 downstream EEG tasks, including motor imagery classification, seizure detection, sleep staging, cognitive load estimation, and emotion recognition. With little to no fine-tuning, it demonstrates strong generalization, and nuanced spatio-temporal modeling. We release code, pretrained weights, and tutorials to support standardized EEG research and accelerate progress in clinical neuroscience.

---

## 论文详细总结（自动生成）

# REVE: 面向脑电图的基础模型——通过大规模预训练2.5万受试者适应任意设置 —— 中文总结

## 1. 核心问题与研究动机
- **背景**：脑电图（EEG）数据在不同协议、设备和电极配置下高度异构，导致现有深度学习模型难以跨设置泛化。尽管基础模型在语言和视觉领域取得巨大成功，但在EEG领域的应用滞后。
- **核心问题**：现有EEG基础模型（如BIOT、LaBraM、CBraMod）大多仅在单一固定电极配置（如TUH数据库的19或21通道）上预训练，无法灵活处理不同电极布局和信号时长，尤其在**线性探测（linear probing）** 场景下表现不佳。
- **整体目标**：构建一个能**任意适应不同EEG配置**的基础模型，通过大规模、多样化预训练学习通用表示，实现跨任务、跨设置的有效迁移。

## 2. 方法论：REVE 模型
### 2.1 核心思想
- 设计一种**4D位置编码**方案，将电极的三维空间坐标与时间补丁索引结合，使模型能处理任意长度和电极排列的信号。
- 采用**掩码自编码器（MAE）** 框架进行自监督预训练，并引入**时空块掩码策略**和**辅助全局表征损失**，促进模型学习鲁棒且通用的特征。
- 在**最大规模、最多样化的EEG数据集**（92个数据集、超过25,000名受试者、60,000多小时数据）上预训练。

### 2.2 关键技术细节
- **EEG表示与分块**：将多通道EEG `X ∈ R^(C×T)` 按通道切分为重叠的补丁（窗口大小1s，重叠0.1s），每个补丁线性嵌入。
- **4D位置编码**：
  - 输入：电极3D坐标 `P ∈ R^(C×3)`（加高斯噪声增强泛化），扩充时间维度得到 `P_ext ∈ R^(C×p×4)`。
  - 采用扩展的**傅里叶位置编码**（4D），每个维度用 `n_freq` 个频率，通过笛卡尔积生成多频特征 `F_pe`。
  - 同时学习一个**线性变换+ GELU + LayerNorm**的可学习表示 `F_lin`。
  - 最终位置编码 = `LayerNorm(F_pe + F_lin)`，结合固定傅里叶偏置与可学习适应。
- **掩码策略**：
  - **时空块掩码**：以比率 `Mr=55%`、空间半径 `Rs=3cm`、时间半径 `Rt=3s`、丢弃率 `Dr=10%` 等参数，掩盖连续时空区域，使重建任务更具挑战性。
- **Transformer架构**：
  - 编码器：使用RMSNorm、GEGLU激活函数、去除偏置项、Flash Attention v2。
  - 解码器：轻量级，共享位置编码，用于重建被掩盖的原始EEG信号。
  - 损失函数：L1损失（对噪声鲁棒）用于主重建任务；辅助任务通过注意力池化所有编码器层的输出，生成全局表征并重建掩码补丁，损失权重 λ=0.1。
- **预训练目标**：总损失 = 主重建损失 + λ · 辅助重建损失。

## 3. 实验设计
### 3.1 数据集与基准
- **预训练数据集**：来自92个公开或可申请的数据集（包括OpenNeuro、MOABB、TUH等），总计19TB原始数据，涵盖24,274名受试者、61,415小时EEG记录。预处理后得到6TB数据（200Hz重采样、0.5-99.5Hz带通滤波、Z-score标准化）。
- **下游任务**：共计10个任务，涵盖不同领域：
  - 运动想象：PhysioNet-MI（4类）、BCIC-IV-2a（4类）
  - 事件类型分类：TUEV（6类）
  - 异常检测：TUAB（2类）
  - 睡眠分期：HMC（5类）、ISRUC（5类，修正了电极选择bug）
  - 情绪识别：FACED（9类）
  - 精神障碍诊断：Mumtaz（2类）
  - 心理应激检测：MAT（2类）
  - 想象语音：BCIC2020-3（5类）
- **对比方法**：
  - 非基础模型：EEGNet、EEGConformer、SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer。
  - 基础模型：BIOT、LaBraM-Base、CBraMod。
- **评估指标**：主要报告**平衡准确率（Balanced Accuracy）** 及其标准差；部分任务还报告Cohen's Kappa、Weighted F1、AUC-PR、AUROC。

### 3.2 实验设置
- 采用与其他基础模型**一致的训练/验证/测试划分**，确保公平对比。
- 微调策略：先训练线性探测头（冻结编码器），然后整体微调（可选LoRA），并使用模型汤（model soup）平均多次运行权重以提升稳定性。
- 报告了3种模型大小（Small、Base、Large）的配置。

## 4. 资源与算力
- **硬件**：NVIDIA A100 GPU（Intel Cascade Lake CPU，192GB RAM），共享全闪存并行文件系统，Slurm调度。
- **训练时间**：对于REVE-Base模型，估计需要**260 A100 GPU小时**（依据PaLM FLOPs公式计算，考虑60k小时EEG、68平均通道、17个epoch、72M参数、312 TFLOPs峰值吞吐量、50%利用效率）。
- **存储**：预处理后数据集约6TB。

## 5. 实验数量与充分性
- **主实验**：在10个下游任务上报告了平衡准确率（表2），每个任务至少5次运行取均值±标准差。
- **消融实验**：
  - 分析**辅助损失**的影响（表17）：在8个任务上对比有无辅助损失，显示在冻结和微调设置下均提升。
  - 分析**掩码比例与策略**（表18）：块掩码优于随机掩码，最优比率为55%。
  - 分析**位置编码组件**（表19）：在PhysioNetMI和MAT上对比了可学习PE、MLP 4D、无位置噪声、无丢弃块掩码、无时间块掩码等。
  - 分析**激活/归一化**（表20）：GEGLU+RMSNorm优于GELU+RMSNorm和GEGLU+LayerNorm。
- **泛化性实验**：稀疏电极配置（表21）和**少样本学习**（表22）证明了REVE在有限数据下的鲁棒性。
- **公平性**：遵循与基线相同的预处理器和评估协议；修正了ISRUC数据集中包含非EEG电极的bug；线性探测对比中（表4）特别复现了CBraMod官方代码以避免偏差。
- **充分性评价**：实验覆盖广泛（临床、BCI、认知），消融充分，全面对比了主流模型，结论可信。

## 6. 主要结论与发现
1. **SOTA性能**：REVE-Base在10个下游任务上平均平衡准确率为**0.715**，比最佳基线CBraMod（0.690）高**+2.5%**，在BCIC-IV-2a（+12.6%绝对提升）和MAT（+4.0%）等任务上优势显著。
2. **线性探测优势**：在冻结编码器的线性探测设置下，REVE-Base平均比CBraMod高**~10%**，REVE-Large高**~17%**，证明其嵌入质量高、通用性强。
3. **跨配置泛化**：能够处理未见过的双极导联（TUEV）以及比预训练更长的输入（30秒睡眠分期），得益于4D位置编码。
4. **模型扩展性**：随着模型增大（Small→Base→Large），线性探测性能持续提升，表明更多参数可压缩更丰富的表征。
5. **预训练贡献显著**：REVE从预训练中获益巨大（+11%），而CBraMod仅+2%，表明REVE更依赖学习到的通用知识。

## 7. 方法亮点
- **4D位置编码**：首次将电极3D坐标与时间位置联合编码，支持任意电极布局和序列长度，突破了传统固定表格嵌入的局限。
- **大规模异构预训练**：汇聚92个数据集/25k受试者/61k小时，覆盖临床、BCI、认知，是目前最大的EEG预训练语料。
- **辅助全局损失**：通过注意力池化跨层表征，强制模型压缩信息，显著提升冻结嵌入质量，这是MAE框架的创新改进。
- **时空块掩码**：相比随机掩码，块掩码更符合EEG的时空连续性，迫使模型学习更鲁棒的表征。
- **实际可用性**：释放预训练权重、代码、教程，并支持以3D坐标提供任意电极配置，便于社区应用。

## 8. 不足与局限
- **输入约束**：要求信号长度至少为1秒且为1秒的整数倍，无法处理极短片段。
- **数据质量控制**：当前未对预训练数据进行筛选（如剔除低质量记录、平衡分布），可能引入噪声或偏差。
- **人口多样性有限**：大部分数据来自北美和欧洲，缺乏全球代表性，可能影响跨人群泛化。
- **自监督方法简单**：仅采用MAE和标准Transformer，未来可探索更先进的SSL策略（如对比学习）和架构（如状态空间模型）。
- **缺少零样本/少样本标准评估**：虽然做了初步少样本实验，但未系统评估零样本场景。
- **未提供精确的缩放定律**：观察到规模效应但未数学建模。
- **隐私风险**：解码器可重建原始EEG，作者选择不发布解码器以降低风险，但使用编码器仍可能通过线性探测泄露敏感信息。

（完）
