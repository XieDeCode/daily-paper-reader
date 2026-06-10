<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-06-10
- 运行时间：2026-06-10 22:44:27 UTC
- 运行状态：成功
- 本次总论文数：19
- 精读区：7
- 速读区：12

### 今日简报（AI）
今日精读两篇高分论文《OSMGraphCLIP》与《NGram-MoSE》，分别聚焦OpenStreetMap全局位置表征和遥感超分辨率；速读覆盖异构基础模型对齐、视觉语言模型连续解码、树木实例分割。重点关注9分工作——OSMGraphCLIP擅用图结构学习位置特征，NGram-MoSE通过N-gram上下文提升遥感图像细节。建议优先阅读精读论文，后者可用于地图与遥感任务的实际场景优化。
- 详情：[/202606/10/README](/202606/10/README)

### 精读区论文标签
1. [OSMGraphCLIP: Learning Global Location Representations from OpenStreetMap Graphs](/202606/10/2606.08046v1-osmgraphclip-learning-global-location-representations-from-openstreetmap-graphs)  
   标签：评分：9.0/10、query:rs-fm
   evidence：基于OpenStreetMap图的地理空间基础模型
2. [NGram-MoSE: Efficient Remote Sensing Super-Resolution via N-Gram Context and Mixture-of-Experts](/202606/10/2606.08535v1-ngram-mose-efficient-remote-sensing-super-resolution-via-n-gram-context-and-mixture-of-experts)  
   标签：评分：9.0/10、query:rs-fm
   evidence：面向遥感超分辨率的轻量Transformer和混合专家模型，处理分布外鲁棒性
3. [Earth-OneVision: Extending Remote Sensing Multimodal Large Language Models to More Sensor Modalities and Tasks](/202606/10/2606.10819v1-earth-onevision-extending-remote-sensing-multimodal-large-language-models-to-more-sensor-modalities-and-tasks)  
   标签：评分：9.0/10、query:rs-fm
   evidence：遥感多模态基础模型
4. [HDST-GNN: Heterogeneous Dynamic Spatiotemporal Graph Neural Networks for Multi-Object Tracking in UAV Aerial Imagery](/202606/10/2606.05587v1-hdst-gnn-heterogeneous-dynamic-spatiotemporal-graph-neural-networks-for-multi-object-tracking-in-uav-aerial-imagery)  
   标签：评分：8.0/10、query:stm
   evidence：用于无人机航拍图像的异构动态时空图神经网络
5. [DOME: Learning Transferable Domain Variables from Sparse Supervision for Test-Time Adaptation](/202606/10/2606.07646v1-dome-learning-transferable-domain-variables-from-sparse-supervision-for-test-time-adaptation)  
   标签：评分：8.0/10、query:cross-domain
   evidence：使用域编码进行测试时自适应，处理分布偏移
6. [Active Source-free Domain Adaptation in Open-set Medical Image Segmentation via Decomposed Uncertainty and Prototype Discrepancy](/202606/10/2606.08749v1-active-source-free-domain-adaptation-in-open-set-medical-image-segmentation-via-decomposed-uncertainty-and-prototype-discrepancy)  
   标签：评分：8.0/10、query:cross-domain
   evidence：医学图像分割中的主动源域缺失域适应
7. [ZODS-RS -- Zero-training Oriented Detection & Segmentation for Remote Sensing](/202606/10/2606.10769v1-zods-rs----zero-training-oriented-detection--segmentation-for-remote-sensing)  
   标签：评分：8.0/10、query:rs-fm
   evidence：利用预训练模型进行遥感零训练检测与分割

### 速读区论文标签
1. [Geometry-Preserving Unsupervised Alignment for Heterogeneous Foundation Models](/202606/10/2606.04385v1-geometry-preserving-unsupervised-alignment-for-heterogeneous-foundation-models)  
   标签：评分：8.0/10、query:world-models
   evidence：异构基础模型对齐
2. [DRIFT: A Residual Flow Adapter for Decoding Continuous Outputs in Vision-Language Models](/202606/10/2606.05758v1-drift-a-residual-flow-adapter-for-decoding-continuous-outputs-in-vision-language-models)  
   标签：评分：7.0/10、query:world-models
   evidence：视觉语言模型的连续输出解码适配器，属于多模态基础模型
3. [SegmentAnyTreeV2: Scaling Transformer-Based Tree Instance Segmentation Across Sensors, Platforms, and Forests](/202606/10/2606.08206v1-segmentanytreev2-scaling-transformer-based-tree-instance-segmentation-across-sensors-platforms-and-forests)  
   标签：评分：7.0/10、query:rs-fm
   evidence：使用Point Transformer的遥感点云树实例分割
4. [SemDINO: A DINOv3-Driven Network for Cross-Temporal Semantic Alignment in Change Detection](/202606/10/2606.09772v1-semdino-a-dinov3-driven-network-for-cross-temporal-semantic-alignment-in-change-detection)  
   标签：评分：7.0/10、query:rs-fm
   evidence：利用DINOv3基础模型特征进行语义变化检测
5. [ABot-Earth 0.5: Generative 3D Earth Model](/202606/10/2606.09967v1-abot-earth-05-generative-3d-earth-model)  
   标签：评分：7.0/10、query:rs-fm
   evidence：基于卫星影像的生成式三维地球模型，采用3D高斯泼溅
6. [Spatially Selective Self-Training for Unsupervised Building Change Detection](/202606/10/2606.10775v1-spatially-selective-self-training-for-unsupervised-building-change-detection)  
   标签：评分：7.0/10、query:rs-fm
   evidence：利用基础模型响应的无监督建筑变化检测
7. [PRISM: Synergizing Vision Foundation Models via Self-organized Expert Specialization](/202606/10/2606.03444v1-prism-synergizing-vision-foundation-models-via-self-organized-expert-specialization)  
   标签：评分：6.0/10、query:rs-fm
   evidence：协同视觉基础模型，对遥感基础模型有参考价值
8. [Physics-Guided Deep Unfolding for Blind Cross-Sensor Spectral Super-Resolution via Learning the Spectral Transformation Function](/202606/10/2606.05759v1-physics-guided-deep-unfolding-for-blind-cross-sensor-spectral-super-resolution-via-learning-the-spectral-transformation-function)  
   标签：评分：6.0/10、query:rs-fm
   evidence：提出PGU-Net，一种物理引导的深度展开网络，用于遥感中的盲跨传感器光谱超分辨率。
9. [RPC-GS: Gaussian Splatting with native RPC Rendering for Satellite Imagery](/202606/10/2606.06690v1-rpc-gs-gaussian-splatting-with-native-rpc-rendering-for-satellite-imagery)  
   标签：评分：6.0/10、query:rs-fm
   evidence：提出基于本地RPC模型的卫星影像高斯泼溅，与地球观测相关
10. [RAPID: Layer-Wise Redundancy-Aware Pruning and Importance-Driven Token Merging for Efficient ViT](/202606/10/2606.08156v1-rapid-layer-wise-redundancy-aware-pruning-and-importance-driven-token-merging-for-efficient-vit)  
   标签：评分：6.0/10、query:rs-fm
   evidence：提出深度感知的ViT令牌缩减方法，与遥感视觉Transformer相关
11. [An Enhanced Geometric-Spectral Feature Learning Framework for Airborne Multispectral Point Cloud Classification](/202606/10/2606.09123v1-an-enhanced-geometric-spectral-feature-learning-framework-for-airborne-multispectral-point-cloud-classification)  
   标签：评分：6.0/10、query:rs-fm
   evidence：基于注意力的几何-光谱特征学习用于多光谱点云分类
12. [Vision-Language Guided Hyperspectral Object Tracking via Semantics Fusion and Contextual Template Updating](/202606/10/2606.09167v1-vision-language-guided-hyperspectral-object-tracking-via-semantics-fusion-and-contextual-template-updating)  
   标签：评分：6.0/10、query:rs-fm
   evidence：视觉语言引导的遥感高光谱目标跟踪


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
