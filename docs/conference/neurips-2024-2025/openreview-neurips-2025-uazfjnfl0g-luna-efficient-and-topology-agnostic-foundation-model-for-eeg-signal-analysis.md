---
title: "LUNA: Efficient and Topology-Agnostic Foundation Model for EEG Signal Analysis"
title_zh: LUNA：高效且拓扑无关的脑电图信号分析基础模型
authors: "Berkay Döner, Thorir Mar Ingolfsson, Luca Benini, Yawei Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=uazfjnFL0G"
tags: ["query:pbci-load"]
score: 9.0
evidence: 拓扑无关的EEG基础模型，直接支持基于EEG的认知负荷评估
tldr: EEG数据电极布局异构限制了基础模型泛化。本文提出LUNA，通过学习查询和交叉注意力将多通道EEG压缩为拓扑无关的隐空间，再以补丁时间自注意力处理。实验表明LUNA在多个分类任务上达到最优，且计算高效。该模型可直接用于被动BCI中的认知负荷估计，解决设备差异问题。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 701, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 1159, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1416, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 789, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1143, \"height\": 910, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 789, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 786, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 903, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1443, \"height\": 616, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1396, \"height\": 655, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1265, \"height\": 854, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1298, \"height\": 602, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1433, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1289, \"height\": 1257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 951, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1388, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1279, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 834, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 850, \"height\": 526, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1449, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 852, \"height\": 132, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1444, \"height\": 206, \"label\": \"Table\"}]"
motivation: 各EEG数据集电极布局不同，阻碍大规模模型泛化。
method: 设计隐查询和交叉注意力将EEG编码为拓扑无关的固定大小表示。
result: 在多个分类任务上表现优异，且复杂度与通道数线性相关。
conclusion: LUNA为异构EEG分析提供了高效的基础模型解决方案。
---

## Abstract
Electroencephalography (EEG) offers a non-invasive lens into human brain activity, but building large‐scale models is hampered by $\textit{topological heterogeneity}$: each public corpus defines its own electrode layout, limiting generalization. We introduce $\textbf{LUNA}$ ($\textbf{L}$atent $\textbf{U}$nified $\textbf{N}$etwork $\textbf{A}$rchitecture), a self-supervised foundation model that reconciles disparate electrode geometries while scaling linearly---not quadratically---with channel count. LUNA compresses multi-channel EEG into a fixed-size, topology-agnostic latent space via learned queries and cross-attention. Downstream transformer blocks then operate exclusively on this latent representation using patch-wise temporal self-attention, decoupling computation from electrode count. Pre-trained on TUEG and Siena ($\>$21,000 h raw EEG across diverse montages) using a masked-patch reconstruction objective, LUNA transfers effectively to four downstream tasks: abnormality detection, artifact rejection, slowing classification, and emotion recognition. It demonstrates highly competitive performance across several benchmarks, achieving state-of-the-art results on TUAR and TUSL, e.g., $\textbf{0.921 AUROC}$ on TUAR, while reducing FLOPs by $\textbf{300}$$\times$ and trimming GPU memory use by up to $\textbf{10}$$\times$. Critically,  these gains are consistent across all evaluated electrode configurations. Code is available at https://github.com/pulp-bio/biofoundation

---

## 论文详细总结（自动生成）

# LUNA：高效且拓扑无关的脑电图信号分析基础模型 —— 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：脑电图（EEG）数据集普遍存在**拓扑异构性**——不同公开数据集使用的电极通道数量、布局和位置各不相同。这导致现有深度学习模型难以在跨数据集、跨通道配置的场景中泛化，例如跨数据集迁移时准确率可下降 13–15 个百分点。
- **现状瓶颈**：现有方法要么为每种蒙太奇训练专用模型，要么仅保留共享电极（丢弃多达 80% 的数据）；使用全自注意力的模型复杂度为 O((S·C)²)，随着通道数增加迅速耗尽内存；交替注意力模型复杂度为 O(max(S²,C²))，仍随主导维度二次增长。
- **研究目标**：提出一个**单一、蒙太奇无关**的架构，能够在任意电极布局上高效扩展，同时保持强大的下游任务表现。

## 2. 方法论（核心思想、关键技术细节）

### 2.1 核心思想
- LUNA 通过**拓扑不变编码器**将任意电极布局投影到**固定大小的隐空间**中，后续时间处理完全基于此隐空间，实现计算与电极数的解耦。
- 采用自监督预训练（掩码补丁重建），在大规模无标签 EEG 数据（>21,000 小时）上学习通用表示。

### 2.2 架构组成（Encoder-Decoder）

#### 2.2.1 编码器
1. **补丁特征提取**：将每个通道的原始 EEG 分割为长度为 P 的非重叠时间补丁，通过两条并行路径嵌入：
   - **时间嵌入**：1D 卷积网络（GroupNorm, GELU）捕捉局部时域特征。
   - **频率嵌入**：对每个补丁的傅里叶变换的幅度和相位通过 MLP 投影。
   - 两者相加得到补丁特征 `x_features`。
2. **通道位置编码**：使用 NeRF 风格的正弦编码处理归一化的 3D 电极坐标，经 MLP 投影得到位置编码 `E_pos`，加到 `x_features`。
3. **通道统一模块（Channel-Unification Module）**：**核心创新**。引入 Q 个**可学习查询向量** `Q_learn ∈ R^{Q×E}`，通过**交叉注意力**与通道特征交互（Q 查询充当 Query，通道特征作为 Key/Value），将可变的 C 个通道特征压缩为固定大小的表示 `R^{(B·S)×Q×E}`。该过程输入形状为 `(B·S)×C×E`，输出 `(B·S)×Q×E`，复杂度为 **O(B·S·Q·C·E)**，与通道数线性相关。
4. **补丁时间编码器**：将统一后的表示重塑为 `B×S×(Q·E)`，通过堆叠的 Transformer 编码器（带 RoPE 位置编码）建模时间依赖。由于每个时间 token 已聚合多个通道信息，序列长度从 S·C 减少为 S，大幅降低计算量。

#### 2.2.2 解码器
- **预训练重构头**：使用 C 个可学习解码器查询，通过交叉注意力从隐空间中重构原始通道信号。线性投影将 E 维映射回 P 个时间点。
- **微调分类头**：使用单个聚合查询通过交叉注意力池化隐空间表示，再送入 MLP 分类。

### 2.3 训练目标
- **掩码重构损失**（Smooth L1 Loss），对掩码和可见补丁均计算损失。
- **查询特化损失**：通过最小化查询-通道注意力亲和矩阵的 Gram 矩阵非对角线元素，鼓励查询多样化、不冗余。

## 3. 实验设计

### 3.1 数据集与场景
| 用途 | 数据集 | 通道数 | 蒙太奇类型 | 数据规模 |
|------|--------|--------|-----------|----------|
| 预训练 | TUEG | 20/22 | 双极 | >21,787 小时 |
| 预训练 | Siena | 29 | 单极 | 141 小时 |
| 微调/评估 | TUAB（异常检测） | 22 | 双极 | 1,139 小时 |
| 微调/评估 | TUAR（伪影检测） | 22 | 双极 | 83.7 小时 |
| 微调/评估 | TUSL（慢波分类） | 22 | 双极 | 27.5 小时 |
| 微调/评估 | SEED-V（情绪识别） | 62（未见拓扑） | 单极 | 32.7 小时 |

- 严格确保预训练与微调数据集**无受试者重叠**。
- SEED-V 用于测试模型对**全新高密度拓扑**的迁移能力。

### 3.2 基准方法
对比了多种方法，包括：
- **监督模型**：SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer、EEGNet、EEG-GNN、GraphS4mer。
- **自监督模型**：BENDR、BrainBERT、EEGFormer、BIOT、EEG2Rep、FEMBA、CEReBrO、LaBraM、CBraMod。
- LUNA 提供三种规模：Base（7M）、Large（43M）、Huge（311M 参数）。

### 3.3 评估指标
- 主要指标：AUROC、AUPR、平衡准确率（Bal. Acc.）、Cohen's Kappa、加权 F1。

## 4. 资源与算力

- **硬件**：8× NVIDIA A100 GPU（预训练 Base/Large），16× A100 GPU（Huge 模型）。
- **软件**：PyTorch 2.4.1，bf16 混合精度。
- **预训练时长**：Base/Large 约 1 天（8 GPU），Huge 约 1 天（16 GPU）。
- **微调**：每个下游任务约 50 轮，早停 patience=10，每任务耗时数小时。
- 文中未提供精确的 GPU 小时数，但给出了清晰的计算环境描述。

## 5. 实验数量与充分性

- **四大下游任务**：异常检测、伪影检测、慢波分类、情绪识别，覆盖临床和认知两个领域。
- **消融实验**：评估了可学习查询 vs. 固定区域、查询特化损失、频率特征的贡献。
- **计算效率对比**：在通道数和补丁数两个维度上系统比较 FLOPs 和内存使用（图 2）。
- **隐空间可视化**：t-SNE 展示预训练编码器对正常/异常、伪影类别的聚类能力。
- **查询可视化**：展示不同查询聚焦于不同脑区，验证其多样化。
- 所有实验均报告 **3 个随机种子的均值和标准差**，具有统计严谨性。
- 消融实验中使用配对 t 检验比较部分变体，报告 p 值，确认差异不显著但保留正则化作用。
- **公平性**：统一预处理（带通滤波、陷波滤波、重采样至 256Hz、z-score 归一化）；TUAB 使用官方划分，其他数据集按近期文献采用随机样本级 80/10/10 分割（文中承认受试者独立分割更优）；预训练数据严格排除下游测试受试者。

**充分性评价**：实验设计全面，涵盖多种拓扑、任务、模型规模和消融。但 SEED-V 性能差距表明对未见稠密拓扑的泛化仍有改进空间。

## 6. 主要结论与发现

- **性能**：LUNA 在 TUAR 和 TUSL 上达到 **SOTA**（AUROC 0.921 / 0.802），TUAB 上达到有竞争力水平（Bal. Acc. 81.57%），SEED-V 上表现中等（Bal. Acc. 39.18%）。
- **效率**：相比 LaBraM 等全注意力模型，**FLOPs 降低高达 300×**，GPU 内存减少 **10×**；复杂度与通道数线性相关，而非二次。
- **拓扑无关性**：在评估的所有电极配置下均保持计算效率和性能优势。
- **可学习查询的有效性**：查询能够自动学习不同的空间滤波器（如专注额叶、全局等），无需预定义解剖区域。
- **预训练表征质量**：t-SNE 显示掩码重建预训练后编码器已能分离正常/异常信号和伪影类别。

## 7. 优点（方法与实验亮点）

- **拓扑不变隐空间**：通过可学习查询 + 交叉注意力实现端到端的蒙太奇统一，无需丢弃通道或依赖手工特征。
- **线性计算复杂度**：解码时间处理与通道数的依赖关系，使模型能高效应用于高密度 EEG（64–256 通道）和长窗口。
- **双路补丁嵌入**：同时使用时域和频域特征，增强表示丰富性。
- **查询特化损失**：促进查询多样性，提升鲁棒性（尤其对伪影复杂场景）。
- **大规模预训练**：>21,000 小时数据覆盖多种蒙太奇，为下游迁移提供坚实基础。
- **计算效率的彻底评估**：在补丁数和通道数两个维度上进行 FLOPs/内存对比，直观展示优势。
- **消融与统计检验**：关键模块（频率嵌入、损失函数等）均有控制实验，并报告 p 值，结论可信。
- **开源代码**：提供 GitHub 仓库，促进复现和社区使用。

## 8. 不足与局限

- **泛化到未见过的高密度拓扑**：在 SEED-V（62 通道）上性能低于 CBraMod 等模型，表明依赖预训练期间习得的位置编码，对全新密集布局的迁移能力有限。
- **预训练蒙太奇多样性有限**：仅包含 20、22、29 通道三种布局，作者承认未来需纳入更多数据集和随机通道丢弃以增强泛化。
- **数据划分**：TUAR/TUSL 使用样本级随机拆分（非受试者独立），可能高估泛化能力。作者建议未来基准采用受试者独立划分。
- **消融效果较小**：查询特化损失和可学习查询带来的性能提升 <0.01 AUROC，统计上不显著；主要价值在于正则化和灵活性，而非显著准确率提升。
- **未探索实时推理场景**：论文指出可作为未来方向，但未提供实际部署延迟或功耗测量。
- **伦理考量**：仅在结论中提及算法偏差和数据隐私风险，未深入分析或提出具体缓解措施。
- **缺失跨模态扩展**：未评估在 sEEG、ECoG 等其他颅内信号上的泛化能力。

（完）
