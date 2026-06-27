---
title: aNy-way ICA and its application to estimate cortico-thalamo-cerebellar functional links in schizophrenia
title_zh: aNy-way ICA及其在精神分裂症中估计皮层-丘脑-小脑功能连接的应用
authors: "Duan, K., Silva, R. F., Rahaman, M. A., Fu, Z., Liu, J., Kochunov, P., van Erp, T. G. M., Shultz, S., Calhoun, V. D."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.1101/2025.06.02.657541v2.full.pdf"
tags: ["query:robust-eeg"]
score: 7.0
evidence: 提出的aNy-way ICA方法可应用于EEG伪影去除
tldr: 多模态数据融合面临尺度与模型阶数不同、正交约束等挑战。本文提出aNy-way ICA，通过高斯独立向量分析优化载荷相关性，结合独立ICA保证独立性，支持不同模态灵活阶数且无需正交约束。仿真表明其在噪声下较现有方法更准确；应用于精神分裂症fMRI数据，识别出皮层-丘脑-小脑环路，该连接异常与认知缺陷相关，并在独立数据集复现，为理解“认知失调”提供了新视角。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有数据融合方法要求各模态同阶数或正交约束，难以灵活利用多模态互补信息，需一种高效、适应不同模型阶数的融合框架。
method: 提出aNy-way ICA，通过IVA-G优化全局载荷相关性，同时对各模态独立进行ICA，允许不同模态不同阶数且无正交限制，实现多源检测。
result: 仿真中噪声环境下识别精度优于对比方法；应用在精神分裂症两组独立fMRI数据中，一致发现高阶丘脑-视觉皮层-默认模式网络-小脑后叶的功能连接异常，且与认知缺陷相关。
conclusion: aNy-way ICA提供灵活高效的多模态融合工具，揭示了精神分裂症皮层-丘脑-小脑环路异常可能是“认知失调”的神经基础，具有潜在诊断价值。
---

## 摘要
国际和国家生物样本库收集的多模态数据具有不同的尺度和模型阶数，并为疾病机制提供独特且互补的见解。我们提出了一种新颖、灵活且高效的数据融合方法——任意维度独立成分分析（aNy-way ICA）。aNy-way ICA通过高斯独立向量分析（IVA-G）优化链接分量的整体载荷相关结构，同时通过独立的ICA优化独立性，从而融合N维多模态或多领域数据。该方法允许不同模态/领域具有不同的模型阶数，并能检测任意数量的模态或领域中的多个链接源，而无需对源施加正交性约束。模拟结果表明，与其他方法相比，aNy-way ICA能够以更高的准确度识别设计的源和载荷以及真实的协方差模式，尤其是在噪声条件下。将aNy-way ICA应用于融合精神分裂症患者的4维多领域fMRI数据，我们识别出皮层-丘脑-小脑回路，突显了高阶丘脑核团、视觉皮层、默认模式网络和小脑后叶之间的功能连接。这些功能连接在两个独立数据集中得到了重复验证。高阶丘脑核团、视觉皮层和默认模式网络之间的连接能够区分精神分裂症患者与对照组，并且这种异常连接在发现和验证数据集中与多种认知缺陷相关，表明所识别的皮层-丘脑-小脑回路可能是精神分裂症中“认知共济失调”的基础。

## Abstract
Multimodal data collected by international and national biobanking efforts have distinct scales and model orders and provide unique and complementary insights into disease mechanisms. We propose a novel, flexible and efficient data fusion approach, aNy-way independent component analysis (aNy-way ICA). aNy-way ICA fuses N-way multimodal or multidomain data by optimizing the entire loading correlation structure of linked components via Gaussian independent vector analysis (IVA-G) and simultaneously optimizing independence via separate ICAs. This allows for distinct model orders for different modalities/domains and multiple linked sources detection across any number of modalities or domains without requiring orthogonality constraints on sources. Simulation results demonstrate that aNy-way ICA identifies the designed sources and loadings, as well as the true covariance patterns, with improved accuracy compared to other approaches, especially under noisy conditions. Applying aNy-way ICA to fuse 4D multi-domain fMRI data in schizophrenia, we identified a cortico-thalamo-cerebellar circuit, highlighting the functional linkages among higher order thalamic nuclei, the visual cortex, default mode network, and the posterior lobe of cerebellum. Their function links were replicated in two independent datasets. The connection among higher order thalamic nuclei, the visual cortex, and default mode network discriminates schizophrenia from controls and this aberrant connection is related to multiple cognitive deficits in both discovery and replication datasets, indicating the identified cortico-thalamo-cerebellar circuit may underlie "cognitive dysmetria" in schizophrenia.