---
title: Geodesic Optimization for Predictive Shift Adaptation on EEG data
title_zh: EEG数据预测偏移自适应的测地线优化方法
authors: "Apolline Mellot, Antoine Collas, Sylvain Chevallier, Alexandre Gramfort, Denis Alexander Engemann"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=qTypwXvNJa"
tags: ["query:pbci-load"]
score: 7.0
evidence: 适用于认知负荷评估的EEG域自适应方法
tldr: 针对EEG数据中因不同人群和设备导致的输入和标签联合分布偏移问题，本文提出一种基于SPD流形的测地线优化域自适应方法。该方法通过流形上的预测偏移校正，有效提升了跨域EEG分类性能。该技术可直接应用于EEG认知负荷评估中的跨场景泛化。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1366, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1424, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1403, \"height\": 599, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1192, \"height\": 1581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1332, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1384, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1391, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1392, \"height\": 919, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qtypwxvnja/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1385, \"height\": 913, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-qtypwxvnja/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qtypwxvnja/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qtypwxvnja/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 337, \"label\": \"Table\"}]"
motivation: EEG数据常受分布偏移限制监督学习，现有域自适应方法难以处理同时发生的输入和标签偏移。
method: 提出在SPD流形上进行测地线优化的域自适应方法，校正预测偏移。
result: 在多个跨域EEG分类任务上显著优于现有域自适应方法。
conclusion: 该流形域自适应方法为EEG的跨场景应用提供了有效工具。
---

## Abstract
Electroencephalography (EEG) data is often collected from diverse contexts involving different populations and EEG devices. This variability can induce distribution shifts in the data $X$ and in the biomedical variables of interest $y$, thus limiting the application of supervised machine learning (ML) algorithms. While domain adaptation (DA) methods have been developed to mitigate the impact of these shifts, such methods struggle when distribution shifts occur simultaneously in $X$ and $y$. As state-of-the-art ML models for EEG represent the data by spatial covariance matrices, which lie on the Riemannian manifold of Symmetric Positive Definite (SPD) matrices, it is appealing to study DA techniques operating on the SPD manifold. This paper proposes a novel method termed Geodesic Optimization for Predictive Shift Adaptation (GOPSA) to address test-time multi-source DA for situations in which source domains have distinct $y$ distributions. GOPSA exploits the geodesic structure of the Riemannian manifold to jointly learn a domain-specific re-centering operator representing site-specific intercepts and the regression model. We performed empirical benchmarks on the cross-site generalization of age-prediction models with resting-state EEG data from a large multi-national dataset (HarMNqEEG), which included $14$ recording sites and more than $1500$ human participants. Compared to state-of-the-art methods, our results showed that GOPSA achieved significantly higher performance on three regression metrics ($R^2$, MAE, and Spearman's $\rho$) for several source-target site combinations, highlighting its effectiveness in tackling multi-source DA with predictive shifts in EEG data analysis. Our method has the potential to combine the advantages of mixed-effects modeling with machine learning for biomedical applications of EEG, such as multicenter clinical trials.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：脑电图（EEG）数据常因不同人群、设备、记录环境而产生分布偏移，且偏移同时发生在输入特征 $X$（协方差矩阵）和预测目标 $y$（如年龄）上，导致传统监督学习模型泛化能力差。现有的域自适应（DA）方法难以处理这种联合偏移。
- **整体含义**：本文旨在提出一种能在测试阶段处理多源域自适应、同时校正 $X$ 和 $y$ 偏移的方法，以提升跨站点EEG预测模型的鲁棒性，尤其适用于多中心临床试验等生物医学应用。

### 2. 论文提出的方法论
- **核心思想**：利用对称正定（SPD）矩阵构成的黎曼流形，通过测地线优化学习每个域特有的平行传输（re-centering）操作，并与全局回归模型联合优化，从而实现预测偏移的自适应。
- **关键技术细节**：
  - 将EEG协方差矩阵映射到SPD流形，使用仿射不变黎曼度量。
  - 定义带参数 $\alpha \in [0,1]$ 的平行传输操作：$\phi(\Sigma_{k,i}, \Sigma_k, \alpha) = \text{uvec}(\log(\Sigma_k^{-\alpha/2} \Sigma_{k,i} \Sigma_k^{-\alpha/2}))$，其中 $\Sigma_k$ 是域 $k$ 的黎曼均值。
  - 训练阶段：联合优化全局回归系数 $\beta_S$ 和域特定参数 $\gamma_k$（通过sigmoid映射到 $\alpha_k$），损失函数为带Ridge正则化的最小二乘，使用L-BFGS求解。
  - 测试阶段：给定目标域均值 $\bar{y}_T$，优化目标域参数 $\gamma_T$ 使预测均值接近 $\bar{y}_T$，再计算最终预测。
- **算法流程**（文字说明）：
  - **训练**：对每个源域计算黎曼均值 → 初始化 $\gamma_S$ → 循环：计算特征矩阵 $Z_S(\gamma)$ → 计算Ridge系数 $\beta_S^*(\gamma)$ → 计算损失梯度 → 更新 $\gamma_S$ → 输出最优 $\beta_S^*(\gamma_S^*)$。
  - **测试**：计算目标域黎曼均值 → 初始化 $\gamma_T$ → 循环：计算 $Z_T(\gamma)$ → 计算损失导数 → 更新 $\gamma_T$ → 用最优 $\gamma_T^*$ 和已训练 $\beta_S^*$ 预测 $\hat{y}_T$。

### 3. 实验设计
- **数据集**：
  - **模拟数据**：基于log-linear生成模型，可独立控制 $X$ 和 $y$ 的偏移强度 $\xi$。
  - **HarMNqEEG**：包含1564名参与者、14个记录站点的大规模多国EEG数据集，任务为年龄回归。
- **Benchmark**：选取多个源站点组合（如 Barbados, Bern, Colombia 等），剩余站点作为目标域，评估跨站点泛化性能。
- **对比方法**：
  - DO Dummy：预测域均值。
  - No DA：无域自适应，所有数据投影到源黎曼均值。
  - Re-center & Re-scale：每个域独立白化至单位矩阵，并可选地匹配尺度。
  - DO Intercept：每个域拟合单独截距，假设已知目标均值。
  - GREEN：基于SPD网络的深度学习模型。
- **评价指标**：Spearman’s $\rho$、$R^2$ 分数、MAE。

### 4. 资源与算力
- 文中提及：实验在标准Slurm集群上运行，使用250个CPU核心，耗时12小时。未明确说明GPU型号或数量（GREEN模型可能涉及GPU，但未详述）。

### 5. 实验数量与充分性
- **实验数量**：对5种源站点组合进行了3个指标的评估，每组合100次重复（stratified shuffle split），并进行了配对统计检验（Nadeau & Bengio修正t检验）。
- **充分性与公平性**：实验覆盖了多种偏移场景（模拟数据中仅X偏移、仅y偏移、联合偏移；真实数据中14个站点的多种组合）。对比方法包括经典基线（No DA、Re-center）、线性方法（DO Intercept）和深度方法（GREEN），超参数通过嵌套交叉验证选择。实验设计较充分、公平。

### 6. 论文的主要结论与发现
- GOPSA在模拟数据上能有效处理 $X$ 和 $y$ 的联合偏移，优于Re-center等传统方法。
- 在HarMNqEEG真实数据上，GOPSA在多数站点组合中显著优于DO Dummy、No DA、Re-center、GREEN等基线，与DO Intercept相比在多个组合上显著提升（尤其MAE指标）。
- GOPSA的 $\alpha$ 值与站点平均年龄呈近乎线性的关系（$R^2=0.99$），说明其学习到的域特定截距具有生物学解释性。
- 黎曼混合效应框架能结合机器学习与生物统计优势，适用于多中心临床试验。

### 7. 优点
- **方法层面**：在SPD流形上统一处理 $X$ 和 $y$ 偏移，弥合了混合效应模型与深度学习之间的鸿沟。
- **实用性**：测试时无需重新训练模型，仅需目标域均值，适应性强。
- **解释性**：$\alpha$ 参数可解释为域特异性截距，提供模型可解释性。
- **实验设计**：模拟+真实数据双重验证，统计检验严谨。

### 8. 不足与局限
- **要求已知目标均值**：在无法获取 $\bar{y}_T$ 的场景下不适用。
- **实验覆盖范围有限**：仅基于年龄回归任务和一个数据集（HarMNqEEG），未在分类或更多数据集上验证。
- **计算效率**：训练阶段需迭代优化 $\gamma_S$，且涉及矩阵对数和特征分解，在大规模数据上可能成为瓶颈。
- **GREEN对比**：虽包含深度基线，但未进行深度方法下的域自适应微调，可能低估了深度模型的潜力。
- **偏差风险**：假设域间共享相同的回归系数，若域间关系非线性或存在更复杂交互，方法可能失效。

（完）
