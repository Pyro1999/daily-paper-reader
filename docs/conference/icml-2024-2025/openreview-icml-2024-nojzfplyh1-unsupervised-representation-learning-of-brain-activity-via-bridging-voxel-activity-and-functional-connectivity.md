---
title: Unsupervised Representation Learning of Brain Activity via Bridging Voxel Activity and Functional Connectivity
title_zh: 通过桥接体素活动和功能连接的无监督大脑活动表征学习
authors: "Ali Behrouz, Parsa Delavari, Farnoosh Hashemi"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=nOjZfpLyh1"
tags: ["query:pbci-load"]
score: 4.0
evidence: 大脑表征学习用于认知过程理解
tldr: 该论文提出无监督框架BrainMixer，融合体素活动时间序列与功能连接来学习大脑表征，克服了以往方法忽略时空动态的局限。该方法在脑认知过程理解上取得了有效结果，其表征学习策略可迁移至基于脑电的认知负荷评估任务，为深度学习评估认知负荷提供了新的表示学习思路。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1677, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 946, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 760, \"height\": 429, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1764, \"height\": 872, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1747, \"height\": 1024, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1744, \"height\": 1034, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1748, \"height\": 1047, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1774, \"height\": 934, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1776, \"height\": 933, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1425, \"height\": 554, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1431, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1431, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1253, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-nojzfplyh1/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1242, \"height\": 545, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 869, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1763, \"height\": 1336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1762, \"height\": 489, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1764, \"height\": 872, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1766, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1770, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1592, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1763, \"height\": 1332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1097, \"height\": 572, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1408, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-nojzfplyh1/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1414, \"height\": 276, \"label\": \"Table\"}]"
motivation: 现有大脑表征学习方法要么忽略体素时空动态，要么遗漏体素级活动，无法全面建模。
method: 设计BrainMixer，利用无监督学习同时建模功能连接和体素时间序列，学习体素级表征。
result: 在多个脑认知任务上验证了表征的有效性，优于基线方法。
conclusion: 所提框架为理解脑活动提供了新范式，可支撑认知负荷等动态认知状态的评估。
---

## Abstract
Effective brain representation learning is a key step toward the understanding of cognitive processes and diagnosis of neurological diseases/disorders. Existing studies have focused on either (1) voxel-level activity, where only a single weight relating the voxel activity to the task (i.e., aggregation of voxel activity over a time window) is considered, missing their temporal dynamics, or (2) functional connectivity of the brain in the level of region of interests, missing voxel-level activities. We bridge this gap and design BrainMixer, an unsupervised learning framework that effectively utilizes both functional connectivity and associated time series of voxels to learn voxel-level representation in an unsupervised manner. BrainMixer employs two simple yet effective MLP-based encoders to simultaneously learn the dynamics of voxel-level signals and their functional correlations. To encode voxel activity, BrainMixer fuses information across both time and voxel dimensions via a dynamic attention mechanism. To learn the structure of the functional connectivity, BrainMixer presents a temporal graph patching and encodes each patch by combining its nodes' features via a new adaptive temporal pooling. Our experiments show that BrainMixer attains outstanding performance and outperforms 14 baselines in different downstream tasks and setups.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：现有大脑表征学习方法存在两个主要局限：
  - 一类方法仅关注**体素级活动**，但通常将体素活动在一个时间窗口内聚合为单一权重（beta值），忽略了体素活动的时间动态。
  - 另一类方法仅关注**区域级（ROI）功能连接**，但遗漏了体素级精细活动信息。
  - 两种方法都缺乏对大脑多尺度、多模态信息的联合利用，且多采用有监督学习，依赖大量标注数据。
- **整体含义**：论文提出一个**无监督学习框架——BrainMixer**，旨在同时利用体素活动的时间序列和功能连接图，学习具有丰富时空信息的体素级表征，以支持认知过程理解和神经系统疾病诊断。

### 2. 论文提出的方法论

- **核心思想**：设计两个MLP-based编码器，分别编码体素活动时间序列（VA Encoder）和功能连接图（FC Encoder），并通过最大化两者互信息进行无监督预训练。
- **关键技术细节**：
  - **VA Encoder**（体素活动编码器）：
    - 首先根据大脑功能系统（Schaefer et al., 2018）对体素进行**功能分块**，对大小不一致的块进行线性插值统一尺寸。
    - 使用**动态注意力机制**（Dynamic Self-Attention）在体素维度混合信息；通过**时间混合器**（Time Mixer，两层MLP）在时间维度混合信息。
  - **FC Encoder**（功能连接编码器）：
    - 提出**时间图块提取**方法：通过带时间偏置的随机游走（biased temporal random walk）采样节点的时间邻居构成空间-时间图块。
    - 使用**自适应时间池化**（TPMixer）对每个图块进行编码，该池化操作被证明是置换不变且为多集合的通用近似器。
    - 结合时间编码（非学习性余弦编码）来区分不同时间戳。
  - **无监督预训练**：采用互信息最大化（结合噪声对比估计NCE），将VA Encoder和FC Encoder输出的局部与全局表征作为正样本对，最大化其互信息，并使用数据增强（连接掩码、时间序列替换）生成负样本。
- **公式/算法流程**（文字说明）：
  - VA Encoder：输入体素时间序列矩阵 → 功能分块 → 线性插值 → 动态自注意力（体素维） → 两层MLP（时间维） → 输出体素编码及全局编码。
  - FC Encoder：输入功能连接图（每个时间窗口一个图） → 时间随机游走提取图块 → 自适应池化（先特征维softmax融合，再动态自注意力） → 得到节点/边/图级编码。
  - 预训练损失：两个互信息项的期望（全局编码与局部编码的NCE损失）。

### 3. 实验设计

- **数据集**：共6个真实数据集，涵盖不同模态：
  - **BVFC**（本文新增）：Task-fMRI，3名受试者观看8460张图像，含720类别，提供体素时间序列和功能连接。
  - **BVFC-MEG**（本文新增）：MEG版本，4名受试者，22248张图像。
  - **HCP**：fMRI，7440个样本，含7种心理状态（HCP-Mental）和年龄分组（HCP-Age）。
  - **ADHD**：Rest-fMRI，250名ADHD患者、450名正常对照。
  - **TUH-EEG**：EEG，642名受试者，痫样发作检测。
  - **ASD**：Rest-fMRI，45名ASD患者、45名正常对照。
- **任务场景**：5种下游任务
  - 边缘级异常检测（Edge AD）
  - 体素级异常检测（Voxel AD）
  - 脑级异常检测（Brain AD，二元分类）
  - 脑多类分类（Brain Classification，如9类图像标签、7类心理状态、5类年龄组）
  - 回归（HCP上的ASR分数预测）
- **基线方法**：共14种，包括：
  - 图异常检测方法：GOutlier, NetWalk, HyperSAGCN, GraphMixer等。
  - 脑网络方法：BrainNetCNN, BrainGNN, FBNetGEN, ADMIRE, BNTransformer, PTGB等。
  - 时间序列方法：USAD, TST, MVTS。
- **评估指标**：分类用Accuracy，异常检测用AUC-PR（主），额外报告Accuracy进行验证；回归用MAE。

### 4. 资源与算力

- **原文说明**：附录E.3提到“BRAIN MIXER is implemented by PyTorch in Python and a Linux machine with GPU and 16GB of RAM is used to run evaluations。”
- **分析**：未明确说明GPU型号、数量、训练时长。仅提到使用了一块16GB显存的GPU（型号未知），因此无法准确计算算力消耗。

### 5. 实验数量与充分性

- **实验数量**：
  - 主实验：表1（多类分类，4个数据集）、表2（异常检测，3个级别×6个数据集，多种异常比例）、附录表8（异常检测Accuracy）、表9（Top-1 Accuracy）、表10（回归）。
  - 消融实验：表3（17种变体配置，在4个数据集上测试）。
  - 参数敏感性：图4-8共5组实验（不同walks数量、walk长度、时间衰减θ、ROI数量、时间聚合程度）。
  - 补丁策略比较：表7（6种时间序列补丁、6种图补丁）。
  - 目标函数比较：表11（对比contrastive和DGI）。
  - 案例研究：ADHD（图3）、ASD（附录F.7）、GAN图像检测（图2）。
  - 容量影响：图13。
- **充分性与公平性**：
  - 所有基线采用相同的训练/验证/测试划分和超参数调优（网格搜索）。
  - 统计显著性通过配对t检验（p≤0.05），标记在表和图中。
  - 消融实验系统性地去除了每个关键组件，验证其必要性。
  - 涵盖多种模态（fMRI、MEG、EEG）、多种任务、多种异常注入比例（1%和5%）。
  - 因此，实验设计充分、客观、公平，结论可信。

### 6. 论文的主要结论与发现

- BrainMixer在所有任务和数据集上**显著优于所有基线**：
  - 多类分类：平均提升14.3%，最高20.3%。
  - 边缘/体素/脑级异常检测：分别平均提升6.2%、5.7%、4.81%。
- **每个模块的重要性**：消融实验表明，预训练、VA编码器、FC编码器、功能分块、时间图块、动态注意力、偏置采样等均为关键组件。
- **案例发现**：
  - ADHD异常体素主要集中在额极、左右颞极、舌回，与已知文献一致。
  - ASD异常出现在右小脑皮质、右楔前叶、左舌回等区域。
  - GAN生成图像检测中，高层视觉区（V3）活性显著降低（约57%），符合视觉皮层层次结构。
- **方法有效性**：证明了联合建模体素时间序列和功能连接可以学到更丰富的脑活动表征。

### 7. 优点

- **方法创新性**：
  - 首次在无监督框架中同时利用体素级时间序列和功能连接，弥补了单尺度分析的不足。
  - 提出了功能分块、动态注意力、时间随机游走图块提取、自适应时间池化等新颖组件。
  - 理论上证明了池化操作的置换不变性和通用近似能力。
- **实验全面性**：涵盖多种神经成像模态（fMRI、MEG、EEG）、多种任务（分类、异常检测、回归）、多种异常类型（合成、真实疾病），消融与参数分析详尽。
- **可解释性**：通过案例研究定位异常脑区，与神经科学已知结果一致，增强了模型可信度。
- **公开贡献**：提供了两个新的大规模预处理数据集（BVFC和BVFC-MEG）。

### 8. 不足与局限

- **实验覆盖方面**：
  - 仅在6个数据集上验证，样本量有限（尤其ASD只90例），可能影响泛化性。
  - 未在独立外部临床数据集上进行验证，临床应用潜力尚需更多测试。
- **算力分析缺失**：未报告训练时间、GPU型号、所需显存，不利于复现和资源评估。
- **方法局限**：
  - 当前仅支持单模态输入，无法融合多种神经成像模态（如fMRI+EEG）的互补信息。
  - 未提供预测不确定性估计，在医疗应用中可靠性重要。
  - 对超参数（如θ、walk长度、walks数量）较敏感，需要调参才能达到最优。
- **偏差风险**：合成异常（边缘/体素注入）可能无法完全模拟真实病理异常模式，虽然与真实疾病案例研究互补，但仍存在偏差可能性。

（完）
