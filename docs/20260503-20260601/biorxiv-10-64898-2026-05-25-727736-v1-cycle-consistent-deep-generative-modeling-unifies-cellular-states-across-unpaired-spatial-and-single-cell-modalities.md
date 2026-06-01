---
title: Cycle-consistent deep generative modeling unifies cellular states across unpaired spatial and single-cell modalities
title_zh: 循环一致深度生成模型统一了未配对空间和单细胞模态下的细胞状态
authors: "Zhang, H., Quinn, J. F., Data Science TeamLab,, Tansey, W."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.727736v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: 用于空间和单细胞数据的多模态生成模型
tldr: 空间和单细胞技术提供互补但视角有限的细胞状态信息，整合面临未配对测量和特征空间不匹配等挑战。MultiTME采用空间正则化的循环一致深度生成模型，通过双向映射一致性学习共享潜在表示，无需配对数据。该框架在多个基准测试中优于现有方法，实现跨模态细胞分型、完善空间转录组面板并生成全转录组空间图谱。应用表明，MultiTME能揭示单一模态无法观察的肿瘤表型轴，并纠正平台偏差，促进跨数据集整合。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有空间和单细胞技术数据异质、未配对且特征空间不匹配，缺乏统一整合方法。
method: 采用空间正则化的循环一致深度生成模型，通过双向映射一致性学习共享潜在表示，无需配对数据或共享特征。
result: 在多个基准测试中优于现有方法，实现跨模态细胞分型、完善空间转录组面板并生成全转录组空间图谱，纠正平台偏差。
conclusion: MultiTME有效整合异质数据，揭示单一模态无法观察的生物学现象，促进跨数据集协调和泛癌研究。
---

## 摘要
当前的空间和单细胞技术捕获了细胞状态的互补但不完整的视图，其中转录组、蛋白质组和空间信息分布在不同的平台上。整合面临未配对测量、特征空间不匹配以及模态特异性偏差的挑战。我们提出了MultiTME，这是一个多模态框架，使用空间正则化、循环一致的深度生成模型整合异质的空间和单细胞数据。通过强制双向映射的一致性，MultiTME学习了一个共享的潜在表示，使得无需配对观测或共享特征即可实现模态之间的转换。在多个基准测试中，MultiTME优于现有方法，生成准确的跨模态细胞分型，改进空间转录组面板的补全，并转移全转录组信息以生成细胞分辨率下的空间解析图谱。应用于一个多模态结直肠癌数据集，我们证明了MultiTME整合揭示了一个在单一模态中无法直接观察到的空间上连续的增殖-侵袭肿瘤轴。在五个多模态空间数据集中，我们展示了MultiTME可以校正Xenium和CosMx之间的平台特异性偏差，从而促进跨数据集协调并支持泛癌空间研究。MultiTME的代码可在https://github.com/tansey-lab/multitme获取。

## Abstract
Current spatial and single-cell technologies capture complementary but incomplete views of cellular state, with transcriptomic, proteomic, and spatial information distributed across distinct platforms. Integration is challenged by unpaired measurements, mismatched feature spaces, and modality-specific biases. We present MultiTME, a multimodal framework that integrates heterogeneous spatial and single-cell data using a spatially-regularized, cycle-consistent deep generative model. By enforcing consistency of bidirectional mappings, MultiTME learns a shared latent representation that enables translation between modalities without requiring paired observations or shared features. Across benchmarks, MultiTME outperforms existing methods, produces accurate cross-modal cell typing, improves spatial transcriptomic panel completion, and transfers whole-transcriptome information to generate spatially resolved maps at cellular resolution. Applied to a multimodal colorectal cancer dataset, we demonstrate that MultiTME integration reveals a spatially coherent proliferative-invasive tumor axis not directly observable within single modalities. Across five multimodal spatial datasets, we show MultiTME can correct for platform-specific biases between Xenium and CosMx, thereby facilitating cross-dataset harmonization and enabling pan-cancer spatial studies. Code for MultiTME is available at https://github.com/tansey-lab/multitme.