---
title: "Learning to See Like a Child: Why Viewpoint Diversity is Fundamental for Human-Aligned Object Recognition"
title_zh: 像孩子一样学习观察：为什么视角多样性对于与人类一致的物体识别至关重要
authors: "Luo, Y., Müller, N., Scholte, H. S."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.27.727784v2.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 物体识别中泛化到新视角，解决分布外问题
tldr: 深度卷积神经网络在标准识别任务上接近人类，但识别新颖视角物体时失败，而人类通过多样视觉经验获得视角不变性。本研究通过合成3D数据集系统控制视角，发现保持数据量不变时，视角多样性显著提升对未见视角的泛化。视角多样的训练迫使网络优先关注形状而非纹理，并保持以物体为中心的注意力，与人类识别策略一致。该工作揭示了视角多样性是实现鲁棒、类人视觉的关键因素。
source: biorxiv
selection_source: fresh_fetch
motivation: 当前模型缺乏人类幼年获得的视角多样性体验，导致对新颖视角泛化失败。
method: 使用合成3D数据集系统控制视角变量，在固定数据量下比较受限视角与多样视角的训练效果。
result: 视角多样训练牺牲了分布内准确性但大幅提升跨视角泛化，且网络转向形状偏好与物体中心注意力。
conclusion: 视角多样性是促进模型学习形状优先策略、实现人类对齐视觉的关键因素。
---

## 摘要
深度卷积神经网络在标准物体识别任务上达到了人类准确率，但无法从新视角识别熟悉的物体。然而，人类通过多样化的视觉体验在很小的时候就发展出了视角不变性的识别能力。这种视觉体验的差距可能解释了为什么模型在物体识别上与人类存在差异。在保持数据集大小不变的情况下，我们表明更大的视角多样性显著提高了对新视角的泛化能力。使用具有系统控制视角的合成3D数据集，我们揭示了一个核心权衡：限制视角的训练能快速学习并在分布内达到接近上限的准确率，但在未见过的视角上表现下降；而视角多样化的训练学习更慢但泛化稳健。增加视角多样性会破坏纹理规律性，同时保留全局形状，从而驱动网络优先考虑形状而非纹理——这与人类物体识别的基础策略相同。分区Grad-CAM分析进一步表明，视角多样化的模型保持以物体为中心的注意力。这些发现与多视角学习的发展理论相一致，并指出视角多样性是实现稳健、与人类一致的视觉的重要因素。

## Abstract
Deep convolutional neural networks match human accuracy on standard object recognition tasks but fail to recognize familiar objects from novel view-points. Humans, however, develop viewpoint-invariant recognition at an early age through diverse visual experience. This gap in visual experience may explain why models diverge from humans in object recognition. Holding dataset size constant, we show that greater viewpoint diversity substantially improves generalization to novel views. Using a synthetic 3D dataset with systematically controlled viewpoints, we reveal a core trade-off: restricted-view training yields rapid learning and near-ceiling in-distribution accuracy but collapses on held-out viewpoints, whereas viewpoint-diverse training learns more gradually yet generalizes robustly. Increasing viewpoint diversity disrupts texture regularities while preserving global shape, driving networks to prioritize shape over texture - the same strategy that underlies human object recognition. Partitioned Grad-CAM analyses further show that viewpoint-diverse models maintain object-centered attention. These findings parallel developmental accounts of multi-view learning and identify viewpoint diversity as an important factor for robust, human-aligned vision.