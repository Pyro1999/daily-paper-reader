---
title: "NeurIPT: Foundation Model for Neural Interfaces"
title_zh: NeurIPT：神经接口基础模型
authors: "Zitao Fang, CHENXUAN LI, Zhou Hongting, Shuyang Yu, Guodong DU, Ashwaq Qasem, Yang Lu, Jing Li, Junsong Zhang, Sim Kuan Goh"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=D4hcJPkJ3y"
tags: ["query:pbci-load"]
score: 9.0
evidence: 面向神经接口的EEG基础模型
tldr: 针对EEG数据跨主体、跨任务和跨电极配置的巨大差异，本文提出NeurIPT，一个基于预训练Transformer的神经接口基础模型。该模型通过捕捉EEG信号中同质和异质的时空特征，在多个解码任务上取得优异性能，显著提升了EEG基础模型的泛化能力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1452, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 674, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1457, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 508, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1459, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 956, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1337, \"height\": 2138, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1464, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1465, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1465, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1466, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1466, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1466, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1421, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1197, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1208, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1197, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1435, \"height\": 519, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 1519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1372, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1365, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1232, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1224, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 440, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 508, \"height\": 137, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1081, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1229, \"height\": 672, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1011, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 845, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1027, \"height\": 1187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 526, \"height\": 471, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 722, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 659, \"height\": 482, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1028, \"height\": 456, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1026, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1031, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1031, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1027, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1027, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1453, \"height\": 473, \"label\": \"Table\"}]"
motivation: 现有EEG模型难以泛化到不同主体、任务和电极配置。
method: 提出NeurIPT，利用预训练Transformer统一建模EEG的时空特性。
result: 在多个解码任务上超越现有方法，展示了强大的跨域泛化能力。
conclusion: NeurIPT为EEG神经接口提供了有效的预训练基础模型。
---

## Abstract
Electroencephalography (EEG) has wide-ranging applications, from clinical diagnosis to brain-computer interfaces (BCIs). With the increasing volume and variety of EEG data, there has been growing interest in establishing foundation models (FMs) to scale up and generalize neural decoding. Despite showing early potential, applying FMs to EEG remains challenging due to substantial inter-subject, inter-task, and inter-condition variability, as well as diverse electrode configurations across recording setups. To tackle these open challenges, we propose **NeurIPT**, a foundation model tailored for diverse EEG-based **Neur**al **I**nterfaces with a **P**re-trained **T**ransformer by capturing both homogeneous and heterogeneous spatio-temporal characteristics inherent in EEG signals. Temporally, we introduce Amplitude-Aware Masked Pretraining (AAMP), masking based on signal amplitude rather than random intervals, to learn robust representations across varying signal intensities beyond local interpolation. Moreover, this temporal representation is enhanced by a progressive Mixture-of-Experts (MoE) architecture, where specialized expert subnetworks are progressively introduced at deeper layers, adapting effectively to the diverse temporal characteristics of EEG signals. Spatially, NeurIPT leverages the 3D physical coordinates of electrodes, enabling effective transfer across varying EEG settings, and develops Intra-Inter Lobe Pooling (IILP) during fine-tuning to efficiently exploit regional brain features. Empirical evaluations across nine downstream BCI datasets, via fine-tuning and training from scratch, demonstrated NeurIPT consistently achieved state-of-the-art performance, highlighting its broad applicability and robust generalization. Our work pushes forward the state of FMs in EEG and offers insights into scalable and generalizable neural information processing systems.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

脑电图（EEG）广泛应用于临床诊断与脑机接口（BCI）等领域。近年来，随着数据量的增长，研究者尝试建立EEG基础模型以实现跨任务、跨主体、跨配置的泛化神经解码。然而，现有基础模型大多直接借用自然语言或时间序列的预训练策略，未充分顾及EEG信号的独特属性。主要挑战包括：
- **电极空间关系被忽略**：现有方法将电极视为可互换的通道，丢失了三维物理布局信息，导致跨数据集迁移困难；
- **随机掩码预训练弊端**：类似BERT的随机连续掩码让模型倾向于局部插值学习，而非捕获有意义的全局表示；
- **缺乏脑区显式建模**：微调时通常使用全局池化或全连接层，无法有效利用不同脑叶的区域特征；
- **时间动态复杂**：EEG信号在不同任务和状态下呈现高度异质性（如慢波睡眠振荡与癫痫棘波），模型需要动态适应。

**整体含义**：本文旨在开发一个面向神经接口的通用基础模型，通过专门设计解决上述问题，推动EEG基础模型的泛化能力和实际应用。

### 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：构建一个预训练Transformer模型，同时捕获EEG信号的同质与异质时空特征。预训练阶段采用无监督的自监督学习；微调阶段针对下游任务进行有监督调优。

**关键技术细节**：
- **3D电极嵌入**：利用国际10-20系统下电极的三维坐标（x, y, z），分别使用正弦/余弦函数编码并拼接，作为空间位置编码。这一设计使得模型可以自然适应不同配置的电极布局（如10-05、10-20），无需重训练或填充。
- **幅值感知掩码预训练（AAMP）**：不同于BERT的随机掩码，AAMP根据信号幅值选址掩码区域。对于每个通道，先按幅值排序，随机选取一个百分位点，然后覆盖该点周围一定比例（如50%）的区间。这样迫使模型重建高能量区间的信号，避免简单插值。
- **渐进式混合专家（PMoE）**：在编码器各层中，浅层使用较少的专家（甚至无专家），深层逐渐增加专家数量。每个专家是一个子FFN，通过门控机制进行稀疏路由（Top-K）激活。同时保留一个共享专家以保证通用特征。辅助损失函数促进专家负载平衡。
- **颅内-颅间叶池化（IILP）**：在微调阶段，先将编码器输出沿时间轴平均池化；然后将电极按脑叶分组（额叶、颞叶左/右、枕叶、顶叶），在每个脑叶内对通道嵌入平均得到脑叶级表示；最后将所有脑叶表示拼接，形成统一的区域特征向量。该过程在每一个编码器块重复，最终所有块的输出拼接后送入分类器。

**简化描述**：
- 输入：原始EEG信号（T×D）。
- 嵌入：每个数据点编码为 s = 可学习投影 + 时间位置编码 + 3D空间编码。
- 编码器：交替进行时间注意力和空间注意力（基于Crossformer的TSA模块），其中深层采用PMoE。
- 预训练损失：ℓp范数重建损失，仅重建被掩码部分。
- 微调：使用IILP聚合脑叶特征，再接MLP分类器，损失为平衡二分类交叉熵（Bal-BCE）。

### 3. 实验设计：数据集、基准、对比方法

**数据集**：
- **预训练**：14个公开数据集（Emobrain、Grasp and Lift、Inria BCI、EEG Motor Movement/Imagery、Raw EEG Data、Resting State、SEED-Series、Siena Scalp、SPIS、Target vs Non-Target、TUAR、TUEP、TUSZ、TUSL），总计超过2,000小时数据。
- **下游任务（8个）**：MentalArithmetic（压力检测）、Mumtaz2016（抑郁症诊断）、PhysioP300（P300检测）、Sleep-EDFx（睡眠分期）、SEED-V（情绪识别）、BCIC-IV-2A（运动想象）、TUAB（异常检测）、TUEV（事件类型分类）。

**基准方法**：
- 非基础模型：EEGNet、EEGConformer、SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer。
- 基础模型：BENDR、BIOT、LaBraM、EEGPT、NeuroLM、CBraMod。

**指标**：二分类任务报告平衡准确率、AUC-PR、AUROC；多分类任务报告平衡准确率、Cohen's Kappa、加权F1。

### 4. 资源与算力

- **预训练硬件**：8张NVIDIA GeForce RTX 4090 GPU。
- **训练设置**：混合精度bfloat16，有效批大小480，约400K步。
- **训练时长**：约30小时。
- **微调**：根据数据集规模耗时数分钟至数小时不等。
- **模型参数**：总参数量73.5M，激活参数与基于MoE的稀疏路由有关（每次仅激活一部分专家）。

文中未明确提供总计算量的具体数值（如总FLOPs），但上述硬件和时长信息已足够。

### 5. 实验数量与充分性

论文进行了大量实验，充分性较高：
- **8个下游数据集**，每个数据集重复多次，报告均值与标准差。
- **11组消融实验**：
  - 不同MoE策略（无专家、均匀、收缩、渐进）
  - 不同PMoE配置（改变各层专家数）
  - 不同池化策略（无池化、均值、半球、冠状、矢状、IILP）
  - 各组件单独消融（3DPE、PMoE、IILP）
  - 不同掩码策略（随机vs AAMP）及掩码率
  - 不同激活函数（ReLU、GELU、SwiGLU）
  - 不同位置编码方式（三角函数、1D可学习、2D可学习、3D PE）
  - 低资源场景实验（1%、5%、10%数据）
- **通过SVM评估预训练表征质量**，验证AAMP优于随机掩码。
- **可视化分析**：专家参与度、注意图、通道扰动相关性等。

所有对比均采用相同时序分割和预处理，基准结果来自原论文或重跑代码，确保公平性。

### 6. 论文的主要结论与发现

- NeurIPT在8个下游数据集的绝大多数指标上达到SOTA，尤其在MentalArithmetic（平衡准确率+13.90%）、PhysioP300、BCIC-IV-2A上提升显著。
- AAMP相比随机掩码使预训练表征质量提升5.25%（SVM分类平衡准确率），且在下游微调中进一步提升。
- PMoE的渐进式设计优于均匀或收缩式MoE配置。
- IILP池化优于其他策略（均值、半球、冠状、矢状），尤其对依赖区域特征的任务（抑郁、异常检测）效果显著。
- 3D电极嵌入是性能提升的关键，在空间敏感任务（如运动想象）中尤为重要。
- 即使仅使用1%的标注数据，NeurIPT仍能保持80%以上的相对性能，显示强大少样本学习能力。

### 7. 优点

- **方法创新**：针对EEG的时空异质性提出了四项专门设计（3D嵌入、AAMP、PMoE、IILP），既新颖又实用。
- **泛化能力强**：统一预训练后直接微调，在多种任务（临床、BCI、情绪等）上稳定SOTA。
- **迁移性好**：3D电极嵌入支持不同电极系统，无需重训练；AAMP不依赖特定采样率或通道数。
- **消融实验全面**：验证了每个组件、多种变体，实验设计严谨。
- **实际部署友好**：微调计算量小，低资源场景表现尚可；代码已开源。

### 8. 不足与局限

- **参数量与计算成本**：NeurIPT总参数量73.5M，虽低于LaBraM-Huge（369M）和NeuroLM-XL（1696M），但仍高于CBraMod（4.2M）等轻量模型，训练和推理资源需求较高。
- **硬件限制**：受限于8张4090，未能探索更大规模模型和完整的标度律研究。
- **性能仍有提升空间**：在SEED-V上虽然领先但提升幅度有限；TUAB的AUC-PR和AUROC略低于CBraMod，仅在平衡准确率上持平。
- **未探索其他EEG特性**：如功能连接网络、跨频率耦合等尚未建模。
- **数据依赖性**：预训练数据以临床和实验室场景为主，真实开放环境下泛化性待验证。
- **潜在伦理风险**：可被用于非授权认知监控，需注意隐私保护。

（完）
