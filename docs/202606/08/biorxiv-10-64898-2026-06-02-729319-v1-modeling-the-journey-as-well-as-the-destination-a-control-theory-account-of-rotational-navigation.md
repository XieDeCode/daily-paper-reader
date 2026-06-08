---
title: "Modeling the journey as well as the destination: a control theory account of rotational navigation"
title_zh: 建模旅程与目的地：旋转导航的控制理论解释
authors: "Huang, Y., Vishwanath, A., Du, Y. K., Watson, M. F., Asiri, O., Dakin, K., Markham, D., Ekstrom, A. D., Wilson, R. C."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729319v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: 导航的闭环控制模型
tldr: 导航中如何将朝向估计转化为运动指令尚不清楚。本文假设导航为闭环过程，通过感觉预测误差更新运动。开发了联合估计朝向和角速度的闭环模型，不仅预测最终位置还预测运动动态。实验表明参与者行为符合模型，地标移动引起快速纠正运动，揭示了自然运动依赖于闭环控制。
source: biorxiv
selection_source: fresh_fetch
motivation: 当前导航模型侧重朝向估计，但忽略了从估计到运动指令的迭代转化过程。
method: 开发闭环控制模型，联合估计朝向和角速度，并用虚拟现实旋转任务验证预测误差对运动的影响。
result: 地标移动引起的视觉预测误差导致参与者加速度快速变化，且误差越大纠正越大。
conclusion: 导航运动通过闭环控制连续更新运动指令，而非开环执行。
---

## 摘要
导航需要估计航向并将这些估计转化为行动。以往的模型解释了自我运动和地标线索如何结合形成航向估计，但对于这些估计如何迭代转化为达到目标的运动指令知之甚少。这里，我们假设导航作为一个闭环过程运作，其中持续的运动由感觉预测误差更新。为了验证这一假设，参与者在虚拟现实中执行目标导向的旋转任务。在选定的试验中，地标在运动过程中被移动，从而在自我运动估计预期的航向与移位地标观察到的航向之间诱导出预测误差。同时，我们开发了一个转向行为的闭环模型，该模型将航向和角速度表示为随时间联合估计的状态。该模型不仅解释了最终位置（目的地），还解释了产生最终位置的运动动力学（旅程）。模型预测，地标诱导的视觉预测误差应在运动中产生快速的修正性改变。参与者的转向行为在定性上与这些模型动态相似：加速度在视觉反馈后发生变化，较大的地标不匹配产生较大的修正响应。总之，这些发现表明，自然运动依赖于通过闭环控制将航向估计连续转化为运动指令。

## Abstract
Navigation requires estimating heading and transforming these estimates into actions. Prior models explain how self-motion and landmark cues are combined into heading estimates, but less is known about how these estimates are iteratively transformed into motor commands to reach a goal. Here, we hypothesized that navigation operates as a closed-loop process in which ongoing movement is updated by sensory prediction errors. To test this hypothesis, participants performed a goal-directed rotation task in virtual reality. On select trials, visual landmarks were shifted during movement, inducing a prediction error between the heading expected from self-motion estimates and the heading observed from the shifted landmarks. In parallel, we developed a closed-loop model of turning behavior that represents heading and angular velocity as jointly estimated states over time. This model accounts not only for final position, the destination, but also for the movement dynamics that produce it, the journey. The model predicts that landmark-induced visual prediction errors should produce rapid corrective changes in movement. Participant turning behavior qualitatively paralleled these model dynamics: acceleration changed after visual feedback, with larger landmark mismatches producing larger corrective responses. Together, these findings suggest that naturalistic movement depends on continuously transforming heading estimates into motor command through closed-loop control.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：导航过程中，大脑如何将航向估计**迭代转化为运动指令**，从而实现对目标的连续控制？现有模型主要关注航向估计本身（如自我运动与地标线索的融合），但忽略了从估计到运动指令的闭环转化机制。
- **整体含义**：该研究提出导航是一个**闭环控制过程**，运动指令通过感觉预测误差不断更新。这为理解自然导航行为从“开环执行”转向“闭环迭代”提供了理论框架，有助于解释人类在动态环境中灵活调整运动的能力。

## 2. 方法论：核心思想、关键技术细节与流程
- **核心思想**：将导航转向行为建模为**联合估计航向与角速度的闭环动态系统**，其中运动指令由视觉预测误差持续修正。
- **关键技术细节**：
  - 开发**闭环状态空间模型**：将航向（heading）和角速度（angular velocity）作为随时间联合估计的状态变量。
  - **预测误差驱动**：当视觉地标在运动中被移动时，自我运动估计的预期航向与移位地标观察到的航向之间产生差异，该差异作为预测误差反馈到模型中，用于更新运动指令。
  - 模型既预测**最终位置（目的地）**，也预测**产生该位置的完整运动动态（旅程）**。
- **算法流程（文字说明）**：
  1. 初始化航向和角速度估计。
  2. 输入自我运动信号与地标视觉信号。
  3. 根据当前运动指令，生成下一步预期感觉（预期航向）。
  4. 对比实际感觉（地标提供的航向）与预期感觉，计算预测误差。
  5. 利用预测误差通过控制律更新运动指令（即加速度/角加速度）。
  6. 重复步骤2-5，形成闭环控制。

## 3. 实验设计
- **使用场景**：虚拟现实（VR）中的**目标导向旋转任务**。参与者需在VR环境中持续旋转到特定目标角度。
- **关键操纵**：在部分试验中，**视觉地标在运动过程中被突然移动**，从而在自我运动估计的航向与地标提供的航向之间诱导出**视觉预测误差**。
- **对比方法**：该研究主要与**开环模型（无预测误差反馈）** 进行对比，同时验证了闭环模型的预测（加速度在视觉反馈后快速变化，且误差越大纠正越大）。
- **Benchmark**：未明确提及标准基准数据集；实验以内省性能（模型预测与参与者真实行为定性对比）为主要验证方式。

## 4. 资源与算力
- 论文中**未明确说明**使用了何种GPU、数量或训练时长等算力信息。鉴于该研究为行为实验结合理论建模，可能未涉及大规模深度网络训练，主要依赖数学推导和虚拟现实行为数据拟合。

## 5. 实验数量与充分性
- **实验数量**：论文摘要中仅提及在虚拟现实中进行了**目标导向旋转任务**，并在地标移动条件下观察了参与者的加速度变化。具体试验次数、参与者数量未给出。
- **充分性评估**：
  - **优点**：通过操纵地标移动直接诱导预测误差，能够清晰检验闭环控制的核心预测（加速度快速变化与误差大小正相关）。
  - **不足**：缺乏定量模型拟合、不同参与者间的统计对比、以及更复杂导航场景（如平移、路径整合）的验证。实验规模有限，对外部效度的覆盖不足。
- **公平性**：未描述与现有导航模型的定量比较（如贝叶斯航向估计模型），仅做了定性对照，科学结论的稳健性依赖于进一步量化验证。

## 6. 主要结论与发现
- 参与者的转向行为与闭环模型动态**定性一致**：视觉反馈后加速度迅速发生变化，且**地标移动幅度越大，修正响应幅度也越大**。
- 结果支持假设：自然导航中的运动不是开环执行预先计算的指令，而是**通过闭环控制连续地将航向估计转化为运动指令**。
- 该模型首次同时预测了“旅程”（运动动态）和“目的地”（最终位置），超越了传统只预测终端状态的导航模型。

## 7. 优点
- **理论创新**：将控制论框架引入人类导航领域，弥补了从航向估计到运动指令转化环节的空白。
- **方法简洁有效**：通过简单的虚拟现实地标移动操纵，就能检验闭环控制的核心特征（预测误差驱动的快速纠正）。
- **动态预测能力**：模型不仅输出终点，还能刻画运动轨迹的实时变化，更具生态效度。

## 8. 不足与局限
- **实验覆盖有限**：仅考察了旋转任务，未涉及平移、路径规划、多目标等复杂场景。
- **量化验证不足**：缺乏正式的模型拟合（如贝叶斯对比、似然比检验）和误差分析，仅以“定性相似”作为结论依据，科学严谨性有待加强。
- **偏差风险**：未报告参与者人数、试次数量，可能存在小样本偏差；未进行跨被试的一致性统计。
- **应用限制**：模型假设线性动态和简单误差更新机制，可能不适用于非稳定环境或存在障碍物等复杂真实导航场景。
- **算力与实现细节缺失**：无法评估模型计算复杂度及可复现性。

（完）
