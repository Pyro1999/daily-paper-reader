---
title: Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling
title_zh: 基于高CMRR与EMRMS数学建模的低延迟表面肌电实时校正系统设计
authors: "Lo, H. U., Gao, Z., Loi, H. F., Cheng, S. K."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.724714v1.full.pdf"
tags: ["query:robust-eeg"]
score: 6.0
evidence: sEMG干扰抑制方法可迁移至EEG去噪
tldr: "表面肌电信号（sEMG）受工频干扰（PLI）和数字处理延迟影响，临床采纳受限。本文设计模拟-数字联合校正系统，采用高CMRR前端、指数窗口RMS（EMRMS）包络估计器和自适应单音PLI消除器。EMRMS将计算复杂度降至O(1)，实现确定性低延迟（每样本8.2μs，端到端30ms）和极低CPU占1.6%。在Ninapro DB2上平均SNR提升13.9dB，包络误差70μV，形态学保真度高（ρ=0.993），代码开源。"
source: biorxiv
selection_source: fresh_fetch
motivation: 解决sEMG中工频干扰与过长数字流水线群延迟对临床采纳的限制。
method: 协同设计高CMRR模拟前端与指数窗口RMS包络估计器（EMRMS）及递归自适应PLI消除器，并提供闭环CMRR模型与稳定性分析。
result: "单通道PLI校正SNR提升9.7dB，多通道平均13.9dB，端到端延迟约30ms，CPU占1.6%，包络RMSE 70μV，相关系数0.993。"
conclusion: 系统实现极低延迟与高能效，显著抑制工频干扰，保持信号形态，开源代码便于复现与应用。
---

## 摘要
表面肌电信号（sEMG）是肌电假肢、外骨骼和康复系统中最实用的无创接口，但电源线干扰（PLI）污染和过长的数字流水线群延迟仍限制了其临床采用。本文提出一种协同设计的模数校正系统，结合了高CMRR前端、指数窗RMS（EMRMS）包络估计器和递归单音PLI消除器。我们提出了一个捕获电极-皮肤不平衡的闭式CMRR模型，并提供了LMS消除器的完整稳定性分析。EMRMS估计器将计算开销从O(L)严格降低到O(1)的时间和空间复杂度。该算法无数据依赖分支，实现确定的算法执行时间（在RTOS环境下零抖动），并且原生兼容缺乏硬件浮点单元（FPU）的微控制器上的定点算术。参考实现达到每样本8.2微秒的中位延迟，产生约30毫秒的端到端延迟——为机电执行留出超过90毫秒的充裕预算——同时仅需1.6%的活跃CPU占空比，从而延长深度睡眠间隔。在公开的Ninapro DB2数据集上的验证表明，平均SNR提升13.9 dB（12通道平均；单通道对比：9.7 dB，表3），与长度为200的矩形参考相比，包络RMSE为70.0微伏。配对Wilcoxon符号秩检验证实了相对于静态基线的统计显著性（p < 0.001），Pearson相关分析（ρ = 0.993 ± 0.0002）确认了严格的形态保真度。完整的开源代码库和基准测试已公开发布。

## Abstract
Surface electromyography (sEMG) is the most practical non-invasive interface for myoelectric prostheses, exoskeletons, and rehabilitation systems, but power-line interference (PLI) contamination and excessive digital pipeline group delay still limit its clinical adoption. This paper proposes a co-designed analog-digital correction system combining a high-CMRR front-end with an exponentially-windowed RMS (EMRMS) envelope estimator and a recursive single-tone PLI canceller. We present a closed-form CMRR model capturing the electrode-skin imbalance, and provide a complete stability analysis of the LMS canceller. The EMRMS estimator reduces the computational overhead from O(L) to strictly O(1) in both time and space complexities. Featuring no data-dependent branching, the algorithm achieves deterministic algorithmic execution time (zero jitter under an RTOS environment) and is natively compatible with fixed-point arithmetic on microcontrollers lacking a hardware Floating-Point Unit (FPU). A reference implementation reaches an 8.2 {micro}s median per-sample latency, yielding an end-to-end delay of[~] 30 ms -- leaving a generous >90 ms budget for electromechanical actuation -- while requiring an active CPU duty cycle of merely 1.6%, enabling prolonged deep-sleep intervals. Validation on the public Ninapro DB2 dataset demonstrates a 13.9 dB mean SNR improvement (averaged across 12 channels; single-channel comparison: 9.7 dB, Table 3) and a 70.0 {micro}V envelope RMSE against a length-200 rectangular reference. Paired Wilcoxon signed-rank tests confirm statistical significance (p < 0.001) over static baselines, and Pearson correlation analysis ({rho} = 0.993 {+/-} 0.0002) confirms strict morphological fidelity. The full open-source codebase and benchmarks are publicly released.

O_TBL View this table:
org.highwire.dtl.DTLVardef@1ca028forg.highwire.dtl.DTLVardef@16e0576org.highwire.dtl.DTLVardef@2886b5org.highwire.dtl.DTLVardef@a4055eorg.highwire.dtl.DTLVardef@5c7a58_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3:C_FLOATNO O_TABLECAPTIONQuantitative comparison on a common 60 s segment of Ninapro-like synthetic sEMG (single channel) with a 3 mV 50.3 Hz mains tone  slightly drifted from the static notchs design centre at 50.0 Hz, stress-testing the adaptive corrector under a frequency mismatch. The Ninapro multi-channel aggregate (13.9 dB) reported in Section 3.4 uses mains exactly at 50 Hz (matched notch) and so achieves a higher {Delta} SNR. "MAC/sample" excludes the EMRMS square root and the pre-computed LMS sine/cosine.

C_TABLECAPTION C_TBL