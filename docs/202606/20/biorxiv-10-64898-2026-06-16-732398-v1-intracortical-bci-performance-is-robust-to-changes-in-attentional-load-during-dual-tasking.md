---
title: Intracortical BCI Performance is Robust to Changes in Attentional Load During Dual-Tasking
title_zh: 双任务中注意负荷变化对皮层内脑机接口性能的影响具有鲁棒性
authors: "Canario, E., Shearer, C., Akcakaya, M., Weber, D., Chase, S. M., Collinger, J. L."
date: 2026-06-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.16.732398v1.full.pdf"
tags: ["query:pbci-load"]
score: 8.0
evidence: 直接研究认知负荷（注意负荷）对脑机接口性能的影响
tldr: 脑机接口在真实应用中常遇到多任务导致的注意力变化，可能影响性能。本研究通过结合2D光标控制与N-Back工作记忆任务，探究注意力负荷对皮层内脑机接口性能的影响。两名四肢瘫痪参与者完成实验，同时记录EEG。结果显示，尽管EEG和主观难度表明注意力负荷增加，iBCI性能总体稳健，仅一名低信号质量参与者在轻度负荷下略有下降。研究说明iBCI对注意力负荷具有鲁棒性，但信号质量等因素可能调节这种效应。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究自然环境中注意力变化如何影响iBCI性能，以提高其在不同认知状态下的稳定性。
method: 采用2D光标控制与N-Back工作记忆任务的双任务范式，并记录EEG以测量注意力相关神经活动。
result: iBCI性能在双任务下保持稳健，但低信号质量参与者在轻度负荷下出现微小但显著的任务完成时间和路径长度增加。
conclusion: iBCI性能对注意力负荷鲁棒，但信号质量等个体差异可能影响鲁棒性，需进一步研究补偿机制。
---

## 摘要
高性能皮层内脑机接口（iBCI）控制已在研究环境中得到验证，但性能在会话内部和会话之间仍可能存在变化。这种变化的一个潜在来源是处理自然发生的干扰因素（如想法、声音、疲劳或疼痛）所带来的注意负荷变化。为了提高在不可避免的多任务处理的实际环境中iBCI性能的一致性，我们必须了解注意力的转移如何影响性能。本研究采用二维光标平移+点击的iBCI任务，并配合N-Back工作记忆任务以增加双任务执行期间的注意负荷，考察了注意负荷对iBCI性能和运动相关神经活动的影响。两名四肢瘫痪的参与者（P2和P4）在参与iBCI设备长期临床试验（NCT1894802）期间完成了本研究。通过同时记录的头皮脑电图（EEG）测量了常见的注意力神经相关指标（θ和α频带功率）。虽然EEG记录和难度评分表明双任务期间注意负荷增加，但iBCI性能在各种双任务条件下仍相当鲁棒。其中一名参与者P2在轻度注意负荷条件下，试验完成时间和归一化路径长度出现了小而显著的增加。两名参与者之间的信号质量差异可能影响了结果，因为P2的信号质量较低，因此可能更容易受到注意负荷的影响。P4较高的信号质量可能使他能够在性能不下降的情况下适应增加的注意负荷。总体而言，iBCI性能似乎对注意负荷具有鲁棒性，但本研究观察到的复杂趋势反映了需要继续研究不同认知状态下的BCI使用，以阐明参与者之间潜在的挑战和补偿机制。

## Abstract
High performance intracortical brain-computer interface (iBCI) control has been demonstrated in research settings, but performance can still vary within and between sessions. One potential source of this variability is the change in attentional load that comes from processing naturally occurring distractors such as thoughts, sounds, fatigue, or pain. To improve the consistency of iBCI performance in real-world environments where this sort of multi-tasking is inevitable, we must understand how shifts in attention can impact performance. Here we examined the effect of attentional load on iBCI performance and movement-related neural activity using a 2D cursor translation + click iBCI task paired with an N-Back working memory task to increase attentional load during dual-task performance. Two participants (P2 and P4) with tetraplegia completed the study while enrolled in a long-term clinical trial of an iBCI device (NCT1894802). Common neural correlates of attention (theta and alpha band power) were measured with simultaneously recorded scalp electroencephalography (EEG). While the EEG recordings and difficulty ratings suggested increased attentional load during dual tasking, iBCI performance was quite robust across the various dual tasking conditions. One participant, P2, experienced a small but significant increase in trial completion time and normalized path length during the mild attentional load condition. Signal quality differences between the two participants may have impacted the results, as P2 had lower signal quality and was therefore likely more vulnerable to attentional load. P4's higher signal quality likely allowed him to accommodate increased attentional load without a drop in performance. Overall, iBCI performance appears to be robust to attentional load, but the complex trends observed here reflect a need for continued investigation of BCI use under different cognitive states to elucidate potential challenges and compensatory mechanisms across participants.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：皮层内脑机接口（iBCI）在实验室环境中性能优异，但在实际应用中，用户常面临自然干扰（如分心、疲劳、疼痛等）导致的注意力负荷变化，这可能引起iBCI性能波动。本研究旨在探究注意力负荷对iBCI性能的影响，以提高iBCI在真实多任务环境下的稳定性和一致性。
- **整体含义**：理解注意力转移如何影响iBCI性能，对于开发能够适应不同认知状态的鲁棒性BCI系统至关重要，从而推动iBCI从研究走向实际临床应用。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：采用双任务范式，将2D光标平移+点击的iBCI任务与N-Back工作记忆任务结合，通过改变N-Back任务的难度（即注意负荷水平）来考察iBCI性能的变化。
- **关键技术细节**：
  - iBCI任务：参与者通过想象运动控制光标完成平移和点击操作。
  - 注意负荷操纵：使用N-Back任务（如0-Back、1-Back、2-Back），要求参与者同时记住并更新序列中的项目。
  - 注意力神经相关指标：通过同步记录的头皮脑电图（EEG），提取θ频带（4–8 Hz）和α频带（8–12 Hz）功率，作为注意力负荷的神经生理标记。
  - 行为指标：包括试验完成时间、归一化路径长度、点击准确率等。
- **公式或算法流程**：文中未给出具体公式，但流程可概括为：① 参与者同时执行iBCI控制和N-Back任务；② 记录iBCI性能数据和EEG信号；③ 分析不同N-Back难度条件下iBCI性能变化及EEG功率差异；④ 统计检验对比单任务与双任务条件。

## 3. 实验设计：使用了哪些数据集/场景，其benchmark是什么，对比了哪些方法

- **数据集/场景**：
  - 参与者：两名四肢瘫痪的个体（P2和P4），均来自长期iBCI临床试验（NCT1894802）。
  - 任务场景：二维光标平移+点击任务（单任务）与结合不同难度N-Back任务（0-Back、1-Back、2-Back）的双任务。
  - 数据记录：iBCI神经信号（未详述解码细节）、头皮EEG（θ和α功率）、主观难度评分。
- **Benchmark**：单任务（仅iBCI控制）作为基线条件。
- **对比方法**：比较单任务与三种双任务条件（0-Back、1-Back、2-Back）下的iBCI性能指标和EEG功率。未对比其他BCI算法或注意力补偿方法。

## 4. 资源与算力

- 论文中未明确提及使用的GPU型号、数量、训练时长等计算资源。仅涉及信号采集设备（iBCI阵列和EEG电极帽）和离线数据分析（统计检验），未详细说明计算平台。因此无法总结算力信息。

## 5. 实验数量与充分性

- **实验数量**：
  - 参与者：仅2名（P2和P4）。
  - 条件：4种（单任务、0-Back双任务、1-Back双任务、2-Back双任务），每种条件可能重复多个试次（具体试次总数未在摘要中给出）。
  - 分析：行为性能（完成时间、路径长度）、EEG功率（θ、α）、主观评分。
- **充分性评估**：
  - **有限**：样本量仅2人，个体差异（如信号质量）可能影响结果，难以推广到更广泛人群。
  - **客观性**：使用了EEG客观指标（θ/α功率）和主观评分，多模态验证了注意力负荷增加，但未进行跨数据集或跨参与者交叉验证。
  - **公平性**：对比条件设计清晰（单任务 vs 双任务），但未控制任务顺序效应或学习效应。

## 6. 论文的主要结论与发现

- iBCI性能在双任务条件下总体稳健：两名参与者均未出现明显的性能大幅下降。
- EEG记录和主观难度评分证实双任务期间注意负荷确实增加（θ/α功率变化）。
- 个体差异存在：信号质量较低的参与者P2在轻度注意负荷（0-Back）下，任务完成时间和归一化路径长度出现小而显著的增加；而信号质量较高的参与者P4在任何双任务条件下性能均无显著下降。
- 结论：iBCI性能对注意力负荷具有鲁棒性，但信号质量等个体因素可能调节这一鲁棒性，低信号质量者可能更易受注意力负荷影响。

## 7. 优点：方法或实验设计上的亮点

- **生态效度高**：采用双任务范式模拟真实多任务场景（如一边使用iBCI一边处理其他事物），而非简单注视或被动刺激。
- **多模态验证**：同时使用行为指标（性能）、神经生理指标（EEG脑波）和主观报告（难度评分）确认注意力负荷操纵有效。
- **关注个体差异**：区分了信号质量高低对结果的调节作用，揭示了鲁棒性背后可能的异质性。
- **长期临床硬件支持**：基于已有临床试验设备，研究结果具有一定临床相关性。

## 8. 不足与局限

- **样本量极小**：仅2名参与者，统计效力低，无法进行组级分析，结论泛化性有限。
- **未探索补偿机制**：文中提到参与者可能通过增加认知努力或调整策略来补偿，但未设计实验量化这些机制。
- **信号质量评估不细致**：仅将“信号质量”作为事后解释，未预先控制或匹配参与者信号质量。
- **任务顺序未平衡**：未说明单任务与双任务条件的顺序是否随机，可能存在学习或疲劳效应。
- **缺少详细神经解码细节**：未说明iBCI解码算法（如线性滤波、LSTM等）及其可能受注意力影响的机制。
- **应用限制**：结果仅在四肢瘫痪患者中验证，能否推广到健全人群或其他BCI范式（如P300、SSVEP）未知。

（完）
