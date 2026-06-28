---
title: Uncovering dynamic human brain phase coherence networks
title_zh: 揭示动态人类脑相位相干网络
authors: "Olsen, A. S., Brammer, A., Fisher, P. M., Moerup, M."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.1101/2024.11.15.623830v5.full.pdf"
tags: ["query:robust-eeg"]
score: 7.0
evidence: 基于相位的混合建模，可对抗噪声和伪迹，实现鲁棒连接分析
tldr: 传统功能脑连接分析依赖信号幅度相关性，易受噪声和头动干扰。本文提出基于信号相位的方法，引入复杂角中心高斯混合模型，直接研究脑相位相干网络的整体动态模式。应用于fMRI数据，模型识别出可重复的脑同步状态，能可靠区分认知任务，且无需训练标签即可泛化至新个体。该方法为研究大规模神经协调提供了清洁且信息丰富的视角。
source: biorxiv
selection_source: fresh_fetch
motivation: 克服传统幅度相关性分析对噪声敏感、难以捕捉脑动态同步的局限。
method: 提出复杂角中心高斯混合模型，对脑信号相位进行数学建模，分析全脑相位相干网络动态。
result: 模型识别出可区分认知任务的脑同步状态，并泛化至未见个体，无需任务标签。
conclusion: 信号相位建模提供了研究脑同步动力学的有效新途径，有助于理解大规模神经协调。
---

## 摘要
复杂的认知功能依赖于分布在不同脑区之间的协调通信，然而捕捉这些随时间演变的相互作用仍具挑战。传统的大脑功能连接分析主要依赖信号振幅的相关性，这容易受到噪声和头部运动等伪影的影响。本文引入一种混合建模方法，专注于脑信号的相位，从而能够直接且完整地研究脑相位相干网络中的大规模同步动态模式。我们为相位建模奠定了数学和概念基础，并引入了复角高斯混合模型，为分析全脑基于相位的相互作用提供了有原则的方法。应用于fMRI数据时，该模型识别出全脑同步活动的重复状态，这些状态能够可靠地区分认知任务，并在未见过的个体中泛化，而无需在训练中使用任何任务标签。这些结果表明，信号相位建模提供了关于脑同步动态的清晰且信息丰富的视角，为研究大规模神经协调开辟了新途径。

## Abstract
Complex cognitive functions rely on coordinated communication between distributed brain regions, yet capturing these interactions as they evolve over time remains challenging. Traditional analyses of functional brain connectivity largely rely on correlations in signal amplitude, which are sensitive to noise and artifacts such as head motion. Here, we introduce a mixture modeling approach that focuses on the phase of brain signals, allowing dynamic patterns of large-scale synchronization in brain phase coherence networks to be studied directly and in their entirety. We lay the mathematical and conceptual groundwork for phase modeling and introduce the complex angular central Gaussian mixture model, providing a principled way to analyze phase-based interactions across the brain. Applied to fMRI data, the model identifies recurring states of brain-wide synchronized activity that reliably distinguish cognitive tasks and generalize across previously unseen individuals, without requiring any task labels during training. These results show that modeling signal phase offers a clean and informative view of brain synchronization dynamics, opening new avenues for studying large-scale neural coordination.