---
title: "REST: Efficient and Accelerated EEG Seizure Analysis through Residual State Updates"
title_zh: REST：通过残差状态更新实现高效加速的EEG癫痫分析
authors: "Arshia Afzal, Grigorios Chrysos, Volkan Cevher, Mahsa Shoaran"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=9GbAea74O6"
tags: ["query:pbci-load"]
score: 4.0
evidence: 基于EEG的深度学习实时分析，可迁移至认知负荷评估
tldr: 该论文针对EEG实时分析中推理速度和内存效率不足的问题，提出了一种基于图神经网络和循环结构的残差状态更新机制REST。该方法有效捕获EEG数据的非欧几里得空间结构和时间依赖，在癫痫检测任务上实现了9倍推理加速并保持高准确率。尽管直接任务是癫痫检测，但其高效深度学习框架可迁移至被动脑机接口中的认知负荷评估等应用。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1659, \"height\": 814, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 832, \"height\": 1135, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1776, \"height\": 1035, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1783, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 703, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1763, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-9gbaea74o6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1765, \"height\": 478, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 798, \"height\": 685, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1725, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 883, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1712, \"height\": 760, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1661, \"height\": 588, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 862, \"height\": 686, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 994, \"height\": 1137, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 546, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1472, \"height\": 602, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1078, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 533, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 862, \"height\": 558, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1074, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-9gbaea74o6/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 908, \"height\": 159, \"label\": \"Table\"}]"
motivation: 现有EEG模型在临床实时设备中面临推理速度慢和内存效率低的问题。
method: 提出图残差状态更新机制，结合图神经网络与循环结构，同时建模空间拓扑和时间依赖性。
result: 在癫痫检测和分类任务上达到高精度，推理速度相比最先进模型提升9倍。
conclusion: 为实时EEG分析提供了高效框架，其方法可拓展至被动BCI认知负荷评估等场景。
---

## Abstract
EEG-based seizure detection models face challenges in terms of inference speed and memory efficiency, limiting their real-time implementation in clinical devices. This paper introduces a novel graph-based residual state update mechanism (REST) for real-time EEG signal analysis in applications such as epileptic seizure detection. By leveraging a combination of graph neural networks and recurrent structures, REST efficiently captures both non-Euclidean geometry and temporal dependencies within EEG data. Our model demonstrates high accuracy in both seizure detection and classification tasks. Notably, REST achieves a remarkable 9-fold acceleration in inference speed compared to state-of-the-art models, while simultaneously demanding substantially less memory than the smallest model employed for this task. These attributes position REST as a promising candidate for real-time implementation in clinical devices, such as Responsive Neurostimulation or seizure alert systems.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 论文的核心问题与整体含义（研究动机与背景）

- **核心问题**：基于EEG的癫痫检测模型在临床实时设备（如响应性神经刺激RNS、深部脑刺激DBS）中面临两大挑战：**推理速度慢**和**内存效率低**。现有深度模型（如CNN-LSTM、DCRNN、Transformer等）虽然在准确率上表现良好，但往往依赖复杂的门控机制（如LSTM/GRU）或深层卷积，导致延迟高、参数多，难以部署在资源受限的边缘设备上。

- **整体含义**：该研究旨在设计一种**兼具高精度、极低延迟和极小内存占用**的模型，使EEG信号分析能够真正满足闭环神经调控系统的实时性要求。通过将图神经网络与循环结构的残差更新相结合，REST（Residual State Update）模型不仅捕获了EEG的非欧几里得空间拓扑（电极布局），还高效建模了时间依赖，为癫痫检测与分类提供了一种可行的轻量化方案。

## 2. 论文提出的方法论：核心思想与关键技术细节

- **核心思想**：REST以**残差状态更新**替代传统RNN的复杂门控机制，利用**图卷积**对每个时间步的空间信息进行聚合，并通过**随机二值掩码**（Binary Random Mask）实现正则化和加速。

- **关键技术细节**：
  1. **EEG距离图构建**：基于10/20标准系统，根据电极之间物理距离构造邻接矩阵（公式1），图结构固定，减少计算。
  2. **状态初始化**：在时间步\(t\)，先将输入\(X_t\)与前一个状态\(S_{t-1}\)通过线性映射得到\(H_t = W X_t + U S_{t-1}\)。
  3. **残差更新**：通过图卷积（公式4）计算增量\(\delta S_t = G_{\Theta}(H_t)\)，然后更新状态\(S_t = H_t + \delta S_t \odot B\)，其中\(B\)为服从Bernoulli分布的随机二值掩码（概率\(p\)）。
  4. **多次更新机制**（Multi-Update）：在同一时间步内，**复用相同的权重**对状态进行多次迭代更新（每次使用不同的随机掩码），最后的状态作为下一时间步的初始状态。这在不增加参数数量的前提下提升了模型表达能力并增强了稳定性。
  5. **避免梯度消失**：残差连接保证了反向传播时梯度流始终包含一个直接通路（附录B，公式14），有效缓解了梯度消失问题。

- **算法流程**（文字描述）：
  - 预处理原始EEG：重采样、分窗（1秒非重叠）、FFT提取对数幅度谱、Z归一化。
  - 构建固定距离图（节点=电极，边基于距离阈值）。
  - 每个时间步：① 线性映射输入和上一状态；② 通过两层图卷积（激活函数ReLU+线性）计算残差；③ 残差乘以随机掩码后与映射结果相加得到新状态；④ 若采用多次更新，则重复步骤①~③（但仍使用相同输入，状态来自上一轮更新结果）。
  - 最终状态经全连接层输出分类/检测结果。

## 3. 实验设计：数据集、基准方法与对比方法

- **数据集**：
  - **TUSZ**（Temple University Hospital EEG Seizure Corpus）：包含5545份EEG文件，5种癫痫发作类型。使用19个标准10-20通道。训练集/评估集比例见表2。
  - **CHB-MIT**（Children's Hospital Boston）：24名患者，192次癫痫发作，采样率256Hz。随机划分子集（18训练、3验证、3测试），病人不重叠（表3）。

- **任务**：
  - **癫痫检测**（二分类）：在不同窗口长度（4s、6s、8s、10s、12s、14s）下评估AUROC。
  - **癫痫分类**（5类）：仅使用发作数据，窗口10s，评估加权F1分数。

- **基准方法**：
  - LSTM、GRU、ResNet-LSTM（两种变体）、CNN-LSTM、DCRNN（有无自监督）、Transformer。
  - 所有基线均经过压缩调整以进行公平比较（附录I）。

- **评估指标**：检测用AUROC，分类用加权F1，同时报告模型大小（MB）、参数量、推理时间（ms）和训练时间（分钟）。

## 4. 资源与算力

- **算力**：所有模型在**单张NVIDIA A100 GPU**上训练，batch size为128。
- **训练时长**（附录F表9）：
  - REST（单次更新）约45-60分钟（检测任务，取决于窗口长度），多次更新约70-100分钟。
  - 基线模型：LSTM约5-7分钟，DCRNN约20-30分钟，Transformer约12-16分钟。
- **推理时间**：REST（多次更新）仅需**1.29ms**（TUSZ），而DCRNN需9.67ms，Transformer需2.5ms。
- **模型大小**：REST仅**37KB**（约8.4K参数），而最小的基线（DCRNN）约0.884MB（126K参数），大模型达27.6MB。

## 5. 实验数量与充分性

- **实验数量**：
  - 2个数据集（TUSZ和CHB-MIT）。
  - TUSZ检测使用6种窗口长度，CHB-MIT使用5种。
  - 分类任务仅用10s窗口。
  - 每个实验重复5次随机种子，报告均值与方差。
  - 消融实验：三种REST变体（DS: 单次确定性、RS: 单次随机、RM: 多次随机）；有/无推理掩码（附录N）；不同RNN应用REST更新策略（附录K）。
  - 额外分析：ROC曲线、混淆矩阵、混淆矩阵（附录C）、训练时间（附录F）。
  - 实时检测实验（附录M）：4s窗口+3s重叠，评估延迟。

- **充分性与公平性**：
  - **公平性**：基线模型经过压缩（附录I），使其参数规模与REST可比。所有模型使用相同预处理、相同训练策略（ADAM优化器）、相同验证集调参。作者还比较了相同神经元数量（64）下的模型大小（附录L）。
  - **充分性**：对比了多种主流架构（RNN、CNN+RNN、GNN+RNN、Transformer），覆盖了不同精度和速度区间。消融实验验证了掩码和多更新的贡献。在CHB-MIT上表现突出，在TUSZ上接近最先进水平。
  - **客观性**：报告了平均值和方差，讨论了性能波动和稳定性（图2显示REST-RM更稳定）。指出了在不同窗口长度下的性能差异。

## 6. 论文的主要结论与发现

- **REST在保持竞争性精度的同时，实现了极致的轻量化与高速**：
  - 在TUSZ上，REST-RM（多次随机更新）检测AUROC最高达83.6%（10s窗口），接近DCRNN w/SS（85.6%）和Transformer（86.0%），但模型大小仅为这些模型的**1/14~1/200**，推理速度为**9倍快**。
  - 在CHB-MIT上，REST-RM在所有窗口长度下**全面超越**所有基线，AUROC最高达96.7%（4s窗口），展现出更佳适应性和鲁棒性。
  - 分类任务中，REST-RM的F1=0.60，仅次于DCRNN w/SS（0.62），但模型尺寸更小、推理更快。
- **多次随机更新和随机掩码是提升性能与稳定性的关键**，单次确定性更新性能较低，而随机掩码和多更新有助于减少过拟合、增加模型容量而不增加参数。
- **该工作为将深度学习模型部署到资源受限的闭环神经刺激设备中提供了可行方案**。

## 7. 优点：方法或实验设计上的亮点

- **方法创新**：
  - 提出**残差状态更新**替代传统门控机制，大幅减少参数和计算量，同时保持时间建模能力。
  - 引入**二值随机掩码**实现轻量级正则化，且能在推理时通过跳过零掩码部分加速。
  - **多次更新复用权重**，在不增加存储的前提下提升模型深度和表达能力，属于简洁而有效的设计。
- **实验设计亮点**：
  - 系统性地比较了**多个窗口长度**（4~14秒），涵盖了短时和长时检测场景，验证了模型对短窗的适应性（CHB-MIT上4s窗口AUROC达96.7%）。
  - **实时检测评价**（附录M）：采用重叠窗口评估延迟和AUROC，REST拥有最低延迟（0.25s）和最快推理。
  - **公平对比**：对基线进行了合理压缩，并报告了相同神经元数量下的参数对比。
  - **消融充分**：验证了掩码、多更新、不同激活函数、损失函数选择（MSE优于BCE）等。

## 8. 不足与局限

- **实验覆盖方面的局限**：
  - 仅在**两个公开数据集**（TUSZ和CHB-MIT）上评估，且TUSZ的评估集规模较小（43名患者，881份EEG文件）。需要更多不同医院、不同人群的临床数据验证泛化性。
  - **能量效率未测量**：作者在Impact Statement中指出，需要进一步测试模型在边缘设备上的能耗，以确保长期植入的安全性。
  - **未与其他轻量化方法对比**：例如MobileNet、TinyML等专门针对边缘部署的模型未纳入基准，但考虑到EEG领域主流对比为文中的模型类别，尚可接受。
- **方法局限**：
  - **训练时间较长**：REST多次更新需要更多训练时间（>70分钟），而简单LSTM仅需约5分钟，这可能限制了快速迭代。
  - **依赖于固定图结构**：基于电极距离的图假设空间关系固定，未能捕获动态功能性连接（如实时脑网络变化）。虽降低了计算，但可能损失部分空间信息。
  - **随机掩码概率\(p\)为超参数**，不同任务/数据集需要手动调整，未给出自动选择方案。
- **偏差风险**：
  - 数据预处理中**随机下采样非发作片段**以保证类别平衡，可能改变了原始分布，影响背景类的检测鲁棒性。
  - 仅基于**0~14秒窗口**，未测试更长的上下文输入（如30秒或1分钟），而这在临床中亦常见。
- **应用限制**：
  - 论文目标为癫痫检测，但作者在引言中提及可迁移至被动BCI（认知负荷评估），然而**论文中并未给出相关实验证实**，该说法需后续工作支持。
  - 模型设计依赖于EEG电极的固定位置，对于可移动电极或不同数量电极的系统可能需要重新构建图。

（完）
