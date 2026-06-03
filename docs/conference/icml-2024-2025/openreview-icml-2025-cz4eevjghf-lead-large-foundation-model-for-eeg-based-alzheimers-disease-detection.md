---
title: "LEAD: Large Foundation Model for EEG-Based Alzheimer’s Disease Detection"
title_zh: LEAD：基于EEG的阿尔茨海默病检测的大型基础模型
authors: "Yihe Wang, Nan Huang, Nadia Mammone, Marco Cecchi, Xiang Zhang"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=cz4EevJGHf"
tags: ["query:pbci-load"]
score: 9.0
evidence: 用于疾病检测的大型EEG基础模型
tldr: 针对EEG数据规模不足和个体差异导致的检测性能差问题，本文构建了包含813名被试的最大EEG-AD数据集，并提出首个EEG基础模型LEAD。通过自监督预训练与全流程优化，LEAD在阿尔茨海默病检测任务上显著超越现有方法，为EEG基础模型在疾病诊断中的应用树立了标杆。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 724, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1696, \"height\": 917, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1378, \"height\": 1034, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1766, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 876, \"height\": 572, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1780, \"height\": 600, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 1148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1423, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1775, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 891, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1776, \"height\": 537, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1782, \"height\": 560, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 893, \"height\": 699, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1780, \"height\": 724, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 894, \"height\": 420, \"label\": \"Table\"}]"
motivation: 现有EEG检测方法受限于数据集规模和个体差异，性能不佳。
method: 构建大规模EEG-AD数据集，提出首个EEG基础模型LEAD，含自监督预训练与端到端流程。
result: 在阿尔茨海默病检测上大幅超越现有方法，验证了EEG基础模型的可行性。
conclusion: LEAD展示了大规模EEG基础模型在疾病检测中的巨大潜力，为后续研究奠定基础。
---

## Abstract
Electroencephalogram (EEG) provides a non-invasive, highly accessible, and cost-effective solution for Alzheimer’s Disease (AD) detection. However, existing methods, whether based on manual feature extraction or deep learning, face two major challenges: the lack of large-scale datasets for robust feature learning and evaluation, and poor detection performance due to inter-subject variations. To address these challenges, we curate an EEG-AD corpus containing 813 subjects, which forms the world’s largest EEG-AD dataset to the best of our knowledge. Using this unique dataset, we propose **LEAD**, the first large foundation model for EEG-based AD detection. Our method encompasses an entire pipeline, from data selection and preprocessing to self-supervised contrastive pretraining, fine-tuning, and key setups such as subject-independent evaluation and majority voting for subject-level detection. We pre-train the model on 11 EEG datasets (4 AD and 7 non-AD) and unified fine-tune it on 5 AD datasets. Our self-supervised pretraining design includes sample-level and subject-level contrastive learning to extract useful general EEG features. Fine-tuning is performed on 5 channel-aligned datasets together. The backbone encoder incorporates temporal and channel embeddings to capture features across both temporal and spatial dimensions. Our method demonstrates outstanding AD detection performance, achieving up to a 9.86% increase in F1 score at the sample level and up to a 9.31% improvement at the subject level compared to state-of-the-art methods. The results of our model strongly confirm the effectiveness of subject-level contrastive pretraining and channel-aligned multi-dataset fine-tuning for addressing inter-subject variation. The source code is at \url{https://anonymous.4open.science/r/LEAD-3B51}.

---

## 论文详细总结（自动生成）

# 论文《LEAD: Large Foundation Model for EEG-Based Alzheimer’s Disease Detection》中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：阿尔茨海默病（AD）是常见神经退行性疾病，早期检测有助于延缓病情。现有基于EEG的AD检测方法面临两大挑战：①缺乏大规模高质量数据集，现有研究通常仅用几十名受试者；②受试者间差异（inter-subject variation）导致模型难以泛化到未见受试者。传统手动特征提取或深度学习方法在这些问题上效果不佳。
- **整体含义**：本文旨在解决数据稀缺和个体差异问题，通过构建当前最大EEG-AD数据集（813名受试者），并提出首个专用于EEG-AD检测的大型基础模型LEAD，实现显著性能提升。

## 2. 论文提出的方法论
- **核心思想**：采用“大规模自监督预训练 + 多数据集统一微调”范式，利用样本级和受试者级对比学习提取通用EEG特征，并通过通道对齐实现跨数据集联合训练。
- **关键技术细节**：
  - **数据集构建**：整合9个AD数据集（6个公开+3个私有）和7个非AD数据集（健康或其他神经疾病），共813名AD受试者（预训练+微调）。预训练使用11个数据集（4个AD+7个非AD），共2354名受试者、1,165,361个1秒样本；微调使用5个高质量AD数据集，共615名受试者。
  - **数据预处理**：统一通道对齐到19个标准国际10-20系统通道（缺失通道插值，多余通道选择最近3D坐标）；统一采样频率至128Hz；分割为1秒样本（128个时间点）；带通滤波0.5-45Hz；z-score归一化。
  - **自监督预训练**：采用SimCLR架构，但引入**受试者级对比学习**。每个样本经两种数据增强生成两个视图，然后计算两个对比损失：
    - 样本级损失（InfoNCE）：同一样本的不同增强视为正对，其他样本为负对。
    - 受试者级损失（InfoNCE）：同一受试者的所有样本视为正对，不同受试者样本为负对。
    - 总损失为加权和：\( L = \lambda_1 L_{\text{Sam}} + \lambda_2 L_{\text{Sub}} \)，其中 \(\lambda_1=\lambda_2=0.5\)。
    - 使用索引洗牌算法确保同受试者样本在批次中出现。
  - **骨干编码器架构**：采用简化版ADformer（双分支Transformer）：
    - 时间分支：将跨通道的时序片段分割为非重叠patch，映射为token + 位置编码，经Transformer编码。
    - 空间分支：将原始数据转置后加通道位置编码，通过1D卷积升维和线性投影得到每个通道的全局表示，经Transformer编码。
    - 取两个分支的最后一个token拼接作为最终表示 \(h\)；预训练时通过投影头 \(g\) 映射到 \(z\) 用于对比；下游任务时直接使用 \(h\) 接线性分类器。
  - **训练与评估**：
    - 受试者独立（subject-independent）划分：训练/验证/测试集按受试者分割，确保同一受试者样本只出现在一个集合。
    - 统一微调：5个AD数据集同时微调，基于加权F1选择最佳模型。
    - 受试者级分类：对每个受试者的所有样本预测结果进行多数投票。

## 3. 实验设计
- **数据集**：
  - 预训练：11个数据集（AD-Auditory, ADFSU, ADSZ, APAVA, Depression, PEARL-Neuro, REEG-BACA, REEG-PD, REEG-SRM, TDBrain, TUEP）。
  - 微调/评估：5个AD数据集（ADFTD, BrainLat, CNBPM, Cognision-ERP, Cognision-rsEEG），均为AD vs HC二分类。
- **Benchmark**：与10个基线方法对比，包括5个全监督方法（TCN, Transformer, Conformer, TimesNet, Medformer）、3个自监督方法（TS2Vec, BIOT, EEG2Rep）、2个大型EEG基础模型（LaBraM, EEGPT）。
- **对比设置**：
  - 自己方法有三个变种：LEAD-Vanilla（单数据集全监督，无通道对齐）、LEAD-Sup（多数据集统一全监督）、LEAD-Base（自监督预训练+统一微调）。
  - 基线方法按各自公开代码或推荐设置运行，统一数据划分和训练框架（除LaBraM/EEGPT外）。
- **评估指标**：样本级准确率/F1（宏平均）和受试者级准确率/F1（宏平均，经多数投票）。
- **实验充分性**：
  - 主实验结果（表2）：在5个数据集上给出了均值与标准差（5个随机种子）。
  - 消融实验（附录F）：①非AD数据集数量对性能的影响（5→7→9→11个预训练数据集）；②AD数据集数量在统一监督学习中的影响（表6）；③对比学习模块消融（样本级 vs 受试者级 vs 两者结合，表7）；④单数据集微调 vs 统一微调（表8）；⑤仅使用公开数据集的训练（表9）。
  - 补充实验（附录G）：①频带分析（δ, θ, α, β, γ）对性能的影响（表10）；②通道重要性分析（掩蔽不同脑区通道，表11）。

## 4. 资源与算力
- 论文明确说明：所有实验在**单张RTX 4090 GPU**和**一台配备4张RTX A5000 GPU的服务器**上运行，使用Python 3.8、PyTorch 2.0.0。
- 预训练固定50个epoch，微调/全监督训练最多100个epoch（早停15个epoch patience）。未给出具体训练时长，但可根据算力规模估计（RTX 4090约24GB显存，A5000约24GB，总批次512/128）。

## 5. 实验数量与充分性
- **数量**：主实验包含5个数据集、10个基线、4个自身变体，共记录80个（5×（10+4）？实际表2中每个方法在每个数据集上给出均值标准差，数据点较多）。消融实验至少5组（非AD数据集消融、AD数据集消融、对比模块消融、微调策略消融、公开数据训练）。补充实验2组（频带、通道重要性）。
- **充分性**：实验设计较为全面，覆盖了关键组件（预训练数据量、对比学习模块、微调策略）。所有结果基于5个随机种子取均值标准差，统计可靠。数据集划分采用受试者独立，避免了数据泄露。基线选择覆盖主流方法（全监督、自监督、现有EEG基础模型）。
- **客观性/公平性**：论文在实现细节中说明所有基线（除LaBraM和EEGPT）都在统一代码框架下训练，超参数设置合理。但注意：LaBraM和EEGPT使用了其公开预训练模型，微调时需将数据重采样至其要求的格式（如8秒/200Hz或4秒/200Hz），可能与LEAD的1秒/128Hz不一致，存在潜在不公平。不过论文在结果中给出了这些模型的性能。

## 6. 论文的主要结论与发现
- LEAD-Base（预训练+统一微调）在大多数数据集上显著优于所有基线，受试者级F1最高达100%（CNBPM）和91.86%（Cognision-rsEEG）。
- 受试者级对比学习是提升跨受试者泛化能力的关键：相比仅用样本级对比，受试者级对比在4/5数据集上提升约5% F1。
- 统一微调（同时微调多个数据集）优于单独微调，尤其对通道数较少的Cognision数据集帮助巨大（超过20% F1提升）。
- 添加更多非AD预训练数据集能普遍提升性能，表明多样化预训练对学习通用EEG表征有益。
- 频带分析表明Theta/Alpha/Beta是AD检测最关键的频段；通道重要性分析表明额叶和枕叶区域最重要。

## 7. 优点
- **数据集规模**：构建了当前最大的EEG-AD语料库（813受试者），覆盖多种场景和设备，弥补了领域数据稀缺短板。
- **方法创新**：首次将受试者级对比学习引入EEG-AD检测，有效缓解个体差异问题；通道对齐策略使跨数据集联合训练成为可能。
- **评估严谨**：采用受试者独立划分和多数投票，贴近实际应用场景；5个随机种子统计结果，实验可重复性强。
- **开源**：代码和模型权重公开，促进领域发展。
- **可解释性分析**：频带和通道重要性实验提供了神经科学角度的验证，增强模型可信度。

## 8. 不足与局限
- **通道对齐的信息损失**：将大于19通道的数据丢弃多余通道，可能导致原始空间信息丢失（如128通道的BrainLat数据）。论文虽声称此权衡可接受，但未系统评估信息损失程度。
- **预训练数据多样性有限**：尽管包含非AD疾病，但所有数据均为静息态或ERP任务，未包含睡眠、运动想象等任务，可能限制通用特征学习。
- **对比学习模块未与生成式方法结合**：仅采用对比学习，未探索掩码重建（如LaBraM、EEGPT）等自监督范式。附录H.3中提到未来可考虑结合。
- **ADFTD数据集异常**：LEAD-Base在ADFTD上性能低于LEAD-Sup（无预训练），消融实验也显示受试者级对比在ADFTD效果差，原因未阐明，可能该数据集存在特殊混淆。
- **计算资源需求**：模型参数量仅3.4M（小模型），但预训练涉及11个数据集、50个epoch，计算成本未具体报告。
- **基线比较可能不公平**：LaBraM和EEGPT需重采样数据至其固定格式（更长的样本长度），与LEAD的1秒样本差异大，可能影响其性能。论文未进行等长样本的公平比较。
- **未与最新基于基础模型的方法对比**：如Neuro-BERT、EEG2Vec等未纳入，但文中已覆盖主流代表性方法。

（完）
