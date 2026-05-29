---
title: "Reinforcement Learning for Out-of-Distribution Reasoning in LLMs: An Empirical Study on Diagnosis-Related Group Coding"
title_zh: 强化学习用于大语言模型分布外推理：诊断相关分组编码的实证研究
authors: "Hanyin Wang, Zhenbang Wu, Gururaj J. Kolar, Hariprasad Reddy Korsapati, Brian Bartlett, Bryan Hull, Jimeng Sun"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=0jvnfH0WYV"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 使用强化学习和大型语言模型进行临床编码
tldr: 针对大型语言模型在诊断相关分组编码任务中面临的数据分布外挑战，提出了DRG-Sapphire框架，采用大规模强化学习（GRPO算法）和基于规则的奖励机制，在Qwen2.5-7B模型上实现自动化临床编码，克服了标注数据稀缺问题，取得了最先进的编码准确率，展示了强化学习在医疗任务中的潜力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1397, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1375, \"height\": 204, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 801, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 508, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1441, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1443, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 726, \"height\": 298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1441, \"height\": 353, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 723, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 959, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0jvnfh0wyv/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 505, \"height\": 414, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-0jvnfh0wyv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 940, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0jvnfh0wyv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1427, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0jvnfh0wyv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1457, \"height\": 791, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0jvnfh0wyv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 998, \"height\": 315, \"label\": \"Table\"}]"
motivation: 大型语言模型在医疗编码任务中因缺乏私密临床数据而表现不佳，需高效自动化方法。
method: 基于Qwen2.5-7B模型，采用GRPO强化学习算法与规则奖励，引入针对医疗领域的RL增强策略。
result: 在DRG编码任务上取得最先进准确率，验证了RL提升医疗编码性能的有效性。
conclusion: 强化学习能有效提升大语言模型在医疗编码领域的分布外推理能力。
---

## Abstract
Diagnosis-Related Group (DRG) codes are essential for hospital reimbursement and operations but require labor-intensive assignment. Large Language Models (LLMs) struggle with DRG coding due to the out-of-distribution (OOD) nature of the task: pretraining corpora rarely contain private clinical or billing data. We introduce DRG-Sapphire, which uses large-scale reinforcement learning (RL) for automated DRG coding from clinical notes. Built on Qwen2.5-7B and trained with Group Relative Policy Optimization (GRPO) using rule-based rewards, DRG-Sapphire introduces a series of RL enhancements to address domain-specific challenges not seen in previous mathematical tasks. Our model achieves state-of-the-art accuracy on the MIMIC-IV benchmark and generates physician-validated reasoning for DRG assignments, significantly enhancing explainability. Our study further sheds light on broader challenges of applying RL to knowledge-intensive, OOD tasks. We observe that RL performance scales approximately linearly with the logarithm of the number of supervised fine-tuning (SFT) examples, suggesting that RL effectiveness is fundamentally constrained by the domain knowledge encoded in the base model. For OOD tasks like DRG coding, strong RL performance requires sufficient knowledge infusion prior to RL. Consequently, scaling SFT may be more effective and computationally efficient than scaling RL alone for such tasks.

---

## 论文详细总结（自动生成）

# 论文结构化总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：诊断相关分组（DRG）编码是医院报销与运营的核心环节，但目前依赖人工专业编码员，成本高、效率低。大型语言模型（LLM）在DRG编码上表现不佳，主要原因在于该任务是典型的**分布外（OOD）推理任务**——LLM的预训练语料几乎不包含私密的临床记录和计费数据，导致模型缺乏相关领域知识。
- **研究目标**：探索如何利用大规模强化学习（RL）使LLM在OOD任务上具备有效推理能力，并以DRG编码为实证案例，同时揭示RL在知识密集型OOD任务中的一般性规律。
- **整体意义**：
  - 首次将大规模RL（GRPO）成功应用于自动化DRG编码，获得新的最先进（SOTA）性能。
  - 生成的思维链（CoT）推理经医生验证具有临床帮助性，显著提升了可解释性。
  - 揭示了RL在OOD任务中的根本约束：RL性能受限于基座模型在RL前已编码的知识量，且RL性能与SFT样本数的对数呈线性关系，暗示对于OOD任务，扩展SFT比单独扩展RL更有效、更计算高效。

## 2. 方法论：核心思想、关键技术细节

- **整体架构（DRG-Sapphire）**：
  - 基座模型：Qwen2.5-7B-Instruct。
  - 训练流程三阶段：
    1. **冷启动数据构建**：用Qwen2.5-7B-Instruct根据临床笔记和真实DRG代码生成CoT推理（经提示工程和人工检查）。
    2. **监督微调（SFT）**：在冷启动数据上微调基座模型，注入DRG领域知识。
    3. **大规模强化学习（GRPO）**：使用基于规则的奖励进行GRPO训练，优化策略。

- **核心算法：GRPO（Group Relative Policy Optimization）**
  - 与PPO不同，GRPO去掉价值函数，利用组内相对奖励估计优势，且论文强制严格on-policy（πθold = πθ）。
  - 优化目标（公式1）：
    \[
    J_{GRPO}(\theta) = \mathbb{E}\left[\frac{1}{G}\sum_{i=1}^{G}\frac{1}{|o_i|}\sum_{t=1}^{|o_i|}\left(\hat{A}_{i,t} - \beta\left(\frac{\pi_{ref}}{\pi_{\theta}} - \log\frac{\pi_{ref}}{\pi_{\theta}} - 1\right)\right)\right]
    \]
  - 优势 \(\hat{A}_{i,t}\) 为组内标准化奖励。

- **RL增强策略（针对医疗领域特有挑战）**：
  - **动态重采样**：当一组生成获得相同奖励时，重新采样多次直到方差非零，但实验发现效果不佳且增加计算。
  - **认知行为干预**：
    - Answer-First、CoT-First、Differential Thinking三种模式。实验显示Answer-First自然收敛并取得最佳性能（与直接预测策略一致）。
  - **KL散度衰减**：余弦衰减KL系数β至零，防止过正则化；移除KL penalty易导致训练崩溃（与数学任务不同）。
  - **GRPO变体**：对比了Vanilla GRPO、DAPO Loss、Dr.GRPO Loss、Dr.GRPO Advantage。DAPO Loss最优，Dr.GRPO Loss最差。
  - **奖励塑形**：尝试了Dense、Balanced、Strict三种准确率奖励。Strict奖励（最稀疏）反而最优，避免局部最优。
  - **课程学习**：去掉简单/困难样本，仅保留中等难度样本效果较好。
  - **分阶段学习**：分三阶段，每阶段后对困难样本进行额外SFT或DPO，改进有限。

## 3. 实验设计

- **数据集**：
  - **主数据集**：MIMIC-IV（公开真实医疗记录），使用“brief hospital course”部分作为输入，MS-DRG代码合并至版本34.0。
  - 训练集：236,192例；测试集：26,244例。
  - 子集DRG-Small：20%数据（46,758例），用于方法论变体和数据配比实验。

- **基准方法**：
  - 分类模型：ClinicalBERT, CAML, DRG-LLaMA-7B（此前SOTA）。
  - 生成式模型：GPT-4o, o3-Mini, R1-Distill-Qwen-32B。
  - 对比DRG-LLaMA-7B（之前最优）。

- **评价指标**：
  - Pass@1（准确率，8次生成取平均）、Pass@8（正确代码出现在8次生成中）、Maj@8（多数投票对应正确DRG）。
  - 专家读者研究：4位医生对30例推理进行帮助性和准确性评级（1-5分）。

- **实验分组**：
  1. **数据分配实验**：在DRG-Small上变化SFT与GRPO比例（5%→100% SFT），对比SFT vs SFT+GRPO的Pass@1/8/Maj@8和训练时间。
  2. **全数据集缩放实验**：在完整236k样本上，以50%、75%、90%、95% SFT比例训练，并使用最佳配置（DAPO损失+严格奖励+KL衰减）和课程学习。
  3. **消融实验**：在DRG-Small子集上（1% SFT冷启动，即2,362样本），对动态重采样、认知行为、KL散度、GRPO变体、奖励塑形、课程学习、分阶段学习七大方向进行逐一消融。
  4. **前置条件实验**：探索模型大小、SFT学习率/ epoch数量对后续RL的影响。
  5. **专家评估**：4名医生评估DRG-Sapphire推理质量。

## 4. 资源与算力

- **硬件**：
  - SFT：4块 H100 或 A100 GPU（根据可用性），DeepSpeed ZeRO Stage 3。
  - GRPO：3-5块 H100 或 A100 GPU，使用时bf16精度，使用vLLM推理和TRL GRPO Trainer。
- **训练时间（摘自Figure 5F）**：
  - 在DRG-Small子集（46,758例）上，不同SFT比例对应的总训练时间：
    - 5% SFT + 95% GRPO：约80小时（其中SFT短，GRPO长）
    - 25% SFT + 75% GRPO：约50小时
    - 50% SFT + 50% GRPO：约40小时
    - 75% SFT + 25% GRPO：约30小时
    - 100% SFT（无RL）：约20小时
  - GRPO是主要耗时环节，SFT相对便宜。
- **全局批次**：64个独特prompt × 8生成（共512条），梯度累积更新。
- **估算总计算量**：论文未给出精确GPU小时数，但可估算约数百至上千GPU小时（全数据集实验更大）。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验组约6种SFT比例，每比例下对比SFT vs 多种GRPO变体（约5种配置），加上全数据集7种配置（约50个独立运行）。
  - 消融实验覆盖7大类、约20个变体（每个变体都有训练曲线和最终指标）。
  - 额外前置条件实验（模型大小、学习率/epoch）和专家评估。
- **充分性与公平性**：
  - 消融实验均在同一子集（DRG-Small）上进行，控制变量扎实。
  - 全数据集实验验证了缩放规律，并与DRG-LLaMA等强基线公平对比。
  - 专家评估采用盲评（30例），四位医生独立评分，结果以中位数4/5呈现，有一定统计意义。
  - **局限**：仅使用单一数据集MIMIC-IV（虽补充了内部数据集验证，但内部数据仅2500例且按MIMIC频率采样），泛化性有待更多外部验证；未与更多RL算法（如PPO、REINFORCE）直接对比；Pass@1/8/Maj@8的随机性通过多次采样均值和标准差报告，但未进行显著性检验。

## 6. 主要结论与发现

1. **DRG-Sapphire达到新SOTA**：在MIMIC-IV测试集上准确率54.8%，超过前SOTA DRG-LLaMA-7B（53.9%）以及GPT-4o、o3-Mini等闭源模型，且提供可解释推理。
2. **RL性能与SFT样本数呈对数线性关系**：在固定总数据预算下，RL提升幅度随SFT样本数增加而增大，但边际递减。对于OOD任务，提高SFT数据量比单纯增加RL步数更有效。
3. **RL主要增强已知能力而非创造新能力**：RL提升Pass@1和Maj@8，但降低Pass@8，说明RL使输出分布向高奖励路径集中，而非增加探索多样性。
4. **KL散度在医疗OOD任务中至关重要**：移除KL penalty易导致训练崩溃，与数学任务（可移除KL）形成鲜明对比。使用余弦衰减策略有益。
5. **Answer-First认知模式自然涌现**：鼓励CoT-First或Differential Thinking反而降低性能，表明DRG编码可能从“先预测再推理”策略中受益。
6. **RL增强策略整体收益有限**：相比简单从更强的SFT基线初始化RL，各种RL算法增强仅带来微小改进（约1-2%绝对准确率），再次印证“苦涩教训”：对于OOD任务，知识注入比RL技巧更关键。
7. **完成长度收缩**：RL训练中生成长度显著下降后稳定，不同于数学任务中长度增长趋势。

## 7. 优点

- **首创性**：首次将大规模GRPO应用于医疗编码这一高难度OOD任务，并在7B模型上取得超越GPT-4o等大模型的效果。
- **系统性探索**：对RL训练中的多个维度（数据分配、奖励设计、KL调度、GRPO变体、认知模式、课程学习）进行了全面消融，提供了可复现的经验法则。
- **可解释性突破**：生成的CoT推理经医生验证具有临床帮助性（中位数4/5），解决了传统分类模型无法提供解释的痛点。
- **洞察深刻**：揭示出RL在OOD任务中的根本限制——依赖基座模型已有知识，并量化了SFT→RL的知识迁移效率，为后续研究提供了原则性指导。
- **实验完整性**：从子集到全数据集，从消融到缩放分析，从自动指标到人工评估，形成完整证据链。

## 8. 不足与局限

- **数据集单一**：主要实验仅基于MIMIC-IV（美国单中心ICU数据），虽补充内部数据集但规模小且分布模仿MIMIC，真实世界多样性（不同地区、不同编码版本）未验证。
- **缺乏过程监督**：仅使用最终DRG代码的规则奖励，未对推理步骤进行过程奖励建模，可能限制了模型探索更优推理路径。
- **课程学习静态**：只进行一次性难度过滤，未采用动态在线难度筛选，可能不是最优策略。
- **RL提升有限**：尽管达到SOTA，但绝对提升（约1%）相对于庞大计算投入（数百GPU小时）仍显有限，实际部署收益存疑。
- **Pass@8下降**：RL损害了多样性，可能不利于需要多次尝试的辅助场景（如医生查看多个候选）。
- **未跨领域验证**：仅针对DRG编码，结论（如SFT重要性、KL敏感性）是否适用于其他OOD任务（如法律、金融）尚需更多证据。
- **计算开销大**：GRPO训练需要大量采样和推理，对于资源受限团队复制困难；论文未给出完整训练的总GPU小时数，影响可复现性。
- **误差分析显示深层挑战**：最终模型仍有大量错误（如32%因难以选择正确基DRG、25%因CC/MCC错误），说明DRG编码的固有困难未被完全克服。

（完）
