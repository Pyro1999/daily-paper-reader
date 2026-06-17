<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-05-19 ~ 2026-06-17
- 运行时间：2026-06-17 03:40:34 UTC
- 运行状态：成功
- 本次总论文数：17
- 精读区：6
- 速读区：11

### 今日简报（AI）
今日聚焦脑电信号处理，精读探讨去噪网络容量与基准饱和问题的论文，以及TMS诱发EEG的精确滤波方法。最值得关注：超紧凑网络已导致基准饱和，且度量与效用存在差距；EPICURUS方法可准确估计TMS诱发的局部EEG活动。建议普通读者优先关注网络容量与实际效用差距，或尝试结合时空特征的Transformer模型处理情感/视觉解码任务。
- 详情：[/20260519-20260617/README](/20260519-20260617/README)

### 精读区论文标签
1. [How Much Capacity Does EEG Denoising Need? Ultra-Compact Networks reveal Benchmark Saturation and Metric-Utility Gap](/20260519-20260617/2606.08594v1-how-much-capacity-does-eeg-denoising-need-ultra-compact-networks-reveal-benchmark-saturation-and-metric-utility-gap)  
   标签：评分：10.0/10、query:robust-eeg
   evidence：直接研究EEG去噪的容量需求和基准测试
2. [EPICURUS: E-field-based spatial filtering procedure for an accurate estimation of local EEG activity evoked by Transcranial Magnetic Stimulation](/20260519-20260617/biorxiv-10-1101-2025-02-16-638512-v2-epicurus-e-field-based-spatial-filtering-procedure-for-an-accurate-estimation-of-local-eeg-activity-evoked-by-transcranial-magnetic-stimulation)  
   标签：评分：9.0/10、query:robust-eeg
   evidence：利用电场模拟的TMS-EEG伪影去除空间滤波
3. [CARACAS, a novel automated tool for Cardiac Artifact Removal in Absence of CArdiac Signal](/20260519-20260617/biorxiv-10-1101-2025-09-02-673728-v2-caracas-a-novel-automated-tool-for-cardiac-artifact-removal-in-absence-of-cardiac-signal)  
   标签：评分：9.0/10、query:robust-eeg
   evidence：提出CARACAS工具，仅利用独立成分时间序列自动识别心电伪迹，无需同步ECG
4. [Beyond Phase Estimation: A Multidimensional Gating Framework for Robust Real-Time Closed-Loop Neural Stimulation](/20260519-20260617/biorxiv-10-64898-2026-05-26-727783-v1-beyond-phase-estimation-a-multidimensional-gating-framework-for-robust-real-time-closed-loop-neural-stimulation)  
   标签：评分：9.0/10、query:robust-eeg
   evidence：用于噪声脑电中鲁棒相位估计的多维门控框架
5. [STAMBRIDGE: Spectral-Temporal Amplitude-aware Mid-Feature Bridge for EEG Visual Decoding](/20260519-20260617/2605.23137v1-stambridge-spectral-temporal-amplitude-aware-mid-feature-bridge-for-eeg-visual-decoding)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：通过振幅感知调制增强脑电信号，减少伪影
6. [Channel-Oriented Design for EEG-to-Music Reconstruction](/20260519-20260617/2606.04040v1-channel-oriented-design-for-eeg-to-music-reconstruction)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：面向通道的设计在噪声环境下鲁棒脑电重建

### 速读区论文标签
1. [Transformer Based Model for Spatiotemporal Feature Learning in EEG Emotion Recognition](/20260519-20260617/2606.10718v1-transformer-based-model-for-spatiotemporal-feature-learning-in-eeg-emotion-recognition)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：在EEG-TransNet中使用小波去噪进行情绪识别
2. [SUP-MCRL: Subject-aware Unified Pseudo-feature Coded Multimodal Contrastive Representation Learning for EEG Visual Decoding](/20260519-20260617/2606.16615v1-sup-mcrl-subject-aware-unified-pseudo-feature-coded-multimodal-contrastive-representation-learning-for-eeg-visual-decoding)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：统一脑电增强器，使用多尺度空洞卷积实现鲁棒信号增强
3. [STAMBRIDGE: Spectral-Temporal Amplitude-aware Mid-Feature Bridge for EEG Visual Decoding](/20260519-20260617/2605.23137v2-stambridge-spectral-temporal-amplitude-aware-mid-feature-bridge-for-eeg-visual-decoding)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：STAMBRIDGE利用频谱时间幅度感知调制提取鲁棒EEG特征，增强视觉解码信号质量
4. [Benchmarking Positional Encoding Strategies for Transformer-Based EEG Foundation Models](/20260519-20260617/2605.29754v1-benchmarking-positional-encoding-strategies-for-transformer-based-eeg-foundation-models)  
   标签：评分：7.0/10、query:pbci-load
   evidence：对基于Transformer的脑电基础模型的位置编码策略进行基准测试
5. [A Sliced-Wasserstein Framework on Correlation Matrices for EEG Decoding](/20260519-20260617/2606.06104v1-a-sliced-wasserstein-framework-on-correlation-matrices-for-eeg-decoding)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：利用相关矩阵进行噪声不变的鲁棒脑电解码
6. [A User-Friendly Ear-EEG-Based Brain-Computer Interface Using Text Sequence Stimulation](/20260519-20260617/biorxiv-10-64898-2026-05-15-721815-v1-a-user-friendly-ear-eeg-based-brain-computer-interface-using-text-sequence-stimulation)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：耳部脑机接口使用文本序列刺激以改善低信噪比
7. [BandVQ: Band-Wise Vector-Quantized EEG Foundation Model](/20260519-20260617/2605.24921v1-bandvq-band-wise-vector-quantized-eeg-foundation-model)  
   标签：评分：6.0/10、query:pbci-load
   evidence：分带向量量化的EEG基础模型提供可迁移表征
8. [Robust Frequency-Calibrated Virtual EEG Channel Generation from Four Frontal Electrodes for Wearable EEG Augmentation](/20260519-20260617/2605.29263v1-robust-frequency-calibrated-virtual-eeg-channel-generation-from-four-frontal-electrodes-for-wearable-eeg-augmentation)  
   标签：评分：6.0/10、query:robust-eeg
   evidence：FAVC-Net从四个额叶电极生成虚拟通道，通过频率校准增强鲁棒性
9. [Robust Frequency-Calibrated Virtual EEG Channel Generation from Four Frontal Electrodes for Wearable EEG Augmentation](/20260519-20260617/2605.29263v2-robust-frequency-calibrated-virtual-eeg-channel-generation-from-four-frontal-electrodes-for-wearable-eeg-augmentation)  
   标签：评分：6.0/10、query:robust-eeg
   evidence：从稀疏额叶脑电生成鲁棒虚拟通道用于可穿戴增强
10. [A 1000-hour EEG-EMG-audio dataset of Japanese speech production](/20260519-20260617/2606.01264v1-a-1000-hour-eeg-emg-audio-dataset-of-japanese-speech-production)  
   标签：评分：6.0/10、query:robust-eeg
   evidence：大规模脑电数据集支持伪影建模和多模态信号处理
11. [Learning aligned EEG representations with subject-specific encoders](/20260519-20260617/2606.16462v1-learning-aligned-eeg-representations-with-subject-specific-encoders)  
   标签：评分：6.0/10、query:robust-eeg
   evidence：主体特定编码器实现鲁棒的跨被试脑电解码


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
