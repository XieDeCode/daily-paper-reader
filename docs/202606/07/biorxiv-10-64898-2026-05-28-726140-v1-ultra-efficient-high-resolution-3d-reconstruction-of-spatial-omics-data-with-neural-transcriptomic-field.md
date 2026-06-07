---
title: Ultra-efficient High Resolution 3D Reconstruction of Spatial Omics Data with Neural Transcriptomic Field
title_zh: 基于神经转录组场超高效高分辨率三维重建空间组学数据
authors: "Gong, Y., Yuan, X., Gao, R., Chen, J., Yu, Z."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.726140v1.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 类似神经辐射场的隐式表示用于3D空间组学
tldr: "生物组织是三维生态系统，但空间组学数据多局限于二维切片，现有重建方法依赖局部插值，难以兼顾高保真、降噪和大规模效率。本研究提出神经转录组场（NTF），利用多分辨率哈希网格编码和隐式神经表示学习全局连续三维模型，从原理上分离生物信号与噪声。NTF实现千倍加速，15分钟内重建含1亿细胞的全鼠胚胎3D图谱，并能从10%切片生成超分辨率体积。该工作为构建下一代大规模三维组织图谱提供了超高效、可扩展的计算框架。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有3D重建方法依赖局部插值，难以兼顾保真度、降噪和大规模效率，需要全局建模方法。
method: NTF采用多分辨率哈希网格编码和隐式神经表示，学习全局连续三维转录组场，实现噪声解耦与高效重建。
result: "NTF比现有方法快1000倍，15分钟重建1亿细胞全鼠胚胎3D图谱，从10%切片即可超分辨率重建。"
conclusion: NTF为构建下一代大规模三维组织图谱提供了超快、可扩展、鲁棒的计算引擎。
---

## 摘要
生物组织本质上是三维（3D）生态系统，其中空间结构决定细胞功能。虽然空间组学技术彻底改变了分子图谱分析，但它们大多局限于孤立的二维（2D）组织切片。现有的尝试从稀疏切片重建3D体积的计算方法严重依赖于局部切片间插值，难以平衡高保真重建、降噪和图谱级效率。在这里，我们提出了神经转录组场（NTF），一种采用多分辨率哈希网格编码和隐式神经表示的深度学习框架。与仅仅连接相邻观测值的基于插值的方法不同，NTF学习组织的全局连续3D表示。通过建模潜在的潜在生物模式，NTF本质上将真正的分子信号与技术伪影分离，自然地实现稳健的降噪和高保真重建。这种全局场范式打破了传统的可扩展性限制：NTF相比现有方法实现了高达1000倍的加速，特别地，在不到15分钟内重建了一个包含1亿细胞规模的3D全小鼠胚胎图谱。此外，NTF可以从稀疏输入（例如仅使用10%的切片）生成超分辨体积，并稳健地外推到未见过的组织区域。我们展示了NTF在多种转录组和蛋白质组数据集上的多功能性，捕获果蝇和小鼠胚胎发生中的复杂时空动态，并绘制人乳腺癌中的瘤内功能梯度。最终，NTF为构建下一代全面的3D组织图谱提供了前所未有的快速、可扩展且稳健的计算引擎。

## Abstract
Biological tissues are inherently three-dimensional (3D) ecosystems where spatial architecture dictates cellular function. While spatial omics technologies have revolutionized molecular profiling, they are largely restricted to isolated two-dimensional (2D) tissue sections. Existing computational methods attempting to reconstruct 3D volumes from sparse slices rely heavily on local slice-to-slice interpolation, struggling to balance high-fidelity reconstruction, noise reduction, and atlas-scale efficiency. Here, we present Neural Transcriptomic Field (NTF), a deep learning framework employing multi-resolution hash-grid encoding and implicit neural representations. Unlike interpolation-based approaches that merely bridge adjacent observations, NTF learns a global, continuous 3D representation of the tissue. By modeling the underlying latent biological patterns, NTF intrinsically decouples true molecular signals from technical artifacts, naturally enabling robust denoising and high-fidelity reconstructions. This global field paradigm shatters traditional scalability limits: NTF achieves up to a 1,000x speedup over existing methods, notably reconstructing a 100-million-cell scale 3D whole-mouse embryo atlas in under 15 minutes. Furthermore, NTF can generate super-resolved volumes from sparse input (e.g., utilizing only 10% of slices) and robustly extrapolating into unseen tissue regions. We demonstrate NTFs versatility across diverse transcriptomic and proteomic datasets, capturing complex spatiotemporal dynamics in Drosophila and mouse embryogenesis, and mapping intra-tumoral functional gradients in human breast cancer. Ultimately, NTF provides an unprecedentedly fast, scalable, and robust computational engine for constructing the next generation of comprehensive 3D tissue atlases.