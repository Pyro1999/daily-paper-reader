---
title: "Beyond the Forest and the Trees: Overlooking the Overlooked Terrain of Neural State Dynamics"
title_zh: 超越森林与树木：被忽视的神经状态动力学地形
authors: "Asai, T., Kashihara, S., Chiyohara, S."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.729738v1.full.pdf"
tags: ["query:pbci-load"]
score: 7.0
evidence: EEG微状态动力学用于状态分析
tldr: 传统EEG微状态分析等神经动力学粗粒化方法依赖初始模板，导致结果对预处理、聚类算法等敏感，难以跨研究比较。本文从拓扑-几何视角重新审视，将模板视为嵌入状态空间全局结构的界标而非聚类质心，保留极性作为几何关系。实验表明，基于界标的状态定义在捕捉状态结构和分析性能上优于传统聚类模板。该工作揭示了超越聚类优化的核心问题，即如何定义有效节点而不丢弃组织它们的拓扑结构，为神经状态动力学研究提供了更稳定、更原理性的基础，并有望推动跨数据集与记录系统的统一比较。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统EEG微状态分析中模板定义对预处理敏感，影响可重复性与跨研究比较。
method: 从拓扑几何角度将模板视为嵌入全局状态空间的界标，保留极性作为几何关系。
result: 基于界标的状态定义在捕捉状态结构和分析性能上优于传统聚类模板。
conclusion: 从模板到界标的转换，为神经状态定义提供了更稳定、更原则的基础。
---

## 摘要
状态转换方法，包括脑电图微状态分析和相关功能磁共振成像方法（如隐马尔可夫模型和共激活模式分析），为将神经动力学粗粒化为一小组准稳定状态提供了广泛使用的工具。其效用已在静息态和任务范式中得到证明，应用范围从认知神经科学到精神疾病和神经系统疾病的候选生物标志物。然而，一个根本性的局限性仍然存在：几乎所有下游时间测量都依赖于最初定义的模板图。在传统流程中，模板源自全局场功率峰值处电压图的极性不变聚类，使得最终的状态定义对预处理、采样、初始化、聚类算法以及聚类数量的选择敏感。因此，该方法捕获了脑电图动力学中的粗略规律，而对产生这些状态的更大几何组织仅施加了较弱的约束。这种模板依赖性对可重复性以及跨研究和脑电图电极帽的比较构成了重大挑战。在这里，我们从拓扑几何视角重新审视这个问题。我们不将模板视为从全局场功率峰值图中提取的聚类中心，而是将其作为嵌入在状态空间全局结构中的地标，该状态空间由头皮电压图之间的相互相似性构建。在这种表述中，微状态模板被重新发现为组织连续神经状态地形学的主要轴线的离散代表。这种重新表述保留了极性作为一种有意义的几何关系，而不是一开始就将其作为分析冗余消除。它还将注意力从孤立的状态标签转移到状态空间本身的地形：即局部状态变得可解释的更广泛的关系结构。使用这种方法，我们展示了基于地标的状态定义在捕捉状态结构和提高分析性能方面优于传统模板。这些发现表明，脑电图微状态分析的核心问题比聚类优化更广泛：它涉及如何定义有效节点以粗粒化连续动力学，同时不丢弃组织它们的拓扑结构。通过将微状态分析的概念基础从模板转移到地标，本方法为状态定义提供了更原则性和可能更稳定的基础，包括在功能磁共振成像中。这种拓扑几何重新评估扩展了传统的微状态分析，并为跨数据集、范式和记录系统进行更统一的比较开辟了道路。

## Abstract
State-transition approaches, including EEG microstate analysis and related fMRI methods such as hidden Markov models (HMMs) and co-activation pattern (CAP) analysis, provide widely used tools for coarse-graining neural dynamics into a small set of quasi-stable states. Its utility has been demonstrated across resting-state and task paradigms, with broad applications ranging from cognitive neuroscience to candidate biomarkers for psychiatric and neurological disorders. A fundamental limitation remains, however: nearly all downstream temporal measures are conditional on the template maps defined at the outset. In the conventional pipeline, templates are derived from polarity-invariant clustering of voltage maps at global field power (GFP) peaks, making the resulting state definitions sensitive to preprocessing, sampling, initialization, clustering algorithms, and the choice of cluster number. Consequently, the method captures coarse regularities in EEG dynamics, while only weakly constraining the larger geometric organization from which those states emerge. This template dependence poses a major challenge for reproducibility and for comparisons across studies and EEG caps. Here, we revisit this problem from a topological-geometric perspective. We treat templates not as cluster centroids extracted from GFP-peak maps, but as landmarks embedded in the global structure of a state space constructed from mutual similarities among scalp voltage maps. In this formulation, microstate templates are rediscovered as discrete representatives of dominant axes that organize continuous neural-state topography. This reformulation preserves polarity as a meaningful geometric relation instead of eliminating it at the outset as analytical redundancy. It also shifts attention from isolated state labels to the terrain of the state space itself: the broader relational structure within which local states become interpretable. Using this approach, we show that landmark-based state definitions outperform conventional templates in capturing state structure and improving analytical performance. These findings suggest that the central problem in EEG microstate analysis is broader than clustering optimization: it concerns how to define valid nodes for coarse-graining continuous dynamics without discarding the topology that organizes them. By shifting the conceptual basis of microstate analysis from templates to landmarks, the present approach provides a more principled and potentially more stable foundation for state definition, including in fMRI. This topolo-geometric reappraisal extends conventional microstate analysis and opens a path toward more unified comparisons across datasets, paradigms, and recording systems.