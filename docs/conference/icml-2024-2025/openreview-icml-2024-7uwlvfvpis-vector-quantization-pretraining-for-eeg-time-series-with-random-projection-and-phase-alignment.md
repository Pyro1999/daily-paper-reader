---
title: Vector Quantization Pretraining for EEG Time Series with Random Projection and Phase Alignment
title_zh: 基于随机投影和相位对齐的EEG时间序列向量量化预训练
authors: "Haokun GUI, Xiucheng Li, Xinyang Chen"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=7uwLvFvpis"
tags: ["query:pbci-load"]
score: 7.0
evidence: EEG自监督预训练方法
tldr: 针对EEG时间序列分析，本文提出VQ-MTM自监督学习模型，核心包括随机投影量化和傅里叶相位对齐模块，能生成类似单词的语义单元，提供鲁棒一致的学习信号；模型复杂度低，易于扩展到大规模数据。在五个真实数据集上的实验验证了其在EEG分类等任务中的有效性。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-7uwlvfvpis/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1413, \"height\": 784, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-7uwlvfvpis/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-7uwlvfvpis/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 862, \"height\": 241, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-7uwlvfvpis/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1756, \"height\": 713, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-7uwlvfvpis/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1596, \"height\": 522, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1075, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 795, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 767, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1431, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1010, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 885, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 891, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1800, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 927, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1225, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 931, \"height\": 372, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1777, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 786, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1003, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 632, \"height\": 738, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-7uwlvfvpis/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 630, \"height\": 736, \"label\": \"Table\"}]"
motivation: 现有EEG自监督方法缺乏良好定义的语义单元和噪声鲁棒性。
method: 提出VQ-MTM，包含随机投影量化和相位对齐模块，采用掩码时间序列建模进行预训练。
result: 在五个真实数据集上，VQ-MTM在EEG分类等任务中取得优异性能。
conclusion: VQ-MTM是一种有效的EEG预训练方法，可推广到多种EEG分析任务。
---

## Abstract
In this paper, we propose a BERT-style self-supervised learning model, VQ-MTM (Vector Quantization Masked Time-Series Modeling), for the EEG time series data analysis. At its core, VQ-MTM comprises a theoretically grounded random-projection quantization module and a phase-aligning module guided by the Time-Phase-Shift Equivariance of Fourier Transform, the two modules can generate well-defined semantic units (akin to words in natural language) for the corrupted and periodic time series, thus offering robust and consistent learning signals for the EEG self-supervised learning. VQ-MTM also owns low model complexity and can easily adapt to large-scale datasets. We conduct experiments on five real-world datasets including two large-scale datasets to verify the efficacy of our proposed model, the experiment results show that VQ-MTM is able to consistently surpass the existing methods by large margins on both seizure detection and classification tasks. Our code is available at https://github.com/HaokunGUI/VQ_MTM.

---

## 论文详细总结（自动生成）

# 论文《Vector Quantization Pretraining for EEG Time Series with Random Projection and Phase Alignment》详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：EEG（脑电图）时间序列数据在医疗诊断中具有重要意义（如癫痫检测与分类），但现有自监督学习方法面临三大挑战：
  1. EEG信号缺乏类似自然语言中“单词”的明确定义语义单元，难以直接应用BERT式的掩码预测。
  2. EEG信号常因采集过程噪声、伪影而损坏，直接重构被掩码片段会导致训练不稳定且学习到噪声特征。
  3. EEG作为生理信号具有固有的周期性，但现有方法未充分利用这一特性，难以处理由时间偏移引起的模式变体。
- **背景**：自监督学习（如MAE、BERT）在NLP和CV中成功，但在EEG分析中进展有限；已有方法如DCRNN、SimMTM等存在扩展性差或对噪声敏感等问题。
- **目标**：设计一种能够生成鲁棒、一致语义单元的BERT式自监督预训练方法，用于EEG时间序列分析，尤其是癫痫检测和分类任务。

## 2. 论文提出的方法论

### 核心思想
提出 **VQ-MTM（Vector Quantization Masked Time-Series Modeling）**，通过将EEG信号拆分为片段，并利用随机投影量化和相位对齐模块将变体映射到同一个语义词（代码本中的索引），从而提供一致的自监督学习目标。模型采用掩码时间序列建模（类似BERT）进行预训练。

### 关键技术细节

- **预处理与通道分离**：将多通道EEG信号按时间划分为不重叠的补丁（patch size=250），并对每个通道独立编码，避免异质通道融合带来的困难。
- **随机投影量化器**：
  - 使用随机初始化的投影矩阵 \( A \in \mathbb{R}^{D\times N} \) 和代码本 \( C \in \mathbb{R}^{D\times K} \)（两者固定不更新）。
  - 对每个补丁 \( z \)，计算其投影 \( Az \) 并归一化，再与代码本中每个归一化向量 \( c_k \) 计算余弦相似度（等价于内积），取最相似的索引作为伪标签。
  - 理论依据：Johnson-Lindenstrauss引理的推广（Theorem 3.1），保证内积近似保留，从而噪声下的相似补丁很大概率获得相同伪标签。
- **相位对齐模块**：
  - 利用傅里叶变换的时间-相位偏移等变性（Theorem 3.2）：时间域的平移对应相位域线性偏移。
  - 对输入补丁 \( z \) 做DFT，通过减去偏移项 \( k\cdot\arg(\hat{z}_1) \) 对齐每个频率分量的相位，再IDFT重建对齐后的信号。
  - 该模块确保由微小时间偏移产生的变体被映射到相同的语义单元。
- **自监督训练损失**：
  - 采用BERT式掩码：随机掩码30%的补丁，用可学习向量替代，Transformer编码器输出上下文表示，通过Softmax预测被掩码位置的伪标签，最大化对数似然。
- **微调阶段**：预训练的编码器后接1×1点卷积融合通道特征，再通过前馈网络输出分类结果。

### 公式与算法流程（文字说明）
1. 输入多通道EEG \( X \in \mathbb{R}^{M\times T} \)。
2. 将每个通道独立分割为L个补丁 \( Z = [z_0,\dots,z_{L-1}], z_i\in\mathbb{R}^N \)。
3. 对每个补丁 \( z_i \)：
   - 通过相位对齐模块得到 \( z_i^{\text{aligned}} \)。
   - 通过随机投影量化器得到伪标签 \( y_i = \arg\max_k \langle c_k/\|c_k\|_2, Az_i^{\text{aligned}}/\|Az_i^{\text{aligned}}\|_2 \rangle \)。
4. 掩码后输入Transformer编码器，输出上下文表示 \( z_i^c \)。
5. 损失：\( \max \sum_{m}\sum_{i\in\mathcal{M}} \log p(y_{m,i} | z_{m,i}^c) \)，其中 \( \mathcal{M} \) 为掩码索引集。
6. 微调：提取[CLS]表示，点卷积融合通道，全连接分类。

## 3. 实验设计

### 数据集与场景
- **TUSZ v2.0.0**（79.4 GB）：最大的公开EEG癫痫数据集，包含癫痫检测（二分类）和癫痫分类（4类：CF、GN、AB、CT）任务。样本分为12秒和60秒片段。
- **TUAB v3.0.0**（58.6 GB）：EEG异常检测数据集，仅用于检测任务（12秒和60秒片段）。
- **额外数据集**（附录H）：UCR/UEA中的Epilepsy、ECG200、ECG5000（较小规模，用于验证通用性）。

### Benchmark与对比方法
- **基线方法**：DCRNN、TimesNet、PatchTST、MAE、SimMTM、BIOT（部分实验还对比了Informer、Autoformer、FEDformer、iTransformer）。
- **评估指标**：癫痫检测用AUROC；癫痫分类用Weighted F1-Score（因类别不平衡严重）。

### 实验设置
- 预处理：均匀采样19个通道，Z-Score归一化。
- 预训练：epoch=150（TUSZ）/100（TUAB），batch size=512，AdamW优化器，peak lr=2e-3，余弦退火。
- 微调：epoch=60，初始lr=1e-3，预训练部分lr=1e-4。

## 4. 资源与算力

- 论文明确说明：“All experiments are conducted on the NVIDIA RTX 4090 GPUs。”（第7页）
- **未明确说明**：使用的GPU数量、单卡还是多卡、具体训练时长（如每个epoch时间或总训练小时数）。文中仅提及batch size=512，但未给出具体计算资源规模。

## 5. 实验数量与充分性

- **主要实验**：表1（TUSZ检测与分类）、表2（TUAB检测）对比了多种基线，覆盖不同长度片段。
- **消融实验**：表3（通道分离有效性）、表4（相位对齐模块有效性）均基于TUSZ。
- **附加实验**：附录包含线性探针实验（表12）、小规模数据集对比（表13）、计算成本分析（表14、15）、代码本分布分析（图5）等。
- **公平性**：基线方法使用官方代码和推荐超参数，VQ-MTM采用固定随机投影和代码本，无需额外训练，对比透明。
- **充分性评价**：实验较为充分，涵盖两个大规模真实临床数据集和多个小数据集，验证了检测与分类两任务；消融实验验证了关键模块；但未在更多不同类型的时间序列任务（如预测、异常检测）上验证，仅在EEG/ECG生物信号领域。

## 6. 论文的主要结论与发现

- VQ-MTM在TUSZ和TUAB上均一致优于所有基线，尤其在60秒片段上提升显著（TUSZ检测AUROC 0.904 vs 0.834）。
- 相位对齐模块对分类任务提升更明显（Weighted F1提升21.30%），说明处理周期性信号的时移变体对提升语义一致性至关重要。
- 通道分离策略有效避免了异质通道融合带来的性能下降（表3）。
- 预训练能显著提升下游性能（表11），且线性探针评估也表明VQ-MTM学习到的表示质量最高。
- 模型复杂度低（参数量0.20M，FLOPs 0.12G），易于扩展至大规模数据。

## 7. 优点

1. **方法创新**：结合随机投影量化和相位对齐，首次在EEG自监督中生成类似单词的语义单元，有效处理噪声和周期性问题。
2. **理论支撑**：量化器有J-L引理推广（Theorem 3.1）保证内积近似；相位对齐有傅里叶时间-相位偏移等变性（Theorem 3.2）指导。
3. **高效且可扩展**：参数少、无额外可学习量化器，容易大规模训练。
4. **实验扎实**：在多个大规模临床数据集验证，消融实验清晰，与众多SOTA方法对比。

## 8. 不足与局限

1. **计算资源细节缺失**：未报告GPU数量、训练总时长，难以复现和比较效率。
2. **应用范围有限**：方法基于EEG/ECG的周期性假设，对非周期或非平稳时间序列可能不适用；相位对齐模块依赖傅里叶变换，对非周期信号可能无效。
3. **超参数敏感**：代码本大小K=1024、维度D=256等选择未进行详尽分析，可能并非最优。
4. **缺少更多下游任务验证**：仅在检测和分类任务上评估，未覆盖预测、异常检测等时间序列常见任务，通用性尚需进一步验证。
5. **基线覆盖不完整**：未与基于对比学习的EEG自监督方法（如COST、TS2Vec）直接比较，虽然它们主要针对一般时间序列。
6. **数据偏差风险**：TUSZ和TUAB来自单一医院（Temple University），可能无法代表全球人群的EEG分布。

（完）
