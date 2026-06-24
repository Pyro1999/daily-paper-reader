---
title: Quantum machine learning for detection of sleep deprivation from EEG signals
title_zh: 基于量子机器学习的脑电图信号睡眠剥夺检测
authors: "Sarma-Sarkar, P., Saini, R., Roy, P. P."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732153v1.full.pdf"
tags: ["query:pbci-load"]
score: 7.0
evidence: 使用EEG和量子机器学习检测认知状态，与认知负荷评估相关
tldr: "针对睡眠剥夺影响认知与健康的问题，本研究利用EEG信号检测睡眠状态。通过提取频谱功率、Hjorth参数和功能连接等特征，并编码为量子态，构建了量子支持向量机（QSVM）和混合量子神经网络（HQNN）模型。HQNN在epoch级和subject级评估中分别达到96.88%和81.25%的准确率，优于此前方法。结果表明量子机器学习在EEG睡眠剥夺检测中具有竞争力和实际应用潜力。"
source: biorxiv
selection_source: fresh_fetch
motivation: 睡眠剥夺普遍影响认知与健康，EEG能客观捕捉神经变化，但传统方法性能有限，亟需更有效的自动检测模型。
method: 提取EEG的频谱带功率、带比、Hjorth参数和功能连接特征，编码为量子态构建量子核，使用QSVM和HQNN分类。
result: "HQNN在epoch级准确率96.88%，subject级81.25%；QSVM分别为93.75%和75.00%，均优于此前最佳结果（68.23%和95.72%）。"
conclusion: 量子机器学习可有效提升EEG睡眠剥夺检测性能，为实际生物医学应用提供新途径。
---

## 摘要
据估计，印度约有50%的人口存在睡眠相关障碍。睡眠剥夺是一种普遍存在的状况，会对认知表现、神经功能和整体健康产生不利影响。脑电图（EEG）提供了一种客观捕捉与睡眠缺失相关的神经变化的方法，因此非常适合用于自动化检测框架。在本研究中，我们探索了应用量子支持向量机和混合量子神经网络，利用静息态脑电图信号对睡眠剥夺状态和充分休息状态进行分类。

我们采用了全面的特征提取流程，包括频谱带功率、频带比率、Hjorth参数和功能连接性度量。这些特征随后被编码成量子态以构建量子核，进而用于分类。模型性能在时期级和受试者级两种数据划分方案下进行评估。

混合量子神经网络（HQNN）在两种评估设置下均取得了最高性能，在时期级和受试者级分别达到了96.88%和81.25%的准确率。QSVM模型在时期级和受试者级评估中分别达到了93.75%和75.00%的准确率。在受试者级和时期级评估中，HQNN的性能超过了先前报告的结果（68.23%和95.72%）。总体而言，这些发现突显了量子机器学习作为基于脑电图的睡眠剥夺检测的一种有竞争力方法的潜力，对现实世界的生物医学应用具有广阔前景。

## Abstract
Approximately 50% of the population in India is estimated to experience sleep-related disorders. Sleep deprivation is a prevalent condition that adversely impacts cognitive performance, neural functioning, and overall health. Electroencephalography (EEG) offers an objective means of capturing neural alterations associated with sleep loss, making it well-suited for automated detection frameworks. In this study, we explore the application of a Quantum Support Vector Machine and Hybrid Quantum Neural Networks to classify sleep-deprived and well-rested states using resting-state EEG signals.

A comprehensive feature extraction pipeline is employed, incorporating spectral band power, band ratios, Hjorth parameters, and functional connectivity measures. These features are subsequently encoded into quantum states to construct a quantum kernel, which is then utilized for classification. Model performance is evaluated under both epoch-level and subject-level data partitioning schemes.

The Hybrid Quantum Neural Network (HQNN) achieves the highest performance across both evaluation settings, attaining an accuracy of 96.88% at the epoch level and 81.25% at the subject level. The QSVM model achieves accuracies of 93.75% and 75.00% for epoch-level and subject-level evaluations, respectively. At subject-level and epoch -level evaluation, HQNN outperforms previously reported results (68.23% and 95.72%). Overall, these findings highlight the potential of quantum machine learning as a competitive approach for EEG-based sleep deprivation detection, with promising implications for real-world biomedical applications.