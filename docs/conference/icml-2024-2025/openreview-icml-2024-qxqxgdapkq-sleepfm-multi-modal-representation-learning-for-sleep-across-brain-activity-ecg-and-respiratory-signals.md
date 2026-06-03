---
title: "SleepFM: Multi-modal Representation Learning for Sleep Across Brain Activity, ECG and Respiratory Signals"
title_zh: SleepFM：跨脑活动、心电图和呼吸信号的多模态睡眠表示学习
authors: "Rahul Thapa, Bryan He, Magnus Ruud Kjaer, Hyatt Moore IV, Gauri Ganjoo, Emmanuel Mignot, James Zou"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=QXqXGDapkQ"
tags: ["query:pbci-load"]
score: 8.0
evidence: 包括EEG在内的多模态睡眠基础模型
tldr: 睡眠分析依赖于多模态生理信号，但现有方法缺乏可泛化的基础模型。本文提出SleepFM，首个针对睡眠的多模态基础模型，在超过10万小时的多导睡眠图上进行预训练。通过新颖的留一法对比学习，模型从脑电、心电和呼吸信号中学习通用表示。下游任务中，基于该嵌入的逻辑回归模型优于端到端CNN，证明了基础模型在睡眠分析中的潜力。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-qxqxgdapkq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 1056, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qxqxgdapkq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1738, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qxqxgdapkq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1741, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qxqxgdapkq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1612, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qxqxgdapkq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1395, \"height\": 966, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1283, \"height\": 865, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1686, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 763, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 789, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 793, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1706, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 760, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1409, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 460, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 500, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1457, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 778, \"height\": 188, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1457, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 778, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1459, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 780, \"height\": 189, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1460, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 779, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1028, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1049, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1043, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1063, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 996, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 995, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 996, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 995, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 995, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 997, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1458, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 780, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qxqxgdapkq/table-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1423, \"height\": 440, \"label\": \"Table\"}]"
motivation: 多导睡眠图数据量大但标注困难，需要能泛化的多模态表示模型来提升下游任务性能。
method: 基于大规模多模态睡眠数据集（脑电、心电、呼吸），采用留一法对比学习预训练基础模型SleepFM。
result: SleepFM的嵌入特征在多项下游任务中优于端到端CNN，验证了基础模型的表示能力。
conclusion: 多模态基础模型SleepFM有效利用大规模未标注睡眠数据，为睡眠分析提供了通用特征提取器。
---

## Abstract
Sleep is a complex physiological process evaluated through various modalities recording electrical brain, cardiac, and respiratory activities. We curate a large polysomnography dataset from over 14,000 participants comprising over 100,000 hours of multi-modal sleep recordings. Leveraging this extensive dataset, we developed SleepFM, the first multi-modal foundation model for sleep analysis. We show that a novel leave-one-out approach for contrastive learning significantly improves downstream task performance compared to representations from standard pairwise contrastive learning. A logistic regression model trained on SleepFM's learned embeddings outperforms an end-to-end trained convolutional neural network (CNN) on sleep stage classification (macro AUROC 0.88 vs 0.72 and macro AUPRC 0.72 vs 0.48) and sleep disordered breathing detection (AUROC 0.85 vs 0.69 and AUPRC 0.77 vs 0.61). Notably, the learned embeddings achieve 48% top-1 average accuracy in retrieving modality clip pairs from 90,000 candidates. This work demonstrates the value of holistic multi-modal sleep modeling to fully capture the richness of sleep recordings. SleepFM is open source and available at https://anonymous.4open.science/r/sleepfm.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：睡眠分析依赖多模态生理信号（脑电、心电、呼吸），但现有自动化方法大多采用针对特定任务的监督学习，难以利用大规模未标注数据中的跨模态信息，缺乏可泛化的基础模型。
- **整体含义**：本文旨在构建首个面向睡眠的多模态基础模型（SleepFM），通过对比学习从超过10万小时的多导睡眠图（PSG）数据中学习通用的多模态表示，从而提升下游睡眠分析任务的性能，并降低对标注数据的依赖。

## 2. 提出的方法论

- **核心思想**：采用对比学习（Contrastive Learning, CL）对齐三种生理模态（脑活动信号BAS、心电图ECG、呼吸信号Resp）的嵌入，使来自同一30秒时间窗口的正样本对在嵌入空间中更接近，负样本对更远离。
- **关键技术细节**：
  - **编码器**：针对各模态分别使用1D CNN（基于EfficientNet架构），首层卷积核数适应各模态通道数（BAS: 10, ECG: 2, Resp: 7）。
  - **两种对比学习策略**：
    - **成对CL（Pairwise CL）**：对每对模态分别计算InfoNCE损失，如式(1)所示。
    - **留一法CL（Leave-One-Out CL）**：对每个模态，将其嵌入与其余模态的平均嵌入进行对比计算InfoNCE损失，如式(2)所示。最终损失为所有模态的留一法损失之和。
  - **预训练**：使用SGD优化器（学习率0.001，动量0.9），训练20个epoch，早停基于验证损失，batch size=32。
  - **下游分类**：冻结编码器，提取嵌入后训练逻辑回归分类器（L2正则化，类平衡权重）。

## 3. 实验设计

- **数据集**：
  - **内部数据集**：斯坦福睡眠诊所1999–2020年的PSG记录，共14,068名参与者，超过10万小时。划分预训练集11,261人、训练集1,265人、验证集141人、测试集1,401人。每段记录分割为30秒片段，共约13M片段。
  - **外部数据集**：Physionet Computing in Cardiology 2018 Challenge（Cinc2018），用于外部验证。
- **Benchmark与对比方法**：
  - **基线**：端到端监督CNN（与预训练编码器架构相同，但用全部标注数据从头训练）。
  - **对比组**：不同CL策略（成对CL vs 留一法CL）、不同模态组合（单模态、双模态、三模态）、不同训练数据量（少样本学习）。
- **评估任务**：
  - 人口属性分类（年龄组、性别）
  - 跨模态检索（Recall@10、中位数排名）
  - 睡眠阶段分类（5类：Wake, Stage1, Stage2, Stage3, REM）
  - 睡眠呼吸障碍（SDB）二分类
  - 少样本学习（从1个病人到全部训练集）
  - 模态消融（预训练时使用不同模态组合）
  - 外部验证（Cinc2018数据集）

## 4. 资源与算力

- 论文明确说明（附录A.3）：所有训练在单个NVIDIA Tesla V100S GPU（32GB显存）上执行。
- 预训练每个epoch约4小时，共20个epoch，总计约80小时；基线监督训练每个epoch约2小时。

## 5. 实验数量与充分性

- **实验数量**：论文报告了十余组实验，包括：
  - 年龄/性别分类（表2、3）
  - 检索分析（表4、5）
  - 睡眠阶段分类（表6）
  - SDB分类（表7）
  - 少样本学习曲线（图2）
  - 模态消融实验（图3）
  - 单模态性能分析（表11–14）
  - 年龄/性别分层分析（表19–22）
  - 外部验证（表8）
  - 不同对比学习策略的详细对比
- **充分性与客观性**：实验设计较为全面，覆盖了主要下游任务、不同数据量、不同模态组合、跨机构泛化能力等。对比基线(Sup-CNN)和两个CL变体，并报告95%置信区间，结论有统计支持。消融实验揭示了各模态的贡献。外部验证增强了泛化说服力。实验较为充分、公平。

## 6. 主要结论与发现

- 留一法CL显著优于成对CL，在所有下游分类任务中表现更好。
- SleepFM的嵌入特征（逻辑回归分类）在睡眠阶段和SDB分类上大幅超越端到端监督CNN（宏平均AUROC 0.88 vs 0.72，AUPRC 0.72 vs 0.48）。
- 在多模态检索任务中，成对CL取得更高召回率，但留一法CL在分类任务上更具优势。
- 少样本场景下，预训练模型相比监督CNN的绝对优势更大。
- 三模态预训练优于双模态或单模态，且ECG模态有助于提升其他模态的表示质量。
- 模型在外部数据集Cinc2018上表现良好（宏平均AUROC 0.924），证明其泛化能力。

## 7. 优点

- **数据规模与多模态**：利用超10万小时真实临床PSG数据，覆盖脑、心、肺三系统19个通道，数据量级罕见。
- **新颖的方法论**：提出留一法对比学习，有效整合多模态信息，且在分类任务上显著优于传统成对CL。
- **实验全面**：包含人口属性、检索、分类、少样本、消融、外部验证等多种评估，结果可靠。
- **开源与可复现**：代码公开，有助于后续研究。
- **实用价值**：预训练嵌入可直接用于下游任务，降低对标注数据的依赖，尤其适合少样本场景。

## 8. 不足与局限

- **数据来源单一**：预训练数据仅来自一个机构（斯坦福），尽管做了外部验证，但外部数据集规模较小（100人），跨机构泛化仍需更大范围验证。
- **未探索其他自监督方法**：仅对比了两种CL变体，未与SimCLR、BYOL、MAE等方法在时间序列上对比。
- **任务覆盖有限**：仅评估了睡眠阶段和SDB，未涉及唤醒检测、周期性腿动、嗜睡症等其他临床事件。
- **忽略缺失通道问题**：实际临床数据经常缺失某些通道，本文未对此进行鲁棒性分析。
- **计算资源**：虽报告了训练时间，但未讨论模型大小、推理效率等，可能限制实际部署。
- **潜在偏差**：数据集性别和年龄分布不够均衡（如0–18岁组较少），模型在该组表现稍差（表21），需注意公平性。

（完）
