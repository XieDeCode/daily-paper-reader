---
title: Protocol-Guided Cross-Domain Transfer Learning for Bovine Facial Pain Recognition under Weak Dairy-Farm Labels
title_zh: 协议引导的跨域迁移学习：在弱奶牛场标签下进行牛面部疼痛识别
authors: "Patel, S., Neethirajan, S."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733162v1.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 跨域迁移学习用于家畜面部识别，处理领域偏移
tldr: 牲畜福利模型从受控实验部署到真实农场时，因品种、标签等差异导致可靠性下降。本文提出协议驱动迁移评估（PDTE）框架，将标签映射、目标设计等适应协议作为实验变量，用于牛肉到奶牛的疼痛识别迁移。实验发现直接迁移弱（AUC 0.418），目标设计主导性能，类平衡焦点适应实现稳定（AUC 0.667），但动物级不确定性大（CI 0.20-1.00）。结果表明迁移性需协议可控、不确定性感知评估。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有牲畜福利模型从受控实验迁移到实际农场时性能不可靠，需系统评估适应协议对迁移效果的影响。
method: 提出PDTE框架，将标签映射、目标设计、域对齐等协议作为变量，通过动物级外部验证与不确定性量化评估迁移。
result: 直接迁移弱（AUC 0.418），目标设计主导性能；类平衡焦点适应最优（AUC 0.667），但动物级不确定性大（CI 0.20-1.00）。
conclusion: 源域性能无法推断迁移性，弱标签下协议设计与操作点选择比预训练更重要，需不确定性感知评估。
---

## 摘要
畜牧福利模型在受控实验条件下开发，但部署到不同农场、品种、管理系统和标签体系时，其可靠性仍不确定。我们提出了协议驱动迁移评估（PDTE）框架，将适应协议（包括标签映射、目标设计、领域对齐、模型选择、校准和阈值策略）作为实验变量，并通过带有不确定性量化的个体水平外部验证来评估迁移效果。我们将PDTE应用于一项牛福利任务，涉及将面部疼痛表示从术后肉牛迁移到奶牛，同时面临品种、性别、生产系统、临床病因、记录环境和标签保真度的变化。使用作者收集的加拿大荷斯坦和娟姗牛数据集以及独立的8头牛测试队列，直接源域迁移效果较弱，序列AUC为0.418，个体水平AUC为0.400。PDTE识别了弱监督下的两种失败模式：阈值崩溃（适应收敛到单一预测类别）和校准诱导崩溃（得分排序保留但决策行为恶化）。在不同协议中，目标设计主导了性能。类别平衡的焦点适应实现了稳定的操作行为（序列AUC 0.611；个体水平AUC 0.667），而仅使用目标域模型在没有源初始化的情况下达到了相当的性能（序列AUC 0.596；配对p = 0.984），表明在弱标签条件下，协议设计和操作点选择比预训练更重要。个体水平的不确定性仍然很大，bootstrap 95%置信区间为0.20至1.00，超过了迁移效应。这些发现表明，迁移能力的限制不能仅从源域性能推断，需要在畜牧人工智能中进行协议控制和具有不确定性意识的评估。

## Abstract
Livestock welfare models are developed under controlled experimental conditions but deployed across farms, breeds, management systems and label regimes, where reliability remains uncertain. We introduce the Protocol-Driven Transfer Evaluation (PDTE) framework, which treats the adaptation protocol, comprising label mapping, objective design, domain alignment, model selection, calibration and threshold policy, as the experimental variable and evaluates transfer through animal-level external validation with uncertainty quantification. We apply PDTE to a bovine welfare task involving transfer of a facial pain representation from postoperative beef cattle to dairy cows under shifts in breed, sex, production system, clinical etiology, recording environment and label fidelity. Using an author-collected Canadian Holstein and Jersey dataset with an independent eight-cow test cohort, direct source-domain transfer was weak, with sequence AUC 0.418 and cow-level AUC 0.400. PDTE identified two failure modes under weak supervision: threshold collapse, in which adaptation converges to a single prediction class, and calibration-induced collapse, in which score ranking is preserved while decision behavior deteriorates. Across protocols, objective design dominated performance. Class-balanced focal adaptation achieved stable operating behavior (sequence AUC 0.611; cow-level AUC 0.667), while a target-only model attained comparable performance without source initialization (sequence AUC 0.596; paired p = 0.984), indicating that protocol design and operating-point choices contributed more than pretraining under weak-label conditions. Animal-level uncertainty remained substantial, with a bootstrap 95% confidence interval of 0.20 to 1.00, exceeding the transfer effect. These findings show that transferability limits cannot be inferred from source-domain performance alone and require protocol-controlled, uncertainty-aware evaluation in livestock AI.