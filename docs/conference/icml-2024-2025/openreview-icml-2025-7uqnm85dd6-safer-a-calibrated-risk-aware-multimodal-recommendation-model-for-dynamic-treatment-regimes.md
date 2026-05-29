---
title: "SAFER: A Calibrated Risk-Aware Multimodal Recommendation Model for Dynamic Treatment Regimes"
title_zh: SAFER：一种用于动态治疗方案的校准风险感知多模态推荐模型
authors: "Yishan Shen, Yuyang Ye, Hui Xiong, Yong Chen"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=7UqNM85dD6"
tags: ["query:ehr-agent"]
score: 8.0
evidence: 使用EHR的医疗代理用于治疗推荐
tldr: 针对动态治疗方案中的治疗推荐问题，现有方法主要依赖结构化EHR数据而忽略临床笔记。本文提出SAFER，一种校准的风险感知多模态推荐框架，同时整合结构化EHR和临床笔记，并通过风险校准确保推荐安全。实验表明SAFER在推荐准确性和安全性上优于基线模型，为精准医疗中的实时决策提供了可靠工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1597, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 830, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1689, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1685, \"height\": 318, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 927, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1747, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1747, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1129, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1125, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1126, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-7uqnm85dd6/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 757, \"height\": 457, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-7uqnm85dd6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7uqnm85dd6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1753, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7uqnm85dd6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1004, \"height\": 158, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-7uqnm85dd6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1834, \"height\": 285, \"label\": \"Table\"}]"
motivation: 现有动态治疗方案推荐模型未充分利用临床笔记，且缺乏风险校准，导致推荐不安全。
method: 提出SAFER框架，融合结构化EHR与临床笔记，通过风险感知校准实现安全推荐。
result: 在真实数据集上，SAFER在推荐准确性和风险控制方面优于现有方法。
conclusion: 多模态EHR数据与风险校准的结合能有效提升治疗方案推荐的安全性与可靠性。
---

## Abstract
Dynamic treatment regimes (DTRs) are critical to precision medicine, optimizing long-term outcomes through personalized, real-time decision-making in evolving clinical contexts, but require careful supervision for unsafe treatment risks. Existing efforts rely primarily on clinician-prescribed gold standards despite the absence of a known optimal strategy, and predominantly using structured EHR data without extracting valuable insights from clinical notes, limiting their reliability for treatment recommendations. In this work, we introduce SAFER, a calibrated risk-aware tabular-language recommendation framework for DTR that integrates both structured EHR and clinical notes, enabling them to learn from each other, and addresses inherent label uncertainty by assuming ambiguous optimal treatment solution for deceased patients. Moreover, SAFER employs conformal prediction to provide statistical guarantees, ensuring safe treatment recommendations while filtering out uncertain predictions. Experiments on two publicly available sepsis datasets demonstrate that SAFER outperforms state-of-the-art baselines across multiple recommendation metrics and counterfactual mortality rate, while offering robust formal assurances. These findings underscore SAFER’s potential as a trustworthy and theoretically grounded solution for high-stakes DTR applications.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：在动态治疗方案（DTR）中，如何安全地、自适应地为患者提供个性化的序贯治疗推荐，尤其是在高风险的临床场景下。现有方法存在三大局限：① 缺乏对不确定性的量化与控制；② 过度依赖结构化EHR数据，忽略了临床笔记中丰富的文本信息；③ 对治疗标签（尤其是死亡患者的标签）的固有不确定性问题缺乏有效处理。
- **研究动机**：精准医疗需要实时、个性化的决策，但最优治疗策略往往未知，且死亡患者的治疗标签可能并不可靠。因此，有必要构建一个能整合多模态数据、量化不确定性并提供统计保障的推荐框架。
- **整体含义**：提出SAFER模型，旨在成为高维决策场景下可信、理论扎实的解决方案。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：构建一个端到端的多模态、风险感知的DTR框架，通过整合结构化EHR和临床笔记、显式建模标签不确定性、以及使用顺应预测（Conformal Prediction）控制错误发现率（FDR），实现安全推荐。
- **关键技术细节**：
  1. **多模态表示学习**：使用Transformer架构，对结构化EHR（编码为嵌入）和临床笔记（通过BioClinicalBERT编码）分别提取特征，通过自注意力机制捕获时序依赖，通过交叉注意力融合跨模态信息，得到统一的患者表示。
  2. **不确定性感知训练**：假设死亡患者的治疗标签存在歧义（可能不正确），而存活患者标签相对可靠。设计一个基于多层感知机（MLP）的不确定性量化模块，仅用存活患者训练，然后计算该模块与主预测模块输出分布的KL散度作为不确定性分数κ。将κ引入风险感知损失函数：L = -1/N Σ (1-κ̂) y log pθ + γ κ²，其中κ̂是归一化分数，γ控制正则强度。
  3. **理论保证**：利用顺应预测构造p值，并通过Benjamini-Hochberg（BH）过程控制FDR ≤ α，保证推荐集合中错误推荐的比例在期望上不超过预设阈值。
- **算法流程**：训练 → 计算校准集和测试集的不确定性分数 → 计算顺应p值 → BH过程选择推荐子集。

### 3. 实验设计：使用的数据集/场景、benchmark、对比方法
- **数据集**：两个公开脓毒症数据集——MIMIC-III（约40000次ICU住院）和MIMIC-IV（约65000次ICU住院），均按Sepsis-3标准定义队列，提取入院前24小时至脓毒症发作后48小时的数据。治疗动作空间为5×5的25类（静脉输液和血管升压药剂量组合）。
- **场景**：动态治疗推荐任务，预测下一个4小时窗口的治疗措施。
- **对比方法**：
  - 序列嵌入方法：LSTM、RETAIN、TAHDNet。
  - 强化学习方法：Naive RL、SRL-RNN、ACIL、ISL。
  - 消融变体：SAFER-F（去掉风险感知微调）、SAFER-N（去掉临床笔记）、SAFER-U（仅用存活患者训练）。
- **评估指标**：Micro AUC、Macro AUC、HR@3、MRR@3，以及反事实死亡率降低（通过额外LSTM模型估计推荐治疗后的死亡率与真实死亡率的差异）。

### 4. 资源与算力
- **文中未明确说明**使用了何种GPU、数量、训练时长等算力信息。仅提及使用BioClinicalBERT（预训练模型）和MLP等，但未报告计算资源细节。

### 5. 实验数量与充分性
- **实验数量**：主要包括：
  - 在两个数据集上的整体性能对比（主表1）。
  - 三个消融实验（表2）。
  - FDR控制的验证实验：两个数据集×四种不确定性阈值×多种α水平（图3、图4），以及分别使用Ridge Regression和Linear Regression的结果（附录C.2）。
  - 超参数敏感性分析：历史序列长度、隐藏维度、γ值（附录C.3）。
  - 病例分析：不确定度随时间变化趋势（附录C.4）。
- **充分性与公平性**：实验设计较为全面，对比方法覆盖了序列嵌入和强化学习两大类，并控制了数据来源一致性（所有方法均接入相同的多模态输入）。评估指标多样，包括分类、排序和临床意义（反事实死亡率）。消融实验验证了各模块贡献。但未进行跨数据集泛化测试（仅在两个MIMIC子集上），且未与最新多模态大模型或医疗专用语言模型对比。

### 6. 论文的主要结论与发现
- SAFER在分类和排序指标上全面优于所有基线方法，尤其在Macro AUC和反事实死亡率降低上提升显著。
- FDR控制实验表明：SAFER能在指定α水平下严格控制FDR，同时保持高检验力（power）。
- 消融实验证实：风险感知微调、临床笔记融合、以及包含死亡患者训练均是性能提升的关键。
- 不确定性分数的时间趋势显示：死亡患者的不确定度随病情恶化上升，而存活患者保持稳定，验证了模型对标签不确定性建模的有效性。

### 7. 优点：方法或实验设计上的亮点
- **方法创新性**：首次将不确定性量化与顺应预测引入DTR领域，提供统计保障，增强高安全关键场景的可信度。
- **多模态融合**：同时利用结构化EHR和临床笔记，通过交叉注意力有效融合，更贴近临床真实决策过程。
- **标签不确定性处理**：通过可学习的KL散度量化标签歧义，并用风险感知损失缓解噪声影响，而非简单丢弃死亡患者数据。
- **实验设计**：反事实死亡率评估体现了对临床实际效果的关注，而不仅仅是离线指标。超参数分析全面，FDR控制验证细致。
- **代码开源**：提供GitHub仓库，有利于复现和进一步研究。

### 8. 不足与局限
- **实验覆盖**：仅使用两个脓毒症数据集，未在其他疾病（如糖尿病、心血管疾病）或更广泛EHR数据库上验证，泛化性存疑。
- **偏差风险**：反事实死亡率估计基于潜在结果假设（无干扰、无未测量混杂、正则性），在实际应用中这些假设可能不成立，导致估计偏差。
- **应用限制**：
  - 需要高质量临床笔记和结构化数据同步，实际中数据缺失或不完整可能影响性能。
  - 治疗动作仅离散为25类，粒度较粗，可能忽略连续剂量信息。
  - 未考虑用药组合相互作用（DDI）和长期副作用。
- **计算资源未报告**：缺乏对模型训练成本的说明，不利于资源受限场景的预判。
- **与最新方法的对比不足**：未与当前热门的医疗大语言模型（如GPT-4, MedPaLM）或更先进的推荐方法（如GAMENet, SafeDrug）比较，虽然这些方法可能不直接针对DTR。

（完）
