---
title: "The cost of data aggregation: spatiotemporal compression obscures causal attribution in biodiversity monitoring"
title_zh: 数据聚合的成本：时空压缩掩盖了生物多样性监测中的因果归因
authors: "Malinowska, K., Wawrzynowicz, M., Markowska, K., Chodkiewicz, T., Butler, S., Kuczynski, L."
date: 2026-05-18
pdf: "https://www.biorxiv.org/content/10.1101/2025.05.17.654658v4.full.pdf"
tags: ["query:stm"]
score: 8.0
evidence: 时空压缩对生物多样性监测中因果归因的影响
tldr: 生物多样性监测中常通过数据压缩（空间或时间聚合）简化分析，但此举可能掩盖真实因果驱动。本研究通过虚拟物种模拟和虚拟生态学家方法，对比传统时间序列、静态物种分布模型与全分辨率时空框架的因果归因准确性。结果显示：全分辨率框架准确率达0.88，灵敏度0.84，显著优于时间序列（准确率0.50，灵敏度0）和物种分布模型（准确率0.68）；且变量选择方法会引入假阳性。研究强调，数据聚合降低信息价值，应优先采用保留原始维度的机制性框架以实现可靠因果归因。
source: biorxiv
selection_source: fresh_fetch
motivation: 数据聚合（空间或时间压缩）可能破坏协方差结构，导致因果驱动识别错误，需量化这种代价。
method: 基于虚拟物种和虚拟生态学家方法，模拟20年大尺度鸟类监测数据，比较TS、SDM与全分辨率FRST框架的因果归因准确率。
result: FRST准确率0.88、灵敏度0.84、特异度0.93；TS几乎无效（准确率0.50，灵敏度0）；SDM中等（准确率0.68）；双惩罚变量选择对TS有微弱改善但降低FRST特异性。
conclusion: 数据聚合显著削弱因果推断能力，全分辨率机制性框架对生物多样性监测的可靠决策至关重要。
---

## 摘要
保护决策需要准确识别种群变化的原因。生态学家通常依赖于聚合高维监测数据的分析方案。我们假设数据压缩——无论是空间上的（如传统时间序列分析TS）还是时间上的（如静态物种分布模型SDMs）——会破坏协方差结构并掩盖因果驱动因素的识别。为了量化这种聚合成本，我们使用虚拟物种进行了严格的模拟实验，以建立已知的种群驱动真相。然后，我们采用虚拟生态学家方法模拟了一个为期20年的大规模鸟类监测计划，并生成了真实的时空数据集来评估分析流程。我们将聚合的TS和SDM协议的因果归因准确性与保留原始数据维度并整合机械时空协方差结构的全分辨率时空（FRST）框架进行了基准比较。我们的模拟表明，空间压缩严重损害了因果推断：未惩罚的TS模型未能检测到任何真正的潜在驱动因素（准确率=0.50，灵敏度=0.00）。时间压缩（SDMs）表现稍好（准确率=0.68），而FRST模型实现了优异的准确率（0.88）、灵敏度（0.84）和特异度（0.93）。此外，我们发现了变量选择悖论：双重惩罚收缩略有改善低效的TS模型，但通过迫使虚假的相关变量吸收残差方差，降低了SDM和FRST框架的特异度。我们的研究结果表明，涉及数据聚合的方案降低了大规模监测数据集的信息价值。全分辨率的、机理知情的框架对于可靠的因果归因和稳健的生物多样性监测至关重要。

亮点：
- 时空数据聚合掩盖了生物多样性监测中的因果驱动因素。
- 时间序列模型中的空间压缩未能检测到真实的种群驱动因素。
- 全分辨率时空模型能准确识别真正的驱动因素。
- 自动变量选择在高分辨率模型中引入了假阳性。

## Abstract
Conservation decision-making requires accurate identification of causes of population changes. Ecologists often rely on analytical protocols that aggregate high-dimensional monitoring data. We hypothesise that compressing data - either spatially, as in conventional time series (TS) analysis, or temporally, as in static species distribution models (SDMs) - destroys covariance structures and obscures the identification of causal drivers. To quantify this  aggregation cost, we conducted a rigorous simulation experiment using virtual species to establish a known  ground truth of population drivers. We then employed a virtual ecologist approach to mimic a 20-year large-scale bird monitoring scheme, and generate realistic spatiotemporal datasets to evaluate the analytical pipelines. We benchmarked the causal attribution accuracy of aggregated TS and SDM protocols against a full-resolution spatiotemporal (FRST) framework, which retains native data dimensions and integrates mechanistic spatiotemporal covariance structures. Our simulations revealed that spatial compression severely compromises causal inference: unpenalised TS models failed to detect any true underlying drivers (accuracy = 0.50, sensitivity = 0.00). Temporal compression (SDMs) performed moderately better (accuracy = 0.68), while the FRST model achieved superior accuracy (0.88), sensitivity (0.84), and specificity (0.93). Furthermore, we identified a variable selection paradox: double penalty shrinkage marginally improved underpowered TS models, although it degraded the specificity of SDM and FRST frameworks by forcing spurious, correlated variables to absorb residual variance. Our findings demonstrate that protocols that involve data aggregation reduce the informational value of large-scale monitoring datasets. Full-resolution, mechanistically informed frameworks are essential for reliable causal attribution and robust biodiversity monitoring.

HighlightsO_LISpatiotemporal data aggregation obscures causal drivers in biodiversity monitoring.
C_LIO_LISpatial compression in time series models fails to detect true population drivers.
C_LIO_LIFull-resolution spatiotemporal models accurately identify true drivers.
C_LIO_LIAutomated variable selection introduces false positives in high-resolution models.
C_LI