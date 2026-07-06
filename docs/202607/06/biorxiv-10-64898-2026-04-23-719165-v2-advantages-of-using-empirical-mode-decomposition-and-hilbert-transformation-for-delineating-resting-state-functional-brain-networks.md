---
title: Advantages of using Empirical Mode Decomposition and Hilbert Transformation for Delineating Resting State Functional Brain Networks
title_zh: 使用经验模态分解和希尔伯特变换描绘静息态功能脑网络的优势
authors: "Kaur, T., Yadav, S., Jain, N."
date: 2026-07-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.23.719165v2.full.pdf"
tags: ["query:robust-eeg"]
score: 6.0
evidence: 经验模态分解和希尔伯特变换方法可用于脑电去噪，实现鲁棒处理
tldr: 静息态功能连接研究常用fMRI的BOLD信号计算皮尔逊相关系数，但所得功能连接与已知结构连接相关性不佳。本文提出结合经验模态分解（EMD）和希尔伯特变换（HT）的方法，以静息态运动网络为例进行分析。结果表明，该方法显著提高了功能连接与结构连接的一致性，尤其适用于低时间分辨率（低TR）的fMRI数据。该工作为更准确地描绘静息态功能脑网络提供了新途径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基于相关性的静息态功能连接与结构连接匹配不佳，需新方法提升准确性。
method: 对BOLD信号进行经验模态分解，再应用希尔伯特变换计算功能连接。
result: 以运动网络为例，EMD-HT方法相比传统方法提高了功能连接与结构连接的相关性。
conclusion: EMD-HT方法能更可靠地揭示静息态功能脑网络，尤其适合低TR的fMRI数据。
---

## 摘要
静息态功能连接研究的目标是确定身体休息时脑网络的内在动态。当大脑参与各种任务（如处理感觉输入、启动运动活动或各种认知任务）时，这些网络会被差异性地激活。静息态功能连接网络通常通过计算来自不同脑区域的血氧水平依赖（BOLD）信号的皮尔逊相关系数来揭示，这些信号是在受试者未主动执行任何任务时使用功能性磁共振成像（fMRI）收集的。然而，这样确定的功能连接与已知的不同脑区域之间的结构连接相关性不佳。在这里，我们使用经验模态分解（EMD），随后进行希尔伯特变换（HT），来确定人脑的静息态功能连接。我们以运动网络为例展示了使用这种EMD-HT方法的优势。我们表明，与常用方法相比，通过该方法分解的时间序列数据改善了所推导的功能连接与已知结构连接的相关性（特别是对于低TR的fMRI数据）。

## Abstract
The goal of the resting-state functional connectivity studies is to determine the inherent dynamics of the brain networks while the body is at rest. These networks get differentially activated when the brain is involved in various tasks such as processing of sensory inputs, initiating motor activities, or various cognitive tasks. Resting state functional connectivity networks are commonly revealed by determining Pearson Correlation Coefficients of the Blood Oxygenation Level Dependent (BOLD) signals collected from different brain regions using functional Magnetic Resonance Imaging (fMRI) while the subject is not actively performing any task. However, the functional connectivity thus determined does not correlate well with the known structural connectivity between different brain regions. Here, we used Empirical Mode decomposition (EMD), followed by Hilbert Transformation (HT), to determine the resting state functional connectivity in the human brains. We show the advantage of using this EMD-HT method using somatomotor network as an example. We show that the time series data decomposed by this method improves correlation of the derived functional connectivity with the known structural connectivity (especially for low -TR fMRI data) as compared to the methods commonly used.