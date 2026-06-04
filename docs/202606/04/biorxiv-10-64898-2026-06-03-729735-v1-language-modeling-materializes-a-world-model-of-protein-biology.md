---
title: Language Modeling Materializes a World Model of Protein Biology
title_zh: 语言模型具体实现蛋白质生物学的世界模型
authors: "Candido, S., Hayes, T., Derry, A., Rao, R., Lin, Z., Verkuil, R., Wu, B. Z., Lee, J. S., Bruguera, E. S., Keval, J. A., Kopylov, M., Pak, J. E., Wu, W., Thomas, N., Mataraso, S., Hsu, A., Trotman-Grant, A. C., Fatras, K., dos Santos Costa, A., Badkundri, R., Akin, H., Oktay, D., Deaton, J., Montabana, E., Sitwala, H., Yu, Y., Wiggert, M., Carlin, D. A., Goering, A. W., Blazejewski, T., Sandora, M., Hla, M., Jia, T. Z., Kloker, L. H., Sofroniew, N. J., Uehara, M., Pannu, J., Bachas, S., Liu, D. S., Sercu, T., Rives, A."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729735v1.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 语言建模实现了蛋白质生物学的世界模型
tldr: 蛋白质研究受限于实验方法。本文提出用语言模型学习蛋白质的通用表示，构建的结构预测模型在复合物预测基准上超越现有方法，并成功设计出纳摩尔级亲和力的蛋白。语言模型表示空间与蛋白质的还原论理解一致，由此构建了包含68亿序列和11亿结构的蛋白质生物学图谱，揭示了跨进化尺度的联系，展示了语言模型在蛋白质生物学中的强大能力。
source: biorxiv
selection_source: fresh_fetch
motivation: 实验方法难以全面表征蛋白质生物学，需要可扩展的数字化表示来加速虚拟实验研究。
method: 采用语言模型学习蛋白质的通用表示，基于此构建结构预测模型，并通过简单搜索进行蛋白质设计。
result: 模型在生物分子复合物预测中超越现有方法，成功设计出纳摩尔级亲和力的蛋白质，并生成了68亿序列和11亿结构的蛋白质组图谱。
conclusion: 语言模型能统一表示蛋白质生物学，从原子级设计到进化尺度图谱，为蛋白质研究提供强大基底。
---

## 摘要
蛋白质是生命的基础。其生物学的全部范围超出了我们在物理实验室中通过实验方法进行表征的能力。准确的数字表示可以通过虚拟实验加速蛋白质生物学的发现。我们提出语言模型来学习可以扩展到所有蛋白质生物学的统一和通用表示。基于这些表示，我们开发了一个结构预测模型，在生物分子复合物预测的各项基准测试中，其性能超过了现有方法，包括抗体与其靶点的相互作用。一个简单的搜索程序在发现具有纳摩尔级结合亲和力的微型蛋白和单链抗体方面取得了高实验成功率，这是治疗设计的关键模式。对语言模型表示空间中概念的研究揭示了一个系统性的组织，与通过经验科学建立的蛋白质还原论理解相一致。利用这种组织，我们生成了一个涵盖超过68亿序列和11亿预测结构的蛋白质生物学综合图谱，识别了已知和未知生物学之间的联系。整体而言，这表明语言模型是表示蛋白质生物学的强大基础，其运作尺度从原子水平的蛋白质相互作用预测与设计，到识别不同粒度和抽象层次的蛋白质特性，再到映射跨越数十亿年进化的蛋白质之间的联系。

## Abstract
Proteins are fundamental to life. The full extent of their biology is beyond our ability to characterize with experimental approaches in the physical laboratory. Accurate digital representations could accelerate the discovery of protein biology through virtual experiments. We propose language modeling to learn unified and general representations that can be scaled to all of protein biology. Building on these representations, we develop a structure prediction model that exceeds the performance of established methods for biomolecular complex prediction across benchmarks, including for the interactions of antibodies with their targets. A simple search procedure yields high experimental success rates for the discovery of proteins with nanomolar binding affinities for both miniproteins and single-chain antibodies, a modality critical for therapeutic design. Study of the concepts in the language model's representation space reveals a systematic organization aligned with the reductionist understanding of proteins developed through empirical science. Leveraging this organization, we generate a comprehensive map of protein biology encompassing over 6.8 billion sequences and 1.1 billion predicted structures, identifying connections across known and unknown biology. As a whole, this shows language modeling as a powerful substrate for representing the biology of proteins, operating across scales from the prediction and design of protein interactions at the atomic level, to identifying properties of proteins at different levels of granularity and abstraction, to the scale of mapping connections between proteins across billions of years of evolution.