---
title: "Learning to Plan & Reason for Evaluation with Thinking-LLM-as-a-Judge"
title_zh: 学习规划与推理：思考型LLM作为评判者的评估方法
authors: "Swarnadeep Saha, Xian Li, Marjan Ghazvininejad, Jason E Weston, Tianlu Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=PNRznmmWP7"
tags: ["query:ehr-agent"]
score: 6.0
evidence: 利用LLM作为评判者进行评估规划
tldr: LLM作为评判者模型在生成评估推理时缺乏高质量思维链，且现有方法将规划与推理混合。本文提出EvalPlanner，一种面向思考型LLM评判者的偏好优化算法，先生成无约束评估计划再执行评估，使推理更系统化。该方法通用，可迁移至医疗智能体评估场景，用于基于EHR的智能体性能评判。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-pnrznmmwp7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1552, \"height\": 515, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1597, \"height\": 789, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1776, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1368, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 875, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1409, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1286, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1551, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 842, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 862, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1022, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 866, \"height\": 166, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pnrznmmwp7/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 760, \"height\": 561, \"label\": \"Table\"}]"
motivation: 现有LLM评判者缺乏结构化的评估推理过程，需要更系统的规划与推理方法。
method: 提出EvalPlanner算法，通过偏好优化使LLM先生成评估计划，再根据计划执行推理，从而解耦合规划与推理。
result: 在多个评估基准上，EvalPlanner生成的评估计划更合理且评估结果更准确。
conclusion: 该方法为通用评估提供了一种新的范式，可应用于医疗智能体的效果评估。
---

## Abstract
LLM-as-a-Judge models generate chain-of-thought (CoT) sequences intended to capture the step-by-step reasoning process that underlies the final evaluation of a response. However, due to the lack of human-annotated CoTs for evaluation, the required components and structure of effective reasoning traces remain understudied. Consequently, previous approaches often (1) constrain reasoning traces to hand-designed components, such as a list of criteria, reference answers, or verification questions and (2) structure them such that planning is intertwined with the reasoning for evaluation. In this work, we propose EvalPlanner, a preference optimization algorithm for Thinking-LLM-as-a-Judge that first generates an unconstrained evaluation plan, followed by its execution, and then the final judgment. In a self-training loop, EvalPlanner iteratively optimizes over synthetically constructed evaluation plans and executions, leading to better final verdicts. Our method achieves a new state-of-the-art performance for generative reward models on RewardBench and PPE, despite being trained on fewer amount of, and synthetically generated, preference pairs. Additional experiments on other benchmarks like RM-Bench, JudgeBench, and FollowBenchEval further highlight the utility of both planning and reasoning for building robust LLM-as-a-Judge reasoning models.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义

- **研究动机**：LLM-as-a-Judge 模型生成的链式思维（CoT）旨在捕捉评估过程的逐步推理，但由于缺乏人工标注的 CoT，有效的推理轨迹所需组件和结构尚未被充分研究。
- **现有局限**：先前方法通常 (1) 将推理轨迹限制在手设计的组件（如评估标准列表、参考答案、验证问题）上，(2) 将规划与评估推理混合在一起，导致结构僵化、泛化性差。
- **整体目标**：提出一种使 LLM 能够先规划（生成无约束评估计划）再推理（执行计划）的偏好优化方法，从而构建更健壮、可解释且数据高效的思考型 LLM 评判者。

## 2. 论文提出的方法论

- **核心思想**：将 LLM-as-a-Judge 的 CoT 解耦为三个独立组件：**评估计划（Plan）**、**计划执行（Execution）** 和 **最终判决（Verdict）**。通过自训练循环迭代优化计划和执行。

- **关键技术细节**：
    - **合成数据生成**：
        - 从 WildChat 和 MATH 中选择指令，使用“噪声指令”或正确/错误答案构造偏好对（选中的和拒绝的响应）。
        - 使用种子模型（如 Llama-3.1-70B-Instruct）**生成评估计划**：仅基于输入指令，不依赖响应对，生成无约束的、任务特定的计划。
        - 对于每个计划，**生成多个执行**：输入指令、响应对和计划，让模型逐步推理产生判决。生成时考虑两种响应顺序以消除位置偏差。
        - 构建 **偏好 CoT 对**：对于每条指令，采样多个计划和多个执行，将正确判决的 CoT 作为“选中”，错误判决的作为“拒绝”。
    - **训练流程**：
        - **SFT**：在选中的 CoT 子集上微调种子模型，得到 MSFT1。
        - **第一轮 DPO**：使用 DPO 对 MSFT1 在所有偏好 CoT 对（计划+执行+判决）上进行优化，得到 MDPO1。
        - **第二轮 DPO**：使用 MDPO1 在新指令集上重复生成计划和执行（采用更高质量的数据），再次进行 DPO 得到 MDPO2。
    - **公式化**：生成过程为 pθ(y|x,a,b) = Σz∈P Σe∈E pθ(y|e,z,x,a,b) pθ(e|z,x,a,b) pθ(z|x)，通过最大化正确 CoT 的概率进行训练。

## 3. 实验设计

- **使用数据集**：
    - **训练数据**：WildChat（17,588 条）和 MATH（4,141 条）的合成偏好对，从中选取 5K 用于第一轮，其余 17K 用于第二轮。
    - **评估基准**：
        - RewardBench（Chat、Chat-Hard、Safety、Reasoning 四个子集）
        - PPE（Preference Proxy Evaluation，含 Preference 和 Correctness 两个子集）
        - FollowBenchEval（自建，基于 FollowBench，含多级约束遵循任务）
        - RM-Bench（鲁棒性测试，分 Easy/Normal/Hard）
        - JudgeBench（知识、推理、数学、编码）

- **对比方法**：
    - 开源/闭源 LLM 作为零样本评判者（如 Llama-3.1-70B-Instruct、GPT-4o、Claude-3.5-sonnet）
    - 带有批评的奖励模型（如 SynRM、CLoud、Critic-RM-Rank）
    - 当前最优的生成式奖励模型（如 Self-Taught Evaluator、SFR-Judge、Skywork-Critic、LMUnit、DeepSeek-GRM）

## 4. 资源与算力

- **论文中未明确说明**具体使用的 GPU 型号、数量和训练时长。
- 仅提到：
    - 使用 **fairseq2** 库进行模型训练，**vLLM** 进行推理。
    - 训练超参数在附录表 12 中列出（如最大序列长度 4096、学习率 SFT 1e-6、DPO 5.5e-8、权重衰减 0.1 等）。
    - 训练在 8 个 tensor parallel size 下进行，使用 bfloat16 精度。
- **结论**：论文缺乏对计算资源的详细报告，如 GPU 类型、节点数、总训练时间等，这是实验可复现性的一个缺口。

## 5. 实验数量与充分性

- **实验数量**：
    - **主实验**：在 5 个基准（RewardBench、PPE、FollowBenchEval、RM-Bench、JudgeBench）上进行了评估。
    - **消融实验**：
        - 对比 DPO 迭代次数（1轮 vs 2轮）
        - 对比数据规模（5K vs 22K）
        - 对比计划类型（无约束计划 vs 约束为评估标准列表或验证问题）
        - 对比训练阶段（SFT vs SFT+DPO）
        - 对比计划/执行采样数量（3/5 计划 × 4/8 执行）
        - 对比指令来源（WildChat vs MATH）
        - 模型规模缩放（8B vs 70B）
- **充分性判断**：实验设计全面，覆盖了多个维度的对比和消融，方法论验证充分。self-training 循环的评估、数据效率分析、泛化性测试均较为完备。公平性方面，采用标准评估协议，并考虑了位置一致性和随机顺序，总体客观。

## 6. 论文的主要结论与发现

- **性能领先**：EvalPlanner 在 RewardBench 上达到 93.9%（使用 Llama-3.1-70B）和 93.8%（使用 Llama-3.3-70B），超越所有基线，包括使用 30 倍以上人类标注数据的模型。
- **数据高效**：仅用 5K 合成偏好对即可获得 92.3 分，与众多基线持平。
- **迭代优化的必要性**：两轮 DPO（从 92.3 提升到 93.9）显著优于单轮，说明在更新模型上生成更高质量的 CoT 至关重要。
- **无约束计划的优越性**：无约束计划（86.8%）优于约束为评估标准列表（83.9%）或验证问题（84.8%）。
- **泛化能力**：在 FollowBenchEval（多级约束遵循）上提升 13%，在 RM-Bench（鲁棒性）上提升最多 8%，在 PPE 和 JudgeBench 上也达到 SOTA 或可比水平。
- **模型规模效益**：EvalPlanner-8B 能与 70B 级大模型（如 Llama-3.1-70B-Instruct）相媲美。

## 7. 优点

- **创新性**：首次将 LLM-as-a-Judge 的 CoT 解耦为独立的规划与执行阶段，并引入自训练循环进行联合优化。
- **数据效率**：完全依赖合成数据，无需人工标注 CoT，且仅需少量偏好对即可取得优异性能。
- **泛化性与灵活性**：规划阶段不依赖特定领域的手工规则，可自动生成针对任意任务（编码、数学、安全、遵循约束）的评估计划。
- **实验严谨性**：覆盖多个主流 benchmark，进行了详细的消融分析（计划类型、迭代数、数据量、模型规模等），验证了各设计选择的有效性。
- **可解释性**：输出的 CoT 包含清晰的计划和步骤执行，提高了评估结果的透明度和可信度。

## 8. 不足与局限

- **计算资源信息缺失**：未报告具体的 GPU 型号、数量、挂壁时长，影响实验的可复现性和成本估计。
- **潜在偏见风险**：种子模型（Llama 系列）可能含有预训练数据中的偏见和刻板印象，合成数据生成过程可能放大这些偏见，论文未对公平性进行专门分析。
- **应用限制**：
    - 仅针对成对偏好评估场景，未讨论点数打分或单输出评估。
    - 自训练循环依赖于正确的合成响应对标签，对于无法自动获得金标的任务（如开放式生成）仍需人工或替代方法。
    - 未探索更多迭代（如第三轮）能否进一步提升。
- **基准覆盖局限**：虽涉及多个任务，但未在更广泛的 RLHF 奖励模型场景（如与人类偏好对齐的实际产品）中进行评估。FollowBenchEval 为自建基准，数据量较小（205 样本）。
- **安全性**：论文在影响声明中提及可能继承预训练数据的负面特性，但未提供缓解措施的具体分析或实验。

（完）
