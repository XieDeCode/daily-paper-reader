---
title: "SciCore-Omics: a tri-modal foundation model unifying histology, spatial transcriptomics and language for spatial biology"
title_zh: SciCore-Omics：一种统一组织学、空间转录组学和语言的三模态基础模型，用于空间生物学
authors: "Xiao, X., Li, Y., Zeng, Z., Yan, Y., Liu, Z., Xiang, Y., Ye, Z., Ying, J., Xie, L., He, F."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.30.728937v2.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 连接组织学、转录组学和语言的三模态基础模型
tldr: "现有基础模型通常仅成对连接组织学、组学或语言，难以联合推断分子状态和解析空间组织。本文提出SciCore-Omics，首个三模态基础模型，融合组织学图像、空间转录组学和生物语言。通过构建15万+空间配对图像-基因-文本数据集并进行三阶段渐进训练，模型在基因表达预测和空间域识别任务上相对最强基线提升23.6-80.9%；在零样本病理分类中平均准确率超越GPT-5达6.16个百分点；在10例乳腺癌案例的专家评估中验证了仅凭H&E切片的分子推理能力。该工作证明三模态框架可有效桥接形态与分子状态，为计算病理学提供更通用且可解释的基础模型。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基础模型仅成对连接组织学、组学或语言，难以联合推断分子状态和空间组织。
method: "构建151,182个空间配对图像-基因-文本样本，三阶段渐进训练三模态模型SciCore-Omics。"
result: "基因表达预测和空间域识别相对提升23.6-80.9%，零样本病理分类准确率超GPT-5 6.16个百分点。"
conclusion: 三模态框架有效桥接形态与分子状态，为计算病理学提供更通用可解释的基础模型。
---

## 摘要
组织形态学和空间转录组学捕捉了组织生物学的互补方面，但它们之间的关系在大规模上仍然难以提取、对齐和解释。现有的基础模型通常仅成对连接组织学、组学或语言，这限制了它们联合推断分子状态、解码空间组织结构和生成生物学解释的能力。在这里，我们展示了SciCore-Omics，这是第一个连接组织学图像、空间转录组学和生物语言的三模态基础模型。我们构建了一个空间配对的图像-基因-文本数据集，包含来自多个组织的151,182个点，并对SciCore-Omics进行了三阶段渐进式训练。在基因表达预测和空间域识别方面，与最强外部基线相比，SciCore-Omics在任务特定指标上实现了23.6-80.9%的相对提升。它还在组织病理学分类中展示了鲁棒的零样本泛化能力，在四个基准测试中的平均准确率上比GPT-5高出6.16个百分点。在10例乳腺癌病例的专家评估中，证实了其仅基于H&E的病例级分子推理能力。总之，我们的方法证明了三模态框架能够有效地桥接组织形态学和分子状态，为计算病理学和组学分析提供了更通用和可解释的基础模型。

## Abstract
Histomorphology and spatial transcriptomics capture complementary aspects of tissue biology, but their relationships remain difficult to extract, align, and interpret at scale. Existing foundation models typically connect histology, omics, or language only pairwise, which limits their capacity to jointly infer molecular states, decode spatial tissue organization, and generate biologically grounded explanations. Here, we show SciCore-Omics, the first tri-modal foundation model linking histology images, spatial transcriptomics, and biological language. We constructed a spatially paired image-gene-text dataset comprising 151,182 spots across multiple tissues and performed a three-stage progressive training of SciCore-Omics on this dataset. Across gene expression prediction and spatial domain recognition, SciCore-Omics achieved 23.6-80.9% relative gains in task-specific metrics over the strongest external baselines. It further showed robust zero-shot generalization in histopathology classification, outperforming GPT-5 by 6.16 percentage points in mean accuracy across four benchmarks. Expert evaluation in 10 breast cancer cases confirmed its H&E-only case-level molecular reasoning capability. Together, our method demonstrates that a tri-modal framework can effectively bridge histomorphology and molecular state, providing a more general and interpretable foundation model for computational pathology and omics analysis.