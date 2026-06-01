---
title: Default Feature Representations of the Cognitive Map
title_zh: 认知地图的默认特征表示
authors: "Bazarjani, A., Piray, P."
date: 2026-05-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.11.724436v1.full.pdf"
tags: ["query:world-models"]
score: 9.0
evidence: 用于强化学习的预测认知地图
tldr: 针对环境变化时预测认知地图更新问题，现有方法依赖显式模型或完整采样学习。本文提出默认特征表示（DFR），将固定特征基与编码环境的算子组合，提供模型基闭式解和无模型TD学习规则。实验表明，DFR在重规划任务上优于后继表示基线，并能捕获网格细胞的局部重映射，为基于局部经验更新预测地图提供了采样驱动的解释。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有认知地图更新方法依赖显式模型或全状态采样，缺乏局部经验驱动的快速适应性。
method: 提出DFR，将固定特征基与编码当前环境的算子组合，提供模型基闭式解和无模型TD学习规则。
result: DFR在重规划任务上优于后继表示基线，且捕获网格细胞的局部重映射现象。
conclusion: DFR通过分离稳定特征基与快速适应算子，实现从局部采样更新预测地图，为认知地图稳定性提供新解释。
---

## 摘要
当环境发生变化时，更新预测性认知地图对于生物体和强化学习都是一个核心问题，然而现有方法要么依赖于显式的模型知识，要么从样本中学习完整的状态索引地图。我们提出了默认特征表示（DFR），这是一种预测性认知地图的特征化参数化方法，其中固定的特征基与一个编码当前环境的算子相结合。我们为该算子提供了两种形式：当环境之间的结构性变化已知时，基于模型的闭式解；以及一种无模型的时序差分学习规则，该规则从采样转换中恢复算子，并能够证明收敛到基于模型的解。无模型DFR仅从样本中重建受扰动的地图，实现了与基于模型解相当的计划性能，并在重新规划任务上显著优于后继表示基线。我们还展示了DFR能够捕捉在局部环境变化下观察到的网格细胞的局部重映射。通过将认知地图分解为稳定的特征基和快速适应的算子，DFR提供了一种基于样本的说明，解释预测地图如何从局部经验中更新，反映了内嗅皮层网格场在不同环境中的稳定性。

## Abstract
Updating a predictive cognitive map when the environment changes is a central problem for both biological agents and reinforcement learning, yet existing approaches either depend on explicit model knowledge or learn the full state-indexed map from samples. We propose Default Feature Representations (DFR), a featurized parameterization of predictive cognitive maps in which a fixed feature basis is composed with an operator that encodes the current environment. We provide two forms for the operator: a model-based closed form when the structural change between environments is known, and a model-free temporal-difference learning rule that recovers the operator from sampled transitions, with provable convergence to the model-based solution. The model-free DFR reconstructs the perturbed map from samples alone, achieves planning performance comparable to the model-based solution, and substantially outperforms successor-representation baselines on replanning tasks. We also show that DFR captures the local remapping of grid cells observed under local environmental change. By separating the cognitive map into a stable feature basis and a fast-adapting operator, DFR offers a sample-based account of how a predictive map can be updated from local experience, mirroring the stability of entorhinal grid fields across environments.