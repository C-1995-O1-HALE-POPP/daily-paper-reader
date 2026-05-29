---
title: Offline Guarded Safe Reinforcement Learning for Medical Treatment Optimization Strategies
title_zh: 面向医疗治疗优化策略的离线受保护安全强化学习
authors: "Runze Yan, Xun Shen, Akifumi Wachi, Sebastien Gros, Anni Zhao, Xiao Hu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=4P6Mployhf"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 离线安全强化学习用于医疗治疗优化，与医疗代理评估相关
tldr: 该论文针对离线强化学习在医疗场景中的分布外问题，提出一种受保护的安全强化学习方法，通过约束动作和状态轨迹来安全改进策略，避免有害推荐。该方法可直接用于医疗代理的策略评估，确保推荐的安全性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 714, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1295, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1362, \"height\": 1659, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1362, \"height\": 1662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1429, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1429, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1429, \"height\": 754, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1400, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1427, \"height\": 750, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1392, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1396, \"height\": 312, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4p6mployhf/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1395, \"height\": 312, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1398, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1008, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1455, \"height\": 718, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1414, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4p6mployhf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1262, \"height\": 461, \"label\": \"Table\"}]"
motivation: 离线强化学习在医疗场景中存在分布外问题，可能导致有害推荐，需要更安全的策略优化方法。
method: 提出受保护的安全强化学习，通过同时约束动作和下游状态轨迹，在安全范围内改进策略。
result: 在医疗治疗优化任务中，所提方法在保证安全的同时提升了长期治疗策略效果。
conclusion: 该工作为离线强化学习在医疗领域的可靠应用提供了安全框架，可用于医疗代理评估。
---

## Abstract
When applying offline reinforcement learning (RL) in healthcare scenarios, the out-of-distribution (OOD) issues pose significant risks, as inappropriate generalization beyond clinical expertise can result in potentially harmful recommendations. 
While existing methods like conservative Q-learning (CQL) attempt to address the OOD issue, their effectiveness is limited by only constraining action selection by suppressing uncertain actions. This action-only regularization imitates clinician actions that prioritize short-term rewards, but it fails to regulate downstream state trajectories, thereby limiting the discovery of improved long-term treatment strategies. To safely improve policy beyond clinician recommendations while ensuring that state-action trajectories remain in-distribution, we propose \textit{Offline Guarded Safe Reinforcement Learning} ($\mathsf{OGSRL}$), a theoretically grounded model-based offline RL framework. $\mathsf{OGSRL}$ introduces a novel dual constraint mechanism for improving policy with reliability and safety. First, the OOD guardian is established to specify clinically validated regions for safe policy exploration. By constraining optimization within these regions, it enables the reliable exploration of treatment strategies that outperform clinician behavior by leveraging the full patient state history, without drifting into unsupported state-action trajectories. Second, we introduce a safety cost constraint that encodes medical knowledge about physiological safety boundaries, providing domain-specific safeguards even in areas where training data might contain potentially unsafe interventions. Notably, we provide theoretical guarantees on safety and near-optimality: policies that satisfy these constraints remain in safe and reliable regions and achieve performance close to the best possible policy supported by the data. When evaluated on the MIMIC-III sepsis treatment dataset, $\mathsf{OGSRL}$ demonstrated significantly better OOD handling than baselines. $\mathsf{OGSRL}$ achieved a 78\% reduction in mortality estimates and a 51\% increase in reward compared to clinician decisions.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

离线强化学习（Offline RL）在医疗治疗优化中具有巨大潜力，但面临一个关键挑战：**分布外（OOD）问题**。当模型泛化到训练数据之外的状态-动作对时，可能产生有害推荐。现有方法如保守Q学习（CQL）仅抑制OOD动作，却无法控制下游状态轨迹的偏移。这意味着即使每个单独动作都在数据支持内，状态序列仍可能进入模型不可靠的区域，导致长期的次优甚至危险治疗。论文旨在**安全地改进策略**，使其超越临床行为，同时确保整个状态-动作轨迹保持在数据分布内，并满足生理安全约束。

## 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：提出**离线受保护安全强化学习（OGSRL）**，一种基于模型的理论离线强化学习框架，引入**双重约束机制**：

- **OOD 守护者（OOD Guardian）**：学习一个分类器 $\hat{g}$，识别状态-动作对是否属于数据支持区域。通过引入**OOD成本约束** $V^\pi_{\hat{g}, \hat{T}}(\rho_0) \leq \bar{c}_{\hat{g}}$，迫使策略保持在高概率的分布内区域。
- **安全成本约束**：编码医学知识（如 SpO₂ ≥ 92%，尿量 ≥ 0.5 mL/kg/hr）作为显式安全约束 $V^\pi_{c_j, \hat{T}}(\rho_0) \leq \bar{c}_j$。

**技术细节**：

- **OOD 守护者构建**：使用**多项式子水平集（PSoS）**定义支持区域，通过求解优化问题最小化集合体积，同时保持经验覆盖率为 $\alpha_c$。理论证明（定理1）：以高概率 $1-\delta$，学习到的子集包含在真实分布内区域中。
- **模型基离线 RL**：从数据集估计转移模型 $\hat{T}$、奖励 $\hat{r}$、成本 $\hat{c}$，形成**估计的 CMDP**。再嵌入 OOD 守护者得到**受保护 E-CMDP**。
- **策略优化**：使用约束策略优化（如 CPO）求解带 OOD 成本和生理安全约束的优化问题（GSRL）。
- **理论保证**：推论1给出策略在有限步长内保持在分布内的概率保证；定理2、3给出价值函数误差界及安全性和次优性保证。

**算法流程**：
1. 从临床数据收集离线数据集 $D_b$。
2. 学习分类器 $\hat{g}$（如 KDE 近似）。
3. 构建受保护 E-CMDP $\hat{\mathcal{M}}_{\hat{g}}$。
4. 使用 CPO 求解安全有效的治疗策略 $\hat{\pi}$。

## 3. 实验设计

### 数据集/场景
- **主要实验**：MIMIC-III 脓毒症治疗数据集（18,923 次 ICU 住院，13 维状态，2 维连续动作：静脉输液量和最大血管加压药剂量，20 个时间步长）。
- **跨疾病验证**：合成急性低血压数据集（3,910 次 ICU 住院，18 维状态，48 个时间步长）。

### Benchmark
- **标准治疗（SOC）**作为基线。
- **对比方法**：
  - 无守护者的模型无关方法：CQL, CCQL。
  - 无守护者的模型基方法：MB-TRPO, MB-CPO。
  - 增加守护者的变体：GCQL, GCCQL, GMB-TRPO, GMB-CPO。

### 评估指标
- **MCR（模型一致率）**：与临床决策的匹配程度。
- **AIR（适宜强化率）**：在生理恶化时正确升级治疗的比例。
- **ME（死亡率估计）**：模拟轨迹的死亡比例。
- **ACP（动作变化惩罚）**：治疗平滑度。
- **OOD 状态可视化**：t-SNE 投影。
- **生理安全性**：SpO₂ 和尿量低于阈值的状态比例。
- **累积奖励分布**。

**实验设置**：5 折交叉验证（60%训练、20%验证、20%测试），每个算法运行 5 个随机种子，报告均值±标准差。

## 4. 资源与算力

论文在附录 J 中说明：所有实验在配备 **NVIDIA A100 和 V100 GPU** 的 HPC 集群上运行。**未明确给出具体 GPU 数量、训练时长或总算力消耗**。

## 5. 实验数量与充分性

- **脓毒症实验**：对比了 8 种方法（加上 SOC），报告了 4 个核心指标（MCR, AIR, ME, ACP），并附加了生理安全图、奖励分布图、t-SNE 状态分布图。5 个不同种子提供误差估计。
- **低血压实验**：选择了 4 种代表性方法（CQL/GCQL, MB-CPO/GMB-CPO）进行跨疾病验证，报告 MCR、AIR、奖励均值。
- **消融分析**：通过有无守护者对比（无守护者 vs. 有守护者）直接体现 OOD 守护者的贡献。还比较了仅约束 vs. 仅守护者 vs. 双约束的效果。
- **统计严谨性**：使用了 5 次随机种子的均值与标准差，显示了分布图。实验覆盖了模型无关和模型基方法，对比全面。

**结论**：实验设计充分、客观、公平，虽未进行超大规模消融，但已覆盖主要维度。

## 6. 论文的主要结论与发现

- **OOD 守护者有效**：在所有方法中加入守护者后，OOD 状态显著减少（t-SNE 可视化验证），MCR 大幅提升（如 GCQL MCR 从 0.789 升至 0.909，GMB-CPO 从~0 升至 0.549）。
- **GMB-CPO 最佳**：在脓毒症上，GMB-CPO 实现了最低死亡率（0.0138 vs SOC 0.0632，降低 78%），累积奖励提升 51%，同时保持与 SOC 几乎相同的动作平滑度（ACP: 4.34 vs 4.34）。
- **跨疾病泛化性**：在低血压数据集上，GMB-CPO 同样取得最优结果，MCR 从 0.060 升至 0.700，AIR 从 0.411 升至 0.482，奖励均值从 3.90 升至 14.88。
- **理论保证成立**：实验观察到的 OOD 状态避免与理论预测一致，证实了定理 1 和推论 1。

## 7. 优点

- **理论支撑**：提供了安全、次优性和分布保持的概率保证，量化了数据集大小对可靠性的影响，便于临床信任。
- **双约束机制**：OOD 守护者处理模型不可靠区域，生理安全约束处理临床风险，互补生效。
- **充分利用临床知识**：通过 OOD 成本约束隐式对齐临床行为，同时允许长期优化，优于仅模仿的策略。
- **跨疾病验证**：在两种不同病理、时间分辨率、状态维度、奖励结构的疾病上验证，显示框架可泛化。
- **改进显著**：在真实数据上死亡率降低 78%，奖励提升 51%，具有临床意义。

## 8. 不足与局限

- **保守性**：OOD 守护者可能限制发现超出临床记录的创新策略，尤其对于罕见但可能安全有效的治疗。
- **动作空间简化**：仅建模液体和血管加压药，未包含抗生素、通气、营养等多方面干预。
- **固定时间离散化**：4 小时窗口可能遗漏快速生理波动，需要更细粒度或自适应时间。
- **数据集偏差**：仅来自单机构（MIMIC-III）数据，治疗模式可能不适用于其他医院或人群。
- **可解释性不足**：OOD 边界由统计特性（密度估计）决定，缺乏临床可理解的推理，降低信任。
- **实用中的理论假设**：理论证明依赖 Hölder 连续性、KDE 带宽条件等，实际中可能不完美满足。
- **缺乏在线验证**：尽管离线评估，但未进行实际临床模拟或人机交互验证，长期效果待考。

（完）
