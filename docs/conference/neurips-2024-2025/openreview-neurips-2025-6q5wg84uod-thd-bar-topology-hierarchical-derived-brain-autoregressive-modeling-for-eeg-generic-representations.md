---
title: "THD-BAR: Topology Hierarchical Derived Brain Autoregressive Modeling for EEG Generic Representations"
title_zh: THD-BAR：面向EEG通用表示的拓扑层次推导脑自回归建模
authors: "Wenchao Yang, Weidong Yan, Wenkang Liu, Yulan Ma, Yang Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=6Q5WG84uOD"
tags: ["query:pbci-load"]
score: 9.0
evidence: 通过自回归预训练学习EEG通用表示，可直接作为EEG基础模型
tldr: 现有EEG自回归模型仅考虑时间序列而忽略脑拓扑，该论文提出THD-BAR，通过拓扑层次推导脑自回归建模，在预训练中同时捕捉时间和动态空间拓扑信息。该方法学习到的通用EEG表示可直接用于被动BCI中的认知负荷评估等下游任务，仅需少量微调。在多个EEG任务上取得最先进性能，验证了其作为EEG基础模型的有效性，是构建面向认知负荷评估的EEG基础模型的重要进展。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1295, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 652, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1434, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 581, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1458, \"height\": 535, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1454, \"height\": 326, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1382, \"height\": 983, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1390, \"height\": 1134, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1272, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1330, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1312, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 688, \"height\": 1084, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1370, \"height\": 785, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 846, \"height\": 531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 1092, \"label\": \"Table\"}]"
motivation: 现有EEG自回归模型忽视脑动态空间拓扑，限制了表示能力。
method: 提出拓扑层次推导的自回归预训练方法，同时建模时间序列和动态空间拓扑。
result: 在多个EEG分类任务上达到最先进性能，证明通用表示的有效性。
conclusion: 该方法为EEG基础模型提供了新的预训练范式，有望支撑被动BCI应用。
---

## Abstract
Large-scale pre-trained models hold significant potential for learning universal EEG representations. However, most existing methods, particularly autoregressive (AR) frameworks, primarily rely on straightforward temporal sequencing of multi-channel EEG data, which fails to capture the rich physiological characteristics inherent to EEG signals. Moreover, their time-centered modeling approach also limits the effective representation of the dynamic spatial topology of brain activity. To address these challenges and fully exploit the potential of large-scale EEG models, we propose a novel Topology Hierarchical Derived Brain Autoregressive Modeling (THD-BAR) for EEG generic representations. The core innovation of THD-BAR lies in the introduction of the Brain Topology Hierarchy (BTH), which establishes a multi-scale spatial order for EEG channels. This hierarchical structure enables a redefinition of autoregressive learning as a "next-scale-time prediction" problem, effectively capturing both spatial and temporal dynamics. Based on BTH, we design a Topology-Hierarchical Vector Quantized-Variational Autoencoder (THVQ-VAE) for multi-scale tokenization and develop an enhanced Brain Autoregressive (BAR) module with specialized masking strategies for prediction. Through extensive large-scale pre-training on 17 datasets, followed by rigorous validation on 10 downstream datasets spanning 5 distinct tasks, THD-BAR consistently outperforms existing methods. These results highlight the superior generalization and modeling capabilities of our proposed approach.

---

## 论文详细总结（自动生成）

# THD-BAR 论文详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）

现有的大规模 EEG 预训练模型，特别是自回归（AR）框架，大多采用简单的多通道时间序列排列方式（“next-time prediction”），未能捕获 EEG 信号丰富的生理特性，尤其是大脑活动的动态空间拓扑结构。这种时间中心的建模方式限制了模型对全局脑动态空间关系的表征能力。本文提出 THD-BAR 框架，旨在通过引入“脑拓扑层次”（Brain Topology Hierarchy, BTH），将自回归学习重新定义为“next-scale-time prediction”问题，同时建模空间尺度和时间序列上的依赖关系，从而学习更通用的 EEG 表示。该研究是构建面向被动 BCI（如认知负荷评估）的 EEG 基础模型的重要进展。

## 2. 方法论

### 核心思想
- 提出 **脑拓扑层次（BTH）**：基于标准电极放置系统（如 10-10 系统），根据空间邻近性和对应脑区功能，将 EEG 通道组织为多尺度空间顺序（从全脑尺度到脑区、子区、通道簇、单个通道），共 5 个尺度（S1–S5）。
- 基于 BTH 设计 **拓扑层次向量量化变分自编码器（THVQ-VAE）**：对 EEG 信号进行多尺度离散 token 化。
- 构建 **脑自回归（BAR）模块**：采用“next-scale-time prediction”策略，结合尺度因果掩码和时间因果掩码，同时学习空间层次内与时间序列间的依赖关系。

### 关键技术细节
- **THVQ-VAE 编码与量化**（Algorithm 1）：将 EEG 信号分割为时间块，通过编码器得到特征图，然后在各尺度上依次执行下采样、量化、查找码本、上采样，并引入残差设计减少信息冗余。所有尺度共享一个码本。
- **THVQ-VAE 解量化与解码**（Algorithm 2）：按尺度反向顺序累积量化特征，再经解码器重建 EEG 信号。
- **BAR 自回归预训练**：将多尺度 token 展平为“层次时间”序列（先空间层次后时间步），训练时使用“尺度-时间因果掩码”，使得每个 token 可以关注之前时间步的所有尺度以及当前时间步的较粗尺度。预测目标为条件概率 P(r_t^s | 前 t-1 时间步所有 token, 当前时间步 1 到 s-1 尺度 token)。
- 损失函数：包含时域重建损失、频域重建损失、特征码本损失以及一个域分类对抗损失（用于多模态对齐）。

### 公式与算法流程（文字说明）
- 编码：`f = Encoder(eeg)` → 对各尺度 s：`r_s = Quantize(downscale(f, ch_S, ch_s))` → 残差更新 `f -= φ_s(upscale(lookup(r_s)))`。
- 解码：逆过程，逐步上采样并累加各尺度特征。
- 自回归概率：`P(q_1,...,q_T) = ∏_t ∏_s P(r_t^s | q_1,...,q_{t-1}, r_t^1,...,r_t^{s-1})`。

## 3. 实验设计

### 数据集
- **预训练数据集**：17 个公开 EEG 数据集，涵盖情绪、运动想象、工作量、睡眠、癫痫等多种任务，总时长超过 2000 小时。
- **下游任务数据集（微调与评估）**：10 个数据集，覆盖 5 大任务：情绪识别（DEAP、SEED）、运动想象（MIBCI、BCIC4-1）、心理工作量（EEGMat、STEW）、睡眠分期（EDF、HMC）、癫痫检测（TUAB、TUEV）。

### 基准与对比方法
- **单任务专用模型**：EEGNet、TSception、LGGNet。
- **通用预训练模型**：BIOT、LaBraM、EEGPT、NeuroLM。
- 对比指标：平衡准确率（Balanced Accuracy）。

### 实验规模
- 在 10 个下游数据集上进行了主实验比较。
- 消融实验：多尺度组合（9 种配置）、掩码设计（3 种变体）。
- 可视化分析：tokenizer 重建质量、自回归预训练曲线。

## 4. 资源与算力

论文明确说明实验基于 **8 块 NVIDIA L40s-48G GPU** 完成。具体训练时长未精确给出，但提供了各阶段超参数（batch size、学习率、epoch 等）。例如神经 tokenizer 训练 50 个 epoch，BAR 预训练 20 个 epoch，指令微调 5（Base/Large）或 3（Huge）个 epoch。

## 5. 实验数量与充分性

- **主实验**：在 10 个下游数据集上报告了 THD-BAR 三种规模（Base/124M、Large/354M、Huge/1555M）与 6 种基线方法的对比结果。
- **消融实验**：多尺度组合从 1 到 5 尺度共 9 种配置，验证了完整 5 尺度（O5）最优；掩码设计三种变体（仅尺度、仅时间、尺度-时间）对比，所提的尺度-时间掩码最佳。
- **可视化实验**：展示了 tokenizer 重建的 PCC、损失曲线，以及空间热图对比。
- **充分性评价**：实验覆盖了主流 EEG 任务类型，对比方法包括近期 SOTA（如 NeuroLM、EEGPT），且消融实验设计合理，结论清晰。多尺度与掩码消融直接验证了核心贡献，实验充分、客观。

## 6. 主要结论与发现

- THD-BAR 在 9/10 个下游数据集上取得了最优平衡准确率，显著优于现有方法，尤其在 DEAP 和 SEED 情绪识别任务上分别比 NeuroLM 高出 2.2% 和 3.3%。
- 模型规模增大（Base→Large→Huge）通常带来性能提升。
- 多尺度 tokenization 比单尺度能更完整地捕获 EEG 信号的复杂性。
- 提出的“尺度-时间因果掩码”优于纯尺度或纯时间掩码，验证了同时建模空间层次和时间序列的必要性。
- 可视化表明 THVQ-VAE 能更好地保留 EEG 信号的动态时空演进模式。

## 7. 优点

- **创新性**：首次将层次拓扑结构引入 EEG 自回归预训练，定义了基于生理的通道空间顺序，突破了传统时间中心建模的局限。
- **框架完整性**：从 BTH 构建、THVQ-VAE tokenizer、BAR 自回归模块、到多任务指令微调，形成完整 pipeline。
- **实验覆盖广**：预训练 17 数据集，微调 10 数据集 5 任务，对比多种主流方法，消融实验设计严谨。
- **代码开源**：促进可复现性和领域发展。
- **性能突出**：在多个任务上达到 SOTA，证明了方法的通用性和泛化能力。

## 8. 不足与局限

- **多模态融合较浅**：当前多模态对齐主要用于指令微调，与文本更深层融合（如文本引导生成）未充分探索。
- **实时性限制**：大模型（Huge 1.5B）推理速度可能不适合实时 BCI 应用，文章未讨论模型压缩或非自回归变体。
- **拓扑定义依赖先验**：BTH 层次划分基于 10-10 系统空间邻近性，对不同电极帽/配置的适应性未系统验证；未探索数据驱动或解剖模板驱动的替代划分。
- **计算资源需求高**：预训练需要 8×L40s GPU，对中小实验室可能成本较高。
- **下游任务覆盖仍有盲区**：虽然涵盖 5 类任务，但未涉及例如脑电去噪、异常检测、神经事件时空定位等生成/回归类应用，通用性验证还可扩展。

（完）
