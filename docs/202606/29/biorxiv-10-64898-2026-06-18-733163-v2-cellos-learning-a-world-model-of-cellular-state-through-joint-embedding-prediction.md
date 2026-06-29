---
title: "CellOS: Learning a World Model of Cellular State through Joint Embedding Prediction"
title_zh: CellOS：通过联合嵌入预测学习细胞状态的世界模型
authors: "Zhou, Q., Le, Y., Qi, X., Chang, S., Lu, H., Wu, Y., Wang, H., Ran, R., li, x."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733163v2.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 细胞状态世界模型基础模型
tldr: 现有单细胞基础模型主要从单一基因表达视图学习，无法整合互补的细胞状态视图。CellOS通过三阶段训练策略（因果语言建模、密集到混合专家扩展、LLM-JEPA潜在空间对齐），在3.905亿单细胞转录组上训练了120亿参数的多视图模型。在细胞状态注释、批次整合和扰动响应预测等任务上，CellOS全面超越现有模型。该工作表明，互补视图的预测性对齐为构建可表征、查询和预测细胞状态的AI虚拟细胞提供了可扩展路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有单细胞模型仅从单一基因表达视图学习，无法整合表达丰度与感知视图等互补信息，限制了细胞状态的全面表征。
method: 提出三阶段训练：因果细胞句子语言建模、功能保持的密集到混合专家扩展、以及基于LLM-JEPA目标的多视图潜在空间对齐。
result: 120亿参数模型在3.905亿单细胞转录组上训练，在细胞状态注释、批次整合和扰动预测等基准上均超越现有最佳模型。
conclusion: 预测性对齐互补细胞视图是构建可迁移AI虚拟细胞和以表征为中心的细胞世界模型的有效路径。
---

## 摘要
基于单细胞转录组学习的基础模型对于能够表示、查询和预测细胞状态的AI虚拟细胞至关重要。然而，当前大多数单细胞基础模型仅从基因表达单一视角学习，并通过重构或下一个标记预测进行优化。因此，它们捕捉了表达丰度，但无法明确调和细胞状态的互补视角。本文提出CellOS，一种多视角基础模型，从配对表达和感知视角学习细胞表征。CellOS通过可扩展的三阶段训练策略整合互补视角，该策略结合了因果细胞句子语言建模、保持功能的密集到混合专家扩展以及通过LLM-JEPA目标的潜在空间对齐。利用这一框架，我们在3.905亿个单细胞转录组上训练了一个120亿参数的模型。在涵盖细胞状态注释、批次整合和扰动响应预测的多样化基准测试中，CellOS始终优于最先进的单细胞基础模型。综合这些结果表明，互补细胞视角之间的预测对齐为以表征为中心的细胞世界模型和可迁移的AI虚拟细胞提供了一条可扩展的路径。

## Abstract
Foundation models learned from single-cell transcriptomes are central to the prospect of AI virtual cell that can represent, query and predict cellular state. However, most current single-cell foundation models learn from a single view of gene expression and are optimized primarily through reconstruction or next-token prediction. As a result, they capture expression abundance but cannot explicitly reconcile complementary views of cellular state. Here we present CellOS, a multi-view foundation model that learns cellular representations from paired expression and perception views. CellOS integrates complementary views through a scalable three-stage training strategy that combines causal cell-sentence language modelling, function-preserving dense-to-mixture-of-experts expansion and latent-space alignment via an LLM-JEPA objective. Using this framework, we trained a 12-billion-parameter model on 390.5 million single-cell transcriptomes. Across diverse benchmarks spanning cell-state annotation, batch integration and perturbation-response prediction, CellOS consistently outperformed state-of-the-art single-cell foundation models. Together, these results suggest that predictive alignment between complementary cellular views provides a scalable path toward representation-centric cellular world models and transferable AI virtual cells.