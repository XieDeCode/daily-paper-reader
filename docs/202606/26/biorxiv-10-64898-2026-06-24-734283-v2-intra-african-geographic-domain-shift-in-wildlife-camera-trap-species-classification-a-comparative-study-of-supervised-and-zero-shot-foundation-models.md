---
title: "Intra-African Geographic Domain Shift in Wildlife Camera Trap Species Classification: A Comparative Study of Supervised and Zero-Shot Foundation Models"
title_zh: 非洲野生动物相机陷阱物种分类中的地理域偏移：监督与零样本基础模型的比较研究
authors: "Nanduri, N., Ogundare, J., Anderson, G."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.734283v2.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 使用基础模型评估野生动物相机陷阱分类中的地理域转移
tldr: 非洲不同地区相机陷阱数据集存在地理分布偏移，影响物种分类模型泛化。本研究首次系统评估非洲内部域偏移，比较监督微调BEiTV2、检索式DINOv2+FAISS和零样本BioCLIP三种架构。在Serengeti训练后，于Kgalagadi、Kruger和Botswana测试集上开展八组实验。结果显示监督模型性能显著下降，而零样本和检索模型更具鲁棒性。工作为保护AI跨区域部署提供了首个实证指导和模型选择建议。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究非洲内部地理偏移对相机陷阱物种分类模型的影响，为跨区域部署提供解决方案。
method: 使用BEiTV2（监督微调）、DINOv2+FAISS（检索）和BioCLIP（零样本）三种架构，在Serengeti训练后在三个南非洲测试集评估。
result: 首次系统评估非洲内部域偏移，发现监督模型性能下降，零样本和检索模型在跨区域迁移中表现更稳定。
conclusion: 实践者应优先使用零样本或检索模型以降低对新标注数据的依赖，实现高效跨区域部署。
---

## 摘要
诸如Snapshot Safari等相机陷阱网络已在非洲生成了数百万张标记的野生动物图像，使得训练用于自动物种分类的深度学习模型成为可能。然而，将在非洲某一地区训练的模型部署到另一地区的效果仍知之甚少。据我们所知，本研究首次对非洲大陆内野生动物相机陷阱物种分类的地理域偏移进行了系统评估，利用了人工智能的机器学习子领域。我们使用了三种模型架构，每种都以不同方式与Snapshot Serengeti进行交互：BEiTV2在Serengeti图像上进行微调作为监督基线；DINOv2结合FAISS将Serengeti图像作为检索索引，不更新任何权重；BioCLIP是一个真正的零样本基础模型，完全没有接收Serengeti训练数据。随后，这三个模型在两个南部非洲测试集（Snapshot Kgalagadi和Snapshot Kruger）以及从博茨瓦纳本地收集的野生动物照片上进行了评估。我们进行了八项实验，涵盖了域内基线、跨数据集迁移、数据缩放、MegaDetector预处理、灰度与彩色图像条件以及逐物种迁移分析。这项工作首次对监督和零样本架构下的非洲内部域偏移进行了实证描述，并为需要在南部非洲多样化生态系统中部署模型而无需收集新标记数据的保护人工智能实践者提供了实用指导。

## Abstract
Camera trap networks such as Snapshot Safari have generated millions of labelled wildlife images across Africa, enabling the training of deep learning models for automated species classification. However, deploying models trained in one African region to another remains poorly understood. To the best of our knowledge, this study presents the first systematic evaluation of geographic domain shift within the African continent for wildlife camera trap species classification, using the Machine Learning sub-field of Artificial Intelligence. We use three model architectures, each interacting with Snapshot Serengeti in a different way: BEiTV2is fine-tuned on Serengeti images as a supervised baseline; DINOv2 with FAISS uses Serengeti images as a retrieval index without any weight updates; and BioCLIP is a true zero-shot foundation model that receives no Serengeti training data at all. All three are then evaluated on two Southern African test sets, Snapshot Kgalagadi and Snapshot Kruger, as well as on locally collected wildlife photographs from Botswana. We conduct eight experiments covering in-domain baselines, cross-dataset transfer, data scaling, MegaDetector preprocessing, grayscale vs. colour image conditions, and per-species transfer analysis. This work provides the first empirical characterisation of intra-African domain shift across both supervised and zero-shot architectures, and offers practical guidance for conservation AI practitioners who need to deploy models across the diverse ecosystems of Southern Africa without collecting new labelled data.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：相机陷阱（camera trap）网络在非洲产生数百万标记图像，但将在一个地区（如东非塞伦盖蒂）训练的物种分类模型部署到另一个地区（如南部非洲）时，性能因**地理域偏移（geographic domain shift）**而严重下降。现有研究主要关注北美跨地点或洲际迁移，而**非洲内部跨区域迁移**的系统评估缺失。
- **背景与动机**：
  - 东非Snapshot Serengeti等数据集规模巨大，手动标注不可持续，深度学习自动化分类成为刚需。
  - 监督模型（如CNN）在训练区域表现好，但跨区域时因依赖背景、光照、植被等位置特定特征而性能崩溃。
  - 零样本基础模型（如BioCLIP、DINOv2）可能提供替代方案，但尚未在非洲内部跨区域场景下系统比较。
  - 南部非洲（博茨瓦纳、南非）保护工作者急需可靠且泛化的AI工具，但缺乏跨区域迁移的实证指导。

## 2. 方法论：核心思想、关键技术细节、公式/算法流程

- **核心思想**：系统比较三种不同范式的模型在**非洲内部地理域偏移**下的表现，评估监督微调、检索式零样本和真正零样本方法的泛化能力。
- **关键技术细节**：
  - **模型架构**（三种）：
    1. **BEiTV2（监督微调基线）**：基于Vision Transformer，采用掩码图像建模+向量量化标记器预训练，在Serengeti训练集上全参数微调，替换分类头为17种物种线性层。输入224×224。
    2. **DINOv2 + FAISS（检索式零样本）**：使用DINOv2 ViT-Large（patch 14，1024维特征）作为特征提取器，将Serengeti训练集所有图像嵌入存储到FAISS索引（IndexFlatIP，L2归一化，余弦相似度）。推理时取最近邻（k=1）的物种标签作为预测，无需训练。
    3. **BioCLIP（真正零样本）**：基于生物图像预训练的视觉-语言模型，使用标准CLIP零样本协议：对每个物种生成文本提示“a photo of [species name]”，取图像嵌入与文本嵌入余弦相似度最高的物种。不接触任何训练数据。
  - **评估指标**：主要指标为**macro F1**（平衡各物种权重），辅以准确率、精确率、召回率、F1。使用McNemar检验（α=0.05）进行统计显著性检验。域距离度量采用**最大均值差异（MMD）**（RBF核，中位数启发式带宽）。
  - **预处理与实验变量**：包括灰度转换（模拟红外夜间图像）、MegaDetector v6（YOLOv9c）动物检测裁剪（置信度0.2，10%边界框填充，正方形填充）。

## 3. 实验设计：数据集、基准、对比方法

- **数据集**：
  - **源域（训练域）**：Snapshot Serengeti（坦桑尼亚，东非热带草原），约7.1M图像，61物种。训练子集46,471张（17物种保留，每物种约3000张）。
  - **目标域（测试域）**：
    - **Snapshot Kgalagadi**（博茨瓦纳/南非，卡拉哈里沙漠），10,222张，31物种。过滤后5个共享物种（146张测试图像）。
    - **Snapshot Kruger**（南非，混合林地草原），10,072张，46物种。过滤后14个共享物种（1,468张测试图像）。
    - **Local Botswana**（本地手持动物摄影，316张，6物种）。
  - 所有测试集排除空帧，并设置每物种最少9张图像阈值以确保可靠指标。
- **基准（基准）**：
  - 域内实验（Serengeti测试集）提供上限性能参考。
  - 比较三种模型：BEiTV2（监督微调）、DINOv2+FAISS（检索零样本）、BioCLIP（零样本）。
- **对比方法**：八组实验覆盖：
  1. 域内基线（Serengeti）
  2. Serengeti → Kgalagadi
  3. Serengeti → Kruger
  4. Serengeti → Local Botswana
  5. 数据缩放分析（BEiTV2训练数据子集：1%、5%、25%、50%、100%）
  6. MegaDetector预处理（原图 vs 裁剪）
  7. 灰度 vs 彩色图像
  8. 逐物种迁移分析

## 4. 资源与算力

- **硬件**：单块NVIDIA GeForce RTX 3070 Laptop GPU（8 GB VRAM），16 GB系统内存。
- **训练时长**：未明确报告具体训练时钟时间，但提到BEiTV2使用混合精度fp16训练，最大50轮，早停patience=10轮。各训练子集（不同数据比例）均因早停提前终止。
- 未说明集群或多GPU并行。

## 5. 实验数量与充分性

- **实验数量**：共**8组实验**，每组包含多模型比较和不同测试集，总计约**20+个子实验**（如数据缩放实验在4个测试集×5个数据比例下运行，灰度/彩色在4个测试集×3模型下运行，MegaDetector在12个条件下运行）。考虑了**统计显著性检验**（McNemar检验）、置信区间（Wilson 95% CI）。
- **充分性与公平性**：
  - 实验设计系统覆盖域内基线、跨区域迁移、数据量影响、预处理影响、颜色鲁棒性、逐物种分析。
  - 公平性：三个模型共享相同输入尺寸（224×224），BEiTV2微调和DINOv2检索均基于同一Serengeti训练数据（或索引），BioCLIP完全不使用该数据。MegaDetector实验中BEiTV2重新训练，DINOv2重建索引，BioCLIP不重训练。对比方法选择代表三种典型范式。
  - 局限：测试集较小（Kgalagadi仅146张，Botswana 316张），置信区间较宽；本地Botswana数据集图像存在个体重复依赖；未探索多域联合训练。

## 6. 论文主要结论与发现

- **核心发现**：
  - **DINOv2 + FAISS（检索式零样本）** 在所有测试集上表现最稳定：域内macro F1 90.65%，Kgalagadi 79.81%，Kruger 71.69%，Botswana 93.06%。即使没有训练，其跨区域泛化能力最强。
  - **BEiTV2（监督微调）** 遭受最严重的域偏移退化：Kgalagadi准确率从域内83.62%降至28.08%（下降55.54pp），Kruger降至45.16%（下降38.46pp），Botswana降至52.22%（下降31.40pp）。
  - **BEiTV2与BioCLIP在Kruger上无统计显著差异**（45.16% vs 45.84%，p=0.676），表明在没有适应的情况下，监督训练无法提供优势。
  - **MMD域距离无法预测跨区域准确率**：Botswana（最大MMD 0.0975）上DINOv2准确率最高（95.57%），而Kruger（最小MMD 0.0348）上准确率最低（75.00%）。图式域偏移（图像格式差异）影响更大。
  - **MegaDetector裁剪极大提升表现**：对BEiTV2跨区域准确率平均提高21.44pp（Kgalagadi +36.30pp），表明背景依赖是域偏移主要因素。
  - **灰度（模拟夜间）下BEiTV2严重下降**：Kruger从45.16%降至25.14%（下降20.03pp）；DINOv2仅下降≤3pp，颜色鲁棒性最强。
  - **数据缩放**：跨区域增益远弱于域内；更多标记数据不能完全弥补域偏移；在重度不平衡测试集上，宏观F1比准确率更可靠（例如Kruger上5%细粮与25%细粮的准确率反转）。

## 7. 优点

- **首次系统评估非洲内部地理域偏移**，填补了该领域空白。
- **对比三种不同范式**（监督、检索零样本、真正零样本），提供清晰的架构选择指导。
- **实验设计全面**：涵盖8个维度，含统计显著性检验、置信区间、MMD量化域距离，分析细致（逐物种、灰度/裁剪消融等）。
- **引入新测试集**：Snapshot Kgalagadi、Snapshot Kruger和本地博茨瓦纳野生动物照片作为跨区域评估基准。
- **实践导向**：为南部非洲保护工作者提供了明确建议——优先使用检索式或零样本基础模型，减少对新标注数据的依赖。

## 8. 不足与局限

- **测试集规模小**：Kgalagadi仅146张、Botswana 316张，置信区间宽，限制统计精度。Botswana数据集存在个体图像依赖（同一动物可能重复出现）。
- **仅使用东非Serengeti作为唯一训练源**：未探索多域联合训练（如混合Serengeti+Kruger+Kgalagadi），可能低估监督模型潜力。
- **DINOv2检索仅基于Serengeti索引**：未测试向索引添加新区域数据的可扩展性（虽然这是检索方法的自然优势，但本文未实验）。
- **MegaDetector检测率并非100%**（Botswana仅89.9%），部分图像使用原图回退，可能略微影响裁剪实验结论。
- **未讨论超参数调优**：BEiTV2超参数直接从现有研究继承，未进行系统搜索。
- **未涉及类别开放集或细粒度分类**（如区分狮子性别/个体）。
- **域偏移仅量化MMD**，其他潜在指标（如标签分布偏移、图像质量差异）未深入探讨。
- **硬件限制**：使用单块笔记本电脑GPU，可能限制更大模型（如DINOv2 ViT-Large在更高分辨率下）的性能。

（完）
