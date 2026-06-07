---
title: Supervised Domain Adaptation Mitigates Cross-Ethnicity Prediction Error in Neuroimaging Based Cognitive Prediction
title_zh: 监督域自适应减轻基于神经影像的认知预测中的跨种族预测误差
authors: "Lal Khakpoor, F., van der Vliet, W., Deng, J., Wang, Y., Pat, N."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.727742v2.full.pdf"
tags: ["query:cross-domain"]
score: 8.0
evidence: 监督域适应方法减少神经影像中的跨种族预测误差
tldr: 大规模神经影像数据集常存在种族不平衡，导致模型对少数族裔预测不准。本研究在ABCD数据集上评估四种监督域适应方法，发现平衡加权能有效降低基于白人大脑结构MRI训练的模型对非裔美国人的预测误差，尤其在MRI模态差异大时改善显著，且仅需少量目标域样本即可实现。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经影像预测模型因训练数据种族失衡，对非裔美国人等少数族裔预测误差更大，亟需低成本策略提升公平性。
method: 在ABCD数据集上，以白人数据训练，对80种MRI指标，比较平衡加权、两阶段TrAdaBoost、特征增强和线性插值四种域适应方法的效果。
result: 所有域适应方法均降低非裔美国人的预测误差，平衡加权最优；在仅用10个非裔样本时仍有效，且对模态差异大的指标改善更显著。
conclusion: 简单的监督域适应方法能有效减少跨种族预测差异，为神经影像机器学习公平性提供实用框架。
---

## 摘要
机器学习模型越来越多地用于从神经影像数据预测认知和临床结果，但在公平性和泛化性方面仍存在挑战。大规模数据集通常在种族和民族上不平衡，导致系统性性能差异，模型通常对训练数据中占多数的群体获得更高准确性。在本研究中，我们评估了监督域自适应方法——包括平衡加权、两阶段TrAdaBoost、使用SrcOnly预测的特征增强和线性插值——是否可以减轻这些偏差。使用ABCD数据集，我们评估了基于80个来自白人参与者的MRI测量训练的模型能否更有效地推广到非裔美国人参与者。所有域自适应方法都减少了非裔美国人参与者的预测误差，特别是对于基线差异较大的MRI模态（例如结构MRI），而在初始差距较小的模态（例如功能连接）上改善有限。在这些方法中，平衡加权表现最好，即使仅使用10名非裔美国人参与者来调整最初完全基于白人参与者训练的模型，该方法也保持稳定且有益。这些发现表明，简单、低成本的策略可以有效减少跨种族性能差距，提高预测性神经影像的公平性，为未来的神经影像预测生物标志物提供了一条实用路径。

重要声明：大规模神经影像数据集越来越多地使机器学习模型能够预测认知和临床结果；然而，这些数据集通常是种族/民族不平衡的。因此，预测模型往往难以泛化到代表性不足的人群。我们证明，在80个MRI表型中，一类统称为监督域自适应的机器学习方法可以显著减少基于神经影像的认知预测中的跨种族差异，即使只有来自代表性不足群体的有限数据可用。在所评估的方法中，平衡加权在保持低计算成本的同时实现了最佳性能。总之，这些发现提供了一个实用且可扩展的框架，用于在种族/民族不平衡的现实条件下提高基于神经影像的机器学习的公平性和泛化性。

## Abstract
Machine-learning models are increasingly used to predict cognitive and clinical outcomes from neuroimaging data, yet challenges in fairness and generalizability remain. Large-scale datasets are often racially and ethnically imbalanced, leading to systematic performance disparities, with models typically achieving higher accuracy for majority populations represented in the training data. In this study, we evaluated whether supervised domain adaptation methods--including balanced weighting, two-stage TrAdaBoost, feature augmentation with SrcOnly prediction, and linear interpolation--can mitigate these biases. Using the ABCD dataset, we assessed whether models trained on 80 MRI measures from White American participants could generalize more effectively to African American participants. All domain adaptation methods reduced prediction error for African American participants, particularly for MRI modalities with large baseline disparities (e.g., structural MRI), while offering limited improvements where initial gaps were smaller (e.g., functional connectivity). Among the approaches, balanced weighting performed best and remained stable and beneficial even when only 10 African American participants were used to adapt the original model trained exclusively on White American participants. These findings suggest that simple, low-cost strategies can effectively reduce cross-ethnic performance gaps and improve equity in predictive neuroimaging, offering a practical path forward for future neuroimaging predictive biomarkers.

Significant StatementLarge-scale neuroimaging datasets increasingly enable machine-learning models to predict cognitive and clinical outcomes; however, these datasets are often ethnically/racially imbalanced. As a result, predictive models tend to generalize poorly to underrepresented populations. We demonstrate that, across 80 MRI phenotypes, a class of machine-learning approaches collectively known as supervised domain adaptation can substantially reduce cross-ethnicity disparities in neuroimaging-based cognitive prediction, even when only limited data from underrepresented groups are available. Among the methods evaluated, balanced weighting achieved the best performance while maintaining low computational cost. Together, these findings provide a practical and scalable framework for improving fairness and generalizability in neuroimaging-based machine learning under realistic conditions of ethnic/racial imbalance.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义
- **研究动机**：大规模神经影像数据集（如ABCD）常存在种族/民族不平衡，训练数据中白人群体占多数，导致模型对非裔美国人等少数族裔的预测误差显著增大。现有机器学习模型在公平性和泛化性方面面临挑战。
- **整体含义**：本研究旨在探索低成本、简单的监督域适应方法能否有效缩小跨种族预测性能差距，为神经影像预测生物标志物提供实用且可扩展的公平性提升框架。

## 2. 方法论
- **核心思想**：利用监督域适应技术，将模型从源域（白人参与者数据）调整到目标域（非裔美国人参与者数据），减少分布偏移带来的预测偏差。
- **关键技术细节**：
  - **平衡加权（Balanced Weighting）**：对训练样本重新分配权重，使得不同种族样本在损失函数中的贡献平衡。
  - **两阶段TrAdaBoost**：一种基于Boosting的迁移学习方法，通过迭代调整样本权重，优先关注目标域中难以预测的样本。
  - **特征增强（Feature Augmentation with SrcOnly prediction）**：将源域模型预测结果作为额外特征，与原始特征拼接后重新训练目标域适配模型。
  - **线性插值（Linear Interpolation）**：将源域模型参数与目标域微调后的参数按一定比例插值，获得最终模型。
- **算法流程（文字说明）**：
  1. 以全部白人参与者数据训练一个基础预测模型（SrcOnly）。
  2. 针对每种域适应方法，使用少量非裔美国人参与者数据（从10个到全量）进行调整。
  3. 比较调整后模型对非裔美国人参与者的预测误差，评估公平性改善。

## 3. 实验设计
- **数据集**：ABCD数据集（Adolescent Brain Cognitive Development），包含80种MRI测量指标（涵盖结构MRI、功能连接等不同模态）。
- **基准（Benchmark）**：完全基于白人参与者训练、未做域适应的模型（SrcOnly）作为基线。
- **对比方法**：四种监督域适应方法：
  - 平衡加权
  - 两阶段TrAdaBoost
  - 特征增强（使用SrcOnly预测）
  - 线性插值
- **评估指标**：预测误差（例如均方误差或绝对误差）在非裔美国人参与者上的表现；同时按MRI模态差异大小进行分层分析。

## 4. 资源与算力
- **文中未明确说明**：论文摘要中未提及使用的GPU型号、数量或训练时长等具体算力信息。仅提到域适应方法“低计算成本”，但未量化。

## 5. 实验数量与充分性
- **实验数量**：覆盖80种MRI表型，四种域适应方法，并考察了不同目标域样本量（如仅10个非裔样本）的效果。实验规模较大。
- **充分性与公平性**：
  - 实验设计较为充分：对比了多种方法，并分析了不同模态的异质性。
  - 但仅使用一个数据集（ABCD）和一个源域（白人）与一个目标域（非裔）的跨种族场景，未涵盖其他种族/民族或不同数据集的交叉验证，泛化性验证有限。
  - 未报告统计显著性检验或置信区间，可能影响结论的可靠性。

## 6. 主要结论与发现
- 所有四种监督域适应方法均能减少非裔美国人的预测误差。
- **平衡加权表现最佳**，且在使用极少量目标域样本（10个非裔参与者）时仍保持稳定和有效。
- 改善幅度与MRI模态的基线差异相关：结构MRI等基线差异大的模态改善显著，功能连接等初始差距小的模态改善有限。
- 简单、低成本的策略即可有效提升跨种族预测公平性，为神经影像机器学习提供实用路径。

## 7. 优点
- **方法简洁实用**：无需复杂深度学习架构，可在现有模型基础上快速应用。
- **低数据依赖**：仅需少量目标域样本（10个）即可获得显著改善，符合现实场景中少数族裔样本稀缺的特点。
- **模态差异性分析**：揭示了不同MRI模态对域适应方法的响应差异，为后续针对性优化提供洞察。
- **综合对比**：在统一数据集和指标下系统比较四种经典域适应方法，结论具有参考价值。

## 8. 不足与局限
- **实验覆盖不广**：仅使用一个数据集（ABCD），且仅涉及非裔美国人单一目标域，结论对其他人群（如亚裔、拉丁裔等）及临床场景的适用性未知。
- **未考虑更复杂的偏差来源**：仅调整种族不平衡，未控制社会经济地位、健康差异等混杂因素。
- **统计报告缺失**：缺乏置信区间、效应量或假设检验，难以评估改善的稳定性和统计显著性。
- **计算资源未披露**：无法复现计算成本，降低了方法可复制性。
- **功能连接模态改善有限**：初始差距小的场景下域适应效果微弱，需要针对不同模态设计更精细的适配策略。

（完）
