---
title: Multimodal Medical Code Tokenizer
title_zh: 多模态医学代码分词器
authors: "Xiaorui Su, Shvat Messica, Yepeng Huang, Ruth Johnson, Lukas Fesser, Shanghua Gao, Faryad Sahneh, Marinka Zitnik"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=UaTrcei5Ba"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 面向EHR代码的多模态分词器，改善代理对EHR的表示
tldr: 现有EHR分词器将医学代码视为孤立文本，忽略了代码的文本描述、本体层次和关联关系。本文提出MedTok多模态分词器，使用语言模型编码文本、图编码器建模关系结构，并量化融合两种模态。该分词器可生成高质量的医学代码表示，为基于EHR的医疗智能体提供重要的输入表示基础，助力下游任务的评估。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 591, \"height\": 678, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1547, \"height\": 808, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1662, \"height\": 435, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 875, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1499, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uatrcei5ba/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 522, \"height\": 638, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-uatrcei5ba/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uatrcei5ba/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 865, \"height\": 197, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uatrcei5ba/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1789, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uatrcei5ba/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1798, \"height\": 557, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uatrcei5ba/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 873, \"height\": 259, \"label\": \"Table\"}]"
motivation: 现有EHR分词器忽略代码的语义和结构信息，限制了下游模型性能。
method: 设计MedTok，结合语言模型和图编码器对代码的文本和关系进行多模态量化。
result: 在多个EHR下游任务中取得更优的代码表示和模型性能。
conclusion: 多模态代码分词可有效提升EHR表示质量，对医疗agent的构建和评估有重要支撑作用。
---

## Abstract
Foundation models trained on patient electronic health records (EHRs) require tokenizing medical data into sequences of discrete vocabulary items. Existing tokenizers treat medical codes from EHRs as isolated textual tokens. However, each medical code is defined by its textual description, its position in ontological hierarchies, and its relationships to other codes, such as disease co-occurrences and drug-treatment associations. Medical vocabularies contain more than 600,000 codes with critical information for clinical reasoning.  We introduce MedTok, a multimodal medical code tokenizer that uses the text descriptions and relational context of codes. MedTok processes text using a language model encoder and encodes the relational structure with a graph encoder. It then quantizes both modalities into a unified token space, preserving modality-specific and cross-modality information.  We integrate MedTok into five EHR models and evaluate it on operational and clinical tasks across in-patient and out-patient datasets, including outcome prediction, diagnosis classification, drug recommendation, and risk stratification. Swapping standard EHR tokenizers with MedTok improves AUPRC across all EHR models, by 4.10% on MIMIC-III, 4.78% on MIMIC-IV, and 11.32% on EHRShot, with the largest gains in drug recommendation. Beyond EHR modeling, we demonstrate using MedTok tokenizer with medical QA systems. Our results demonstrate the potential of MedTok as a unified tokenizer for medical codes, improving tokenization for medical foundation models.

---

## 论文详细总结（自动生成）

# 多模态医学代码分词器 (Multimodal Medical Code Tokenizer) —— 论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **背景**：电子健康记录（EHR）中的结构化数据通过标准医学代码（ICD-9/10、SNOMED CT、ATC等）表示诊断、手术、药物等。现有Transformer模型需要对这些医学代码进行分词，但传统分词器（如BERT的WordPiece）将每个代码视为孤立文本，忽略了代码的**文本定义**、**本体层次关系**（如ATC药物分类）以及**代码间的关联**（如疾病共现、药物-治疗关系）。
- **问题**：医学词汇超过60万代码，标准分词存在六方面挑战：词汇规模过大、丢失层次结构、跨系统代码冗余、存储效率低、低频代码表示稀疏、缺乏多模态（文本+图结构）信息。
- **整体含义**：需要一个能够同时利用代码文本描述和图结构关系的统一分词器，以提升下游临床预测和医疗基础模型的表现。

## 2. 方法论：核心思想、关键技术细节、流程

- **核心思想**：提出**MedTok**，一种多模态医学代码分词器。它基于**向量量化（VQ）** 框架，将每个医学代码的**文本描述**（通过语言模型编码）和**知识图谱子图**（通过图编码器编码）映射到共享的离散令牌空间，并保持模态特定和跨模态信息。
- **技术细节**：
  - **多模态编码**：  
    - 文本编码器（冻结的预训练语言模型）提取文本语义嵌入 \(\mathbf{x}_t\)。  
    - 图编码器（可训练GNN）抽取基于PrimeKG的子图，得到图级嵌入 \(\mathbf{x}_g\)。  
  - **特征投影**：通过线性层 \(f_t, f_g\) 将两种嵌入投影到共同维度 \(d\)，得到模态特定嵌入 \(\mathbf{e}_s^t, \mathbf{e}_s^g\)。  
  - **跨模态交互**：使用交叉注意力模块计算跨模态嵌入 \(\mathbf{e}_c^t, \mathbf{e}_c^g\)（如公式1、2）。  
  - **向量量化**：定义一个统一码本 \(\mathbf{C} \in \mathbb{R}^{N \times d}\)（含文本专用、图专用、共享三个区域）。对每个嵌入，选择与其欧氏距离最近的top-K码本向量作为令牌，并通过stop-gradient + 加权求和得到量化向量 \(\hat{\mathbf{e}}\)。  
  - **令牌打包损失**：包括码本损失 \(\mathcal{L}_C\)、KL散度损失 \(\mathcal{L}_{KL}\)（对齐模态间距离分布）、以及基于互信息的共享/特定信息优化损失 \(\mathcal{L}_{\text{token}}\)（公式6-9），最终联合训练。
- **流程**：  
  1. 输入医学代码 \(m\)，获取其文本描述和PrimeKG子图。  
  2. 通过编码器获得多模态嵌入，经量化和令牌打包生成离散令牌序列。  
  3. 下游模型（EHR模型或LLM）使用这些令牌作为输入。

## 3. 实验设计

- **数据集**：
  - **医学代码**：8个编码系统共617,490个代码（ICD-9、ICD-10-CM/PCS、SNOMED CT、ATC、NDC、CPT、RxNorm）。  
  - **EHR患者数据**：  
    - 住院数据集：MIMIC-III（35,707患者）、MIMIC-IV（123,488患者）。  
    - 门诊+住院数据集：EHRShot（6,739患者，长时序列）。  
  - **医疗QA数据集**：MMLU、MedDDx、AfrimedQA。
- **任务**：
  - 住院场景5个任务：死亡率预测（MT）、再入院预测（RA）、住院时长预测（LOS）、表型预测（Pheno）、药物推荐（DrugRec）。  
  - 门诊场景2个任务：运营结果（OO，含MT/RA/长LOS）、新诊断分配（ND，如高血压、高脂血症等）。  
  - 医疗QA：多项选择问答（三个数据集）。
- **对比方法**：
  - 分词器对比：BERT文本分词、VQGraph图分词。  
  - EHR模型基线：ETHOS、GT-BEHRT、MulT-EHR、TransformEHR、BEHRT。  
  - 医疗QA：LLaMA3.1-8B、Qwen2.5-7B、MMedLM。
- **评价指标**：主要采用AUPRC（因类别不平衡）；QA任务采用准确率。

## 4. 资源与算力

- **训练硬件**：  
  - MedTok预训练：4块NVIDIA H100 GPU。  
  - 所有下游实验：单块NVIDIA H100 GPU。  
- **训练参数**：  
  - 训练步数：3000步。  
  - 全局批次大小：1024。  
  - 量化向量维度：64。  
  - 文本编码器冻结，图编码器可训练。  
- **其他**：代码基于Python 3.9.19、PyTorch 2.3.1、Transformers 4.43.1。

## 5. 实验数量与充分性

- **实验组数**：  
  - 住院场景：5个任务 × 5个基线模型 × 2个数据集 → 约50组主要对比。  
  - 门诊场景：2个任务类型（含7个子任务）× 5个基线 → 约35组。  
  - 消融实验：模态消融（w/o text, w/o graph）和损失消融（不同损失组合）。  
  - 超参数敏感性：λ/β（0.01~0.5）、码本大小 N（3000~24000）。  
  - 医疗QA：3种LLM × 3个数据集，对比纯LLM与MedTok+LLM。  
  - 可解释性分析：分析了高脂血症高危患者的令牌频率。
- **充分性**：实验覆盖了多种数据集、任务和基线，并进行了充分的消融和敏感性分析，结果客观（多次重复并报告标准差）。对比方法（BERT、VQGraph）的选择合理。评估指标AUPRC适合不平衡数据。总体实验设计比较充分。

## 6. 主要结论与发现

- MedTok作为统一分词器，显著提升了EHR模型在各任务上的AUPRC：  
  - MIMIC-III：+4.10%，MIMIC-IV：+4.78%，EHRShot：+11.32%。  
  - 最大提升在药物推荐任务上（提示图结构信息的优势）。  
- 在医疗QA中，将MedTok令牌作为前缀与LLM结合，准确率提升2-10个百分点。  
- 消融表明：**文本和图模态都很重要**，图模态对药物推荐和新诊断检测更关键；**共享与特定信息优化**均有效。  
- 码本大小影响：住院数据集最优N=12000，门急诊长序列数据集最优N=24000。

## 7. 优点

- **多模态融合**：首次将文本与知识图谱子图结合用于医学代码分词，保留丰富信息。  
- **跨系统泛化**：通过统一码本和共享交互，可对齐不同编码系统的语义（如ICD与SNOMED）。  
- **即插即用**：可集成到任何需要医学代码分词的Transformer模型或LLM中。  
- **实验全面**：覆盖多种数据集、任务、基线和详细消融，验证了方法的鲁棒性。  
- **可解释性**：提供了令牌频率分析的定性验证，显示捕获了与预测疾病相关的医学概念。

## 8. 不足与局限

- **依赖图谱质量**：使用了PrimeKG，图谱的完整性和准确性影响效果；对于罕见或新代码，子图可能不充分。  
- **计算开销**：需要额外训练图编码器和多模态量化模块，预训练和推理成本高于传统分词。  
- **评价范围**：未在非英语编码系统（如中文ICD）或真实（非MIMIC）EHR系统上验证；可能对资源匮乏环境（低频代码）仍有挑战。  
- **QA实验有限**：仅在少数LLM和数据集上进行，且使用了前缀微调，未探索其他融合方式。  
- **偏差风险**：训练数据主要来自英美医疗系统（MIMIC、EHRShot），可能不直接推广到其他医疗体系。  
- **对比基线较弱**：主要对比了标准分词（BERT、VQGraph），但缺少与同样使用外部知识的模型（如GraphCare）在相同条件下的公平对比（因集成方式不同）。

（完）
