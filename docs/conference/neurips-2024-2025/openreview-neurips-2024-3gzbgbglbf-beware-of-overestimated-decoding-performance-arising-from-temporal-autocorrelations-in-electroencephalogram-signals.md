---
title: Beware of Overestimated Decoding Performance Arising from Temporal Autocorrelations in Electroencephalogram Signals
title_zh: 警惕脑电图信号时间自相关导致的过高解码性能估计
authors: "Xiran Xu, Bo Wang, Boda Xiao, Yadong Niu, Yiwen Wang, Xihong Wu, Jing Chen"
date: 2024-05-06
pdf: "https://openreview.net/pdf?id=3gZBGBglBf"
tags: ["query:pbci-load"]
score: 4.0
evidence: 对EEG解码高估的批判性分析，与可靠的认知负荷估计相关
tldr: EEG信号时间自相关可能导致解码性能被高估，影响认知负荷评估的可靠性。本文系统分析了这一偏差来源，并提出实验验证方法。对于使用EEG进行认知负荷估计的研究者具有重要警示意义，有助于设计更严谨的实验和评估流程。
source: NeurIPS-2024-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-3gzbgbglbf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 785, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3gzbgbglbf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3gzbgbglbf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3gzbgbglbf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 781, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3gzbgbglbf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1462, \"height\": 366, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 935, \"height\": 170, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1117, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1015, \"height\": 183, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1456, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1456, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1457, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3gzbgbglbf/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1454, \"height\": 359, \"label\": \"Table\"}]"
motivation: EEG解码高准确率可能源于时间自相关伪迹。
method: 通过理论和实验分析自相关对解码性能的影响。
result: 揭示了多个BCI任务中性能高估的存在。
conclusion: EEG解码需谨慎处理时间依赖性。
---

## Abstract
Researchers have reported high decoding accuracy (>95%) using non-invasive Electroencephalogram (EEG) signals for brain-computer interface (BCI) decoding tasks like image decoding, emotion recognition, auditory spatial attention detection, etc. Since these EEG data were usually collected with well-designed paradigms in labs, the reliability and robustness of the corresponding decoding methods were doubted by some researchers, and they argued that such decoding accuracy was overestimated due to the inherent temporal autocorrelation of EEG signals. However, the coupling between the stimulus-driven neural responses and the EEG temporal autocorrelations makes it difficult to confirm whether this overestimation exists in truth. Furthermore, the underlying pitfalls behind overestimated decoding accuracy have not been fully explained due to a lack of appropriate formulation. In this work, we formulate the pitfall in various EEG decoding tasks in a unified framework. EEG data were recorded from watermelons to remove stimulus-driven neural responses. Labels were assigned to continuous EEG according to the experimental design for EEG recording of several typical datasets, and then the decoding methods were conducted. The results showed the label can be successfully decoded as long as continuous EEG data with the same label were split into training and test sets. Further analysis indicated that high accuracy of various BCI decoding tasks could be achieved by associating labels with EEG intrinsic temporal autocorrelation features. These results underscore the importance of choosing the right experimental designs and data splits in BCI decoding tasks to prevent inflated accuracies due to EEG temporal correlations. The watermelon EEG dataset collected in this work can be obtained at Zenodo: https://zenodo.org/records/11238929, and all the codes of this work can be obtained in the supplementary materials.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：近年来，基于脑电图（EEG）的脑机接口（BCI）解码任务（如图像分类、情感识别、听觉空间注意检测）中，研究者报告了极高的解码准确率（>95%）。但部分学者质疑这种高准确率可能源于EEG信号固有的时间自相关性（temporal autocorrelation），而非真正的刺激驱动神经响应。然而，由于刺激驱动的神经响应与时间自相关耦合，难以直接证明高估的存在，且缺乏统一的理论框架来解释这一偏差。
- **整体含义**：本文旨在系统性地揭示和证明EEG时间自相关导致的解码性能高估现象，并构建统一框架阐释其机制。通过使用无神经活动的“水蜜桃EEG”作为对照，作者有力地证明了模型可以仅基于时间自相关（域特征）实现高准确率解码，从而警示研究者在实验设计和数据拆分时必须避免此类数据泄漏，以确保BCI研究的可靠性。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：将EEG时间自相关定义为“域特征”（domain feature）。在一段连续采集、具有相同类别标签的EEG数据中，时间上邻近的样本比时间上远离的样本更相似，这构成了一个独特的“域”。模型可能学习到域特征而非真正的类别相关特征，从而在训练集和测试集共享同一域时获得虚高的性能。
- **关键技术细节**：
  - **数据收集**：从10个西瓜（水蜜桃）上采集EEG，称为“Watermelon EEG”（一种“phantom EEG”方法），完全排除了任何神经活动，仅保留设备噪声和基线漂移等时间自相关。同时使用SparrKULee人类EEG数据集作为对照。
  - **数据重组**：按照三个经典BCI数据集（图像分类CVPR、情感识别DEAP、听觉空间注意力KUL）的实验设计，将西瓜EEG和人类EEG重新组织成对应的块设计（block-design）结构，形成6个数据集：WM-CVPR, WM-DEAP, WM-KUL, SK-CVPR, SK-DEAP, SK-KUL。每个块内连续EEG被赋予相同的类标签和域标签。
  - **模型**：使用简单的CNN（包含LayerNorm、2D卷积、平均池化、全连接层）进行所有分类任务。对于联合训练和图像生成，使用CLIP图像编码器和Stable Diffusion生成器。
  - **关键公式**：假设数据生成过程：\(z \sim p(\cdot)\)（域隐变量），\(x \sim p(\cdot| z, y)\)。解码目标是 \(p(y|x) = \int p(y, z|x) dz = \int p(y|x,z)p(z|x) dz\)。当使用西瓜EEG时，类相关特征不存在，因此 \(p(y|x,z) = p(y|z)\)，模型只需学习 \(p(y|z)\) 和 \(p(z|x)\) 即可解码。
  - **分割策略**：对比“leave-samples-out”（同一域内随机分割训练/测试）与“leave-domains-out”（不同域的数据分别用于训练和测试）。前者会导致域特征泄漏，后者可避免。

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：
  - **水蜜桃EEG数据集**：10个西瓜，每段连续采集超过1小时，64通道，1000Hz采样率。按CVPR、DEAP、KUL实验设计重组。
  - **SparrKULee人类EEG数据集**：选取10名受试者，64通道，自然语音刺激，同类重组。
  - 重组后共6个数据集：WM-CVPR, WM-DEAP, WM-KUL, SK-CVPR, SK-DEAP, SK-KUL。
- **基准（Chance level）**：各类别均匀分布下的随机准确率（如图像分类40类为2.5%）。
- **对比方法**：未与其他SOTA方法对比，而是重点对比不同数据分割策略（leave-samples-out vs. leave-domains-out），以及不同频带（delta, theta, alpha, beta, gamma）的影响。实验包括：
  - 域标签分类（验证 \(p(z|x)\) 可学习）
  - 从域特征解码类标签（验证 \(p(y|z)\) 可学习）
  - 端到端类别分类（leave-samples-out vs. leave-domains-out）
  - 零样本分类（训练时未见类别，观察模型是否将其分到时间上相邻的类）
  - 联合训练（EEG-图像检索任务，使用余弦相似度或InfoNCE损失）
  - 图像生成（使用Stable Diffusion，评估生成图像的语义正确性）
  - 不同频率范围的分析（全频、delta、theta、alpha、beta、low gamma、high gamma）
  - 留受试者分割策略的验证。

### 4. 资源与算力

- **明确说明**：论文提到神经网络使用PyTorch实现，并在单个高性能计算节点上使用8块NVIDIA A800 GPU进行训练。对于不同任务，优化器为AdamW，学习率分别为 \(10^{-3}\)（分类和联合训练）和 \(5 \times 10^{-4}\)（图像生成）。未给出每个实验的具体训练时长或总计算量。

### 5. 实验数量与充分性

- **实验数量**：非常丰富。包括：
  - 6个数据集 × 多种分类任务（表1：域标签、类标签、端到端、留域分割）
  - 零样本分类（表2）
  - 联合训练（表3）
  - 图像生成（表4）
  - 频率带分析（附录表6-9）
  - 留受试者分割分析（附录表5）
  - 时间自相关分析（附录图5）
- **充分性**：实验覆盖了多个BCI任务、多种数据分割方式、不同频率范围，并进行了统计显著性检验（单样本t检验，Bonferroni校正），结果一致支持核心结论。数据集来源多样（西瓜和人），排除了神经活动的影响，对照严谨。总体而言，实验设计客观、公平，充分证明了域特征的作用。

### 6. 论文的主要结论与发现

- **结论1**：EEG信号中固有的时间自相关（域特征）足够强大，即使在没有神经活动的西瓜EEG中，模型也能通过学习域特征实现显著高于随机水平的解码准确率。
- **结论2**：高解码性能的关键在于将同一连续EEG（同一域）分割为训练集和测试集（leave-samples-out）。只要避免这种泄漏（使用leave-domains-out），准确率即降至随机水平。
- **结论3**：该陷阱不仅存在于分类任务，也存在于检索（联合训练）和图像生成任务中。
- **结论4**：低频基线漂移并非唯一来源；长范围时间相关（LRTC）在所有频带均存在，滤波无法消除，因此必须依靠合理的实验范式和数据拆分来防止高估。
- **结论5**：建议未来BCI工作避免将同一类别的连续EEG分割为训练/测试集，应采用留域分割（如留受试者分割）或交叉验证等策略。

### 7. 优点：方法或实验设计上的亮点

- **创新性**：首次使用西瓜作为“phantom”来完全剥离神经响应，直接证明时间自相关的贡献，方法新颖且说服力强。
- **统一框架**：将不同BCI任务（图像、情感、听觉注意）纳入同一问题公式，揭示了共通的陷阱。
- **全面性**：实验涵盖了分类、检索、生成多种任务，分析了不同频带、不同分割策略，并进行了零样本评估，结论普适性强。
- **严谨统计**：所有结果均报告标准误差，并使用单样本t检验和Bonferroni校正确认显著性。
- **开源数据与代码**：提供了西瓜EEG数据集和所有代码，便于复现和后续研究。

### 8. 不足与局限

- **实验覆盖局限**：西瓜EEG虽然能排除神经活动，但其时间自相关特性（如基线漂移、设备噪声）是否完全代表人类EEG的时间自相关仍有待讨论。人类EEG中的LRTC更复杂，可能包含神经振荡成分。
- **样本量有限**：西瓜和人类受试者各仅10个，虽然统计显著，但更广泛的验证（如更多受试者、不同设备）可能增强结论的稳健性。
- **未提出解决方案**：论文指出陷阱存在并呼吁注意，但未给出有效的去偏方法（如域适应或自监督预训练）来减轻对域特征的过度依赖，仅作为未来方向提及。
- **未涉及真实在线BCI场景**：实验均为离线分析，在线应用中时间动态可能更复杂，尚未验证。
- **模型简单**：使用的CNN较为基础，未验证更复杂模型（如Transformer或大规模EEG基础模型）是否同样容易受域特征影响。但简单模型恰好凸显了问题的普遍性。
- **缺少与其他现有方法的对比**：未直接对比已知的防泄漏策略（如交叉验证、相对基线校正）的效果。

（完）
