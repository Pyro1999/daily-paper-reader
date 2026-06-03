---
title: Flow Matching for Few-Trial Neural Adaptation with Stable Latent Dynamics
title_zh: 用于少试次神经适应且具有稳定潜动态的流匹配
authors: "Puli Wang, Yu Qi, Yueming Wang, Gang Pan"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=nKJEAQ6JCY"
tags: ["query:pbci-load"]
score: 6.0
evidence: 用于BCI神经适应的流匹配方法
tldr: 脑机接口（BCI）中神经信号的非平稳性导致跨天性能下降，现有适应方法在少试次下不稳定。本文提出基于流匹配的分布对齐框架（FDA），利用稳定潜动态高效实现少试次神经适应，在真实BCI数据上验证了其稳定性和性能提升，为BCI实际部署提供了新方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 690, \"height\": 645, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1747, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 723, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 731, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1774, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1772, \"height\": 803, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1764, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1762, \"height\": 902, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1072, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1413, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1409, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1781, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1765, \"height\": 722, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1757, \"height\": 613, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 751, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1761, \"height\": 757, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 845, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 841, \"height\": 127, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 851, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 719, \"height\": 134, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 580, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 927, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 928, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1749, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1762, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 991, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1591, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 579, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1753, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1129, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 512, \"height\": 128, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1310, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1747, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1750, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 905, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 905, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 924, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 999, \"height\": 202, \"label\": \"Table\"}]"
motivation: BCI跨天性能退化，现有神经适应方法在少试次下不稳定。
method: 提出FDA框架，利用流匹配进行分布对齐，学习稳定潜动态。
result: 在少试次设置下实现高效稳定的神经适应，改善跨天BCI性能。
conclusion: FDA为BCI的跨天适应问题提供了一种稳定且样本高效的解决方案。
---

## Abstract
The primary goal of brain-computer interfaces (BCIs) is to establish a direct linkage between neural activities and behavioral actions via neural decoders. Due to the nonstationary property of neural signals, BCIs trained on one day usually obtain degraded performance on other days, hindering the user experience. Existing studies attempted to address this problem by aligning neural signals across different days. However, these neural adaptation methods may exhibit  instability and poor performance when only a few trials are available for alignment, limiting their practicality in real-world BCI deployment. To achieve efficient and stable neural adaptation with few trials, we propose Flow-Based Distribution Alignment (FDA), a novel framework that utilizes flow matching to learn flexible neural representations with stable latent dynamics, thereby facilitating source-free domain alignment through likelihood maximization. The latent dynamics of FDA framework is theoretically proven to be stable using Lyapunov exponents, allowing for robust adaptation. Further experiments across multiple motor cortex datasets demonstrate the superior performance of FDA, achieving reliable results with fewer than five trials. Our FDA approach offers a novel and efficient solution for few-trial neural data adaptation, offering significant potential for improving the long-term viability of real-world BCI applications.

---

## 论文详细总结（自动生成）

### 论文总结：Flow Matching for Few-Trial Neural Adaptation with Stable Latent Dynamics

#### 1. 核心问题与整体含义
- **研究动机**：脑机接口（BCI）部署中，神经信号的非平稳性导致解码器跨天性能显著下降。现有神经适应方法（如 NoMAD、Cycle-GAN）依赖大量目标试次进行校准，在仅有少量试次（<5 个）时表现不稳定，且易出现负迁移或训练发散，限制了实际长期应用。
- **整体含义**：本文旨在实现**极少试次下的高效、稳定神经适应**，从而提升 BCI 在慢性植入场景下的实用性和用户长期体验。

#### 2. 方法论
- **核心思想**：提出 **Flow-Based Distribution Alignment (FDA)** 框架，利用**流匹配（Flow Matching）**学习灵活的神经表示，并通过理论保证的**稳定潜动态**实现无源（source-free）域对齐。
- **关键技术细节**：
  - **两阶段框架**：
    - **预训练**：基于源域数据，使用条件流匹配学习从高斯噪声到神经表示（与行为标签线性相关）的连续归一化流。条件特征由 Transformer 从短窗信号中提取，流路径设为线性插值（`z(τ) = (1-τ)z(0) + τz(1)`），优化向量场 `vθ` 匹配预定义场。
    - **微调**：固定流网络 `vθ`，仅微调条件特征提取器 `fα`。提供两种对齐策略：
      - **FDA-MLA**：通过直接最大化目标域在流模型下的对数似然实现无源对齐（使用 Fokker-Planck 方程或 Hutchinson 跟踪估计）。
      - **FDA-MMD**：最小化源/目标域最终潜表示 `z(1)` 之间的最大均值差异（需访问源样本）。
  - **稳定性理论**：证明潜动态在 Lyapunov 意义下稳定——速度场由 Lipschitz 连续的 MLP 构建且缩放系数受约束，使状态误差随步数指数衰减（定理 3.1）。
- **公式与流程**（文字描述）：
  - 预训练损失 `L_cfm` 为预测速度与 `(z(1)-z(0))` 的 ℓ2 误差。
  - 微调时，FDA-MLA 最大化 `-log det(∂vθ/∂z(0))`，FDA-MMD 最小化 RKHS 中的分布距离。

#### 3. 实验设计
- **数据集**：三个非人灵长类运动皮层（M1）数据集——**CO-C**（中心-外伸手任务，猴子 C）、**CO-M**（猴子 M）、**RT-M**（随机目标任务，猴子 M）。源域为某一天完整约 200 试次，目标域为另一天未标注数据，以不同目标比率 r（0.02~0.06，对应 <5 试次）评估。
- **基准方法**：未对齐的 LSTM、CEBRA、ERDiff、NoMAD、Cycle-GAN。评价指标为解码光标速度的 R² 分数。
- **消融与变体实验**：
  - 对齐策略：移除流的 FDA-t、用 Cycle-GAN 对齐潜空间的 FDA-g、对齐条件特征而非潜空间的 FDA-c。
  - 组件：不同流路径（VP、GVP）、不同条件提取器（时域相关注意力的 Transformer、MLP）、添加重构正则化的 FDA-re。
  - 稳定性：移除激活函数（FDA-al）或缩放系数（FDA-sc）。
  - 零样本性能对比、合成数据（Lorenz 系统）恢复实验。

#### 4. 资源与算力
- **硬件**：NVIDIA GeForce RTX 3080 Ti（12GB）用于主要实验；部分推理时间测试在 GTX 1080 Ti（11GB）上。
- **训练时长**：预训练约 98.95 秒（FDA），NoMAD 135.34 秒，ERDiff 2449.68 秒；微调每 epoch 0.14 秒。单个窗口推理约 4 ms。
- **未明确说明**：训练轮数（3500 预训练 epoch，25 微调 epoch），批量大小 256，未提及多卡或特定种子数下的平均计算量细节。

#### 5. 实验数量与充分性
- **充分性**：实验覆盖 3 个数据集、11~12 个跨天会话（每个会话 5 次独立预训练 & 25 次目标选择），多种目标比率（0.02~0.6），与 5 个强基线对比，并进行了 7 项消融研究（对齐策略、组件、稳定性）及合成数据验证。
- **客观性与公平性**：基线使用公开代码或默认超参数；NoMAD、ERDiff 也包含了联合训练解码器；报告了平均 R² 和标准差；对少试次随机性进行了多次重复。
- **潜在不足**：缺少跨主体/跨任务实验，部分会话上 FDA-MLA 的 R² 随目标比例增加而下降（文中归因于异常值影响），但总体趋势仍显示提升。

#### 6. 主要结论与发现
- FDA 在少试次（r=0.02，<5 试次）下显著优于所有基线，平均 R² 提升约 15%，且方差更小。
- 潜动态的 Lyapunov 指数绝大部分非正，证明理论稳定性成立；破坏稳定性的变体（FDA-al、FDA-sc）表现严重下降。
- 无源对齐方法（FDA-MLA）性能略逊于需要源数据的 FDA-MMD，但避免了隐私问题，且收敛平滑（约 20 个微调 epoch）。
- 计算效率优于 ERDiff 和 NoMAD，适合实时应用。

#### 7. 优点
- **方法创新**：首次将流匹配引入 BCI 神经适应，无需对潜变量施加先验分布假设，避免了少试次下先验失效问题。
- **理论保障**：严格证明了潜动态在 Lyapunov 意义下的稳定性，为鲁棒适应提供了数学基础。
- **高效实用**：支持源无关的似然最大化对齐，微调仅需少量试次和很少 epoch，推理速度快。
- **实验充分**：在多个真实运动皮层数据集上验证，消融实验系统，并展示了零样本性能也优于基线。

#### 8. 不足与局限
- **应用限制**：所有数据来自同一主体，神经元群体重叠较大，跨主体或跨任务场景未验证。
- **临床验证缺失**：仅使用非人灵长类数据，人类临床实验中的适用性尚待证实。
- **self-supervised 潜力未深入**：与 NDT-2 的对比显示零样本泛化能力有限，大规模预训练结合 FDA 的潜力值得探索。
- **模态局限**：仅测试了尖峰信号，其他记录模态（如 LFP、Neuropixels）的适用性未评估。
- **异常现象未完全解释**：FDA-MLA 在个别会话随目标比例增加 R² 下降，文中归因于异常值，但缺乏更深入分析。

（完）
