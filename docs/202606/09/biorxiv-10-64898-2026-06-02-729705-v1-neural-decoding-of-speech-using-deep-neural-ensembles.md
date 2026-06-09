---
title: Neural decoding of speech using deep neural ensembles
title_zh: 使用深度神经集成进行语音神经解码
authors: "Yoon, S., Avansino, D. T., Madugula, S., Levin, A. D., Fan, C., Abramovich Krasa, B., Singh, A., Vo, C., Hahn, N. V., Card, N. S., Fogg, Z., Wairagkar, M., Nason-Tomaszewski, S. R., Jacques, B. G., Bechefsky, P. H., Iacobacci, C., Deo, D. R., Hochberg, L. R., Brandman, D. M., Stavisky, S. D., Au Yong, N., Pandarinath, C., Henderson, J. M., Willett, F. R."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729705v1.full.pdf"
tags: ["query:pbci-load"]
score: 6.0
evidence: 深度集成用于语音BCI解码
tldr: "语音脑机接口可恢复瘫痪患者的快速沟通，但解码错误限制了性能。深度集成方法通过组合多个独立解码器的预测，在最近比赛中大幅提升准确率，但之前未进行实时测试且计算成本高。本文首次在双侧皮层内微电极阵列参与者中实现闭环深度集成，将大词汇量任务的词错误率从33.7%降至26.0%。通过三名参与者的数据，分析了增益与基线错误率、训练集大小和集成规模的关系，并引入基于测试时增强的高效伪集成方法，在仅需单个解码器的情况下提升准确率，降低了计算负担。结果表明深度集成的优势可在实时和资源约束下实现，推动语音BCI走向临床。"
source: biorxiv
selection_source: fresh_fetch
motivation: 深度集成方法在离线语音解码中表现优异，但未在实时闭环中验证，且计算资源需求高，其临床可行性未知。
method: 首次在双侧皮层内微电极阵列参与者中闭环测试深度集成；分析基线错误率、数据量、集成规模的影响；提出基于测试时增强的伪集成方法降低计算成本。
result: "大词汇量任务词错误率从33.7%降至26.0%；伪集成方法在仅需单个解码器时提升准确率。"
conclusion: 深度集成的实时优势可在资源约束下实现，为语音BCI的临床应用铺平道路。
---

## 摘要
语音脑机接口可以恢复瘫痪患者的快速交流能力，但解码错误仍然限制了其性能。在最近的脑到文本解码竞赛中，深度集成方法（结合多个独立训练的解码器的预测）在准确性上取得了显著提升，并且是超越基线方法的最大收益来源。然而，这些方法此前未在实时场景中测试过，需要大量计算资源，且其在各种临床相关约束下的性能仍不明确。在此，我们首次对一名双侧皮层内微电极阵列的参与者进行了深度集成的闭环测试，在大词汇量任务中，词错误率从33.7%降至26.0%。利用来自三名参与者的额外数据，我们评估了这些增益如何依赖于基线错误率、训练数据集大小和集成大小，包括与现实部署最相关的资源-准确性权衡。最后，我们引入了一种基于测试时增强的计算高效伪集成方法，该方法在仅需单个基础解码器的情况下提高了解码准确性，大大降低了集成的计算负担。这些结果共同表明，深度集成的优势可以在实时和实际资源约束下实现，使语音脑机接口更接近广泛的临床应用。

## Abstract
Speech brain-computer interfaces (BCIs) can restore rapid communication to people with paralysis, but decoding errors still limit performance. In recent brain-to-text decoding competitions, deep ensemble methods, which combine predictions from multiple independently trained decoders, have delivered striking accuracy improvements and account for the largest gains over baseline approaches. However, these methods have not previously been tested in real-time, require substantial computational resources, and their performance under various clinically relevant constraints remains poorly understood. Here, we present the first closed-loop test of deep ensembles in a participant with bilateral intracortical microelectrode arrays, demonstrating a reduction in word error rate from 33.7% to 26.0% on a large-vocabulary task. Using additional data from three participants, we then assess how these gains depend on baseline error rate, training dataset size, and ensemble size, including the resource-accuracy tradeoffs most relevant for real-world deployment. Finally, we introduce a computationally efficient pseudoensembling approach based on test-time augmentation that improves decoding accuracy while requiring only a single base decoder, greatly reducing the computational burden of ensembling. Together, these results show that the benefits of deep ensembling can be realized in real time and under practical resource constraints, bringing speech BCIs closer to broader clinical adoption.