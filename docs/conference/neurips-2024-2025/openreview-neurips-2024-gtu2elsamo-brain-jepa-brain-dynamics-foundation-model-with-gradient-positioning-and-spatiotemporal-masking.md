---
title: "Brain-JEPA: Brain Dynamics Foundation Model with Gradient Positioning and Spatiotemporal Masking"
title_zh: Brain-JEPA：具有梯度定位和时空掩码的脑动力学基础模型
authors: "Zijian Dong, Li Ruilin, Yilei Wu, Thuan Tinh Nguyen, Joanna Su Xian Chong, Fang Ji, Nathanael Ren Jie Tong, Christopher Li Hsian Chen, Juan Helen Zhou"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=gtU2eLSAmO"
tags: ["query:pbci-load"]
score: 5.0
evidence: 具有潜力的脑动力学基础模型，可用于EEG认知负荷
tldr: 本文提出Brain-JEPA，一种基于联合嵌入预测架构（JEPA）的脑动力学基础模型。通过脑梯度定位和时空掩码技术，该模型在人口统计预测、疾病诊断等任务上达到最先进水平，并在不同人群间展现优异泛化性。虽然主要基于fMRI，但其架构和理念可迁移至EEG认知负荷评估。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 769, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1165, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1170, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 635, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1166, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-gtu2elsamo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1458, \"height\": 393, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1214, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1052, \"height\": 749, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1067, \"height\": 434, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1100, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 861, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 861, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 859, \"height\": 537, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 658, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 863, \"height\": 437, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 861, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-gtu2elsamo/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 863, \"height\": 239, \"label\": \"Table\"}]"
motivation: 现有脑模型泛化性不足，且缺乏对脑功能分区的合理建模。
method: 提出Brain-JEPA，采用联合嵌入预测架构，结合脑梯度定位和时空掩码。
result: 在人口预测、疾病诊断等多个任务上取得最优性能，并展现跨种族泛化能力。
conclusion: Brain-JEPA为脑动力学建模提供了新的基础模型框架，可拓展到EEG领域。
---

## Abstract
We introduce *Brain-JEPA*, a brain dynamics foundation model with the Joint-Embedding Predictive Architecture (JEPA). This pioneering model achieves state-of-the-art performance in demographic prediction, disease diagnosis/prognosis, and trait prediction through fine-tuning. Furthermore, it excels in off-the-shelf evaluations (e.g., linear probing) and demonstrates superior generalizability across different ethnic groups, surpassing the previous large model for brain activity significantly. Brain-JEPA incorporates two innovative techniques: **Brain Gradient Positioning** and **Spatiotemporal Masking**. Brain Gradient Positioning introduces a functional coordinate system for brain functional parcellation, enhancing the positional encoding of different Regions of Interest (ROIs). Spatiotemporal Masking, tailored to the unique characteristics of fMRI data, addresses the challenge of heterogeneous time-series patches. These methodologies enhance model performance and advance our understanding of the neural circuits underlying cognition. Overall, Brain-JEPA is paving the way to address pivotal questions of building brain functional coordinate system and masking brain activity at the AI-neuroscience interface, and setting a potentially new paradigm in brain activity analysis through downstream adaptation.

---

## 论文详细总结（自动生成）

## 论文详细总结

### 1. 核心问题与整体含义（研究动机和背景）

- **问题背景**：功能性磁共振成像（fMRI）是研究脑活动和认知过程的重要工具，但传统任务特定模型泛化性差，无法充分利用大量无标注数据。已有基础模型（如BrainLM）采用掩码自编码器（MAE）直接重建原始fMRI信号，但fMRI信噪比低、信息密度稀疏，直接重建易混淆噪声与信号，且生成式架构在线性探测等即用评估中表现不佳。此外，现有工作缺乏针对脑功能分区的合理位置编码和适配fMRI时空特性的掩码策略。
- **核心动机**：构建一个能够学习高抽象、可泛化脑动态表示的基座模型，同时解决脑功能坐标系构建和时空掩码这两个关键的AI-神经科学交叉问题。
- **整体含义**：提出Brain-JEPA，采用联合嵌入预测架构（JEPA），通过预测目标块在隐空间中的表示而非重建原始信号，提升表示质量与下游适应能力。

### 2. 方法论

- **核心思想**：基于JEPA架构，在预训练阶段不重建掩码输入，而是利用观察块（observation block）的表示预测多个目标块（target blocks）在隐空间中的表示。模型包含观察编码器、目标编码器和预测器，目标编码器参数通过观察编码器的指数移动平均（EMA）更新。
- **关键技术细节**：
  - **Brain Gradient Positioning（脑梯度定位）**：用于空间位置编码。先计算ROI间功能连接的非负亲和矩阵，通过扩散映射（diffusion map）降维得到功能梯度（functional gradients），将每个ROI映射到梯度空间中的坐标。然后将梯度向量通过可训练线性层转换为位置嵌入，与时间位置编码（正弦-余弦函数）拼接，形成完整的位置嵌入。该方法能反映脑功能网络的组织结构（如默认模式网络、视觉网络等）。
  - **Spatiotemporal Masking（时空掩码）**：针对fMRI异质时间序列补丁设计。将输入数据除观察块外分为三个不重叠区域：跨ROI（α）、跨时间（β）和双重交叉（γ），分别采样目标块。迫使模型学会跨ROI泛化、时间预测以及同时对未见过ROI和时间步的预测。采用重叠采样策略（部分观察块与α/β目标块重叠）以灵活调节掩码比例，引入更强的归纳偏置。
- **训练流程**：输入fMRI数据先分块（patchify），随机选取观察块输入观察编码器，得到表示s_x；预测器g_ϕ根据s_x和位置嵌入预测三类目标块的表示ŝ_ry；损失为预测表示与目标编码器输出s_ry的L2距离的平均。

### 3. 实验设计

- **数据集与场景**：
  - **预训练**：UK Biobank (UKB) 约40,162名参与者（44-83岁）的静息态fMRI，80%用于预训练，20%用于内部下游评估（年龄、性别预测）。
  - **外部评估**：HCP-Aging（656名健康老年人，预测年龄、性别、神经质、Flanker分数）；ADNI（189名参与者用于NC vs MCI分类，100名用于淀粉样蛋白阳性/阴性分类）；MACC亚洲人群（539名参与者，NC vs MCI分类）。额外在OASIS-3（MCI向AD转换预测）和CamCAN（抑郁症诊断）上验证。
- **基准方法**：对比BrainNetCNN（CNN）、BrainGNN（GNN）、BNT（Transformer）、BrainLM（MAE基础模型），以及SVM/SVR、BrainMass、CSM、SwiFT等额外基线。
- **评估指标**：回归任务使用均方误差（MSE）和皮尔逊相关系数（ρ）；分类任务使用准确率（ACC）和F1分数。所有结果均为5次独立运行的平均值和标准差。

### 4. 资源与算力

- 文中提到预训练使用了4块A100 GPU，每块40GB显存。ViT-Base（86M参数）模型预训练300个epoch。未明确说明总训练时长（如小时数），但基于4块A100和batch size设置（总batch size = 4 GPU × 8 gradient accumulation steps × 16 per GPU = 512），可推断训练资源中等。

### 5. 实验数量与充分性

- **实验数量**：非常充分。涵盖内部任务（年龄、性别）和多个外部数据集（HCP-Aging、ADNI、MACC、OASIS-3、CamCAN）共8类任务；对比了多种基线方法（包括传统机器学习、CNN、GNN、Transformer、其他自监督方法）；进行了模型规模消融（ViT-S/B/L）、数据规模消融（25%-100%预训练数据）、位置编码消融（正弦余弦 vs 解剖位置 vs 梯度定位）、掩码策略消融（标准多块采样 vs 时空掩码）、框架消融（JEPA vs MAE）、梯度维度消融（3维 vs 30维）等。
- **充分性与公平性**：实验设计较全面，对不同基线采用了相同的微调/线性探测设定，且Brain-JEPA与BrainLM均使用ViT-B骨干以确保公平比较。但在部分任务（如ADNI的NC/MCI分类）上，Brain-JEPA未显著优于BrainLM（准确率略低但F1略高），需注意统计显著性标记。

### 6. 主要结论与发现

- Brain-JEPA在人口统计预测、疾病诊断/预后、特质预测等多项下游任务中达到最优或最先进性能，尤其在跨种族（亚洲人群）泛化上表现突出。
- 线性探测性能显著优于BrainLM，说明学到的表示具有更高级的抽象和鲁棒性。
- 模型规模越大（ViT-L）、预训练数据越多，性能持续提升，显示良好可扩展性。
- 消融实验证实脑梯度定位优于传统位置编码，时空掩码带来更快收敛和更好性能。
- 注意力分析显示模型关注到默认模式网络、控制网络等与认知障碍相关的脑网络，与神经科学文献一致。

### 7. 优点

- **方法创新**：首次将JEPA架构应用于fMRI，为脑动态建模提供了新范式；脑梯度定位巧妙融合了认知神经科学中的功能梯度概念，提供更自然的脑功能坐标系；时空掩码针对fMRI异质性设计，引入强归纳偏置。
- **实验全面**：覆盖多种数据类型（不同TR、多站点、多民族）、多种任务（回归、分类、诊断），且进行了充分的消融和对比，验证了各组件贡献。
- **泛化能力**：在完全未见的亚洲人群数据集上表现优异，证明跨种族泛化能力，具有临床推广潜力。
- **可解释性**：通过注意力权重分析揭示关键脑网络，提供了与已有神经科学知识一致的洞察。

### 8. 不足与局限

- **计算资源限制**：未测试更大模型（如ViT-H），可能限制性能上限。
- **预训练数据单一**：仅使用UK Biobank的白人群体数据，尽管在亚洲人群表现好，但更广泛的种族、扫描协议、任务条件等多样性仍有欠缺，可能影响泛化鲁棒性。
- **解释粒度不够细**：目前仅分析了网络级注意力，未来可进一步识别关键ROI和关键时间点，实现更精细的时空解释。
- **多模态整合缺失**：仅使用fMRI，未考虑MEG、EEG或结构MRI等多模态数据，限制了理解脑结构与功能联系的深度。
- **部分任务表现**：在ADNI的NC/MCI分类准确率上，Brain-JEPA（76.84%）并未显著优于BrainLM（75.79%），且BrainLM的F1更高（85.66% vs 86.32%），表明在某些任务上优势尚不明显，需进一步分析。

（完）
