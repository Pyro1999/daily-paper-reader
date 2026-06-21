---
title: Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling
title_zh: 基于高CMRR与EMRMS数学建模的低延迟表面肌电实时校正系统设计
authors: "Lo, H. U., Gao, Z., Loi, H. F., Cheng, S. K."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.724714v2.full.pdf"
tags: ["query:robust-eeg"]
score: 6.0
evidence: 肌电去噪方法可迁移至脑电解噪
tldr: "表面肌电信号受工频干扰和数字处理群延迟限制临床推广。本文提出协同设计的模拟-数字校正系统，含高CMRR前端、指数窗RMS包络估计器和递归单音PLI自适应消除器。EMRMS估计器将计算复杂度从O(L)降为O(1)，无数据依赖分支，实现确定性执行。参考实现每样本延迟8.2μs，端到端约30ms，CPU占空比仅1.6%。在Ninapro DB2数据集上平均SNR提升13.9dB，包络RMSE为70μV，形态保真度高达0.993。系统开源，为肌电假肢等提供低延迟高保真实时方案。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有sEMG系统受工频干扰和数字群延迟影响，难以满足临床实时性，需低延迟高保真校正方案。
method: 提出高CMRR前端结合EMRMS包络估计与LMS自适应PLI消除器，EMRMS复杂度降为O(1)，并给出闭环CMRR模型和稳定性分析。
result: "实现8.2μs每样本延迟，端到端30ms，CPU占空比1.6%；SNR提升13.9dB，包络RMSE 70μV，形态保真度ρ=0.993。"
conclusion: 该低延迟校正系统为肌电接口提供高效实时方案，开源代码利于推广复现。
---

## 摘要
表面肌电（sEMG）是肌电假肢、外骨骼和康复系统最实用的非侵入式接口，但工频干扰（PLI）污染和过长的数字流水线群延迟仍限制其临床采用。本文提出了一种数模协同校正系统，结合高共模抑制比（CMRR）前端、指数窗均方根（EMRMS）包络估计器和递归单音PLI抵消器。我们给出了一个捕捉电极-皮肤不平衡的闭式CMRR模型，并提供了LMS抵消器的完整稳定性分析。EMRMS估计器将计算开销从[O]（L）严格降低到[O]（1）的时间和空间复杂度。该算法无数据依赖性分支，实现确定性算法执行时间（RTOS环境下零抖动），且原生兼容缺乏硬件浮点单元（FPU）的微控制器上的定点算术。参考实现达到每样本8.2微秒的中位延迟，产生约30毫秒的端到端延迟——为机电驱动留下充裕的>90毫秒预算——同时仅需1.6%的主动CPU占空比，支持长时间深度睡眠间隔。在公共Ninapro DB2数据集上的验证表明，平均信噪比改善13.9 dB（12通道平均；单通道比较：9.7 dB，表3），包络均方根误差为70.0微伏（相对于长度为200的矩形参考）。配对Wilcoxon符号秩检验证实相对于静态基线的统计显著性（p < 0.001），皮尔逊相关分析（ρ = 0.993 ± 0.0002）确认严格的形态保真度。完整的开源代码库和基准测试已公开发布。

O_TBL 查看此表：
org.highwire.dtl.DTLVardef@192c116org.highwire.dtl.DTLVardef@1c2966aorg.highwire.dtl.DTLVardef@213522org.highwire.dtl.DTLVardef@277968org.highwire.dtl.DTLVardef@193b8ab_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3: C_FLOATNO O_TABLECAPTION在常见60秒Ninaropro样合成sEMG（单通道）片段上的定量比较，其中包含从静态陷波设计中心50.0 Hz轻微漂移的3 mV 50.3 Hz市电音调，在频率失配下对自适应校正器进行压力测试。第3.4节报告的Ninapro多通道聚合值（13.9 dB）使用恰好50 Hz市电（匹配陷波），因此获得更高ΔSNR。“MAC/样本”不包括EMRMS平方根和预计算的LMS正弦/余弦。

C_TABLECAPTION C_TBL

## Abstract
Surface electromyography (sEMG) is the most practical non-invasive interface for myoelectric prostheses, exoskeletons, and rehabilitation systems, but power-line interference (PLI) contamination and excessive digital pipeline group delay still limit its clinical adoption. This paper proposes a co-designed analog-digital correction system combining a high-CMRR front-end with an exponentially-windowed RMS (EMRMS) envelope estimator and a recursive single-tone PLI canceller. We present a closed-form CMRR model capturing the electrode-skin imbalance, and provide a complete stability analysis of the LMS canceller. The EMRMS estimator reduces the computational overhead from[O] (L) to strictly[O] (1) in both time and space complexities. Featuring no data-dependent branching, the algorithm achieves deterministic algorithmic execution time (zero jitter under an RTOS environment) and is natively compatible with fixed-point arithmetic on microcontrollers lacking a hardware Floating-Point Unit (FPU). A reference implementation reaches an 8.2 {micro}s median per-sample latency, yielding an end-to-end delay of[~] 30 ms -- leaving a generous >90 ms budget for electromechanical actuation -- while requiring an active CPU duty cycle of merely 1.6%, enabling prolonged deep-sleep intervals. Validation on the public Ninapro DB2 dataset demonstrates a 13.9 dB mean SNR improvement (averaged across 12 channels; single-channel comparison: 9.7 dB, Table 3) and a 70.0 {micro}V envelope RMSE against a length-200 rectangular reference. Paired Wilcoxon signed-rank tests confirm statistical significance (p < 0.001) over static baselines, and Pearson correlation analysis ({rho} = 0.993 {+/-} 0.0002) confirms strict morphological fidelity. The full open-source codebase and benchmarks are publicly released.

O_TBL View this table:
org.highwire.dtl.DTLVardef@192c116org.highwire.dtl.DTLVardef@1c2966aorg.highwire.dtl.DTLVardef@213522org.highwire.dtl.DTLVardef@277968org.highwire.dtl.DTLVardef@193b8ab_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3:C_FLOATNO O_TABLECAPTIONQuantitative comparison on a common 60 s segment of Ninapro-like synthetic sEMG (single channel) with a 3 mV 50.3 Hz mains tone  slightly drifted from the static notchs design centre at 50.0 Hz, stress-testing the adaptive corrector under a frequency mismatch. The Ninapro multi-channel aggregate (13.9 dB) reported in Section 3.4 uses mains exactly at 50 Hz (matched notch) and so achieves a higher {Delta} SNR. "MAC/sample" excludes the EMRMS square root and the pre-computed LMS sine/cosine.

C_TABLECAPTION C_TBL