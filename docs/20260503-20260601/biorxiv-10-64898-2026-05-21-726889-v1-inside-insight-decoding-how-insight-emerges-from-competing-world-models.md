---
title: "Inside insight: decoding how insight emerges from competing world models"
title_zh: 内在洞察：解码洞察如何在竞争的世界模型中涌现
authors: "Inutsuka, K., Nishioka, T., Macpherson, T., Fujiwara, M., Hikida, T., Naoki, H."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.21.726889v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: 从行为数据解码竞争世界模型中顿悟的出现
tldr: 洞察力源于世界模型的重构，但难以直接观测。本文提出内省洞察动力学（IID）框架，从小鼠行为数据中解码潜在世界模型动态，揭示洞察出现的时间点与竞争信念演变。在困难任务中，新模型需先被识别才可学习（门控学习）；在简单任务中，候选模型被并行学习。IID为量化洞察动态提供了新方法。
source: biorxiv
selection_source: fresh_fetch
motivation: 洞察力作为世界模型重构的涌现现象，缺乏可观测的解析手段，需从行为数据反演内在认知动态。
method: 开发IID机器学习框架，估计小鼠在两类任务中竞争世界模型的动态，解码洞察式转变的时序与奖励信念。
result: 困难任务支持门控学习（新模型先识别后学习），简单任务支持并行学习（多模型同步表征）。
conclusion: IID有效量化洞察动态，揭示不同复杂度任务中世界模型重构的差异性学习机制。
---

## 摘要
洞察何时以及如何涌现？我们将洞察概念化为一种由重构世界模型——一种将行动与结果联系起来的内部解释——而产生的突然领悟。然而，即使通过口头报告，这一过程也难以触及。在此，我们发展了内在洞察动力学（IID），一个从行为数据中估计潜在世界模型动力学的机器学习框架。我们分析了来自两个难度不同的任务的鼠标数据，这些任务要求动物从初始世界模型转向新模型。IID 解码了类似洞察转换的时间点以及在竞争的世界模型内不断演化的奖励信念。我们研究了这些转换是如何通过学习获得的。我们发现，较难的任务更好地由门控学习解释，其中只有在新模型被识别后才变得可学习，而较简单的任务则倾向于并行学习，其中候选模型事先被学习。因此，IID 为量化潜在洞察动力学开辟了一条途径。

## Abstract
When and how does insight emerge? We conceptualize insight as a sudden realization arising from restructuring a world model--an internal interpretation linking actions to outcomes. However, this process remains inaccessible even with verbal report. Here we developed inside insight dynamics (IID), a machine-learning framework estimating latent world-model dynamics from behavioral data. We analyzed mouse data from two tasks differing in difficulty and requiring animals to shift from an initial world model to a new one. IID decoded timing of insight-like shifts and evolving reward beliefs within competing world models. We examined how these shifts were acquired through learning. We found that the harder task was better explained by gated learning, in which a new model becomes learnable only after being recognized, whereas the simpler task favored parallel learning, in which candidate models are learned in advance. Thus, IID opens a route to quantifying latent insight dynamics.