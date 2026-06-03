---
title: "EEGPT: Pretrained Transformer for Universal and Reliable Representation of EEG Signals"
title_zh: EEGPT：用于通用可靠EEG信号表征的预训练Transformer
authors: "Guangyu Wang, Wenchao Liu, Yuhong He, Cong Xu, Lin Ma, Haifeng Li"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=lvS2b8CjG5"
tags: ["query:pbci-load"]
score: 9.0
evidence: 提出EEGPT，一种用于EEG信号处理的基础模型
tldr: 当前EEG信号处理面临低信噪比、高跨被试变异性等挑战。本文提出EEGPT，一个基于Transformer的EEG预训练基础模型，通过掩码双自监督学习和时空表征对齐，实现通用可靠的EEG特征提取。实验表明EEGPT在多个下游任务上达到最优性能，为EEG基础模型研究提供了新范式。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1149, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1169, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 420, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 564, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1070, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 770, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 718, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 718, \"height\": 525, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 714, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 713, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1343, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 874, \"height\": 876, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 858, \"height\": 251, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 731, \"height\": 759, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 485, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 747, \"height\": 605, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 869, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lvs2b8cjg5/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 455, \"height\": 374, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1112, \"height\": 544, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1084, \"height\": 388, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1353, \"height\": 384, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1380, \"height\": 863, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1160, \"height\": 385, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1413, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1422, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1330, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1054, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1320, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1157, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1085, \"height\": 424, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lvs2b8cjg5/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1084, \"height\": 423, \"label\": \"Table\"}]"
motivation: 现有EEG特征提取方法受限于低信噪比和高变异性，缺乏通用可靠的表征。
method: 提出基于Transformer的10M参数预训练模型，采用掩码双自监督学习和时空对齐。
result: 在多个EEG下游任务上取得最优结果，验证了模型的通用性和可靠性。
conclusion: EEGPT为EEG信号处理提供了首个大规模预训练基础模型，有望推动BCI等应用发展。
---

## Abstract
Electroencephalography (EEG) is crucial for recording brain activity, 
  with applications in medicine, neuroscience, and brain-computer interfaces (BCI). 
  However, challenges such as low signal-to-noise ratio (SNR), high inter-subject variability, and channel mismatch complicate the extraction of robust, 
  universal EEG representations. 
  We propose EEGPT, a novel 10-million-parameter pretrained transformer model designed for universal EEG feature extraction. 
  In EEGPT, a mask-based dual self-supervised learning method for efficient feature extraction is designed. 
  Compared to other mask-based self-supervised learning methods, 
  EEGPT introduces spatio-temporal representation alignment. 
  This involves constructing a self-supervised task based on 
  EEG representations that possess high SNR and rich semantic information, 
  rather than on raw signals. 
  Consequently, this approach mitigates the issue of poor feature quality typically 
  extracted from low SNR signals.
  Additionally, EEGPT's hierarchical structure processes spatial and temporal information separately, 
  reducing computational complexity while increasing flexibility and adaptability for BCI applications. 
  By training on a large mixed multi-task EEG dataset, we fully exploit EEGPT's capabilities.
  The experiment validates the efficacy and scalability of EEGPT, 
  achieving state-of-the-art performance on a range of downstream tasks with linear-probing.
  Our research advances EEG representation learning, offering innovative solutions for bio-signal processing and AI applications.
  The code for this paper is available at: https://github.com/BINE022/EEGPT

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：脑电图（EEG）信号在医学、神经科学和脑机接口（BCI）等领域具有重要价值，但面临低信噪比（SNR）、高跨被试变异性、以及不同采集设备间通道不匹配等问题，导致难以提取鲁棒且通用的EEG表征。
- **整体含义**：现有基于自监督学习的方法（如BENDR、BIOT、LaBraM）在EEG表示学习上取得了一定进展，但依然受限于低SNR下特征质量差、卷积编码器难以解耦通道与信号相关性、以及对不同采样率和电极位置适应性不足等问题。本文旨在通过设计一种全新的预训练Transformer模型——EEGPT，实现通用、可靠的EEG特征提取，推动EEG基础模型的发展。

## 2. 方法论

### 核心思想
- 提出**双自监督学习方法**：同时进行**掩码重建**和**时空表征对齐**。不同于传统仅对原始波形重建的方法，EEGPT引入了一个基于动量编码器的对齐分支，促使编码器输出富含高语义信息的全局特征，从而缓解低SNR导致的特征质量差问题。
- 采用**层次化结构**，分别处理空间和时间信息，降低计算复杂度的同时提升BCI应用的灵活性和适应性。
- 设计**局部时空嵌入方法**，增强对不同EEG采集设备的鲁棒性和兼容性。

### 关键技术细节
- **输入处理**：将多通道EEG信号 \( x \in \mathbb{R}^{M \times T} \) 分块为 \( p_{i,j} \)（通道i、时间块j），每个块长度为 \( d = 64 \) 时间点（约250ms），通过线性嵌入和可学习的通道编码得到 token。
- **模块组成**：编码器（Encoder）、预测器（Predictor）、动量编码器（Momentum Encoder）和重建器（Reconstructor）。其中，编码器处理未掩码部分，预测器根据编码器输出预测所有时间段的特征，动量编码器（结构与编码器相同，参数通过指数移动平均更新）对完整信号提取特征，重建器根据编码器和预测器的输出恢复被掩码的原始信号块。
- **掩码策略**：在预训练时，随机对50%的时间块和80%的通道块进行掩码。
- **损失函数**：总损失 \( L = L_A + L_R \)。
  - \( L_A \)：对齐损失（MSE），使预测特征与动量编码器输出（经层归一化）对齐。
  - \( L_R \)：重建损失（MSE），使重建块与原始块对齐。
- **下游任务**：使用线性探测（linear-probing）方法，冻结编码器参数，仅训练一个自适应空间滤波器（1×1卷积）和线性分类头，防止过拟合并评估编码器质量。

### 公式流程（文字说明）
1. 输入EEG信号分块 → 嵌入为 tokens → 掩码得到M和未掩码部分。
2. 编码器处理未掩码tokens，输出特征 \( enc_j \)。
3. 预测器结合位置编码，从 \( enc_j \) 预测所有时间段特征 \( pred_t \)。
4. 动量编码器处理完整信号，输出 \( menc_j \)；对齐损失使 \( pred_j \) 逼近 \( menc_j \)。
5. 重建器利用 \( enc_j \) 和 \( pred_j \) 重建被掩码块，计算重建损失。
6. 总损失为两损失之和，联合优化。

## 3. 实验设计

### 数据集
- **预训练数据集**：混合多任务EEG数据集，包括：
  - PhysioMI（运动想象/执行，109人）
  - HGD（运动想象，14人）
  - TSU（SSVEP，35人）
  - SEED（情绪识别，15人）
  - M3CV（多任务，106人）
- **下游任务数据集**：
  - 运动想象：BCIC-2A（4类，10人）、BCIC-2B（2类，10人）
  - 睡眠分期：Sleep-EDFx（197人，5类）
  - ERP类型：KaggleERN（ERN检测，26人，2类）、PhysioP300（P300检测，9人，2类）
  - 异常检测：TUAB（异常/正常，2类，约40万样本）
  - 事件类型分类：TUEV（6类，约11万样本）

### Benchmark 与对比方法
- 在TUAB和TUEV上，对比了SPaRCNet、ContraWR、CNN-T、FFCL、ST-T、BIOT等全微调方法。
- 在其他下游任务上，对比了BENDR、BIOT、LaBraM（均使用线性探测进行公平比较）。
- 评估指标：平衡准确率（BAC）、AUROC、加权F1、Cohen's Kappa。

## 4. 资源与算力

- 文中明确说明：使用**8块Nvidia 3090 GPU**进行预训练。
- 训练设置：AdamW优化器，OneCycle学习率策略（初始2.5e-4，最大5e-4，最小3.13e-5），训练200个epoch，batch size为64，16位混合精度训练。
- 模型参数量：最大模型约1.01亿参数（large），主实验使用2500万参数模型（base2），最小模型约40万参数（tiny1）。

## 5. 实验数量与充分性

- **实验总数**：涵盖6个下游数据集（BCIC-2A/2B、Sleep-EDFx、KaggleERN、PhysioP300、TUAB、TUEV），加上预训练实验和消融实验，共约10余组主要实验。
- **消融实验**：
  - 对比有无对齐损失、有无层归一化、有无跳跃连接、有无预测器等变体。
  - 对比线性探测与全微调、有无自适应空间滤波器。
  - 探究模型规模（8种变体）与预训练数据量（100%、50%、25%、12.5%）的缩放规律。
- **充分性评价**：实验覆盖了多种范式（运动想象、睡眠分期、ERP、异常检测、事件分类），且在多个任务上报告了平均和标准差，重复3次。对比方法选择主流基线，且采用相同的线性探测设置，公平性较好。但TUAB和TUEV上LaBraM使用了更大的预训练集（含TUEG），可能导致性能优势，论文对此进行了说明。

## 6. 主要结论与发现

- EEGPT在BCIC-2A、BCIC-2B、Sleep-EDFx、KaggleERN、PhysioP300上均取得最优或接近最优结果，尤其在TUEV上相比BIOT提升BAC 9.5%、加权F1 6.9%。
- 相比BENDR（全微调）和BIOT/LaBraM（线性探测），EEGPT在运动想象任务上提升明显（BCIC-2A上BAC 58.46% vs LaBraM 56.13%）。
- 消融实验证实双自监督方法有效：去对齐损失导致性能下降6%~9%；去层归一化或跳跃连接也会降低性能。
- 模型规模越大，下游性能越好，符合缩放定律：ACC = (33.6 * N)^0.029，L_R = (0.72 * N)^{-0.014}。
- 预训练数据量越大，性能越好，缩放定律为ACC = (0.58 * D)^0.0461等。
- 线性探测方法优于全微调（在BCIC-2B和KaggleERN上），且自适应空间滤波器能提升性能。

## 7. 优点

- **方法创新**：提出掩码双自监督学习（掩码重建 + 时空表征对齐），有效缓解低SNR下特征质量差的问题。
- **层次化结构**：分别处理空间和时间信息，降低计算复杂度，增强对BCI场景的适应性。
- **局部时空嵌入**：通过可学习通道编码和灵活映射，兼容不同通道配置的设备。
- **线性探测评估**：冻结编码器仅训练线性层，能更公正地评估预训练表征质量，同时防止小样本过拟合。
- **实验全面**：涵盖多种范式、多个数据集，验证了模型的通用性和可扩展性。
- **代码开源**：提供GitHub仓库，便于复现和后续研究。

## 8. 不足与局限

- **模型规模仍有限**：最大1.01亿参数，相比于CV/NLP的大模型仍有差距，论文指出这是探索性工作。
- **预训练数据量不足**：虽然混合多任务数据集，但规模远小于视觉/语言领域的预训练数据，且TUAB/TUEV上LaBraM因使用更大预训练集（含TUEG）而表现更好。
- **时间窗口限制**：EEGPT预训练时使用4s的EEG片段，可能限制了其对长时间依赖的建模能力。
- **计算资源需求高**：8块3090 GPU训练200个epoch，对一般实验室而言成本较高。
- **实验偏差风险**：部分下游任务（如TUAB）使用线性探测，而基线BIOT等使用全微调，虽然对基线有利，但EEGPT仍取得可比较结果；但在Sleep-EDFx上，EEGPT使用了4层Transformer的额外分类器，可能增加了不公平性（但论文已说明原因）。
- **应用限制**：模型主要针对EEG，未验证对ECG等其他生物信号的泛化性；且仅支持4s输入，对更长或更短的任务可能需要额外调整。
- **未讨论隐私或伦理问题**：如模型在真实BCI场景中的安全性、公平性等。

（完）
