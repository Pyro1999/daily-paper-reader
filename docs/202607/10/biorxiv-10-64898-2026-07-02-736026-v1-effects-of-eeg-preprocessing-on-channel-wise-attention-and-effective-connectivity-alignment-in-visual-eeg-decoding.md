---
title: Effects of EEG Preprocessing on Channel-Wise Attention and Effective Connectivity Alignment in Visual EEG Decoding
title_zh: 脑电预处理对视觉脑电解码中通道注意力和有效连接对齐的影响
authors: "Elichatiti, V. V., Basari, B., Arif, M., Ikhsan, M."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736026v1.full.pdf"
tags: ["query:robust-eeg"]
score: 8.0
evidence: 评估了EEG预处理（ICA和陷波滤波）对基于变换器的深度学习解码模型的影响
tldr: Transformer模型在视觉EEG解码中展现潜力，但其注意力机制与神经生理的一致性尚不明确。本研究采用Adaptive Thinking Mapper模型，对比基线MVNN预处理与集成ICA和陷波滤波的综合流程，通过交叉泛化、噪声鲁棒性等分析评估，并利用节点强度相关性和表征相似性分析对比注意力权重与有效连接网络。结果表明，综合预处理有效抑制伪迹，保持解码精度，且学习到的注意力空间组织稳定，捕捉关键定向连接动态。工作桥接了数据驱动注意力与神经生理一致性，推动可解释脑机接口发展。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1784, \"height\": 1338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1862, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1876, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1871, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1875, \"height\": 1137, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1855, \"height\": 1043, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 918, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 927, \"height\": 804, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 906, \"height\": 730, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 942, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1885, \"height\": 1029, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 812, \"height\": 917, \"label\": \"Table\"}]"
motivation: 探究EEG预处理策略对Transformer注意力表征与神经生理连接对齐的影响，提升模型可解释性。
method: 基于ATM模型，对比MVNN与ICA+陷波预处理，通过交叉泛化、噪声鲁棒性、消融分析及与GPDC/PDC/DTF网络的结构对应分析。
result: 综合预处理有效抑制伪迹；注意力空间组织跨流程稳定，捕捉关键定向连接动态，但全局几何存在度量依赖的细微差异。
conclusion: 数据驱动注意力权重可反映神经生理连接，为透明BCI提供实证支持。
---

## 摘要
基于Transformer的深度学习模型在视觉脑电信号解码方面展现出巨大潜力。然而，其内部注意力机制通常主要基于优化目标进行评估，与生物大脑连接的对齐程度仍是一个开放问题。本研究以自适应思维映射器（ATM）模型为框架，实证评估了脑电预处理策略的变化如何影响这些注意力表示。我们比较了基线管道（仅MVNN）与整合了ICA和陷波滤波的综合清理管道。通过交叉泛化、噪声鲁棒性和频谱-时间消融分析对模型进行了评估。此外，我们利用节点强度相关性和表征相似性分析（RSA）研究了模型数据驱动注意力权重与神经生理参考网络（GPDC、PDC和DTF）之间的结构对应关系。结果表明，综合预处理成功抑制了非神经伪迹（如额叶噪声和电气干扰），同时保持了相当的解码准确性和基线鲁棒性。对齐分析显示，学习到的注意力模式的广泛空间组织在不同管道间保持高度稳定，捕捉了关键的有向连接动态，全局表征几何结构存在细微且依赖于度量指标的变化。这项工作为弥合数据驱动注意力权重与神经生理一致性之间的差距提供了实证探索，为更透明的脑机接口提供了见解。

## Abstract
Transformer-based deep learning models have shown great potential for decoding visual EEG signals. However, their internal attention mechanisms are often evaluated primarily on optimization objectives, leaving their alignment with biological brain connectivity an open question. This study empirically evaluates how variations in EEG preprocessing strategies affect these attention representations using the Adaptive Thinking Mapper (ATM) model as a framework. We compared a baseline pipeline (MVNN only) against a comprehensive cleaning pipeline integrating ICA and notch filtering. The models were evaluated through cross-generalization, noise robustness, and spectral-temporal ablation analyses. Furthermore, we investigated the structural correspondence between the models data-driven attention weights and neurophysiological reference networks (GPDC, PDC, and DTF) using Node Strength Correlation and Representational Similarity Analysis (RSA). The results show that the comprehensive preprocessing successfully suppresses non-neural artifacts, such as frontal noise and electrical interference, while maintaining comparable decoding accuracy and baseline robustness. Alignment analyses revealed that the broad spatial organization of the learned attention patterns remains highly stable across pipelines, capturing key directed connectivity dynamics with subtle, metricdependent variations in global representational geometry. This work provides an empirical exploration into bridging data-driven attention weights with neurophysiological consistency, offering insights toward more transparent brain-computer interfaces.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义

- **研究动机**：Transformer 模型在视觉脑电图（EEG）解码中表现优异，但其内部注意力机制主要基于损失函数优化，与大脑真实的神经生理连接（即有向有效连接）之间的对齐程度尚不清楚。同时，EEG 预处理策略（如 ICA、陷波滤波）可能改变信号结构，进而影响模型学到的注意力表征的生物学可解释性。
- **核心问题**：不同 EEG 预处理方案如何影响 Transformer 通道注意力权重的生物合理性？注意力模式是否能反映已知的视觉处理通路中的有向连接？
- **整体意义**：为数据驱动的深度学习模型与神经生理学之间建立桥梁，推动更透明、可解释的脑机接口（BCI）发展。

## 2. 论文提出的方法论

- **核心思想**：以 Adaptive Thinking Mapper（ATM）模型为框架，通过对比基线预处理（仅 MVNN）与综合预处理（ICA + 陷波滤波 + MVNN），系统评估预处理对注意力表征的影响，并将注意力权重与基于 MVAR 的有向连接参考（GPDC、PDC、DTF）进行结构对齐分析。
- **关键技术细节**：
    - **预处理流程**：原始信号 → 50 Hz 陷波滤波（仅提议管道）→ ICA 分解（63 个成分，去除眼动、肌电伪迹）→ 分段（-0.2 s 到 1.0 s）→ 基线校正 → 降采样至 250 Hz → MVNN（协方差白化）。基线管道跳过 ICA 和陷波滤波。
    - **模型架构**：ATM 编码器包含 Subject Token 和 63 个 Channel Token，通过多头自注意力（4 个头）学习通道间关系。注意力公式：`Attention(Q, K, V) = softmax(Q K^T / sqrt(d_k)) V`。最终平均 4 个头和所有试验的注意力矩阵作为稳定表示。
    - **有效连接计算**：基于多变量自回归模型（MVAR，阶数 p=5 由 BIC 确定），在频率域导出 PDC、GPDC、DTF 三个度量。
    - **对齐评估**：① 节点强度相关性：计算每个通道的入、出、总强度（加权连接和），用 Spearman 相关比较注意力与各连接度量；② 表征相似性分析（RSA）：构建表征相异矩阵（RDM），用 Spearman 相关比较结构相似性。

## 3. 实验设计

- **数据集**：THINGS-EEG2，包含 10 名健康受试者，采用 RSVP 范式，63 通道 EEG（采样率 1000 Hz，重参考至 Fz），16,540 训练图像与 200 测试图像。
- **基准**：基线管道（仅 MVNN）作为对比基准；提议管道（MVNN + ICA + 陷波滤波）作为待评估方法。
- **对比方法与评估**
    - **分类性能**：Top-1、Top-5 准确率，以及 V2、V4、V10 候选集设置。训练 40 个 epoch，取最终模型。
    - **交叉泛化**：训练与测试预处理互换（基线训练+提议测试；提议训练+基线测试）。
    - **频谱消融**：分别删除 δ、θ、α、β、γ 频带和线噪声频带（45-55 Hz），观察性能下降。
    - **时间消融**：删除不同时间段（T1~T5：0-200 ms、200-400 ms、400-600 ms、600-800 ms、800-1000 ms）。
    - **噪声鲁棒性**：在测试阶段注入不同标准差的高斯噪声（σ=0.0, 0.1, 0.3, 0.5, 1.0）。
    - **对齐分析**：对比注意力矩阵与 GPDC/PDC/DTF 的节点强度相关性和 RSA，涵盖宽带和各频带。

## 4. 资源与算力

- 论文**未明确说明**所使用的 GPU 型号、数量或训练时长。
- 仅提到优化器为 AdamW（学习率 3e-4），batch size 64，训练 40 个 epoch，针对 10 名受试者独立训练。随机种子固定为 24。

## 5. 实验数量与充分性

- **实验组别**：
  - 分类性能（表 I，图 3）：基线 vs 提议，10 名受试者，5 个指标。
  - 交叉泛化（表 I）：4 种训练-测试组合。
  - 频谱消融（表 II，图 4A-B）：5 个频带 + 线噪声，基线 & 提议。
  - 时间消融（表 III，图 4C-D）：5 个时间段，基线 & 提议。
  - 噪声鲁棒性（表 IV，图 4E-F）：5 个噪声级，基线 & 提议。
  - 节点强度相关（表 V，图 5A）：3 个连接度量 × 7 个频带/宽带 × 3 种强度类型。
  - RSA（表 VI，图 5B）：同样维度。
  - 地形图可视化（图 6）：对比 GPDC θ 和 α 带。
- **充分性评价**：实验覆盖了预处理、频谱、时间、噪声干扰以及两种结构对齐指标，设计较为系统。所有结果均基于 10 名受试者的配对 t 检验并经过 FDR 校正，统计严谨。但缺少对模型在不同视觉刺激类别上表现的细分分析，也未探讨多个随机初始化的稳定性（仅用一个种子）。整体而言，实验数量充分，设计客观公平。

## 6. 论文的主要结论与发现

- 综合预处理（ICA + 陷波）成功抑制额叶伪迹和 50 Hz 线噪声，且**不显著损害解码准确率**。基线比提议仅高出微小且非显著的幅度（Top-1 26.3% vs 24.7%）。
- **交叉泛化**表现稳定，说明模型不依赖于预处理特异性特征。
- **频谱消融**显示θ和δ频带对性能最关键；移除后 Top-1 下降至约 8-12%。
- **时间消融**显示 0-400 ms 窗口最不可少（P300 等早期 ERP），移除后性能降至 5-6%。
- 两种管道对**噪声鲁棒性**表现几乎一致，说明 ICA 去除伪迹不引入额外脆弱性。
- **注意力-连接对齐**：
  - 节点强度层面：基线略优于提议，但 FDR 校正后无显著差异；GPDC 在θ和α带与注意力对齐最好（总强度相关系数 0.4-0.5），PDC/DTF 对齐很弱。
  - RSA 层面：提议管道在所有连接度量上倾向获得更高（虽不显著）的对齐分数，效应量中等。
  - **核心结论**：注意力模式的**空间组织（hub 级拓扑）跨预处理保持稳定，但全局表征几何（RSA）存在度量依赖的细微差异**；综合预处理可以改善全局对齐但未显著改变局部 hub。

## 7. 优点

- **系统性**：从预处理效果、模型鲁棒性到生物对齐，构建了完整的评估链条，层次清晰。
- **对比视角**：同时采用节点强度（局部）和 RSA（全局）两种互补指标，避免单一指标偏差。
- **统计严谨**：使用配对 t 检验、Cohen's d 效应量、FDR 多重比较校正，结果可信。
- **多维度消融**：不仅消融频带和时段，还进行了跨预处理泛化，揭示了模型的泛化能力。
- **实际意义**：为深度学习模型在 BCI 中的可解释性提供了实证指导，说明注意力权重能在一定程度上反映有效连接。

## 8. 不足与局限

- **算力资源缺失**：未报告 GPU 型号、数量和总训练时间，影响可复现性。
- **种子单一**：仅使用随机种子 24，未测试不同随机初始化下的稳定性，存在过拟合风险。
- **单数据集**：仅用了 THINGS-EEG2 一个数据集，泛化性需更多数据集验证。
- **模型局限**：仅评估了 ATM 模型，结论可能不适用于其他 Transformer 架构或 CNN 模型。
- **有效连接估计**：MVAR 模型阶数固定为 5（基于 BIC 中位数），但不同频带或受试者最优阶数可能不同，且 MVAR 对非平稳 EEG 数据有局限性。
- **注意力提取方式**：仅取了最后一层平均注意力，忽略了不同层或头可能代表不同子空间，可能导致信息丢失。
- **无因果关系证明**：虽探究了“对齐”，但未实施因果干预（如扰动注意力），不能证明注意力直接反映神经连接。
- **生物解释深度**：结论停留在“整体对齐”，未深入探讨哪些具体通路（如枕颞、枕顶）的注意力模式与连接一致，缺乏神经生物学细节。

（完）
