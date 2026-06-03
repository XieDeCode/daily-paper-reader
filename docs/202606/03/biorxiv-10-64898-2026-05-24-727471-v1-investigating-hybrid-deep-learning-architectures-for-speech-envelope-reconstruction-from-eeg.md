---
title: Investigating Hybrid Deep Learning Architectures for Speech Envelope Reconstruction from EEG
title_zh: 基于EEG的语音包络重建的混合深度学习架构研究
authors: "Gottipalli, U. S., Jha, A., Miyapuram, K. P."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.24.727471v1.full.pdf"
tags: ["query:world-models"]
score: 7.0
evidence: 使用混合深度学习分析EEG时空模式
tldr: 针对基于EEG的语音包络重建任务，现有深度学习模型多局限于单层架构，难以充分捕捉时空与结构模式。本研究在VLAAI框架下系统评估了26种混合架构，融合CNN、LSTM和GCN。实验表明CNN仍是最强单模型，但CNN-LSTM和CNN-GCN-LSTM等混合设计达到竞争或更优性能，强调了空间、时序与图处理的结合。这是首个混合模型大规模比较分析，推动了非侵入性语音解码BCI的发展。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有深度学习重建EEG语音包络的方法多采用单层架构，无法捕获复杂时空与结构模式，需探索混合架构。
method: 在VLAAI框架下，系统评估26种集成CNN、LSTM和GCN的单层及混合架构，基于SparrKULee数据集实验。
result: CNN仍是最强单模型，但CNN-LSTM和CNN-GCN-LSTM混合架构达到竞争或更优性能，验证了混合设计的优势。
conclusion: 结合空间、时序与图处理的混合架构提升重建性能，为混合设计提供实践指导，促进非侵入性语音解码BCI发展。
---

## 摘要
从脑电图信号中重建语音包络是一项具有挑战性但有价值的脑机接口任务，在言语障碍患者的辅助沟通中具有应用前景。虽然深度学习提高了重建精度，但现有方法大多局限于单层架构（如卷积神经网络），这限制了其捕捉脑电图时空和结构模式完整复杂性的能力。在本工作中，我们系统性地扩展了VLAAI框架，评估了26种架构，这些架构以单层和混合配置集成了卷积神经网络、长短期记忆网络和图卷积网络。在64通道SparKULee数据集上的实验表明，CNN仍然是最强的独立模型，但混合设计（尤其是CNN-LSTM和CNN-GCN-LSTM）达到了具有竞争力或更优的性能。这些结果凸显了结合空间、时序和基于图的处理的重要性，并为混合架构设计提供了实用指南。我们的研究首次对基于脑电图的语音包络重建的混合模型进行了大规模比较分析，推动了用于非侵入式语音解码的鲁棒脑机接口系统的发展。

## Abstract
Reconstructing speech envelopes from electroen-cephalography (EEG) signals is a challenging but valuable task for brain-computer interfaces (BCIs), with applications in assistive communication for individuals with speech impairments. While deep learning has improved reconstruction accuracy, most existing approaches are restricted to single-layer architectures such as convolutional neural networks (CNNs). This limits their ability to capture the full complexity of spatio-temporal and structural EEG patterns. In this work, we systematically extend the VLAAI framework by evaluating 26 architectures that integrate CNNs, long short-term memory networks (LSTMs), and graph convolutional networks (GCNs) in both single-layer and hybrid configurations. Experiments on the 64-channel Spar-rKULee dataset demonstrate that CNNs remain the strongest standalone models, but hybrid designs--particularly CNN-LSTM and CNN-GCN-LSTM--achieve competitive or superior performance. These results highlight the importance of combining spatial, temporal, and graph-based processing, and provide practical guidelines for hybrid architecture design. Our study offers the first large-scale comparative analysis of hybrid models for EEG-based speech envelope reconstruction, advancing robust BCI systems for non-invasive speech decoding.