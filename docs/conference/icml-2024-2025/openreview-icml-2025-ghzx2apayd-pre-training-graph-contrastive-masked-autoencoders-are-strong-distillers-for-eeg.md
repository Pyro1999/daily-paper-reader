---
title: Pre-Training Graph Contrastive Masked Autoencoders are Strong Distillers for EEG
title_zh: 预训练图对比掩码自编码器是EEG的强大蒸馏器
authors: "Xinxu Wei, kanhao zhao, Yong Jiao, Hua Xie, Lifang He, Yu Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=gHzx2apaYD"
tags: ["query:pbci-load"]
score: 9.0
evidence: 专门针对EEG信号的预训练图对比掩码自编码器
tldr: 高密度EEG数据标注成本高昂，而低密度EEG数据利用率低。本文提出EEG-DisGCMAE，一种统一的图自监督预训练范式，结合图对比学习和图掩码自编码器。通过图拓扑蒸馏损失函数，模型能够从无标签高密度EEG迁移知识到有标签低密度EEG，显著提升低密度设置下的分类性能。该工作为EEG基础模型提供了有效的预训练策略。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1747, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 839, \"height\": 210, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 361, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1626, \"height\": 258, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 852, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1541, \"height\": 1720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1555, \"height\": 587, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1573, \"height\": 664, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1759, \"height\": 767, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 865, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 890, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 883, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 828, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1250, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1398, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1675, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1686, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1542, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1147, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1268, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1436, \"height\": 497, \"label\": \"Table\"}]"
motivation: 无标签高密度EEG数据丰富但标注有限，需有效利用其预训练以提升低密度场景下的性能。
method: 提出统一预训练框架EEG-DisGCMAE，融合图对比学习和图掩码自编码器，并设计图拓扑蒸馏损失实现知识迁移。
result: 在低密度EEG分类任务上，预训练后的模型显著优于直接从零训练的方法，证明了蒸馏的有效性。
conclusion: EEG-DisGCMAE方法为EEG基础模型研究提供了可迁移的预训练框架，缓解了标注数据稀缺问题。
---

## Abstract
Effectively utilizing extensive unlabeled high-density EEG data to improve performance in scenarios with limited labeled low-density EEG data presents a significant challenge. In this paper, we address this challenge by formulating it as a graph transfer learning and knowledge distillation problem. We propose a Unified Pre-trained Graph Contrastive Masked Autoencoder Distiller, named EEG-DisGCMAE, to bridge the gap between unlabeled and labeled as well as high- and low-density EEG data. Our approach introduces a novel unified graph self-supervised pre-training paradigm, which seamlessly integrates the graph contrastive pre-training with the graph masked autoencoder pre-training. Furthermore, we propose a graph topology distillation loss function, allowing a lightweight student model trained on low-density data to learn from a teacher model trained on high-density data during pre-training and fine-tuning. This method effectively handles missing electrodes through contrastive distillation. We validate the effectiveness of EEG-DisGCMAE across four classification tasks using two clinical EEG datasets with abundant data.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：高密度（HD）EEG数据分辨率高、诊断效果好，但设备成本高昂且标注困难；低密度（LD）EEG设备便宜易用，但信号分辨率低导致诊断精度不足。同时，大量无标注的EEG数据未被充分利用。如何利用丰富的无标注HD-EEG数据提升有限标注LD-EEG场景下的性能，是一个关键挑战。
- **整体含义**：本文将该问题形式化为**图迁移学习**和**知识蒸馏**问题，提出统一的预训练蒸馏框架EEG-DisGCMAE，旨在桥接无标注/有标注、HD/LD EEG数据之间的鸿沟，使得轻量级学生模型在LD数据上能达到接近HD教师模型的性能。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
- 提出一种**统一的图自监督预训练范式 GCMAE-PT**，融合图对比预训练（GCL-PT）和图掩码自编码预训练（GMAE-PT），通过相互监督与联合优化增强表征能力。
- 设计**图拓扑蒸馏损失（GTD Loss）**，在预训练和微调阶段将教师模型从HD图中学到的拓扑知识蒸馏到学生模型中，处理缺失电极问题。

### 关键技术细节
1. **EEG图构建**：将EEG时间序列通过带通滤波提取θ、α、β、γ频带，选取α频带的功率谱密度（PSD）作为节点特征，计算皮尔逊相关系数作为邻接矩阵。
2. **GCMAE-PT统一预训练**：
   - 对HD和LD图进行图增强（随机丢弃节点/边）得到查询图(Q)和键图(K)。
   - 将混合后的增强样本进行掩码，用可学习嵌入替代丢弃节点，送入教师和学生编码器进行编码。
   - 解码器重建掩码图，使用MSE损失（节点特征和结构重建）。
   - 将重建的查询/键图与原始增强样本混合，形成扩展的对比样本。
   - 采用动量键队列存储扩展键样本，通过对比损失（NT-Xent）联合优化教师和学生编码器（共享键队列）。
   - 总预训练损失 = 联合对比损失 + 联合重建损失。
3. **图拓扑蒸馏损失（GTD Loss）**：
   - 定义正样本对：在HD图中直接相连（1跳）或通过被删除节点间接相连（2跳）的节点对。
   - 定义负样本对：在LD图中相连但在HD图中不直接也不通过被删除节点间接相连的节点对。
   - 使用KL散度对齐正样本对的节点相似性分布，并惩罚负样本对的错误连接。
   - 最终GTD损失 = 正样本KL均值 / (负样本KL均值 + ε)。
4. **微调阶段**：使用交叉熵损失 + 传统logits蒸馏损失（KL散度）+ GTD损失联合优化。

## 3. 实验设计

### 数据集与场景
- **EMBARC**：308名受试者（眼开/眼闭），64通道。任务：MDD患者性别分类、抑郁症严重程度分类（HAMD-17评分）。
- **HBN**：1594眼开/1745眼闭样本，128通道。任务：MDD（健康 vs 患者）、ASD（健康 vs 患者）。
- 电极密度：HD（EMBARC: 64, HBN: 128）、MD（32/64）、LD（16/32）。
- 预训练数据集：将两个数据集（眼开+眼闭）合并，通过滑动窗口（窗口50s，重叠20s）扩增，得到约24k图样本。

### Benchmark与对比方法
- **传统机器学习**：MLP、LSTM。
- **GNN基础模型**：GCN、Graph Transformer、Hyper-GCN。
- **特定EEG模型**：EEGNet、DGCNN、EEG-Conformer、RGNN。
- **图对比预训练模型**：GCC、GraphCL、GRACE。
- **图生成预训练模型**：GraphMAE、GPT-GNN、GraphMAE2。
- **时间序列EEG预训练**：LaBraM。
- 本文方法（Ours）支持两种骨干网络：基于DGCNN（谱域GCN）或Graph Transformer（空域Transformer）。

## 4. 资源与算力
- 论文**未明确说明**使用的GPU型号、数量、训练时长等算力资源。仅在实现细节中提到批大小（预训练128，微调32）和优化器（Adam），未提供硬件细节。

## 5. 实验数量与充分性

### 实验数量
- **主要性能对比**：在2个数据集、4个分类任务上，对比了12种以上方法，每种方法报告HD和LD下的AUROC/ACC。
- **消融实验**：
  - 电极密度与模型大小（HD/MD/LD vs Tiny/Large，教师/学生）。
  - 不同蒸馏损失（Logits, GTD, 联合, LSP, G-CRD）。
  - 不同预训练方法（GCL-PT, GMAE-PT, 序列组合, GCMAE-PT）。
  - 不同掩码比率、图增强比率。
  - 不同核函数（线性、欧氏、多项式、RBF）。
  - 不同EEG频带（α, β, γ, θ, 全频带）。
  - 不同图构建连接方式（功能连接 vs 空间距离）。
  - 不同微调范式（全参数微调 vs 参数高效微调）。
  - 非常低密度（VLD）8电极场景。
  - subject-dependent/independent评估。
  - 留出法验证（held-out，仅在HBN预训练，在EMBARC微调）。
  - 扰动鲁棒性测试（加噪、随机丢弃电极）。
- **可视化分析**：EEG模式重建图、损失曲线。
- **总体实验组数**：超过20组异同实验，覆盖性能、消融、鲁棒性、泛化性。

### 充分性与公平性
- **充分**：涵盖了不同密度、不同骨干、不同预训练方法、多种消融，验证了各模块贡献。
- **客观**：使用10折交叉验证（10 runs）报告平均结果，统计严谨。
- **公平**：所有对比方法使用相同的数据划分和评估协议；教师/学生模型容量报告了参数量（如Tiny 1.3M, Large 5.7M），确保公平比较。

## 6. 论文的主要结论与发现

- GCMAE-PT统一预训练显著优于单独的GCL-PT或GMAE-PT及其序列组合，验证了联合对比与生成预训练的有效性。
- GTD损失在HD→LD蒸馏中大幅提升学生模型性能，尤其在缺失电极场景下。
- 预训练+蒸馏后，轻量级学生模型（1.3M参数）可接近或超越未预训练的大模型（5.7M参数）性能，实现效率与效果的平衡。
- 模型在低密度（如16/32通道）上相比基线提升约5% AUROC/ACC，在极低密度（8通道）仍有效。
- 重建的EEG模式保留了临床相关特征（如额叶、中央区激活），具有诊断可解释性。
- 模型对噪声和电极丢失具有更强鲁棒性。

## 7. 优点：方法或实验设计上的亮点

- **方法创新**：首次在图领域将对比预训练和掩码自编码预训练统一到同一框架，通过相互重建和对比实现深度融合。
- **蒸馏设计**：针对HD→LD电极缺失场景设计的GTD损失，利用被删除节点的间接连接关系进行拓扑知识迁移，具有强针对性。
- **通用性**：骨干网络兼容谱域GCN（DGCNN）和空域Graph Transformer，且支持不同参数规模的教师/学生配置。
- **实验全面**：覆盖多数据集、多任务、多密度、多种消融和鲁棒性分析，验证方法普适性。
- **临床应用潜力**：在低成本LD设备上达到接近高成本HD设备的性能，具有现实推广价值。

## 8. 不足与局限

- **算力资源未披露**：未提供GPU型号、训练时长等，影响可复现性评估。
- **数据同源性限制**：所有数据集来自同一10-20系统，对不同电极配置的统一处理仅通过降采样，可能造成信息损失；未处理跨系统异构数据。
- **基线方法选择**：对比的预训练方法仅包括图领域模型，未包括最新EEG时间序列预训练（如LaBraM仅略提），且未与更强大的大型EEG模型对比。
- **蒸馏仅考虑单一配对**：仅探索了一对教师/学生蒸馏，未探索多教师蒸馏或不同密度交叉蒸馏。
- **未讨论计算开销**：预训练和蒸馏的计算成本未量化，不利于实际部署评估。
- **图构造简化**：仅使用α频带的PSD特征和皮尔逊相关，其他频带或更复杂的连接指标（如coherence）仅在消融中对比，最佳配置（coherence）未在主实验中使用。
- **极端低密度场景测试有限**：虽然测试了8电极VLD，但仅在一个任务上报告，且对比方法未覆盖。

（完）
