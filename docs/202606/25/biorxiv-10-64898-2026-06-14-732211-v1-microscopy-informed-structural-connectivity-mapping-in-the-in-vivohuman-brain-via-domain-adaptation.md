---
title: Microscopy-informed structural connectivity mapping in the in vivohuman brain via domain adaptation
title_zh: 基于域自适应的显微镜信息引导的人脑活体结构连接映射
authors: "Zhu, S., Dinsdale, N. K., Jbabdi, S., Miller, K., Howard, A."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732211v1.full.pdf"
tags: ["query:cross-domain"]
score: 7.0
evidence: 领域自适应方法应用于脑连接图谱
tldr: 表征人脑连接是神经科学挑战，多模态数据结合扩散MRI与显微镜提供独特联系但缺乏利用工具。提出深度模型预测显微镜指导的纤维取向，在猕猴数据训练后经域自适应迁移到人脑。方法从扩散MRI推导微结构纤维，无需推理时显微镜，支持有生物学意义的纤维追踪。建立了从显微镜到非侵入性成像的通用框架，实现生物信息指导的脑连接映射。
source: biorxiv
selection_source: fresh_fetch
motivation: 缺乏工具利用多模态显微镜-扩散MRI数据改进体内人脑连接估计。
method: 深度模型以显微镜导出的三维纤维取向图为目标，在猕猴数据训练，经域自适应迁移至人脑。
result: 显微镜指导的纤维取向分布增强浅层白质和皮层-皮下通路描绘。
conclusion: 建立了从显微镜迁移微结构信息的通用框架，支持体内人脑生物信息连接映射。
---

## 摘要
表征人脑连接仍然是神经科学的一个重大挑战。将扩散磁共振成像与同一大脑的高分辨率显微镜相结合的多模态数据集，为宏观成像与微观结构细节之间提供了独特的联系，但我们缺乏利用这些数据来改进活体人脑成像连接估计的工具。

我们提出了一种深度学习模型，该模型从扩散磁共振成像预测高分辨率显微镜信息引导的纤维方向。该模型使用显微镜导出的三维纤维方向图作为基于生物学的训练目标。它在一个定制的猕猴数据集上进行训练，该数据集整合了活体MRI、死后MRI和全脑显微镜，然后迁移到活体人脑成像。我们使用域自适应来从不同的MRI数据集中预测纤维方向：首先弥合猕猴组织状态的差异（死后到活体），然后跨物种泛化（猕猴到人类）。

我们的方法从扩散磁共振成像中推导出微观结构信息引导的纤维结构，而在推理时不需要显微镜。它利用了仅在动物模型中容易获取的数据，同时以最小的采集需求泛化到活体人脑扩散MRI。显微镜信息引导的纤维方向分布支持有生物学意义的纤维追踪，增强了活体人脑数据的浅层白质和皮质-皮质下通路描绘。更广泛地说，这项工作建立了一个通用框架，用于将微观结构信息从显微镜转移到非侵入性成像，从而实现生物信息引导的大脑连接映射。

## Abstract
Characterising human brain connectivity remains a major challenge in neuroscience. Multimodal datasets combining diffusion MRI with high-resolution microscopy in the same brain offer a unique link between macroscopic imaging and microstructural detail, but we lack tools to leverage these data to improve connectivity estimates for in vivo human imaging.

We present a deep learning model that predicts high-resolution microscopy-informed fibre orientations from diffusion MRI. The model uses microscopy-derived three-dimensional fibre orientation maps as biologically grounded training targets. It is trained on a bespoke macaque dataset integrating in vivo MRI, postmortem MRI, and whole-brain microscopy, and then translated to in vivo human imaging. We use domain adaptation to predict fibre orientations from diverse MRI datasets: first to bridge differences in tissue state in the macaque (postmortem to in vivo), and then to generalise across species (macaque to human).

Our method derives microscale-informed fibre architecture from diffusion MRI without requiring microscopy at inference. It leverages data that can easily be acquired only in animal models whilst generalising to in vivo human diffusion MRI with minimal acquisition requirements. The microscopy-informed fibre orientation distributions support biologically meaningful tractography, enhancing superficial white matter and cortical-subcortical pathway delineation for in vivo human data. More broadly, this work establishes a general framework for transferring microstructural information from microscopy to non-invasive imaging, enabling biologically informed mapping of brain connectivity.