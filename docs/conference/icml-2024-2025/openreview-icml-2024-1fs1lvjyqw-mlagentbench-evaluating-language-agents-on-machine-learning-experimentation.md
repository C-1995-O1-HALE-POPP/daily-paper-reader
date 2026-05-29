---
title: "MLAgentBench: Evaluating Language Agents on Machine Learning Experimentation"
title_zh: MLAgentBench：评估机器学习实验中的语言代理
authors: "Qian Huang, Jian Vora, Percy Liang, Jure Leskovec"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=1Fs1LvjYQW"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 语言代理的基准评估框架，可迁移至医疗代理领域
tldr: 机器学习实验是研究核心，但语言代理在此任务上的评估缺乏统一基准。本文提出MLAgentBench，包含13个机器学习实验任务，基于ReAct框架构建代理，并评估多种LLM的性能。该工作为医疗代理的评测提供了可借鉴的方法论和基准设计思路，尽管未直接涉及EHR。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1716, \"height\": 773, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1590, \"height\": 1004, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 831, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 653, \"height\": 1058, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 821, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 790, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1594, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1232, \"height\": 827, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-1fs1lvjyqw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1236, \"height\": 847, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-1fs1lvjyqw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1751, \"height\": 1105, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1fs1lvjyqw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1798, \"height\": 749, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1fs1lvjyqw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1675, \"height\": 777, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1fs1lvjyqw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1674, \"height\": 776, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-1fs1lvjyqw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1365, \"height\": 771, \"label\": \"Table\"}]"
motivation: 语言代理能否有效进行机器学习实验？目前缺乏标准化评估基准。
method: 构建13个实验任务和ReAct框架代理，评测多种LLM在实验流程中的表现。
result: 揭示了不同LLM在代理实验任务中的性能差异和局限性。
conclusion: MLAgentBench可作为评估代理自动化实验能力的标准测试平台，可用于医疗agent评估。
---

## Abstract
A central aspect of machine learning research is experimentation, the process of designing and running experiments, analyzing the results, and iterating towards some positive outcome (e.g., improving accuracy). Could agents driven by powerful language models perform machine learning experimentation effectively? To answer this question, we introduce MLAgentBench, a suite of 13 tasks ranging from improving model performance on CIFAR-10 to recent research problems like BabyLM. For each task, an agent can perform actions like reading/writing files, executing code, and inspecting outputs. We then construct an agent that can perform ML experimentation based on ReAct framework. We benchmark agents based on Claude v1.0, Claude v2.1, Claude v3 Opus, GPT-4, GPT-4-turbo, Gemini-Pro, and Mixtral and find that a Claude v3 Opus agent is the best in terms of success rate. It can build compelling ML models over many tasks in MLAgentBench with 37.5% average success rate. Our agents also display highly interpretable plans and actions. However, the success rates vary considerably; they span from 100% on well-established older datasets to as low as 0% on recent Kaggle challenges created potentially after the underlying LM was trained. Finally, we identify several key challenges for LM-based agents such as long-term planning and reducing hallucination.

---

## 论文详细总结（自动生成）

# MLAgentBench 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- 机器学习研究的核心活动是实验：设计并运行实验、分析结果、迭代改进。然而，将这一过程自动化面临巨大挑战，需要研究者具备广泛先验知识、编写功能代码以及解读结果的能力。
- 近年来，强大的语言模型（LM）展现出理解与生成类人文本的能力，但它们在端到端进行机器学习实验上的表现缺乏系统评估。
- 为此，论文提出了 **MLAgentBench**，旨在成为首个专门评估语言代理（Language Agent）在机器学习实验任务上能力的标准化基准。该工作不仅填补了评估空白，也为更广泛的语言代理评测（如医疗领域）提供了可借鉴的方法论和基准设计思路。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：构建一个通用框架，将机器学习实验任务描述为环境、动作和评估器，并设计一个基于 ReAct 框架的 LM 代理，使其能够自主探索、修改代码、执行实验并提交结果。
- **关键技术细节**：
  - **任务规范**：每个任务包括（1）文本描述（目标、提交格式）；（2）起始文件（数据、基线代码等）；（3）评估器（用于打分）。
  - **环境与动作**：通用环境，包含 9 种基本动作（列出文件、读/写/追加/复制/撤销编辑、执行脚本等）和 3 种复合动作（理解文件、编辑脚本、编辑脚本片段）。复合动作内部调用 LM 辅助完成。
  - **代理设计**：基于 ReAct，但加入了更丰富的思考结构。代理的 **Prompt** 包含：可用工具描述、任务描述、响应格式模板（要求按以下顺序输出）：
    - **Reflection**：对上一观察的反思
    - **Research Plan and Status**：当前研究计划与进度记录
    - **Fact Check**：检查更新中陈述是否被直接确认
    - **Thought**：下一步动作的推理
    - **Action** 与 **Action Input**（JSON 格式）
  - 每一步，LM 输出上述格式文本，解析出动作 at，环境执行后返回新观察，代理更新记忆（历史轨迹）。循环直至提交最终答案或达到步数/时间上限。

## 3. 实验设计：数据集 / 场景、benchmark、对比方法

- **数据集与场景**：包含 13 个任务，按类别分为：
  - **经典任务**：CIFAR-10（图像分类）、imdb（文本分类、需从零编写模型）、ogbn-arxiv（图节点分类）
  - **经典 Kaggle**：house-price（房价回归）、spaceship-titanic（分类），要求从零编写和训练模型
  - **Kaggle 挑战**：parkinsons-disease、fathomnet、feedback、identify-contrails（发布在 LM 训练之后，测试泛化性）
  - **近期研究**：CLRS（算法推理）、BabyLM（语言建模）
  - **代码改进**：llama-inference（加速推理）、vectorization（加速卷积）
- **对比方法**：
  - 语言模型：GPT-4 (0613)、GPT-4-turbo (0125)、Claude v1.0、Claude v2.1、Claude v3 Opus (opus-20240229)、Gemini Pro、Mixtral (Instruct-v0.1)
  - 其他代理框架：AutoGPT（开源通用代理）、LangChain 中的“zero-shot-react-description”（即 ReAct，但缺乏研究计划和事实检查）
- **评估指标**：
  - **能力**：成功率（性能指标相比基线提升 ≥10% 的试次比例）和平均改进百分比
  - **效率**：总壁钟时间、总输入/输出 token 数

## 4. 资源与算力

- 论文未明确说明使用的 GPU 型号、数量和训练时长。所有实验均通过调用 API 完成（GPT-4、Claude 等），并非进行模型训练。
- 每个运行的成本仅几美元；完整运行一次基准（GPT-4-turbo）约消耗 600 万 token，约 60 美元。但考虑到低成功率（26%），期望成本达 231 美元。
- 运行限制：多数代理允许最多 50 步或 5 小时；GPT-4 由于成本仅允许 30 步。

## 5. 实验数量与充分性

- 每个代理在每个任务上执行 **8 次运行**，共涉及 7 种 LLM × 13 任务 × 8 轮 = 728 次运行（加上框架对比实验，总数更多）。
- 补充实验：对比 AutoGPT 和 LangChain（使用 GPT-4-turbo 和 Claude v3 Opus）。
- 消融分析：对 CIFAR-10 上的错误模式进行了分类统计（幻觉、糟糕计划、响应格式错误、提交格式错误、小改进），并展示了不同模型在这些模式上的分布。
- 充分性评价：实验覆盖了多种领域、难度和数据新鲜度，且每种条件重复 8 次以降低随机性。但受限于 API 成本和时间，部分任务成功率极低（如 parkinsons-disease、BabyLM 为 0%），可能未能充分探索代理的潜力。整体实验设计客观公平，但未进行更细粒度的消融（如单独移除 Fact Check 组件）。

## 6. 论文的主要结论与发现

- **最佳代理**：基于 Claude v3 Opus 的代理以 37.5% 平均成功率领先，但在经典任务上可达 100%（如 house-price），而在新 Kaggle 挑战上仅为 0-25%。
- **性能差异**：同一模型家族中，最新版本性能更好；GPT-4 的平均改进百分比高于 Claude v3 Opus，主要受 identify-contrails 任务的高改进驱动。
- **错误分析**：主要错误模式为幻觉、糟糕计划、响应/提交格式错误。Claude v3 Opus 表现更稳健，GPT-4/turbo 更易出现幻觉和格式错误。
- **长期规划挑战**：智能体在长时间步后性能可能下降（除 Claude v3 Opus 外），说明长期计划与重新规划存在困难。
- **成本与效率**：GPT-4-turbo 虽成功率略低，但 token 效率最高（比其他代理少 51% 的 token）。

## 7. 优点

- **任务多样性**：涵盖了经典研究、Kaggle 挑战、最新研究以及代码优化，跨多种模态（图像、文本、图、表格、时间序列），且包含数据新鲜度指标以缓解数据污染。
- **代理设计**：强调可解释性，通过 Research Plan and Status 和 Fact Check 组件，让代理的思考过程透明，便于人类理解、干预和审核。
- **模块化框架**：环境、动作、评估器均独立，易于扩展新任务或新动作。
- **开源与可重复性**：代码已发布，有助于后续研究者复现和构建更优的代理。
- **对安全与人类协同的重视**：指出在自主执行代码时需人类监督，并强调可解释性作为人类增强的钩子。

## 8. 不足与局限

- **成功率低**：整体成功率仅 37.5%（最佳模型），对于实际可用性仍显不足；在近期任务上几乎全部失败，表明现有代理对分布外和新颖任务的泛化能力差。
- **成本与可靠性问题**：低成功率意味着期望成本高（如 GPT-4-turbo 为 231 美元/任务），限制了现实部署的经济性。
- **幻觉与计划失误**：代理经常幻觉出性能改进、做出错误计划且难以恢复，尤其是在复杂大代码库（如 CLRS、BabyLM）上表现糟糕。
- **实验覆盖偏差**：所有任务的计算开销控制在几分钟内，可能无法反映更长周期、更大规模实验的挑战；部分任务无基线（需从零写模型），但评估时只得与随机基线对比。
- **代理设计的局限性**：仅测试了基于 ReAct 的单一模板，未比较不同提示结构（如纯 CoT 或更复杂的记忆机制）；复合动作依赖于 LM 辅助，可能引入额外错误。
- **安全风险**：代理可任意修改和执行代码，可能写出危险系统代码，必须受密切监督。

（完）
