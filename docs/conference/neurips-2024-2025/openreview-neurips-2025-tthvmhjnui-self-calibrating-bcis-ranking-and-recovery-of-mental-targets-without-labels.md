---
title: "Self-Calibrating BCIs: Ranking and Recovery of Mental Targets Without Labels"
title_zh: 自我校准BCI：无标签下的心理目标排序与恢复
authors: "Jonathan Grizou, Carlos De la Torre-Ortiz, Tuukka Ruotsalo"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=TtHvmhjNui"
tags: ["query:pbci-load"]
score: 4.0
evidence: 基于EEG的无标签自我校准BCI，用于心理目标恢复，属于被动脑机接口
tldr: 针对缺乏标签数据时BCI解码困难的问题，本文提出CURSOR框架，利用EEG和图像对数据进行自我校准，无需标签即可恢复心理目标。实验证明其预测的相似度评分与人类感知判断相关，为无监督BCI提供了新途径。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1438, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1168, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 429, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1314, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 681, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 680, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1006, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1001, \"height\": 1030, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 702, \"height\": 713, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 704, \"height\": 696, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1021, \"height\": 2203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1440, \"height\": 949, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 998, \"height\": 817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1014, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tthvmhjnui/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1002, \"height\": 1008, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-tthvmhjnui/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 446, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tthvmhjnui/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 913, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tthvmhjnui/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1663, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tthvmhjnui/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1314, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tthvmhjnui/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1226, \"height\": 174, \"label\": \"Table\"}]"
motivation: 传统BCI需要大量标签数据，限制了实际应用。
method: 提出CURSOR算法，通过自监督学习从无标签EEG-图像对中恢复心理目标。
result: 在自然图像数据集上，CURSOR能预测与人类判断相关的相似度评分。
conclusion: 该工作展示了无监督BCI的潜力，有望减少数据标注成本。
---

## Abstract
We consider the problem of recovering a mental target (e.g., an image of a face) that a participant has in mind from paired EEG (i.e., brain responses) and image (i.e., perceived faces) data collected during interactive sessions without access to labeled information. The problem has been previously explored with labeled data but not via self-calibration, where labeled data is unavailable. Here, we present the first framework and an algorithm, CURSOR, that learns to recover unknown mental targets without access to labeled data or pre-trained decoders. Our experiments on naturalistic images of faces demonstrate that CURSOR can (1) predict image similarity scores that correlate with human perceptual judgments without any label information, (2) use these scores to rank stimuli against an unknown mental target, and (3) generate new stimuli indistinguishable from the unknown mental target (validated via a user study, N=53). We release the brain response data set (N=29), associated face images used as stimuli data, and a codebase to initiate further research on this novel task.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：传统的脑机接口（BCI）需要大量带标签的数据（例如已知的心理目标）来训练解码器，但在实际应用中，标签往往难以获取。论文旨在解决从无标签的EEG-图像对中恢复参与者心中所想的目标（如特定人脸图像）这一挑战。
- **意义**：首次提出并验证了**连续域下的自校准BCI（Self-Calibrating BCI, SC-BCI）框架**，无需预训练解码器、无标签数据或启发式规则，即可从脑电信号中推断并恢复心理目标图像，为BCI在无监督场景中的实用化开辟了新路径。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：利用**一致性检验**：对于一个假设的心理目标 \(h\)，构建它的“预测距离”数据集（将观测图像与\(h\)的欧氏距离作为伪标签），训练一个回归器从EEG预测该距离；然后比较该回归器在原始数据上的误差与其在打乱配对数据（shuffled）上的误差的比值作为评分 \(S(h)\)。该评分在真实目标 \(z^*\) 处应最高，因为EEG在真实目标下最能反映距离关系。
- **关键步骤**（算法CURSOR）：
  1. **假设生成**：在潜在空间 \(Z\) 中采样假设目标 \(h\)。
  2. **构建假设数据集**：\(\Gamma_h^N = \{ (e_i, d_i^h) \}\)，其中 \(d_i^h = \|h - z_i\|_2\)。
  3. **训练回归器**：在 \(\Gamma_h^N\) 上训练模型 \(f_{\theta_h}\) 预测 \(d_i^h\)，计算对齐误差 RMSE_aligned。
  4. **打乱对照**：随机打乱 \(e_i\) 与 \(d_i^h\) 的配对得到 \(\Gamma_{h,\sigma}^N\)，训练打乱模型 \(f_{\theta_{h,\sigma}}\)，计算打乱误差 RMSE_shuffled。
  5. **评分**：\(S(h) = \frac{\text{RMSE\_shuffled}}{\text{RMSE\_aligned}}\)。最大化 \(S(h)\) 得到最佳估计 \(\hat{h}\)。
- **关键细节**：使用**相对增益**（比值而非绝对误差）来消除不同假设下距离分布差异的影响；回归器使用**线性回归**（LR）效果最佳，并采用10折交叉验证；相似度函数采用欧氏距离（假设与EEG反映的感知距离线性相关）。

## 3. 实验设计

- **数据集**：作者收集了**新的EEG数据集**（N=9234个刺激-响应对），来自29名参与者，使用GAN生成的人脸图像在512维潜在空间表示。这是目前唯一适合该任务的公开数据集（连续刺激空间、参与者主动集中注意、有定量距离度量、有用户研究验证）。
- **任务**：
  - **排序（Ranking）**：从60个候选假设中排序，衡量算法评分与真实距离的相关系数、目标排名、top-1距离。
  - **优化（Optimization）**：在降维后的潜在空间（EEG降为20维，图像降为10维）使用CMA-ES进行优化，恢复目标图像。
- **对比方法**：
  - **有效估计器**：线性回归（LR）、支持向量回归（SVR）、多层感知器（MLP）及超参数优化版本（BestMLP、BestSVR）。
  - **控制条件**：打乱线性回归（S-LR，训练前打乱配对）、均值预测器（Dummy，忽略EEG）。两者理论上应表现随机。
  - **随机基线**：随机猜测（预期平均排名30/60）。
- **用户研究**：
  - **H-Rank**：人工评分图像相似度（无限时），与算法评分对比。
  - **H-ID**：短时（0.5s）识别任务，确定人类感知不可辨别的距离阈值（\(d \leq 1.6\) 时误差率≈50%）。
- **消融实验**：不同数据量（N=100~9234）、移除近目标数据（阈值0~40）、两种EEG表示（经典窗口化和EEGNet嵌入）。

## 4. 资源与算力

- 文中未使用GPU，全部实验在**CPU**上运行。
- 计算环境：本地机器（Intel/AMD CPU）及**HPC集群**（AlmaLinux 8.7，SLURM调度，AMD EPYC 7452 CPU）。每个实验使用单核，最大RAM 600MB（SVR），最长运行时间15小时。线性回归仅需4小时。
- 论文明确说明了共执行了**超过8000次实验**（包括消融控制），但未给出总计算时间或总核时。

## 5. 实验数量与充分性

- **实验数量丰富**：覆盖了不同估计器（5种）、数据规模（12个N值）、距离消融（8个阈值）、两种EEG表示、用户研究（N=53）、超参数搜索（GridSearchCV）、降维分析（PCA成分数扫描），以及优化过程的消融。
- **充分性评价**：实验设计系统，对照条件（S-LR、Dummy）有效验证了EEG是信息源；统计检验（Mann-Whitney U、Bonferroni校正）均显著表明LR优于基线。
- **局限性**：优化仅在降维空间进行（10D/20D），且降维参数选择依赖于外部指标（如Pearson相关），在真正无监督场景中不可行。未进行在线闭环实验，所有评估均为**离线**。

## 6. 主要结论与发现

- **算法评分与人类感知高度相关**：LR的排序评分与真实距离的相关系数R=-0.77（p<0.001），且与人类H-Rank评分的R=-0.97，几乎完全匹配。
- **可恢复感知上不可区分的目标**：优化后平均距离0.93（小于人类不可辨别的阈值1.6），远超控制方法（S-LR距离24.09，Dummy距离22.51）。
- **标签恢复能力**：利用恢复的目标\(\hat{h}\)重建距离标签，RMSE仅为0.18（全距离范围约0.4%），与有监督方法性能相当（RMSE=0.17）。
- **无标签自我校准可行**：首次证明在连续感知空间中，无需任何标签即可有效恢复心理目标，打破了对校准数据的依赖。

## 7. 优点

- **创新性**：首次在BCI领域实现连续域的自校准，克服了以往分类域方法的局限。
- **方法论严谨**：使用相对误差比而非绝对误差，有效避免了不同假设下距离分布不同带来的混淆。通过打乱对照验证了信息来自EEG而非伪相关。
- **实验全面**：包含大量消融、多种估计器、用户验证，统计检验充分。代码和数据开源，可复现。
- **实用导向**：可恢复真实标签，为一劳永逸的“零校准”BCI提供基础。

## 8. 不足与局限

- **刺激域单一**：仅使用GAN生成的合成人脸，未验证真实人脸或类间（如物体、场景）的泛化能力。
- **相似度假设**：假设EEG编码的感知距离与潜在空间欧氏距离线性相关，该假设可能不成立于其他域。
- **优化依赖降维**：PCA降维参数需要外部指标确定，实际无监督场景中难以获取。优化过程在10D/20D空间进行，可能有偏差。
- **未闭环验证**：所有实验离线模拟，未进行在线实时迭代。近目标刺激使用对数采样，存在采集偏差。
- **跨被试泛化未知**：当前实验每个被试独立处理，未探索模型是否可跨被试迁移。
- **隐私与伦理风险**：从EEG推断心理内容可能侵犯认知隐私，需要谨慎部署。

（完）
