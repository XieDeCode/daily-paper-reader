---
title: "CellOS: Learning a World Model of Cellular State through Joint Embedding Prediction"
title_zh: CellOS：通过联合嵌入预测学习细胞状态的世界模型
authors: "Zhou, Q., Le, Y., Qi, X., Chang, S., Lu, H., Wu, Y., Wang, H., Ran, R., li, x."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733163v1.full.pdf"
tags: ["query:world-models"]
score: 9.0
evidence: 通过联合嵌入预测学习细胞状态的世界模型
tldr: 现有单细胞基础模型多从单一基因表达视图学习，难以整合互补的细胞状态信息。CellOS提出多视角框架，结合表达和感知视图，通过因果语言建模、混合专家扩展和LLM-JEPA潜在空间对齐的三阶段训练，在3.9亿细胞上训练120亿参数模型。在细胞注释、批次整合和扰动预测等任务上超越现有模型。该工作为构建可迁移的表示中心细胞世界模型和AI虚拟细胞提供了可扩展路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有单细胞模型仅从单一视图学习，无法整合互补的细胞状态信息。
method: CellOS通过三阶段策略整合表达与感知视图：因果语言建模、混合专家扩展、LLM-JEPA对齐。
result: 120亿参数模型在3.9亿细胞上训练，在多项基准上超越现有单细胞基础模型。
conclusion: 互补视图的预测对齐为构建可迁移的AI虚拟细胞提供了可扩展路径。
---

## 摘要
从单细胞转录组中学习的基础模型是AI虚拟细胞（能够表示、查询和预测细胞状态）前景的核心。然而，当前大多数单细胞基础模型仅从基因表达单一视角学习，并主要通过重建或下一个标记预测进行优化。因此，它们捕获了表达丰度，但无法显式地调和细胞状态的互补视图。在此，我们提出CellOS，一个多视角基础模型，它从配对的表达和感知视角学习细胞表示。CellOS通过可扩展的三阶段训练策略整合互补视图，该策略结合了因果细胞句子语言建模、功能保持的密集到混合专家扩展以及通过LLM-JEPA目标的潜在空间对齐。利用这一框架，我们在3.905亿个单细胞转录组上训练了一个120亿参数的模型。在涵盖细胞状态注释、批次整合和扰动响应预测的多个基准测试中，CellOS始终优于最先进的单细胞基础模型。这些结果共同表明，互补细胞视图之间的预测对齐为以表示为中心的细胞世界模型和可迁移的AI虚拟细胞提供了一条可扩展的路径。

## Abstract
Foundation models learned from single-cell transcriptomes are central to the prospect of AI virtual cell that can represent, query and predict cellular state. However, most current single-cell foundation models learn from a single view of gene expression and are optimized primarily through reconstruction or next-token prediction. As a result, they capture expression abundance but cannot explicitly reconcile complementary views of cellular state. Here we present CellOS, a multi-view foundation model that learns cellular representations from paired expression and perception views. CellOS integrates complementary views through a scalable three-stage training strategy that combines causal cell-sentence language modelling, function-preserving dense-to-mixture-of-experts expansion and latent-space alignment via an LLM-JEPA objective. Using this framework, we trained a 12-billion-parameter model on 390.5 million single-cell transcriptomes. Across diverse benchmarks spanning cell-state annotation, batch integration and perturbation-response prediction, CellOS consistently outperformed state-of-the-art single-cell foundation models. Together, these results suggest that predictive alignment between complementary cellular views provides a scalable path toward representation-centric cellular world models and transferable AI virtual cells.

---

## 论文详细总结（自动生成）

# CellOS 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

**核心问题**：现有单细胞基础模型大多只从单一基因表达视图（如表达丰度排序）学习，通过重建或下一个标记预测优化，无法显式整合互补的细胞状态信息。例如，高表达管家基因可能携带较少状态特异性信息，而低表达但稀有基因可能对识别罕见状态至关重要。单一视图无法同时捕捉“细胞表达什么”和“哪些表达事件在群体中最具信息量”。

**整体含义**：CellOS提出一种多视图基础模型，将每个转录组表示为两个互补视图——**表达视图**（按表达丰度排序）和**感知视图**（按群体相对信息含量排序），并通过联合嵌入预测架构（LLM-JEPA）对齐两者的潜在表示，从而学习更鲁棒、可迁移的细胞状态表示，为构建AI虚拟细胞和细胞世界模型提供可扩展路径。

## 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：将每个细胞视为一个“细胞句子”，但使用两种不同的排序标准生成两个句子；然后通过三阶段训练，结合因果语言建模、稀疏混合专家（MoE）扩展和跨视图潜在对齐，学习统一的细胞表示。

**关键技术细节**：

- **双视图构建**：
  - **表达视图**：将基因按标准化表达值（每百万转录本计数）降序排列，得到序列 \( S_{expr}^c = (g_{(1)}, g_{(2)}, ..., g_{(n)}) \)。
  - **感知视图**：基于群体中每个基因的非零表达值的经验分位数，计算感知信息得分 \( I_{cg} = -\log(1 - q_g(e_{cg}) + \epsilon) \)，然后将基因按该得分降序排列，得到 \( S_{perc}^c \)。该得分反映该基因的表达值在自身全局分布中处于多高的上尾区域，值越大越意外。

- **三阶段训练策略**：
  1. **阶段一**：使用密集Transformer在表达视图上进行因果语言模型预训练，学习细胞表达语法。
  2. **阶段二**：通过**功能保持的密集到MoE转换**：将密集前馈权重初始化为一个共享专家，引入32个路由专家（近零初始化），路由器近均匀初始化；然后继续在表达视图上预训练，结合MoE辅助损失。
  3. **阶段三**：引入感知视图，使用LLM-JEPA目标：共享编码器分别处理两个视图，从表达视图的表示标记隐状态通过预测器映射到感知视图的表示空间，使用余弦距离作为JEPA对齐损失；同时保留因果语言建模损失。总损失为 \( L = \lambda_{LM} L_{LM} + \lambda_{JEPA} L_{JEPA} + \lambda_{MoE} L_{aux} \)。

- **模型架构**：共享的仅解码器因果Transformer，包含一个专用的表示标记。MoE层每层一个共享专家+32个路由专家，采用top-1路由。

## 3. 实验设计：数据集、基准、对比方法

- **数据集**：
  - **注释基准**：6个数据集——PBMC免疫衰老、iPSC细胞类型分化、iPSC分化时间序列、T细胞亚群、人肺、IFN-β刺激的PBMC。
  - **批次整合基准**：2个数据集——人肺图谱、嗅周皮层。
  - **扰动响应预测**：5个细胞环境——H1、HepG2、Jurkat、K562、RPE1（来自Perturb-seq数据）。

- **基准**：
  - 注释：使用调整兰德指数（ARI）、归一化互信息（NMI）、平均轮廓宽度（ASW），先按数据集归一化再平均得到生物保守分数。
  - 批次整合：使用轮廓批次分数（sil_batch）、图连通性（GC）、iLISI，平均得到批次效应分数。
  - 扰动预测：使用DE Spearman、皮尔逊edist、聚类一致性、DE方向匹配、Pearson Δ。

- **对比方法**：UCE、State、scGPT、TranscriptFormer、STACK、C2S（C2S-2B），共6种代表性基础模型。

## 4. 资源与算力

论文未明确说明训练CellOS 12B模型所使用的GPU型号、数量及训练时长。仅提及在3.905亿个单细胞转录组、47845个样本上训练。但通过模型参数规模（12B）可以推断需要大量计算资源。文中提到使用了“token-balanced data engine”进行分布式训练，但具体硬件细节缺失。

## 5. 实验数量与充分性

- **实验数量**：注释基准6个数据集+批次整合2个数据集+扰动预测5个场景，共13组对比实验。另外在T细胞亚群上进行了消融实验，比较0.2B、2B单视图预训练和12B多视图JEPA三个检查点。
- **充分性与公平性**：
  - 对比了6种主流基础模型，且扰动预测任务中所有方法使用相同的下游过渡模型，仅替换嵌入，保证了公平比较。
  - 指标覆盖全面（聚类、分离、批混合、扰动DE恢复、转录组距离等）。
  - 消融实验验证了规模和多视图对齐的贡献。
  - 但缺乏与更简单基线（如线性模型）的对比（在扰动预测中已有相对比较）；批次整合实验仅2个数据集，规模有限。评估集主要来自人类，未见跨物种或跨模态验证。

## 6. 论文的主要结论与发现

- CellOS在注释综合基准中取得最高生物保守分数（0.792），显著优于所有对比模型。
- 在批次整合中达到最高图连通性（0.964），批次效应分数第二（0.771），平衡了生物保守与批混合。
- 在扰动预测中整体排名第一，在DE Spearman、Pearson edist和聚类一致性上最优，表明其表示捕捉了静态细胞类型和状态转变相关信息。
- 消融实验显示：从0.2B到12B，ARI提升36%、NMI提升19%；多视图JEPA对齐带来额外收益（从2B到12B，ΔARI=+0.042），表明规模和对齐均有益。
- 结论：互补视图的预测对齐为构建可迁移的表示中心细胞世界模型提供了可扩展路径。

## 7. 优点：方法或实验设计亮点

- **新颖的多视图设计**：首次将群体相对信息含量作为独立视图，将信息论原则显式融入表示学习，而非隐藏于单一排序中。
- **LLM-JEPA到单细胞领域的首度应用**：避免了重建具体排序，而是对齐潜在表示，强调语义结构。
- **功能保持的密集到MoE转换**：在不破坏预训练知识的前提下扩展模型容量，支持平稳继续训练。
- **三阶段渐进式训练**：先学表达语法，再扩容量，最后引入多视图对齐，逻辑清晰。
- **扰动预测的公平比较**：采用共享下游模型，仅替换嵌入，直接评估表示质量。
- **模型规模大**：12B参数使其成为最大的单细胞基础模型之一，展示了可扩展性。

## 8. 不足与局限（包括实验覆盖、偏差风险、应用限制）

- **感知视图的局限性**：当前感知视图基于整个预训练语料的全局经验分位数，未区分组织、谱系或条件特异性背景，可能丢失上下文依赖信息。
- **仅使用转录组数据**：未整合染色质可及性、蛋白质丰度、空间信息、扰动读数等，限制了多模态表示能力。
- **缺乏因果建模**：JEPA对齐仅促进表示稳定性，并不直接学习因果机制；扰动预测需依赖独立下游模型。
- **实验覆盖有限**：批次整合仅2个数据集，数量偏少；注释数据集主要为人，未涉及跨物种或大量疾病状态；未在更基础的定值任务（如基因调控关系推断）上评估。
- **资源信息缺失**：未公开训练所需GPU型号、数量及时间，不利于复现和资源评估。
- **未见与更简单的线性基线系统对比**：在扰动预测中已有STATE框架的对比，但未体现如Ahlmann-Eltze等人指出的“深度模型不总优于线性基线”的问题。

（完）
