---
title: Neural networks learn forward dynamics when freed from numerical integration
title_zh: 神经网络在摆脱数值积分时学习正向动力学
authors: "Bahdasariants, S., Yakovenko, S."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.27.728310v1.full.pdf"
tags: ["query:world-models"]
score: 6.0
evidence: 学习前向动力学用于人机控制，类似世界模型
tldr: 人机界面机器学习预测肢体动态时，直接映射RNN存在数值不稳定性。本文提出人工物理引擎APE，将运动方程近似与时间数值积分分离。APE在外部扰动下保持低预测误差，而直接RNN产生大误差。通过因果物理结构提高鲁棒性，为器人/假肢控制提供新范式。
source: biorxiv
selection_source: fresh_fetch
motivation: 直接映射RNN在预测肢体动态时数值不稳定，需改进方法以实现鲁棒的人机交互。
method: 提出两阶段人工物理引擎APE，分别近似运动方程和进行数值积分，替代端到端映射。
result: APE在未训练的外部扰动下预测误差低且稳定，而直接RNN误差大且违反交互力矩。
conclusion: 分离动力学近似与积分可提升前向动态预测的鲁棒性，解决因果建模难题。
---

## 摘要
人与机器之间的无缝交互需要接口在面对生物信号和物理环境中固有的变异性时保持鲁棒性。先进的人机界面越来越依赖机器学习来预测或控制肢体动力学。这些系统必须学习控制变量与肢体状态之间的输入-输出映射，例如从作用于分段关节的肌肉力或关节扭矩到随时间变化的肢体姿态的映射。这种统计性的输入-输出转换可能导致预测的运动学与动力学数值不稳定。实现生物运动控制的鲁棒性需要同时解决正向和逆向动力学问题；然而，这些问题在计算上是不对称的，因为它们涉及相反的操作——积分与微分。由于我们之前已经证明，当训练神经网络在伸手过程中将运动学信号映射为动力学信号时，它能解决逆向动力学问题，因此我们假设，分别近似运动方程及其时间数值积分可能捕捉到正向动力学问题的相关计算结构。我们通过比较传统的直接映射递归神经网络与两阶段模型——人工物理引擎来检验这一假设。在预测受到训练中未遇到的外部扰动时，双段系统的状态时，直接映射的整体模型产生了与预期交互扭矩不一致的大预测误差，而人工物理引擎在初始条件和扰动下保持低误差且稳定。以运动方程的形式映射系统动力学，通过在人机界面设计中施加基于因果关系的物理结构，提高了对内在和外在变异性源的鲁棒性。

## Abstract
Seamless interaction between humans and machines requires interfaces that remain robust to the variability inherent in biological signals and physical environments. Advanced human-machine interfaces (HMIs) increasingly rely on machine learning to predict or control limb dynamics. These systems must learn input-to-output mappings between control variables and limb state, such as the mapping from muscle forces or joint torques acting about segmented arm joints to limb posture over time. Such statistical input-to-output transformations can result in numerical instability of predicted musculoskeletal kinematics and dynamics. Achieving the robustness of biological motor control requires solving both forward and inverse dynamics problems; however, these problems are computationally asymmetric because they entail opposing operations-integration and differentiation. Since we have previously shown that neural networks solve the inverse dynamics problem when trained to map kinematic to dynamic signals during reaching, we hypothesized that representing separately the approximation of equations of motion (EOM) and their temporal numerical integration may capture the relevant computational structure of the forward dynamics problem. We tested this hypothesis by comparing a conventional direct-mapping recurrent neural network (RNN) with a two-stage model, the artificial physics engine (APE). When predicting the state of a two-segment system under external perturbations not encountered during training, the direct-mapping, monolithic model produced large prediction errors inconsistent with the expected interaction torque, whereas the APE maintained low error and remained stable under novel initial conditions and perturbations. Mapping system dynamics in the terms of the EOM improves robustness against intrinsic and extrinsic sources of variability by imposing a causal, physics-based structure on HMI design.