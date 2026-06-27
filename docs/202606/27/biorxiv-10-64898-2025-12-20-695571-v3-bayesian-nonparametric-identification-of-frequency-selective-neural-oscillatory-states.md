---
title: Bayesian Nonparametric Identification of Frequency-Selective Neural Oscillatory States
title_zh: 贝叶斯非参数方法识别频率选择性神经振荡状态
authors: "Yamada, S., Nagel, S. E., Kobeleva, X., Schmidt, R."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2025.12.20.695571v3.full.pdf"
tags: ["query:pbci-load"]
score: 7.0
evidence: 贝叶斯无参数方法识别与认知负荷相关的神经振荡状态
tldr: 神经振荡识别面临频带预定义和状态数量未知的挑战。本文提出贝叶斯非参数方法，结合时间延迟嵌入与狄利克雷过程高斯混合模型，自动推断振荡状态数量并捕获频域特征。在合成数据和真实MEG数据上，该方法可靠恢复了多个频率成分，发现了个体间异质性的短暂振荡状态。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法需预定义频带或状态数量，易欠拟合或过拟合，无法自适应发现神经振荡状态。
method: 结合时间延迟嵌入与狄利克雷过程高斯混合模型，利用局部自协方差结构和非参数先验自动确定状态数。
result: 在合成数据中可靠恢复多个频率成分；在MEG数据中识别出多种频率选择性的短暂振荡状态，且个体间存在异质性。
conclusion: 提供无需预定义频带或状态数的无监督框架，用于发现频率选择性神经振荡状态。
---

## 摘要
识别神经振荡对于将快速大脑动态与潜在认知过程联系起来至关重要。然而，这具有挑战性，因为振荡事件可能短暂、嵌入在类似1/f的背景活动中，并可能包含未知数量的频谱不同状态。传统方法通常对一或几个预定义频带应用窄带带通滤波器，然后使用幅度阈值识别振荡事件，但检测结果对此类选择高度敏感。尽管最近基于隐马尔可夫模型（HMM）的无监督替代方法解决了这些局限性，但它们仍需要事先指定状态数量，并且当该数量指定错误时可能导致欠拟合或过拟合。我们提出了一种贝叶斯非参数方法，该方法识别不同的振荡状态，同时直接从数据中推断出合适的状态数量。该方法将时间延迟嵌入（TDE）与狄利克雷过程高斯混合模型（DP-GMM）相结合。TDE通过时间平移副本增强信号，使DP-GMM能够捕获特定频率的局部自协方差结构，而狄利克雷过程先验通过修剪非活动成分来适应模型复杂度。我们使用设计用于模拟神经时间序列（如EEG、MEG和局部场电位）的单通道合成数据，其中多个频率成分被类似1/f的噪声掩盖，将该方法与基于滤波器的阈值方法和时间延迟嵌入HMM进行了基准测试。在此设置下，所提出的模型在噪声条件下可靠地恢复了多个不同的频率成分，同时还推断出振荡状态的数量。应用于静息态运动皮层MEG数据集时，该模型识别出多个频率选择性、短暂的振荡状态，以及具有不同频谱特征的明显非周期性状态。这些状态在峰值频率、发生率和功率上表现出显著的个体间异质性。总体而言，这提供了一种无监督框架，用于发现频率选择性振荡状态，而无需预定义频带或固定状态数量。

## Abstract
Identifying neural oscillations is essential for linking fast brain dynamics to underlying cognitive processes. However, this is challenging because oscillatory events can be brief, embedded in 1/f-like background activity, and may comprise an unknown number of spectrally distinct states. Conventional approaches often apply narrowband band-pass filters to one or a few predefined frequency bands and then use amplitude thresholding to identify oscillatory events, but detection outcomes can be highly sensitive to these choices. Although recent unsupervised alternatives based on hidden Markov models (HMMs) address these limitations, they still require the number of states to be specified in advance and can underfit or overfit when this number is misspecified. We propose a Bayesian nonparametric method that identifies distinct oscillatory states while inferring an appropriate number of states directly from the data. This method combines time-delay embedding (TDE) with the Dirichlet-process Gaussian mixture model (DP-GMM). TDE augments the signal with time-shifted copies, enabling the DP-GMM to capture frequency-specific local autocovariance structures, while the Dirichlet-process prior adapts model complexity by pruning inactive components. We benchmarked the approach against a filter-based thresholding method and the time-delay embedded HMM using single-channel synthetic data designed to mimic neural time series (e.g., EEG, MEG, and local field potentials), with multiple frequency components masked by 1/f-like noise. In this setting, the proposed model reliably recovered multiple distinct frequency components under noisy conditions while also inferring the number of oscillatory states. Applied to a resting-state motor-cortex MEG dataset, the model identified multiple frequency-selective, short-lived oscillatory states alongside distinct aperiodic states with different spectral profiles. These states exhibited substantial inter-individual heterogeneity in peak frequency, occurrence rate, and power. Overall, this provides an unsupervised framework for discovering frequency-selective oscillatory states without predefining frequency bands or fixing the number of states.