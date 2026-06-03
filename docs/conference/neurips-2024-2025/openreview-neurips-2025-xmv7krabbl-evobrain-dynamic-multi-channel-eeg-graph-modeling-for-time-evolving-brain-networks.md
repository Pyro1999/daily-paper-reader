---
title: "EvoBrain: Dynamic Multi-Channel EEG Graph Modeling for Time-Evolving Brain Networks"
title_zh: EvoBrain：面向时变脑网络的多通道EEG动态图建模
authors: "Rikuto Kotoge, Zheng Chen, Tasuku Kimura, Yasuko Matsubara, Takufumi Yanagisawa, Haruhiko Kishima, Yasushi Sakurai"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=XmV7KRABBl"
tags: ["query:pbci-load"]
score: 6.0
evidence: 动态图建模用于EEG癫痫检测，方法可迁移至被动BCI认知负荷评估
tldr: 针对癫痫检测中脑连接动态变化难以建模的问题，该论文提出EvoBrain动态图神经网络，在EEG数据上同时学习时序信号和动态图结构。该方法不限于癫痫检测，其动态图建模框架可直接迁移至被动BCI中的认知负荷评估，因为认知负荷同样涉及脑功能连接的变化。实验表明EvoBrain在癫痫检测上优于静态图方法，验证了动态建模的有效性，为基于图深度学习的EEG认知负荷分析提供了可行方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1424, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 678, \"height\": 344, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 663, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1426, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1349, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1420, \"height\": 718, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1141, \"height\": 764, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1456, \"height\": 137, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 852, \"height\": 302, \"label\": \"Table\"}]"
motivation: 现有EEG动态GNN使用固定图结构，无法捕捉脑连接的时变特性。
method: 提出动态图神经网络，联合学习时序信号和动态图结构。
result: 在癫痫检测任务上性能优于静态图方法，有效建模脑网络演化。
conclusion: 动态图建模为EEG脑状态分析提供了新工具，可推广至认知负荷等应用。
---

## Abstract
Dynamic GNNs, which integrate temporal and spatial features in Electroencephalography (EEG) data, have shown great potential in automating seizure detection.
However, fully capturing the underlying dynamics necessary to represent brain states, such as seizure and non-seizure, remains a non-trivial task and presents two fundamental challenges.
First, most existing dynamic GNN methods are built on temporally fixed static graphs, which fail to reflect the evolving nature of brain connectivity during seizure progression. 
Second, current efforts to jointly model temporal signals and graph structures and, more importantly, their interactions remain nascent, often resulting in inconsistent performance.
To address these challenges, we present the first theoretical analysis of these two problems, demonstrating the effectiveness and necessity of explicit dynamic modeling and time-then-graph dynamic GNN method.
Building on these insights, we propose EvoBrain, a novel seizure detection model that integrates a two-stream Mamba architecture with a GCN enhanced by Laplacian Positional Encoding, following neurological insights.
Moreover, EvoBrain incorporates explicitly dynamic graph structures, allowing both nodes and edges to evolve over time.
Our contributions include 
(a) a theoretical analysis proving the expressivity advantage of explicit dynamic modeling and time-then-graph over other approaches, 
(b) a novel and efficient model that significantly improves AUROC by 23\% and F1 score by 30\%, compared with the dynamic GNN baseline, and 
(c) broad evaluation of our method on the challenging early seizure prediction task.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义（研究动机和背景）

- **研究动机**：癫痫发作本质上是脑网络异常连接导致的网络障碍，自动检测癫痫依赖于从EEG信号中捕捉脑连接的动态演化。现有动态GNN大多使用静态图结构（固定邻接矩阵），忽略了脑连接在癫痫发作过程中的时变特性；同时，现有方法在联合建模时序信号与图结构时效果不一致。
- **核心问题**：如何设计能有效表示脑网络动态演化的图神经网络模型，同时提升癫痫检测和预测的准确性与效率。

### 方法论：核心思想、关键技术细节

- **核心思想**：基于理论证明，提出“显式动态图建模”与“time-then-graph”架构组合。
- **关键技术细节**：
  1. **显式动态图结构**：将EEG信号分割为短时快照，对每个快照计算通道间归一化互相关作为边权重，保留top-τ最大相关边，构建随时间变化的邻接矩阵序列，而非固定矩阵。
  2. **频率特征提取**：对EEG信号进行短时傅里叶变换（STFT），取非负频率分量的对数幅度作为节点特征。
  3. **时序建模（双流Mamba）**：分别使用两个独立的Mamba模块（可视为输入依赖参数的线性RNN）处理节点特征和边特征，捕捉短时与长时依赖。
     - 节点Mamba：输入每个通道的时序特征序列，输出节点最终隐藏状态。
     - 边Mamba：输入每个边权重的时序序列，输出边的最终隐藏状态。
  4. **空间建模（GCN + Laplacian Positional Encoding）**：将节点和边的时序表示拼接，使用Laplacian Positional Encoding（LapPE）注入脑区空间特异性（避免结构对称性导致的节点不可区分），然后通过GCN聚合邻域信息，最后用最大池化得到图表示，经全连接层和softmax输出分类。

### 实验设计

- **数据集**：
  - 主要数据集：Temple University Hospital EEG Seizure dataset v1.5.2（TUSZ），包含5,612条记录、3,050次标注发作。
  - 辅助数据集：CHB-MIT（844小时22通道头皮EEG，163次发作）。
- **任务**：癫痫检测（分类发作/非发作）和早期预测（区分发作前1分钟预发作期与正常期）。
- **对比方法**：
  - 传统机器学习：SVM、Random Forest。
  - 深度学习非图模型：LSTM、CNN-LSTM。
  - 基础模型：BIOT、LaBraM、EEGPT。
  - 动态GNN：EvolveGCN（graph-then-time）、DCRNN（time-and-graph）、GRAPHS4MER（time-then-graph）、GRU-GCN（time-then-graph）。
- **评估指标**：AUROC和F1分数，所有结果在5个随机种子下取平均±标准差。

### 资源与算力

- 文中明确提到：使用NVIDIA A6000 GPU和Xeon Gold 6258R CPU进行训练，所有模型训练100个epoch，初始学习率1e-4，Adam优化器。但未给出具体GPU数量、训练总时长或能耗数据。

### 实验数量与充分性

- 实验较充分：包括两个数据集（TUSZ和CHB-MIT），两个任务（检测和预测），两种输入长度（12秒和60秒），对比了多种基线（传统/深度学习/基础模型/不同架构动态GNN）。
- 消融实验：评估了不同架构（time-then-graph vs. time-and-graph vs. graph-then-time）、是否使用动态图结构、是否使用FFT/LapPE、替换GNN/RNN层等。
- 计算效率对比：测量了训练和推理时间，并展示了内存消耗表。
- 临床分析：可视化动态图结构与不同脑状态（正常、预发作、局灶性发作、全面性发作）的对应关系，验证了神经科学一致性。
- 总体评价：实验设计客观、公平，覆盖了主要对比和消融，但仅聚焦于癫痫任务，未推广到其他EEG任务。

### 论文主要结论与发现

1. 理论证明：显式动态图建模严格强于隐式（静态）动态图建模；time-then-graph架构严格强于time-and-graph和graph-then-time。
2. 所提EvoBrain在TUSZ数据集上，癫痫检测AUROC最高达0.877，F1达0.539，相比动态GNN基线提升23% AUROC和30% F1；早期预测任务AUROC提升13.8%。
3. EvoBrain训练速度比time-and-graph基线快17倍，推理快14倍。
4. 动态图结构能提升所有动态GNN方法的性能，验证了显式动态建模的必要性。
5. 临床可视化显示模型学到的动态图结构与癫痫发作的不同阶段（正常、预发作、局灶性、全面性）神经学特征一致。

### 优点

- **理论创新**：首次对EEG动态图建模进行严格的表达性理论分析，为架构选择提供依据。
- **方法有效性**：结合Mamba和GCN，利用Mamba的输入依赖参数特性模拟神经可塑性，设计巧妙。
- **高效性**：采用time-then-graph，只在最终做一次GCN，计算复杂度显著低于time-and-graph。
- **应用价值**：在更具挑战的早期预测任务中保持优势，临床可视化可辅助病灶定位。

### 不足与局限

- **任务局限**：仅评估癫痫检测/预测，未在认知负荷、睡眠分期等任务验证泛化能力。
- **预发作定义**：早期预测中预发作期固定为1分钟，缺乏临床统一标准，可能限制可解释性。
- **数据偏差风险**：作者承认模型可能对特定人群存在偏差，训练数据来自有限医院，未进行人口统计审计。
- **算力汇报不完整**：未给出总训练时长或具体GPU消耗，可重复性细节可进一步补充。
- **虚假警报风险**：预测任务中误报可能造成患者不必要的干预和焦虑。

（完）
