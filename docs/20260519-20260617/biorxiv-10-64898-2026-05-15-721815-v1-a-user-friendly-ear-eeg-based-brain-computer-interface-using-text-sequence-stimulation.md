---
title: A User-Friendly Ear-EEG-Based Brain-Computer Interface Using Text Sequence Stimulation
title_zh: 一种基于文本序列刺激的用户友好型耳部脑机接口
authors: "Li, X., Xu, Z., Li, B., Wang, Y., Gao, X."
date: 2026-05-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.15.721815v1.full.pdf"
tags: ["query:robust-eeg"]
score: 7.0
evidence: 耳部脑机接口使用文本序列刺激以改善低信噪比
tldr: "传统耳戴式脑机接口采用亮度调制稳态视觉诱发电位范式，存在信噪比低和用户适应率差的问题。本研究提出文本序列刺激范式，利用腹侧视觉通路对自然文本的响应特性，通过离线优化确定4.6-6.8 Hz频率与0.25π相位偏移的刺激参数，构建12目标BCI系统。在线实验表明，文本序列刺激的平均信息传输率达44.59 bits/min，比亮度调制提升76.18%，且所有14名参与者的准确率均超过70%（平均86.37%），而亮度调制下50%用户准确率低于70%。该方法将闪烁面积减少14%，模拟阅读时的自然亮度变化，显著提升了视觉舒适度和BCI实用性。"
source: biorxiv
selection_source: fresh_fetch
motivation: 传统亮度调制SSVEP在耳戴式EEG中信噪比低且文盲率高，需设计更友好的刺激范式以提升性能。
method: 提出文本序列刺激范式，通过离线频率扫描确定最优参数（4.6-6.8 Hz，0.25π相位偏移），集成12目标在线BCI系统。
result: "文本序列刺激平均ITR达44.59 bits/min，比亮度调制高76.18%；所有参与者准确率≥70%，平均86.37%。"
conclusion: "文本序列刺激范式在减少闪烁面积14%的同时显著提升性能和舒适度，为耳戴式BCI提供实用方案。"
---

## 摘要
背景与传统的头皮脑电图系统相比，基于耳部脑电图的脑机接口（BCI）提供了更好的可穿戴性和舒适性。然而，在传统的亮度调制稳态视觉诱发电位（SSVEP）范式下，其性能受到低信噪比和高BCI文盲率的限制。方法本研究引入了一种文本序列刺激范式，通过利用靠近耳朵的电极更容易获取的腹侧视觉通路响应来解决这些限制。通过离线频率扫描实验（4-8 Hz），我们确定了最佳刺激参数（4.6-6.8 Hz，相位偏移0.25π），并将其集成到一个12目标BCI系统中。我们进一步进行了在线实验，以比较所提出的文本序列范式和传统亮度刺激之间的响应特性和实时拼写性能。结果与14名参与者的对比实验表明，文本序列刺激实现了44.59 ± 10.50比特/分钟的平均信息传输速率（ITR），在ITR上比亮度调制提高了76.18%。值得注意的是，文本序列刺激有效缓解了BCI文盲率，所有参与者的准确率均接近或超过70%（平均值：86.37 ± 9.61%）。相比于亮度调制（其中50%的用户准确率低于70%），这代表了显著的改进。结论通过将闪烁区域减少14%并模拟阅读过程中发生的自然亮度变化，所提出的方法增强了视觉舒适度。在线结果进一步验证了文本序列刺激作为耳部脑电BCI的一种高性能且用户友好的范式，支持其在辅助应用中的实用性。

## Abstract
BackgroundEar-EEG-based brain-computer interfaces (BCIs) provide improved wearability and comfort compared to traditional scalp-EEG systems. However, their performance is constrained by low signal-to-noise ratios (SNRs) and high rates of BCI illiteracy under conventional luminance-modulated steady-state visual evoked potential (SSVEP) paradigms.

MethodsThis study introduces a text-sequence stimulation paradigm to address these limitations by leveraging ventral visual pathway responses that are more accessible to electrodes near the ear. Using offline frequency-sweeping experiments across 4-8 Hz, we identified optimal stimulus parameters (4.6-6.8 Hz with 0.25{pi} phase shifts) and integrated them into a 12-target BCI system. We further conducted online experiments to compare the response characteristics and real-time spelling performance between the proposed text-sequence paradigm and conventional luminance stimulation.

ResultsComparative experiments with 14 participants demonstrate that text sequence stimuli achieve an average information transfer rate (ITR) of 44.59 {+/-} 10.50 bits/min, outperforming luminance modulation by 76.18% in ITR. Notably, text sequence stimulation effectively mitigated BCI illiteracy, with all participants achieving near or above 70% accuracy (mean: 86.37 {+/-} 9.61%). This represents a significant improvement over luminance modulation, where 50% of users fell below 70% accuracy.

ConclusionsBy reducing the flicker area by 14% and mimicking the natural luminance variations that occur during reading, the proposed method enhanced visual comfort. The online results further validate text-sequence stimulation as a high-performance and user-friendly paradigm for ear-EEG BCIs, supporting their practicality for assistive applications.