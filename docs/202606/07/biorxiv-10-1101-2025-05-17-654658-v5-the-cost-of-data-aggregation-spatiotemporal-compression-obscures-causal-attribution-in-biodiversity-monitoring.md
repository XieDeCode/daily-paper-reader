---
title: "The cost of data aggregation: spatiotemporal compression obscures causal attribution in biodiversity monitoring"
title_zh: 数据聚合的代价：时空压缩模糊了生物多样性监测中的因果归因
authors: "Malinowska, K., Wawrzynowicz, M., Markowska, K., Chodkiewicz, T., Butler, S., Kuczynski, L."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.1101/2025.05.17.654658v5.full.pdf"
tags: ["query:stm"]
score: 6.0
evidence: 时空压缩对因果归因的影响，基于生态模拟数据
tldr: 生物多样性监测中，数据聚合会模糊因果归因。通过模拟实验对比空间压缩(TS)、时间压缩(SDM)与全分辨率时空(FRST)模型，发现TS完全无法识别真实驱动因子(准确率0.50)，SDM中等(0.68)，而FRST表现最优(准确率0.88)。双惩罚收缩对TS有微弱提升但降低SDM/FRST特异度。结果表明，保留原生数据维度的全分辨率模型对可靠因果归因至关重要。
source: biorxiv
selection_source: fresh_fetch
motivation: 生态学常用聚合数据(时间序列或物种分布模型)分析种群变化，但聚合可能破坏协方差结构，模糊因果识别，需要量化这种“聚合代价”。
method: 通过虚拟物种模拟生成已知因果真相，采用虚拟生态学家方法模仿20年大规模鸟类监测，对比TS、SDM和全分辨率时空(FRST)三种分析管线的因果归因精度。
result: TS模型准确率0.50（灵敏度0），SDM准确率0.68，FRST准确率0.88（灵敏度0.84，特异度0.93）。双惩罚收缩对TS有微弱改善，但降低SDM/FRST特异度。
conclusion: 数据聚合会大幅降低因果推断能力，全分辨率且整合机制协方差结构的框架(如FRST)是实现可靠因果归因和生物多样性监测的必要条件。
---

## 摘要
保护决策需要准确识别种群变化的原因。生态学家通常依赖于聚合高维监测数据的分析方案。我们假设，压缩数据——无论是空间上的（如传统时间序列分析）还是时间上的（如静态物种分布模型）——都会破坏协方差结构，并模糊因果驱动因素的识别。为了量化这种“聚合代价”，我们使用虚拟物种进行了严格的模拟实验，以建立种群驱动因素的已知“基准真相”。然后，我们采用虚拟生态学家方法，模拟了一个为期20年的大规模鸟类监测计划，并生成了真实的时空数据集来评估分析流程。我们将聚合TS和SDM方案的因果归因准确性与全分辨率时空框架进行了基准测试，后者保留了原始数据维度并整合了机理性的时空协方差结构。我们的模拟揭示，空间压缩严重损害了因果推断：未受惩罚的TS模型未能检测到任何真正的潜在驱动因素（准确率=0.50，敏感性=0.00）。时间压缩（SDM）表现稍好（准确率=0.68），而FRST模型实现了优越的准确率（0.88）、敏感性（0.84）和特异性（0.93）。此外，我们识别出一个变量选择悖论：双重惩罚收缩略微改进了统计功效不足的TS模型，尽管它通过迫使虚假的相关变量吸收残差方差而降低了SDM和FRST框架的特异性。我们的研究结果表明，涉及数据聚合的方案会降低大规模监测数据集的信息价值。全分辨率、具有机理性信息的框架对于可靠的因果归因和稳健的生物多样性监测至关重要。

## Abstract
Conservation decision-making requires accurate identification of causes of population changes. Ecologists often rely on analytical protocols that aggregate high-dimensional monitoring data. We hypothesise that compressing data - either spatially, as in conventional time series (TS) analysis, or temporally, as in static species distribution models (SDMs) - destroys covariance structures and obscures the identification of causal drivers. To quantify this "aggregation cost", we conducted a rigorous simulation experiment using virtual species to establish a known "ground truth" of population drivers. We then employed a virtual ecologist approach to mimic a 20-year large-scale bird monitoring scheme, and generate realistic spatiotemporal datasets to evaluate the analytical pipelines. We benchmarked the causal attribution accuracy of aggregated TS and SDM protocols against a full-resolution spatiotemporal (FRST) framework, which retains native data dimensions and integrates mechanistic spatiotemporal covariance structures. Our simulations revealed that spatial compression severely compromises causal inference: unpenalised TS models failed to detect any true underlying drivers (accuracy = 0.50, sensitivity = 0.00). Temporal compression (SDMs) performer moderately better (accuracy = 0.68), while the FRST model achieved superior accuracy (0.88), sensitivity (0.84), and specificity (0.93). Furthermore, we identified a variable selection paradox: double penalty shrinkage marginally improved underpowered TS models, although it degraded the specificity of SDM and FRST frameworks by forcing spurious, correlated variables to absorb residual variance. Our findings demonstrate that protocols that involve data aggregation reduce the informational value of large-scale monitoring datasets. Full-resolution, mechanistically informed frameworks are essential for reliable causal attribution and robust biodiversity monitoring.