<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-06-24
- 运行时间：2026-06-24 22:11:56 UTC
- 运行状态：成功
- 本次总论文数：13
- 精读区：6
- 速读区：7

### 今日简报（AI）
今天聚焦脑与生理信号基础模型，精读两篇高分论文：基于流匹配的脑基础模型和基于时空池化单token重构的通用生理信号自监督学习。最值得关注的方向是脑基础模型与通用生理信号自监督学习，分别采用流匹配和单token重构实现高效特征提取。下一步建议尝试将流匹配或自监督方法应用到自己的EEG/生理信号分析任务中，提升模型泛化能力。
- 详情：[/202606/24/README](/202606/24/README)

### 精读区论文标签
1. [B[FM]$^2$: Brain Foundation Model via Flow Matching with SplitUNet](/202606/24/2606.20812v1-bfm2-brain-foundation-model-via-flow-matching-with-splitunet)  
   标签：评分：9.0/10、query:pbci-load
   evidence：提出基于流匹配的脑电基础模型，可直接用于脑机接口任务
2. [SPOTR: Spatio-temporal Pooling One-Token Reconstruction for Universal Physiological Signal Self-supervised Learning](/202606/24/2606.21973v1-spotr-spatio-temporal-pooling-one-token-reconstruction-for-universal-physiological-signal-self-supervised-learning)  
   标签：评分：9.0/10、query:pbci-load
   evidence：通用的EEG信号自监督学习框架
3. [Foundation Models for Epileptogenic Zone Identification in Drug-Resistant Epilepsy](/202606/24/2606.22657v1-foundation-models-for-epileptogenic-zone-identification-in-drug-resistant-epilepsy)  
   标签：评分：9.0/10、query:pbci-load
   evidence：提出用于颅内脑电信号处理的双基座模型系统
4. [Embedded Polygon Symbolic Transfer Entropy (EPSTE): A Geometric Token and Deep Learning Approach to Estimating Transfer Entropy in Neuroimaging Time Series](/202606/24/2606.21754v1-embedded-polygon-symbolic-transfer-entropy-epste-a-geometric-token-and-deep-learning-approach-to-estimating-transfer-entropy-in-neuroimaging-time-series)  
   标签：评分：8.0/10、query:pbci-load
   evidence：提出深度学习框架用于从EEG估计有向交互，可用于认知负荷分析
5. [EEG Benchmarking Needs a Task Specification Layer: NeuroDoc for Rulebook-Guided, Executable Benchmark Construction](/202606/24/2606.22925v1-eeg-benchmarking-needs-a-task-specification-layer-neurodoc-for-rulebook-guided-executable-benchmark-construction)  
   标签：评分：8.0/10、query:pbci-load
   evidence：脑电基础模型基准构建，用于多数据集评估
6. [OPM-FLUX: A Pipeline for OPM MEG Data Analysis](/202606/24/biorxiv-10-64898-2026-04-24-720604-v2-opm-flux-a-pipeline-for-opm-meg-data-analysis)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：OPM-FLUX流水线提供噪声抑制和伪迹处理，可直接迁移至脑电脑机接口

### 速读区论文标签
1. [Robust EEG Functional Connectivity Metrics for Decoding Action Observation Conditions and Observed Actions](/202606/24/2606.21055v1-robust-eeg-functional-connectivity-metrics-for-decoding-action-observation-conditions-and-observed-actions)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：基准测试了稳健的脑电功能连接指标用于解码
2. [Unifying Adaptive Fourier and Möbius-Based Models for Efficient and Interpretable Biomedical Signal Decomposition](/202606/24/2606.23713v1-unifying-adaptive-fourier-and-mbius-based-models-for-efficient-and-interpretable-biomedical-signal-decomposition)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：用于EEG信号增强的分解方法
3. [Generative Modeling for Physiological Signals](/202606/24/2606.23864v1-generative-modeling-for-physiological-signals)  
   标签：评分：7.0/10、query:pbci-load
   evidence：生理信号生成模型综述（含EEG），支持认知负荷数据增强
4. [Quantum machine learning for detection of sleep deprivation from EEG signals](/202606/24/biorxiv-10-64898-2026-06-14-732153-v1-quantum-machine-learning-for-detection-of-sleep-deprivation-from-eeg-signals)  
   标签：评分：7.0/10、query:pbci-load
   evidence：使用EEG和量子机器学习检测认知状态，与认知负荷评估相关
5. [MedTS-TTT: Test-Time Training for Medical Time Series Classification](/202606/24/2606.21329v1-medts-ttt-test-time-training-for-medical-time-series-classification)  
   标签：评分：6.0/10、query:pbci-load
   evidence：提出适用于EEG等医疗时间序列的测试时训练深度学习方法，可迁移至认知负荷评估
6. [Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling](/202606/24/biorxiv-10-64898-2026-06-11-724714-v1-design-of-a-low-latency-semg-real-time-correction-system-based-on-high-cmrr-and-emrms-mathematical-modeling)  
   标签：评分：6.0/10、query:robust-eeg
   evidence：sEMG干扰抑制方法可迁移至EEG去噪
7. [Data aggregation strategies for a P300 speller: decoding models, epoch averaging, cross-subject ensembles, and multi-channel models](/202606/24/biorxiv-10-64898-2026-06-17-732982-v1-data-aggregation-strategies-for-a-p300-speller-decoding-models-epoch-averaging-cross-subject-ensembles-and-multi-channel-models)  
   标签：评分：6.0/10、query:pbci-load
   evidence：P300拼写器EEG解码，使用深度学习模型，与被动脑机接口相关


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
