---
title: "SciCore-Omics: a tri-modal foundation model unifying histology, spatial transcriptomics and language for spatial biology"
title_zh: SciCore-Omics：一个统一组织学、空间转录组学和语言的三模态基础模型，用于空间生物学
authors: "Xiao, X., Li, Y., Zeng, Z., Yan, Y., Liu, Z., Xiang, Y., Ye, Z., Ying, J., Xie, L., He, F."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.30.728937v1.full.pdf"
tags: ["query:world-models"]
score: 8.0
evidence: 三模态基础模型用于空间生物学
tldr: "组织形态学与空间转录组学互补但难以对齐，现有基础模型仅双向连接。本文构建151,182个空间配对图像-基因-文本数据集，通过三阶段训练提出首个三模态模型SciCore-Omics。该模型在基因表达预测和空间域识别上相对最强基线提升23.6-80.9%，零样本病理分类平均准确率超越GPT-5达6.16个百分点。它实现了组织形态与分子状态的有效桥接，为计算病理学提供更通用可解释的基础模型。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基础模型仅能连接组织学、组学或语言中的两者，无法联合推断分子状态和解码空间组织。
method: "构建151,182个空间配对图像-基因-文本数据集，对SciCore-Omics进行三阶段渐进训练，实现三模态对齐。"
result: "基因表达预测和空间域识别上相对最强基线提升23.6-80.9%，零样本病理分类准确率超越GPT-5 6.16个百分点。"
conclusion: 首个三模态基础模型有效桥接组织形态与分子状态，为计算病理学提供更通用可解释的工具。
---

## 摘要
组织形态学和空间转录组学捕捉组织生物学的互补方面，但它们之间的关系在大规模尺度上仍然难以提取、对齐和解释。现有的基础模型通常仅成对连接组织学、组学或语言，这限制了它们联合推断分子状态、解码空间组织结构以及生成有生物学依据的解释的能力。在这里，我们展示了SciCore-Omics，这是第一个连接组织学图像、空间转录组学和生物语言的三模态基础模型。我们构建了一个空间配对的图像-基因-文本数据集，包含跨多个组织的151,182个点，并在该数据集上对SciCore-Omics进行了三阶段渐进式训练。在基因表达预测和空间域识别方面，SciCore-Omics在任务特定指标上比最强外部基线实现了23.6%至80.9%的相对提升。它还在组织病理学分类中展现出强大的零样本泛化能力，在四个基准测试的平均准确率上比GPT-5高出6.16个百分点。在10例乳腺癌病例中的专家评估证实了其仅基于H&E染色的病例级分子推理能力。总之，我们的方法表明，三模态框架能够有效地弥合组织形态学和分子状态之间的鸿沟，为计算病理学和组学分析提供了一个更通用、可解释性更强的基础模型。

## Abstract
Histomorphology and spatial transcriptomics capture complementary aspects of tissue biology, but their relationships remain difficult to extract, align, and interpret at scale. Existing foundation models typically connect histology, omics, or language only pairwise, which limits their capacity to jointly infer molecular states, decode spatial tissue organization, and generate biologically grounded explanations. Here, we show SciCore-Omics, the first tri-modal foundation model linking histology images, spatial transcriptomics, and biological language. We constructed a spatially paired image-gene-text dataset comprising 151,182 spots across multiple tissues and performed a three-stage progressive training of SciCore-Omics on this dataset. Across gene expression prediction and spatial domain recognition, SciCore-Omics achieved 23.6-80.9% relative gains in task-specific metrics over the strongest external baselines. It further showed robust zero-shot generalization in histopathology classification, outperforming GPT-5 by 6.16 percentage points in mean accuracy across four benchmarks. Expert evaluation in 10 breast cancer cases confirmed its H&E-only case-level molecular reasoning capability. Together, our method demonstrates that a tri-modal framework can effectively bridge histomorphology and molecular state, providing a more general and interpretable foundation model for computational pathology and omics analysis.

---

## 论文详细总结（自动生成）

# SciCore-Omics：统一组织学、空间转录组学和语言的三模态基础模型（详细总结）

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **背景**：组织形态学（H&E染色图像）和空间转录组学（基因表达+空间位置）是空间生物学中互补的两种模态，但两者之间的关系难以大规模提取、对齐和解释。
- **现状问题**：现有基础模型通常仅成对连接模态（组织学-语言、组学-语言、组织学-组学），缺乏一个统一的框架来联合推理分子状态、解码空间组织，并生成可解释的生物学描述。
- **论文目标**：提出**SciCore-Omics**——首个连接组织学图像、空间转录组学和生物语言的**三模态基础模型**，实现组织形态与分子状态的有效桥接。

## 2. 论文提出的方法论：核心思想、关键技术细节
### 核心思想
- 以**语言为中心**，将组织学图像和空间基因表达投影到共享的token空间，与文本token一起输入自回归语言模型（基于MiniCPM-V和Nicheformer）进行生成。
- 构建了**分子引导的语义配对**（molecularly grounded semantic pairing）管线：从每个空间点的基因表达、标志基因、富集通路和组织元数据自动生成结构化文本描述，形成图像-基因-文本三元组，无需人工标注。

### 三阶段渐进式训练
- **Stage I – 组织学-文本对齐**：使用约50.3万张病理图像和2852万条文本句子预训练视觉分支和语言骨干，学习病理视觉语义。
- **Stage II – 基因-文本对齐**：使用约5.16万个基因-文本配对，初始化基因编码器和投影模块，将转录组表示映射到语言语义空间。
- **Stage III – 三模态联合对齐**：使用15.1万个空间点（图像+基因+文本三元组）进行联合优化，支持图像、基因或两者同时输入。

### 关键技术组件
- **视觉编码器**：将H&E图像编码为64个视觉虚拟令牌。
- **基因编码器**（基于Nicheformer）：将基因表达谱通过Q-Former压缩为32个分子虚拟令牌，再经投影层映射到语言模型隐藏维度。
- **训练损失**：自回归语言建模损失 + 多模态对比损失（InfoNCE，跨图像-文本、基因-文本、图像-基因对）。
- **后续精炼**：轻量离线奖励加权强化学习（RL），提高输出格式规范性和证据一致性。

## 3. 实验设计：数据集、基准与对比方法
### 数据集与任务场景
| 任务 | 数据集/场景 | 规模 |
|------|-------------|------|
| 基因表达预测 | 人类正常心脏空间转录组（39个切片） | 使用top 50高表达基因，10折交叉验证 |
| 空间域识别 | 人类背外侧前额叶皮层DLPFC（12个切片） | 8训练/4测试，手动皮层层注释 |
| 零样本组织病理学分类 | MHIST（二分类）、BACH（四分类）、CRC100K（9类）、PatchCamelyon（二分类） | 共约44万张图像 |
| 病理视觉问答 | PathVQA（4,998图像，32,795问答对） | 细调后评估open/closed-ended |
| H&E病例级推理 | 10例乳腺癌病例（内部队列） | H&E全切片输入，Ki-67 IHC+报告仅用于专家评价 |

### 对比方法
- **基因表达预测**：OmiCLIP、Hist2ST、HisToGene、BLEEP。
- **空间域嵌入**：Nicheformer、Geneformer、scGPT、scVI、PCA。
- **零样本病理分类**：GPT-4o、GPT-5、PathGen-LLaVA、LLaVA-Med、Quilt-LLaVA。
- **多模态/问答**：LLaVA-Med、BioMedGPT、CellWhisperer、Cell2Sentence、MMQ、M2I2等。

## 4. 资源与算力
- **硬件**：8张 NVIDIA A800 GPU（每张40GB显存）。
- **训练超参数**：epoch=2，per-device batch size=1，gradient accumulation=16，learning rate=5e-4，cosine schedule，warmup ratio=0.1，weight decay=0.01，混合精度bfloat16。
- **模型参数**：总参数量约85亿（8.5B），包含语言骨干、视觉分支、Nicheformer基因编码器、Q-Former和投影层。
- **说明**：论文未披露总训练时长，仅提及checkpoint保存间隔2000步，日志间隔20步。

## 5. 实验数量与充分性
- **实验数量**：覆盖5大类任务（基因预测、空间域识别、零样本分类、病理VQA、病例推理），涉及7个以上公开数据集+内部队列。
- **消融分析**：
  - 三阶段训练效果（Stage I→II→III在基因到文本生成上的BLEU、ROUGE-L、BERTScore持续提升）。
  - 不同模态输入（图像only、基因only、图像+基因）在空间域识别和病例推理上的对比。
  - 冻结/微调视觉编码器对基因预测的影响。
- **公平性**：所有对比方法使用相同数据划分、基因集和预处理，使用官方实现或按相同协议重训。对于不支持某些输入输出设置的基线，在图中明确标注（灰色叉号）。
- **充分性评价**：实验设计系统、场景多样，但部分任务（如零样本仅4个数据集、病例推理仅10例）规模有限，整体上具有说服力但非大规模单一疾病闭环验证。

## 6. 论文的主要结论与发现
- **三模态对齐的有效性**：渐进式训练显著提升了转录组到语言生成的质量（BLEU-4从0.024提升至0.791，BERTScore从0.346提升至0.831）。
- **基因表达预测**：微调后平均PCC相对OmiCLIP提升23.6%，MSE降低15.8%，并能准确预测具有空间特异性的基因（如NPPA的r=0.82）。
- **空间域识别**：联合图像-基因嵌入的macro-F1达到0.850，相对最强外部基线（Nicheformer等）提升80.9%；预测的皮层分层结构与真实注释高度一致。
- **零样本分类**：在4个H&E基准上平均准确率56.46%，超越GPT-5（50.30%）和GPT-4o（45.36%）。
- **病理推理**：在10例乳腺癌病例中，专家评分最高（3.67/5），能基于H&E图像独立推理增殖状态，与独立IHC和报告一致。

## 7. 优点：方法或实验设计上的亮点
- **首次实现三模态统一生成框架**：在同一个自回归骨干中联合建模组织学、转录组和语言，相比成对模型更具泛化性。
- **无标注的语义配对策略**：利用空间转录组学自动生成结构化描述，避免了昂贵的人工标注，可扩展。
- **灵活的模态支持**：同一模型可在图像only、基因only或联合输入下工作，无需架构改变。
- **渐进式训练策略**：分阶段对齐各模态，避免灾难性遗忘，训练稳定。
- **多任务通用性**：从分子级预测到病例级推理覆盖多个生物学尺度，均在统一框架内完成。
- **可解释性**：生成自然语言描述，可揭示图像特征与分子程序的关联，增强生物学可信度。

## 8. 不足与局限
- **实验覆盖分散**：评估跨多个生物背景而非聚焦单一疾病，难以建立从分子到表型的闭环证据链。
- **训练语料精细度不足**：主要依赖组织类别和转录组衍生描述，缺乏细胞类型组成、病理亚型、临床行动标签等细粒度标注。
- **病例级推理仅限10例**：小样本、回顾性设计，不能代表临床验证；且内部队列未公开，限制了可复现性。
- **模型规模与部署**：8.5B参数较大，需高性能GPU，可能限制在资源受限环境中的使用。
- **对比方法未涵盖所有输入输出设置**：部分基线不支持某些模态组合（如Cell2Sentence无图像输入），但图中已透明标记。
- **预印本状态**：尚未经同行评审，部分结论可能随后续修订变化。

（完）
