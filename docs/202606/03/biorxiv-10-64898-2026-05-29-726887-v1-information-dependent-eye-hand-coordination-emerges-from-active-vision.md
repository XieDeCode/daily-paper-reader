---
title: Information-dependent eye-hand coordination emerges from active vision
title_zh: 信息依赖的手眼协调源于主动视觉
authors: "Zhao, J., VERDEL, D., Tan, Y., Burdet, E."
date: 2026-06-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.29.726887v1.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 通过主动视觉构建用于手部运动规划的内部模型
tldr: 日常活动中人类依赖视觉信息规划手部运动，但缺乏统一计算原理解释连续任务中的眼动模式。本文提出双随机模型预测控制框架，通过最小化任务相关不确定性并构建内部模型，自然涌现出扫视-追踪模式。该模型准确预测实验中的眼手运动特征。研究为理解人类眼动连续调节提供原则框架，并拓展了机器人辅助与主动感知应用。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有研究缺乏统一计算原理来解释连续任务中眼手协调模式的涌现机制。
method: 提出双随机模型预测控制公式，眼动连续控制以最小化任务不确定性并构建内部模型。
result: 模型自然涌现扫视-追踪模式，准确预测了眼手运动的关键实验特征。
conclusion: 为理解人类眼动连续调节提供原则框架，并开辟机器人辅助与主动感知的新视角。
---

## 摘要
在日常活动中，人类依赖视觉信息来规划手部运动，因此通过眼睛注视提取任务相关信息成为运动控制的关键方面。行为研究揭示了典型的扫视-追踪模式，可能由共享神经回路控制，从而有效减少任务相关的不确定性。然而，目前仍缺乏一个统一的计算原理解释这些模式在阅读或驾驶等连续任务中的出现。本文提出了一种主动视觉的双随机模型预测控制公式，其中眼睛运动被持续控制以最小化任务相关不确定性，并构建用于手部运动规划的内部模型。通过操纵未来视觉信息的数量、密度和难度的实验，我们展示了眼睛运动模式如何适应信息上下文，同时保持不变的提取视野。扫视-追踪模式自然地从模型中产生，精确预测了实验中观察到的眼睛和手部运动特征。这些结果为理解人类眼睛运动的连续调节提供了原则性框架，并为机器人辅助和主动感知应用开辟了新视角。

## Abstract
In daily activities, humans rely on visual information to plan hand movements, making the extraction of task-relevant information through eye gaze a key aspect of motor control. Behavioral studies have revealed characteristic saccade-pursuit patterns, likely governed by shared neural circuits, which enable an efficient reduction of task-related uncertainty. However, a unifying computational principle explaining the emergence of these patterns in continuous tasks such as reading or driving is still lacking. Here we propose a dual stochastic model predictive control formulation of active vision, in which eye movements are continuously controlled to minimize task-relevant uncertainty and build an internal model used for hand movement planning. Through experiments manipulating the amount, density, and difficulty of future visual information, we show how eye movement patterns adapt to the information context while maintaining an invariant extraction horizon. A saccade-pursuit pattern naturally emerges from the model, which accurately predicts both eye and hand movement features observed in experiments. These results provide a principled framework for understanding the continuous regulation of human eye movements and open new perspectives for applications in robotic assistance and active perception.