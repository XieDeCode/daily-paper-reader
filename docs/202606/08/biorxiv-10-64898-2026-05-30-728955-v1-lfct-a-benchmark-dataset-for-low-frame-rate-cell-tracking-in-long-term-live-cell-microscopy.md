---
title: "LFCT: A Benchmark Dataset for Low-Frame-Rate Cell Tracking in Long-Term Live-Cell Microscopy"
title_zh: LFCT：长期活细胞显微成像中低帧率细胞跟踪的基准数据集
authors: "Gachloo, M., Biswas, T., Lu, X., Greene, C. M., Hargett, C. K., Simancik, K. R., Birtwistle, M. R., Iuricich, F."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.30.728955v1.full.pdf"
tags: ["query:stm"]
score: 6.0
evidence: 低帧率细胞追踪数据集，支持时空数据分析
tldr: 现有细胞追踪基准多针对高帧率成像，低帧率下细胞运动大、追踪困难。为此，提出低帧率细胞追踪数据集LCFT，包含4种人类细胞系的多日活细胞显微镜序列，结合自动化分割追踪与人工校对生成精确标注。数据集提供了细胞识别、时序链接、谱系关系和有丝分裂事件标注。该基准有助于开发鲁棒的细胞追踪算法，支持处理稀疏时间采样和大帧间运动的长时成像实验。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基准缺乏低帧率条件下的细胞追踪数据，无法评估算法在稀疏时间采样和大运动场景下的性能。
method: 收集多日活细胞显微镜序列，结合自动化分割追踪与人工校对生成精确标注。
result: 构建了包含4种细胞系、多倍率成像的低帧率细胞追踪标注数据集。
conclusion: 该数据集为开发鲁棒的细胞追踪算法提供了重要基准，推动了长时低帧率成像的生物动态研究。
---

## 摘要
延时显微成像中的细胞跟踪对于研究动态生物过程（如迁移、增殖和谱系形成）至关重要。现有基准数据集主要关注高帧率成像，其中短时间间隔简化了连续帧间细胞对应的建立。我们提出了低帧率细胞跟踪数据集（LCFT），这是一个专门用于评估低帧率条件下细胞跟踪方法的基准数据集。该数据集包含来自四种人类细胞系（MCF10A、MDA-MB-231、HEK293T和U87）的多日活细胞显微成像序列，使用相差和荧光成像（细胞核）以10倍和20倍放大倍数获取。真实标注包括细胞识别、时间链接、谱系关系和有丝分裂事件。为了生成可靠的标注，自动分割和跟踪与广泛的人工校正相结合。LCFT为开发和基准测试能够处理长期活细胞成像实验中稀疏时间采样和大帧间运动的稳健细胞跟踪算法提供了全面资源。

## Abstract
Cell tracking in time-lapse microscopy is essential for studying dynamic biological processes such as migration, proliferation, and lineage formation. Existing benchmarks primarily focus on high-framerate imaging, where short temporal intervals simplify correspondence between cells across consecutive frames. We present the Low Frame-rate Cell Tracking dataset (LCFT), a benchmark dataset designed specifically for evaluating cell tracking methods under low-frame-rate conditions. The dataset contains multi-day live-cell microscopy sequences from four human cell lines (MCF10A, MDA-MB-231, HEK293T, and U87), acquired at 10x and 20x magnifications using phase-contrast and fluorescence imaging (nucleus). Ground-truth annotations include cell identifications, temporal linking, lineage relationships, and mitosis events. To generate reliable annotations, automated segmentation and tracking were combined with extensive manual curation. LCFT provides a comprehensive resource for developing and benchmarking robust cell tracking algorithms capable of handling sparse temporal sampling and large inter-frame motion in long-term live-cell imaging experiments.