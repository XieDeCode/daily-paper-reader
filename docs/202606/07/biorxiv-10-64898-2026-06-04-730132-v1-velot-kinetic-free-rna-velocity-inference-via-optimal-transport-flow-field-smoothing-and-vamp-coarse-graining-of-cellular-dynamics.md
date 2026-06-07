---
title: "VelOT: kinetic-free RNA velocity inference via optimal transport, flow-field smoothing, and VAMP coarse-graining of cellular dynamics"
title_zh: "VelOT: 通过最优传输、流场平滑和VAMP粗粒化细胞动力学的无动力学RNA速率推断"
authors: "Rincon de la Rosa, L., Perez Garcia, D., Alentorn, A."
date: 2026-06-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.730132v1.full.pdf"
tags: ["query:stm"]
score: 7.0
evidence: 时空窗口和流场平滑用于细胞动态推断
tldr: 针对单细胞RNA测序中剪接和非剪接计数稀疏不可靠时推断细胞动态困难的问题，提出无动力学假设的RNA速度框架VelOT。该方法通过扩散伪时间排序细胞，构建重叠时空窗口，用熵正则化最优传输估计位移向量，并经轻量神经流场平滑，最后以VAMP模块粗粒化得到软元状态和有向图。在四个真实基准和三个合成拓扑上，跨边界方向性和簇内一致性均优于scVelo、DeepVelo和FluxMatching，且计算高效。该工作将RNA速度重新定义为几何与传输问题，无需动力学建模即能恢复复杂分化轨迹。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有RNA速度方法依赖剪接动力学模型，在稀疏或不可靠数据下性能下降，亟需无动力学假设的替代方案。
method: 通过扩散伪时间排序细胞，构建重叠时空窗口，用熵正则化最优传输估计位移，并经神经流场平滑，最后利用VAMP粗粒化得到元状态和有向图。
result: 在四个真实和三个合成数据集上，VelOT在跨边界方向性和簇内一致性上显著优于scVelo、DeepVelo和FluxMatching。
conclusion: VelOT将RNA速度重新框架化为几何与传输问题，无需动力学假设即可恢复初始、终末、分支和循环状态，拓宽了应用场景。
---

## 摘要
当剪接和未剪接计数稀疏或不可靠时，从快照单细胞RNA测序推断细胞动力学仍然困难。我们提出VelOT，一种无动力学的RNA速率框架，将动力学公式化为基因表达流形上的局部最优传输。VelOT通过扩散伪时间对细胞排序，构建重叠的时空窗口，用熵正则化传输估计位移向量，并用轻量级神经流场对其进行平滑。下游基于VAMP的MetaFlow模块学习软元状态和类似PAGA的有向图，通过提交概率识别初始、终末、分支和循环状态。在四个真实基准和三个合成拓扑上，VelOT在跨边界方向性和簇内一致性方面优于scVelo、DeepVelo和FluxMatching，同时保持计算效率。在成人少突胶质细胞瘤scRNA-seq中，VelOT无需动力学输入即可恢复干细胞样到星形胶质细胞样和少突胶质细胞样的分化轴。VelOT将scRNA-seq中的RNA速率重新定义为不需要动力学建模的几何和传输问题。

## Abstract
Inferring cellular dynamics from snapshot single-cell RNA sequencing remains difficult when spliced and unspliced counts are sparse or unreliable. We present VelOT, a kinetic-free RNA velocity framework that formulates dynamics as local optimal transport on the gene-expression manifold. VelOT orders cells by diffusion pseudotime, constructs overlapping spatial-temporal windows, estimates displacement vectors with entropy-regularized transport, and smooths them with a lightweight neural flow field. A downstream VAMP-based MetaFlow module learns soft meta-states and a directed PAGA-like graph, identifying initial, terminal, branching, and cycling regimes with committor probabilities. Across four real benchmarks and three synthetic topologies, VelOT outperforms scVelo, DeepVelo, and FluxMatching in cross-boundary directionality and intra-cluster coherence while remaining computationally efficient. In adult oligodendroglioma scRNA-seq, VelOT recovers stem-like to astrocyte-like and oligodendrocyte-like differentiation axes without kinetic inputs. VelOT reframes RNA velocity within scRNA-seq as a geometry and transport problem that does not require kinetic modeling.