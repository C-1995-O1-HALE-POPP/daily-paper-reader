---
title: "AGILE: A Novel Reinforcement Learning Framework of LLM Agents"
title_zh: AGILE：一种新颖的LLM代理强化学习框架
authors: "Peiyuan Feng, Yichen He, Guanhua Huang, Yuan Lin, Hanchong Zhang, Yuchen Zhang, Hang Li"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=Ul3lDYo3XQ"
tags: ["query:ehr-agent"]
score: 6.0
evidence: RL框架用于LLM代理并在医疗问答（MedMCQA）上测试
tldr: 现有LLM代理缺乏有效的强化学习训练机制。本文提出AGILE框架，将LLM代理构建为强化学习问题，使用PPO算法在动作标签数据上微调，并集成反射、工具使用和专家咨询能力。在MedMCQA等医疗问答数据集上取得了显著性能提升，证明了RL在医疗代理训练中的可行性。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1382, \"height\": 895, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 657, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 659, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 601, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1438, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1400, \"height\": 888, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1402, \"height\": 1369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1432, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ul3ldyo3xq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1438, \"height\": 352, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1430, \"height\": 468, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1421, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 523, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 994, \"height\": 410, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1019, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1070, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1402, \"height\": 500, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1305, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1418, \"height\": 439, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1449, \"height\": 418, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1484, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1423, \"height\": 1042, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1289, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1068, \"height\": 2273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1435, \"height\": 848, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1130, \"height\": 824, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1246, \"height\": 2340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1088, \"height\": 2298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ul3ldyo3xq/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1431, \"height\": 174, \"label\": \"Table\"}]"
motivation: 现有LLM代理无法有效利用环境反馈进行强化学习，限制了其复杂任务能力。
method: 提出AGILE框架，将LLM作为策略模型，使用PPO算法在动作标签上微调，并整合反射、工具使用和专家咨询。
result: 在MedMCQA、ProductQA等数据集上，AGILE显著优于基线，展示了RL框架的有效性。
conclusion: AGILE为LLM代理的强化学习训练提供了通用框架，可迁移至医疗等领域的代理优化。
---

## Abstract
We introduce a novel reinforcement learning framework of LLM agents named AGILE (AGent that Interacts and Learns from Environments)  designed to perform complex conversational tasks with users, leveraging LLMs, memory, tools, and interactions with experts. The agent possesses capabilities beyond conversation, including reflection, tool usage, and expert consultation. We formulate the construction of such an LLM agent as a reinforcement learning (RL) problem, in which the LLM serves as the policy model. We fine-tune the LLM using labeled data of actions and the PPO algorithm. We focus on question answering and release a dataset for agents called ProductQA, comprising challenging questions in online shopping. Our extensive experiments on ProductQA, MedMCQA and HotPotQA show that AGILE agents based on 7B and 13B LLMs trained with PPO can outperform GPT-4 agents. Our ablation study highlights the indispensability of memory, tools, consultation, reflection, and reinforcement learning in achieving the agent's strong performance. Datasets and code are available at https://github.com/bytarnish/AGILE.

---

## 论文详细总结（自动生成）

# AGILE: A Novel Reinforcement Learning Framework of LLM Agents — 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：大型语言模型（LLM）在指令遵循、推理等方面表现出色，催生了基于 LLM 的自主代理（LLM agent）。现有工作提出了规划、反思、工具使用等组件，但如何将这些组件统一到一个框架中并进行端到端优化仍不明确。
- **核心问题**：如何构建一个能够统一记忆、工具、反思、专家咨询等能力，并通过强化学习（RL）端到端训练的 LLM 代理，使其在复杂问答任务中超越 GPT-4 等强基线。
- **整体含义**：提出 AGILE 框架，将 LLM 代理构建为强化学习问题，LLM 作为策略模型，使用 PPO 算法在动作标签上微调，同时引入主动寻求人类专家建议的能力，使代理能够自适应地平衡准确性和人力成本。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- 将 LLM 代理视为一个 token 级别的马尔可夫决策过程（MDP），LLM 的词汇表作为动作空间，上下文和记忆组成状态。通过 RL 来训练策略（即 LLM），使其学会何时调用不同模块（如检索记忆、使用工具、寻求建议、反思等）。

### 关键技术细节
1. **系统架构**：由四个模块组成——LLM、记忆、工具、执行器。执行器根据 LLM 预测的动作 token 执行相应函数（如获取问题、检索记忆、寻求建议、搜索产品、预测答案、提交答案、清除上下文等）。
2. **RL 公式化**：
   - 状态：`(context, memory)` 对。
   - 动作：每个 token 为一个动作。
   - 状态转移：由执行器根据函数注册表完成（例如 `[GetQuestion]` 触发用户输入，`[UpdateMemory]` 写入记忆）。
   - 奖励：正确答案+1，错误答案0，寻求建议有固定成本 -c。
3. **策略学习**：
   - **阶段1：模仿学习（IL）**：从人类或更优代理（如 GPT-4）生成的轨迹中抽取训练序列，仅在动作 token 上计算损失。
   - **阶段2：强化学习（PPO）**：使用 Proximal Policy Optimization 优化策略，同样只对动作 token 应用策略梯度，并使用上下文作为注意力掩码。
   - **会话级优化**：针对长轨迹提出会话级优化算法（附录 A），使用状态优势函数 `A_i = V(S_{i+1}) - V(S_i)` 的启发式定义来近似跨会话依赖。
4. **主动寻求建议**：代理可调用 `[SeekAdvice]` 函数，从人类专家获取答案，并通过 `[Reflection]` 提炼通用知识存入记忆，用于未来会话。RL 可端到端地学习何时寻求建议，因为成本和收益都可建模为奖励。

## 3. 实验设计

### 使用的数据集
- **ProductQA**：新构建的电商在线购物 QA 数据集，包含 88,229 对 QA，覆盖 26 个产品类别（20 训练、6 测试），包含事实型、搜索型、推理型问题，评估代理的历史信息处理、工具使用、人机交互、自我评估、反思和跨任务适应能力。
- **MedMCQA**：医学领域多项选择 QA 数据集（印度医学院入学考试），使用完整开发集。
- **HotPotQA**：自然多跳推理 QA 数据集，使用完整开发集。

### Benchmark 与对比方法
- 基线包括：
  - 直接提示 GPT-3.5 和 GPT-4（`prompt`）。
  - 将 GPT-3.5/4 放入 AGILE 框架（`agile-gpt3.5-prompt`, `agile-gpt4-prompt`）。
  - 在 ProductQA 上：Vicuna-13b 直接提示、AGILE 变体。
  - 在 HotPotQA 上：ReAct、CRITIC、Expel、AutoAct 等。
- 评估指标：准确率（Accuracy）、寻求建议率（Advice Rate）、总分（Total Score，考虑建议成本）。

### 实验设置
- LLM 初始化：ProductQA 和 HotPotQA 使用 Vicuna-13b-1.5；MedMCQA 使用 Meerkat-7b（医学专用 7B 模型）。
- 训练：SFT 2 epoch，lr=1e-5，batch=64；PPO 1 epoch，lr=1e-6，batch=64。全参数微调，不使用 LoRA。
- 建议成本 c：默认 ProductQA 和 HotPotQA 为 0.3，MedMCQA 为 0.4。

## 4. 资源与算力

- **GPU 型号**：NVIDIA H800。
- **使用数量**：每项实验使用 8 张 H800 GPU。
- **训练时长**：
  - ProductQA：SFT 3.6 小时，RL 5.5 小时。
  - MedMCQA：SFT 0.9 小时，RL 2.0 小时。
  - HotPotQA：SFT 7.9 小时，RL 27.5 小时。
- 论文未提及总计算量或完整项目计算成本。

## 5. 实验数量与充分性

- **实验组数**：
  - 三个数据集共 3 组主要实验。
  - 在 ProductQA 上进行详尽的**消融实验**：分别去除 reflection、memory、advice、tool-use、RL，共 5 组，每组对比完整 AGILE。
  - 在 MedMCQA 上进行了 5 组消融。
  - 在 HotPotQA 上进行了 3 组消融。
  - 额外实验：不同建议成本 c 的敏感性分析（5 个成本值）、多个 PPO 随机种子（3 次）的鲁棒性实验、随机初始策略下的 RL 效果（2 种设置）。
  - 还展示了训练曲线、会话级 advice rate 变化等。
- **充分性评价**：
  - 覆盖了多种 QA 场景（电商、医学、多跳推理），具有较强的泛化性。
  - 消融实验系统性地验证了每个模块的必要性。
  - 进行了鲁棒性测试（3 次独立 RL 训练），标准差小。
  - 长期答案评估使用 GPT-4 评判，并与人工标注对比（94% 一致率），验证了评估可靠性。
  - 总体实验设计较为充分、客观、公平。

## 6. 主要结论与发现

1. **AGILE 代理超越 GPT-4 代理**：在 ProductQA 上，基于 Vicuna-13b 的 AGILE 代理（PPO）总分比 GPT-4 代理相对提升 9.2%（短答案）；在 MedMCQA 上，基于 Meerkat-7b 的代理准确率 85.2%，超过 GPT-4 MedPrompt（79.1%）；在 HotPotQA 上，准确率 67.5%，比最强基线 ReAct-GPT-4 提升 40%。
2. **主动寻求建议显著提升性能**：可以纠正错误、积累知识，且 PPO 训练能有效优化寻求建议的时机。
3. **记忆、反思、工具使用均不可或缺**：缺失任一组件都会导致建议率上升或总分下降，尤其移除工具使用导致建议率增加 25.9%，总分下降 9.3%。
4. **RL 训练带来一致提升**：相比仅模仿学习（w/o RL），PPO 使总分相对提升 2.3%-7.1%，且能适应不同建议成本，灵活控制准确率-成本权衡。
5. **建议率随时间下降**：随着会话进行，代理知识积累，对专家依赖减少，证明持续学习能力。

## 7. 优点

- **统一框架**：首次将记忆、工具、反思、专家咨询等多个能力纳入一个 RL 框架端到端训练，具有通用性。
- **主动寻求建议**：新颖的设计，允许代理在不确定时主动向人类求助，并通过 RL 学习何时求助，避免了硬编码规则。
- **全面的数据集**：构建了 ProductQA，专门用于评估 LLM 代理的综合能力，涵盖长期依赖、工具使用、跨任务适应等，填补了现有基准的空白。
- **充分的消融与敏感性分析**：系统验证了各组件和 RL 的作用，以及成本参数的影响，结论可靠。
- **开源与可复现**：公开代码和数据集，实验设置详细。

## 8. 不足与局限

- **模型规模有限**：实验仅使用 7B 和 13B 的 LLM，未尝试更大模型（如 70B+），可能限制了框架在复杂规划任务上的潜力。
- **训练数据规模小**：ProductQA 仅使用 6 个产品类别训练，尽管效果显著，但更大规模的训练数据可能进一步提升性能。
- **建议成本假设理想化**：假设专家总是提供正确答案，且成本固定。实际场景中专家可能出错，成本也可能动态变化。论文未讨论这些情况。
- **跨会话依赖的近似处理**：会话级优化使用启发式状态优势函数（基于相似度计数），并不是学习得到的，可能存在偏差。
- **评估依赖 GPT-4**：长答案评估使用 GPT-4 评判，尽管与人工有 94% 一致，但仍有少数不一致风险。
- **未讨论安全与偏见**：论文在伦理部分提到移除有害数据，但未系统评估代理在对抗性输入或有害查询下的表现。
- **资源公开有限**：代码和数据集虽开源，但未提供预训练模型权重，可能影响完全复现。

（完）
