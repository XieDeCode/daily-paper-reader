<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-08-11
- 运行时间：2026-08-11 21:26:48 UTC
- 运行状态：成功
- 本次总论文数：19
- 精读区：7
- 速读区：12

### 今日简报（AI）
今日共读19篇论文，精读7篇、速读12篇，重点关注遥感变化检测与城市多模态理解。最值得精读的是AdaDINO（10分）和Geo-Embed（9分），前者用冻结DINO实现高效遥感变化检测，后者推动城市统一多模态嵌入。建议普通读者优先从这两篇切入，再结合速读中的NDVI重建和VLM联邦学习扩展视野。
- 详情：[/202608/11/README](/202608/11/README)

### 精读区论文标签
1. [AdaDINO: Pair-Aware In-Backbone Adaptation of Frozen DINO for Efficient Remote Sensing Change Detection](/202608/11/2608.07982v1-adadino-pair-aware-in-backbone-adaptation-of-frozen-dino-for-efficient-remote-sensing-change-detection)  
   标签：评分：10.0/10、query:rs-fm
   evidence：将冻结的DINO视觉基础模型通过成对感知骨干内适应用于遥感变化检测
2. [Geo-Embed: Towards Unified Multimodal Embeddings for Urban Understanding](/202608/11/2608.03826v1-geo-embed-towards-unified-multimodal-embeddings-for-urban-understanding)  
   标签：评分：9.0/10、query:rs-fm
   evidence：面向城市理解的地理空间统一多模态嵌入与基准
3. [EvBS: Event-guided Blur Synthesis for Domain-adaptive Motion Deblurring](/202608/11/2608.08066v1-evbs-event-guided-blur-synthesis-for-domain-adaptive-motion-deblurring)  
   标签：评分：9.0/10、query:cross-domain
   evidence：直接面向预训练去模糊模型的域漂移问题，提出事件引导的模糊合成方法
4. [Test-Time Prototype Adaptation for Open-Vocabulary Semantic Segmentation](/202608/11/2608.08290v1-test-time-prototype-adaptation-for-open-vocabulary-semantic-segmentation)  
   标签：评分：9.0/10、query:cross-domain
   evidence：基于预训练CLIP的免训练测试时原型适配，用于开放词汇语义分割
5. [Domain-Aware Pruning: Sparsity and Domain Generalization via Regularized Probabilistic Masking](/202608/11/2608.08624v1-domain-aware-pruning-sparsity-and-domain-generalization-via-regularized-probabilistic-masking)  
   标签：评分：9.0/10、query:cross-domain
   evidence：直接面向域泛化和分布外鲁棒性，使用概率掩码实现稀疏性
6. [LASA: Language-and-Source-Anchored Alignment for Domain Generalized Semantic Segmentation](/202608/11/2608.08805v1-lasa-language-and-source-anchored-alignment-for-domain-generalized-semantic-segmentation)  
   标签：评分：9.0/10、query:cross-domain
   evidence：面向语义分割的领域泛化方法
7. [Distilled Roads: Generalisable Road Network Extraction Across Sensors, Resolutions, and Region](/202608/11/2608.03407v1-distilled-roads-generalisable-road-network-extraction-across-sensors-resolutions-and-region)  
   标签：评分：8.0/10、query:cross-domain
   evidence：面向路网提取的跨传感器与区域领域泛化

### 速读区论文标签
1. [Global-Scale Self-Supervised Spatiotemporal Learning for NDVI Time-Series Reconstruction](/202608/11/2608.02322v1-global-scale-self-supervised-spatiotemporal-learning-for-ndvi-time-series-reconstruction)  
   标签：评分：8.0/10、query:stm
   evidence：NDVI时间序列重建中的自监督时空学习
2. [On the Effectiveness of Adaptation Strategies for VLM-Based Federated Learning in Remote Sensing](/202608/11/2608.04791v1-on-the-effectiveness-of-adaptation-strategies-for-vlm-based-federated-learning-in-remote-sensing)  
   标签：评分：8.0/10、query:rs-fm
   evidence：遥感中基于视觉语言模型的联邦学习，并研究适配策略应对非独立同分布数据
3. [Summarize First, Download Later: Onboard VLMs for Bandwidth-Efficient Earth Observation](/202608/11/2608.06959v1-summarize-first-download-later-onboard-vlms-for-bandwidth-efficient-earth-observation)  
   标签：评分：8.0/10、query:rs-fm
   evidence：视觉语言模型用于地球观测；星上处理；带宽高效下行
4. [Understand Before Detect: Vision--Language Learning for Omni-Domain Infrared Small Target Detection](/202608/11/2608.07015v1-understand-before-detect-vision--language-learning-for-omni-domain-infrared-small-target-detection)  
   标签：评分：8.0/10、query:cross-domain
   evidence：通过视觉-语言理解解决红外小目标检测中的域偏移问题
5. [UniEvo-RS: Omni-Prompt Unified Remote Sensing Segmentation with Representative Exemplar-Driven Prototype Evolution](/202608/11/2608.03911v1-unievo-rs-omni-prompt-unified-remote-sensing-segmentation-with-representative-exemplar-driven-prototype-evolution)  
   标签：评分：7.0/10、query:rs-fm
   evidence：将提示驱动的视觉语言基础模型适配到统一遥感分割
6. [Design Choices That Matter: A Functional ANOVA Analysis for Remote Sensing Multi-Label Classification](/202608/11/2608.04702v1-design-choices-that-matter-a-functional-anova-analysis-for-remote-sensing-multi-label-classification)  
   标签：评分：7.0/10、query:rs-fm
   evidence：系统分析遥感多标签分类模型中的微调策略与初始化选择，关于遥感任务中预训练模型的使用。
7. [DARAD: Dual Adapters and Ranking-Aware Distillation for Continual Remote Sensing Image-Text Retrieval](/202608/11/2608.06059v1-darad-dual-adapters-and-ranking-aware-distillation-for-continual-remote-sensing-image-text-retrieval)  
   标签：评分：7.0/10、query:rs-fm
   evidence：面向遥感图文检索的连续学习与双适配器方法
8. [LoRSA: Toward Generalizable Parameter-Efficient Fine-Tuning for Biomedical Downstream Tasks](/202608/11/2608.07749v1-lorsa-toward-generalizable-parameter-efficient-fine-tuning-for-biomedical-downstream-tasks)  
   标签：评分：7.0/10、query:cross-domain
   evidence：面向不可见成像域泛化的参数高效微调方法
9. [Linear Multi-Timescale Retention as a Memory-Efficient Vision-Language Bridge](/202608/11/2608.01614v1-linear-multi-timescale-retention-as-a-memory-efficient-vision-language-bridge)  
   标签：评分：6.0/10、query:world-models
   evidence：面向视觉-语言模型的高效跨模态桥接
10. [HiResNets: Native Full-HD Video Recognition with Foveal Residual Streams](/202608/11/2608.02140v2-hiresnets-native-full-hd-video-recognition-with-foveal-residual-streams)  
   标签：评分：6.0/10、query:stm
   evidence：高分辨率视频识别架构中的时空建模，与时空模型主题相关
11. [Adapting Vision Foundation Models with Cascaded Semantics](/202608/11/2608.05393v1-adapting-vision-foundation-models-with-cascaded-semantics)  
   标签：评分：6.0/10、query:rs-fm
   evidence：面向预训练ViT的视觉提示调优，注入语义先验，是适应视觉基础模型的通用方法。
12. [RoRA: Role-Oriented Regional Allocation for Visual Token Pruning in MLLMs](/202608/11/2608.07088v1-rora-role-oriented-regional-allocation-for-visual-token-pruning-in-mllms)  
   标签：评分：6.0/10、query:world-models
   evidence：面向多模态大语言模型的视觉Token剪枝方法，与多模态基础模型效率相关


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
