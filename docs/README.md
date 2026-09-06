<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-09-06
- 运行时间：2026-09-06 22:11:31 UTC
- 运行状态：成功
- 本次总论文数：14
- 精读区：6
- 速读区：8

### 今日简报（AI）
今日14篇脑机接口与可穿戴研究速览，聚焦EEG解码与姿态反馈两大热点。

最值得精读：EEG基础模型在运动想象跨域/跨受试者鲁棒性研究（9.0分），以及ErgoAssist认知感知姿势反馈系统（9.0分）。

下一步可重点关注EEG-VID预训练方法、Socrates学习交互对比，以及RobustSeiz癫痫检测鲁棒性基准的开源成果。
- 详情：[/202609/06/README](/202609/06/README)

### 精读区论文标签
1. [Lightweight Adaptation of EEG Foundation Models for Stroke Motor Imagery Decoding: Domain Shift and Subject-Level Robustness](/202609/06/2609.00282v1-lightweight-adaptation-of-eeg-foundation-models-for-stroke-motor-imagery-decoding-domain-shift-and-subject-level-robustness)  
   标签：评分：9.0/10、query:pbci-load
   evidence：利用LoRA适配EEG基础模型实现鲁棒的运动想象解码
2. [ErgoAssist: Cognition-Aware Posture Feedback in Wearable Ergonomic Systems](/202609/06/2609.00440v1-ergoassist-cognition-aware-posture-feedback-in-wearable-ergonomic-systems)  
   标签：评分：9.0/10、query:pbci-load
   evidence：用消费级脑电头带估计任务诱发认知负荷，直接对应脑电认知负荷估计
3. [EEG-AS: Instance-Level Foundation Model Selection for EEG Foundation Models via Behavior Reconstruction](/202609/06/2609.00653v1-eeg-as-instance-level-foundation-model-selection-for-eeg-foundation-models-via-behavior-reconstruction)  
   标签：评分：9.0/10、query:pbci-load
   evidence：提出面向EEG基础模型的实例级选择框架
4. [Augmenting Human Performance with an XR Agent Learning from Online Behavior and BCI Evidence](/202609/06/2608.30369v1-augmenting-human-performance-with-an-xr-agent-learning-from-online-behavior-and-bci-evidence)  
   标签：评分：8.0/10、query:pbci-load
   evidence：一种被动脑机接口系统，将被动脑电与行为证据在线融合以自适应XR辅助智能体。
5. [EEG-VID: Task-Guided Latent Predictive Pretraining for EEG Decoding and Assistive Target Selection](/202609/06/2609.00566v2-eeg-vid-task-guided-latent-predictive-pretraining-for-eeg-decoding-and-assistive-target-selection)  
   标签：评分：8.0/10、query:pbci-load
   evidence：面向EEG解码的任务引导潜在预测预训练，契合EEG基础模型处理需求
6. [A Dry-Contact Ear-EEG System With Continuous Electrode-Skin Impedance Mismatch Monitoring for Motion Artifact Cancellation Using DRL Stimulus](/202609/06/2609.02777v1-a-dry-contact-ear-eeg-system-with-continuous-electrode-skin-impedance-mismatch-monitoring-for-motion-artifact-cancellation-using-drl-stimulus)  
   标签：评分：8.0/10、query:robust-eeg
   evidence：一种基于DRL刺激连续监测电极-皮肤阻抗失配的EEG运动伪影在线消除技术，符合脑电解噪需求。

### 速读区论文标签
1. [EEG-VID: Task-Guided Latent Predictive Pretraining for EEG Decoding and Assistive Target Selection](/202609/06/2609.00566v1-eeg-vid-task-guided-latent-predictive-pretraining-for-eeg-decoding-and-assistive-target-selection)  
   标签：评分：7.0/10、query:pbci-load
   evidence：面向脑电解码的任务引导潜在预测预训练，类似脑电基础模型的预训练范式，可迁移用于BCI认知负荷等任务
2. [Socrates went Nuclear: Comparing Interaction Strategies for AI systems in a Learning Context using Brain Sensing](/202609/06/2609.00584v1-socrates-went-nuclear-comparing-interaction-strategies-for-ai-systems-in-a-learning-context-using-brain-sensing)  
   标签：评分：7.0/10、query:pbci-load
   evidence：利用脑信号推断认知投入并实时调节AI辅导难度，属于被动BCI负荷与投入评估的应用
3. [RobustSeiz: An Open-Source Framework for Benchmarking the Robustness of EEG Seizure Detection Models](/202609/06/2609.04007v1-robustseiz-an-open-source-framework-for-benchmarking-the-robustness-of-eeg-seizure-detection-models)  
   标签：评分：7.0/10、query:robust-eeg
   evidence：面向EEG模型的鲁棒性开源基准框架，涵盖伪迹、噪声与对抗扰动评估
4. [Frequency Selective Neural Networks as a Foundation Architecture for Time Series Learning](/202609/06/2608.29012v1-frequency-selective-neural-networks-as-a-foundation-architecture-for-time-series-learning)  
   标签：评分：6.0/10、query:pbci-load
   evidence：频率选择的时间序列基础架构，可能迁移至脑电频谱建模与认知负荷任务。
5. [MEL: Coordinate-Preserving EEG Tokenization for fMRI Translation](/202609/06/2608.29304v1-mel-coordinate-preserving-eeg-tokenization-for-fmri-translation)  
   标签：评分：6.0/10、query:pbci-load
   evidence：面向fMRI转换的保坐标脑电标记化框架，可服务于脑电信号处理建模
6. [TSPFN: A Temporal Tabular Foundation Model for Physiological Time Series Classification](/202609/06/2608.31013v1-tspfn-a-temporal-tabular-foundation-model-for-physiological-time-series-classification)  
   标签：评分：6.0/10、query:pbci-load
   evidence：面向生理时间序列的时间基础模型，其时间与通道建模可迁移到EEG信号处理
7. [Decoding Decision Correctness from EEG Under High Cognitive Workload in Virtual Reality: Implications for Collaborative Brain-Computer Interface Teams](/202609/06/2609.02436v1-decoding-decision-correctness-from-eeg-under-high-cognitive-workload-in-virtual-reality-implications-for-collaborative-brain-computer-interface-teams)  
   标签：评分：6.0/10、query:pbci-load
   evidence：高认知负荷VR场景下的EEG协作BCI研究，与被动BCI操作者状态解码相关
8. [Detecting Interbrain Synchronization in EEG Hyperscanning with MUSE-S EEG headban](/202609/06/2609.03404v1-detecting-interbrain-synchronization-in-eeg-hyperscanning-with-muse-s-eeg-headban)  
   标签：评分：6.0/10、query:pbci-load
   evidence：用CNN对脑电放松与游戏状态进行分类，深度学习解码方法可服务于被动脑机接口状态监测


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
