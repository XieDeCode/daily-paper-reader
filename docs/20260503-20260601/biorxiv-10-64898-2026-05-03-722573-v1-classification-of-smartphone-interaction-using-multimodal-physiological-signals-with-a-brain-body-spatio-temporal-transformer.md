---
title: Classification of Smartphone Interaction Using Multimodal Physiological Signals with a Brain-Body Spatio-Temporal Transformer
title_zh: 使用多模态生理信号与脑-身体时空变换器的智能手机交互分类
authors: "Mishra, P., Kagathara, V., Gandhi, T. K."
date: 2026-05-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.03.722573v1.full.pdf"
tags: ["query:stm"]
score: 9.0
evidence: 使用多模态信号的脑体时空Transformer分类智能手机交互
tldr: "智能手机交互行为（如短视频、游戏）引发不同生理信号，但现有研究常将其视为整体。本文提出脑-体时空变换器（BB-STT），融合EEG、EDA、PPG和眼动追踪等多模态信号，实现交互分类。模型在区分智能手机与非智能手机活动上达83.51%准确率，三分类（短视频、游戏、基线）达74.13%。跨模态注意力是关键，提升三分类准确率16.74个百分点；眼动特征（注视深度）实现粗分类，而瞳孔和EEG共同贡献细粒度区分。研究证明多模态生理信号可用于自然情境下数字参与的客观实时评估。"
source: biorxiv
selection_source: fresh_fetch
motivation: 智能手机交互行为差异常被忽视，需细粒度分类以客观评估数字参与。
method: 提出BB-STT，利用Transformer架构融合EEG、EDA、PPG与眼动追踪的多模态时空特征。
result: "三分类准确率74.13%，跨模态注意力提升16.74%，眼动与EEG分层贡献识别精度。"
conclusion: 多模态生理信号可有效区分智能手机交互类型，支持自然场景下的实时评估应用。
---

## 摘要
不同的智能手机交互行为，如短视频滚动和手机游戏，会引发性质不同的认知和生理反应。然而，这种区别常常被将智能手机使用视为单一行为的方法所忽略。本文提出了脑-身体时空变换器（BB-STT），这是一个统一的深度学习框架，用于从多模态信号（包括脑电图、皮肤电活动、光电容积描记和眼动追踪）中对交互特异的生理特征进行分类。BB-STT在区分智能手机与非智能手机活动方面达到了83.51%的准确率，并在短视频、游戏和基线观看的三类分类中达到了74.13%的准确率。该模型表现出强大的泛化能力，留一被试（LOSO）性能也与五折交叉验证准确率相当。跨模态注意力作为关键组件，通过动态整合多模态信号将三类分类准确率提升了16.74个百分点。可解释性分析表明生理反应存在层级组织。眼动追踪特征，特别是注视深度，能够初步区分智能手机与非智能手机活动。相比之下，智能手机上被动视频观看与主动游戏之间的更精细区分依赖于双侧瞳孔扩张和中央脑电图特征的共同作用。这些结果共同证明了多模态生理信号在自然场景中对数字参与进行客观、实时评估的潜力。

## Abstract
Distinct smartphone interaction behaviors, like short-form video scrolling and mobile gaming, elicit qualitatively different cognitive and physiological responses. However, such distinctions is often overlooked by approaches that treat smart-phone use as a monolithic behavior. This paper presents Brain-Body Spatio-Temporal Transformer (BB-STT), a unified deep learning framework for classifying interaction-specific physiological signatures from multimodal signals, including EEG, EDA, PPG, and eye-tracking. BB-STT achieves 83.51% accuracy in distinguishing smartphone from non-smartphone activity and 74.13% accuracy in three-class classification of short-form video, gaming, and baseline viewing. The model demonstrates strong generalization with leave-one-subject-out (LOSO) performance that is also comparable to 5-fold cross-validation accuracy. Cross-modal attention emerges as the key component, improving three-class accuracy by 16.74 points through dynamic integration of multimodal signals. Interpretability analysis indicates a hierarchical organization of physiological responses. Eye-tracking features, particularly gaze depth, enable coarse separation between smartphone and non-smartphone activity. In contrast, finer discrimination between passive video viewing and active gaming on smartphones relies on the joint contribution of bilateral pupil dilation and central EEG features. Together, these results demonstrate the potential of multimodal physiological signals for objective, real-time assessment of digital engagement in naturalistic settings.