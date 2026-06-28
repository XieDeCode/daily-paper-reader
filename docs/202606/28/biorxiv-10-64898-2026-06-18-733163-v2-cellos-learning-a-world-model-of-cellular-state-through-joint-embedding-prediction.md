---
title: "CellOS: Learning a World Model of Cellular State through Joint Embedding Prediction"
title_zh: CellOS：通过联合嵌入预测学习细胞状态的世界模型
authors: "Zhou, Q., Le, Y., Qi, X., Chang, S., Lu, H., Wu, Y., Wang, H., Ran, R., li, x."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733163v2.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 通过联合嵌入预测学习细胞状态的世界模型
tldr: 现有单细胞基础模型多基于单一基因表达视图，通过重构或下词预测优化，无法整合互补的细胞状态视图。CellOS提出了多视图学习框架，结合因果细胞句子语言建模、保留功能的密集到混合专家扩展以及基于LLM-JEPA的潜在空间对齐三阶段训练，在3.905亿单细胞转录组上训练了120亿参数模型。在细胞状态注释、批次整合和扰动响应预测等基准上，CellOS持续超越现有最先进模型，展现了互补视图预测对齐对构建表征中心细胞世界模型的可扩展路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有单细胞基础模型仅从单一表达视图学习，无法显式整合互补的细胞状态视图。
method: CellOS通过三阶段训练：因果细胞句子语言建模、功能保持的密集到混合专家扩展、LLM-JEPA潜在空间对齐，整合表达与感知视图。
result: 在120亿参数模型上，CellOS在细胞注释、批次整合和扰动预测基准上均优于现有最先进模型。
conclusion: 互补细胞视图的预测对齐为可扩展的表征中心细胞世界模型和可迁移AI虚拟细胞提供了路径。
---

## 摘要
基于单细胞转录组学习的基石模型对于实现能够表征、查询和预测细胞状态的AI虚拟细胞至关重要。然而，目前大多数单细胞基石模型仅从单一视图的基因表达中学习，并主要通过重建或下一个token预测进行优化。因此，它们捕捉了表达丰度，但无法显式整合细胞状态的互补视图。在此，我们提出CellOS，一个多视图基石模型，从配对表达和感知视图中学习细胞表征。CellOS通过可扩展的三阶段训练策略整合互补视图，该策略结合了因果细胞句子语言建模、功能保持的密集到混合专家扩展以及通过LLM-JEPA目标的潜在空间对齐。利用这一框架，我们在3.905亿个单细胞转录组上训练了一个120亿参数的模型。在涵盖细胞状态注释、批次整合和扰动响应预测的多个基准测试中，CellOS始终优于最先进的单细胞基石模型。这些结果共同表明，互补细胞视图之间的预测对齐为以表征为中心的细胞世界模型和可迁移的AI虚拟细胞提供了一条可扩展的路径。

## Abstract
Foundation models learned from single-cell transcriptomes are central to the prospect of AI virtual cell that can represent, query and predict cellular state. However, most current single-cell foundation models learn from a single view of gene expression and are optimized primarily through reconstruction or next-token prediction. As a result, they capture expression abundance but cannot explicitly reconcile complementary views of cellular state. Here we present CellOS, a multi-view foundation model that learns cellular representations from paired expression and perception views. CellOS integrates complementary views through a scalable three-stage training strategy that combines causal cell-sentence language modelling, function-preserving dense-to-mixture-of-experts expansion and latent-space alignment via an LLM-JEPA objective. Using this framework, we trained a 12-billion-parameter model on 390.5 million single-cell transcriptomes. Across diverse benchmarks spanning cell-state annotation, batch integration and perturbation-response prediction, CellOS consistently outperformed state-of-the-art single-cell foundation models. Together, these results suggest that predictive alignment between complementary cellular views provides a scalable path toward representation-centric cellular world models and transferable AI virtual cells.