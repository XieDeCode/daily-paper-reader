---
title: Integrating Histology with Spatial Molecular Programs Using a Multimodal Foundation Model
title_zh: 利用多模态基础模型整合组织学与空间分子程序
authors: "Zhang, Z., Qin, B., Zhao, Y., Qi, Z., Xu, H., Wang, Y., Zheng, W., Dai, J., Chen, A., Wang, N., Nie, L., Zhang, P., Zhang, H., Xu, T., Lin, S., Ren, P., Xue, L., Xue, X., Yang, Z., Xu, J., Pan, D., Wang, C., Liu, Z., Meng, Y., Zeng, Z."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729028v1.full.pdf"
tags: ["query:world-models"]
score: 6.0
evidence: 多模态基础模型整合组织学与空间转录组学
tldr: 组织学评估是癌症诊断核心，但缺乏分子解释。SQUALL多模态基础模型整合组织学与空间分子程序，基于33种组织、12种平台共17.6亿配对点预训练。该模型能进行转录组范围虚拟生物标志物分析、发现与三级淋巴结构成熟和卵巢癌复发相关的预后生态位，并重建乳腺癌侵袭分子轨迹。在898例患者全切片图像中，SQUALL在预后预测上超越现有病理基础模型，实现了可解释的风险分层。研究建立了空间对齐多模态预训练新范式，将分子见解扩展到病理图像。
source: biorxiv
selection_source: fresh_fetch
motivation: 组织学评估缺乏分子背景，现有方法无法从病理图像中推断空间分子程序，需多模态整合以提升诊断和预后准确性。
method: SQUALL使用大规模配对组织学-空间转录组数据集histMol进行多模态预训练，学习对齐的图像与分子表示，支持后续任务。
result: SQUALL在虚拟生物标志物、预后空间生态位发现和疾病进展建模中表现优异，且在898例全切片图像预后预测上超越现有模型。
conclusion: 空间对齐的多模态预训练为从病理图像获取分子见解提供新范式，有望推动精准医学和可解释风险分层。
---

## 摘要
组织病理学评估仍是癌症诊断和分层的关键，但缺乏分子背景使其机制解释受限。为此，我们开发了SQUALL，一种整合组织学与空间分子程序的多模态基础模型。在预训练阶段，我们构建了histMol，一个包含来自33种组织、12个平台、3446张组织切片的17.6亿个配对组织学-空间转录组斑点/网格的大规模语料库。预训练后，SQUALL可实现全转录组虚拟生物标志物分析、预后相关空间生态位发现以及整合性疾病进展建模。利用其多模态嵌入，SQUALL识别出与三级淋巴结构（TLS）成熟和卵巢癌复发相关的生态位，重建了跨越325,112个斑点的乳腺癌侵袭分子轨迹，并揭示了潜在的转录程序。应用于898名患者的全切片图像时，SQUALL在结果预测方面优于现有病理学基础模型，同时实现了可解释的风险分层。这些结果共同确立了空间对齐的多模态预训练作为将分子见解扩展到病理图像的新范式。

## Abstract
Histopathological assessment remains central to cancer diagnosis and stratification, yet its mechanistic interpretation remains limited without molecular context. To address this, we developed SQUALL, a multimodal foundation model integrating histology with spatial molecular programs. For pretraining, we assembled histMol, a large-scale corpus of 1.76 billion paired histology-spatial transcriptomics spots/bins across 33 tissues and 12 platforms from 3,446 tissue sections. Following pretraining, SQUALL enables transcriptome-wide virtual biomarker profiling, prognostically relevant spatial niches discovery, and integrative disease progression modeling. Leveraging its multimodal embeddings, SQUALL identifies niches associated with tertiary lymphoid structure (TLS) maturation and ovarian cancer relapse, reconstructs molecular trajectories of breast cancer invasion across 325,112 spots, and uncovers underlying transcriptional programs. Applied to whole-slide images from 898 patients, SQUALL outperforms existing pathology foundation models in outcome prediction while enabling interpretable risk stratification. Together, these results establish spatially aligned multimodal pretraining as a new paradigm for extending molecular insights into pathology images.