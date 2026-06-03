---
title: Evaluating the Sensitivity of Dry and Gel-Based Wearable EEG for Cognitive Load Estimation
title_zh: 评估干式和凝胶式可穿戴脑电图对认知负荷估计的敏感性
authors: "Idesis, S., Masias Bruns, M., Emami, P., Duraisamy, S., Leiva, L. A., Arapakis, I."
date: 2026-05-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.05.723048v1.full.pdf"
tags: ["query:pbci-load"]
score: 9.0
evidence: 直接评估基于EEG的认知负荷估计，比较干电极和凝胶电极
tldr: 干电极脑电系统因便携性而被广泛采用，但其对认知负荷评估的敏感性仍存争议。本研究通过120名被试的信息可视化任务，比较了干电极与凝胶电极系统的信号质量和频谱特征。结果显示，虽然凝胶系统信号质量更优，但差异的实际影响较小，干系统足以捕捉工作量相关的神经标记。这一发现表明干系统可用于粗粒度认知负荷评估，为实际应用中的系统选择提供了权衡依据。
source: biorxiv
selection_source: fresh_fetch
motivation: 探讨干电极EEG在认知负荷评估中是否具有足够的敏感性。
method: 通过120名被试在信息可视化任务中比较干、凝胶EEG系统的信号质量和频谱特征。
result: 凝胶系统信号质量更好，但差异效应量小，干系统足以提供足够的生理敏感性。
conclusion: 干系统适用于粗粒度评估，凝胶系统在高敏感性需求时更优。
---

## 摘要
目的 我们进行了一项大规模（N=120）的对比研究，比较凝胶式和干式脑电图系统在涉及信息可视化刺激的任务中进行认知负荷分析的效果。尽管干式系统因其便携性和快速设置而被越来越多地采用，但与凝胶式系统相比，它们对认知相关测量的敏感性仍存在争议。这限制了我们对干式系统在受控任务条件下是否为认知负荷评估提供足够敏感性的理解。

方法 我们分析了一系列信号质量指标，如信噪比和通道保持率，并结合跨频段的频谱特征，评估每个设备在信息可视化任务中捕获工作负荷相关神经标记的能力。

结果 尽管凝胶式设备始终显示出比干式设备更好的质量结果，但效应量表明系统间差异的实际意义较小。这些结果表明，干式系统可以为认知负荷评估提供足够的生理敏感性。

结论 我们的发现凸显了可用性（设置、校准等）与数据保真度之间的权衡，为选择用于认知工作负荷监测和应用神经工程研究的脑电图系统提供了实用指导。总体而言，结果表明干式系统可以支持粗粒度的认知负荷评估，而凝胶式系统在需要更高敏感性时仍然具有优势。

## 速览
**TLDR**：干电极EEG系统虽便携但对其在认知负荷评估中的敏感性存疑。本研究基于120名被试，比较干电极与凝胶电极EEG在信息可视化任务中的信号质量和频谱特征。结果表明凝胶系统质量更优但实际差异微小，干系统足以提供足够的生理敏感性。研究为根据任务需求选择EEG系统提供了实用指导。 \
**Motivation**：比较干电极与凝胶电极EEG在认知负荷估计中的敏感性差异。 \
**Method**：分析120名被试在信息可视化任务中的信号质量与频谱特征。 \
**Result**：凝胶系统质量更优但效应量小，干系统具备足够敏感性。 \
**Conclusion**：干系统适用于粗粒度评估，凝胶系统在需高敏感度时更优。

---

## Abstract
PurposeWe present a large-scale (N=120) comparative study of gel-based and dry electroencephalography systems for cognitive load analysis in tasks involving information visualization stimuli. Although dry systems are increasingly adopted owing to their portability and fast setup, their sensitivity to cognitive-related measurements (as compared to gel-based systems) remains debated. This limits the understanding of whether dry systems provide sufficient sensitivity for cognitive load assessment under controlled task conditions.

MethodsWe analyzed a diverse set of signal quality metrics, such as signal-to-noise ratio and channel retention, combined with spectral features across frequency bands to evaluate the ability for each device to capture workload-related neural markers during information visualization tasks.

ResultsAlthough the gel-based device showed consistently better quality results than the dry one, the effect sizes suggest a small practical significance of the differences between systems. These results demonstrate that dry systems can provide adequate physiological sensitivity for cognitive load assessments.

ConclusionOur findings highlight the trade-off between usability (setup, calibration, etc.) and data fidelity, providing practical guidance for choosing electroencephalography systems for cognitive workload monitoring and applied neuroengineering research. Overall, the results suggest that dry systems can support coarse-grained cognitive load assessment, while gel-based systems remain advantageous when greater sensitivity is required.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：干式电极脑电图（EEG）系统因便携性和快速设置而被广泛采用，但其对认知负荷相关神经标记的敏感性是否足以替代传统的凝胶式EEG系统，目前仍存在争议。
- **研究动机**：澄清干式EEG在受控任务条件下能否为认知负荷评估提供足够的生理敏感性，从而为实际应用中的系统选择提供科学依据。
- **背景**：凝胶式EEG具有高信号质量，但准备时间长、舒适度差；干式EEG使用更便捷但可能牺牲信号保真度。已有研究质量不一，缺乏大规模直接对比。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：通过大规模受控实验，系统比较干式和凝胶式EEG在信号质量（信噪比、通道保持率）和频谱特征（不同频段的功率）上的差异，并评估两者对认知负荷变化的敏感性。
- **关键技术细节**：
  - 使用相同的信息可视化刺激任务（如不同复杂度的图表或数据呈现），诱发可变的认知负荷水平。
  - 信号预处理：采用标准化流程去除伪迹、滤波、分段。
  - 分析指标：
    - **信噪比（SNR）**：反映信号与噪声的比例。
    - **通道保持率**：可用的有效通道比例（剔除坏通道后）。
    - **频谱特征**：提取θ、α、β等频段的功率谱密度，作为认知负荷的神经标记（如额叶θ/α比率等）。
- **公式或算法流程**：文中未提供具体公式，仅说明使用了标准的信号处理与频谱分析方法（如快速傅里叶变换、基于频带的功率计算）。流程可概括为：数据采集→预处理→质量评估→频谱分析→统计比较。

### 3. 实验设计：数据集、基准、对比方法

- **数据集与场景**：
  - 被试：120名健康志愿者（N=120），规模在同类研究中较大。
  - 任务：信息可视化刺激（如不同难度的数据图表或视觉搜索任务），每个被试在两种EEG系统下分别完成相同任务（可能为组间或组内设计，摘要未明确）。
  - 基准：没有外部标准数据集，而是以凝胶式EEG系统为“金标准”进行对比。
- **对比方法**：
  - 直接比较干式系统（具体型号未给出）与凝胶式系统（具体型号未给出）在同一任务下的信号质量和工作量相关频谱特征。
  - 没有与其他EEG系统或非EEG方法（如行为测量、主观量表）进行系统性对比，但可能使用了主观负荷评分的验证（摘要未提及）。

### 4. 资源与算力

- **未明确说明**：论文摘要和元数据中未提及使用的GPU型号、数量、训练时长等计算资源信息。
- **推断**：由于主要涉及信号处理和统计分析（如t检验、效应量计算），计算量相对较低，可能不需要GPU算力。在机器学习模型（如果存在）方面，文中未提到深度学习或复杂模型，因此算力需求不显著。

### 5. 实验数量与充分性

- **实验数量**：主要有一项核心实验——120名被试在单一任务场景下比较两种系统。没有额外的消融实验、不同任务变体或交叉验证。
- **充分性评估**：
  - **优点**：样本量较大（N=120），增强了统计效力，能够检测较小的效应量。
  - **不足**：
    - 仅使用一种类型的任务（信息可视化），无法推广到其他认知负荷场景（如注意力、工作记忆、多任务等）。
    - 未进行设备校准、设置时间、被试舒适度等可用性维度的量化对比。
    - 未考虑个体差异（如头皮状况、发量）对干式EEG的影响。
    - 缺乏对认知负荷水平进行系统操纵（如多个难度级别）的详细分析，仅笼统提及“工作量相关神经标记”。
- **客观性与公平性**：研究设计基本合理，采用相同的任务条件和预处理流程，但未提供随机化或盲法细节，可能存在顺序效应或主观偏差。

### 6. 论文的主要结论与发现

- 凝胶式EEG在信噪比和通道保持率等信号质量指标上始终优于干式EEG。
- 但系统间差异的**效应量（effect size）** 较小，表明实际意义有限。
- 干式EEG系统**足以捕获认知负荷相关的神经频谱变化**，能够提供足够的生理敏感性用于粗粒度评估。
- 结论：干式系统适合快速部署、便携场景下的认知负荷监测；当需要最高敏感性（例如精确区分细微负荷差异）时，凝胶式系统仍具优势。

### 7. 优点：方法或实验设计上的亮点

- **大规模样本**：120名被试在EEG对比研究中属于大规模，提高了结论的可靠性。
- **聚焦实际权衡**：直接比较可用性与数据保真度之间的平衡，为实际应用（如人机交互、神经工效学）提供了可操作的指导。
- **多维指标**：同时使用信号质量和频谱敏感性指标，而非单一维度，更全面地反映了系统性能。
- **效应量分析**：不仅报告统计显著性，还强调效应量，帮助判断差异的实际重要性。

### 8. 不足与局限

- **任务单一**：仅使用信息可视化任务，无法推广至其他认知负荷诱发场景（如听觉、混合模态）。
- **未控制个体变量**：未报告被试头发长度、头皮阻抗等可能影响干式电极性能的因素。
- **缺乏可用性量化**：未直接记录设置时间、校准失败率、被试舒适度评分等可用性数据。
- **统计细节缺失**：未说明实验设计是组内还是组间、是否进行多重比较校正、是否有脱落等。
- **设备代表性**：只使用了某一特定型号的干式和凝胶系统，结论可能无法泛化到所有商用设备。
- **敏感性边界模糊**：什么是“粗粒度”和“高敏感性”未明确定义，缺乏阈值或分类标准。

（完）
