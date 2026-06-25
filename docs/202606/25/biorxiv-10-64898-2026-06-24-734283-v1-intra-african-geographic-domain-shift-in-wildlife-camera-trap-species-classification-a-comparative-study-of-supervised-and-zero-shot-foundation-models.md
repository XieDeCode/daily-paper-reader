---
title: "Intra-African Geographic Domain Shift in Wildlife Camera Trap Species Classification: A Comparative Study of Supervised and Zero-Shot Foundation Models"
title_zh: 非洲内部野生动物相机陷阱物种分类中的地理域偏移：监督模型与零样本基础模型的比较研究
authors: "Nanduri, N., Ogundare, J., Anderson, G."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.734283v1.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 野生动物相机陷阱物种分类中的地理域偏移
tldr: 非洲内部地理域偏移对野生动物相机陷阱物种分类模型的影响尚不明确。本文使用三种架构（监督微调BEiTV2、基于检索的DINOv2+FAISS、零样本BioCLIP），在Serengeti训练后迁移至南部非洲三个测试集。实验表明零样本模型在域偏移下表现稳健，监督模型性能显著下降。该工作首次系统刻画了非洲内部域偏移，为跨区域部署提供了实用指导。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有模型在非洲不同区域间部署时性能未知，缺乏对非洲内部地理域偏移的系统评估。
method: 比较三种模型架构：监督微调BEiTV2、检索式DINOv2+FAISS、零样本BioCLIP，从东非Serengeti迁移至南部非洲Kgalagadi、Kruger及博茨瓦纳数据。
result: 零样本BioCLIP在跨域测试中表现最优，监督模型显著下降；数据尺度增大可部分缓解域偏移，但零样本模型优势稳定。
conclusion: 零样本基础模型对非洲内部地理域偏移更具鲁棒性，推荐在缺乏本地标注数据时优先采用此类方法。
---

## 摘要
相机陷阱网络（如Snapshot Safari）已在非洲生成了数百万张带有标签的野生动物图像，使得训练用于自动物种分类的深度学习模型成为可能。然而，将在一个非洲区域训练的模型部署到另一个区域的情况仍知之甚少。据我们所知，本研究首次系统评估了非洲大陆内部野生动物相机陷阱物种分类中的地理域偏移，使用了人工智能的机器学习子领域。我们使用了三种模型架构，每种架构以不同方式与Snapshot Serengeti交互：BEiTV2在Serengeti图像上进行微调作为监督基线；DINOv2与FAISS结合，将Serengeti图像用作检索索引而不进行任何权重更新；BioCLIP是一种真正的零样本基础模型，完全未接收Serengeti训练数据。然后，我们在两个南部非洲测试集（Snapshot Kgalagadi和Snapshot Kruger）以及从博茨瓦纳本地收集的野生动物照片上对这三个模型进行了评估。我们进行了八个实验，涵盖域内基线、跨数据集迁移、数据缩放、MegaDetector预处理、灰度与彩色图像条件以及逐物种迁移分析。这项工作首次对监督架构和零样本架构下的非洲内部域偏移进行了经验性刻画，并为需要在南部非洲不同生态系统中部署模型而无需收集新标签数据的保护人工智能从业者提供了实用指导。

## Abstract
Camera trap networks such as Snapshot Safari have generated millions of labelled wildlife images across Africa, enabling the training of deep learning models for automated species classification. However, deploying models trained in one African region to another remains poorly understood. To the best of our knowledge, this study presents the first systematic evaluation of geographic domain shift within the African continent for wildlife camera trap species classification, using the Machine Learning sub-field of Artificial Intelligence. We use three model architectures, each interacting with Snapshot Serengeti in a different way: BEiTV2is fine-tuned on Serengeti images as a supervised baseline; DINOv2 with FAISS uses Serengeti images as a retrieval index without any weight updates; and BioCLIP is a true zero-shot foundation model that receives no Serengeti training data at all. All three are then evaluated on two Southern African test sets, Snapshot Kgalagadi and Snapshot Kruger, as well as on locally collected wildlife photographs from Botswana. We conduct eight experiments covering in-domain baselines, cross-dataset transfer, data scaling, MegaDetector preprocessing, grayscale vs. colour image conditions, and per-species transfer analysis. This work provides the first empirical characterisation of intra-African domain shift across both supervised and zero-shot architectures, and offers practical guidance for conservation AI practitioners who need to deploy models across the diverse ecosystems of Southern Africa without collecting new labelled data.