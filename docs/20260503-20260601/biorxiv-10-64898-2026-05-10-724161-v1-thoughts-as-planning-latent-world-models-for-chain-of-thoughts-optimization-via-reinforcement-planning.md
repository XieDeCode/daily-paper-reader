---
title: "Thoughts-as-Planning: Latent World Models for Chain-of-Thoughts Optimization via Reinforcement Planning"
title_zh: 想法即规划：基于强化规划的思维链优化的潜在世界模型
authors: "Liu, D., Yu, Y., Wu, Y. N."
date: 2026-05-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.10.724161v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: 潜在世界模型用于推理链规划
tldr: 大型语言模型的推理链优化常依赖黑盒启发式或免梯度搜索，缺乏可解释性和样本效率。本文提出Thoughts-as-Planning框架，将推理链优化形式化为潜在语义空间中的序列决策过程，学习世界模型模拟编辑效果，并利用梯度下降或强化学习进行规划。实验表明该方法在效率、鲁棒性和泛化性上超越现有方法，同时通过结构化规划路径提供可解释性。该工作统一了多尺度编辑，提升了推理链优化的样本效率。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有推理链优化方法依赖黑盒启发式或免梯度搜索，缺乏可解释性和样本效率。
method: 将推理链优化视为潜在语义空间中的序列决策，学习世界模型模拟编辑效果，并利用梯度下降或强化学习规划。
result: 在语言理解和生成任务上，该方法在效率、鲁棒性和泛化性上超越当前最优的推理链调优方法。
conclusion: 该框架通过结构化规划路径实现可解释推理链优化，并支持从token到指令的多尺度统一编辑，具有良好的通用性。
---

## 摘要
大型语言模型在各种自然语言处理任务中的成功，使得推理链优化成为将模型行为与任务目标对齐的关键步骤。现有的推理链调优方法通常依赖黑盒启发式或无梯度搜索，缺乏可解释性、泛化能力和样本效率。在这项工作中，我们引入了“想法即规划”这一新颖框架，将推理链优化形式化为在潜在语义空间上的顺序决策过程。我们将大型语言模型建模为部分可观测环境，并学习一个潜在世界模型，模拟推理链编辑对下游输出的影响。构建了一个保持邻近性的嵌入空间来编码推理链-响应动态，从而通过梯度下降或强化学习实现规划。我们的方法支持多尺度抽象，将词元、片段和指令级别的推理链编辑集成到统一规划器中。通过在语言理解和生成任务上的大量实验，我们证明“想法即规划”在效率、鲁棒性和泛化能力上优于最先进的推理链调优基线，同时通过其结构化规划轨迹提供可解释性。我们的代码可在 https://github.com/FastLM/Thoughts-as-Planning 获取。

## Abstract
The success of large language models (LLMs) across diverse NLP tasks has elevated the importance of reasoning chain optimization as a critical step in aligning model behavior with task objectives. Existing reasoning chain tuning methods often rely on black-box heuristics or gradient-free search, which lack interpretability, generalization, and sample efficiency. In this work, we introduce Thoughts-as-Planning, a novel framework that formalizes reasoning chain optimization as a sequential decision-making process over a latent semantic space. We model the LLM as a partially observable environment and learn a latent world model that simulates the effect of reasoning chain edits on downstream outputs. A proximity-preserving embedding space is constructed to encode reasoning chain-response dynamics, enabling planning via gradient descent or reinforcement learning. Our method supports multi-scale abstraction, allowing reasoning chain edits at token, segment, and instruction levels to be integrated into a unified planner. Through extensive experiments on language understanding and generation tasks, we demonstrate that Thoughts-as-Planning outperforms state-of-the-art reasoning chain tuning baselines in efficiency, robustness, and generalization, while offering interpretability through its structured planning trajectory. Our code is available at https://github.com/FastLM/Thoughts-as-Planning.