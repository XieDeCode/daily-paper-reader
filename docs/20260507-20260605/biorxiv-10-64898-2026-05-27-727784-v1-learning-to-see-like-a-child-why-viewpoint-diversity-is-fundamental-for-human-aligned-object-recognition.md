---
title: "Learning to See Like a Child: Why Viewpoint Diversity is Fundamental for Human-Aligned Object Recognition"
title_zh: 像孩子一样学习看：为什么视角多样性对于与人类对齐的物体识别至关重要
authors: "Luo, Y., Müller, N., Scholte, H. S."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.27.727784v1.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 面向新视角的分布外泛化
tldr: 深度卷积网络虽在标准任务上精度与人类相当，但面对陌生视角时泛化能力显著不足，而人类通过婴幼儿期的多样化视觉经验即可发展出视角不变性。本研究采用合成3D数据集系统控制视角分布，发现增加训练视角多样性虽会降低学习速度，却能大幅提升对新视角的泛化能力，同时破坏纹理规律性并引导网络优先利用形状线索，这与人类识别策略一致。进一步通过Grad-CAM分析证实，多视角训练促使模型保持以对象为中心的注意力模式，从而在类人视觉对齐方面取得重要进展。
source: biorxiv
selection_source: fresh_fetch
motivation: 人类通过多视角经验获得视角不变性，而模型因缺乏此类数据导致泛化失败，需探究视角多样性对模型学习的影响。
method: 利用合成3D数据集系统控制观察视角，对比受限视角与多样视角训练在分类任务上的表现差异。
result: 多样视角训练提升新视角泛化性能，驱动模型从纹理偏好转向形状偏好，且维持物体中心注意力。
conclusion: 视角多样性是构建鲁棒且类人视觉系统的关键因素，为模型与人类对齐提供了新路径。
---

## 摘要
深度卷积神经网络在标准物体识别任务上达到了人类水平的准确度，但在识别新视角下的熟悉物体时却失败了。然而，人类在幼年时期通过多样化的视觉经验发展出视角不变的识别能力。这种视觉经验的差距可能解释了为何模型在物体识别上与人类存在差异。在保持数据集大小不变的情况下，我们表明更大的视角多样性显著提高了对新视角的泛化能力。通过使用系统控制视角的合成3D数据集，我们揭示了一个核心权衡：受限视角训练能快速学习并达到分布内准确度的天花板，但在留出视角上表现崩溃，而视角多样化训练则学习更缓慢但能稳健泛化。增加视角多样性破坏了纹理规律性，同时保留全局形状，驱使网络优先考虑形状而非纹理——这与人类物体识别所采用的策略相同。分区Grad-CAM分析进一步表明，视角多样化模型保持了以物体为中心的注意力。这些发现与多视角学习的发展性描述一致，并将视角多样性确定为稳健、与人类对齐视觉的重要因素。

## Abstract
Deep convolutional neural networks match human accuracy on standard object recognition tasks but fail to recognize familiar objects from novel view-points. Humans, however, develop viewpoint-invariant recognition at an early age through diverse visual experience. This gap in visual experience may explain why models diverge from humans in object recognition. Holding dataset size constant, we show that greater viewpoint diversity substantially improves generalization to novel views. Using a synthetic 3D dataset with systematically controlled viewpoints, we reveal a core trade-off: restricted-view training yields rapid learning and near-ceiling in-distribution accuracy but collapses on held-out viewpoints, whereas viewpoint-diverse training learns more gradually yet generalizes robustly. Increasing viewpoint diversity disrupts texture regularities while preserving global shape, driving networks to prioritize shape over texture - the same strategy that underlies human object recognition. Partitioned Grad-CAM analyses further show that viewpoint-diverse models maintain object-centered attention. These findings parallel developmental accounts of multi-view learning and identify viewpoint diversity as an important factor for robust, human-aligned vision.