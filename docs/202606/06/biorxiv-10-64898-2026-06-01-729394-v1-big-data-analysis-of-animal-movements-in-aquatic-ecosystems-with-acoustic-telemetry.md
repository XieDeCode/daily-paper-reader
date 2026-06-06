---
title: Big data analysis of animal movements in aquatic ecosystems with acoustic telemetry
title_zh: 利用声学遥测技术对水生生态系统中动物运动的大数据分析
authors: "Lavender, E., Futia, M. H., Scheidegger, A., Biber, S. W., Brodersen, J., Briers, R. A., Thorburn, J., Albert, C."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729394v1.full.pdf"
tags: ["query:stm"]
score: 7.0
evidence: 使用状态空间模型的时空数据分析
tldr: "被动声学遥测系统广泛应用于追踪水生动物，但针对大规模数据的统计计算方法发展不足。本研究将贝叶斯状态空间模型扩展到大型声学遥测数据集，对北美洲尚普兰湖93条湖鳟（Salvelinus namaycush）四年的定位数据进行分析，重建了动物移动轨迹。通过嵌入生物学知识和精细定位系统、加速计等互补数据集，实现了运动模式与区域停留时间的高精度估计，中位误差和精度（标准误差）低于1%。这项工作推动了全球声学遥测系统大规模运动模式的稳健推断，强化了生态管理证据基础。"
source: biorxiv
selection_source: fresh_fetch
motivation: 提升被动声学遥测网络对大规模动物追踪数据的统计分析价值，弥补统计与计算方法的不足。
method: 应用贝叶斯状态空间模型，并融合精细定位系统、加速计、游泳隧道实验和野外测距数据等生物学知识。
result: "基于93条湖鳟657,360时间步的数据，重建了运动模式，中位误差和精度均低于1%。"
conclusion: 推动了声学遥测系统大规模稳健运动推断，扩展了数据在生态管理中的价值。
---

## 摘要
水下接收器网络（被动声学遥测系统）被部署在世界各地的水生栖息地追踪动物，但令人惊讶的是，通过统计和计算进步来增强这些网络价值的研究关注度有限。在这里，我们将贝叶斯推断的最先进方法扩展到来自声学遥测的大型动物追踪数据集，这是迄今为止在稀疏被动声学遥测系统（非重叠接收器）中进行的最大地理定位分析。利用北美尚普兰湖93条湖鳟（Salvelinus namaycush）的四年数据（每条鱼657,360个时间步），我们构建并拟合状态空间模型以重建动物随时间的变化运动。独特地，我们直接将生物学专业知识以及来自精细定位系统、加速度计、泳道实验和野外范围测试的详细互补数据集嵌入到分析中。利用模拟和真实数据集，我们绘制运动模式图并估计不同管理区的停留时间。我们量化阵列精度，并提供中位数误差和精度（标准误差）低于1%的地图和停留时间估计。这些结果为管理提供了更坚实的证据基础。这项工作使我们朝着在全球声学遥测系统中对运动模式进行大规模稳健推断迈出了一步。我们能够并且应该基于先前的科学进展，将来之不易的数据价值扩展到个体研究之外，以完善生态学和管理学的推断。

## Abstract
Underwater receiver networks (passive acoustic telemetry systems) are deployed to track animals in aquatic habitats all over the world, but remarkably limited attention has been given over to how we can strengthen the value of these networks through statistical and computational advances. Here, we upscale state-of-the-art methods of Bayesian inference to big animal-tracking datasets from acoustic telemetry, with the largest geolocation analysis in a sparse passive acoustic telemetry system (with non-overlapping receivers) to date. Using four years of data from 93 lake trout (Salvelinus namaycush) in North America's Lake Champlain (657,360 timesteps per individual), we formulate and fit state-space models to reconstruct animal movements through time. Uniquely, we directly embed biological expertise and detailed complementary datasets from fine-scale positioning systems, accelerometry, swim-tunnel experiments and field range tests in our analysis. Using simulated and real-world datasets, we map movement patterns and estimate residency in distinct management zones. We quantify array precision and deliver maps and residency estimates with a median error and precision (standard error) below 1 %. These results strengthen the evidence base for management. This work takes us a step towards robust inference of movement patterns at scale in acoustic telemetry systems across the world. We can, and should, build on prior scientific progress and extend the value of hard-earned data beyond individual studies to refine inferences for ecology and management.