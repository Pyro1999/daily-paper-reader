---
title: "NeuroBOLT: Resting-state EEG-to-fMRI Synthesis with Multi-dimensional Feature Mapping"
title_zh: NeuroBOLT：基于多维度特征映射的静息态EEG到fMRI合成
authors: "Yamin Li, Ange Lou, Ziyuan Xu, SHENGCHAO ZHANG, Shiyu Wang, Dario J. Englot, Soheil Kolouri, Daniel Moyer, Roza G Bayrak, Catie Chang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=y6qhVtFG77"
tags: ["query:pbci-load"]
score: 5.0
evidence: 深度神经网络用于EEG到fMRI合成，与EEG基础模型相关
tldr: 本文提出NeuroBOLT，利用深度神经网络从静息态EEG合成高分辨率fMRI，通过多维度特征映射解决EEG空间模糊性。该工作展示了深度网络在EEG信号处理中的强大能力，为构建EEG基础模型提供了跨模态监督训练思路。尽管不直接评估认知负荷，但其方法可迁移至EEG特征提取，对被动BCI中的认知负荷评估有间接帮助。实验表明合成的fMRI在空间精度上具有竞争力。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1435, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1275, \"height\": 779, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1435, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1446, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1426, \"height\": 1705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-y6qhvtfg77/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1446, \"height\": 642, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1447, \"height\": 250, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1432, \"height\": 1450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 914, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-y6qhvtfg77/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1440, \"height\": 433, \"label\": \"Table\"}]"
motivation: fMRI成本高且不便携，希望用便携的EEG推断高分辨率fMRI。
method: 设计多维度特征映射深度网络，将EEG转换为fMRI体素活动。
result: 在静息态数据集上合成的fMRI与真实fMRI空间一致性高。
conclusion: 该方法为EEG到fMRI跨模态合成提供了有效框架。
---

## Abstract
Functional magnetic resonance imaging (fMRI) is an indispensable tool in modern neuroscience, providing a non-invasive window into whole-brain dynamics at millimeter-scale spatial resolution. However, fMRI is constrained by issues such as high operation costs and immobility. With the rapid advancements in cross-modality synthesis and brain decoding, the use of deep neural networks has emerged as a promising solution for inferring whole-brain, high-resolution fMRI features directly from electroencephalography (EEG), a more widely accessible and portable neuroimaging modality. Nonetheless, the complex projection from neural activity to fMRI hemodynamic responses and the spatial ambiguity of EEG pose substantial challenges both in modeling and interpretability. Relatively few studies to date have developed approaches for EEG-fMRI translation, and although they have made significant strides, the inference of fMRI signals in a given study has been limited to a small set of brain areas and to a single condition (i.e., either resting-state or a specific task). The capability to predict fMRI signals in other brain areas, as well as to generalize across conditions, remain critical gaps in the field. To tackle these challenges, we introduce a novel and generalizable framework: NeuroBOLT, i.e., Neuro-to-BOLD Transformer, which leverages multi-dimensional representation learning from temporal, spatial, and spectral domains to translate raw EEG data to the corresponding fMRI activity signals across the brain. Our experiments demonstrate that NeuroBOLT effectively reconstructs unseen resting-state fMRI signals from primary sensory, high-level cognitive areas, and deep subcortical brain regions, achieving state-of-the-art accuracy with the potential to generalize across varying conditions and sites, which significantly advances the integration of these two modalities.

---

## 论文详细总结（自动生成）

# NeuroBOLT：基于多维度特征映射的静息态EEG到fMRI合成

## 1. 论文的核心问题与整体含义

- **研究动机**：fMRI具有毫米级空间分辨率，但成本高、不可移动；EEG便携、时间分辨率高，但空间模糊。现有EEG-to-fMRI翻译方法仅能预测少数脑区，且局限于特定任务（如睁眼闭眼），对静息态（眼睛闭合）条件下的大范围脑区预测尚属空白。
- **整体含义**：本文旨在构建一个通用、可泛化的深度学习框架，直接从原始EEG信号重建全脑高分辨率fMRI BOLD信号，推动两种模态的融合，为低成本、非侵入性脑功能成像提供新途径。

## 2. 论文提出的方法论

- **核心思想**：利用多维度特征映射（时间、空间、频谱）学习EEG到fMRI的复杂映射关系，模型采用“序列到单点”（Sequence-to-One）结构：用EEG窗口（16秒）预测对应时刻的fMRI值，不预设固定的血流动力学延迟。
- **关键技术细节**：
    - **时空表示模块**：借鉴EEG基础模型LaBraM，将多通道EEG分割为1秒长的patches，加上可学习的时间位置编码和空间通道编码，输入Transformer编码器，输出时空嵌入。
    - **多尺度频谱表示模块**：对EEG进行多尺度短时傅里叶变换（STFT），窗口大小分别为0.5s、1s、2s、4s等，得到不同时频分辨率的频谱图；每个尺度经线性投影后相加得到融合频谱嵌入，再通过线性Transformer（降低计算复杂度）编码。
    - **融合与回归**：将时空嵌入与频谱嵌入求和，通过GELU激活和线性层输出fMRI预测值。
- **公式/算法流程**（文字说明）：
    1. 输入：多通道EEG信号 X ∈ R^{C×T}，C为通道数，T=3200（16秒×200Hz）。
    2. 时空路径：分割成C×16个patch（每通道16个1秒patch），加位置和通道编码后经Transformer得到嵌入 r_st。
    3. 频谱路径：对X进行多尺度STFT（L=4个尺度），每个尺度的幅度谱加频率嵌入和窗口嵌入，经线性Transformer得到嵌入 r_sp。
    4. 融合：r = r_st + r_sp，经GELU + Linear输出fMRI预测值 Ŷ_p,t。
    5. 优化目标：最小化预测与真实fMRI之间的均方误差（MSE）。

## 3. 实验设计

- **数据集**：
    - 静息态数据集：22名受试者，29次扫描，每次约20分钟，同时采集32通道EEG（保留26个非伪迹通道，200Hz重采样）和fMRI（TR=2100ms）。
    - 听觉任务数据集：另一个站点采集，16次扫描，10名受试者，包含听觉刺激任务。
- **基准方法**：
    - EEG-to-fMRI翻译基线：BEIRA、Li et al. (2024)。
    - EEG编码模型：BIOT、LaBraM、FFCL、CNN Transformer、STT Transformer。
- **评估指标**：Pearson相关系数（R，主要指标）、均方误差（MSE）。
- **实验场景**：
    - **受试者内预测**：单个扫描内8:1:1划分训练/验证/测试，测试约2分钟数据。
    - **受试者间预测**：按约3:1:1划分扫描（18:5:6），确保同一人多次扫描在同一组。
    - **跨条件泛化**：静息态预训练→任务数据零样本测试；静息态预训练+任务微调；静息态+任务联合训练。
    - **消融实验**：分别评估时空模块、频谱模块的贡献，以及多尺度级别的选择（l0~l4）。

## 4. 资源与算力

- 文中明确说明：实验使用**单张RTX A5000 GPU**，Python 3.9.12，PyTorch 2.0.1，CUDA 11.7。未提及训练时长或总计算量。

## 5. 实验数量与充分性

- **实验数量**：文中呈现了多组系统实验：
    - 受试者内预测（1种设置）。
    - 受试者间预测（1种主要设置）。
    - 跨条件泛化（零样本、微调、联合训练共4种设置）。
    - 消融实验（10种配置对比）。
    - 对不同脑区（7个ROI）分别报告结果。
    - 在附录中补充了MSE结果、最佳/最差重建示例、统计显著性检验（t-test）。
- **充分性与公平性**：
    - 对比方法覆盖了当前主流EEG编码和翻译模型，且文中声称保持超参数一致以实现公平比较。
    - 通过固定随机种子、划分独立验证集等方式控制变量。
    - 但受试者间预测仅使用一组划分，缺乏多折交叉验证或多随机种子重复，结果可能受单次划分影响。
    - 样本量相对较小（29次扫描），部分ROI性能波动较大（如标准差较高），但统计检验显示了部分显著性差异。

## 6. 论文的主要结论与发现

- NeuroBOLT在**静息态fMRI重建**上达到目前最优，受试者内平均R=0.531，受试者间平均R=0.473，均高于所有对比方法（其次为BIOT，R=0.473/0.435）。
- 首次成功从少量电极（26通道）EEG预测出**深部脑区**（如丘脑、壳核）的静息态fMRI信号，且性能与皮层区域相当。
- 模型具备**跨条件泛化能力**：在听觉任务数据上，静息态预训练模型零样本测试R=0.380，微调后提升至0.418，联合训练达到0.420。
- 消融实验证实：**多尺度频谱模块**的加入比纯时空模块提升平均R约0.285；四尺度（l3）配置最佳，平均R=0.473。

## 7. 优点

- **方法创新**：首次将预训练EEG基础模型（LaBraM）与多尺度频谱学习结合，形成统一的多维度特征映射框架，不依赖预设的血流动力学延迟。
- **通用性设计**：支持任意EEG通道数，可适应不同实验设置。
- **实验全面**：覆盖受试者内/间、静息态与任务条件、多脑区评估，并进行了详细的消融分析。
- **结果有说服力**：在深部脑区和跨条件均表现出良好性能，且性能指标（R≈0.4-0.6）在神经影像预测任务中被认为是强相关（低信噪比背景下）。

## 8. 不足与局限

- **效率问题**：当前对每个脑区单独训练模型，不利于全脑高分辨率重建；未来需开发联合训练方法利用脑区间共变关系。
- **样本量限制**：静息态仅22人29次扫描，任务数据10人16次扫描，可能引入过拟合或偏差；文中也承认需要更大、更多样化的数据集。
- **评估稳健性**：未使用多随机种子重复实验，单次划分可能导致结果波动（如部分基线标准差较大）；文中计划未来加入多种子评估。
- **可解释性**：虽然声称“可解释”，但具体哪些EEG特征被用于预测不同脑区未深入分析。
- **应用限制**：需要同时采集EEG-fMRI的数据进行训练，获取成本依然较高；且模型仅适用于相同或相近的采集协议。

（完）
