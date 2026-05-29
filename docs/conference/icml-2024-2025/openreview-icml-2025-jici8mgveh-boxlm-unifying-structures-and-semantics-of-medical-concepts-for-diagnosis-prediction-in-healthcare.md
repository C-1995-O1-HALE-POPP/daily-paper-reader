---
title: "BoxLM: Unifying Structures and Semantics of Medical Concepts for Diagnosis Prediction in Healthcare"
title_zh: BoxLM：统一医学概念的结构和语义用于医疗诊断预测
authors: "Yanchao Tan, Hang Lv, Yunfei Zhan, Guofang Ma, Bo Xiong, Carl Yang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=jIci8mGVeh"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 使用电子健康记录进行医学概念表示和诊断预测
tldr: 现有基于语言模型的诊断预测方法未能充分利用医学概念的结构信息（如层次结构）。本文提出BoxLM框架，通过盒嵌入统一医学概念的结构与语义，融合本体驱动和EHR驱动的层次结构以及语言模型语义嵌入。实验表明，BoxLM在诊断预测任务上优于现有方法，并提供了可解释的医学概念表示，为构建基于EHR的医疗智能体提供了基础能力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jici8mgveh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 859, \"height\": 595, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jici8mgveh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1772, \"height\": 891, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jici8mgveh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1743, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jici8mgveh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1771, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jici8mgveh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1744, \"height\": 409, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 824, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1789, \"height\": 770, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 503, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 857, \"height\": 461, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1675, \"height\": 749, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1025, \"height\": 424, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1770, \"height\": 562, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jici8mgveh/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 774, \"height\": 379, \"label\": \"Table\"}]"
motivation: 现有方法无法充分捕获EHR中医学概念的层次结构，限制了诊断预测的准确性。
method: 提出BoxLM框架，利用盒嵌入机制融合本体层次和EHR驱动层次与语言模型语义。
result: 在诊断预测任务上取得优于基线的性能，同时提供可解释的概念表示。
conclusion: 统一医学概念结构和语义可提升诊断预测效果，为EHR驱动的医疗agent提供关键支持。
---

## Abstract
Language Models (LMs) have advanced diagnosis prediction by leveraging the semantic understanding of medical concepts in Electronic Health Records (EHRs). Despite these advancements, existing LM-based methods often fail to capture the structures of medical concepts (e.g., hierarchy structure from domain knowledge). In this paper, we propose BoxLM, a novel framework that unifies the structures and semantics of medical concepts for diagnosis prediction. Specifically, we propose a structure-semantic fusion mechanism via box embeddings, which integrates both ontology-driven and EHR-driven hierarchical structures with LM-based semantic embeddings, enabling interpretable medical concept representations.
Furthermore, in the box-aware diagnosis prediction module, an evolve-and-memorize patient box learning mechanism is proposed to model the temporal dynamics of patient visits, and a volume-based similarity measurement is proposed to enable accurate diagnosis prediction. Extensive experiments demonstrate that BoxLM consistently outperforms state-of-the-art baselines, especially achieving strong performance in few-shot learning scenarios, showcasing its practical utility in real-world clinical settings.

---

## 论文详细总结（自动生成）

# BoxLM 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：基于语言模型（LM）的诊断预测方法虽然能利用医学概念的语义信息，但普遍无法捕获医学概念的结构信息（如本体中的层次关系、电子健康记录（EHR）驱动的访问模式层次），导致预测精度受限。
- **整体含义**：现有方法使用点向量嵌入，只能建模相似性，不能体现包含/继承等复杂关系。例如，向量可以表示“高血压”和“心血管疾病”相似，但无法表达后者包含前者。BoxLM 通过盒嵌入（box embedding）统一结构表示和语义表示，提升诊断预测的准确性和可解释性，尤其在小样本场景下具有实用价值。

## 2. 方法论
### 核心思想
- 将医学概念（诊断、CCS代码）、患者访问、患者整体表示为高维超矩形（box），利用盒的相交、包含等几何运算来建模层次和语义关系，结合预训练语言模型（PLM）的语义嵌入和结构图卷积。

### 关键技术细节
- **结构-语义融合机制**：
  - **本体驱动层次建模**：使用 BioBERT 获取诊断和 CCS 代码的名称嵌入作为盒中心；通过关系图卷积网络（R-GCN）在医学概念层次图中聚合邻居信息，计算盒偏移（offset）。父概念偏移更大、子概念偏移更小，体现层次。
  - **EHR驱动层次建模**：每次患者访问视为一个盒，中心由注意力机制聚合关联诊断/CCS代码的盒中心得到；偏移取关联概念盒偏移的元素级最大值，反映访问内的多样性。
- **盒感知诊断预测模块**：
  - **演化-记忆患者盒学习**：患者盒中心由历史访问盒中心加权求和（权重由时间间隔经 MLP 归一化得到），患者盒偏移取历史访问盒偏移的最大值。这建模了患者病情的时间演化与结构记忆。
  - **基于体积的诊断预测**：患者盒与 CCS 代码盒的相似度用相交盒体积度量。为解决不相交时梯度消失问题，使用 GumbelBox 技巧（Gumbel 分布近似最大/最小操作），推导出体积的近似表达式（含 Bessel 函数和 softplus 近似）。预测采用二分类交叉熵损失。

## 3. 实验设计
- **数据集**：MIMIC-III（5449名患者，14141次访问，3874个诊断，285个CCS代码）和 MIMIC-IV（79393名患者，329597次访问，37917个诊断，842个CCS代码）。
- **基准/对比方法**：13种方法，分为三类：
  - 时间感知：DoctorAI、RETAIN、StageNet、TRANS
  - 层次感知：KAME、CGL、HiTANet、BoxCare
  - 语义感知：BERT、BERT*、BioBERT、BioBERT*、VecoCare（*表示使用了历史访问）
- **评价指标**：Visit-level Precision@k（P@k）、Code-level Accuracy@k（Acc@k）、Recall@k、Consistency@k（k=10,20）。
- **训练/验证/测试划分**：7:1:2，以患者为单位分层。5折交叉验证报告均值和标准差。

## 4. 资源与算力
- **文中说明**：所有实验使用两台 NVIDIA GTX 3090 Ti GPU。
- **运行时分析**：图3(c)和附录H展示了在 MIMIC-III 和 MIMIC-IV 上不同训练数据比例下的训练时间，BoxLM 比 RETAIN、TRANS 和 BoxCare 更高效（平均比 BoxCare 低 36.57% 和 33.48%）。
- **未明确信息**：未报告总训练时长、单个 epoch 时间或具体硬件配置除 GPU 外的细节。评估阶段算力也未提及。

## 5. 实验数量与充分性
- **实验组数**：
  - 主要诊断预测结果（5%训练数据）在 MIMIC-III 和 MIMIC-IV 上各报道了 P@10/20、Acc@10/20。
  - 不同训练数据比例（1%、5%、10%、15%、50%、100%）在 MIMIC-III 上实验，并在 MIMIC-IV 上补充了 1%-15% 的结果。
  - 消融实验：Base → +Onto → +EHR → BoxLM，在两个数据集上均进行。
  - 超参数研究：维度 dim（4/8/16/32）、Gumbel 尺度 β（0.1-0.6）、体积计算方法对比（Bessel vs. Soft）。
  - 案例研究：展示一个实际病人预测对比（BoxCare 与 BoxLM）。
  - 可解释性度量：Consistency@k 在 MIMIC-IV 上对比 RETAIN、TRANS、BoxCare。
  - 附录还给出了 Recall@k 结果。
- **充分性与公平性**：对比方法覆盖三大范式，采用 5 折交叉验证，报告均值和标准差，超参数按原论文调优。实验设计较为全面，消融各部分验证了每个组件的贡献。但未进行统计显著性检验（如 t-test），不过标准差较小。

## 6. 主要结论与发现
- BoxLM 在所有评价指标上一致优于 13 种基线方法。
- 在小样本场景（5%训练数据）下，BoxLM 在 MIMIC-III 上 P@10 达 43.88%，比第二名 BoxCare（38.21%）提升 14.84%；在 MIMIC-IV 上提升 19.67%。
- 随着训练数据比例增加，BoxLM 性能稳步提升，且使用 15% 数据即可超过基线使用 100% 数据的效果。
- 消融实验证实：本体驱动层次（+Onto）、EHR 驱动层次（+EHR）、演化-记忆机制均对性能有显著贡献，且对大型数据集（MIMIC-IV）增益更明显。
- 可解释性：Consistency@k 度量表明 BoxLM 预测更符合医学层次结构，案例研究展示了模型能捕获临床关联（如高血压→冠心病）。

## 7. 优点
- **方法创新**：首次将盒嵌入同时用于本体层次和 EHR 驱动层次的统一建模，结合 PLM 语义，实现结构和语义的联合表示。
- **技术细节**：提出演化-记忆患者盒机制（时间加权中心+最大偏移）和 Gumbel 体积计算（解决梯度消失）具有实用性。
- **实验全面**：覆盖多个数据集、多种基线、多种数据比例、消融、超参数、案例和可解释性量化。
- **效率**：相比同类层次方法（BoxCare）和 RNN/Transformer 方法训练更快，尤其在大数据集上优势明显。
- **可解释性**：盒的几何直观性提供了可解释的预测过程，Consistency 指标验证了层次一致性。

## 8. 不足与局限
- **定义依赖**：方法依赖预定义的本体层次（如 ICD/CCS 树）和 EHR 驱动层次（访问-诊断关联），在缺乏结构化本体或访问记录稀疏时可能受限。
- **实验覆盖**：仅评估了诊断预测任务，未在用药推荐、预后预测等其他医疗任务上验证泛化性。
- **数据集偏差**：MIMIC 系列来自 ICU 患者，可能无法代表普通门诊或急诊场景，存在选择偏差。
- **可迁移性**：未讨论跨医院或跨系统 EHR 的适用性，本体映射和语义嵌入可能需重新适配。
- **未见对大规模语言模型（LLM）的比较**：2025 年已有众多医疗 LLM，论文未评估 LLM 作为预测模型或特征提取器的效果。
- **未报告统计显著性**：虽有均值与标准差，但未提供显著性检验（如 p 值）来确认提升的统计可靠性。
- **应用限制**：作为决策辅助工具，实际临床部署前需进行前瞻性验证和公平性评估，论文未涉及。

（完）
