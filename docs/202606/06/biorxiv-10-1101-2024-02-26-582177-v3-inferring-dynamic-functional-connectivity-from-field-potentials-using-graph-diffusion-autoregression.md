---
title: Inferring Dynamic Functional Connectivity from Field Potentials Using Graph Diffusion Autoregression
title_zh: 使用图扩散自回归从场电位推断动态功能连接性
authors: "Schwock, F., Bloch, J., Khateeb, K., Zhou, J., Atlas, L., Yazdan-Shahmorad, A."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.1101/2024.02.26.582177v3.full.pdf"
tags: ["query:pbci-load"]
score: 6.0
evidence: 利用图扩散自回归从场电位推断动态功能连接
tldr: 现有动态功能连接研究多忽略脑结构组织且依赖静态估计。本文提出图扩散自回归模型，在结构连接图上融合扩散约束进行网络约束线性自回归，生成高动态功能连接信号。在模拟数据和猕猴皮层记录中验证，模型能揭示光遗传刺激、中风后静息态变化及任务行为相关的快速神经通信动态。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有静态功能连接无法捕捉神经动态，且缺乏结构信息，亟需能融合结构约束的动态功能连接模型。
method: 在预定义结构连接图基础上，引入图扩散约束构建网络约束线性自回归模型，输出边缘动态功能连接。
result: 在模拟数据和猕猴感觉运动皮层记录中，模型成功描述光遗传、中风后静息态及行为任务中的快速动态变化。
conclusion: 图扩散自回归模型能有效结合结构信息推断动态功能连接，提升对神经过程动态的刻画能力。
---

## 摘要
估计动态功能连接性（dFC）正受到越来越多的关注，这得益于多部位神经记录技术的快速进步以及对认知过程更好理解的努力。然而，大多数研究侧重于功能连接性的静态估计，无法捕捉高度动态的神经过程，同时也忽略了关于大脑结构组织的信息。为了解决这些问题，我们引入了一类网络约束的线性自回归模型，该模型在预定义的结构连接图的边缘上产生高度动态的功能连接性信号。此外，我们证明添加额外的扩散约束可以提高模型性能。我们成功地验证了所得到的图扩散自回归（GDAR）模型在模拟神经活动以及放置在猕猴感觉运动皮层的硬膜下和皮层内微电极阵列记录上的效果，展示了其描述由光遗传刺激引发的快速通信动态、中风和电刺激后静息态dFC的变化，以及到达任务期间行为的神经关联的能力。

## Abstract
Estimating dynamic functional connectivity (dFC) is attracting increased attention, spurred by rapid advancements in multi-site neural recording technologies and efforts to better understand cognitive processes. Yet, most studies focus on static estimates of functional connectivity that cannot capture highly dynamic neural processes, while also ignoring information about the structural organization of the brain. To address these issues, we introduce a class of network-constrained linear autoregressive models that give rise to a highly dynamic functional connectivity signal on the edges of a predefined structural connectivity graph. Furthermore, we demonstrate that adding an additional diffusion constraint improves the models performance. We successfully validated the resulting graph diffusion autoregressive (GDAR) model on simulated neural activity and recordings from subdural and intracortical micro-electrode arrays placed in macaque sensorimotor cortex demonstrating its ability to describe rapid communication dynamics induced by optogenetic stimulation, changes in resting state dFC following stroke and electrical stimulation, and neural correlates of behavior during a reach task.