---
title: "Agent-as-a-Judge: Evaluate Agents with Agents"
title_zh: 智能体即裁判：用智能体评估智能体
authors: "Mingchen Zhuge, Changsheng Zhao, Dylan R. Ashley, Wenyi Wang, Dmitrii Khizbullin, Yunyang Xiong, Zechun Liu, Ernie Chang, Raghuraman Krishnamoorthi, Yuandong Tian, Yangyang Shi, Vikas Chandra, Jürgen Schmidhuber"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Nn9POI9Ekt"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 用智能体评估智能体系统的通用框架
tldr: 现存的智能体评估方法要么只关注最终结果，忽略逐步推理过程，要么需要大量人工。为此，本文提出智能体即裁判（Agent-as-a-Judge）框架，利用智能体系统本身的特征来评估其他智能体，支持对整个任务解决过程进行中间反馈以获得更精确的评估。该框架在代码生成任务上进行了验证，但其方法论具有通用性，可迁移至医疗智能体评估等场景。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1646, \"height\": 877, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1558, \"height\": 859, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 834, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 636, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 666, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 635, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1531, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 240, \"height\": 68, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nn9poi9ekt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1116, \"height\": 2255, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1429, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1424, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1424, \"height\": 1039, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1755, \"height\": 565, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1766, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 628, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 717, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 890, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1769, \"height\": 384, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nn9poi9ekt/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1599, \"height\": 395, \"label\": \"Table\"}]"
motivation: 现有智能体评估技术要么忽略逐步推理过程，要么需要过度手工劳动，缺乏对中间过程的精细评估。
method: 提出Agent-as-a-Judge框架，利用智能体系统作为裁判，在任务解决过程中提供中间反馈，实现更精确的逐步评估。
result: 在代码生成任务上验证了框架有效性，构建了DevAI基准（55个任务），展示了智能体评估智能体的可行性。
conclusion: 该框架为在医疗等复杂领域评估智能体提供了可迁移的方法论，有望提升评估的细粒度与自动化程度。
---

## Abstract
Contemporary evaluation techniques are inadequate for agentic systems. These approaches either focus exclusively on final outcomes---ignoring the step-by-step nature of the thinking done by agentic systems---or require excessive manual labour. To address this, we introduce the **Agent-as-a-Judge** framework, wherein agentic systems are used to evaluate agentic systems. This is a natural extension of the LLM-as-a-Judge framework, incorporating agentic features that enable intermediate feedback for the entire task-solving processes for more precise evaluations. We apply the Agent-as-a-Judge framework to the task of code generation. To overcome issues with existing benchmarks and provide a proof-of-concept testbed for Agent-as-a-Judge, we present **DevAI**, a new benchmark of 55 realistic AI code generation tasks. DevAI includes rich manual annotations, like a total of 365 hierarchical solution requirements, which make it particularly suitable for an agentic evaluator. We benchmark three of the top code-generating agentic systems using Agent-as-a-Judge and find that our framework dramatically outperforms LLM-as-a-Judge and is as reliable as our human evaluation baseline. Altogether, we believe that this work represents a concrete step towards enabling vastly more sophisticated agentic systems. To help that, our dataset and the full implementation of Agent-as-a-Judge will be publically available at https://github.com/metauto-ai/agent-as-a-judge

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：当前评估方法对智能体系统（agentic systems）不充分。传统方法要么只关注最终结果（如 pass@1），忽略智能体逐步推理的过程；要么依赖过多人工，成本高昂且难以扩展。
- **核心问题**：如何实现对智能体系统高效、细粒度、可自动化的评估，既能捕捉中间步骤的反馈，又能大幅降低人力成本。
- **整体含义**：该工作提出了“智能体即裁判”（Agent-as-a-Judge）框架，是“LLM即裁判”（LLM-as-a-Judge）的自然延伸，但通过引入智能体系统的特征（如多步交互、环境反馈、工具使用），提供了对完整任务解决过程进行中间评估的能力。这为大规模、复杂智能体系统的评估开辟了新途径。

## 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

- **核心思想**：使用一个或多个**智能体系统**来评估另一个智能体系统的输出和过程。与LLM-as-a-Judge仅使用单个LLM不同，Agent-as-a-Judge能够访问生成的工作空间、执行轨迹、代码文件等，模拟人类评估者的逐步审查过程。
- **关键模块设计**（初始设计包含8个组件，消融后保留5个核心组件）：
  1. **Graph（图形模块）**：构建项目结构图，包括文件、模块、依赖关系，并可将代码分解为代码片段。
  2. **Locate（定位模块）**：根据需求识别特定文件夹或文件路径。
  3. **Read（读取模块）**：支持读取和理解多模态数据（代码、图像、视频、文档等33种格式），以验证不同类型需求。
  4. **Retrieve（检索模块）**：从长文本（如执行轨迹）中提取相关信息，识别与需求相关的段落。
  5. **Ask（询问模块）**：基于上述证据，判定给定需求是否被满足（输出 SATISFIED/UNSATISFIED 及简要理由）。
- **算法流程**（文字说明）：
  1. 接收用户查询和智能体产生的完整工作空间（代码、文件、轨迹）。
  2. 利用 Graph 模块构建工作空间的结构图。
  3. 根据需求列表，依次对每个需求进行判断：
     - 使用 Locate 模块定位相关文件路径。
     - 使用 Read 模块读取文件内容（代码、图像等）。
     - 若需要，使用 Retrieve 模块从轨迹中提取执行反馈（如错误信息）。
     - 合并所有证据后，通过 Ask 模块做出判断。
  4. 输出每个需求是否满足的二元判定，并可提供详细理由。
- **优化细节**：通过消融发现，移除 Planning（规划模块）和 Memory（记忆模块）以及 Search（搜索模块，因工作空间简单时效果不佳）后，性能最佳。最终的 Agent-as-a-Judge 仅包含 Graph、Locate、Read、Ask、Retrieve 五个模块。

## 3. 实验设计：使用了哪些数据集/场景、benchmark、对比方法

- **数据集**：自建基准 **DevAI**，包含 **55个真实AI开发任务**，覆盖监督学习、强化学习、计算机视觉、自然语言处理、生成模型等。每个任务包含：
  - 一段自然语言用户查询；
  - 一组分层需求（共 **365个**），需求间构成有向无环图（DAG）；
  - 一组偏好（可选软约束，共 **125个**）。
- **场景**：代码生成。具体为自动化AI开发任务，例如“使用YOLOv3和COCO数据集进行目标检测”、“使用CNN-LSTM进行语音情感识别”等。
- **基准（Baseline）**：三种开源代码生成智能体系统：
  - **MetaGPT**（含 Data Interpreter）
  - **GPT-Pilot**
  - **OpenHands**
  所有系统均使用 GPT-4o-2024-05-13 作为后端语言模型。
- **对比方法**：三种评估范式：
  1. **Human-as-a-Judge**：三位人类专家独立评估，再通过讨论达成共识，作为 ground truth。
  2. **LLM-as-a-Judge**：直接使用 GPT-4o 对需求进行判断（黑盒/灰盒设置，灰盒可访问轨迹）。
  3. **Agent-as-a-Judge**：本文提出的框架（同样分黑盒/灰盒设置）。
- **评估指标**：
  - 需求满足率（独立/考虑依赖）
  - 任务完成率
  - 对齐率（Alignment Rate，与人类共识一致的比例）
  - 法官偏移（Judge Shift）
  - PR 曲线（处理类别不平衡）

## 4. 资源与算力

- **算力说明**：论文中**未明确提及**使用的 GPU 型号、数量或训练时间。所有评估均基于预训练的 GPT-4o 模型进行推理，没有训练过程。
- **成本与时间**：
  - 人工评估：总共约 **86.5 小时**，按 $15/小时计费约 **$1297.50**。
  - Agent-as-a-Judge：平均每个任务约 **118.43 分钟**，API 成本 **$30.58**（占人工成本的 2.36%）。
  - LLM-as-a-Judge：平均 **10.99 分钟**，成本 **$29.63**。
- 后端模型使用 GPT-4o-2024-05-13，推理时消耗 API 资源。

## 5. 实验数量与充分性

- **主要实验组数**：
  - **初步统计**（表1）：对三个开发者系统在 DevAI 上的运行成本、时间、输出等进行了统计。
  - **人类评估**（表2）：三位专家对所有任务、所有系统进行两轮评估（第一轮独立，第二轮讨论共识）。
  - **AI 法官评估**（表3）：LLM-as-a-Judge 和 Agent-as-a-Judge 分别在黑盒和灰盒设置下进行评估，报告了对齐率和法官偏移。
  - **消融实验**（表4、表5、表6、表7）：
    - 组件消融（逐步添加 ask, graph, read, locate, search, retrieve, planning, memory）。
    - 搜索算法消融（BM25 vs Sentence-BERT vs Fuzzy）。
    - 检索模块消融（不同截断策略）。
  - **PR 曲线**（图6）：对比不同方法。
  - **后端 LLM 敏感性实验**（表10）：测试 Llama 3.2 90B、Qwen Coder 2.5 32B、GPT-4o、Claude 3.5 Sonnet 的对齐率。
  - **额外人类验证**（附录P）：招募10名额外专家评估7个随机样本，验证共识结果的可靠性。

- **充分性与公平性**：
  - 实验覆盖了多种评估范式，消融完整，对比了不同后端的影响。
  - 公平性：所有开发者系统使用相同后端模型、相同时间限制（1800秒）、相同任务集。评估过程使用双盲设置（？存疑，但描述了人类评估的独立性）。
  - 不足：仅针对代码生成领域验证，通用性仅声称；任务规模较小（55个任务），可能存在领域偏差。

## 6. 论文的主要结论与发现

1. **Agent-as-a-Judge 显著优于 LLM-as-a-Judge**：在所有指标上（对齐率、法官偏移、PR曲线），Agent-as-a-Judge 更接近人类共识。
   - 例如，在 OpenHands 的黑盒评估中，Agent-as-a-Judge 对齐率达 **90.44%**，而 LLM-as-a-Judge 仅为 **60.38%**。
2. **Agent-as-a-Judge 与人类评估基线相当**：其对齐率（约 90%）甚至超过单个人类专家（平均值约 85-89%），接近人类多数投票的结果（约 94%）。
3. **成本大幅降低**：相比人工（约 $1297.50），Agent-as-a-Judge 仅需 $30.58，时间缩短至 2.36%。
4. **DevAI 基准的挑战性**：当前最好的开源智能体系统（GPT-Pilot、OpenHands）仅能满足约 29% 的需求（考虑依赖后），只有一个任务完全满足所有需求，表明该基准具有适度的挑战性。
5. **消融发现**：核心模块（Graph、Locate、Read、Ask、Retrieve）均显著提升性能；而 Planning、Memory、Search 模块在现有设置下效果不佳甚至起反作用。

## 7. 优点

- **框架新颖且通用**：将评估从“LLM评估LLM”扩展到“智能体评估智能体”，概念上更贴近人类评估流程，且设计为模块化，便于迁移到其他领域（声称通过修改 prompt 和工作流即可适配）。
- **高质量的基准建设**：DevAI 不仅包含真实任务，还引入了分层需求和依赖图，提供了比二分类指标更丰富的评估粒度，减少了过拟合风险。
- **实验设计严谨**：
  - 使用多轮人类评估（独立 + 辩论共识）建立可靠的 ground truth。
  - 分析了人类评估者之间的不一致性（10%-30%），并验证了多数投票的纠错能力。
  - 进行了充分的消融和敏感性分析，包括不同后端 LLM 的测试。
  - 用 PR 曲线处理类别不平衡，避免误导性指标。
- **成本效益显著**：自动化评估成本降低超过 97%，同时保持与人类评估相当的质量，对资源有限的团队极具价值。

## 8. 不足与局限

- **领域局限**：实验仅在代码生成领域（AI 开发任务）进行验证。虽然论文声称框架通用，但未在其他领域（如机器人控制、对话系统）中测试。
- **任务规模较小**：DevAI 仅包含 55 个任务，且每个任务代码量较小（数百行），可能无法代表大型、复杂的实际项目。
- **潜在偏见与误差传播**：Agent-as-a-Judge 依赖于后端 LLM（如 GPT-4o），若判断模型存在偏见或出现错误（如附录N中误认合成数据集为真实数据集），则可能产生系统性偏差。同时，若某一需求判断错误，可能影响后续相关需求。
- **模块设计的局限性**：
  - 消融表明 Planning 和 Memory 模块在当前设置下有害，但作者承认先进优化方法（如提示自动优化）可能改进，未做深入探索。
  - Search 模块因工作空间简单导致精度下降，但在复杂场景下可能重要，实验未能充分覆盖。
- **后端模型依赖**：论文主要使用 GPT-4o，对开源模型（Llama、Qwen）的测试仅做了少量对齐率比较，未系统评估不同后端对评估结果的影响范围。
- **人类评估可复制性问题**：人类评估者具有主观性，即使通过辩论达成共识，仍可能残留误差（论文中多数投票与共识仍有约 5% 差异）。额外10名专家的验证样本量较小（7个任务），统计效力有限。
- **未讨论代码执行安全性**：评估过程中需要智能体主动执行代码，存在安全风险（如恶意代码），论文未提及如何防范。
- **缺乏可解释性分析**：虽然报告了对齐率等指标，但未深入分析哪些类型的任务或需求更容易出错，仅附录N给出了少量示例。

（完）
