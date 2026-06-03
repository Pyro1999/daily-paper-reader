---
title: "S$^2$M-Former: Spiking Symmetric Mixing Branchformer for Brain Auditory Attention Detection"
title_zh: S2M-Former：用于脑听觉注意检测的脉冲对称混合Branchformer
authors: "Jiaqi Wang, Zhengyu Ma, Xiongri Shen, Chenlin Zhou, Leilei Zhao, Han Zhang, Yi Zhong, Siqi Cai, Zhenxi Song, Zhiguo Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=WtMuGdHvh6"
tags: ["query:pbci-load"]
score: 6.0
evidence: 基于EEG和深度学习的听觉注意检测，属于被动脑机接口范畴
tldr: 针对EEG听觉注意检测中缺乏能效约束下的协同框架问题，本文提出S2M-Former，一种脉冲驱动对称混合架构，通过空间-频率双分支与生物启发的令牌-通道混合器，在低能耗下实现高效注意解码。实验证明其性能优于现有方法，为神经控制助听设备提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 661, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 1102, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 571, \"height\": 969, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 630, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1451, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 584, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 635, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 698, \"height\": 451, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1402, \"height\": 788, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1402, \"height\": 781, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 430, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 942, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 946, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1383, \"height\": 570, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1438, \"height\": 422, \"label\": \"Table\"}]"
motivation: 现有EEG听觉注意检测方法难以在能效约束下充分利用互补特征。
method: 提出脉冲驱动对称架构，包含并行空间和频率分支，以及令牌-通道混合器。
result: 在多个数据集上取得领先的注意检测准确率，同时能耗显著降低。
conclusion: 该工作为神经控制助听设备的发展提供了高效能解决方案。
---

## Abstract
Auditory attention detection (AAD) aims to decode listeners' focus in complex auditory environments from electroencephalography (EEG) recordings, which is crucial for developing neuro-steered hearing devices.  Despite recent advancements, EEG-based AAD remains hindered by the absence of synergistic frameworks that can fully leverage complementary EEG features under energy-efficiency constraints. We propose ***S$^2$M-Former***, a novel ***s***piking ***s***ymmetric ***m***ixing framework to address this limitation through two key innovations:  i)   Presenting a spike-driven symmetric architecture composed of parallel spatial and frequency branches with mirrored modular design, leveraging biologically plausible token-channel mixers to enhance complementary learning across branches; ii) Introducing lightweight 1D token sequences to replace conventional 3D operations, reducing parameters by 14.7$\times$. The brain-inspired spiking architecture further reduces power consumption, achieving a 5.8$\times$ energy reduction compared to recent ANN methods, while also surpassing existing SNN baselines in terms of parameter efficiency and performance. Comprehensive experiments on three AAD benchmarks (KUL, DTU and AV-GC-AAD) across three settings (within-trial, cross-trial and cross-subject) demonstrate that S$^2$M-Former achieves comparable state-of-the-art (SOTA) decoding accuracy, making it a promising low-power, high-performance solution for AAD tasks. Code is available at https://github.com/JackieWang9811/S2M-Former.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究背景**：听觉注意检测（AAD）旨在从脑电图（EEG）中解码听者在复杂听觉环境中的注意力焦点，这对开发神经控制的助听设备至关重要。尽管近期方法取得了进展，但大多数现有方法未能充分利用EEG中互补的时空和频谱特征，同时在能效约束下难以实现轻量化部署。
- **核心问题**：现有双分支网络（如DBPNet、M-DBPNet）虽然融合了多种EEG特征，但存在两个主要缺陷：一是采用孤立学习范式（简单拼接或求和，忽略了分支间互补学习的潜力）；二是引入大量计算开销（如使用3D卷积），限制了可部署性。
- **整体目标**：提出一种轻量、低功耗的脉冲神经网络（SNN）模型S²M-Former，在保持高解码精度的同时大幅降低参数和能耗，为AAD任务提供高效能的神经形态解决方案。

## 2. 论文提出的方法论

**核心思想**：采用脉冲驱动的对称双分支混合架构（Spiking Symmetric Mixing），通过并行处理空间（CSP特征）和频率（DE特征）域表示，利用生物启发的令牌-通道混合器实现互补学习，并用轻量级1D令牌序列替代传统3D操作以降低参数和计算量。

**关键技术细节**：

- **输入特征**：
  - 空间分支：使用共空间模式（CSP）提取时空特征，输入为 $E_S \in \mathbb{R}^{C \times T}$（$C$=通道数，$T$=时间点）。
  - 频率分支：提取差分熵（DE）特征并投影到2D拓扑图，输入为 $E_F \in \mathbb{R}^{5 \times H \times W}$（5个频段，$H \times W$为图大小）。

- **分支专属脉冲编码器**：
  - 空间分支编码器（SBE）：由级联的时间卷积和双路径空间卷积组成，结合批归一化和脉冲神经元（LIF/CPLIF），渐进提取时空依赖性。
  - 频率分支编码器（FBE）：通过三个扩张卷积层（扩张率=2）和池化层提取频率-空间表示，最终通过1×1卷积和残差连接增强稳定性。

- **S²M模块**（核心对称混合模块）：包含一系列镜像脉冲驱动子模块，按顺序处理：
  1. **脉冲通道式自注意力（SCSA）**：修改标准自注意力为通道维度计算（D×D而非N×N），降低复杂度，增强可解释性（空间分支揭示电极相关性，频率分支揭示频带关系）。
  2. **脉冲多尺度可分离卷积（SMSC）**：使用三个并行深度可分离卷积（核大小1,3,5）提取多尺度局部模式，后接通道混洗促进跨尺度信息融合。
  3. **脉冲门控通道混合器（SGCM）**：通过门控机制（查询-键值）自适应融合空间和频率分支的通道表示。
  4. **膜电位感知令牌混合器（MPTM）**：利用全局平均池化构建核心表示，结合来自融合分支和原始分支的信息进行比例填充，通过脉冲元素级调制和残差连接实现跨分支令牌融合。
  5. 上述子模块按对称方式组织：SCSA → SGCM+MPTM → SMSC → SGCM+MPTM，确保层次化互补学习。

- **脉冲神经元**：
  - 模块内通信使用标准LIF神经元。
  - 模块间通信使用提出的**通道式参数化LIF（CPLIF）**：为每个通道赋予可学习的膜时间常数，实现更细粒度的时域建模。

- **输出**：融合后的D维嵌入通过分类头生成预测 $\hat{Y}$。

## 3. 实验设计

- **数据集**（三个公开AAD数据集）：
  - **KUL**：16名受试者，音频-only，荷兰语，8次试验，每次360秒，共12.8小时。
  - **DTU**：18名受试者，音频-only，丹麦语，60次试验，每次50秒，共15小时。
  - **AV-GC-AAD**：11名受试者，视听刺激，荷兰语，8次试验，每次600秒，共14.7小时。

- **评估设置**：
  - **Within-trial**：每个试验数据按8:1:1划分训练/验证/测试，所有试验拼接。
  - **Cross-trial**：所有试验随机按8:1:1划分，避免过拟合特定EEG片段。
  - **Cross-subject**：留一受试者（LOSO）交叉验证，用其余受试者训练，留一个受试者测试。
  - 所有评估在0.1秒、1秒、2秒决策窗口下进行（滑动窗口重叠50%）。

- **对比方法**（5个公开基线）：
  - 单分支：SSF-CNN、MBSSFCC、DARNet。
  - 双分支：DBPNet、M-DBPNet。
  - 额外对比：与若干SNN骨干（Spikformer、QKFormer、Spike-driven Transformer）以及自身消融变体比较。

## 4. 资源与算力

- 论文在附录A.4中说明：所有实验基于**NVIDIA GeForce RTX 4090 GPU**。
- 训练超参数：优化器Adam，批量大小32（受试者依赖）/ 128（受试者无关），训练300轮，采用早停策略（25轮无改善即停止）。
- **未明确给出**总训练时长或具体GPU数量，但提到使用SpikingJelly和PyTorch框架，在单个RTX 4090上完成所有实验。

## 5. 实验数量与充分性

- **实验数量**：覆盖三个数据集、三种评估设置（within-trial、cross-trial、cross-subject），每个设置下三个决策窗口，总计大量比较实验。
- **消融实验**（表4、8、9）：从多方面验证：
  - 比较S²M-Former与ANN对应体（SM-Former）。
  - 比较CPLIF与标准LIF。
  - 去掉SGCM和MPTM模块。
  - 仅用单分支（空间/频率）对比。
  - 比较时间步数（1-8）对性能的影响（图8）。
- **公平性**：所有对比方法采用相同预处理流水线，特征提取在各自集合内独立进行以防信息泄露；优化策略按原论文报告执行，使用相同随机种子确保可重复性。
- **充分性判断**：实验设计较为充分，涵盖主要评估范式、多窗口、消融与基线对比，统计指标包括均值和标准差（±SD），并给出箱线图展示分布。但**未提供置信区间或统计显著性检验**，且部分跨试验结果标准差较大（如KUL cross-trial SD达±25%），说明数据变异性高，可能影响结论稳健性。

## 6. 论文的主要结论与发现

- **性能**：S²M-Former在11/18个条件（within-trial & cross-trial）下达到最高解码准确率，83.33%条件进入前三名，尤其在跨试验（零样本）场景表现突出。
- **参数效率**：仅0.06M参数，比DBPNet小14.7倍，比M-DBPNet小22倍。
- **能效**：能量消耗0.0779 mJ，比DBPNet低5.8倍；与ANN变体相比FLOPs减少53.9%。
- **SNN优势**：脉冲设计不仅降低能耗，还提升了解码准确率（对比ANN变体SM-Former，如在DTU 2s within-trial提升4.34%）。
- **互补学习**：SGCM和MPTM模块的移除导致性能下降，验证了跨分支互补融合的有效性。
- **CPLIF有效性**：替代为标准LIF后性能下降，说明通道式自适应膜时间常数有利于时序建模。
- **可推广性**：在跨受试者（LOSO）设置中同样领先，证明其对未见受试者的泛化能力。

## 7. 优点

- **创新性**：首次将脉冲对称混合框架引入AAD任务，设计生物启发的令牌-通道混合器促进分支间互补学习，而非简单拼接。
- **效率突出**：使用1D令牌序列替换传统3D操作，大幅降低参数和能耗；脉冲驱动架构天然适于神经形态硬件部署。
- **实验全面**：覆盖三种数据集、三种评估设置、多种决策窗口，消融实验系统，对比基线丰富（包括ANN和SNN方法）。
- **可复现性**：公开代码和预训练模型，提供详细超参数和预处理步骤。
- **结果一致**：在多个基准上取得SOTA或接近SOTA的性能，同时能效优势显著，体现良好的trade-off。

## 8. 不足与局限

- **未提供统计显著性检验**：结果仅报告均值和标准差，缺乏置信区间或p值，难以判断差异是否显著。
- **跨试验性能差距**：在KUL和AV-GC的跨试验设置中，标准差较大（如KUL 2s跨试验SD达±25.21%），部分受试者低于机会水平，说明泛化能力仍有提升空间。
- **时间动态建模受限**：论文自述CSP和DE特征预处理破坏了EEG原始时序动态，未来可探索直接建模时间动态的方法（如脉冲序列学习）。
- **硬件验证不足**：理论能耗基于45nm工艺估算，但未在真实神经形态芯片（如Loihi）上进行实验部署验证。
- **消融实验范围有限**：未对SCSA和SMSC单独进行深入消融（仅在DTU 0.1s/1s/2s窗口下部分展示），跨数据集一致性未充分验证。
- **受试者排除后的样本量**：AV-GC数据集仅保留11名受试者（原始16名，排除5名），可能引入选择偏差。
- **可扩展性**：论文提到未来需探索更大规模模型的可扩展性，当前0.06M参数是否能应对更复杂场景尚不明确。

（完）
