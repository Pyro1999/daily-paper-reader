---
title: Preventing Data Leakage in Neural Decoding
title_zh: 防止神经解码中的数据泄露
authors: "Wong, R., McCullough, M. H., Lu, T., Zhu, S. I., Goodhill, G. J."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.26.701583v2.full.pdf"
tags: ["query:pbci-load"]
score: 6.0
evidence: 防止神经解码中的数据泄露，与被动BCI认知负荷评估的深度学习相关
tldr: 神经解码研究中，数据泄漏会污染训练集导致性能估计偏差甚至错误结论。常见预处理（如降维）和自相关时间序列的交叉验证均可能引入泄漏。泄漏有时反常地降低解码性能，而随机k折交叉验证会高估性能。本文通过理论分析和实验揭示了这些现象，并给出了避免泄漏的具体建议。
source: biorxiv
selection_source: fresh_fetch
motivation: 数据泄漏在神经解码中普遍存在且未被充分认识，亟需系统分析其对性能估计的影响。
method: 分析监督/无监督降维等预处理及自相关时间序列交叉验证中的泄漏机制，结合理论推导和实验验证。
result: 泄漏可导致性能低估（降维场景）或高估（自相关时间序列交叉验证），与常见认知相反。
conclusion: 提出了避免数据泄漏的详细操作建议，确保神经解码研究的可靠性。
---

## 摘要
神经解码是一种广泛使用的机器学习技术，用于研究行为、感知和认知如何在神经活动中表示。然而，如果不谨慎应用，可能会出现数据泄露，即测试集的信息污染了训练集，导致解码性能估计有偏，并可能使生物学结论无效。在这里，我们展示数据泄露可能通过常见的监督和无监督预处理步骤（包括降维）引入神经解码研究。我们揭示，在某些情况下，与无偏估计相比，数据泄露可能会矛盾地降低解码性能，并提供理论分析解释这是如何发生的。我们还表明，对于自相关的神经时间序列，随机k折交叉验证可能会极大地夸大解码性能。基于这些发现，我们提供了避免神经解码中数据泄露的详细建议。

## Abstract
Neural decoding is a widely-used machine learning technique for investigating how behavior, perception and cognition are represented in neural activity. However without careful application data leakage can occur, where information from the test set contaminates the training set, leading to biased estimates of decoding performance and potentially invalidating biological conclusions. Here we show that leakage can be introduced in neural decoding studies by common supervised and unsupervised preprocessing steps, including dimensionality reduction. We reveal that in some cases leakage can paradoxically decrease decoding performance relative to unbiased estimates, and we provide theoretical analyses explaining how this occurs. We also show that, for autocorrelated neural time series, randomized k-fold cross-validation can dramatically overstate decoding performance. Based on these findings, we provide detailed recommendations for avoiding data leakage in neural decoding.