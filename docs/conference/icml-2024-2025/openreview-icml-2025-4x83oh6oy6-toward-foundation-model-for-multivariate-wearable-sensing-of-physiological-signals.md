---
title: Toward Foundation Model for Multivariate Wearable Sensing of Physiological Signals
title_zh: 面向多变量可穿戴生理信号感知的基础模型
authors: "Yunfei Luo, Yuliang Chen, Asif Salekin, Tauhidur Rahman"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=4x83oH6Oy6"
tags: ["query:pbci-load"]
score: 7.0
evidence: 基于多生理信号（含EEG）预训练的基础模型，用于可穿戴传感
tldr: 可穿戴设备产生的生理信号多样性高且带内变异大，现有基础模型难以直接应用。本文提出NormWear，一个在多个公开数据集上预训练的多变量可穿戴传感基础模型，涵盖PPG、ECG、EEG、GSR和IMU。通过自监督预训练，它提取可泛化的波形表示，并在多个下游任务（如健康监测）中展现出优于专用模型的适应性和准确率。工作推动了生理信号基础模型的发展。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1675, \"height\": 769, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1689, \"height\": 945, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1695, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1658, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1610, \"height\": 811, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1626, \"height\": 1260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 972, \"height\": 238, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 746, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 555, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1681, \"height\": 1006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1394, \"height\": 754, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1379, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1391, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1890, \"height\": 2192, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1891, \"height\": 2181, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 918, \"height\": 940, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 730, \"height\": 991, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1677, \"height\": 1235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1688, \"height\": 590, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 821, \"height\": 785, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1724, \"height\": 1297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 456, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1730, \"height\": 1149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1739, \"height\": 1153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1762, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1762, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1725, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 763, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1216, \"height\": 370, \"label\": \"Table\"}]"
motivation: 可穿戴生理信号模式多变且频率带各异，需要具备泛化能力的基础模型来适应不同传感配置。
method: 提出NormWear基础模型，在包含PPG、ECG、EEG等信号的多元数据集上进行自监督预训练，学习通用表示。
result: 在多个下游任务中，NormWear的嵌入特征优于任务特定的端到端模型，验证了其泛化能力。
conclusion: NormWear证明了生理信号基础模型的可行性，为可穿戴健康分析提供了统一的特征提取器。
---

## Abstract
Time-series foundation models excel at tasks like forecasting across diverse data types by leveraging informative waveform representations. Wearable sensing data, however, pose unique challenges due to their variability in patterns and frequency bands, especially for healthcare-related outcomes. The main obstacle lies in crafting generalizable representations that adapt efficiently across heterogeneous sensing configurations and applications. To address this, we propose NormWear, a foundation model designed to extract generalized and informative representations from wearable sensing data. NormWear is pretrained on a diverse set of physiological signals, including PPG, ECG, EEG, GSR, and IMU, from various public datasets. For evaluation, we benchmark its performance across 11 public wearable sensing datasets, spanning 18 applications in mental health, body state inference, biomarker estimation, and disease risk evaluation, demonstrating superior performance compared to competitive baselines. Additionally, using a novel representation-alignment-match method, we align physiological signal embeddings with text embeddings, enabling zero-shot inference for unseen wearable signal-based health applications.

---

## 论文详细总结（自动生成）

## 论文中文总结

### 1. 核心问题与整体含义
**研究动机**：可穿戴设备采集的生理信号（PPG、ECG、EEG、GSR、IMU等）模式多样、频段各异，现有时间序列基础模型（如Chronos、TF-C、CLAP）要么依赖固定传感器类型，要么仅支持单变量输入，无法有效处理多变量、异构的穿戴信号，也难以适应不同的传感配置和应用场景。

**整体含义**：本文提出 **NormWear**，旨在构建首个专为可穿戴传感设计的基础模型，通过自监督预训练学习通用、可迁移的生理信号表示，并在身心健康状态推断、疾病风险评估、生命体征估计等广泛下游任务中验证其泛化能力，同时首次实现穿戴信号的零样本推理。

### 2. 方法论
**核心思想**：基于掩码自编码器（MAE）框架，采用**重建式自监督学习**，通过连续小波变换（CWT）将各通道生理信号转换为多尺度时频谱图，再进行随机掩码和重建，迫使模型学习鲁棒的波形表示。

**关键技术细节**：
- **令牌化**：对每个信号通道计算原始序列及其一、二阶导数，分别做CWT（Mexican Hat小波，尺度1~64），得到三通道RGB-like scalogram，再切分为非重叠 patches（类似ViT）。
- **架构**：
  - 卷积投影层 + 12层Transformer编码器（每个编码器间插入[CLS]令牌）。
  - 通道感知融合层：采用**[CLS]-注意力融合**，将各通道[CLS]令牌拼接后做自注意力，再与对应patch令牌拼接，实现跨通道信息交互。
  - 轻量解码器：2层Transformer + 线性/卷积层，重建原始信号。
- **掩码策略**：同时沿时间轴和尺度轴进行结构化掩码（掩码率分别为0.6和0.5），总掩码率约80%。
- **零样本推理**：提出**MSiTF（记忆流激发时序融合）** 模块，包含三个评分：
  - **相关性分数**：查询句子嵌入与各时间步patch嵌入的交叉注意力。
  - **新近性分数**：指数衰减，使近期时间步权重更高。
  - **重要性分数**：用Gumbel-Softmax学习二进制门控，决定保留哪些patch。
  - 三分数加权求和得到融合向量，再经变分推断（似然参数采样）与文本句子嵌入对齐。
- **损失函数**（公式2）：曼哈顿距离 + 余弦相似度的加权和，兼顾幅度和方向对齐。
- **数据增强**（算法1）：随机从两个序列中交换片段，扩展10倍。

### 3. 实验设计
**数据集**：
- **预训练**：9个公开数据集（PPG-DaLiA、Cuff-Less-BP、Auditory-EEG等），共约230,962个多变量片段（4,294小时），经增强至2,576,418段（14,943小时）。覆盖PPG、ECG、EEG、GSR、PCG、IMU。
- **下游评估**：11个未见数据集，18个任务，分四类：
  - 状态识别（WESAD、UCI-HAR、DriverFatigue）
  - 脑电任务（Epilepsy、GAMEEMO）
  - 疾病风险评估（ECG-Abnormal、PPG-BP、PhysioNet EMG）
  - 生命体征估计（Noninvasive-BP、PPG-Hgb、Fetal-fPCG）

**基准方法**：
- **统计方法**（手工特征+线性分类器）
- **Chronos**（SoTA时间序列预测模型，基于LLM）
- **CLAP**（SoTA谱图建模，音频-文本对齐）
- **TF-C**（SoTA自监督时间-频率一致性）

**评估方式**：线性探针（logistic回归/岭回归），主要指标AUC ROC（分类）、相对精度（回归）。还评估了零样本性能。

### 4. 资源与算力
- **预训练超参数**：45,000步，batch size 256，学习率1e-3，AdamW优化器，使用12层编码器+6层融合层+2层解码器。
- **硬件信息**：附录D中提及推理测试使用NVIDIA RTX 3090（0.18秒）、Jetson Nano 4GB（34.87秒），但**未明确说明预训练时使用的GPU数量及总耗时**。

### 5. 实验数量与充分性
- **实验量**：共执行18个下游任务（11个数据集）的线性探针评估，2组零样本评估（含消融），以及3组主要消融研究（融合方案、掩码策略、输入表示），加上数据规模缩放实验和特征可视化。
- **统计检验**：进行了置换检验（p<0.01）、Friedman检验（p<0.001）、Conover事后检验，证明NormWear显著优于基线。临界差异图也支持这一结论。
- **充分性**：实验覆盖多类型任务、多种传感器组合、多种评估范式（线性探针、零样本、消融），并检查了人口统计信息的混淆影响（附录表A.7），总体设计客观、公平。但**缺乏全参数微调实验**（仅线性探针），且未在真实临床部署中测试。

### 6. 主要结论与发现
- NormWear在18个下游任务的平均AUC ROC上优于所有基线：比TF-C高3.9%、比CLAP高5.3%、比Chronos高6.1%、比统计方法高5.2%。
- 在疾病风险评估任务中提升最显著（+4.1% vs TF-C），活动识别和EEG任务也均有大幅提升。
- 零样本性能（MSiTF）显著优于CLAP（宏平均AUC 60.1% vs 51.2%），且消融表明重要性分数和文本增强都有贡献。
- 模型遵循缩放定律：预训练数据从37k增至2.5M样本时，性能持续提升。
- 特征可视化显示，模型能区分不同传感器类型，且深层特征复杂度递增，体现了有意义的学习。

### 7. 优点
- **首创性**：第一个专门为可穿戴多变量生理信号设计的基础模型，可处理任意数量/类型的传感器输入。
- **方法创新**：CWT多尺度令牌化使得预处理统一；[CLS]-注意力融合高效捕获跨通道关系；MSiTF模块首次实现穿戴信号的零样本推理。
- **实验充分**：涵盖18个任务、13个数据集、多种基线，且进行了严格的统计检验和消融研究，代码、数据、模型将开源。
- **可视化分析**：t-SNE和动力学复杂度分析有助于理解模型行为，增加可解释性。

### 8. 不足与局限
- **数据规模相对有限**：预训练数据仅约2.5M段（15k小时），远小于CV/NLP领域的十亿级数据，可能限制表示能力的上限。
- **零样本性能仍较低**：尽管优于CLAP，但远低于线性探针（宏平均60.1% vs 84.4%），说明零样本泛化仍有很大提升空间。
- **缺少全参数微调对比**：仅用线性探针，未比较端到端微调的效果，可能低估/高估基础模型的可迁移性。
- **边缘部署延迟较高**：Jetson Nano上推理需35秒，不满足实时监测需求。
- **未在真实临床场景验证**：所有实验均在公开数据集上进行，实际噪声、传感器漂移、数据缺失等挑战未覆盖。
- **文本生成依赖GPT-3.5**：用于数据增强的句模板可能引入语言偏差，且未检测对非英语任务的影响。

（完）
