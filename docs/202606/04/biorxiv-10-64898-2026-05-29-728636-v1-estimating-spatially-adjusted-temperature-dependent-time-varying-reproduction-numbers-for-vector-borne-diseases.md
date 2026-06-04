---
title: Estimating spatially adjusted temperature-dependent time-varying reproduction numbers for vector-borne diseases
title_zh: 估计空间调整的温度依赖的媒介传播疾病时变再生数
authors: "Ponce, L. J., Choo, E. L. W., Mailepessov, D., Bansal, S., Tan, K. B., Parag, K. V., Lim, J. T."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.29.728636v1.full.pdf"
tags: ["query:stm"]
score: 7.0
evidence: 用于疾病传播数的时空数据分析
tldr: 传统再生数估计未充分考虑温度和空间异质性。本文将温度依赖的世代时间分布和空间衰减权重集成到Wallinga-Teunis框架中，模拟比较发现估计误差主要源于随机不确定性而非模型偏差。在登革热数据上，空间调整模型能更灵敏地响应病例波动，高斯核优于指数核，温度依赖性有限影响。该框架可稳健应用于不同气候，助力回顾性分析。
source: biorxiv
selection_source: fresh_fetch
motivation: 媒介传播疾病的传播受环境和空间条件影响，现有再生数估计方法未整合温度依赖的世代时间和空间传播加权，可能导致估计偏差。
method: 将温度依赖的生成时间分布和空间衰减函数（高斯或指数核）嵌入Wallinga-Teunis方法，通过仿真比较不同场景下的估计误差，并应用于新加坡登革热数据。
result: "误差主要由方差而非偏差主导；高斯空间核性能最佳；温度依赖性误设在地面实况为温度依赖时误差增大（16-58% vs 36-58%），否则相似；空间调整模型产生更起伏的估计轨迹。"
conclusion: 显式建模空间异质性和温度动态能提高再生数估计对波动的敏感性，框架稳健且适用于不同气候条件下的回顾性分析。
---

## 摘要
估计有效再生数对于理解和控制传染病暴发至关重要。对于登革热等媒介传播疾病，传播取决于环境和空间条件：温度影响蚊子的外潜伏期，改变传播时间，而空间邻近性可能导致传播聚集。我们将温度依赖的世代时间分布和按距离加权传播可能性的空间衰减函数整合到Wallinga & Teunis估计框架中。模拟比较了真实世代时间对于空间调整疾病病例是温度依赖还是温度独立的情况，以及对应的模型假设。通过百分误差与真实值对比评估每日再生数(Rt)。我们发现误差主要由方差而非偏差驱动，表明指示感染者的随机不确定性是不准确的主要驱动因素，而非系统模型校准错误。假设空间权重函数赋予地理上接近的感染者-被感染者对更高的传播概率（高斯空间衰减），其估计值与真实值之间的百分误差优于其他空间核函数。在高斯空间核下错误指定温度依赖关系时，当真实情况为温度依赖时误差较高（16-38% vs 36-58%偏差），而为温度独立时误差相似（32-52% vs 35-56%偏差），表明当底层传播过程中不存在温度依赖性时，对温度依赖的敏感性有限。对新加坡登革热病例数据的应用表明，空间调整模型产生的时间轨迹比时间序列平滑方法更具可变性，高斯衰减比指数衰减产生更稳定的估计，而温度依赖模型产生适度改进，表明明确建模空间异质性和温度依赖的传播动力学增加了对病例数波动的响应能力。我们的框架在气候上具有鲁棒性，通过使用更广温度范围的模拟得到证明，并表明在回顾性分析中具有有用的应用。

## Abstract
Estimating the effective reproduction number is crucial for understanding and managing infectious disease outbreaks. For vector-borne diseases like dengue, transmission depends on environmental and spatial conditions: temperature affects the extrinsic incubation period in mosquitoes, altering transmission timing, while spatial proximity can lead to clusters of transmission. We integrated a temperature-dependent (TD) generation time (GT) distribution and a spatial decay function weighting transmission likelihood by distance into the Wallinga & Teunis estimation framework. Simulations compared scenarios where the true generation time for spatially adjusted disease cases were TD or temperature independent (TI), versus their corresponding model assumptions. Daily reproduction numbers (Rt) estimated were evaluated via percent error against true values. We found error to be predominantly driven by variance rather than bias, indicating that stochastic uncertainty in infector assignment was the primary driver of inaccuracies rather than systematic model miscalibration. Assuming a spatial weighting function assigning higher probabilities of transmission to geographically close infector-infectee pairs (Gaussian spatial decay) percent errors measuring deviation between estimated and true outperformed those of alternative spatial kernels. Mis-specifying temperature-dependence under a Gaussian spatial kernel yielded higher errors when the ground truth was TD (16-38% vs 36-58% deviation), and similar errors when it was TI (32-52% vs 35-56% deviation), indicating limited sensitivity to temperature dependence when it was not present in the underlying transmission process. Application to dengue case data in Singapore showed that spatially adjusted models produced more variable trajectories than time-series smoothing approaches, with Gaussian decay yielding more stable estimates than exponential decay and the TD model producing modest refinements, suggesting that explicitly modeling spatial heterogeneity and TD transmission dynamics increases responsiveness to even fluctuations in case counts. Our framework is robust across climates, shown by simulations using a broader temperature range, and suggests a useful application in retrospective analyses.