---
title: "Data aggregation strategies for a P300 speller: decoding models, epoch averaging, cross-subject ensembles, and multi-channel models"
title_zh: P300拼写器的数据聚合策略：解码模型、周期平均、跨被试集成与多通道模型
authors: "Sidorov, L., Makarova, A., Maysuradze, A., Lebedev, M."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.732982v1.full.pdf"
tags: ["query:pbci-load"]
score: 6.0
evidence: P300拼写器EEG解码，使用深度学习模型，与被动脑机接口相关
tldr: P300脑电信号解码面临信噪比低和个体差异大的挑战。本研究系统比较了多种数据聚合策略，在10名受试者数据集上使用EEGNet、BaseCNN和SVM模型。结果表明单试次ITR仅0.15-0.64 bits/trial，而受控聚合可提升性能。跨受试者组合（每个参与者K=3试次，30通道）在多通道EEGNet下达到最高ITR 0.95-0.97 bits/聚合决策，接近理论极限。该工作为多受试者脑机接口的P300解码提供了有效策略。
source: biorxiv
selection_source: fresh_fetch
motivation: 单试次P300检测准确率低，亟需高效数据聚合方法提升解码性能。
method: 对比7种聚合策略，包括单受试者模型、Epoch平均、跨受试者集成、多通道模型等，使用EEGNet、BaseCNN和SVM评估。
result: 跨受试者K=3试次组合结合多通道EEGNet实现最高ITR 0.95-0.97 bits/决策，优于随机混合和简单平均。
conclusion: 受控跨受试者聚合与多通道架构可有效提升P300解码性能，适用于多用户脑机接口。
---

## 摘要
由于低信噪比和显著的被试间变异性，从头皮脑电图（EEG）中准确检测P300事件相关电位在小样本试验中仍然具有挑战性。本研究系统比较了提升P300分类的数据聚合策略，在10名被试的数据集上使用两种卷积神经网络架构（EEGNet和BaseCNN）以及支持向量机（SVM）进行评估。我们比较了：(1) 针对单次试验的被试特定模型与通用池化模型；(2) 使用5次和10次刺激重复的周期平均；(3) 将被试对应不同输入通道的多通道模型；(4) 跨被试平均；(5) 混合（非受控）平均；(6) 所有参与者中每个被试取K次试验的组合方法；(7) 来自扩展单次试验历元的时移通道。解码性能通过信息传输率（ITR）量化，基于二分类准确率计算。我们发现单次试验ITR不实用（0.15–0.64比特/次试验），而受控聚合提升了性能。每个参与者取K=3次试验（30通道）的组合跨被试方法与多通道EEGNet实现了最高ITR：在无孔径记录中为0.95比特/聚合决策，在有孔径数据中为0.97比特/聚合决策，接近聚合决策的理论二分类极限。受控跨被试平均始终优于随机试验混合，且当保持被试间结构时，多通道架构优于简单平均。这些发现有助于改进P300解码并实现多被试脑机接口（BCI）。

## Abstract
Accurate detection of P300 event-related potentials from electroencephalography (EEG) remains challenging for small numbers of trials due to low signal-to-noise ratios and substantial inter-subject variability. This study presents a systematic comparison of data aggregation strategies for improving P300 classification, evaluated on a 10-subject dataset using two convolutional neural network architectures (EEGNet and BaseCNN) and a support vector machine (SVM). We compared: (1)~subject-specific and pooled general models for single trials; (2)~epoch averaging with 5 and 10 stimuli repetitions; (3)~multi-channel models where subjects corresponded to different input channels; (4)~cross-subject averaging; (5)~mixed (uncontrolled) averaging; (6)~a combined approach with $K$ trials per subject across all participants; and (7)~time-shifted channels from extended single-trial epochs. Decoding performance was quantified using the Information Transfer Rate (ITR), computed for binary classification accuracy. We found that single-trial ITR was unpractical (0.15--0.64~bits/trial), whereas controlled aggregation improved the performance. The combined cross-subject approach with $K=3$ trials per participant (30 channels) achieves the highest ITR with multi-channel EEGNet: 0.95~bits/aggregated decision in the no-aperture recordings and 0.97~bits/aggregated decision on Aperture data, approaching the theoretical binary-classification limit for the aggregated decision. Controlled cross-subject averaging consistently outperformed random trial mixing, and multi-channel architectures outperformed simple averaging when inter-subject structure was preserved. These findings contribute to improving P300 decoding and implementing multi-subject brain-computer interfaces (BCIs).