---
title: EEG-Language Pretraining for Highly Label-Efficient Clinical Phenotyping
title_zh: 用于高标签效率临床表型分析的EEG-语言预训练
authors: "Sam Gijsen, Kerstin Ritter"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=yaI2ZYFmeD"
tags: ["query:pbci-load"]
score: 8.0
evidence: EEG语言基础模型
tldr: 针对临床试验中EEG数据标签稀缺的问题，本文提出首个EEG语言预训练模型（ELM），通过多实例学习对齐EEG片段与临床报告，在四个临床评估任务上显著优于仅用EEG的模型，并首次实现了零样本分类与检索，展示了多模态脑电语言模型的潜力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1734, \"height\": 546, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1412, \"height\": 818, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 834, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1570, \"height\": 747, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1394, \"height\": 668, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1765, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 886, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1320, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 867, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 871, \"height\": 1057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1321, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1572, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1043, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1227, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1225, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1227, \"height\": 616, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1228, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1418, \"height\": 723, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1504, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 725, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 874, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 400, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 466, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 836, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 388, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1185, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1500, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 567, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 825, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1110, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1106, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 772, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1313, \"height\": 877, \"label\": \"Table\"}]"
motivation: 临床表型分析中EEG数据标签稀缺，亟需高效预训练方法。
method: 提出EEG语言模型（ELM），结合时间序列裁剪与文本分割，利用多实例学习对齐EEG和临床报告。
result: 在四项临床评估中显著优于EEG仅模型，并实现零样本分类与检索。
conclusion: 本文证明了EEG语言模型在临床表型分析中的有效性，为多模态脑电研究开辟新方向。
---

## Abstract
Multimodal language modeling has enabled breakthroughs for representation learning, yet remains unexplored in the realm of functional brain data for clinical phenotyping. This paper pioneers EEG-language models (ELMs) trained on clinical reports and 15000 EEGs. We propose to combine multimodal alignment in this novel domain with timeseries cropping and text segmentation, enabling an extension based on multiple instance learning to alleviate misalignment between irrelevant EEG or text segments. Our multimodal models significantly improve over EEG-only models across four clinical evaluations and for the first time enable zero-shot classification as well as retrieval of both neural signals and reports. In sum, these results highlight the potential of ELMs, representing significant progress for clinical applications.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **问题**：临床脑电图（EEG）数据在病理检测（如癫痫、睡眠障碍）中广泛使用，但标注数据极其稀缺，限制了深度学习方法的性能。
- **背景**：自监督学习（SSL）在EEG上已有探索，但受限于数据增强困难、信噪比低。而多模态语言模型（如CLIP）在计算机视觉和医学影像中展现了强大的表示学习能力，通过自然语言监督实现零样本泛化。
- **动机**：首次将**功能脑电图（EEG）与临床文本报告**进行多模态对齐预训练，以解决EEG临床表型分析中标签不足的瓶颈。利用医院中伴随EEG记录的临床报告（包含病史、观察、解释等）作为语言信号，引导EEG表示学习。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：训练**EEG-语言模型（ELM）**，通过对比学习对齐EEG时间片段与临床报告段落。针对EEG长时序列和报告多段落带来的不对齐问题，提出**子单元对齐（sub-unit alignment）** 和**多实例学习扩展（MIL-InfoNCE）**。
- **关键技术细节**：
  - **EEG与文本预处理**：将EEG裁剪为非重叠的片段（如60秒或20秒）；将临床报告按标题分段落（如临床历史、记录描述、药物、解释），可筛选或使用LLM（Llama-3 8B）生成单句摘要。
  - **编码器**：
    - EEG编码器（fe）：随机初始化的残差CNN，约0.93M参数。
    - 文本编码器（fl）：冻结的预训练**MedCPT**（基于PubMed搜索日志的对比学习模型）。
  - **对齐策略**：
    - **ELM_e,l**：双投影头（ge, gl），将EEG和文本分别投影到共享潜在空间，使用InfoNCE损失。
    - **ELM_l**：仅EEG有投影头，文本不投影，使用M-FLAG风格的对齐+正交损失。
    - **ELM-MIL**：基于**多实例学习**的扩展，对每个EEG片段采样多个正文本（P(l|e)），对每个文本段落采样多个正EEG片段（P(e|l)），然后计算**MIL-InfoNCE损失**，允许灵活的多对多对齐，缓解了无关片段/句子的错误对齐。
  - **损失函数**：
    - InfoNCE：标准对比损失，温度参数τ。
    - MIL-InfoNCE：对每个锚点，正样本集内平均相似度，负样本集外相似度。
- **训练**：LARS优化器，余弦退火学习率，50 epoch，batch size根据输入长度调整。

## 3. 实验设计：数据集、场景、benchmark与对比方法

- **数据集**：
  - **TUEG**（Temple University Hospital EEG Corpus）：最大公开医院EEG数据集，~15000条记录带临床报告。用于预训练。
  - **TUAB**（TUH Abnormal EEG）：异常/正常二分类，评估记录级病理检测。
  - **NMT**（NMT Scalp EEG Dataset）：不同源（巴基斯坦人群）的异常分类，测试跨域泛化。
  - **TUSZ**（TUH Seizure Detection）：癫痫发作检测，分段级（5秒）二分类。
  - **TUEV**（Events Corpus）：六类事件（三种临床事件、眼动、伪迹、背景），分段级分类。
- **评价场景**：
  - **零样本分类**：通过文本模板（21种变体）计算EEG与“正常/异常”文本的相似度。
  - **线性探测（Linear Probe）**：在冻结的EEG表示上训练逻辑回归，标签比例1%、10%、100%。
  - **检索（Retrieval）**：互相检索EEG和报告，计算Top-K准确率。
- **基准方法**：
  - **EEG-only自监督方法**：BYOL、VICReg、ContraWR、Relative Positioning (RP)、Temporal Shuffling (TS)、Contrastive Predictive Coding (CPC)。
  - **全监督基线**：使用相同EEG编码器端到端训练。
  - **大型预训练模型**：LaBraM (Base/Large/Huge)、CEReBrO等。
- **对比公平性**：所有方法使用相同的EEG编码器架构，预训练数据相同（除LaBraM使用额外数据）。线性探测超参数通过验证集选择。

## 4. 资源与算力

- 文中明确说明：单卡训练，使用**Nvidia Geforce GTX 3090或Tesla V100**，显存小于24GB。训练时间：EEG-language模型约**9小时**，EEG-only模型约**18小时**（因数据增强更耗时）。训练**50个epoch**。
- 未说明使用的GPU数量（推测为单卡），也未提及总计算量（如FLOPs）。模型参数量很小（0.93M），训练开销远小于LaBraM-Huge（369M参数需调优）。

## 5. 实验数量与充分性

- **实验数量**：论文报告了多个方面的实验：
  - **主实验**：TUAB（1%、10%、100%标签）、NMT（1%、10%、100%）、TUSZ（1%、10%、100%）、TUEV（100%）。
  - **消融实验**：温度参数τ、正样本数量（N, M）、聚合方式（Max/Attn/Sum vs MIL-InfoNCE）、文本聚类选择、LLM摘要、语言模型选择、输入长度、数据泄露检测。
  - **检索实验**：EEG→报告、报告→EEG的Top-K准确率。
  - **可视化**：t-SNE、对齐时间序列可视化。
  - **与大型模型比较**：与LaBraM-Base的线性探测对比（使用相同线性探测pipeline）。
- **充分性与客观性**：
  - 实验设计较为全面，覆盖了多个数据集（包括域外验证），标签比例从1%到100%，对比了多种EEG-only方法。消融实验充分，说明了MIL-InfoNCE的优势。使用5次随机初始化报告标准差，统计可靠。
  - 但存在一定局限性：TUAB训练集被包含在预训练数据中（有数据泄露风险），作者通过额外实验证明影响很小。此外，与LaBraM的比较并非完全公平（LaBraM使用更多数据和更大模型，且需要微调），但作者仍进行了线性探测对比以展示ELM表示的质量。

## 6. 论文的主要结论与发现

- **ELM显著优于EEG-only方法**：在TUAB上1%标签时，平衡准确率提升最高达8.7%，AUROC提升9.7%；在NMT上跨域泛化也优于基线。
- **首次实现EEG零样本病理分类**：通过文本提示达到84.31%平衡准确率（双向对齐ELM-MIL e,l），且对温度参数不敏感。
- **多模态检索成功**：可从EEG中检索到对应报告，反之亦然，且病理相关文本（如解释）检索效果最好。
- **MIL-InfoNCE有效**：比标准InfoNCE、Max、Attn、Sum等聚合方式更好，且对正样本数量敏感。
- **子单元对齐本身提供有益归纳偏置**：随机打乱报告仍能提升分类（促进组内不变性），但语义对齐带来更大增益。
- **小模型可媲美大模型**：0.93M参数的ELM在TUAB上线性探测甚至超过369M的LaBraM-Huge（需微调），表明临床语义对齐的高效性。

## 7. 优点

- **方法创新**：首次将EEG与自然语言进行多模态对齐预训练，并针对性提出子单元对齐+多实例学习，解决了长序列与长文本的不对齐问题。
- **标签效率极高**：在极低标签比例（1%）下取得大幅提升，极具临床实用价值。
- **零样本能力**：无需下游标注即可进行病理检测，打破了脑电图领域缺乏零样本研究的局面。
- **可解释性**：通过文本-EEG对齐可视化，可以定位具有临床意义的时段，且语义对齐具有一致性。
- **计算效率高**：模型参数量小，训练显存需求低，训练时间短，便于复现和部署。
- **实验严谨**：进行了数据泄露分析、温度灵敏度、多源数据验证、与大型模型对比等，结论可靠。

## 8. 不足与局限

- **数据局限性**：目前公开的EEG-报告配对数据有限，预训练数据仅来自TUH，域外验证仅一个数据集（NMT）。未来需要更大规模和多样性的数据集。
- **模型规模未探索**：论文未进行模型缩放实验（如增大EEG编码器），无法确定性能是否随参数增长而提升。
- **文本处理局限性**：报告中的伪迹、技术问题等被过滤，可能损失信息（如TUEV上伪迹类检测较弱）；LLM摘要可能丢失细节。
- **零样本分类依赖模板**：虽用21种模板集成，但仅针对二分类，更细粒度的零样本能力（如疾病亚型）未验证。
- **下游任务局限**：主要聚焦病理二分类，未测试多分类、回归或更复杂的临床决策任务。
- **公平性**：与LaBraM比较时，LaBraM需要微调而ELM仅线性探测，虽显示表示质量但非完全公平；LaBraM使用了更多预训练数据（包括TUEV、TUSZ），而ELM排除了这些数据避免泄露，但TUSZ/TUEV线性探测中ELM仍优于TS等基线。
- **可解释性分析较浅**：对齐可视化仅展示少数示例，缺乏系统性分析（如频率、偏侧性的定位能力）。

（完）
