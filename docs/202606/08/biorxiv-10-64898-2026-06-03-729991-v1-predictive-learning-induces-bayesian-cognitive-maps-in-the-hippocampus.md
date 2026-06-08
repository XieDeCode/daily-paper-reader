---
title: Predictive learning induces Bayesian cognitive maps in the hippocampus
title_zh: 预测性学习在海马中诱导贝叶斯认知地图
authors: "Kim, Y., Kang, Y. H."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729991v1.full.pdf"
tags: ["query:world-models"]
score: 6.0
evidence: 海马体中的预测学习与时空表示
tldr: 导航中位置感知存在不确定性，但经典模型忽略感知噪声。本文引入贝叶斯理想观察者，发现其信念能更好解释位置细胞活动。训练递归神经网络预测下一感官输入时，网络学会类似贝叶斯信念的表征，并产生位置细胞样活动。结果表明海马通过预测性学习构建贝叶斯认知地图。
source: biorxiv
selection_source: fresh_fetch
motivation: 经典空间表征模型假设位置可直接观察，忽略了感知不确定性，无法解释位置细胞的特性。
method: 比较贝叶斯理想观察者与经典模型，训练递归神经网络预测下一自我中心输入，分析其内部表征。
result: 贝叶斯信念准确再现位置细胞宽度、面积和密度；预测网络产生类似活动，优于自编码器。
conclusion: 海马回路可能通过预测性感知学习构建贝叶斯认知地图，将感知整合到空间表征中。
---

## 摘要
导航需要感知：位置必须从有噪声和模糊的自我中心感官输入中推断，例如距离的视觉估计。然而，许多经典的空间表示模型隐含地假设异中心位置是直接可观测的，从而忽略了感知不确定性。在此，我们将这样的模型与一个明确包含感知推理的贝叶斯理想观察者进行比较。我们发现，贝叶斯观察者对位置的信念更准确地再现了位置细胞活动的关键属性，包括环境内和跨环境的位置野宽度、面积和密度。通过解析论证和数值模拟，我们表明，训练用于预测下一个自我中心感官输入的循环神经网络学习到类似于贝叶斯信念的表示，并在熟悉和不熟悉的环境中产生类似位置细胞的活动，优于训练用于重现当前输入的自编码器。综上所述，这些结果表明海马回路可能通过预测性感知学习从经验中构建贝叶斯认知地图。

## Abstract
Navigation requires perception: location must be inferred from noisy and ambiguous egocentric sensory inputs, as in visual estimation of distance. However, many classical models of spatial representation implicitly assume that allocentric location is directly observable, thereby neglecting perceptual uncertainty. Here, we compare such a model with a Bayesian ideal observer that explicitly incorporates perceptual inference. We find that the Bayesian observer's beliefs over location more accurately reproduce key properties of place cell activity, including place field width, area, and density, within and across environments. Using analytic arguments and numerical simulations, we show that recurrent neural networks trained to predict the next egocentric sensory input learn representations resembling Bayesian beliefs and yield place cell-like activity in both familiar and unfamiliar environments, outperforming autoencoders trained to reproduce the current input. Together, these results suggest that hippocampal circuits may construct Bayesian cognitive maps from experience through predictive perceptual learning.