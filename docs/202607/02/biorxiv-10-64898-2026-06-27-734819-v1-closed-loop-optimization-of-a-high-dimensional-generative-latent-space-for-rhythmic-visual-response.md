---
title: Closed-loop optimization of a high-dimensional generative latent space for rhythmic visual response
title_zh: 高维生成潜空间中节律视觉响应的闭环优化
authors: "Livezey, J. A., Su, Y., Wolfer, S., Ingster, A., Klein, D. J., Hanina, A."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.27.734819v1.full.pdf"
tags: ["query:pbci-load"]
score: 6.0
evidence: 使用非侵入式脑电图进行SSVEP闭环调制，与被动脑机接口相关
tldr: 神经振荡伴随多种认知状态，以往闭环调制主要依赖侵入记录并聚焦发放率。本文利用非侵入性EEG测量SSVEP相对功率，在10-40维潜空间中优化图像刺激参数以调节alpha/theta频带。实验在单次会话内成功调制，且优化刺激可泛化至新被试。结果表明闭环刺激优化是非侵入性节律神经调制的有效方法。
source: biorxiv
selection_source: fresh_fetch
motivation: 实现非侵入性、面向节律的视觉响应闭环调制，克服以往依赖侵入记录和发放率最大化的局限。
method: 在alpha和theta频带下，基于EEG的SSVEP功率反馈，在10/20/40维潜空间中通过贝叶斯优化迭代更新图像刺激参数。
result: 优化刺激显著调制SSVEP相对功率，并在开环中泛化至新被试；特征分析发现低频空间功率对theta和alpha有相反驱动作用。
conclusion: 闭环刺激优化是一种可行的非侵入性神经调制方法，可用于调节节律性视觉响应。
---

## 摘要
神经振荡伴随多种认知状态和行为，包括感知、记忆和运动，对它们的调节在基础神经科学和临床研究中日益受到关注。以往对视觉神经反应进行闭环调节的演示主要依赖于侵入性记录，并侧重于发放率最大化而非节律性调节。在此，我们展示了使用易于获得的非侵入性脑电图测量的稳态视觉诱发电位（SSVEP）的相对功率，可以在单次实验中对单个参与者通过图像刺激参数进行闭环调节。在α和θ波段的闪烁频率刺激优化在10、20和40维潜在空间中均获得了成功。我们还表明，优化后的刺激在开环条件下对新参与者具有泛化能力。最后，我们描述了调节相对SSVEP功率的视觉特征，并发现图像中的低频空间功率以相反方向驱动θ和α。总之，我们的结果表明，闭环刺激优化是利用非侵入性神经成像方法进行节律性神经调节的可行方法。

## Abstract
Neural oscillations accompany a wide range of cognitive states and behaviors including perception, memory, and movement, and modulating them is of growing interest for both basic neuroscience and clinical research. Previous demonstrations of closed-loop modulation of visual neural responses mainly relied on invasive recordings and focused on firing-rate maximization rather than rhythmic modulation. Here, we show that the relative power of steady-state visual evoked response (SSVEP), measured with readily-available, non-invasive electroencephalography, can be modulated in closed-loop as a function of image stimulus parameters for single participants within a single session. Stimulus optimization with flicker frequencies in the alpha and theta bands was successful in 10, 20, and 40 dimensional latent spaces. We also show that optimized stimuli generalize to new participants when shown in open-loop. Finally, we characterize the visual features that modulate relative SSVEP power and find that low-frequency spatial power in the image drives theta and alpha in opposite directions. Together, our results show that closed-loop stimulus optimization is a viable method for rhythmic neural modulation using noninvasive neuroimaging methods.