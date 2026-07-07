---
title: Generalized cell phenotyping for spatial proteomics with language-informed vision models
title_zh: 基于语言感知视觉模型的广义细胞表型分析方法用于空间蛋白质组学
authors: "Wang, X., Dilip, R., Iqbal, A. R., Bussi, Y., Brown, C., Pradhan, E., Jain, Y., Yu, K., Li, S., Abt, M., Borner, K., Keren, L., Yue, Y., Barnowski, R., Van Valen, D. A."
date: 2026-07-06
pdf: "https://www.biorxiv.org/content/10.1101/2024.11.02.621624v4.full.pdf"
tags: ["query:cross-domain"]
score: 7.0
evidence: 使用语言信息视觉模型实现细胞表型的域泛化
tldr: 空间蛋白质组学中，不同平台和标记面板导致细胞表型分析难以泛化。本文提出DeepCell Types，利用带通道注意力的Transformer构建语言信息视觉模型，从异质数据学习语义理解。在扩展的Expanded TissueNet数据集上，模型在细胞类型预测上超越现有方法，标记物阳性预测与专家相当，且少量微调即可适应新数据。该工作为社区提供了通用、可持续改进的开源表型模型。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有细胞表型分析方法难以泛化到不同标记面板和平台，限制了空间蛋白质组学数据的整合与利用。
method: 提出DeepCell Types，采用带通道注意力的Transformer，利用语言信息理解标记面板语义，从多样化数据集学习。
result: 在细胞类型预测上超越现有方法，标记物阳性预测匹配专家，且通过少量微调即可适应新数据。
conclusion: 提供了一个通用、可持续改进的开源细胞表型模型，能够泛化到新标记面板并高效微调。
---

## 摘要
我们提出了DeepCell Types，一种新颖的细胞表型分析方法，用于空间蛋白质组学，解决了在不同平台收集的、具有不同标记物组合的多样化数据集中泛化能力的挑战。我们的方法利用带有通道注意力的Transformer构建语言感知视觉模型；该模型对底层标记物组合的语义理解使其能够从异质数据集中学习并适应。通过利用一个名为Expanded TissueNet的精选多样化数据集，该数据集包含涵盖文献和美国国立卫生研究院人类生物分子图谱计划（HuBMAP）联盟的细胞类型标签，我们的模型在各种细胞类型、组织和成像模式上展现出稳健的性能。全面的基准测试表明，我们的方法在细胞类型预测上优于现有方法，并且同一模型在预测标记物阳性方面与专门的专家模型竞争；它进一步匹配了手动专家门控，并通过适度的微调适应新数据，远超过基线从头训练的效果。这项工作为空间蛋白质组学界提供了一个单一的、可持续改进的表型分析模型，该模型能泛化到新的标记物组合，并在需要时能高效微调。我们将DeepCell Types和Expanded TissueNet作为开源资源发布。

## Abstract
We present DeepCell Types, a novel approach to cell phenotyping for spatial proteomics that addresses the challenge of generalization across diverse datasets with varying marker panels collected across different platforms. Our approach utilizes a transformer with channel-wise attention to create a language-informed vision model; this model's semantic understanding of the underlying marker panel enables it to learn from and adapt to heterogeneous datasets. Leveraging a curated, diverse dataset named Expanded TissueNet with cell type labels spanning the literature and the NIH Human BioMolecular Atlas Program (HuBMAP) consortium, our model demonstrates robust performance across various cell types, tissues, and imaging modalities. Comprehensive benchmarking shows that our method outperforms existing approaches on cell-type prediction and, from the same model, predicts marker positivity competitively with a dedicated specialist; it further matches manual expert gating and adapts to new data with modest fine-tuning, well past what baselines reach when trained from scratch. This work equips the spatial proteomics community with a single, continuously improvable phenotyping model that generalizes to new marker panels and can be fine-tuned efficiently when needed. We release both DeepCell Types and Expanded TissueNet as open-source resources.