---
title: "Integrative Transfer Network: Deep Transfer Learning Across Populations and Prediction Targets"
title_zh: 整合迁移网络：跨人群和预测目标的深度迁移学习
authors: "Gao, Y., Cui, Y."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.12.731936v1.full.pdf"
tags: ["query:cross-domain"]
score: 7.0
evidence: 跨群体和预测目标的深度迁移学习
tldr: 大规模临床数据包含子群属性与多预测目标，现有方法常独立处理。提出集成迁移网络（ITN），联合利用子群与结果间的共享和特有信息。实验表明，ITN在时间事件和分类任务中，通过跨子群和结果的信息借用，一致提升子群预测性能。ITN为异质性数据集的学习提供了统一框架，子群特异性洞察至关重要。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法未能联合利用子群差异与多目标预测中的共享及特有信息，需统一框架提升子群特异性预测。
method: 提出深度神经网络ITN，同时学习跨子群和多个相关结果，捕捉共享与子群特有表示。
result: 在时间事件和分类任务中，ITN一致改善子群预测，优于单独建模方法。
conclusion: ITN作为统一框架，有效利用异质性数据集，提升子群预测精度。
---

## 摘要
大规模临床和生物医学数据集日益包含多样的亚组属性（如人口统计学或临床亚组）和多个预测目标。尽管各种机器学习方法可以处理亚组差异或多目标预测，但它们通常独立考虑这些方面而非联合考虑。为了更有效地捕捉这类复杂数据集中的共享和亚组特有信息，我们提出了整合迁移网络（ITN），这是一种深度神经网络，旨在同时跨亚组和多个相关结果利用数据。在广泛实验中，包括时间到事件和分类任务（其中人口统计学亚组和多个疾病终点普遍存在），ITN通过借用其他亚组和结果的强度，展示了亚组特定预测的一致改进。我们将ITN视为一个从异质性数据中学习的统一框架，其中亚组特定见解至关重要。

## Abstract
Large-scale clinical and biomedical datasets increasingly contain both diverse subgroup attributes (e.g., demographic or clinical subgroups) and multiple prediction targets. Although various machine learning approaches can address subgroup differences or multi-target prediction, they often consider these aspects independently rather than jointly. To more effectively capture the shared and subgroup-specific information in such complex datasets, we propose the Integrative Transfer Network (ITN), a deep neural network designed to leverage data across subgroups and multiple related outcomes simultaneously. In extensive experiments, including time-to-event and classification tasks where demographic subgroups and multiple disease end-points are prevalent, ITN demonstrates consistent improvements in subgroup-specific prediction by borrowing strength from other subgroups and outcomes. We envision ITN as a unified frame-work for learning from heterogeneous datasets where subgroup-specific insights are critical.