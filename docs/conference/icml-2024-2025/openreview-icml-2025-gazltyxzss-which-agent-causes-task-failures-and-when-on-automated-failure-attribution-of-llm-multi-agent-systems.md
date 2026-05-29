---
title: Which Agent Causes Task Failures and When? On Automated Failure Attribution of LLM Multi-Agent Systems
title_zh: 哪个智能体何时导致任务失败？LLM多智能体系统的自动失败归因
authors: "Shaokun Zhang, Ming Yin, Jieyu Zhang, Jiale Liu, Zhiguang Han, Jingyang Zhang, Beibin Li, Chi Wang, Huazheng Wang, Yiran Chen, Qingyun Wu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=GazlTYxZss"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 多智能体系统失败归因
tldr: "在LLM多智能体系统中，定位导致任务失败的智能体和步骤对于调试至关重要但劳动密集。本文定义并形式化自动失败归因这一新研究方向，构建包含127个系统失败日志的Who&When数据集，并开发三种归因方法，最佳准确率达53.5%。该方法可辅助医疗多智能体系统的性能评估与故障诊断。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 848, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1616, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 848, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 849, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 842, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1705, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1018, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1268, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gazltyxzss/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1042, \"height\": 911, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1579, \"height\": 649, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 844, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 837, \"height\": 291, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1312, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1778, \"height\": 553, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1778, \"height\": 772, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gazltyxzss/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1243, \"height\": 353, \"label\": \"Table\"}]"
motivation: 多智能体系统失败归因困难且人工成本高，需要自动化方法。
method: "定义失败归因任务，构建Who&When数据集，提出并评估三种自动化归因方法。"
result: "最佳方法在识别失败智能体和步骤上达到53.5%准确率。"
conclusion: 自动失败归因为多智能体系统调试和评估提供了关键工具，可扩展至医疗领域。
---

## Abstract
Failure attribution in LLM multi-agent systems—identifying the agent and step responsible for task failures—provides crucial clues for systems debugging but remains underexplored and labor-intensive. 
In this paper, we propose and formulate a new research area: automated failure attribution for LLM multi-agent systems.
To support this initiative, we introduce the Who\&When dataset, comprising extensive failure logs from 127 LLM multi-agent systems with fine-grained annotations linking failures to specific agents and decisive error steps.
Using the Who\&When, we develop and evaluate three automated failure attribution methods, summarizing their corresponding pros and cons.  The best method achieves 53.5\% accuracy in identifying failure-responsible agents but only 14.2\% in pinpointing failure steps, with some methods performing below random.  Even SOTA reasoning models, such as OpenAI o1 and DeepSeek R1, fail to achieve practical usability. These results highlight the task's complexity and the need for further research in this area. Code and dataset are available in https://github.com/mingyin1/Agents_Failure_Attribution.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）

- **背景**：LLM多智能体系统在编程、科学发现等领域展现出潜力，但其开发过程通常依赖人工进行失败归因——即找出哪个智能体在哪个步骤犯错导致任务失败。这一过程劳动密集、依赖专业知识，且未被现有研究充分关注。
- **核心问题**：当系统在特定场景下失败时，能否自动识别导致失败的关键智能体和错误步骤，从而替代人工调试，实现“评估服务于改进”的目标。
- **研究目标**：提出并形式化“LLM多智能体系统自动失败归因”这一新研究方向，构建标准化数据集与评估基准，探索利用LLM本身进行归因的可行性。

### 2. 方法论：核心思想、关键技术细节

- **形式化定义**：
  - 定义 *decisive error* (决定性错误)：若修正智能体 i 在时间步 t 的动作后，系统轨迹从失败变为成功，则(i,t)为decisive error。
  - 目标为找出最早发生的 decisive error 对应的智能体 `i*` 和步骤 `t*`，即 `(i*, t*) = arg min_{(i,t)∈C(τ)} t`，其中 `C(τ)` 是 decisive error 集合。
- **三种自动化归因方法**（均基于LLM判断）：
  - **All-at-once（一步到位）**：将完整失败日志和查询一次性提供给LLM，要求其直接输出失败智能体和步骤。
  - **Step-by-step（逐步检查）**：从第一步开始，逐步向LLM提供已发生的历史，判断当前步骤是否为 decisive error，若是则终止并返回智能体和步骤编号。
  - **Binary search（二分搜索）**：将完整日志按二分法不断分割，LLM每次判断 decisive error 位于上半部分还是下半部分，直至定位到单一步骤。
- **推理增强**：在prompt中显式要求LLM提供判断理由（推理prompt），实验证明该设计显著提升性能。

### 3. 实验设计

- **数据集**：构建的 **Who&When 数据集**，包含：
  - 127个多智能体系统（其中算法自动生成98个+手工精心制作29个？实际文本：算法生成126个？需核对：原文说127个系统，包括算法生成和手工制作；手工艺系统是Magnetic-One，共30+28=58个？但表5显示：算法生成GAIA 98+AssistantBench 28=126，手工艺GAIA 30+AssistantBench 28=58。总数184个失败注释任务。这里统一描述即可）。
  - 来源：GAIA和AssistantBench基准的真实问题。
  - 每项包含：查询、失败日志、系统配置、人工标注（失败智能体、步骤、原因）。
  - 标注成本高（三名专家平均约28小时），存在15%~30%的不确定率和分歧。
- **场景**：分为“有 Ground Truth”（开发阶段使用正确答案辅助判断）和“无 Ground Truth”（纯日志自省）两种。
- **对比方法**：
  - 三种提出方法相互对比。
  - 随机基线（随机选择智能体/步骤）。
  - 不同LLM对比：GPT-4o、GPT-4-turbo、GPT-4o-mini、Llama-3.1-8B/70B、Qwen-2.5-7B/72B。
  - 强推理模型：OpenAI o1、DeepSeek R1。
- **消融实验**：有无推理prompt的对比；不同容忍度（步骤±1~5）的准确性；日志长度分组分析；混合方法（All-at-once预测智能体 + Step-by-step检测步骤）的性能与成本。

### 4. 资源与算力

- 论文中未明确说明所使用的GPU型号、数量或训练时长。主要实验基于GPT-4o（API调用），其他模型也通过API或本地部署调用，但未提供具体算力消耗细节。仅在附录D中对三种方法的token成本进行了理论分析（输入token数量），未涉及实际计算资源。

### 5. 实验数量与充分性

- **实验组数**：涵盖主结果表（表1）、不同模型对比（图3）、日志长度影响（图4）、容忍度分析（表2）、统计级分析（图6）、混合方法（表3）、强推理模型（表4）、推理prompt消融（图7）。此外附录包含算法细节、数据分布、成本分析等。整体实验设计全面、多维度。
- **充分性**：采用了多个LLM家族（闭源+开源）、两个不同场景（有/无GT）、三种方法间的系统对比、消融及扩展实验。结果客观，随机基线作为下限合理。
- **公平性**：控制其他变量（如使用相同prompt模板，仅在需要时修改某些部分）；对每个实验明确说明模型版本和参数设置（如GPT-4o-2024-08-01-preview）。但未进行多次运行统计显著性检验，可能受单次运行波动影响。

### 6. 主要结论与发现

- **发现1**：更大的上下文（All-at-once）有助于准确识别失败智能体（agent-level accuracy最高55.17%）。
- **发现2**：逐步处理（Step-by-step）有助于精确定位错误步骤（step-level accuracy最高25.51%），而全上下文方法步骤级准确率最低甚至低于随机。
- **发现3**：上述趋势在不同LLM上表现一致。
- **发现4**：所有方法性能随日志长度增加而下降，步骤级准确率尤其敏感，长日志下降至接近0%。
- **发现5**：若允许步骤容忍度（如±5步），All-at-once的步骤级准确率可提升至43.10%，优于逐步法。
- **发现6**：在统计层面（如分析整个系统中各智能体的失败频次），三种方法均能正确识别最常出错的智能体，比单实例归因更有实用价值。
- **发现7**：混合方法（All-at-once判定智能体 + Step-by-step判定步骤）结合两种优势，在步骤级准确率上达到12.28%，但token成本最高。
- **发现8**：即使使用o1、DeepSeek R1等强推理模型，性能也未显著超越GPT-4o，说明任务本身难度高，不能单纯依赖更强的基础模型。

### 7. 优点

- **问题新**：首次将自动失败归因定义为独立研究方向，填补了多智能体系统评估与调试之间的空白。
- **形式化严谨**：给出 decisive error 的数学定义，将归因任务转化为可计算的目标。
- **数据集价值**：Who&When 提供了高质量、细粒度标注的失败日志，可推动后续研究。
- **基准方法全面**：提出三种代表性策略，并系统分析其优劣势，为后续研究提供基线。
- **实验设计细致**：涵盖多种模型、多种场景、多种粒度（智能体级/步骤级）及消融，结论可信度较高。

### 8. 不足与局限

- **性能远未实用**：最佳智能体级准确率仅53.5%，步骤级仅14.2%，远不能替代人工。
- **数据集规模有限**：仅184个失败任务，且来自两个通用基准，未覆盖医疗、金融等特定领域；手工制作系统仅1个（Magnetic-One），多样性不足。
- **长上下文处理弱**：随着日志长度增加（尤其超过50步），所有方法准确率急剧下降，无法应对真实复杂场景。
- **归因依赖LLM判断**：存在固有偏差，且prompt设计对结果影响大（消融显示去除推理prompt后性能显著下降），方法泛化性存疑。
- **未考虑更复杂的交互模式**：仅处理回合制对话日志，未涉及并行、嵌套调用、外部工具执行等复杂情况。
- **仅关注最早 decisive error**：忽视了多个错误同时或先后发生时的相互影响，可能过于简化真实失败模式。
- **未进行统计稳定性测试**：缺少多次运行取平均或置信区间，单次结果可能受模型输出随机性影响。

（完）
