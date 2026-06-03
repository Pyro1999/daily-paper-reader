---
title: "ManiBCI: Manipulating EEG BCI with Invisible and Robust Backdoor Attack via Frequency Transform"
title_zh: ManiBCI：通过频域变换对EEG BCI进行不可见且鲁棒的后门攻击
authors: "Xuanhao Liu, Xinhao Song, Dexuan He, Wei-Long Zheng, Bao-liang Lu"
date: 2024-05-13
pdf: "https://openreview.net/pdf?id=NMwPKjNTEP"
tags: ["query:pbci-load"]
score: 4.0
evidence: 针对EEG BCI的后门攻击，涉及深度学习，与被动BCI安全性相关
tldr: 该论文研究EEG BCI中的后门攻击，提出ManiBCI方法，通过频域变换实现不可见且鲁棒的攻击，可任意操控目标类别。虽然论文主题是攻击而非认知负荷评估，但其暴露的深度学习模型漏洞对被动BCI系统的安全性有重要警示。此外，论文中使用的EEG和深度学习方法与被动BCI领域高度相关，因此对需求中的深度学习研究方法具有参考价值。
source: NeurIPS-2024-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 471, \"height\": 255, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1446, \"height\": 279, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 519, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1451, \"height\": 274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1446, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 513, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1450, \"height\": 1186, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1451, \"height\": 1244, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 1864, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1447, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1439, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-nmwpkjntep/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1434, \"height\": 1782, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1414, \"height\": 694, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1364, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 503, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1410, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1056, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1021, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1405, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1341, \"height\": 1557, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1304, \"height\": 1514, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-nmwpkjntep/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1339, \"height\": 1912, \"label\": \"Table\"}]"
motivation: EEG BCI的深度学习模型易受后门攻击，现有攻击缺乏隐蔽性和多目标能力。
method: 利用频域变换注入后门，实现任意目标类别的攻击且保持隐蔽。
result: 在多个EEG数据集上成功实现高成功率且不可见的攻击。
conclusion: EEG BCI系统的安全性需警惕此类后门威胁。
---

## Abstract
The electroencephalogram (EEG) based brain-computer interface (BCI) has taken the advantages of the tremendous success of deep learning (DL) models, gaining a wide range of applications. However, DL models have been shown to be vulnerable to backdoor attacks. Despite there are extensive successful attacks for image, designing a stealthy and effect attack for EEG is a non-trivial task. While existing EEG attacks mainly focus on single target class attack, and they either require engaging the training stage of the target DL models, or fail to maintain high stealthiness. Addressing these limitations, we exploit a novel backdoor attack called ManiBCI, where the adversary can arbitrarily manipulate which target class the EEG BCI will misclassify without engaging the training stage. Specifically, ManiBCI is a three-stages clean label poisoning attacks: 1) selecting one trigger for each class; 2) learning optimal injecting EEG electrodes and frequencies masks with reinforcement learning for each trigger; 3) injecting the corresponding trigger’s frequencies into poisoned data for each class by linearly interpolating the spectral amplitude of both data according to the learned masks. Experiments on three EEG datasets demonstrate the effectiveness and robustness of ManiBCI. The proposed ManiBCI also easily bypass existing backdoor defenses. Code will be published after the anonymous period.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：基于脑电图（EEG）的脑机接口（BCI）受益于深度学习（DL）模型，但其对后门攻击（backdoor attack）的脆弱性长期被忽视。图像领域已有大量成功攻击，但EEG信号存在信噪比低、类间形态差异小、需保持标签一致性等特性，使得设计隐蔽且有效的后门攻击非常困难。现有EEG后门攻击仅针对单一目标类别，且要么需要介入目标模型的训练过程，要么隐蔽性不足。
- **核心问题**：如何在不介入训练阶段的前提下，实现**多目标类别任意操控**的、**高隐蔽性**且**鲁棒**的后门攻击？具体包括三个子问题：  
  - Q1：如何获得高攻击成功率（ASR）的同时保持原始任务准确率？  
  - Q2：如何为不同EEG任务找到最优的电极和频率注入策略？  
  - Q3：如何保持触发样本的标签与形态一致性（避免被人类专家发现）？
- **整体含义**：提出一种名为**ManiBCI**的新型后门攻击，首次在频域对EEG BCI进行攻击，实现任意目标类别的操纵，且无需控制模型训练过程，具有高隐蔽性和鲁棒性。该工作暴露了EEG BCI系统的重大安全隐患，呼吁防御研究。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- 在**频域**通过线性插值注入干净数据与真实EEG触发数据的幅度谱，生成中毒样本。选择真实EEG作为触发器（clean label），保持自然频率分布；使用强化学习（RL）为每个触发器自适应地学习最优的电极子集和频率子集作为注入掩码；通过奖励函数引导策略网络同时优化攻击性能、鲁棒性和隐蔽性。

### 关键技术细节
1. **三阶段流程**（见图1a-c）：
   - **阶段1：触发器选择**：从每个类别中随机选取一个真实EEG样本作为该类的触发器。
   - **阶段2：学习最优注入策略（RL）**：
     - 将问题建模为非凸优化：最小化清洁准确率损失与攻击成功率损失的加权和。
     - 使用**策略梯度（Policy Gradient）** 方法训练一个轻量策略网络π_θ，输出两个向量：v1∈R^E（电极重要性）、v2∈R^F（频率重要性），取Top-k作为注入掩码M_ci^e（电极）和M_ci^f（频率）。
     - **奖励函数**设计为：  
       `R_t = CA + λ·ASR + μ·dis(M_ci^f) + ν·min(M_ci^f)`  
       其中dis()为注入频率位置对间的最小距离（鼓励分散），min()为最低频率位置（鼓励注入高频，提升隐蔽性）。λ, μ, ν为超参数。
     - RL收敛后取最佳动作作为该触发器的策略。
   - **阶段3：生成中毒数据**：
     - 对干净数据x_i和触发器x_tci分别做FFT，得到幅度谱A_xi、A_xtci和相位谱P_xi（保留相位）。
     - 根据掩码M_ci，通过线性插值合成中毒幅度谱：`AP_xi = [(1-α)A_xi + α·A_xtci] ⊙ M_ci + A_xi ⊙ (1-M_ci)`。α∈(0,1]为插值比例。
     - 用iFFT恢复时间域信号：`x_pi = F^{-1}(AP_xi, P_xi)`。
   - 中毒样本保持原标签（clean label），与原始训练集混合训练目标模型。

2. **多目标攻击**：每个类别有独立的触发器和注入策略，攻击时可指定任意目标类别，模型会将该类别的触发样本分类为目标类别。

3. **无需控制训练阶段**：中毒数据直接注入训练集，模型正常训练即可植入后门。

## 3. 实验设计

### 使用的数据集与场景
- **情感识别（ER）**：SEED数据集，3类情绪（开心、中性、悲伤），15名受试者，62通道，200Hz采样，1秒片段。
- **运动想象（MI）**：BCIC-IV-2a，4类运动想象（左手、右手、脚、舌头），9名受试者，22通道，250Hz，1秒片段。
- **癫痫检测（ED）**：CHB-MIT，4类（发作期、发作前期、发作后期、发作间期），23名患者（处理后视为10组），23通道，256Hz，1秒片段。

### Benchmark与对比方法
- **目标模型**：EEGNet、DeepCNN、LSTM（三种常用EEG DL模型）。
- **对比基线**（均为多目标多触发器扩展）：
  - **非隐蔽**：PatchMT（固定时间窗口填充常数）、PulseMT（窄带脉冲信号）
  - **隐蔽**：CompMT（幅度压缩）、AdverMT（基于对抗滤波的空间滤波器学习）
- **评价指标**：清洁准确率（CA）和攻击成功率（ASR），要求对每个测试样本枚举所有目标类别，分类正确即视为成功。

### 实验设置
- 采用**留一受试者交叉验证**（LOSO）：对于n个受试者的数据集，每次选1个作为中毒集（Dp），1个作为测试集，其余作训练集（含验证集）。每个方法运行n(n-1)次验证。
- 中毒率ρ=40%（主实验），插值比例α=0.8，电极注入比例γ=0.5，频率注入比例β=0.1。
- RL训练：策略网络用Adam，lr=0.01，运行T步取最佳策略。

## 4. 资源与算力

- **文中明确提及**：使用两台服务器：
  - 一台配备1块Nvidia Tesla V100 GPU（CUDA 12.3），用于RL训练。
  - 另一台配备4块Nvidia RTX 3090 GPU（CUDA 11.4），用于后门攻击实验。
- **训练时长**：RL在ED数据集上约5.2小时（ER 2.5h, MI 1.8h），相比于遗传算法（GA）的10~30小时，显著节省时间。主后门攻击训练的具体时长未报告，但可推断每个模型训练100 epoch，批量32，在RTX 3090上应较快。
- **总结**：算力资源充足，但未对每个实验的精确GPU时长做详细统计，仅给出了RL阶段的相对耗时。

## 5. 实验数量与充分性

- **实验数量**：非常丰富，覆盖三大类任务、三种目标模型、多种基线、多种超参数（中毒率、注入率、RL超参数等），以及多种防御和预处理鲁棒性测试。
- **具体实验分组**：
  - **主实验**（表1）：3 datasets × 3 models × 5 methods = 45个配置，每个配置有CA和每个类的ASR（共多列），结果充分。
  - **RL优化对比**（表2）：对比Random、GA、Policy Gradient，在3个数据集上。
  - **策略迁移性**（表3）：在3个数据集上，用模型f学到的策略攻击模型f_hat，交叉验证。
  - **超参数分析**（图3、表7-9）：不同中毒率（0.05~0.40）、频率注入率β、电极注入率γ、RL中的λ等，进行网格搜索。
  - **鲁棒性实验**：
    - 预处理（20Hz低通、30Hz高通、25%降采样）（表4）。
    - 防御：Neural Cleanse（图4）、STRIP（图5）、Spectral Signature（图6）、Fine-Pruning（图7）。
  - **可视化**：图2 t-SNE、图8中毒样本时域图、附录中更多触发重建、学习曲线等。
- **充分性与公平性**：实验设计基本全面，公平性较好，基线方法参数均尽量调优（附录D说明）。但存在以下不足：
  - 未与最新图像频域后门攻击（如FIBA、FTROJAN）直接对比（因为不适用）。
  - 对于隐蔽性，仅依赖视觉分析（图8）和防御绕过，未进行系统的人类感知实验。
  - 未讨论中毒样本对模型泛化能力的影响（如过拟合风险）。
  - 实验重复次数（标准差）只在表10部分提供，主实验结果未显示误差棒，统计显著性仅提及p<0.05但未给出具体值。

## 6. 主要结论与发现

- **有效性**：ManiBCI在几乎所有配置下显著优于基线，ASR常超过0.9，在MI数据集上可达1.0（EEGNet），且CA无明显下降（甚至在某些任务中略有提升）。
- **RL优势**：Policy Gradient相比GA和随机搜索，在更短的时间（GA的16%）内找到接近最优的策略，且在50 epoch内收敛。
- **可迁移性**：在一个模型上学习的策略可有效转移到其他模型（轻微性能下降），表明策略泛化性较好。
- **鲁棒性**：
  - 对常见EEG预处理（低通/高通滤波、降采样）鲁棒，但若移除奖励函数中的离散损失（DIS），则鲁棒性显著下降。
  - 可轻易绕过Neural Cleanse、STRIP、Spectral Signature、Fine-Pruning等经典后门防御。
- **隐蔽性**：通过高频损失（HF loss）使中毒样本在时域上与干净样本几乎不可区分（图8），t-SNE显示嵌入到真实数据流形中（图2）。

## 7. 优点

- **创新性**：
  1. 首次在EEG后门攻击中采用频域注入，利用真实EEG作为触发器，保持自然频率分布。
  2. 首次将EEG电极和频率选择性注入问题建模为RL问题，并设计包含鲁棒性和隐蔽性目标的奖励函数。
  3. 支持多目标任意类别攻击，无需控制训练阶段，具有实际威胁性。
- **实验全面性**：
  - 覆盖三个典型EEG任务（情感、运动、癫痫），三种主流DL架构。
  - 对比了多种基线（包括非隐蔽和隐蔽），并进行了充分的超参数分析、鲁棒性测试。
  - 对防御方法的绕过能力进行了细致评估。
- **可复现性**：提供了详细的超参数设置、网络架构、数据预处理步骤，承诺公开代码。
- **可视化清晰**：通过t-SNE、时域图、学习曲线等直观展示隐蔽性和有效性。

## 8. 不足与局限

- **局限性（作者自述）**：
  - FFT与iFFT操作带来额外计算开销，比时域直接注入方法（如PatchMT、PulseMT）更耗时。
  - RL寻找最优策略需要训练多个候选模型（约50个），计算成本较高，但可通过随机策略或固定策略牺牲部分性能来避免（表2显示随机也有不错结果）。
- **实验覆盖不足**：
  - 仅针对三种EEG任务，未覆盖更复杂的BCI场景（如P300、SSVEP）或在线实时场景。
  - 未考虑自适应攻击场景（即攻击者动态调整策略）。
  - 未与其他域无关的后门防御（如激活聚类、神经清除变体）进行对比。
- **公平性与客观性**：
  - 主实验结果未报告标准差或置信区间（仅部分超参数分析有），统计可靠性存疑。
  - 基线方法PatcMT和PulseMT的参数（常数大小）可能未达到最优，尽管作者声称尽力调整，但缺少详细搜索过程。
  - 未对比图像领域成熟的频域后门攻击（如FTROJAN、FIBA），尽管它们不直接用于EEG，但可证明方法在频域上的独特性。
- **应用限制**：
  - 攻击假设攻击者能控制部分训练数据（作为数据提供者），且需要了解目标模型结构（用于RL训练策略），现实威胁有限。
  - 模型需要训练至收敛，对联邦学习、在线学习等分布式场景的适用性未探讨。
  - 隐蔽性仅依靠视觉评估和防御绕过，缺乏人类评估实验或定量感知指标（如PSNR、SSIM）。
- **其他**：
  - 未分析中毒样本对模型方差、公平性、隐私的影响。
  - RL奖励函数中的超参数（λ, μ, ν）需手动调节，依赖经验值，未提供自动调优方法。

（完）
