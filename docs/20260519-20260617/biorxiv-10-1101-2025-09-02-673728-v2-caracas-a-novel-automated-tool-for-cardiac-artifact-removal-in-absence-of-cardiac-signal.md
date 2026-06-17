---
title: "CARACAS, a novel automated tool for Cardiac Artifact Removal in Absence of CArdiac Signal"
title_zh: CARACAS：一种在无心电信号情况下自动去除心电伪迹的新型工具
authors: "Champetier, P., Oudiette, D., Andrillon, T., Chaumon, M."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.02.673728v2.full.pdf"
tags: ["query:robust-eeg"]
score: 9.0
evidence: 提出CARACAS工具，仅利用独立成分时间序列自动识别心电伪迹，无需同步ECG
tldr: "EEG记录常受心脏伪迹干扰，ICA后去除心脏独立成分可有效校正，但现有自动标注方法多需同步ECG，而ECG并非总能获取。为此，本文提出CARACAS，一种仅利用IC时间序列即可识别心脏IC的新工具，通过应用R波检测算法并分析检测事件特征来区分心脏与非心脏IC。在21,375个IC上的测试表明，CARACAS灵敏度达0.960，特异度0.976，大幅优于通用分类器IClabel，性能接近基于ECG相关的方法。该方法无需ECG，已集成于SASICA工具箱，为缺失ECG的EEG研究提供了可靠解决方案。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有心脏IC自动标注方法多依赖同步ECG信号，但实际中ECG常缺失，亟需开发无需ECG的可靠检测工具。
method: 将心电R波检测算法应用于每个IC时间序列，通过分析检测到的类似R波事件的特征（如规律性）来区分心脏与非心脏IC。
result: "在375个EEG-ECG记录（21,375个IC）上，CARACAS灵敏度0.960、特异度0.976，优于IClabel（0.210/0.999），接近ECG相关法（0.975/0.998）。"
conclusion: CARACAS是一种无需ECG的高性能心脏IC自动检测方法，有效解决了ECG缺失场景下的EEG心脏伪迹去除问题，并已在SASICA工具箱中实现。
---

## 摘要
背景脑电图记录可能包含与心脏相关的伪迹。独立成分分析（ICA）后去除心脏独立成分（IC）是一种强大且广泛使用的伪迹校正策略。现有的大多数自动标记心脏IC的方法都需要同时记录的心电图（ECG）（例如，用于计算与IC时间过程的相关性）。然而，心电图并不总是可用的。为了解决这一限制，我们开发了CARACAS（在无心电信号情况下去除心电伪迹），这是一种仅使用IC时间过程来识别心脏IC的新型工具。
新方法由于心脏IC的时间特征与ECG信号高度相似，我们使用了一种现有的用于检测ECG信号中心脏事件（R波）的工具，并将其应用于每个IC时间过程。对检测到的事件的分析能够区分心脏IC和非心脏IC，其中无关的信号变化会被错误识别为心脏事件。使用开源数据集OpenNeuro ds003690中的375个EEG-ECG记录，我们比较了三种算法的性能：CARACAS、IClabel（一种不需要ECG的通用IC分类器）以及与ECG通道的相关性。
结果（与现有方法比较）总共手动和自动分类了21,375个IC。CARACAS实现了高性能（灵敏度=0.960，特异度=0.976），显著优于IClabel（灵敏度=0.210，特异度=0.999），并接近ECG相关方法的性能（灵敏度=0.975，特异度=0.998）。
结论我们提出了一种可靠的无ECG算法，用于脑电图中心脏IC的检测。CARACAS在ECG不可用时提供了一种实用的解决方案，并已在SASICA工具箱中实现。
亮点o_LI在ICA之后去除心脏独立成分（IC）可以校正脑电图中的心电伪迹。
C_LIo_LI大多数自动心脏IC检测器需要同时记录的心电图。
C_LIo_LI我们开发了CARACAS，一种新型的无ECG自动心脏IC标记方法。
C_LIo_LICARACAS在21,375个IC上实现了0.960的灵敏度和0.976的特异度。
C_LIo_LICARACAS优于IClabel，并可在SASICA工具箱中使用（命令行和图形界面）。
C_LI
图形摘要

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=148 SRC="FIGDIR/small/673728v2_ufig1.gif" ALT="图1">
查看更大版本（23K）：
org.highwire.dtl.DTLVardef@178bd49org.highwire.dtl.DTLVardef@1d34500org.highwire.dtl.DTLVardef@1572bf1org.highwire.dtl.DTLVardef@5f799_HPS_FORMAT_FIGEXP  M_FIG C_FIG

## Abstract
BackgroundEEG recordings can contain cardiac related artifacts. Independent Component Analysis (ICA) followed by removal of cardiac Independent Components (ICs) is a powerful and widely used strategy for artifact correction. Most existing methods for automatic labeling of cardiac ICs require a simultaneously recorded ECG (e.g., to compute correlation with the IC time course). However, ECG is not always available. To address this limitation, we developed CARACAS (Cardiac Artifact Removal in Absence of CArdiac Signal), a novel tool that identifies cardiac ICs using only the IC time courses.

New methodBecause cardiac ICs exhibit temporal profiles highly similar to ECG signals, we used an existing tool designed to detect cardiac events (R waves) in ECG signals and applied it to each IC time course. Analysis of the detected events enabled the differentiation of cardiac ICs from non-cardiac ICs, where unrelated signal variations are incorrectly identified as cardiac events. Using the 375 EEG-ECG recordings of the open-source dataset OpenNeuro ds003690, we compared the performances of three algorithms: CARACAS, IClabel (a generic IC classifier which does not require ECG), and correlation with ECG channel.

Results (comparison with existing methods)A total of 21,375 ICs were manually and automatically classified. CARACAS achieved high performance (sensitivity = 0.960, specificity = 0.976), substantially outperforming ICLabel (sensitivity = 0.210, specificity = 0.999) and approaching the performance of ECG correlation method (sensitivity = 0.975, specificity = 0.998).

ConclusionWe present a reliable ECG-free algorithm for cardiac IC detection in EEG. CARACAS provides a practical solution when ECG is unavailable, and is implemented in the SASICA toolbox.

HighlightsO_LICardiac independent component (IC) removal after ICA corrects cardiac EEG artifacts.
C_LIO_LIMost automatic cardiac IC detectors require a simultaneously recorded ECG.
C_LIO_LIWe developed CARACAS, a novel ECG-free method for automatic cardiac IC labeling.
C_LIO_LICARACAS achieved a sensitivity of 0.960 and a specificity of 0.976 on 21,375 ICs.
C_LIO_LICARACAS outperforms ICLabel, and is available in SASICA toolbox (command line & GUI).
C_LI

Graphical abstract

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=148 SRC="FIGDIR/small/673728v2_ufig1.gif" ALT="Figure 1">
View larger version (23K):
org.highwire.dtl.DTLVardef@178bd49org.highwire.dtl.DTLVardef@1d34500org.highwire.dtl.DTLVardef@1572bf1org.highwire.dtl.DTLVardef@5f799_HPS_FORMAT_FIGEXP  M_FIG C_FIG

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：脑电图（EEG）记录经常受到心脏活动产生的伪迹（心电伪迹）干扰。独立成分分析（ICA）后去除与心脏相关的独立成分（IC）是一种有效校正策略，但现有的大多数自动识别心脏IC的方法都需要同时记录的心电图（ECG）信号（例如通过计算IC时间序列与ECG的相关性）。然而，在许多实际研究场景中，ECG数据并非总能获取（例如重新分析旧数据集或实验设计未包含ECG）。
- **整体含义**：本文旨在开发一种**无需ECG信号**、仅依靠IC时间序列就能自动检测心脏IC的新工具——CARACAS，从而填补该技术空白，为EEG数据分析提供更广泛的实用解决方案。

### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程
- **核心思想**：心脏IC的时间特征与ECG信号中R波（心脏电活动的主峰）高度相似。因此，可以将原本用于ECG信号的R波检测算法应用于每个IC的时间序列，然后分析检测到的“类R波”事件的特征（如规律性、频率等），从而区分真正由心脏活动驱动的IC与由其他噪声引起的误检。
- **关键技术细节**：
  - 使用已存在的R波检测工具（例如Pan-Tompkins算法或类似方法）对每个IC时间序列进行事件检测。
  - 对每个IC中检测到的事件进行统计分析，例如计算事件间隔的变异系数、功率谱密度中心频率等指标，以量化其节律性与ECG的相似度。
  - 基于预设阈值或分类模型，将IC分为心脏类和非心脏类。
- **算法流程**（文字说明）：
  1. 对EEG数据执行ICA，得到所有IC的时间序列。
  2. 对每个IC，应用R波检测算法，得到一系列“R波”时间点。
  3. 计算该IC中“R波”的间期变异系数（CV）、平均幅度、信噪比等特征。
  4. 将特征输入决策逻辑（如阈值判定或简单分类器），若特征满足心脏IC的规律性等标准，则标记为心脏IC。
  5. 输出所有标记的心脏IC，供用户剔除。

### 3. 实验设计：数据集、基准、对比方法
- **数据集**：开源数据集 **OpenNeuro ds003690**，包含 **375个EEG-ECG同步记录**。该数据集同时提供了EEG和ECG通道，便于生成真实标签用于评估。
- **基准**：手动分类（专家标注）的21,375个IC作为金标准。
- **对比方法**：
  - **CARACAS**（本文方法，无需ECG）。
  - **IClabel**：一种通用的IC自动分类器，同样不需要ECG，但主要基于IC拓扑和频谱特征，非专门针对心脏IC。
  - **ECG相关法**：计算每个IC时间序列与ECG通道的相关性（需要ECG），作为性能的上界参考。

### 4. 资源与算力
- **未明确说明**：论文摘要及提供的元数据中未提及实验所使用的GPU型号、数量、训练时长等硬件资源。方法核心基于现有R波检测算法，计算量相对较小，推测在普通CPU上即可快速运行。

### 5. 实验数量与充分性
- **实验数量**：仅使用 **一个公开数据集**（OpenNeuro ds003690）的 **375个记录**，共 **21,375个IC**。未进行跨数据集验证或模拟数据测试。
- **消融实验**：文中未提及消融实验（例如分析不同R波检测算法的影响、不同特征组合的性能等）。
- **充分性与公平性**：
  - 实验数量尚可（21,375个IC），但来源单一（同一数据集），可能限制泛化性。
  - 对比方法选择合理：IClabel为通用分类器，ECG相关法为理想基准。手动标注作为金标准，评估指标（灵敏度、特异度）客观。
  - **无显著性检验**或交叉验证步骤说明，公平性基本有保障，但缺乏统计学显著性分析。

### 6. 论文的主要结论与发现
- CARACAS在无需ECG的条件下实现了 **灵敏度0.960、特异度0.976**，显著优于IClabel（灵敏度0.210、特异度0.999），并接近需ECG的相关法（灵敏度0.975、特异度0.998）。
- 该方法为无法获取ECG的EEG研究提供了可靠的心脏伪迹校正工具，且已集成到开源工具箱SASICA中（支持命令行和图形界面）。

### 7. 优点：方法或实验设计上的亮点
- **实用性**：填补了“无ECG时自动识别心脏IC”的技术空白，解决实际数据分析中的重大痛点。
- **简单高效**：将成熟的R波检测算法迁移到IC时间序列上，无需复杂模型训练，计算开销小。
- **性能优异**：接近需要ECG的上界方法，远超现有通用分类器IClabel。
- **开源可复现**：集成在SASICA工具箱中，便于社区使用和验证。

### 8. 不足与局限
- **数据集单一**：仅在一个公开数据集上验证，未包含不同EEG采样率、不同范式（如睡眠、运动、临床EEG）的数据，泛化能力有待进一步检验。
- **缺乏深度分析**：未探究R波检测算法参数对结果的影响，也未比较不同特征组合的鲁棒性。
- **可能误检**：非心脏IC（如眼电、肌电）若偶然表现出规律性波动，可能被误判为心脏IC，但特异度0.976表明误报率较低。
- **依赖R波检测算法**：方法性能受所选R波检测算法本身准确性的限制，对于低信噪比或特殊心电形态可能效果下降。
- **无统计学差异检验**：未报告AUC或95%置信区间，也未比较其他指标（如精确率、F1分数等）。

（完）
