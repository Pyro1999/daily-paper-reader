---
title: "ComCat: Combating Covariate Effects in Brain Analysis"
title_zh: ComCat：应对脑影像分析中的协变量效应
authors: "Gaser, C., Dahnke, R., Ganjgahi, H., Nichols, T."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733200v1.full.pdf"
tags: ["query:robust-eeg"]
score: 6.0
evidence: ComCat框架消除脑数据中的连续混杂变量
tldr: 多站点脑影像分析中，现有ComBat仅处理分类站点效应，无法消除连续混杂变量（如图像质量、头动）。ComCat扩展ComBat，通过B样条基展开建模连续协变量的平滑非线性效应，同时去除站点和连续混杂。在五个多样化数据集（含旅行幻影、单扫描仪变参数、运动伪影等）上，ComCat相比ComBat-GAM降低脑龄预测平均绝对误差（MAE），且能保留疾病组间差异（如ABIDE中ASD与对照）。ComCat无需站点标签也可工作，适用于体素/表面形态学、规范建模和机器学习预测，提升多站点数据整合的鲁棒性。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有ComBat仅建模分类站点效应，无法消除图像质量等连续混杂变量导致的不必要变异。
method: 在ComBat基础上，利用B样条基展开对连续混杂变量（如CAT12图像质量指标）进行平滑非线性建模，同时去除站点和连续协变量效应。
result: 在五个数据集（含旅行幻影、单扫描仪变参数、运动伪影等）上，ComCat均降低脑龄预测MAE；ABIDE中去除扫描仪效应同时保留ASD组间差异。
conclusion: ComCat可灵活处理分类与连续混杂变量，无需站点标签，适用于多种脑分析任务，提升多站点数据整合质量。
---

## 摘要
随着神经影像分析向大规模、多中心研究转变，管理由合并异质数据集引入的非期望变异性已成为关键挑战。尽管ComBat及其神经影像扩展等工具被广泛用于解决这种变异性，但它们仅允许对分类的站点效应进行建模，无法解释连续的混淆源，如图像质量、头部运动和采集参数。我们引入了ComCat，这是ComBat框架的一个扩展，它保留生物学相关的协变量，同时移除分类站点指标和连续干扰变量的影响。后者通过B样条基展开被建模为平滑非线性函数。ComCat适用于广泛的脑分析任务，包括基于体素和基于表面的形态测量学、规范建模和基于机器学习的预测。为展示其能力，我们在五个数据集上评估了ComCat在脑年龄预测中的表现，这些数据集涵盖了互补的多中心协调场景：ON-Harmony（10名受试者 × 6台扫描仪；n=80）；Buchert旅行模体数据集（1名受试者 × 116台扫描仪；n=531）；东北大学单扫描仪、不同采集参数数据集（n=121）；MR-ART（148名受试者，不同运动水平）；以及ABIDE子集，包含来自14台扫描仪的229名对照受试者和208名自闭症谱系障碍患者。使用从CAT12导出的图像质量测量作为连续干扰变量，ComCat在所有五个数据集中相对于ComBat-GAM降低了脑年龄预测的平均绝对误差（MAE），包括站点信息不可用或无效的两种场景。在ABIDE数据集中，ComCat在保留对照组与ASD组差异的同时改善了协调性，表明可以在不影响生物学意义信号的情况下去除扫描仪相关的方差。ComCat可以在有或没有站点标签的情况下运行，并且对图像质量指标的来源不敏感。

## Abstract
As neuroimaging analysis shifts toward large-scale, multi-site studies, managing the unwanted variability introduced by combining heterogeneous datasets has become a critical challenge. Although tools such as ComBat and its neuroimaging extensions are widely used to address this variability, they only permit the modeling of categorical site effects and cannot account for continuous sources of confounding, such as image quality, head motion, and acquisition parameters. We introduce ComCat, an extension of the ComBat framework that preserves biologically relevant covariates while removing the effects of categorical site indicators and continuous nuisance variables. The latter are modeled as smooth nonlinear functions via B-spline basis expansion. ComCat is applicable to a broad range of brain analysis tasks, including voxel- and surface-based morphometry, normative modeling, and machine learning-based prediction. To demonstrate its capabilities, we evaluated ComCat on brain age prediction across five datasets covering complementary multi-site harmonization scenarios: ON-Harmony (10 subjects x 6 scanners; n = 80); the Buchert traveling-phantom dataset (1 subject x 116 scanners; n = 531); the Tohoku single-scanner, varying-acquisition dataset (n = 121); MR-ART (148 subjects with varying motion levels); and an ABIDE subset comprising 229 control subjects and 208 individuals with autism spectrum disorder across 14 scanners. Using image quality measures derived from CAT12 as continuous nuisance variables, ComCat reduced the mean absolute error (MAE) in brain age prediction relative to ComBat-GAM in all five datasets, including the two scenarios where site information was unavailable or uninformative. In the ABIDE dataset, ComCat improved harmonization while preserving the difference between the control and ASD groups, demonstrating that scanner-related variance can be removed without affecting biologically meaningful signals. ComCat can operate with or without site labels and is agnostic to the source of image quality metrics.