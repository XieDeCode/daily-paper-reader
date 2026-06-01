---
title: "STEM-LM: Spatio-Temporal Ecological Modeling via Masked Language Model for Joint Species Distribution"
title_zh: STEM-LM：基于掩码语言模型的时空生态建模用于联合物种分布
authors: "Li, J. K., Lim, W., Callahan, F. M., Raskin, L. Y., Lemmon-Kishi, M., Nielsen, R."
date: 2026-05-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.13.724718v1.full.pdf"
tags: ["query:world-models"]
score: 9.0
evidence: 用于时空物种分布建模的Transformer
tldr: 联合物种分布模型（JSDM）对生物多样性预测至关重要，但现有方法难以处理大规模时空数据。本文提出STEM-LM，将每个物种的存在/缺失视为token，站点物种组合及协变量视为句子，通过掩码语言建模（MLM）学习共现结构。在北美蝴蝶和全球植物数据集上，STEM-LM在判别排名上优于或持平现有方法，且产生更准确的概率校准。利用部分观测物种可显著提升预测性能，展示了MLM在生态建模中的潜力。
source: biorxiv
selection_source: fresh_fetch
motivation: 大规模生态数据需要灵活可扩展的联合物种分布模型，现有方法在时空动态和条件推断上存在局限。
method: 将物种存在/缺失作为token，站点信息作为句子，用Transformer进行掩码语言建模，通过可变掩码率支持条件预测。
result: 在北美蝴蝶和全球植物数据集上，STEM-LM的判别排名优于或持平基线，概率校准更准确，部分观测可提升性能。
conclusion: 掩码语言建模为联合物种分布提供统一框架，兼具灵活性与可扩展性，可用于生态预测与推理。
---

## 摘要
联合物种分布模型（JSDMs）是生物多样性预测和保护决策的核心。随着生态数据在规模、维度和时空分辨率上的增长，需要针对大规模物种观测数据设计灵活且可扩展的JSDMs。文本和基因组学中掩码语言建模的最新进展提供了一种自然替代方案：通过将每个物种的存在或缺失视为一个标记，将地点的物种组合及其时空和生态协变量视为一个句子，我们可以通过从邻近地点重建被掩码的物种来学习联合共现结构。我们提出了STEM-LM，一种基于Transformer的JSDM，它将联合物种分布建模视为掩码语言建模。通过在训练过程中改变掩码率，单个训练好的模型既支持纯时空/生态预测，也支持在给定地点对任意观测到的物种子集进行条件化，以进行联合共现推断。在一个北美蝴蝶数据集和一个全球植物分布数据集上，STEM-LM在判别排序方面优于或等同于其他统计和基于深度学习的方法，同时产生了显著更好的校准出现概率。利用同一地点的部分物种观测大大提升了预测性能。

## Abstract
Joint species distribution models (JSDMs) are central to biodiversity forecasting and conservation decision-making. As ecological datasets grow in size, dimensionality, and spatio-temporal resolution, there is a need for flexible yet scalable JSDMs tailored to large-scale species observation data. Recent advances in masked language modeling for text and genomics suggest a natural alternative: by treating each species presence or absence as a token, and a sites species assemblage together with its spatio-temporal and ecological covariates as a sentence, we can learn joint co-occurrence structure by reconstructing masked species from their neighboring sites. We propose STEM-LM1, a Transformer-based JSDM that frames joint species distribution modeling as masked language modeling. By varying the masking rate during training, a single trained model supports both purely spatiotemporal/ecological prediction and conditioning on arbitrary subsets of observed species for joint co-occurrence inference at a given site. On a North American butterfly and a global plant distribution dataset, STEM-LM performs better or on par with other statistical and deep-learning based methods in terms of discriminative ranking, while producing substantially better rank-calibrated occurrence probabilities. Utilizing partial species observations at the same site greatly enhances prediction performance.