---
title: Are Large Brainwave Foundation Models Capable Yet ? Insights from Fine-Tuning
title_zh: 大型脑波基础模型是否已具备能力？来自微调的见解
authors: "Na Lee, Konstantinos Barmpas, Yannis Panagakis, Dimitrios Adamos, Nikolaos Laskaris, Stefanos Zafeiriou"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=J5SbLoq7Uv"
tags: ["query:pbci-load"]
score: 7.0
evidence: 评估脑波基础模型在BCI任务上的表现
tldr: "尽管脑波基础模型在AI领域取得成功，但针对BCI任务的能力尚不明确。本文通过系统微调实验，在记忆和睡眠分类等多个BCI基准上评估了当前最先进的大型脑波基础模型（LBMs），发现它们仅比传统深度架构有0.5%的微小提升，却需要数百万参数量，质疑了其在BCI中的效率与适用性，并提出了未来方向。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 707, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 700, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 884, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 816, \"height\": 622, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1778, \"height\": 424, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 870, \"height\": 355, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1592, \"height\": 673, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1780, \"height\": 812, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1164, \"height\": 280, \"label\": \"Table\"}]"
motivation: 大型脑波基础模型在BCI任务上的能力缺乏系统评估。
method: 在多个BCI基准任务上对当前LBMs进行微调与全面比较。
result: "LBMs相比传统模型仅提升0.5%，但参数量大，效率存疑。"
conclusion: 当前LBMs在BCI任务上效率不高，需改进以适应实际应用。
---

## Abstract
Foundation Models have demonstrated significant success across various domains in Artificial Intelligence (AI), yet their capabilities for brainwave modeling remain unclear. In this paper, we comprehensively evaluate current Large Brainwave Foundation Models (LBMs) through systematic fine-tuning experiments across multiple Brain-Computer Interface (BCI) benchmark tasks, including memory tasks and sleep stage classification. Our extensive analysis shows that state-of-the-art LBMs achieve only marginal improvements (0.5\%) over traditional deep architectures while requiring significantly more parameters (millions vs thousands), raising important questions about their efficiency and applicability in BCI contexts. Moreover, through detailed ablation studies and Low-Rank Adaptation (LoRA), we significantly reduce trainable parameters without performance degradation, while demonstrating that architectural and training inefficiencies limit LBMs' current capabilities. Our experiments span both full model fine-tuning and parameter-efficient adaptation techniques, providing insights into optimal training strategies for BCI applications. We pioneer the application of LoRA to LBMs, revealing that performance benefits generally emerge when adapting multiple neural network components simultaneously. These findings highlight the critical need for domain-specific development strategies to advance LBMs, suggesting that current architectures may require  redesign to fully leverage the potential of foundation models in brainwave analysis.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究动机**：尽管Foundation Models在NLP和CV等领域取得了巨大成功，但在脑波建模（brainwave modeling）领域，尤其是用于脑机接口（BCI）的大规模脑波基础模型（Large Brainwave Foundation Models, LBMs）的实际能力尚不明确。作者希望通过系统性微调实验，评估当前最先进的LBMs（LaBraM和NeuroGPT）在多种BCI下游任务上的表现，并与传统深度学习方法进行公平对比。
- **核心问题**：LBMs是否真正为BCI任务带来了效率或性能上的显著优势？现有的预训练和架构设计是否存在根本性缺陷？
- **整体含义**：研究发现，当前LBMs仅比传统小型模型（如EEGNet）有极微小（约0.5%~1.2%）的平均准确率提升，却需要数百万甚至数千万的可训练参数，这严重质疑了其在实际BCI应用中的效率与适用性。同时，开源模型的预训练策略和架构设计可能存在低效问题，亟需领域特定的改进。

## 2. 论文提出的方法论

### 2.1 核心思想
- 通过对两个代表性LBM（LaBraM和NeuroGPT）进行全模型微调、冻结骨干微调以及参数高效微调（LoRA）的全面对比，系统揭示LBMs在BCI任务上的真实能力与局限性。
- 引入Low-Rank Adaptation（LoRA）到脑波领域，探索其在减少可训练参数的同时保持性能的潜力，并通过消融研究分析不同网络组件（注意力、全连接、卷积层）对下游任务的贡献。

### 2.2 关键技术细节
- **数据预处理**：针对每个模型使用其预训练时采用的采样率、滤波器和通道映射规则。例如LaBraM使用200Hz、0.5-45Hz带通、50/60/100Hz陷波；NeuroGPT使用250Hz、0.05-100Hz带通。对缺失通道采用就近或置零处理，所有数据集均进行共平均参考（CAR）。
- **微调设置**：所有模型（包括传统基线）均训练20个epoch，采用10折subject-independent交叉验证（按受试者划分），添加合适的分类头（LaBraM为线性+dropout；NeuroGPT为三层MLP+dropout+ELU）。
- **LoRA实现**：对每个目标模块的权重矩阵W，引入低秩矩阵A和B（即ΔW=AB），秩r可调（实验中取1,2,4,8,16）。不对偏置项微调。对注意力模块，将Q、K、V视为单一矩阵W_qkv，输出投影冻结。对卷积和全连接层也应用LoRA。缩放因子α固定为8。
- **公式**：W' = W + ΔW = W + AB，其中A∈R^(d×r), B∈R^(r×k)，r << min(d,k)。可训练参数从d×k减少为r×(d+k)。

### 2.3 算法流程（文字说明）
1. 收集并预处理五个BCI基准数据集，使其符合各模型的输入格式。
2. 对传统基线（EEGNet、EEGInception）从零训练（20 epoch，10-fold CV）。
3. 对LaBraM、NeuroGPT（全模型和编码器模型）进行三种策略的微调：
   - 全模型微调（所有参数更新，包括分类头）。
   - 冻结骨干，仅训练分类头。
   - 使用LoRA（不同秩、不同层组合）微调。
4. 计算所有设置下的分类准确率、可训练参数数量，并进行配对t检验（p<0.05视为显著）。
5. 进一步针对最佳模型（LaBraM）探索LoRA dropout的影响。

## 3. 实验设计

### 3.1 数据集与任务场景
- **5个BCI基准任务**：
  - **Motor**（High Gamma数据集）：运动想象分类
  - **ERP**（Korean University数据集）：事件相关电位分类
  - **Memory**（Pavlov et al.工作记忆数据集）：工作记忆任务
  - **Sleep**（Sleep-EDF数据集）：睡眠阶段分类
  - **Eyes**（Physionet Motor数据集）：睁眼/闭眼分类
- 这些任务涵盖不同脑机范式，且数据集被选为“人工伪迹最少”以降低假阳性。

### 3.2 对比方法
- **传统深度学习基线**：
  - EEGNet（参数2,394）
  - EEGInception（参数22,366）
- **LBMs**：
  - LaBraM base（参数5,854,288）
  - NeuroGPT full model（参数78,536,146）
  - NeuroGPT encoder only（参数717,958）

### 3.3 实验设置细节
- 所有模型均使用相同epoch数（20）和交叉验证策略（10折subject-independent）。
- 分类头结构针对各模型给出（见论文Table 4）。
- 对LoRA实验进行了多种秩（1~16）和多种层组合（注意力/全连接/卷积，单独或组合）的消融。
- 额外实验：在LaBraM上引入LoRA dropout（概率0.5）进行对比。

## 4. 资源与算力

- **文中未明确说明使用的GPU型号、数量或具体训练时长**。仅提到所有模型训练20个epoch，且使用10折交叉验证（需多次运行）。对于LBMs（数百万参数）的微调，计算资源需求较大，但论文未提供量化信息。
- 在LoRA实验中，由于只更新少量低秩矩阵，计算开销相对全微调更小，但具体硬件平台未知。

## 5. 实验数量与充分性

### 5.1 实验数量
- **核心对比实验**：3种传统基线 vs 3种LBM配置（全微调）→ 5个数据集 → 15个主要结果（Table 1）。
- **冻结骨干实验**：3种LBM配置 × 5个数据集 = 15个结果（Table 3）。
- **LoRA秩实验**：3种LBM配置 × 5种秩（1,2,4,8,16）× 5个数据集（但部分结果只汇报了4个任务，Motor未汇报）→ 约3×5×4=60个结果（Table 5）。
- **LoRA层组合消融**：3种LBM配置 × 6种层组合 × 5个数据集 → 90个结果（Table 6）。
- **LoRA dropout实验**：仅在LaBraM上 × 5种秩 × 5个数据集 = 25个结果（Table 7）。
- **统计检验**：配对t检验（Table 2）比较EEGInception与各LBM的差异。

### 5.2 充分性与公平性评价
- **充分性**：实验覆盖了全微调、冻结、参数高效微调、不同秩、不同层组合、dropout等多个维度，消融系统全面。但缺少与其他PEFT方法（如Adapter、Prefix Tuning）的对比，也未探索更大epoch或不同学习率的影响。
- **客观性**：使用subject-independent 10-fold CV保证泛化，报告均值±标准差，并进行统计显著性检验（p值）。数据集选择避免伪迹，降低虚假性能。
- **公平性**：所有模型相同训练epoch数，分类头结构按模型规范设计，但未针对传统模型进行超参数调优（可能对基线不利）。另外，LBM的预训练数据中包含部分下游任务的数据（如Motor、ERP、Sleep、Eyes的类似范式），这可能导致在评估中受益，而Memory任务（未见类似数据）则表现更差，体现了公平性。

## 6. 论文的主要结论与发现

1. **LBMs优势微弱**：在相同epoch数下，当前最先进的LBMs（LaBraM、NeuroGPT）平均性能仅比传统小型深度学习模型（EEGNet/EEGInception）提升约0.5%（具体数值：EEGNet平均0.731，EEGInception 0.733，LaBraM 0.742，NeuroGPT full 0.736，encoder 0.745），但参数量增加数千倍。
2. **冻结骨干失败**：仅训练分类头时，LBMs性能远低于传统基线（低8-10%），说明模型必须整体微调才能发挥作用，这也凸显了参数高效微调（如LoRA）的必需性。
3. **LoRA可大幅压缩参数**：应用LoRA后，LBMs的可训练参数减少90%以上（如LaBraM从5.85M减至约34K），而性能没有下降，甚至在某些任务上略有提升。
4. **LoRA最佳实践**：性能提升通常出现在同时适配多个网络组件（如卷积+全连接，或注意力+卷积）时，单独适配某一层效果较差；且注意力层单独的贡献不如预期，提示当前LBMs中时间编码层可能比注意力层更关键。
5. **架构与训练效率不足**：当前LBMs的架构和预训练策略可能并未针对脑波信号特点进行优化，直接照搬NLP/CV的方法，导致效率低下。

## 7. 优点

- **首次系统评估**：填补了LBM在BCI任务上缺乏全面基准测试的空白，为社区提供了客观的参考。
- **首次将LoRA引入脑波基础模型**：开创性地探索了参数高效微调在脑波领域的应用，并给出了针对不同层组合的详细指南。
- **严谨的实验方法论**：采用subject-independent 10-fold CV、统计显著性检验、多种消融（秩、层类型、dropout），结果可信度高。
- **揭示深层问题**：通过分析冻结和LoRA消融，指出了当前LBM架构可能过分依赖注意力机制而忽略时间编码的局限性，为未来模型设计提供了方向。
- **强调领域特定性**：明确呼吁开发领域特定的预训练策略（如脑启发掩码、多模态EEG特征），而非简单迁移其他领域方法。

## 8. 不足与局限

- **计算资源信息缺失**：未提供GPU型号、数量、训练耗时等，不利于复现和资源估算。
- **仅评估两个LBM**：没有覆盖更多脑波基础模型（如NeuroLM、CBraMod等），结论可能局限于特定架构。
- **分类任务单一**：只评估了分类准确率，未涉及生成任务（如脑信号重建、序列预测）或回归任务，而生成能力是LBM的重要卖点。
- **超参数调优不足**：对传统基线未进行超参数搜索，可能导致基线性能未达最优；LoRA的秩和dropout参数也可能不是最优组合。
- **预训练数据泄露风险**：LBM的预训练数据中包含与测试任务相似的数据分布（如Sleep-EDF可能被用于预训练？论文未明确说明），可能高估LBM的泛化能力。Memory任务上表现更差印证了这一点。
- **训练epoch局限**：仅20 epoch对大型模型可能不够，尤其对LoRA来说，更多epoch可能带来更好结果。缺少早停或收敛分析。
- **缺乏与其他PEFT方法对比**：如Adapter、Prefix Tuning、BitFit等，未验证LoRA是否是最优选择。
- **未探讨模型规模缩放规律**：没有分析不同参数规模的LBM性能变化，未能说明“更大模型是否带来更大收益”。

（完）
