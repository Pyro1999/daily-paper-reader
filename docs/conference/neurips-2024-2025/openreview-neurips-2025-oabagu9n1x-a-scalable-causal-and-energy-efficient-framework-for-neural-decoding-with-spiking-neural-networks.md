---
title: "A Scalable, Causal, and Energy Efficient Framework for Neural Decoding with Spiking Neural Networks"
title_zh: 用于神经解码的可扩展、因果且能量高效的脉冲神经网络框架
authors: "Georgios Mentzelopoulos, Ioannis Asmanis, Konrad Kording, Eva L Dyer, Kostas Daniilidis, Flavia Vitale"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=oAbaGU9N1X"
tags: ["query:pbci-load"]
score: 6.0
evidence: 用于BCI神经解码的因果高效SNN框架
tldr: 为了解决现有BCI神经解码器在实时和资源受限场景下的效率问题，本文提出基于脉冲神经网络（SNN）的可扩展、因果且能量高效的框架。该方法在保持因果性的同时实现了良好的泛化，并在多个基准上验证了其性能，为被动BCI系统提供了高效的深度学习替代方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1382, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 756, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1429, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1443, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 661, \"height\": 667, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 813, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1447, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1439, \"height\": 312, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1425, \"height\": 1207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1407, \"height\": 329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 853, \"height\": 343, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1322, \"height\": 149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 858, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 585, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 793, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 916, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 899, \"height\": 275, \"label\": \"Table\"}]"
motivation: 现有神经解码器要么简单因果但泛化差，要么复杂非因果但实时性差，且功耗高。
method: 提出基于脉冲神经网络（SNN）的因果、可扩展框架，实现高效神经解码。
result: 在多个基准上证明该框架在保持低功耗和因果性的同时达到良好解码性能。
conclusion: 该SNN框架为资源受限的BCI系统提供了实用的神经解码方案。
---

## Abstract
Brain-computer interfaces (BCIs) promise to enable vital functions, such as speech and prosthetic control, for individuals with neuromotor impairments. Central to their success are neural decoders, models that map neural activity to intended behavior. Current learning-based decoding approaches fall into two classes: simple, causal models that lack generalization, or complex, non-causal models that generalize and scale offline but struggle in real-time settings. Both face a common challenge, their reliance on power-hungry artificial neural network backbones, which makes integration into real-world, resource-limited systems difficult. Spiking neural networks (SNNs) offer a promising alternative. Because they operate causally (i.e. only on present and past inputs) these models are suitable for real-time use, and their low energy demands make them ideal for battery-constrained environments. To this end, we introduce **Spikachu: a scalable, causal, and energy-efficient neural decoding framework based on SNNs**. Our approach processes binned spikes directly by projecting them into a shared latent space, where spiking modules, adapted to the timing of the input, extract relevant features; these latent representations are then integrated and decoded to generate behavioral predictions. We evaluate our approach on 113 recording sessions from 6 non-human primates, totaling 43 hours of recordings. Our method outperforms causal baselines when trained on single sessions using between 2.26× and 418.81× less energy. Furthermore, we demonstrate that scaling up training to multiple sessions and subjects improves performance and enables few-shot transfer to unseen sessions, subjects, and tasks. Overall, Spikachu introduces a scalable, online-compatible neural decoding framework based on SNNs, whose performance is competitive relative to state-of-the-art models while consuming orders of magnitude less energy.

---

## 论文详细总结（自动生成）

# 论文总结：Spikachu——基于脉冲神经网络的可扩展、因果、能量高效神经解码框架

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有脑机接口（BCI）神经解码器面临三难困境——简单因果模型（如MLP、GRU）实时性好但泛化差、复杂非因果模型（如POYO）性能强但无法在线且能耗高，而两类模型均依赖高功耗的人工神经网络（ANN），难以集成到电池约束的植入式设备中。
- **整体含义**：作者旨在同时实现神经解码器的**因果性（实时兼容）**、**能量高效**（适合电池供电）和**可扩展性**（跨session、跨subject、跨任务泛化），从而推动BCI从实验室走向临床应用。脉冲神经网络（SNN）因其固有因果性和低能耗成为理想基础，但此前SNN解码工作仅限于浅层网络和单session，缺乏规模和泛化能力。本文首次将SNN与transformer结合，提出Spikachu框架，在保持低功耗的同时达到与最先进模型竞争的性能，并通过大规模预训练实现跨session/subject/task的快速迁移。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
以SNN为主体架构，结合perceiver encoder实现异构神经活动的统一token化与共享潜空间映射，再通过多尺度SNN模块、脉冲自注意力机制以及膜电位观测器层实现因果、低功耗的连续行为预测。

### 关键技术细节（算法流程文字说明）

1. **Tokenization与共享潜空间（Harmonizer）**
   - 将每个神经单元（unit）映射为可学习嵌入（32维），形成输入序列X。
   - 使用Perceiver编码器：通过交叉注意力将变长输入X投影到固定长度的潜在token Z1（128个token，各32维），再经线性层得到低维潜变量Z2（128维虚拟单元）。该过程无session/subject特定参数，实现跨session共享表征。

2. **多尺度SNN特征提取（Multi Scale SNN-I）**
   - 将Z2输入p=3个并行脉冲前馈网络（spiking MLP），每个网络具有可学习的不同泄漏时间常数（τ初始值分别为1.11, 1.46, 434.79），从而在不同时间尺度上提取特征。每个网络输出256维，拼接形成序列Zms（3×256）。

3. **脉冲自注意力（Spiking Self-Attention, SSA）**
   - 对Zms应用Zhou et al.提出的脉冲自注意力：先通过脉冲层生成Q、K、V，再计算注意力矩阵，避免softmax高功耗计算。使用8头，输出256维，后接残差连接和脉冲前馈网络。

4. **时空压缩与多尺度融合**
   - 将SSA输出（3×256）展开后经脉冲MLP降维至384维。
   - 再经过2个并行脉冲MLP（Multi Scale SNN-II），tau分别初始化为1.11和434.79，输出各384维，拼接为768维。

5. **膜电位观测器与连续输出**
   - 使用不发放脉冲的膜电位观测器层（Leaky Integrate神经元），跟踪膜电位作为连续表征。
   - 最后经线性层投影到2维（速度vx, vy），完成行为预测。

整个模型因果：仅依赖当前和过去输入。SNN层通过二进制脉冲实现用加法（AC操作）替代乘法，显著节能。

## 3. 实验设计

### 数据集与场景
- **主数据集**：Perich et al. 2018数据集，包含4只猴子的111个session，涵盖Center-Out（CO）和Random Target（RT）任务，总计43小时、1.11亿spikes、2000万行为时间点。
- **测试迁移数据集**：Pei et al.的Neural Latents Benchmark（MC-RTT和MC-Maze），包含不同猴子的新任务，用于评估跨动物、跨设置、跨任务泛化。

### Benchmark与对比方法
- **因果基线**：MLP、GRU、LSTM、POYO-causal（POYO加因果掩码）。
- **非因果基线**：POYO（当前state-of-the-art多session解码模型）。
- 评价指标：R²（解码性能）、能量消耗（μJ/推理）。

### 实验设置
- 单session训练：对99个session（猴C、J、M）分别训练，CO任务平均R²=0.84，RT=0.68。
- 多session预训练：Spikachu-mp在99个session联合训练，然后finetune到单session。
- 迁移实验：将Spikachu-mp迁移到新猴T的12个session、以及MC-RTT和MC-Maze。
- 缩放律：在20、49、75、99个session上预训练，评估性能与能量随数据量增长趋势。
- 消融实验：移除各模块（Multi Scale SNN-I/II、SSA、Harmonizer等）测试贡献。
- ANN变体对照：用ReLU替换LIF神经元，验证SNN机制的必要性。

## 4. 资源与算力

- **GPU型号**：NVIDIA L40s, L40, A40, 3090, A6000, 2080 Ti, A10等（多GPU集群，取决于可用性）。
- **单session训练**：显存<11GB，时间<1小时（少数达5小时）。
- **多session预训练**：单个A40（48GB），Spikachu-mp（99 session）在48小时内完成。
- **Finetune**：与单session训练时间相近。
- **推理能耗**：通过FLOPs换算（MAC/AC操作能耗），详见附录E。

## 5. 实验数量与充分性

### 实验数量
- 单session训练：99个模型（覆盖3猴、CO+RT）。
- 多session预训练：4个模型（20/49/75/99 session）。
- 迁移实验：新猴T（12 session）、MC-RTT、MC-Maze，每个均有finetune对比。
- 消融实验：5种组件去除，在单session和多session上均进行。
- ANN与SNN对比：全变体实验。
- 嵌入空间分析：LDA、SVM分类。

### 充分性评估
- **充分性**：实验覆盖了单session、多session、跨subject、跨task、跨设置（manipulandum vs 触摸屏）；对比了主流因果/非因果基线；消融实验系统；能量分析遵循标准方法（Horowitz能耗模型）。实验设计相当全面，满足NeurIPS级别。
- **客观性**：评价指标（R²）和能耗估算均公开可复现；超参数未精细调优（直接使用Spikachu默认设置），但基线也按标准训练，公平性可接受。唯一可能偏差：POYO-causal是作者自己加掩码实现的，非原文默认，但已说明。
- **局限性**：仅使用公开数据集（灵长类运动皮层），未涉及真实人体或其他脑区；能量估算基于FLOPs理论而非实际芯片测量；未进行在线闭环实验。

## 6. 论文的主要结论与发现

1. **单session性能**：Spikachu以远低于所有基线的能耗（比GRU省2.26倍，比POYO省418倍）获得与GRU相当的R²（CO:0.84，RT:0.68），超越其他因果模型，接近非因果POYO（CO:0.89）。
2. **多session预训练增益**：Spikachu-mp（99 session联合训练）finetune后R²提升（CO:+3.75%, RT:+1.71%），能耗略降（~2%）。
3. **迁移能力**：迁移到新猴T后，性能提升（CO:0.76→0.78, RT:0.66→0.68），能耗降3.6-3.7%，收敛速度提升3-4倍。
4. **缩放律**：预训练session数量越大，finetune后性能增益和能耗优化越明显，且呈现饱和趋势（75 session后趋平）。
5. **跨任务泛化**：虽性能未显著提升（MC-RTT:0.57→0.56, MC-Maze:0.79→0.78），但收敛速度提升2.3-2.7倍，能耗降低2-3%。
6. **消融结论**：Multi Scale SNN模块对性能影响最大；SSA在小规模训练中不必要，但在大规模训练中体现价值；SNN机制（LIF）本身是关键，不能由ANN+上下文替代。

## 7. 优点

- **创新性**：首次将SNN与transformer结合实现大规模、多session、跨subject神经解码，突破了以往SNN解码狭隘的单session限制。
- **工程实用性**：框架因果、低能耗、可在线部署，且参数规模小（<4M突触，~10K神经元），适配Loihi 2等神经形态芯片的物理约束。
- **实验完整性**：系统评估了性能、能耗、缩放律、迁移、消融、表征分析，结论有说服力。
- **能量分析细致**：区分MAC/AC操作，并考虑记忆访问成本，方法严谨。
- **代码与模型开放**：承诺开源，促进可复现性。

## 8. 不足与局限

- **能耗估算的局限性**：基于FLOPs的理论推导而非真实神经形态硬件实测（如Loihi），实际能效可能更高但未验证。
- **实验场景受限**：仅使用运动皮层（M1、PMd）数据，其他脑区（如感觉皮层、语言区）未涉及；仅解码二维速度，高维控制（如手指协调、语音）未测试。
- **未进行在线闭环实验**：虽然因果性保证理论上可在线，但实际实时延迟、系统稳定性未验证。
- **ANN-Harmonizer能耗占比高**：虽然参数少于15%，但能耗占比高，作者指出未来可用全SNN替代。
- **跨任务迁移性能未提高**：仅获得收敛加速，R²未提升，说明预训练的表征对新任务泛化有限。
- **消融实验仅做了去除某模块**，未进行多模块交叉消融；超参数（如并行流数量、τ初值）未系统搜索。
- **数据集全为非人灵长类**，向人类转化仍需验证；且仅两个公开数据集，通用性待扩增。

（完）
