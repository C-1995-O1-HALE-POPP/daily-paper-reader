---
title: "What Limits Virtual Agent Application? OmniBench: A Scalable Multi-Dimensional Benchmark for Essential Virtual Agent Capabilities"
title_zh: 什么限制了虚拟智能体的应用？OmniBench：一个可扩展的虚拟智能体基本能力多维基准
authors: "Wendong Bu, Yang Wu, Qifan Yu, Minghe Gao, Bingchen Miao, Zhenkui Zhang, Kaihang Pan, liyunfei, Mengze Li, Wei Ji, Juncheng Li, Siliang Tang, Yueting Zhuang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=4tFSKOY2mT"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 虚拟智能体能力基准
tldr: 现有虚拟智能体基准存在任务复杂度不可控、人工标注多、缺乏多维评估等问题。为此提出OmniBench，一个自生成的基于图的基准，通过子任务组合合成可控复杂度的任务，并配套OmniEval多维评估框架。该工作为通用智能体评估提供了方法论参考，但未涉及医疗或EHR场景。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1757, \"height\": 1123, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1747, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 981, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 843, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 829, \"height\": 457, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 859, \"height\": 598, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 859, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 845, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4tfskoy2mt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 866, \"height\": 570, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1779, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 862, \"height\": 202, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 858, \"height\": 197, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 754, \"height\": 830, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1771, \"height\": 858, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1775, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 854, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 866, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 863, \"height\": 468, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 857, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 858, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4tfskoy2mt/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 856, \"height\": 292, \"label\": \"Table\"}]"
motivation: 现有虚拟智能体基准在任务复杂度控制和多维评估方面存在局限，需要更通用的评估方法。
method: 提出OmniBench，一个基于图的自动生成基准，通过子任务组合合成可控复杂度的任务，并设计OmniEval多维评估框架。
result: OmniBench能够生成多样化的任务，并提供包括子任务级评估和图指标的全面评价。
conclusion: 该工作为虚拟智能体评估提供了可扩展、多维度的基准方案，可启发医疗智能体评估方法的设计。
---

## Abstract
As multimodal large language models (MLLMs) advance, MLLM-based virtual agents have demonstrated remarkable performance. However, existing benchmarks face significant limitations, including uncontrollable task complexity, extensive manual annotation, and a lack of multidimensional evaluation. In response to these challenges, we introduce OmniBench, a self-generating, graph-based benchmark with an automated pipeline for synthesizing tasks of controllable complexity through subtask composition. To evaluate the diverse capabilities of virtual agents on the graph, we further present OmniEval, a multidimensional evaluation framework that includes subtask-level evaluation, graph-based metrics, and comprehensive tests across 10 capabilities. Our synthesized dataset contains 36k graph-structured tasks across 20 scenarios, achieving a 91% human acceptance rate. Training on our graph-structured data shows that it improves generalization across environments. We conduct multidimensional evaluations for virtual agents, revealing their performance across various capabilities and paving the way for future advancements. Our project is available at https://omni-bench.github.io.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

现有基于多模态大语言模型（MLLM）的虚拟智能体在 web 导航、移动设备控制等任务上表现出色，但已有的评估基准存在三大核心局限：
- **任务复杂度不可控且固定**：现有基准以整体任务形式提出，缺乏细粒度引导，无法针对不同能力设计测试数据，也难以跟随智能体能力增长而扩展。
- **大量人工标注、场景有限**：依赖人工合成示范轨迹或评估函数，成本高昂且规模受限，难以覆盖多样化场景。
- **缺乏多维评估**：通常仅基于最终状态（结果导向）或与人类示范的轨迹相似性，忽略了中间步骤和多种能力（如规划、指令理解、决策等）的量化评价。

论文的核心动机是：**构建一个成本低廉、可扩展、复杂度可控、支持多维度评估的虚拟智能体基准**，以全面揭示现有智能体的能力边界与改进方向。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心思想
- **基于图的任务表示**：每个任务表示为一个有向无环图（DAG），节点是子任务（subtask），边表示依赖关系。子任务通过输入/输出资源连接。
- **自底向上的自动任务合成管道**：从子任务发现开始，逐步合成轨迹和评估函数，再通过资源匹配和意图约束组合成任务图，最后验证指令与图语义一致。
- **五维任务复杂度**：在图上定义依赖复杂度（边数）、指令复杂度（节点数）、知识复杂度（应用类别数）、层级复杂度（深度）、分支复杂度（宽度）。每个维度分 Easy/Medium/Hard 三级。
- **多维评估框架 OmniEval**：基于图评估器，提出覆盖率（Coverage Rate, CR）和逻辑一致性（Logical Consistency, LC）两个新指标，并构建 10 种能力（如并行规划、长程规划、跨领域决策等）的测试任务集。

### 2.2 关键技术细节与流程

**阶段1：子任务合成（Subtask Synthesis）**
- **子任务探索**：使用先进 MLLM 在含 49 个应用的虚拟环境中自动探索并生成子任务（包括指令模板、输入输出资源列表）。
- **迭代合成**：MLLM 合成子任务的轨迹（含截图、动作、思考链），Code LLM 用预定义的 11 个系统级 API 合成评估函数。引入**交叉验证**算法：循环迭代验证轨迹与评估函数的正确性，基于失败反馈优化。

**阶段2：任务合成（Task Synthesis）**
- **任务组合**：从子任务池中提取任务意图（如“为 Emily 创建自我介绍 PPT”），将相关子任务按资源依赖组合成 DAG。通过意图提取避免无意义组合（如打开食物APP后又关闭）。
- **任务验证**：使用 GPT-4o 根据子任务指令和 DAG 结构生成任务指令，再通过**一致性验证器**检查指令推断出的依赖是否与真实 DAG 匹配，若不匹配则重新生成。

**质量控制**：交叉验证、意图提取、一致性验证三个模块联合将人类接受率从 41.2% 提升至 90.7%（表3）。

**评估指标**：
- **覆盖率（CR）**：按子任务深度加权，越深的子任务权重越大，衡量智能体在任务图上的整体进展。
- **逻辑一致性（LC）**：衡量智能体操作序列与应用切换的相似性，即智能体是否像人类一样优先完成同一应用内的子任务再切换应用，基于可排序序列的最大逻辑一致性计算。

## 3. 实验设计

### 3.1 数据集与场景
- **OmniBench 数据集**：共 36,076 个图结构任务，覆盖 20 个实际交互场景（如办公、网页浏览、创意编辑等），涉及 49 个应用。任务平均使用 2.21 个应用，每个高级指令平均 51.7 词。
- **额外基准数据集**：AndroidControl（手机端）、OmniAct（桌面和 web 端）用于迁移评估。

### 3.2 基准（Baselines）
- **闭源 MLLMs**：GPT-4o、Qwen-VL-Max、Claude-3.5-Sonnet、Gemini-2.0-Flash
- **开源 MLLMs**：Qwen2-VL-7B、InternVL2-8B、InternVL2.5-8B
- **视觉数字智能体**：Aguvis-7B、OS-Atlas-Pro-4B、ShowUI-2B*、OS-Atlas-Base-4B*、UGround-V1-7B*（带 * 表示使用 GPT-4o 作为规划器）
- **监督微调智能体（本文）**：Omni-OS-Atlas-Base-4B、Omni-UGround-V1-7B（在 OmniBench 数据上微调）

### 3.3 实验内容
1. **主实验**：对比 12 个模型在 10 个能力维度上的 CR 和 LC 分数（表4）。
2. **复杂度级别性能下降分析**：观察各模型在 Easy/Medium/Hard 任务上的性能下降幅度（表5）。
3. **图结构 vs 链结构任务对比**：控制节点数和边数相同，比较模型在两种结构上的表现（图7）。
4. **指令顺序敏感性分析**：对同一任务图构造三种不同文本顺序的指令，用标准差衡量敏感性（表8）。
5. **任务意图影响实验**：对照组/实验组分别用包含/不含意图的数据微调或推理，观察规划能力变化（表9）。
6. **迁移到其他基准**：在 AndroidControl 和 OmniAct 上测试微调后模型的接地（grounding）和成功率（表6、表7）。
7. **消融实验**：对三个质量控制模块进行消融，验证其效果（表3）。
8. **失败分析**：从 100 个随机失败案例中统计五大错误类型分布（图8）。

## 4. 资源与算力

论文提到：所有实验均在 **NVIDIA A100 80G GPUs** 上进行。但**未明确给出**使用的 GPU 数量、具体训练时长或推理资源消耗。仅在实验设置中提及使用该 GPU 型号。

## 5. 实验数量与充分性

- **实验数量**：超过 10 组不同维度的实验，包括主对比（12个模型 * 10能力）、复杂度级别分析（5级别 * 3水平）、图结构 vs 链结构、指令敏感性（3种顺序）、意图影响（4闭源+2开源）、迁移至2个额外基准、消融实验（3模块）、失败分析（100案例）。
- **充分性**：实验设计较为全面，覆盖了多种模型类型（闭源/开源/专用智能体/微调模型），多个维度（10能力，5复杂度），并进行了跨基准迁移验证和消融分析。但**缺少统计显著性检验**（如置信区间或p值），且人类评估部分仅凭两名标注者平均，可能引入主观偏差。
- **客观性与公平性**：控制了输入分辨率、使用了统一 prompt（若无默认），并对 OS-Atlas 的特殊性（零样本无法双击）进行了适应性调整。对比方法均采用官方默认或统一设置，较为公平。

## 6. 论文的主要结论与发现

1. **现有智能体在图结构任务上严重不足**：即便 GPT-4o 在链结构任务上可达 48.8%，在图结构上仅 20.5%，而人类达 80.1%。
2. **任务意图可显著提升规划能力**：在提示或训练数据中加入意图，可使规划平均分从 23.4% 提升至 28.9%（闭源）或 30.5%→31.9%（开源）。
3. **指令顺序敏感性**：现有智能体对指令表达顺序敏感，而用图结构数据微调可降低敏感性，提高稳定性。
4. **微调效益**：在 OmniBench 数据上微调后的 OS-Atlas 和 UGround 在 AndroidControl 和 OmniAct 上均取得平均 0.3~0.73 点的成功率提升。
5. **能力瓶颈**：子任务识别（SI）和长指令遵循（LIF）是所有模型（包括 GPT-4o）的显著短板，远低于人类基线。
6. **错误模式**：主要失败原因包括幻觉性成功（36%）、指令误解（23%）、知识缺乏（21%）、接地错误（17%）、环境错误（3%）。

## 7. 优点

- **自动化与可扩展性**：通过自底向上自动合成管道，无需人工标注即可生成大规模多样化任务，任务规模 36k，比多数环境基准大 40 倍。
- **复杂度可控**：通过约束 DAG 的五维属性，可精确控制任务难度，便于细粒度能力测试。
- **多维评估体系**：首次同时评估 10 种能力，并提出基于图的新指标（CR、LC），比传统结果/轨迹评估更合理。
- **高质量数据**：通过交叉验证、意图提取、一致性验证三个质量控制模块，人类接受率达 91%。
- **跨平台通用性**：支持桌面、移动、web 平台，易于扩展。
- **实用指导**：揭示了任务意图、指令顺序等关键因素对智能体性能的影响，提供了即插即用的改进方向。

## 8. 不足与局限

- **环境依赖**：目前主要基于 Windows 11 桌面环境构建，其他平台（如 macOS、Linux）的适应性未验证。虽然声称跨平台，但实验主要展示桌面和部分 web。
- **合成数据偏差**：子任务和轨迹均由 MLLM 合成，可能引入模型固有偏差（如偏好某种操作模式），且评估函数依赖预设 API，无法覆盖所有真实交互细节。
- **人类评估局限性**：接受率和失败分析均基于少量标注人员（2 名），可能不够鲁棒，未报告标注者间一致性。
- **未涉及医疗或 EHR 场景**：论文属于通用智能体评估，完全不涉及电子健康记录或医疗领域，如要迁移需大量调整（应用、环境、评估指标）。
- **资源消耗未报告**：虽提及 A100 GPU，但未给出训练/推理的具体算力和时间，不利于复现和工程判断。
- **统计显著性缺失**：比较结果未提供置信区间或统计检验，部分差异可能不显著。
- **未讨论实时性**：对虚拟智能体的执行效率、步数限制等实际应用要求考虑较少（仅设最大步数 N）。

（完）
