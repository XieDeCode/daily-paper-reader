---
title: A Deep Learning Framework for Spatiotemporal Modeling of Visual Task fMRI
title_zh: 一种用于视觉任务fMRI时空建模的深度学习框架
authors: "Li, M., Chen, Y., Ning, C., Dang, X., Wu, D."
date: 2026-05-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.05.722117v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: STREAM框架用于fMRI时空建模
tldr: 传统任务fMRI分析仅关注局部激活，无法揭示信息流。提出STREAM深度学习框架，通过学习神经转移函数建模有效连接与全脑信息流。在1074名参与者的视觉类别处理任务中，STREAM准确重构激活图，发现传统激活区主要由传入信号驱动，默认模式网络实为传出调控中枢。结果表明大脑通过动态重构关键枢纽间的信号模式实现类别特异性通信。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统fMRI分析仅关注局部激活，缺乏揭示驱动信息流的机制。
method: 提出STREAM框架，学习任务fMRI的神经转移函数，建模有效连接与全脑信息流。
result: STREAM准确重构激活图，发现激活区由传入信号驱动，默认模式网络为传出调控中枢。
conclusion: 大脑通过动态重构关键枢纽间的信号模式实现类别特异性通信，揭示方向性信号机制。
---

## 摘要
表征认知任务期间分布式脑区的动态协调仍具挑战性，因为传统fMRI分析侧重于局部激活，而未揭示驱动这些激活的潜在信息流。在此，我们提出STREAM（有效连接分析模型的时空表征），这是一种深度学习框架，通过学习任务fMRI中的神经转移函数来表征有效连接和全脑信息流。将其应用于1074名参与者的视觉类别处理，STREAM准确重建了激活图，同时进一步揭示传统激活区域主要受传入信号驱动。此外，默认模式网络作为一个具有广泛传出影响的高层调节枢纽，挑战了其被动表征。另外，类别特异性通信源于关键枢纽间信号模式的动态重构，而非静态通路。这些发现建立了一种新的计算范式，揭示了驱动任务fMRI中局部动态的定向信号机制，阐明了大脑如何灵活重构功能架构以支持复杂认知。

## Abstract
Characterizing the dynamic coordination of distributed brain regions during cognitive tasks remains challenging, as traditional fMRI analysis focuses on localized activations without revealing the underlying information flow that drives them. Here, we propose STREAM (Spatiotemporal Representation for Effective connectivity Analysis Model), a deep-learning framework that learns neural transition functions in task-fMRI to characterize effective connectivity and whole-brain information flow. Applied to visual category processing in 1074 participants, STREAM accurately reconstructs activation maps while further revealing that traditional activation regions are primarily driven by incoming signals. Moreover, the Default Mode Network acts as a high-level regulatory hub with extensive outgoing influence, challenging its passive characterization. Additionally, category-specific communication emerges from dynamic reconfiguration of signaling patterns among key hubs rather than static pathways. These findings establish a novel computational paradigm that uncovers directional signaling mechanisms driving local dynamics in task-fMRI, revealing how the brain flexibly reconfigures functional architecture for complex cognition.