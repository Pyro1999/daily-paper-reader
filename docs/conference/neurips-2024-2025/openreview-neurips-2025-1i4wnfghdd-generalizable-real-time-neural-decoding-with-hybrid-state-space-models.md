---
title: "Generalizable, real-time neural decoding with hybrid state-space models"
title_zh: 具有泛化性的实时神经解码：混合状态空间模型
authors: "Avery Hee-Woon Ryoo, Nanda H Krishna, Ximeng Mao, Mehdi Azabou, Eva L Dyer, Matthew G Perich, Guillaume Lajoie"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=1i4wNFgHDd"
tags: ["query:pbci-load"]
score: 4.0
evidence: 混合状态空间模型用于实时神经解码，与被动BCI相关
tldr: 本文针对实时神经解码中传统方法泛化性差、Transformer计算量大的问题，提出POSSM混合架构，结合尖峰令牌化和交叉注意力与递归机制，在保证低延迟的同时实现了高泛化性能。该方法适用于BCI中的实时认知负荷评估，因为其处理的对象是神经尖峰而非EEG，但思路可启发EEG实时解码。实验证明POSSM在多个数据集上优于现有方法，为被动BCI提供了新的实时解码选项。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 620, \"height\": 219, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1458, \"height\": 811, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1433, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1446, \"height\": 738, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1421, \"height\": 453, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 786, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 543, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 467, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1278, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1453, \"height\": 640, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 605, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1042, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1379, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1063, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1131, \"height\": 256, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1288, \"height\": 211, \"label\": \"Table\"}]"
motivation: 实时神经解码需平衡泛化性能与延迟，现有方法难以兼顾。
method: 提出POSSM，结合尖峰令牌化交叉注意力和递归模块的混合架构。
result: 在多个尖峰数据集上实时解码准确率和泛化性优于基线。
conclusion: 该架构为实时BCI应用提供了高效且泛化的解码方案。
---

## Abstract
Real-time decoding of neural activity is central to neuroscience and neurotechnology applications, from closed-loop experiments to brain-computer interfaces, where models are subject to strict latency constraints. Traditional methods, including simple recurrent neural networks, are fast and lightweight but often struggle to generalize to unseen data. In contrast, recent Transformer-based approaches leverage large-scale pretraining for strong generalization performance, but typically have much larger computational requirements and are not always suitable for low-resource or real-time settings. To address these shortcomings, we present POSSM, a novel hybrid architecture that combines individual spike tokenization via a cross-attention module with a recurrent state-space model (SSM) backbone to enable (1) fast and causal online prediction on neural activity and (2) efficient generalization to new sessions, individuals, and tasks through multi-dataset pretraining. We evaluate POSSM's decoding performance and inference speed on intracortical decoding of monkey motor tasks, and show that it extends to clinical applications, namely handwriting and speech decoding in human subjects. Notably, we demonstrate that pretraining on monkey motor-cortical recordings improves decoding performance on the human handwriting task, highlighting the exciting potential for cross-species transfer. In all of these tasks, we find that POSSM achieves decoding accuracy comparable to state-of-the-art Transformers, at a fraction of the inference cost (up to 9x faster on GPU). These results suggest that hybrid SSMs are a promising approach to bridging the gap between accuracy, inference speed, and generalization when training neural decoders for real-time, closed-loop applications.

---

## 论文详细总结（自动生成）

# 论文总结：Generalizable, real-time neural decoding with hybrid state-space models

## 1. 论文的核心问题与整体含义（研究动机和背景）

实时神经解码是脑机接口（BCI）和闭环神经科学实验的关键技术，对延迟有严格约束（通常≤10 ms）。传统模型（如简单循环神经网络）速度快、计算轻量，但难以泛化到新会话、新个体或新任务；近期基于Transformer的模型通过大规模预训练获得了强泛化能力，但其二次计算复杂度和高资源需求不适合低资源或实时场景。论文旨在构建一种混合架构，同时满足**高精度、低延迟、易泛化**三个要求。

## 2. 论文提出的方法论

### 核心思想
结合**POYO风格的尖峰令牌化与交叉注意力**（处理变长输入）和**递归状态空间模型（SSM）骨干**（实现快速因果在线预测），实现高效且泛化的实时解码。

### 关键技术细节
- **输入处理**：神经活动以连续50 ms时间块（chunk）流式输入，每个块内尖峰数可变。
- **尖峰令牌化**：每个尖峰表示为三元组 `(UnitEmb(unit_id), timestamp)`，其中单位嵌入可学习，时间戳使用旋转变换（RoPE）编码，保留相对时序信息。
- **输入交叉注意力**：采用PerceiverIO风格，用可学习查询向量 `q` 从尖峰令牌序列中压缩出一个固定维度的潜在向量 `z(t)`。
- **递归骨干**：将 `z(t)` 输入SSM（支持S4D、GRU、Mamba等），更新隐藏状态 `h(t) = f_SSM(z(t), h(t-1))`，整合历史上下文。
- **输出交叉注意力与读出**：使用最近 `k` 个隐藏状态（实验中 `k=3`），通过交叉注意力生成行为预测。输出支持多时间戳预测、非对齐行为以及未来预测（带延迟）。
- **迁移学习**：
  - **单元识别（UI）**：冻结模型权重，仅训练新会话的单元嵌入和会话嵌入（更新参数<1%）。
  - **全微调（FT）**：先UI再逐步解冻整个模型，端到端训练。

### 公式/算法流程（文字说明）
给定一个50 ms时间块内产生的N个尖峰令牌 `X_t`，首先通过交叉注意力得到潜在向量 `z(t)`，再输入递归骨干更新隐藏状态，最后利用最近3个隐藏状态经交叉注意力输出行为（如速度）。无需重放历史数据，每次仅处理当前块。

## 3. 实验设计

### 数据集与场景
- **NHP（非人灵长类）到达任务**：包含4个公开数据集（Perich等、O’Doherty等、Churchland等、NLB Maze），覆盖中心外出（CO）、随机目标（RT）、迷宫任务。训练集共148个会话、26,032个神经元、超过6.7亿尖峰。测试集包括同动物其他天、新动物、新数据集。
- **人类手写解码**：Willett等2021数据集，1名受试者想象书写字符/画直线，共11个会话，9个用于评估（每个字符10试次）。
- **人类语音解码**：Willett等2023数据集，1名受试者尝试说话，24个会话，句子长度2–18秒，使用CTC损失。

### Benchmark与对比方法
- **NHP到达**：对比MLP、GRU、S4D、Mamba、POYO（单会话SS和预训练-1）、NDT-2。因果评估（所有模型使用50 ms步长滑动窗口，递归模型自然因果）。
- **手写**：对比PCA-KNN（原方法）、GRU、S4D、Mamba、POYO。还对预训练的o-POSSM进行跨物种迁移测试。
- **语音**：对比GRU、S4D、Mamba（均带数据增强），以及有无增强的消融。POSSM使用GRU骨干。

### 实验充分性
- 覆盖3大类任务、多个物种、多个数据集、多种骨干（S4D/GRU/Mamba）。
- 消融实验：时间块大小20ms vs 50ms（附录D.1）、尖峰时间信息（附录D.6）、上下文长度影响（附录D.2）、递归编码器替代交叉注意力（附录D.8）、LoRA微调（附录D.9）、特征混合器MLP（附录D.7）。
- 统计分析：报告均值±标准差，手写任务进行配对t检验。

## 4. 资源与算力

- **NHP单会话训练**：1块NVIDIA RTX8000 GPU，约30分钟完成500 epochs。
- **NHP多数据集预训练（o-POSSM）**：4块NVIDIA H100 GPU，约36小时。
- **手写任务**：单块RTX8000 GPU，预训练模型微调1000 epochs（baseline 600 epochs）。
- **语音任务**：单块NVIDIA A100 80GB GPU，100 epochs。
- 文中未明确报告总实验消耗，但规模中等。

## 5. 实验数量与充分性评价

### 数量
- NHP到达：5组测试条件（同动物其他天2组、新动物CO/RT各1组、新数据集1组），每组含多个会话，表1结果充分。
- 手写：9个会话×3个随机种子，共27个模型运行。
- 语音：3个随机种子，多组消融（有无增强、单向/双向）。
- 消融实验覆盖关键设计选择（时间分辨率、尖峰时间、编码器类型、微调方式）。

### 客观性与公平性
- 所有模型采用因果评估（除POYO外均按50 ms步长滑动，POYO使用1 s窗口滑动50 ms，但仅用最后50 ms预测，略有优势）。
- 报告了标准差和统计显著性（*p≤0.05），手写任务比较公正。
- 不足之处：人类受试者仅1–2人，样本量有限；NHP数据来自少数猴；未在真正的在线闭环中运行，仅为离线模拟。

## 6. 论文的主要结论与发现

1. **POSSM在NHP到达任务上匹配或超越Transformer（POYO、NDT-2），推断速度更快（GPU上最高快9倍，CPU约5.65 ms/chunk），满足实时BCI延迟要求（≤10 ms）。**
2. **多数据集预训练显著提升迁移性能**：o-POSSM通过UI或FT在新会话、新动物、新数据集上优于单会话模型，尤其在低数据量下优势明显。
3. **首次展示跨物种迁移**：仅用NHP数据预训练的o-POSSM在手写任务上达到97.73%准确率，相比基线PCA-KNN提升约16%，相比从零训练也有显著提升。
4. **长序列语音解码**：POSSM（GRU骨干）在不使用数据增强时表现稳健，PER低至19.80%（双向），优于纯GRU（21.74%）。且参数更少（32M vs 55M）。
5. **消融显示**：保留尖峰精确时间信息对性能很重要，时间块20ms仍可工作，输出交叉注意力可预测未来50–100 ms行为。

## 7. 优点

- **高效实时**：推理时间极短（GPU ~2–5.6 ms/chunk），适合在线BCI部署。
- **灵活输入**：尖峰令牌化支持变长度、变神经元集合，无需重新训练架构。
- **易于迁移**：单元识别（UI）更新极少参数，全微调（FT）可进一步适配。
- **跨物种潜力**：利用丰富NHP数据改善人类临床数据不足的问题，具有实际价值。
- **架构可扩展**：可替换骨干（S4D/GRU/Mamba），可适配不同模态（未验证但理论上可）。
- **实验设计较全面**：覆盖多任务、多数据集、多骨干，并包含多种消融。

## 8. 不足与局限

- **实验覆盖**：仅基于侵入式皮层记录（Michigan阵列），未在EEG、ECoG等非侵入或不同脑区验证。虽在附录D.4展示小鼠视觉行为数据解码，但非主要任务。
- **人类样本极少**：手写和语音各仅1名受试者，跨物种结论仍需更大规模验证。
- **离线模拟**：虽称设计为实时，但所有实验均为离线模拟因果推理，未在真正在线闭环中部署测试。
- **语音解码未使用语言模型**，也未与最新混合模型（如Jamba、Griffin）比较，仅对比纯GRU/S4D/Mamba。
- **部分数据预处理限制**：语音任务中仅提供归一化计数而非原始尖峰时间，无法使用完整POYO式令牌化，改用价值嵌入，可能削弱优势。
- **未报告与其他混合模型的直接对比**（如Block-Recurrent Transformer），也未对POYO-1进行相同规模的预训练比较（o-POSSM参数量更大）。
- **公平性考量**：因果评估下Transformer模型（POYO、NDT-2）使用固定1 s窗口并滑动，其输入范围大于POSSM的50 ms块，但POSSM通过隐藏状态累积历史，二者比较仍需谨慎解释。

（完）
