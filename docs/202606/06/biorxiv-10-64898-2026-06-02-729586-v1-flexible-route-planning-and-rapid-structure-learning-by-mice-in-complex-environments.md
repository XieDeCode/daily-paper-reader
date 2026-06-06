---
title: Flexible route planning and rapid structure learning by mice in complex environments
title_zh: 复杂环境中小鼠的灵活路径规划与快速结构学习
authors: "Pereira, M., Godinho, B. S., Machens, C. K., Costa, R. M., Akam, T."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729586v1.full.pdf"
tags: ["query:world-models"]
score: 9.0
evidence: 用于规划和导航的世界模型
tldr: 动物灵活行动依赖环境预测模型，但机制不明。空间导航涉及习惯、向量导航和路径规划等多种系统。我们设计了优化的行为试验，让小鼠在复杂迷宫中导航至随机变化的目标位置，收集数千条非重复轨迹。小鼠表现出高效导航（偏好最短路径）和快速结构学习（首次会话即掌握迷宫结构）。该试验为解离控制系统、量化脑-行为关系提供了有效方法。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有空间导航试验难以分离不同控制系统和解相关行为变量，限制了对世界模型如何指导灵活行动的理解。
method: 开发并计算优化行为试验，小鼠在复杂迷宫中导航至视觉提示目标，随机化起始和目标位置以生成多样化轨迹。
result: 小鼠高效导航并快速学习迷宫结构，表现为偏好最短路径和首次会话即展现环境知识。
conclusion: 本试验为研究世界模型支持灵活行为提供了强大工具，有助于揭示空间导航的神经机制。
---

## 摘要
利用环境预测模型进行行动选择在人和动物行为中起着基础性作用，但在回路和算法层面上的理解仍然有限。空间导航是描述世界模型如何指导行动选择的一个有吸引力的领域。然而，空间行为受到多种控制系统的影响，包括习惯、使用空间关系的欧几里得模型进行矢量导航，以及使用环境结构模型进行路径规划。理解世界模型如何支持导航需要能够分离控制系统并去相关行为变量的实验方法，同时生成大量数据集以精确量化脑-行为关系。在这里，我们开发并计算优化了一个行为测试，以量化利用环境结构知识的灵活导航。小鼠在复杂迷宫中导航到视觉提示的目标，每次试验中起始位置和目标位置随机化，产生了数千个不重复的目标导向导航轨迹。它们导航效率高——强烈偏好最短路径上的选项，并且学习迅速——在新环境中的第一次实验就表现出对迷宫结构的了解。我们预期该测试将有助于描述世界模型如何支持灵活行为。

## Abstract
Action selection using predictive models of the environment plays a fundamental role in human and animal behaviour, yet is poorly understood at circuit and algorithmic levels. Spatial navigation is an attractive domain for characterising how world models guide action selection. However spatial behaviours are shaped by multiple control systems including habits, vector-navigation using a Euclidean model of spatial relationships, and route planning using models of environment structure. Understanding how world models support navigation requires assays that dissociate control systems and decorrelate behavioural variables, while generating large datasets that allow precise quantification of brain-behaviour relationships. Here we developed and computationally optimised a behavioural assay to quantify flexible navigation using knowledge of environment structure. Mice navigated to visually cued goals in complex mazes, with randomised start and goal locations on each trial, generating thousands of non-repetitive goal-directed navigation trajectories. They navigated efficiently - strongly favouring options on the shortest path-to-goal, and learnt rapidly - demonstrating knowledge of maze structure from their first sessions in new environments. We anticipate the assay will be useful for characterising how world models support flexible behaviour.

---

## 论文详细总结（自动生成）

# 复杂环境中小鼠的灵活路径规划与快速结构学习——论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：动物如何利用环境预测模型（世界模型）进行灵活的行动选择？具体在空间导航中，多个控制系统（习惯、基于欧几里得模型的矢量导航、基于环境结构模型的路径规划）如何协同或竞争？现有行为实验难以分离这些系统，且行为变量高度相关，限制了神经机制的研究。
- **研究动机**：为了解构世界模型在回路和算法层面的作用，需要一种行为范式，能够：
  - 分离不同的控制系统（如习惯 vs 路径规划）；
  - 去相关行为变量（如距离、角度、历史选择等）；
  - 产生大量、多样化的轨迹数据，以精确量化脑-行为关系。
- **整体含义**：该论文旨在开发一个计算优化的行为测试，用于量化小鼠在复杂迷宫中利用环境结构知识进行灵活导航的能力，为后续神经记录和干扰实验提供标准化工具。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：设计一个“随机起始-随机目标”的复杂迷宫导航任务，迫使小鼠每次试验都产生全新的、非重复的轨迹，从而排除习惯化、固定路径等简单策略，迫使小鼠利用环境结构模型进行在线路径规划。
- **关键技术细节**：
  - **迷宫结构**：复杂但可控的迷宫，包含多个岔路口，形成连通图。
  - **视觉提示目标**：每次试验中，一个目标位置被视觉线索标记（例如闪烁LED），小鼠需导航至该位置获得奖励。
  - **随机化策略**：每次试验独立随机选择起始位置和目标位置，确保轨迹多样性，打破空间位置与运动序列的简单关联。
  - **计算优化**：通过计算机模拟优化迷宫布局（如分支数量、连通性），使小鼠的行为变量（如路径长度、转向角度、历史奖赏）尽可能去相关，同时保证任务难度适中。
- **流程说明**：
  1. 小鼠在迷宫中适应后，开始试验。
  2. 每次试验开始：目标位置亮灯，小鼠从随机起始位置出发。
  3. 小鼠自由探索并按最短/高效路径到达目标则奖励。
  4. 记录每一帧的位置、选择、时间等。
  5. 离线分析轨迹特征（如是否偏好最短路径选项、学习速度）。

## 3. 实验设计：使用了哪些数据集 / 场景，它的 benchmark 是什么，对比了哪些方法

- **使用的数据集/场景**：
  - 场景：小鼠在复杂迷宫中导航至视觉提示目标。
  - 数据：数千条非重复的、目标导向的导航轨迹（来自多只小鼠、多次试验）。
- **Benchmark**：论文未表明与已有方法进行定量对比。其本身的基准是小鼠行为表现（效率、学习速度）。
- **对比方法**：未提及与其他具体行为模型（如强化学习、拓扑规划、向量导航）的对比。该论文主要贡献是提出新行为范式，而非对比算法。

## 4. 资源与算力

- **文中未明确提及**任何关于计算资源的描述（如GPU型号、数量、训练时长）。仅提到“计算优化”，但未说明使用何种硬件或软件。可能涉及迷宫设计的计算机模拟，但无具体细节。

## 5. 实验数量与充分性

- **实验数量**：文中仅概括性地描述“小鼠……产生了数千个不重复轨迹”“首次会话即表现出迷宫结构知识”。未报告具体小鼠数量、试验次数、迷宫版本数、是否进行消融（如去除视觉提示、改变迷宫拓扑等）。缺乏统计细节（均值、方差、显著性检验）。
- **充分性评估**：
  - **优点**：样本量可能较大（“数千轨迹”），且设计旨在去相关变量，具备较好的控制。
  - **不足**：
    - 缺乏与对照组（如无随机化、固定路径训练、模型预测等）的比较。
    - 未明确区分不同控制系统（习惯、矢量导航、路径规划）的相对贡献。
    - 未进行神经干预或记录，仅停留在行为层面。
    - 未提供跨迷宫拓扑的泛化实验。
    - 论文是预印本（biorxiv），可能尚未完成同行评审，实验设计细节可能不完整。

## 6. 论文的主要结论与发现

- **小鼠导航高效**：强烈偏好选择位于到达目标最短路径上的岔路选项（而非等长路径或随机选择），表明使用环境结构进行路径规划。
- **小鼠学习迅速**：在新环境的第一次实验会话中即表现出对迷宫结构的了解（例如能直接选择通往目标的正确分支），而非需要多次试错学习。
- **行为范式有效**：该测试能够产生大量去相关行为变量、非重复轨迹，适合用于量化脑-行为关系，为研究世界模型支持灵活行为提供了工具。

## 7. 优点：方法或实验设计上的亮点

- **去相关行为变量**：通过随机化起始和目标位置，有效减少了传统导航任务中位置、距离、历史选择等变量的共线性，便于后续神经数据分析（如回归、解码）。
- **大样本量**：数千条非重复轨迹，有利于高统计功效和精确的行为量化。
- **快速学习效应**：小鼠首次会话即表现知识，缩短了训练周期，降低实验成本。
- **分离控制系统**：任务设计迫使依赖环境结构（图模型），而非简单习惯或矢量导航，为研究路径规划的神经基础提供纯净场景。
- **计算优化**：提前模拟确定了迷宫参数，提高了实验效率。

## 8. 不足与局限

- **实验覆盖不足**：
  - 未系统变化迷宫拓扑（如网格、树状、图环等）验证泛化性。
  - 未比较不同物种（仅小鼠）。
  - 未包含神经活动记录或操作（如光遗传、钙成像），无法直接关联脑区。
- **偏差风险**：
  - 小鼠可能利用非结构化线索（如气味、本体感觉）辅助导航，而非严格依赖视觉目标。
  - 随机化可能引入其他变量（如记忆干扰），未被控制。
- **算法层面缺失**：
  - 未建立计算模型（如强化学习、图搜索）拟合行为，缺乏对小鼠所使用策略的定量判定。
  - 未与现有导航模型（如基于局部视景、路径整合）进行对比。
- **应用限制**：
  - 迷宫设计可能复杂，复现需一定工程条件。
  - 仅适用于高度受控的实验室环境，与现实世界复杂导航有差距。

（完）
