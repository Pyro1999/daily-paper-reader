---
title: A Simple Subject Independent Channel Selection in EEG for Motor Imagery Task
title_zh: 一种简单的用于运动想象任务的脑电信号中独立于被试的通道选择方法
authors: "Dev, R., Kumar, S., Gandhi, T. K."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.26.734867v1.full.pdf"
tags: ["query:robust-eeg"]
score: 6.0
evidence: 面向脑机接口的独立于被试的脑电通道选择方法
tldr: "运动想象脑电分类中，现有通道选择方法依赖被试和任务。本文提出一种无主题依赖的通道选择，基于各通道与参考通道Cz的差异度进行排序，差异越小越相关。结合带通滤波、共空间模式滤波和SVM/1-NN/5-NN分类器评估。在PhysioNet和BCI Competition数据集上，仅用20/118或16/64通道，精度比3通道高15-20%，仅比全通道低2.91%，显著优于CSP Rank等传统方法。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有脑电通道选择方法依赖被试和任务，缺乏通用性，且通道组合搜索是组合优化难题。
method: 先基于各通道与参考通道Cz的差异度排序，选择差异最小的通道；再使用带通滤波、共空间模式滤波和SVM/1-NN/5-NN分类器评估。
result: "在BCI Competition数据上用20/118通道精度比3通道高15.21%，仅比全通道低2.91%；在PhysioNet上用16/64通道高19.64%。"
conclusion: 基于通道间差异度排序的无主题依赖通道选择方法有效且通用，优于CSP Rank等传统模型。
---

## 摘要
通过脑电信号对运动想象任务进行分类在脑机接口和康复工程中具有重要价值。用于运动想象任务分类的脑电通道选择是一个被充分讨论的问题，但由于其组合性质而具有挑战性。大多数现有方法是依赖于被试和任务的。本文引入了一种独立于被试的脑电通道选择方法。所提出的方法包括两个阶段。首先，我们根据通道与参考通道Cz的差异度对通道进行排名。我们假设与Cz差异较小的通道与运动想象任务分类更相关。在第二阶段，我们采用一个三阶段特征选择和分类模型来评估所选通道。它包括一个带通滤波器，随后是共空间模式（CSP）滤波器和三个分类器，即SVM、1-NN和5-NN。使用两个公开数据集（PhysioNet和BCI Competition III IVa数据集）来评估该方法。在BCI Competition数据上，使用仅20/118个通道，它的性能比3Cs方法高出15.21%，仅比全通道准确率低2.91%；在PhysioNet数据集上使用16/64个通道，比3Cs方法高出19.64%。经验比较表明，该方法明显优于经典模型如CSP Rank、Fisher秩和归一化互信息。结果支持我们的假设：通道与参考通道Cz之间的差异度可以作为通道选择的排名度量。

## Abstract
Classification of motor imagery (MI) tasks through EEG is valuable in brain-computer interfacing and rehabilitation engineering. EEG channels selection for MI task classification is well discussed problem and is challenging due to its combinatorial nature. Most of the existing methods are subject and task-dependent. This paper introduces a subject-independent EEG channel selection. The proposed approach consists of two stages. First, we rank channels based on their divergence from a reference channel Cz. We hypothesize that channels less divergent from Cz are more relevant for MI task classification. In the second stage, we employ a three-stage feature selection and classification model to evaluate the selected channels. It consists of a bandpass filter, followed by common spatial pattern (CSP) filter and three classifiers viz. SVM, 1-NN and 5-NN. Two publicly available datasets viz. PhysioNet and BCI Competition III IVa datasets have been used to assess the method. It performs 15.21% more than 3Cs and just 2.91% less than all-channels accuracy with as few as 20/118 channels on BCI Competition data and 19.64% more than 3Cs on the PhysioNet dataset with 16/64 channels. Empirical comparison implies that the method performs better than classical models such as CSP Rank, fishers rank, and normalized mutual information, significantly. Results support that our hypothesis that divergence between channels and a reference channel Cz can be used as a ranking measure for channel selection.