---
title: Canonical Correlation Analysis and Multi-Channel Cardiography Improve Artefact Cleaning in Heartbeat-Locked Analyses
title_zh: 典型相关分析与多通道心电描记术改善心跳锁定分析中的伪迹清理
authors: "Vidaurre, C., Azanova, M., Germanova, K., Greschke, E., Steinfath, T. P., Laufs, U., Uhe, T., Villringer, A., Nikulin, V."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738519v1.full.pdf"
tags: ["query:robust-eeg"]
score: 8.0
evidence: 提出基于CCA的多通道心电伪影去除方法用于脑电信号
tldr: 心脏伪迹干扰锁定心跳的脑电分析，传统单通道心电伪迹去除不充分。本文提出基于典型相关分析的多变量方法，结合15通道心电记录进行伪迹去除。在14名被试的脑电数据中，该方法在减少R峰伪迹和保持α功率方面优于独立成分分析。研究还发现少量通道组合即可达到接近全通道的性能，为多通道心脏伪迹去除提供可靠方案。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 834, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1670, \"height\": 897, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1642, \"height\": 1154, \"label\": \"Figure\"}]"
motivation: 传统心电伪迹去除方法未充分利用多通道心电信息，导致心跳锁定脑区分析中伪迹残留。
method: 提出基于典型相关分析的多变量伪迹去除方法，使用15通道心电同时记录，评估不同通道组合效果。
result: 典型相关分析在减少R峰伪迹和保持α功率上均优于独立成分分析；4-5个心前区加肢体/锁骨上电极性能接近全通道。
conclusion: 典型相关分析是多通道心脏伪迹去除的可靠方法，提供了通道选择的决策标准，但需在其他数据集中验证。
---

## 摘要
心脏伪迹对神经生理学分析造成问题，尤其是在心跳锁定脑响应中，神经活动和伪迹在时间上同时发生。传统的使用单通道心电图去除伪迹的方法不能完全捕捉心脏场的多维扩散。此外，即使记录了多个通道，也没有成熟的方法将它们整合用于伪迹去除。本文提出了一种基于典型相关的多维方法用于心脏伪迹去除，并报告了其在14名参与者中与定制15通道心电描记术同时记录的脑电图上的有效性。我们通过残留R波伪迹量化清洁质量，并通过α功率量化神经信号保存。典型相关在减少R波伪迹和保存α功率方面系统性地优于传统的独立成分分析。通过分析所有可能的通道组合，我们发现在只有少量通道可用时，颈部或锁骨上电极可以改善清洁效果。当使用四或五个通道时，心前区电极与肢体或锁骨上位置的组合提供了与15通道设置相当的性能。虽然这些发现需要在其他数据集中验证，但我们概述了清洁效率的明确决策标准，并表明典型相关是多通道心脏伪迹去除的可靠方法。

## Abstract
Cardiac artefacts are problematic for neurophysiological analyses, especially for heartbeat-locked brain responses where neural activity and artefacts co-occur in time. Traditional approaches using single-channel electrocardiography for artefact removal do not fully capture the multidimensional spread of cardiac fields. Moreover, even if several channels are recorded, no established methods exist for integrating them for artefact removal. Here, we propose a multivariate approach based on Canonical Correlation for cardiac artefact removal and report its effectiveness in electroencephalography recorded simultaneously with a custom 15-channel electrocardiography in 14 participants. We quantify cleaning quality via residual R-peak artefact and neural signal preservation via alpha power. Canonical Correlation systematically outperforms the traditional Independent Component Analysis in both reducing R-peak artefacts and preserving alpha power. By analysing all possible channel combinations, we found that neck or supraclavicular electrodes improve cleaning when only a few channels are available. With four or five channels, precordial electrodes in combination with limb or supraclavicular locations provide a performance comparable to the 15-channel setup. While these findings require validation in other datasets, we outline clear decision criteria for cleaning efficiency and show that canonical correlation is a reliable approach for multi-channel cardiac artefact removal.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：在心跳锁定（heartbeat-locked）的脑电（EEG）分析中，心脏电场伪迹（Cardiac Field Artefacts, CFA）与神经信号在时间上高度重叠，难以区分。传统方法（如单通道心电图（ECG）记录配合独立成分分析（ICA））不能充分捕捉心脏场的多维空间结构，导致伪迹去除不彻底，干扰对真实神经活动（如心跳诱发电位HER）的解释。
- **背景价值**：心脑交互是认知神经科学和自主神经科学的热点，准确的伪迹去除是可靠结果的前提。当前缺乏利用多通道ECG信息的系统方法，也缺少评估清洁效果的公认标准。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：利用典型相关分析（Canonical Correlation Analysis, CCA）直接识别EEG中与多通道ECG最大相关的成分，从而针对性地去除心脏伪迹。CCA将EEG和ECG作为两组多变量信号，寻找线性组合使两者相关性最大，得到的典型成分按相关系数排序，代表受心脏污染程度递减的方向。
- **关键技术细节**：
  - 数据预处理：EEG降采样至250 Hz，去除50 Hz工频，滤除坏导，重参考至平均，带通滤波0.5-20 Hz。
  - CCA实施：对连续EEG（X∈R^{T×N}）和ECG（Y∈R^{T×M}）求解最大化相关性的权重向量w_x和w_y，得到空间滤波器W_x和模式矩阵A。通过迭代去除相关系数最大的前k个成分来计算伪迹子空间投影（ˆX_artefact = X P_k），并从原始数据中减去，得到清洁信号˜X_k。
  - 迭代去除与停止准则：提出以**R波峰幅度**（EEG中与R峰时间锁定的最大绝对值）作为残留伪迹的指标，以**α功率**（个体化α频带平均功率）作为神经信号保存的指标。当后续成分去除不再使R波峰幅度有实质下降（超过最小效应量SESOI，设定为基线的5%），则停止。
  - 与ICA对比：ICA使用Infomax算法，成分通过ICLabel自动分类（去除肌肉、眼动、通道噪声），然后按成分与所有ECG通道的最大绝对相关系数排序，迭代去除。

## 3. 实验设计

- **数据集**：14名健康对照参与者（来自更大项目控制组），采集同时的64通道EEG和定制15通道ECG（包括标准胸前V1-V6、肢体导联RA/LA/LL（改良躯干放置）、两个锁骨上电极和四个颈电极）。
- **实验场景**：安静、电屏蔽室内的静息态EEG-ECG记录，每次10分钟，共两次（本文仅分析静息态数据）。无特定任务，属于基线状态。
- **基准（benchmark）**：以无清洁的原始数据作为基线；以15通道CCA达到的最低R波峰幅度作为“黄金标准”（full-15 optimum）。
- **对比方法**：
  - ICA（基于Infomax + ICLabel + 与ECG相关性排序）迭代去除成分。
  - CCA使用不同数量的ECG通道组合（1-15通道）进行清洁。
- **评估指标**：
  - 清洁效果：残留R波峰幅度（基线校正后，锁定到R峰的试次平均信号窗口内最大绝对值）。
  - 神经信号保存：α功率（个体化频带，约6.75-14.75 Hz）。
  - 还使用统计模型（贝叶斯多水平模型）对比差异，并定义最小效应量SESOI=5%基线值。

## 4. 资源与算力

- **文中未明确说明**使用的GPU型号、数量或训练时长。该方法是非深度学习信号处理方法，计算主要在CPU上完成（MATLAB），不需要大量算力。文中未提及具体计算时间。

## 5. 实验数量与充分性

- **实验数量与类型**：
  - 主实验：在14名受试者上比较CCA与ICA在不同去除成分数（1-15）下的表现，覆盖每个受试者的64个EEG通道，产生大量观测（14×64×15 ≈ 13440个数据点用于对比）。
  - 通道组合分析：对所有可能的1-5通道ECG子集（1通道：15种；2通道：105种；3通道：455种；4通道：1365种；5通道：3003种）进行评估，每个子集在所有参与者、所有EEG通道上测试最优清洁水平，并计算与15通道全集的差距。
  - 使用贝叶斯多水平模型进行统计推断，包含受试者和通道随机效应，控制多次比较。
  - 补充分析：分析了不同解剖家族（颈、锁骨上、肢体、心前区）在最优组合中的出现频率，并通过bootstrap重采样（100次）评估稳定性。
- **充分性与客观性**：
  - 实验设计系统，覆盖了所有可能的降维配置，具有穷尽性。
  - 使用标准化预处理和自动成分分类，减少了主观偏差。
  - 但是样本量仅14人，且全部来自健康对照组，可能限制泛化性。方法比较完全内部进行（无外部基准数据集），公平性主要在于使用相同的预处理和迭代框架。

## 6. 主要结论与发现

1. **CCA优于ICA**：在残留R波峰幅度方面，CCA显著低于ICA（后验中位数差异-0.416 μV，95% PI -0.426至-0.407，P(CCA<ICA)>0.999）；在α功率保存方面，CCA略高或相当（差值0.05 dB，提示神经信号损失更少）。
2. **迭代清洁轨迹不同**：CCA表现出渐进稳定的下降，约在去除4个成分后达到平台期；ICA在第一个成分后改善有限，后续效果不稳定。
3. **通道组合建议**：
   - 单个ECG通道效果有限（即使最佳通道V6也只恢复约50%的全15通道改善）。
   - 2-3通道时，颈部和锁骨上电极搭配肢体参考相对最优。
   - 4-5通道时，心前区（V）电极结合肢体和/或锁骨上电极可接近15通道性能（5通道最佳组合恢复95.28%改善，49.58%观测与15通道无实质差异）。
   - 建议实际应用：记录越多ECG通道越好；若受限，优先使用4-5个电极，包括多个心前区（如V1-V6中选择）和至少一个肢体或锁骨上电极。
4. **评估准则实用**：R波峰幅度和α功率组成有效的停止准则和清洁质量指标。

## 7. 优点

- **方法创新**：首次系统地将CCA用于多通道ECG引导的EEG伪迹去除，直接利用心脏场的多维信息，避免了ICA盲分离的不确定性。
- **评估体系完善**：提出基于残留R波和α功率的双重准则，既量化伪迹残留，又监控神经信号损失，提供数据驱动的停止规则。
- **分析全面**：穷尽搜索所有通道组合，提供具体配置建议，具有实践指导意义。
- **统计分析严谨**：使用贝叶斯多水平模型处理分层数据，报告后验不确定性和效应方向概率。
- **代码和数据开放**：提供GitHub代码和OSF数据，可复现。

## 8. 不足与局限

- **样本量小**：仅14名健康对照，可能无法代表群体变异；未包含临床人群（如心律失常患者），心脏伪迹特征可能不同。
- **缺乏外部验证**：结论基于单一研究自己的数据集，需在独立EEG/MEG数据集、不同记录系统、不同实验室中验证。
- **评估指标有限**：主要关注R峰和α功率；未评估其他频带（如θ/β）、空间模式、或对不同HER成分的影响。R波准则主要针对直接电场传导，但不能完全排除延迟的机械性伪迹（如脉动伪迹）。
- **仅考虑静息态数据**：未测试任务态下的表现，任务可能带来额外噪声或干扰。
- **MEG未测试**：虽然方法可能适用于MEG，但未直接验证。
- **过度清洁风险**：保守的CCA可能移除部分与心跳时间锁定的真实神经活动，本文认为保守策略更安全，但未量化这种损失对HER幅度的影响。
- **停止准则的依赖性**：SESOI设定为5%基线值，可能因记录特性而需调整，非通用最优值。

（完）
