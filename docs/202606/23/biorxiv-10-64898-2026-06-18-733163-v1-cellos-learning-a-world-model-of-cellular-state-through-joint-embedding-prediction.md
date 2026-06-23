---
title: "CellOS: Learning a World Model of Cellular State through Joint Embedding Prediction"
title_zh: CellOS：通过联合嵌入预测学习细胞状态的世界模型
authors: "Zhou, Q., Le, Y., Qi, X., Chang, S., Lu, H., Wu, Y., Wang, H., Ran, R., li, x."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733163v1.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 学习细胞状态的世界模型
tldr: 单细胞基础模型大多只学习基因表达单一视图，无法整合互补的细胞状态信息。CellOS提出多视图基础模型，通过因果语言建模、密集到专家混合扩展和LLM-JEPA对齐的三阶段训练，从3.905亿转录组学习120亿参数模型。在细胞注释、批次整合和扰动预测上超越现有模型。该框架为构建表征中心的细胞世界模型和可迁移AI虚拟细胞提供了可扩展路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有单细胞基础模型仅从单一基因表达视图学习，无法整合互补的细胞状态信息，限制了虚拟细胞的能力。
method: CellOS采用三阶段训练：因果细胞句子语言建模、功能保持的密集到专家混合扩展、以及基于LLM-JEPA的潜在空间对齐，融合表达和感知多视图。
result: 120亿参数模型在细胞状态注释、批次整合和扰动响应预测基准上一致优于现有单细胞基础模型，同时保持鲁棒的批次整合。
conclusion: 多视图预测对齐为构建表征中心的细胞世界模型和可迁移AI虚拟细胞提供了可扩展路径。
---

## 摘要
从单细胞转录组学习的基础模型是AI虚拟细胞前景的核心，该虚拟细胞能够表示、查询和预测细胞状态。然而，当前大多数单细胞基础模型从单一视图的基因表达中学习，并主要通过重建或下一个令牌预测进行优化。因此，它们捕捉表达丰度，但无法明确协调细胞状态的互补视图。在这里，我们提出了CellOS，一个多视图基础模型，从配对的表达和感知视图中学习细胞表示。CellOS通过一个可扩展的三阶段训练策略整合互补视图，该策略结合了因果细胞句语言建模、保持功能的密集到混合专家扩展以及通过LLM-JEPA目标的潜在空间对齐。使用这一框架，我们在3.905亿个单细胞转录组上训练了一个120亿参数的模型。在涵盖细胞状态注释、批次整合和扰动响应预测的多样化基准测试中，CellOS在细胞状态注释和扰动响应预测方面始终优于最先进的单细胞基础模型，同时保持了稳健的批次整合。这些结果表明，互补细胞视图之间的预测对齐为以表示为中心的细胞世界模型和可迁移的AI虚拟细胞提供了一条可扩展的路径。

## Abstract
Foundation models learned from single-cell transcriptomes are central to the prospect of AI virtual cell that can represent, query and predict cellular state. However, most current single-cell foundation models learn from a single view of gene expression and are optimized primarily through reconstruction or next-token prediction. As a result, they capture expression abundance but can-not explicitly reconcile complementary views of cellular state. Here we present CellOS, a multi-view foundation model that learns cellular representations from paired expression and perception views. CellOS integrates complementary views through a scalable three-stage training strategy that combines causal cell-sentence language modelling, function-preserving dense-to-mixture-of-experts expansion and latent-space alignment via an LLM-JEPA objective. Using this framework, we trained a 12-billion-parameter model on 390.5 million single-cell transcriptomes. Across diverse benchmarks spanning cell-state annotation, batch integration and perturbation-response prediction, CellOS consistently outperformed state-of-the-art single-cell foundation models in cell-state annotation and perturbation-response prediction while preserving robust batch integration. Together, these results suggest that predictive alignment between complementary cellular views provides a scalable path toward representation-centric cellular world models and transferable AI virtual cells.