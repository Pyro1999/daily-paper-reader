---
title: Efficient Personalized Adaptation for Physiological Signal Foundation Model
title_zh: 生理信号基础模型的高效个性化适应
authors: "Chenrui Wu, Haishuai Wang, Xiang Zhang, Chengqi Zhang, Jiajun Bu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=55ysNwbOTI"
tags: ["query:pbci-load"]
score: 6.0
evidence: 生理信号基础模型与个性化适应
tldr: 针对医疗场景中计算资源和数据隐私受限的问题，本文提出PhysioPFM框架，用于生理信号基础模型的高效个性化适应；通过参数高效微调等方式，在保持隐私的同时提升模型在本地数据上的性能。实验证明了其有效性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 833, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 810, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1685, \"height\": 694, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1584, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 858, \"height\": 536, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1418, \"height\": 601, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1416, \"height\": 597, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 779, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 787, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 774, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1775, \"height\": 979, \"label\": \"Table\"}]"
motivation: 基础模型在医疗应用中面临计算资源有限和数据隐私问题。
method: 提出PhysioPFM框架，利用个性化适应策略对生理信号基础模型进行高效微调。
result: 在多个生理信号数据集上，PhysioPFM优于通用基础模型和任务特定方法。
conclusion: PhysioPFM为生理信号基础模型的部署提供了一种实用方案。
---

## Abstract
Time series analysis is crucial across various fields like energy, environment, transportation, finance and health. Deep learning has significantly advanced this field, particularly, the Time Series Foundation Model (TSFM) excels in multiple domains due to extensive pre-training. In this work, we focus on TSFM's challenges in medical practice: limited computing resources and medical data privacy. TSFM variants include fine-tuned models and those pre-trained for rapid deployment on diverse data. There may not be enough computing resources to train physiological signals locally in hospitals, and generalized TSFM is still inferior to task-specific methods on private, imbalanced local data. To address this, we propose PhysioPFM, a framework for efficiently personalizing TSFM. Our approach involves low-rank pre-training on public datasets, generator training by trained LoRA weights, and efficient weight generation via local data. Experimental results demonstrate that integrating generated models with TSFM enhances performance, and transferability, and reduces the need for additional sensitive data training.

---

## 论文详细总结（自动生成）

# 论文结构化总结：Efficient Personalized Adaptation for Physiological Signal Foundation Model (PhysioPFM)

## 1. 核心问题与整体含义（研究动机和背景）

- **背景**：时间序列基础模型（TSFM）在多个领域表现出色，但在医疗实践中面临两大挑战：一是医院本地计算资源有限，无法对大规模模型进行完整微调；二是患者生理信号数据敏感，受GDPR等隐私法规限制，不能上传至云端进行预训练或微调。
- **问题**：现有的两类TSFM——① 基于通用预训练LLM并在本地微调的模型（如OneFitsAll、Time-LLM），以及② 在大规模多领域时间序列上预训练、零样本部署的通用模型（如MOMENT、Timer），要么需要大量本地计算，要么在私有且类别不均衡的生理信号数据上表现不如任务专用模型。此外，许多任务专用TSFM（如SleepFM、ECG-FM）依赖大量私有数据训练，且难以迁移到未见过的信号类型。
- **目标**：本文提出PhysioPFM框架，旨在**高效、轻量级地个性化适应**生理信号基础模型，在保护隐私的同时，以极低的本地计算开销获得与任务专用模型相当甚至更优的性能。核心理念是“Train-Once-for-All Personalization”：预先在公开生理信号数据集上通过LoRA训练获得适配器参数与数据的映射，训练一个扩散Transformer（DiT）来根据本地数据的判别性子序列（Shapelets）生成定制化LoRA权重，从而无需本地微调即可获得个性化模型。

## 2. 方法论：核心思想、关键技术细节

### 2.1 总体框架
PhysioPFM包含三个阶段：
1. **数据准备阶段**：使用公开生理信号数据集，通过LoRA（Low-Rank Adaptation）对预训练TSFM进行微调，得到每个子任务对应的LoRA权重（∆W = BA），并存储任务数据与LoRA的映射对。
2. **生成器训练阶段**：利用扩散Transformer（DiT）作为生成器，以任务的判别性Shapelets作为条件，学习从数据子序列到LoRA权重的生成。
3. **个性化推理阶段**：给定本地私有数据，提取其Shapelets作为条件输入DiT，生成定制的LoRA权重，与原始TSFM结合后直接用于分类。

### 2.2 关键技术细节
- **低秩适应（LoRA）**：固定预训练模型参数W₀，引入两个低秩矩阵A∈ℝ^{r×k}和B∈ℝ^{d×r}（r≪min(d,k)），更新量ΔW=BA。前向传播为W₀x + BAx。
- **去偏训练损失**：为解决类别不平衡和长度异质性，除交叉熵损失外，还引入**锚定分类器损失（Anchored Classifier Loss, L_ac）**，基于神经坍缩（Neural Collapse）理论，将分类器权重和特征原型拉向一个Simplex Equiangular Tight Frame（ETF）结构，实现最大类间分离。
- **Shapelets提取**：采用离线Shapelet发现（Offline Shapelet Discovery）方法，通过感知重要点（PIPs）提取判别性子序列，每个类选择固定数量的Shapelets作为条件输入。
- **扩散Transformer训练**：DiT的输入为加入噪声的LoRA权重（展平并分块），条件为任务对应的Shapelets编码（经编码器）。训练目标是最小化去噪后的LoRA与真实LoRA之间的均方误差：min_ϕ ∑_k∑_j ||∆W_k - G_ϕ(S(t_k), ∆W_k^j)||²₂。
- **个性化推理**：用户仅需运行DiT生成（轻量）和TSFM推理，无需反向传播微调。

### 2.3 算法流程（文字说明）
1. 收集公开生理信号数据集D_pub，划分为多个子任务t_k；
2. 对每个子任务，使用LoRA微调TSFM，得到∆W_k，并提取每个数据集的Shapelets S(t_k)；
3. 将映射对(∆W_k, t_k)用于训练DiT：对每个训练步，采样一个映射对，对∆W_k添加噪声，以S(t_k)为条件，让DiT预测去噪后的权重，计算MSE损失更新参数；
4. 部署时，用户提供本地私有数据，经Shapelet提取后输入训练好的DiT，生成定制LoRA，与原始TSFM合并得到个性化模型，进行预测。

## 3. 实验设计

### 3.1 数据集与任务
- **睡眠阶段检测**：Sleep-EDF数据集（多通道EEG、EOG、EMG），五分类（Wake, N1, N2, N3, REM）。
- **情绪识别**：DREAMER数据集（EEG和ECG），二分类（效价、唤醒度、支配度）。
- **心律失常诊断**：MIT-BIH心律失常数据集（ECG），二分类（正常/异常）。
- **步态冻结检测（FoG）**：FOG数据集（EEG, EMG, ECG, SC, ACC），二分类（有无冻结）。

### 3.2 基准方法
- **通用深度学习模型**：Informer、FEDformer、SimMTM、TimesNet、PatchTST、iTransformer。
- **时间序列基础模型**：OneFitsAll、Time-LLM、MOMENT。
- **任务专用模型**：SleepFM、SleepDG（睡眠）；LSTM-MLP、OMHGL（情绪）；DeepArr（心律失常）；Extra Tree Classifier（FoG）。

### 3.3 评估指标
- 睡眠：准确率、宏F1、κ系数及每类F1；
- 情绪：准确率、F1、AUC；
- 心律失常与FoG：准确率、精确率、召回率、F1。

### 3.4 实验设置
- 随机采样60%训练、20%验证、20%测试，重复3次取平均。
- 基础模型：6层GPT-2预训练模型（基于UTSD数据集），LoRA秩r=4。
- 生成器：12层GPT-2作为DiT，扩散步数1000，线性噪声调度，学习率4e-4，批次64。
- 训练样本：公开数据集（附录表6，涉及10+种生理信号任务）的子任务分解（包括子类子集）以扩充映射数量。

## 4. 资源与算力

- 论文明确提及：DiT生成器训练需约**20GB GPU显存**（在服务器上可行），本地DiT推理仅需**3GB GPU显存**。
- **未明确说明**：GPU型号、数量、训练总时长。但从显存需求推测，服务器端可能使用单张A100 40GB或V100 32GB，本地推理可在低端GPU或嵌入式设备上运行。训练时间未报告，但根据扩散模型训练（1000步、64批次）和数据集规模，推测在数小时至一天内完成。

## 5. 实验数量与充分性

- **主要实验**：4个不同任务（睡眠、情绪、心律失常、FoG），每个任务对比11~12个基准方法，报告3次平均结果及标准差。实验覆盖了通用模型、基础模型和任务专用模型，具有较强的对比性。
- **消融实验**：对PhysioPFM的各个模块进行消融，包括去除锚定损失（L_ac）、改变温度参数τ、去除本地Shapelets、去除本地LoRA生成（直接用原始TSFM），以及全量本地训练。消融实验在Sleep-EDF、MIT-BIH、FoG三个任务上进行，验证了每个组件的贡献。
- **参数分析**：分析LoRA秩（r=1,4,8,16）的影响、训练样本数（50,100,200,1000）的影响、不同条件类型（Shapelets、完整序列、文本）及数量对性能的影响。均以图表呈现（如图4）。
- **效率比较**：展示了FoG任务上各方法的准确率、适应时间（训练+推理）和内存消耗的三维散点图。
- **充分性评价**：实验设计较全面，覆盖了多任务、多指标、多种对比及参数敏感性，且提供了消融和效率分析，结论可靠。但缺少在更大规模、更多样化的私有数据上的验证，所有实验均基于公开数据集拆分为训练/测试，未在真实医院私有数据上测试。

## 6. 主要结论与发现

- **性能优势**：PhysioPFM在所有四个任务上均超过所有基线方法，显著提升：
  - 睡眠检测准确率86.39%，比最佳基线MOMENT高4.49%；
  - 情绪识别（效价/唤醒度/支配度）准确率73.97%/82.19%/84.45%；
  - 心律失常诊断准确率89.94%，F1达89.55%；
  - FoG检测准确率81.32%，F1达79.48%。
- **效率与隐私**：通过生成LoRA而非本地微调，实现了低计算开销（3GB GPU推理）和隐私保护（数据不出本地）。
- **消融验证**：每个组件（锚定损失、Shapelets条件、LoRA生成）均对性能有正贡献；LoRA秩取4即可；训练样本越多生成效果越好；Shapelets作为条件优于完整序列或文本。
- **与全量微调对比**：PhysioPFM（86.39%）接近全量本地训练（87.15%），但无需大量计算资源，且保护隐私。

## 7. 优点

- **创新性**：将“Train-Once-for-All”个性化思想引入时间序列基础模型，结合LoRA和扩散生成，首次利用Shapelets桥接生理信号和模型参数。
- **实用性强**：针对医疗场景的轻量化和隐私保护需求设计，本地仅需生成器推理（3GB显存），可部署于边缘设备。
- **理论扎实**：引入神经坍缩理论设计去偏分类损失（锚定分类器损失），有效处理医学数据中的类别不均衡。
- **实验充分**：多任务、多指标、多基线对比，消融和参数分析到位，且提供效率对比。
- **可复现性**：公开数据集、预训练模型选择（GPT-2、UTSD）、开源细节（附录详列数据集）较好。

## 8. 不足与局限

- **实验覆盖有限**：仅在4个公开数据库上评估，未涉及真实医院私有数据或更复杂的多信号融合任务（如多模态联合分类）。部分数据集（如DREAMER）样本量较小，泛化性需进一步验证。
- **假设限制**：默认用户可以提供足够数量的本地数据（用于Shapelet提取），但对于极端小样本（如每位患者仅10条记录），Shapelets可靠性可能不足，论文未探讨。
- **生成器训练数据依赖**：DiT训练依赖大量公开生理信号任务映射对，需收集并加工多个数据集，工作量较大；且形状特征不同的信号（如EEG与ECG的形态差异）可能影响生成质量，论文未深入分析跨域泛化。
- **未见报告训练时长**：缺乏生成器训练的具体时间、所需GPU数量等信息，难以评估全流程的实际时间成本。
- **基准选择偏重**：对比的“专用方法”仅各选一个（如DeepArr、SleepFM），且这些方法本身也是近年工作，可能存在未包含最强基线（如2024年之后模型）的情况。
- **伦理与公平性**：论文未讨论模型在不同人口学群体上的公平性，医疗AI可能存在偏差风险（如年龄、性别、疾病亚型）。
- **代码与数据未公开**：论文未提供开源代码链接（仅说明数据集来源），可复现性受限。

（完）
