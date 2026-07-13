---
title: Text guidance is powerful but prompt-sensitive for weakly-supervised leaf symptom segmentation
title_zh: 文本引导在弱监督叶片病斑分割中虽强大但对提示敏感
authors: "Dubois, R., Bousset, L., Jumel, S., Leclerc, M., Parisey, N., Joly, A."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737680v1.full.pdf"
tags: ["query:rs-fm"]
score: 6.0
evidence: 使用基础模型SAM3进行农业叶片分割，可应用于遥感图像分析
tldr: 植物病害症状分割通常需要昂贵的像素级标注。本文探索使用SAM3的文本引导作为弱监督替代方案，比较了三种伪掩码生成策略：基于CAM与SAM/SAM3精细化、零样本文本引导SAM3、以及结合弱空间线索与文本提示的混合方法。结果发现，纯文本引导可达0.46 IoU，但对提示表述敏感；混合策略提升鲁棒性至0.50 IoU，同时降低提示敏感性。文本引导是传统弱监督的有前景替代，混合方案更稳健。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1296, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 1638, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1422, \"height\": 493, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1491, \"height\": 640, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1235, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1430, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1162, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 684, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737680-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1431, \"height\": 651, \"label\": \"Table\"}]"
motivation: 降低植物病害症状分割对像素级标注的依赖，探索文本引导作为弱监督信号的有效性与鲁棒性。
method: 比较三种伪掩码策略：CAM+SAM/SAM3精细化、零样本文本引导SAM3、以及混合弱空间线索与文本提示；用伪掩码训练DeepLabV3。
result: 纯文本引导达0.46 IoU，公共数据集0.61 IoU；混合策略主数据集0.50 IoU，附加数据集0.58 IoU，降低提示敏感性。
conclusion: 文本引导是传统弱监督的有前景替代，混合方法提供更鲁棒的植物病害分割方案。
---

## 摘要
准确分割植物病害症状对于作物监测和表型分析至关重要，但这通常需要昂贵的像素级标注。弱监督语义分割（WSSS）通过使用图像级标签减轻了这一负担，但其性能取决于类激活图（CAM）等空间先验的质量。我们研究了使用Segment Anything Model 3（SAM3）进行文本引导分割是否可以作为替代的弱监督信号。比较了三种伪掩码生成策略：（i）用SAM或SAM3细化的CAM；（ii）零样本文本引导的SAM3；（iii）结合弱空间线索和文本提示的混合方法。生成的伪掩码用于训练DeepLabV3模型。纯文本引导在无空间监督的情况下达到了0.46 IoU，在公共数据集上达到了0.61 IoU，与常规WSSS相当或更优，尽管性能对文本提示的表述敏感。混合策略提高了鲁棒性，在主数据集上达到0.50 IoU，在额外数据集上达到0.58 IoU，同时降低了对提示的敏感性。总体而言，文本引导是传统弱监督的一种有前景的替代方案，而混合方法为植物病害分割提供了更鲁棒的解决方案。

## Abstract
Accurate segmentation of plant disease symptoms is essential for crop monitoring and phenotyping, yet it typically requires costly pixel-level annotations. Weakly supervised semantic segmentation (WSSS) alleviates this burden using image-level labels, but its performance depends on the quality of spatial priors such as class activation maps (CAMs). We investigate whether text-guided segmentation with the Segment Anything Model 3 (SAM3) can serve as an alternative weak supervision signal. Three pseudo-mask generation strategies are compared: (i) CAMs refined with SAM or SAM3, (ii) zero-shot text-guided SAM3, and (iii) a hybrid approach combining weak spatial cues with text prompts. The resulting pseudo-masks are used to train a DeepLabV3 model. Text guidance alone matches or outperforms conventional WSSS, achieving up to 0.46 IoU without spatial supervision and 0.61 IoU on a public dataset, although performance is sensitive to text prompt formulation. The hybrid strategy improves robustness, reaching 0.50 IoU on the primary dataset and 0.58 IoU on the additional dataset while reducing prompt sensitivity. Overall, text guidance is a promising alternative to conventional weak supervision, while hybrid approaches provide a more robust solution for plant disease segmentation.