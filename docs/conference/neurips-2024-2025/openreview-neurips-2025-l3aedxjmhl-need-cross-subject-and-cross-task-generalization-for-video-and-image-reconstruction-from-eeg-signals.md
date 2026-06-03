---
title: "NEED: Cross-Subject and Cross-Task Generalization for Video and Image Reconstruction from EEG Signals"
title_zh: NEED：基于EEG信号的视频和图像重建的跨主体与跨任务泛化
authors: "Shuai Huang, Huan Luo, Haodong Jing, Qixian Zhang, Litao Chang, Yating Feng, Xiao Lin, Chendong Qin, Han Chen, Shuwen Jia, Siyi Sun, Yongxiong Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=L3aEdxJMHl"
tags: ["query:pbci-load"]
score: 6.0
evidence: 具有跨主体泛化能力的EEG解码框架，与被动BCI相关
tldr: EEG视觉重建面临跨主体和跨任务泛化难题。本文提出NEED，通过个体适应模块和多数据集预训练实现零样本泛化。实验显示在未见主体和任务上均取得高质量重建。其跨主体泛化方法可直接用于被动BCI的认知负荷评估，提升模型实用性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 1000, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 1114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1444, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1457, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 1190, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1458, \"height\": 1057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1430, \"height\": 855, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1450, \"height\": 875, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1415, \"height\": 842, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 708, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 627, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1451, \"height\": 591, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 1359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1447, \"height\": 1436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 483, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1442, \"height\": 817, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1441, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1442, \"height\": 876, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1440, \"height\": 403, \"label\": \"Table\"}]"
motivation: 现有EEG解码泛化性差，局限于特定视觉任务。
method: 引入个体适应模块和多数据集预训练，实现零样本跨主体跨任务。
result: 在多个数据集上实现高质量视觉重建，泛化性强。
conclusion: NEED为EEG通用解码提供了有效框架。
---

## Abstract
Translating brain activity into meaningful visual content has long been recognized as a fundamental challenge in neuroscience and brain-computer interface research. Recent advances in EEG-based neural decoding have shown promise, yet two critical limitations remain in this area: poor generalization across subjects and constraints to specific visual tasks. We introduce NEED, the first unified framework achieving zero-shot cross-subject and cross-task generalization for EEG-based visual reconstruction. Our approach addresses three fundamental challenges: (1) cross-subject variability through an Individual Adaptation Module pretrained on multiple EEG datasets to normalize subject-specific patterns, (2) limited spatial resolution and complex temporal dynamics via a dual-pathway architecture capturing both low-level visual dynamics and high-level semantics, and (3) task specificity constraints through a unified inference mechanism adaptable to different visual domains. For video reconstruction, NEED achieves better performance than existing methods. Importantly, Our model maintains 93.7% of within-subject classification performance and 92.4% of visual reconstruction quality when generalizing to unseen subjects, while achieving an SSIM of 0.352 when transferring directly to static image reconstruction without fine-tuning, demonstrating how neural decoding can move beyond subject and task boundaries toward truly generalizable brain-computer interfaces.

---

## 论文详细总结（自动生成）

# 论文结构化总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：基于EEG信号的视觉内容重建面临两大瓶颈：**跨主体泛化性差**（模型对训练集外的个体性能急剧下降）和**任务特异性约束**（图像与视频重建需独立设计框架，无法统一）。
- **研究背景**：现有脑机接口（BCI）中，EEG因其非侵入性、高时间分辨率、低成本等优势被广泛用于视觉解码。但个体间神经活动模式差异（解剖、电极位置、功能组织）导致模型学到主体特异性特征而非通用表征；同时，静态图像和动态视频的刺激特性差异要求不同架构，限制实际应用。
- **整体含义**：NEED旨在突破这些边界，实现真正可泛化的BCI——在未见主体和新任务上直接工作，无需微调。

## 2. 论文提出的方法论

### 核心思想
NEED提出一个统一框架，通过三个创新模块解决上述挑战：
1. **个体适应模块（IAM）**：在多数据集上预训练，将主体特定EEG信号标准化到公共表示空间。
2. **双路径架构（DSGNet）**：并行处理空间模式与时间动态，捕捉低层视觉动态（感知路径PU）和高层语义（语义路径SU）。
3. **统一推理机制**：根据任务类型（视频/图像）自适应调整条件信号，支持零样本跨任务迁移。

### 关键技术细节
- **IAM**：包含主体感知注意力机制（公式1：带主体嵌入的注意力输出 + 风格注入）和分层适应策略（信号级、频谱级、时间级、语义级）渐进归一化。预训练用多目标损失（重建损失 \(L_{recon}\)、对抗性主体解耦 \(L_{adv}\)、KL散度 \(D_{KL}\)）。
- **DSGNet**：
  - **空间流**：球谐函数编码电极位置，经图卷积网络建模电极间关系。
  - **时间流**：Riemann-Liouville分数阶变换（\(\alpha \in \{0.2,0.4,0.6,0.8\}\)）捕获多尺度动态，后接扩张时间卷积。
  - **跨流集成**：交叉注意力机制融合空间和时间特征，再通过门控融合输出。
- **感知理解模块（PU）**：含动态特征提取器（DFE）和时空记忆增强循环网络（SMARN），提取运动、空间、时间动态；采用双向动态对比对齐（BDC）损失对齐EEG与视觉特征。
- **语义理解模块（SU）**：利用CLIP-ViT-G/14、BLIP-2、LLM适配器将EEG特征映射为高层语义；使用层次语义对比（HSC）损失和跨模态语义对齐（CSA）损失。
- **统一推理**：任务适配器生成条件嵌入 \(c_t\)，融合ControlNet关键帧、文本嵌入、动态模式、EEG特征；通过任务编码 \(\tau_t\) 调节扩散过程（条件层调制），视频时激活时间注意，图像时增强空间细节。

## 3. 实验设计

### 数据集与场景
- **主要训练**：SEED-DV（20名被试、62通道、1400个视频片段、40个视觉类别）。
- **IAM预训练**：SEED（15人情感影片）、DEAP（32人音乐视频）、EEGEYENET（356人14通道视觉任务）。
- **跨任务测试**：THINGS-EEG（10人、22000张静态图片、1854个类别）。
- **跨主体泛化**：SEED-DV中留出未见主体测试。

### Benchmark与对比方法
- **分类任务**：对比SVM（PSD/DE）、MLP、GLMNet、ShallowNet、DeepNet、EEGNet、TSCNet、Conformer、BraVL、EEGPT、TSConv等。
- **重建任务**：对比EEG2video、Wang等（fMRI）、Kupershmidt（fMRI）、MinD-Video（fMRI）、NeuroClips（fMRI）、CognitionCapturer（EEG）、Mind’s Eye（fMRI）、META-MEG（MEG）等。
- **消融实验**：移除IAM、PU、SU、Task Conditioning、Dynamic Pattern、ControlNet、Caption等组件。

## 4. 资源与算力

- 论文仅在附录E（Implementation Details）中提到使用**NVIDIA A100 GPU**，但**未明确说明GPU数量、训练时长、总计算量**。消融与跨主体实验较多，合理推测需多卡训练数天至数周，但需更透明披露。

## 5. 实验数量与充分性

- **实验覆盖广泛**：共11张表格和多个图表，涵盖：
  - 视觉感知分类（9种任务，对比10+方法）。
  - 视频/图像重建（10+方法对比，7组消融）。
  - 跨主体泛化（不同训练主体数、单主体分析、组件消融）。
  - 时间动态分析、频率带贡献、脑区贡献。
- **充分性**：消融实验系统（核心组件逐一移除）、统计显著性标注（p<0.05）、误差棒报告。对比方法全面，包括EEG、fMRI、MEG方法（尽管fMRI/MEG非直接可比，但作者包含它们展示差距）。
- **客观公平**：使用公开数据集（SEED-DV、THINGS-EEG等），遵循标准预处理。跨任务测试为零样本（无微调），避免数据泄露。

## 6. 论文的主要结论与发现

- **分类性能**：DSGNet在40类top-1准确率达14.23%（相对最好基线提升101.8%），9类达29.93%，二分类达81.34%。
- **视频重建**：NEED在SEED-DV上2-way语义准确率0.898、SSIM 0.356，超越所有EEG方法，与fMRI方法可比。
- **跨主体泛化**：用19人训练，在未见主体上保持93.7%分类性能和92.4%重建质量；用10人训练仍保留76.3%分类性能。
- **跨任务泛化**：零样本迁移到THINGS-EEG图像重建，SSIM达0.352（EEG方法最佳），显著高于移除任务条件后的0.063。
- **消融关键**：IAM模块最重要（移除后2-way准确率从0.898降至0.642）；PU和SU互补贡献；任务条件对跨任务迁移必不可少。

## 7. 优点

1. **首个统一框架**：同时实现跨主体零样本和跨任务零样本（视频→图像），打破传统界限。
2. **IAM创新**：多数据集预训练+对抗解耦有效归一化主体差异，是泛化核心。
3. **架构设计合理**：双路径（感知+语义）互补，DSGNet时空分离再融合，符合神经科学原理。
4. **实验严谨**：大量消融、多个度量（SSIM、FVD、CLIP准确率等）、统计检验，结果可信。
5. **实际价值**：为通用BCI铺路，减少个体校准成本，支持动态场景。

## 8. 不足与局限

- **重建保真度有限**：复杂光照、细粒度物体仍无法达到照片级真实感（失败案例集中在这些场景）。
- **硬件依赖**：当前框架在62/64通道高密度EEG上表现最佳，对便携式设备（如14通道EMOTIV）适配挑战大（虽在EEGEYENET上有泛化测试，但性能远低于高密度）。
- **跨任务范围有限**：仅测试视频→图像迁移，未涉及文本、语音等其他模态；图像→视频迁移未验证。
- **算力成本不透明**：未报告训练时间和资源消耗，可重复性受影响。
- **伦理讨论不足**：仅简洁提及隐私和监管，未深入分析潜在滥用（如脑部信息窃取）。
- **基线对比偏差**：部分对比方法是fMRI/MEG，设备原理不同（EEG空间分辨率低），直接比较可能不公平（作者虽已注明，但仍需谨慎解读）。

（完）
