---
title: "Position: Reinforcement Learning in Dynamic Treatment Regimes Needs Critical Reexamination"
title_zh: 立场：动态治疗方案中的强化学习需要批判性重新审视
authors: "Zhiyao Luo, Yangchen Pan, Peter Watkinson, Tingting Zhu"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=xtKWwB6lzT"
tags: ["query:ehr-agent"]
score: 9.0
evidence: 批判性审视基于EHR的RL动态治疗方案评估指标
tldr: "离线强化学习在动态治疗方案中的应用面临评估指标不一致、缺乏基线和RL公式多样化等问题。本文基于脓毒症EHR数据集进行了超过17,000次实验，系统性地揭示了现有评估框架的缺陷，并呼吁重新审视RL在DTR中的评价方法。该研究为医疗代理评估指标的选择提供了重要警示与指导。"
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 796, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 787, \"height\": 817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1761, \"height\": 397, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1770, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1592, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1759, \"height\": 1095, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1762, \"height\": 792, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1774, \"height\": 1400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1776, \"height\": 854, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1415, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1413, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1414, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1413, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1414, \"height\": 578, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1414, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1412, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1415, \"height\": 577, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1414, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1413, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1415, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1414, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1413, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-xtkwwb6lzt/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1414, \"height\": 578, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1754, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1630, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 813, \"height\": 314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1777, \"height\": 534, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1057, \"height\": 593, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1033, \"height\": 114, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 671, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 507, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 498, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1769, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1767, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1590, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1597, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1630, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1593, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1576, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1604, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1619, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1610, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1661, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1619, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1668, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1700, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1629, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1610, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1612, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1596, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1600, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1602, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1582, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1621, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 1622, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1641, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 1624, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-035.webp\", \"caption\": \"\", \"page\": 0, \"index\": 35, \"width\": 1633, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-036.webp\", \"caption\": \"\", \"page\": 0, \"index\": 36, \"width\": 1596, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-037.webp\", \"caption\": \"\", \"page\": 0, \"index\": 37, \"width\": 1584, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-038.webp\", \"caption\": \"\", \"page\": 0, \"index\": 38, \"width\": 1576, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-039.webp\", \"caption\": \"\", \"page\": 0, \"index\": 39, \"width\": 1579, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-040.webp\", \"caption\": \"\", \"page\": 0, \"index\": 40, \"width\": 1588, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-041.webp\", \"caption\": \"\", \"page\": 0, \"index\": 41, \"width\": 1614, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-042.webp\", \"caption\": \"\", \"page\": 0, \"index\": 42, \"width\": 1615, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-043.webp\", \"caption\": \"\", \"page\": 0, \"index\": 43, \"width\": 1602, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-044.webp\", \"caption\": \"\", \"page\": 0, \"index\": 44, \"width\": 1578, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-045.webp\", \"caption\": \"\", \"page\": 0, \"index\": 45, \"width\": 1622, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-xtkwwb6lzt/table-046.webp\", \"caption\": \"\", \"page\": 0, \"index\": 46, \"width\": 1691, \"height\": 328, \"label\": \"Table\"}]"
motivation: 现有RL在DTR中的评估指标不一致且缺乏基线，导致结果不可靠。
method: 通过大规模实验系统分析RL算法在EHR数据集上的评估问题。
result: 发现多种评估指标和RL公式导致评价结果矛盾，缺乏稳健性。
conclusion: 需要重新设计评估标准和实验流程以确保RL在医疗决策中的可信性。
---

## Abstract
In the rapidly changing healthcare landscape, the implementation of offline reinforcement learning (RL) in dynamic treatment regimes (DTRs) presents a mix of unprecedented opportunities and challenges. This position paper offers a critical examination of the current status of offline RL in the context of DTRs. We argue for a reassessment of applying RL in DTRs, citing concerns such as inconsistent and potentially inconclusive evaluation metrics, the absence of naive and supervised learning baselines, and the diverse choice of RL formulation in existing research. Through a case study with more than 17,000 evaluation experiments using a publicly available Sepsis dataset, we demonstrate that the performance of RL algorithms can significantly vary with changes in evaluation metrics and Markov Decision Process (MDP) formulations. Surprisingly, it is observed that in some instances, RL algorithms can be surpassed by random baselines subjected to policy evaluation methods and reward design. This calls for more careful policy evaluation and algorithm development in future DTR works. Additionally, we discussed potential enhancements toward more reliable development of RL-based dynamic treatment regimes and invited further discussion within the community. Code is available at https://github.com/GilesLuo/ReassessDTR.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 论文的核心问题与整体含义

- **研究动机**：离线强化学习（RL）在动态治疗方案（DTR）中的应用正受到关注，但现有研究存在三个关键问题：**（1）评估指标不一致且可能产生误导性结论**；（2）**缺乏简单基线（如随机策略）和监督学习基线的对比**；（3）**RL公式（MDP定义、状态/动作空间设计、奖励函数）高度多样化**，导致研究之间难以比较和复现。
- **整体含义**：论文呼吁对RL在DTR中的评估方法进行批判性重新审视，指出如果不解决这些不一致性，RL的临床部署可能带来风险。通过脓毒症病例研究，作者证明RL算法的相对性能会因评估指标和MDP公式的改变而发生显著变化，甚至有时会被随机基线超越。

## 2. 论文提出的方法论

- **核心思想**：通过大规模、系统性的实验，量化不同评估方法、奖励设计和基线选择对RL算法排名的影响，从而揭示当前评估框架的脆弱性。
- **关键技术细节**：
    - 使用**MIMIC-III数据库**构建脓毒症治疗任务，基于Sepsis-3标准提取患者轨迹，处理为4小时间隔的时序数据。
    - **状态空间**：46维连续临床变量（含生命体征、实验室指标等），使用3帧历史窗口（12小时）扁平化作为输入。
    - **动作空间**：离散的5×5动作（IV液体和血管升压药的剂量区间），共计25种组合。
    - **奖励设计**：对比三种方案：
        - **结果奖励**：最终步存活+100，死亡-100，中间步0。
        - **SOFA风险奖励**：基于SOFA评分变化和乳酸水平，加上存活/死亡终局奖励（±15）。
        - **NEWS2风险奖励**：基于归一化的NEWS2评分（死亡率概率）作为负奖励，终局奖励死亡-1，存活0。
    - **策略评估方法**：采用加权重要性采样（WIS）、带bootstrap的WIS（WIS_b）、截断WIS（WIS_t）、同时bootstrap+截断（WIS_bt）、以及双重鲁棒（DR）估计器。同时使用直接方法（DM，即Q值估计）的L1损失进行诊断。
    - **对比策略**：包括监督学习（LSTM行为克隆）、离线RL算法（DQN、CQL、IQL、BCQ），以及五种简单基线（随机、始终最小剂量、始终最大剂量、交替策略、按训练集动作频率加权的策略）。
    - **性能度量**：除OPE指标外，还包括RMSE（模拟动作与医生动作的偏差）、病人级别F1、样本级别F1、以及目标值函数估计（GD，即医生策略的OPE值作为参照）。

## 3. 实验设计

- **数据集**：**MIMIC-III 脓毒症数据集**（经预处理，排除时间序列不一致的患者）。训练/验证/测试集划分按患者分层抽样确保各组分布均衡。
- **基准与对比方法**：
    - 对照RL算法：DQN、CQL、IQL、BCQ。
    - 监督学习基线：LSTM最小化交叉熵。
    - 必要基准（Naive baselines）：随机、最小、最大、交替、加权。
    - 医生策略（GD，行为策略）作为性能参照。
- **评估场景**：
    - **3种奖励设计**（结果、SOFA、NEWS2）。
    - **9种指标**（RMSE IV、RMSE vaso、WIS、WIS_b、WIS_t、WIS_bt、DR、P.F1、S.F1）。
    - **13个患者组**（整体测试集+12个按NEWS2变化率高低方差分层的子集）。
- **实验汇总**：总计 10策略 × 9指标 × 13组 × 3奖励 = 17,550次评估；此外还包含模型校准实验、行为策略和值函数误差分析等补充实验。

## 4. 资源与算力

- **论文未明确说明使用的GPU型号、数量或训练时长**。仅提到使用线性层网络结构以减少架构影响，超参数搜索通过网格搜索在统一搜索空间进行。文中未提供具体计算资源信息。

## 5. 实验数量与充分性

- **实验数量**：主体实验多达17,550次独立评估，覆盖多种策略、指标、分组和奖励设置，规模较大。
- **充分性**：
    - **正面**：非常充分地覆盖了评估方法、奖励设计和策略的多样性，且引入分层子组分析，能暴露整体指标下的隐藏问题。补充的模型校准实验、误差分析进一步支撑结论。
    - **局限性**：
        - **仅使用一个数据集（MIMIC-III 脓毒症）**，结论的泛化性需在其他疾病或数据集上验证。
        - **所有RL算法采用线性函数近似**，未探索更先进的神经网络或表示学习方法。
        - **只考虑离散动作**，未涵盖连续动作空间（尽管提及但未实验）。
        - **未进行多重最优治疗可能性的分析**，可能忽略策略的多模态性质。
    - **客观性与公平性**：实验设计较为公平，所有RL算法共享相同模型结构、超参数搜索空间和数据划分。但部分朴素基线（如加权策略）在OPE上超越医生策略，暗示OPE方法可能存在偏差，说明评价公平性仍需谨慎对待。

## 6. 论文的主要结论与发现

1. **评估指标不一致导致结论矛盾**：同一算法在不同OPE指标下的排名差异显著，例如WIS和DR可能给出相反结论。DR方法并非“双重鲁棒”，因其在高偏差行为策略或错误值函数下反而变得“双向不鲁棒”。
2. **朴素基线意外获胜**：某些朴素策略（如加权随机策略）在整体测试集或子组中的OPE指标上优于甚至超越所有RL算法和医生策略，揭示了当前OPE方法可能存在严重偏差，不能仅依赖OPE值判断策略优劣。
3. **RL与监督学习对比复杂**：RL在OPE上优于SL时，并不总能翻译为更好的RMSE或F1；反之，SL在OPE上看似弱于RL时，在监督指标上可能相近或更优。需要同时分析两类指标。
4. **奖励设计显著影响算法排序**：不同奖励设置下，最优算法变化极大。例如DQN在NEWS2奖励上获胜次数最多，CQL在结果奖励上获胜最多，而SOFA奖励下所有RL算法获胜次数均少于SL。
5. **分层分析揭示隐藏差异**：整体测试集上的排名并不能代表所有患者子组的表现。某些RL算法（如CQL）在特定高风险快速改善的子组上显著优于SL，显示了RL的潜在价值；但整体上算法排名不稳定。
6. **行为策略和值函数估计误差是OPE方差的重要来源**：重要性采样中小概率与高损失的负相关、Q值估计中终端奖励过大导致的误差集中，都会影响OPE可靠性。模型校准可能加剧而非缓解此问题。

## 7. 优点

- **提出明确的批判性立场**：系统梳理了RL-DTR领域存在的三个关键问题（评估指标、基线、MDP公式），并给出实证支持，对社区具有警示和指导意义。
- **大规模、多维度的实验设计**：17,550次评估覆盖策略、指标、分组、奖励四维度，结论稳健，且引入分层分析，揭示了整体评估无法发现的差异。
- **关注医疗特殊性**：针对医疗场景的高风险和评估困难，强调了朴素基线和不合理OPE的潜在危害。
- **提供实用建议**：如必须包含SL基线、必须进行数据分层、谨慎使用模型校准、开发更适应DTR的OPE方法等，具有较强的实践指导价值。
- **开源代码**：便于复现和进一步研究。

## 8. 不足与局限

- **数据集单一**：仅用MIMIC-III脓毒症数据，结论是否适用于其他疾病（如糖尿病、心理健康、癌适应症）尚需验证。
- **函数近似简化**：仅使用线性层，未探索更先进的表示学习方法（如RNN、因果推断、多模态建模）。线性近似可能限制RL最终性能，同时也可能影响OPE估计的准确性。
- **忽略连续动作空间**：现有大量DTR研究已探索连续动作，本文仅讨论离散动作，结论对连续域的适用性未知。
- **未考虑多模态策略**：可能存在多个同等最优的治疗方案。SL可能拟合训练数据中的主流模式，而RL可能学习到不同模式，导致两者性能比较不公。论文未对此进行实验控制或讨论。
- **未与其他先进OPE方法对比**：如高置信区间界限、方差缩减方法等，仅使用了标准WIS/DR变体，可能未覆盖当前OPE的全部手段。
- **模型校准分析不深入**：仅测试了温度缩放一种校准方法，未探索其他校准技术（如保序回归、贝叶斯校准），结论“校准可能无帮助”需谨慎推广。
- **分层标准主观**：仅基于NEWS2变化率的分层，未探讨初始状态分层等其他合理方式。

（完）
