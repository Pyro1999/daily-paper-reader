---
title: Selective Auditory Attention Decoding with a Two-Node Wireless EEG Sensor Network
title_zh: 使用双节点无线脑电图传感器网络的选择性听觉注意力解码
authors: "Geirnaert, S., Ding, R., Bertrand, A."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.17.706305v2.full.pdf"
tags: ["query:pbci-load"]
score: 7.0
evidence: 无线脑电图被动脑机接口用于注意力解码
tldr: "选择性听觉注意解码（sAAD）需可穿戴EEG设备。本研究使用双节点无线EEG传感器网络（WESN），每耳提供4通道，实现样本级同步。基于相关性解码，60秒决策窗口平均准确率69.24%，经隐马尔可夫模型后处理稳态达77.17%，且双耳配置因冗余性优于单耳。证实了完全无线耳周WESN用于sAAD的实用可行性。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有sAAD依赖有线EEG，缺乏可穿戴无线方案，限制实际应用。
method: 采用两节点无线耳周EEG传感器，每耳4通道，样本级同步后组成8通道，基于相关性解码并加入HMM后处理。
result: "60秒窗口平均准确率69.24%，HMM后处理稳态77.17%，双耳优于单耳，固定双极配置即可维持性能。"
conclusion: 无线耳周WESN可实现可靠的sAAD，为神经引导助听设备提供实用硬件基准。
---

## 摘要
选择性听觉注意力解码（sAAD）通过从脑电图（EEG）记录的神经活动中识别多说话者环境中的注意说话者，实现神经导向助听设备。尽管算法有所进展，但由于缺乏可穿戴、不显眼且完全无线的EEG采集解决方案，实际部署仍然受限。因此，本研究旨在评估在由微型化、电流隔离的EEG传感器节点组成的无线EEG传感器网络（WESN）所施加的现实硬件约束下，能否实现可靠的sAAD。这里，我们使用这样一个由两个同步、紧凑的耳周EEG传感器节点组成的WESN，双侧佩戴。每个节点提供四个局部EEG通道，来自五个预凝胶电极，包括一个局部参考。两个节点数据的逐样本无线同步使得联合处理成为八通道EEG。在使用该设置采集的新记录数据集上，基于相关性的刺激解码在60秒决策窗口上实现了平均69.24%的sAAD准确率，与测量长距离头皮电位的有线耳周EEG系统相当。基于隐马尔可夫模型的后处理进一步将稳态准确率提高到77.17%，平均模拟注意力切换检测时间为32.79秒。双耳传感器节点的组合优于单耳配置，主要是通过提供冗余来增强鲁棒性，而非利用互补空间信息。最后，我们表明，每耳使用四个电极的固定双极配置（产生三个通道）足以保持性能。这些结果证明了使用完全无线、电流隔离的耳周WESN进行sAAD的实际可行性，并在实际硬件约束下建立了现实的性能基准。

## Abstract
Selective auditory attention decoding (sAAD) enables neuro-steered hearing devices by identifying the attended speaker in a multi-speaker environment from neural activity recorded with electroencephalography (EEG). Despite algorithmic progress, practical deployment remains constrained by a lack of wearable, unobtrusive, and fully wireless EEG acquisition solutions. Therefore, this work aims to evaluate whether reliable sAAD can be achieved under realistic hardware constraints imposed by using a wireless EEG sensor network (WESN) consisting of miniaturized, galvanically isolated EEG sensor nodes. Here, we use such a WESN consisting of two synchronized, compact around-ear EEG sensor nodes worn bilaterally. Each node provides four local EEG channels derived from five pre-gelled electrodes, including a local reference. Sample-wise wireless synchronization of data from both nodes enables joint processing as an eight-channel EEG. On a newly recorded dataset acquired with this setup, correlation-based stimulus decoding achieves an average sAAD accuracy of 69.24% on 60s decision windows, comparable to wired around-ear EEG systems that measure long-distance scalp potentials. Hidden Markov model-based post-processing further improves to a steady-state accuracy of 77.17% with an average simulated attention switch detection time of 32.79s. Combining sensor nodes at both ears outperforms single-ear configurations, primarily by providing redundancy that increases robustness rather than by exploiting complementary spatial information. Finally, we show that a fixed bipolar configuration using four electrodes per ear, yielding three channels, suffices to maintain performance. These results demonstrate the practical feasibility of sAAD using a fully wireless, galvanically isolated around-ear WESN and establish a realistic performance benchmark under practical hardware constraints.