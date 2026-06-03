---
title: "Neural decoding from stereotactic EEG: accounting for electrode variability across subjects"
title_zh: 从立体脑电图进行神经解码：解决跨被试电极变异性问题
authors: "Georgios Mentzelopoulos, Evangelos Chatzipantazis, Ashwin G Ramayya, Michelle Hedlund, Vivek Buch, Kostas Daniilidis, Konrad Kording, Flavia Vitale"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=LR1nnsD7H0"
tags: ["query:pbci-load"]
score: 6.0
evidence: 跨被试sEEG解码框架，适用于被动BCI应用
tldr: 该论文针对立体脑电图（sEEG）中电极位置个体差异大的问题，提出了seegnificant框架，通过令牌化神经活动和跨被试架构实现行为解码。该方法可直接应用于被动BCI中的认知负荷评估，因为其能够处理多被试的异质性电极布局，且使用深度学习方法。实验表明该方法在不同被试间具有良好的泛化性能，为基于EEG的被动BCI提供了可迁移的深度学习方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1309, \"height\": 768, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1396, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 897, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 918, \"height\": 350, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 908, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 876, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-lr1nnsd7h0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 548, \"height\": 423, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-lr1nnsd7h0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 733, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lr1nnsd7h0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 801, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-lr1nnsd7h0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 640, \"height\": 266, \"label\": \"Table\"}]"
motivation: sEEG数据中电极数量与位置因人而异，难以整合多被试数据以扩展模型规模。
method: 提出seegnificant框架，将神经活动令牌化，并通过跨被试架构实现统一解码。
result: 在多个行为解码任务上跨被试泛化性能优于基线。
conclusion: 该框架为sEEG跨被试解码提供了有效方案，可扩展至被动BCI应用。
---

## Abstract
Deep learning based neural decoding from stereotactic electroencephalography (sEEG) would likely benefit from scaling up both dataset and model size. To achieve this, combining data across multiple subjects is crucial. However, in sEEG cohorts, each subject has a variable number of electrodes placed at distinct locations in their brain, solely based on clinical needs. Such heterogeneity in electrode number/placement poses a significant challenge for data integration, since there is no clear correspondence of the neural activity recorded at distinct sites between individuals. Here we introduce seegnificant: a training framework and architecture that can be used to decode behavior across subjects using sEEG data. We tokenize the neural activity within electrodes using convolutions and extract long-term temporal dependencies between tokens using self-attention in the time dimension. The 3D location of each electrode is then mixed with the tokens, followed by another self-attention in the electrode dimension to extract effective spatiotemporal neural representations. Subject-specific heads are then used for downstream decoding tasks. Using this approach, we construct a multi-subject model trained on the combined data from 21 subjects performing a behavioral task. We demonstrate that our model is able to decode the trial-wise response time of the subjects during the behavioral task solely from neural data. We also show that the neural representations learned by pretraining our model across individuals can be transferred in a few-shot manner to new subjects. This work introduces a scalable approach towards sEEG data integration for multi-subject model training, paving the way for cross-subject generalization for sEEG decoding.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：基于立体脑电图（sEEG）的神经解码有望通过扩大数据集和模型规模来提升性能，这就要求整合多个被试的数据。但在临床实践中，每个被试的电极数量及植入位置完全由临床需求决定，导致个体间电极布局高度异质，无法直接建立神经活动的对应关系。现有工作大多局限于单被试模型，既无法扩展也难以泛化。
- **整体含义**：本文旨在提出一个能有效融合多被试sEEG数据、训练统一神经解码模型的框架，克服电极异质性带来的数据整合难题，为sEEG跨被试行为解码奠定基础。

## 2. 论文提出的方法论

- **核心思想**：采用“共享主干+被试特定头”的架构，将各电极的神经活动先分别token化，再通过时间维度和电极维度交替的自注意力机制捕捉时空依赖，并利用MNI坐标空间位置编码注入电极位置信息，最终由被试专用的浅层网络完成行为解码。
- **关键技术细节**：
    1. **电极选择**：基于高γ频带（70-150 Hz）的调制显著性筛选反应相关电极，计算信噪比（SNR = σ²(Median_task)/σ²(Median_baseline)）并通过bootstrap检验（FDR校正，p<0.05）确定。
    2. **卷积tokenizer**：对每个电极单独进行1D时间卷积（K个核），生成维度为E×T×K的张量，其中E为电极数、T为时间点、K为特征数。
    3. **时间自注意力**：沿电极维并行，对每个电极的T个token进行标准Transformer自注意力（含层归一化、前馈网络），捕获电极内长程时间依赖。
    4. **空间位置编码**：利用径向基函数（RBF）对电极的MNI三坐标（x,y,z）进行编码，每个坐标用n个中心μ_i和m个方差σ²_j的高斯函数值拼接，经线性投影至K维后与时间自注意力输出相加。
    5. **空间自注意力**：沿时间维并行，对每个时间点的E个token进行自注意力，捕获电极间依赖。
    6. **特征压缩与解码**：将最终潜伏态展平后通过一个前馈网络投影至低维表示F∈R^d，再经各被试专属的线性头回归反应时。
- **公式/算法流程**（文字说明）：输入sEEG信号 → 卷积tokenizer得到ze,i = xe ∗ ki → 批归一化+池化得z∈R^(E×T×K) → 对每个电极做时间自注意力 → 叠加空间位置编码 → 对每个时间点做空间自注意力 → 展平+MLP得全局表示F → 对不同被试分别用任务头输出反应时。

## 3. 实验设计

- **数据集**：21名药物难治性癫痫患者，共29个记录session，执行颜色变化检测任务（视觉刺激后变绿，被试按键反应）。共3600+ trial，100 电极-小时。每位被试电极数量3-28个，位置因人而异。
- **Benchmark**：在1816个session的测试集上评估反应时解码的R²和RMSE。
- **对比方法**：
    - 传统非深度学习：Wiener Filter、Ridge Regression、Lasso Regression、XGBoost。
    - 深度学习：MLP（4层）、CNN+MLP（1层CNN+3层MLP）。
- **主要实验组**：
    1. 单被试模型（21个被试分别训练）。
    2. 多被试联合模型（所有数据一起训练）。
    3. 多被试模型微调至单个被试。
    4. 留一法跨被试迁移学习（在20个被试上预训练，微调至第21个被试）。
    5. 消融实验：分别去掉空间注意力、时间注意力、位置编码、被试特定头等组件；以及对比2D注意力变体、不同位置编码方案（Vaswani、Fourier等）。

## 4. 资源与算力

- **硬件**：AMD EPYC 7502P 32核CPU + 1块 Nvidia A40 GPU（44.99 GiB显存），内存未明确但GPU显存占约8 GiB。
- **训练时间**：单被试模型平均约5分钟，多被试模型约1小时，消融实验使用3次数据分割（文中提及部分实验用5次，消融用3次）。
- **推理时间**：在两种机器（服务器CPU、GPU；笔记本CPU、GPU）上均低于10 ms，满足实时需求。

## 5. 实验数量与充分性

- **数量**：共训练了21个单被试模型、1个全数据多被试模型、21个留一法预训练模型、每个留一法再微调至对应被试；消融实验对6个组件分别移除并测试，还对比了2D注意力和不同位置编码；基线方法各训练了多组超参数。总体实验组数较多。
- **充分性**：大部分实验结果报告了多次数据分割的平均值和标准误（单被试、多被试等多用5次，消融用3次），结果统计量明确。但留一法实验只用了1次数据分割（因计算量大），且未报告统计显著性检验（仅做了位置编码有无的Wilcoxon检验）。实验覆盖了单一任务（反应时），未涉及多任务或自监督预训练，但已能支撑主要结论。总体实验设计比较客观、公平，但可进一步扩展。

## 6. 论文的主要结论与发现

- 多被试联合训练相比单被试模型显著提升解码性能：平均被试内R²从0.30（单被试）提升至0.39（多被试），再经微调至0.41，提升ΔR²≈0.11。
- 留一法迁移学习（预训练+微调）接近多被试模型性能（ΔR²=-0.01），且大幅降低计算成本，适合临床小样本场景。
- 消融实验表明被试特定头是最关键组件（去除后R²下降0.18），空间注意力（下降0.10）次之，时间注意力和位置编码贡献较小。
- 模型推理时间<10 ms，具备实时应用潜力。
- 所提出的架构优于所有基线方法（包括传统和深度学习），平均R²提升≥0.03（单被试时），≥0.12（多被试时）。

## 7. 优点

- **创新性地解决电极异质性问题**：通过逐电极1D卷积tokenizer、空间位置编码和电极维自注意力，使得可变数量/位置的电极可以统一输入模型，实现跨被试数据融合。
- **共享表示学习**：共享主干能够提取跨被试通用的神经表征，被试特定头则拟合个体差异，兼顾共性与个性。
- **强大的可迁移性**：预训练模型可快速微调到新被试，且性能几乎不损失，极大降低了新被试的数据需求。
- **实时可行**：推理速度快，适用于闭环BCI应用。
- **实验设计严谨**：进行了多维度对比（单vs多被试、微调、迁移、消融、基线），结果稳健。

## 8. 不足与局限

- **任务单一**：仅针对反应时解码一种行为指标，未验证在其他行为（如运动想象、语音解码）上的泛化能力。
- **位置编码增益有限**：消融实验显示空间位置编码仅带来ΔR²=0.02的微弱提升，且统计上不显著。未来需探索更有效的空间表征方法（如利用全脑MRI图谱）。
- **依赖高伽马频段选择电极**：仅使用高伽马调制显著的电极，可能忽略了其他频段的信息，且选择过程依赖阈值，存在一定偏差。
- **未利用无监督数据**：sEEG连续记录多数天，但本工作仅使用有标签的行为实验数据，未尝试自监督预训练等方法来利用大量未标记数据。
- **实验数据集规模仍有限**：21名被试、3600+ trial在临床sEEG研究中算较大，但相比其他领域（如自然语言处理）仍较小，且全部来自同一脑疾病人群（癫痫患者），可能影响泛化性。
- **计算资源描述不够详细**：仅给出GPU型号和显存，未说明CPU内存等，且训练时间仅给出大致范围。

（完）
