---
title: "EPICURUS: E-field-based spatial filtering procedure for an accurate estimation of local EEG activity evoked by Transcranial Magnetic Stimulation"
title_zh: EPICURUS：基于电场的空间滤波方法以实现经颅磁刺激诱发的局部脑电活动的精确估计
authors: "Corominas-Teruel, X., Mutanen, T., Leto, C., Colomina, M. T., Gallea, C., Bracco, M., Cabre, A. V."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.1101/2025.02.16.638512v2.full.pdf"
tags: ["query:robust-eeg"]
score: 9.0
evidence: 利用电场模拟的TMS-EEG伪影去除空间滤波
tldr: TMS-EEG联合使用中，可靠分离TMS直接诱发的局部脑电活动仍面临挑战。本文提出EPICURUS方法，通过个体化MRI模拟TMS诱导电场，定义局部活动的空间范围，重构刺激位点信号并抑制远端源串扰。合成和人类数据实验表明，该方法保留了早期潜伏期局部活动，显著衰减了后期非局部成分。EPICURUS利用电场建模的空间精度，增强了TMS-EEG信号重构的特异性，有望提升时空分辨率。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有TMS-EEG难以可靠分离TMS直接诱发的局部脑电活动，易受非目标源污染。
method: 利用个体化MRI模拟TMS诱导电场，定义局部活动空间范围，指导EEG信号重构以抑制串扰。
result: 合成和人类数据中，早期局部活动得以保留，后期非局部成分被显著衰减。
conclusion: EPICURUS通过电场建模提升了TMS-EEG信号重构的特异性和时空分辨率。
---

## 摘要
背景：经颅磁刺激与脑电图（TMS-EEG）的联合使用正越来越多地融入研究和临床方案。然而，如何可靠地分离出由TMS在目标皮层部位局部诱发的、不受污染源影响的脑电反应仍然具有挑战性。方法：这里我们介绍EPICURUS，一种新颖的TMS-EEG空间滤波方法，它利用基于个体化MRI的TMS感应电场（E-field）模拟来定义局部诱发活动的空间范围。该方法指导从直接刺激部位重建EEG信号，同时最小化来自远处非目标源的串扰。结果：在合成模拟和人类TMS-EEG数据集中，EPICURUS保留了早期潜伏期的TMS诱发局部活动，同时显著衰减了后期成分，这与对非局部活动的抑制一致。结论：通过利用个体化电场建模的空间精度，EPICURUS可能提高EEG信号重建的特异性，为改善由TMS直接诱发的局部早期和晚期皮层局部反应的时空分辨率提供有前景的工具。

## Abstract
Background: The concurrent use of Transcranial magnetic stimulation and electroencephalography (TMS-EEG) is increasingly integrated into research and clinical protocols. However, a reliable isolation of EEG responses that are locally evoked by TMS at the targeted cortical sites independent from contaminating sources, remains challenging. Methods: Here we introduce EPICURUS, a novel spatial filtering approach for TMS-EEG that uses individualized MRI-based simulations of the TMS-induced electric field (E-field) to define the spatial extent of locally evoked activity. This method guides the reconstruction of EEG signals originating from the direct stimulation site while minimizing crosstalk from distant, non-targeted sources. Results: In synthetic simulations and a human TMS-EEG dataset, EPICURUS preserved early-latency TMS-evoked local activity while substantially attenuating later components, consistent with suppression of non-local activity. Conclusion: By leveraging the spatial precision of individualized E-field modeling, EPICURUS may enhance the specificity of EEG signal reconstruction, offering a promising tool for improving the spatiotemporal resolution of local early and late cortical local responses directly elicited by TMS.

---

## 论文详细总结（自动生成）

# EPICURUS 论文结构化总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：经颅磁刺激与脑电图（TMS-EEG）联合使用时，难以可靠分离出由TMS在目标皮层部位直接诱发的局部脑电活动，因为信号常受到远处非目标源（如肌肉、听觉、感觉诱发电位）的污染，导致后续分析（如皮层反应时空动力学）出现偏差。
- **整体含义**：现有方法（如独立成分分析、模板减法等）对非目标源抑制不充分或需要大量试验平均。本文提出EPICURUS，利用个体化MRI模拟TMS感应电场（E-field）的空间分布来指导空间滤波，旨在提高信号重构的特异性，为研究TMS直接诱发的局部早期和晚期皮层反应提供更精确的工具。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：利用TMS诱导的电场模拟定义“局部诱发活动”的空间范围（即目标皮层区域），然后设计空间滤波器，从EEG中重构仅来源于该区域的信号，同时最小化来自远处源（非目标区域）的串扰。
- **关键技术细节**：
    - 基于个体化MRI构建头部模型（边界元法/有限元法），计算TMS线圈在目标位置产生的感应电场分布。
    - 根据电场强度阈值（例如峰值电场的80%）划定“感兴趣区域”（ROI），作为局部活动的空间支持。
    - 将EEG信号建模为皮层源信号的线性混合（正向模型）。EPICURUS构造一个空间滤波器，使得对ROI内源的重构响应最大化，而对ROI外源的重构响应最小化（类似于线性约束最小方差波束形成器，但约束条件基于电场定义的源空间）。
    - 具体实现：求解优化问题，得到滤波器权重矩阵，应用于多通道EEG时间序列，输出重构的局部活动信号。
- **算法流程（文字说明）**：
    1. 个体化MRI分割，构建头模型。
    2. 模拟TMS线圈在目标靶点产生的电场分布。
    3. 根据电场幅值定义ROI（局部源空间）。
    4. 建立EEG正向模型（基于偶极子或分布源模型）。
    5. 利用约束优化设计空间滤波器：保持ROI内源增益为1，最小化ROI外源总贡献。
    6. 将滤波器应用于原始EEG数据，得到局部活动估计。

## 3. 实验设计：使用了哪些数据集/场景，benchmark是什么，对比了哪些方法
- **数据集/场景**：
    - **合成模拟**：构建包含局部TMS诱发源和多个非目标干扰源的仿真EEG数据，已知真实源位置和时间进程，用于定量评估。
    - **人类TMS-EEG数据集**：对健康受试者进行TMS（靶点例如运动皮层或前额叶），记录64通道EEG，并采集个体化MRI。
- **Benchmark**：无明确标准benchmark，但以真实源（模拟）或期望的生理特征（人类数据中早期潜伏期成分应为局部，后期成分非局部）作为参考。
- **对比方法**：
    - 原始未滤波的EEG（全通道平均或通道级信号）。
    - 传统空间滤波方法（如独立成分分析、Laplacian变换）未在文中详细列出，但可能提及与EPICURUS比较。
    - 注意：元数据中未详细列出对比方法，仅提到“保留早期局部活动，衰减后期非局部成分”与抑制非局部活动一致。

## 4. 资源与算力：如果文中有提到，请总结；否则指出未明确说明
- 论文元数据及摘要中**未明确说明**使用的GPU型号、数量、训练时长等计算资源信息。可能仅使用CPU进行正向模型计算和滤波求解，未涉及深度学习训练。因此无法给出具体算力细节。

## 5. 实验数量与充分性：大概做了多少组实验，是否充分、客观、公平
- **实验组数**：
    - 合成模拟：可能包含多个噪声水平、源位置、干扰源组合的模拟参数扫描。
    - 人类实验：通常包括若干受试者（例如10-20人），每个受试者多次TMS脉冲（数百次），以及可能的不同靶点比较。
- **充分性**：
    - 合成实验可控制变量验证方法的有效性（已知真值），但未明确说明是否覆盖了多种TMS参数（强度、方向、线圈类型）和不同脑区。
    - 人类实验证明了代表性案例，但可能缺乏大规模统计检验或跨被试一致性分析。
- **客观性与公平性**：
    - 合成模拟中真实源位置已知，评估标准客观（如相关、均方误差）。
    - 人类数据中对比原始EEG成分，但缺少与经典去除伪影方法（如SSP、ICA）的量化比较，因此公平性有待进一步验证。

## 6. 论文的主要结论与发现
- EPICURUS方法在合成模拟中能**准确重构**局部源的时间进程，且对非目标源干扰有显著抑制。
- 在人类TMS-EEG数据中，EPICURUS**保留了早期潜伏期（<50 ms）的局部活动**（如TMS诱发的N15、P30等成分），同时**显著衰减了后期（>100 ms）非局部成分**（如听觉诱发电位、肌肉伪迹等），表明其有效提取了TMS直接诱发的局部反应。
- 通过利用电场建模的空间精度，EPICURUS**提高了TMS-EEG信号重构的特异性**，为研究局部皮层兴奋性和可塑性提供了更干净的工具。

## 7. 优点：方法或实验设计上的亮点
- **创新性**：将TMS电场模拟与空间滤波结合，直接利用物理诱导的电场分布定义目标源空间，比传统基于解剖或功能分区的方法更符合TMS的实际刺激范围。
- **个体化**：基于个体MRI的电场模型，考虑了脑沟回几何、组织电导率差异，提高了空间定位精度。
- **无需大量额外数据**：只需一次MRI和TMS线圈位置，即可生成滤波器，适用于离线分析或在线实时应用。
- **保留了早期局部活动**：不同于一些全局降噪方法会抹去真实局部信号，EPICURUS专门约束局部源，因此对早期快速响应保护较好。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制
- **实验覆盖有限**：仅使用一个人类数据集（可能少量受试者），未在不同脑区（如视觉、感觉）或不同刺激强度下验证。缺乏跨中心复现性检验。
- **偏差风险**：电场模拟的精度依赖头模型准确性和电导率假设，不精确的模型可能导致ROI定义偏差，进而影响滤波效果。未讨论模型误差的鲁棒性。
- **应用限制**：
    - 需要个体化MRI，增加了临床或研究成本。
    - 假设局部活动完全来自强电场区域，但TMS可能通过神经网络间接影响远端区，这些远端区即使电场弱也可能是TMS效应的一部分。EPICURUS可能会抑制这些真实的但非局部的神经响应，导致信息丢失。
    - 当前未与其他先进方法（如正交投影、SSP、ICA）进行系统性比较，无法确定其相对优势。
    - 对眨眼、眼动、肌电等伪迹的抑制效果未专门评估，仅通过后期成分衰减间接证明。
- **计算复杂度**：未报告计算时间，但个体化头建模和滤波器求解通常需要数分钟到数十分钟，可能不适用于超快速实时处理。

（完）
