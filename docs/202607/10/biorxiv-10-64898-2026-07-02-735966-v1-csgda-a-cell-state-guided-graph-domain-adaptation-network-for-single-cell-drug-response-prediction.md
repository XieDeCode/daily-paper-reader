---
title: "CSGDA: A Cell State-Guided Graph Domain Adaptation Network for Single-Cell Drug Response Prediction"
title_zh: CSGDA：一种细胞状态引导的图域自适应网络用于单细胞药物响应预测
authors: "Yan, F., Cao, X., Mao, F., You, Z., Chen, Y., Du, Z., Huang, Y.-A."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.735966v1.full.pdf"
tags: ["query:cross-domain"]
score: 6.0
evidence: 用于药物响应预测的图域适应网络
tldr: "单细胞药物响应预测面临跨领域分布漂移挑战，现有方法难以处理。本文提出CSGDA框架，利用细胞状态先验引导图结构学习，结合域自适应和重叠惩罚机制，在五个数据集上平均提升ACC和AUPR约6%。集成梯度分析揭示了转移耐药的关键基因，为精准医学提供新工具。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1839, \"height\": 1216, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 898, \"height\": 843, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 854, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1775, \"height\": 1309, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 812, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 808, \"height\": 708, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-735966-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1843, \"height\": 379, \"label\": \"Table\"}]"
motivation: 解决单细胞药物响应预测中因测序平台、组织微环境和转移演化导致的跨领域分布漂移问题。
method: 构建细胞状态引导的图域自适应网络，通过生物先验映射基因表达、结构学习及重叠惩罚机制对齐域分布。
result: "在五个单细胞数据集上ACC和AUPR平均提升约6%，并识别出跨转移顺铂耐药关键基因。"
conclusion: CSGDA有效处理单细胞异质性，为跨领域药物响应预测提供鲁棒方案，推动精准医学应用。
---

## 摘要
肿瘤内异质性驱动癌症复发和转移，然而单细胞药物响应预测面临严峻的“跨域”挑战，例如将体外模型应用于体内组织，或从原发肿瘤推断转移性耐药。这些场景触发由异质测序平台、不同的组织微环境和转移性演变引起的分布偏移——现有方法很少解决这些问题。我们引入CSGDA，一种细胞状态引导的图域自适应框架，旨在跨这些生物异质性预测药物响应。CSGDA整合生物先验知识，将基因表达映射到功能性细胞状态，引导结构学习模块构建稳健的细胞拓扑。为了克服分布偏移，该模型采用图域自适应结合一种新颖的重叠惩罚机制。在五个scRNA-seq数据集上的广泛基准测试表明，CSGDA优于最先进的方法，在ACC和AUPR上平均提升约6%。除了预测准确性，我们还在一个具有挑战性的跨转移顺铂数据集中使用积分梯度有效定位了与耐药相关的关键基因。这些发现强调了CSGDA在单细胞药物响应预测中的优越性能及其在解决单细胞异质性方面的潜力，为精准医学铺平了道路。

## Abstract
Intratumoral heterogeneity drives cancer recurrence and metastasis, yet single-cell drug response prediction faces severe "cross-domain" challenges, such as applying in vitro models to in vivo tissues or inferring metastatic resistance from primary tumors. These scenarios trigger distribution shifts arising from heterogeneous sequencing platforms, distinct tissue microenvironments, and metastatic evolution--problems rarely addressed by existing methods. We introduce CSGDA, a cell state-guided graph domain adaptation framework designed to predict drug responses across these biological heterogeneities. CSGDA incorporates biological priors to map gene expression into functional cell states, guiding a structure learning module to construct robust cell topology. To conquer distribution shifts, the model employs graph domain adaptation combined with a novel overlap penalty mechanism. Extensive benchmarks on five scRNA-seq datasets demonstrate that CSGDA outperforms state-of-the-art methods, achieving an average gain of [~]6% in ACC and AUPR. Beyond prediction accuracy, we employed integrated gradients to effectively pinpoint key genes involved in drug resistance within a challenging cross-metastasis cisplatin dataset. These findings underscore CSGDAs superior performance in single-cell drug response prediction and its potential in resolving single-cell heterogeneity, paving the way for precision medicine.