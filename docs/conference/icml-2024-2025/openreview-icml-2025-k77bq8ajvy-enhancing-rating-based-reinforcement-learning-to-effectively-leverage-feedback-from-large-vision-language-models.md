---
title: Enhancing Rating-Based Reinforcement Learning to Effectively Leverage Feedback from Large Vision-Language Models
title_zh: 增强基于评分的强化学习以有效利用大视觉语言模型的反馈
authors: "Tung Minh Luu, Younghwan Lee, Donghoon Lee, Sunho Kim, Min Jun Kim, Chang D. Yoo"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=k77bq8AJVy"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 从AI反馈的强化学习用于奖励学习，可应用于医疗智能体评估
tldr: 该论文提出ERL-VLM，一种增强的基于评分的强化学习方法，利用大视觉语言模型提供的AI反馈来学习奖励函数。相比人工反馈，该方法降低了对人类标注的依赖，并通过查询具体评分而非成对比较来提升效率。在多个任务上展示了有效性。该方法可直接用于医疗智能体的奖励建模与评估，减少对专家反馈的依赖。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1419, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 848, \"height\": 731, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1769, \"height\": 269, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1774, \"height\": 708, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1679, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1680, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1087, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1754, \"height\": 156, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1277, \"height\": 654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1282, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1281, \"height\": 641, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1626, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1777, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1477, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1771, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1479, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 200, \"height\": 201, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 200, \"height\": 202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 199, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 199, \"height\": 197, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 199, \"height\": 201, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 199, \"height\": 204, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 200, \"height\": 199, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1663, \"height\": 237, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1666, \"height\": 152, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1036, \"height\": 164, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1670, \"height\": 137, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1658, \"height\": 213, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1219, \"height\": 171, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1546, \"height\": 132, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1545, \"height\": 123, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 1130, \"height\": 130, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1783, \"height\": 2019, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-k77bq8ajvy/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 1615, \"height\": 2285, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 874, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1771, \"height\": 1012, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 780, \"height\": 756, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 957, \"height\": 887, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 797, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1748, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1749, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1750, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1749, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-k77bq8ajvy/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1749, \"height\": 268, \"label\": \"Table\"}]"
motivation: 强化学习依赖人工奖励设计，成本高且难以扩展。
method: 利用大视觉语言模型生成反馈，通过查询评分的方式学习奖励函数。
result: 在多个连续控制环境中优于依赖人工反馈的基线方法。
conclusion: AI反馈可作为人类反馈的替代，降低强化学习奖励学习的成本。
---

## Abstract
Designing effective reward functions remains a fundamental challenge in reinforcement learning (RL), as it often requires extensive human effort and domain expertise. While RL from human feedback has been successful in aligning agents with human intent, acquiring high-quality feedback is costly and labor-intensive, limiting its scalability. Recent advancements in foundation models present a promising alternative--leveraging AI-generated feedback to reduce reliance on human supervision in reward learning. Building on this paradigm, we introduce ERL-VLM, an enhanced rating-based RL method that effectively learns reward functions from AI feedback. Unlike prior methods that rely on pairwise comparisons, ERL-VLM queries large vision-language models (VLMs) for absolute ratings of individual trajectories, enabling more expressive feedback and improved sample efficiency. Additionally, we propose key enhancements to rating-based RL, addressing instability issues caused by data imbalance and noisy labels. Through extensive experiments across both low-level and high-level control tasks, we demonstrate that ERL-VLM significantly outperforms existing VLM-based reward generation methods. Our results demonstrate the potential of AI feedback for scaling RL with minimal human intervention, paving the way for more autonomous and efficient reward learning.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

强化学习（RL）的成功高度依赖于奖励函数的设计，传统上需要大量人工和领域专业知识来手动定义和调整奖励函数，这一过程耗时且容易出错。近年来，从人类反馈中学习奖励（RLHF）取得了显著进展，但高质量人类反馈的获取成本高昂、劳动密集，限制了其可扩展性。随着大型视觉-语言模型（VLM）的快速发展，其展示出与人类判断高度对齐的能力，为利用AI生成的反馈替代人类监督提供了新途径。论文旨在解决如何有效利用VLM的AI反馈来学习奖励函数，从而减少对人工设计的依赖，提升RL的可扩展性和自主性。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
论文提出**ERL-VLM**（Enhanced Rating-based RL from VLM feedback），通过查询大型VLM（如Gemini）对单个轨迹段进行**绝对评分**（而非成对比较），利用评分反馈训练奖励函数，进而用于策略学习。

### 关键技术细节
- **评分生成**：采用两阶段提示：首先让VLM分析轨迹段（包含连续图像及动作），然后基于Likert量表（如“坏”、“平均”、“好”）给出绝对评分。相比于偏好比较，绝对评分提供更丰富信息，避免查询歧义，且所有采样样本均可利用。
- **奖励学习**：基于评分数据集，训练奖励模型 $\hat{r}_\psi$ 使其预测的评分分布匹配真实评分分布。使用概率评分模型（公式1）将累积回报映射为各评分类别的概率。
- **针对不稳定性增强**：
  - **分层采样**（Stratified Sampling）：训练批次中保证每个评分类别都有样本，缓解数据不平衡。
  - **加权损失**：根据类别频率加权损失，进一步平衡样本。
  - **平均绝对误差（MAE）损失**（公式3）：替代交叉熵损失，对VLM的噪声标签具有鲁棒性。
- **训练流程**：每 $K$ 步查询VLM，更新奖励模型，重新标记回放缓冲区中的经验，然后使用任意离策略RL算法（如SAC、IQL）更新策略。

## 3. 实验设计

### 使用场景/数据集
- **MetaWorld**：3个低层连续控制任务（Sweep Into、Drawer Open、Soccer），使用图像观测和语言任务描述。
- **ALFRED**：高层视觉语言导航任务，包含4类20个子任务（PickupObject, PutObject, CoolObject, CleanObject），多任务学习。
- **真实机器人**：使用Sawyer机械臂的3个桌面操作任务（Sweep Bowl, Drawer Open, Pickup Banana）。

### Benchmark与方法对比
- **CLIP Score**：利用CLIP嵌入相似度作为奖励。
- **RoboCLIP Score**：基于S3D视频嵌入的相似度。
- **RL-VLM-F**：基于偏好比较的VLM反馈方法（类似方法）。
- **Environment Reward**：使用环境原始奖励（MetaWorld为密集，ALFRED为稀疏）作为上界。

### 评价指标
- 成功率（Success Rate），每个评估运行计算10个（MetaWorld）或100个（ALFRED）episodes的平均值，报告3次运行的均值和标准差。

## 4. 资源与算力

论文**未明确说明**使用的GPU型号、数量及训练时长等算力信息。仅在附录中提及训练超参数（如步数、批量大小等），但未提供硬件配置。因此无法总结具体算力开销。

## 5. 实验数量与充分性

- **实验数量**：在3个领域（模拟连续控制、模拟导航、真实机器人）共进行7个模拟任务（MetaWorld 3个，ALFRED 4类聚合）+ 3个真实任务，总计10个直接对比实验。此外包含详细的消融研究（4个变体对比）、不同评分类别数（n=2,3,4）、标签平滑对比、MAE在偏好学习中的影响等。
- **充分性与公平性**：实验设计较为充分，覆盖了低层连续和高层离散动作空间以及真实场景。对比基线包括传统相似度方法和同类VLM反馈方法，超参数保持一致（仅奖励函数不同）。消融实验清晰地验证了各增强模块的贡献。不足在于：未在更多样化或大规模任务上测试（如复杂长时任务），且未与人类反馈方法进行直接成本比较。

## 6. 主要结论与发现

- ERL-VLM在所有7个模拟任务中的6个上**显著优于**所有基线，尤其在ALFRED任务中表现突出，甚至超过稀疏环境奖励。
- 绝对评分相比于偏好比较在相同查询预算下提供更丰富信息，样本效率更高。
- 提出的增强（分层采样、MAE损失）有效解决了数据不平衡和噪声标签导致的训练不稳定问题，每项增强都贡献了性能提升。
- 在真实机器人实验中，ERL-VLM训练的奖励函数显著优于行为克隆和稀疏奖励方法。
- 不同评分类别数对性能有影响：二分类在二元任务中更好，三分类在主观性更强的任务中更优，四分类导致性能下降（歧义增加）。

## 7. 优点

- **方法创新**：将VLM绝对评分用于奖励学习，避免了偏好比较的歧义和样本浪费，提升了数据利用效率。
- **实用性强**：仅需语言任务描述和图像观测，无需特权状态信息或环境源码，易于迁移到新任务。
- **增强设计有效**：针对评分反馈中数据不平衡和噪声标签提出了简单但有效的改进（分层采样+MAE损失），实验结果证实了其必要性。
- **实验全面**：覆盖模拟和真实环境，包括低层连续控制和高层导航任务，包含充分的消融和敏感性分析，验证了方法鲁棒性。

## 8. 不足与局限

- **算力未报告**：缺少GPU型号、数量及训练时间等关键资源信息，影响可复现性和实际部署评估。
- **实验覆盖有限**：仅在MetaWorld和ALFRED部分任务上测试，未在更复杂或多样化环境（如多机器人、长时任务、动态环境）中验证。
- **标签噪声处理依赖VLM质量**：VLM可能产生幻觉或不一致评分，虽然MAE损失缓解了部分噪声，但当评分严重错误时仍可能误导训练。
- **评分类别数选择不明确**：论文指出不同任务需要不同类别数，但缺乏自动化选择机制，依赖人工试错。
- **与人类反馈比较不足**：未定量比较ERL-VLM与同等预算下人类反馈的性能差异，也无法判断AI反馈是否完全可替代人类。
- **潜在偏差风险**：VLM本身携带的偏见可能通过评分传播到奖励函数，导致智能体学习到不安全或有偏行为，论文仅在影响声明中提及而未进行系统评估。

（完）
