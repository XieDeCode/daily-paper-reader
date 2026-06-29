---
title: Modeling Dynamical Vision with Biologically Plausible Recurrent Convolutional Networks
title_zh: 用生物可信的循环卷积网络建模动态视觉
authors: "Gutzen, R., Lindsay, G. W."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.1101/2025.08.11.669756v2.full.pdf"
tags: ["query:stm"]
score: 7.0
evidence: 用于动态视觉的循环卷积网络，涉及时空现象
tldr: "标准前馈CNN缺乏视觉皮层中普遍的递归连接，难以模拟时空适应等现象。为此，该研究提出了DynVision，一个模块化开源工具箱，用于构建生物合理的递归卷积网络（RCNN），支持多种递归类型、异构延迟和数值ODE求解器。通过系统参数空间探索发现，连续时间递归动力学能自然产生皮层时间现象，且不同递归配置可达到接近人类的噪声鲁棒性。该框架实现了52%的训练加速，并为连接生物学与深度学习提供了实用工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有CNN缺乏递归连接，难以模拟视觉皮层的时空动力学，需要可比较不同架构选择的工具。
method: 开发DynVision开源工具箱，集成数值ODE求解器、异构延迟和五种递归类型，采用配置驱动设计分离建模与实现。
result: "训练加速52%；连续时间递归自动产生皮层时间现象，特定配置实现接近人类的噪声鲁棒性。"
conclusion: 递归类型和连接模式对动力学定性差异敏感，需综合框架指导生物合理视觉模型探索。
---

## 摘要
经过图像识别训练的卷积神经网络（CNN）与灵长类动物的腹侧视觉通路表现出显著的概念相似性，但其标准的前馈架构缺乏视觉皮层中普遍存在的循环连接。这种循环被认为支撑着时空现象，包括适应、延迟归一化以及对噪声输入的鲁棒性。然而，将功能有益的循环纳入能够捕捉生物视觉时空现象的CNN中仍然具有挑战性。尽管近期进展已经融入了神经生物学约束，但该领域缺乏可用的工具来系统比较不同的架构选择（如循环类型、时间延迟和连接模式）如何塑造神经动态和行为。在此，我们介绍DynVision，一个模块化的开源工具箱，用于构建和评估生物可信的循环卷积神经网络（RCNN）。DynVision实现了具有异质延迟的数值ODE求解器，支持五种侧向循环类型，范围从简单的自连接到皮层组织的局部循环，并通过配置驱动设计将科学建模决策与实现细节分离。训练计算效率高，比参考实现提速52%。我们通过系统探索参数空间来展示该框架，揭示时间动态的定性差异对通常隐式的建模选择高度敏感，例如循环整合的目标位置和用于损失计算的时间窗口。关键的是，我们发现连续时间循环动态可以自然产生皮层时间现象，无需显式的分式归一化，而另一种循环配置则产生接近人类水平的噪声鲁棒性。这些发现表明了循环的不同功能配置，并凸显了创建完全逼真模型的挑战，从而强调需要全面且连贯的建模框架以辅助探索。代码和文档见 https://github.com/Lindsay-Lab/DynVision/。

## Abstract
AO_SCPLOWBSTRACTC_SCPLOWConvolutional Neural Networks (CNNs) trained for image recognition have demonstrated remarkable conceptual similarities to the primate ventral visual pathway, but their standard feedforward architectures lack the recurrent connections that are ubiquitous in visual cortex. Such recurrence is thought to underlie spatiotemporal phenomena including adaptation, delayed normalization, and robustness to noisy input. However, incorporating functionally beneficial recurrence into CNNs that captures spatiotemporal phenomena of biological vision remains challenging. Although recent advances have incorporated neurobiological constraints, the field lacks accessible tools for systematically comparing how different architectural choices, such as recurrence type, temporal delays, and connectivity patterns, shape neural dynamics and behavior. Here, we introduce DynVision, a modular open-source toolbox for constructing and evaluating biologically plausible recurrent convolutional neural networks (RCNNs). DynVision implements numerical ODE solvers with heterogeneous delays, supports five types of lateral recurrence ranging from simple self-connections to cortically-organized local recurrence, and separates scientific modeling decisions from implementation details through a configuration-driven design. Training is computationally efficient, achieving a 52% speedup over reference implementations. We demonstrate the framework through systematic exploration of the parameter space, revealing that qualitative differences in temporal dynamics are highly sensitive to often-implicit modeling choices such as the target location of recurrent integration and the temporal window used for loss computation. Critically, we find that continuous-time recurrent dynamics can naturally give rise to cortical temporal phenomena without requiring explicit divisive normalization, while a different recurrent configuration produces noise robustness approaching human-level performance. These findings suggest functionally distinct configurations of recurrence and highlight the challenge of creating fully realistic models, thus emphasizing the need for a comprehensive and cohesive modeling framework to aid exploration. Code and documentation are available at https://github.com/Lindsay-Lab/DynVision/.