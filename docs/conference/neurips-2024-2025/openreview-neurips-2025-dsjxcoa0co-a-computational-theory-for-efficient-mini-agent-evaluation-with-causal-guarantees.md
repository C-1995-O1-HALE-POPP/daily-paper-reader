---
title: A Computational Theory for Efficient Mini Agent Evaluation with Causal Guarantees
title_zh: 高效迷你智能体评估的计算理论及因果保证
authors: Hedong Yan
date: 2025-04-17
pdf: "https://openreview.net/pdf?id=dsjxCoa0CO"
tags: ["query:ehr-agent"]
score: 8.0
evidence: 提出了用于高效智能体评估的计算理论和元学习器，并在个体医学场景上进行了测试。
tldr: "该论文针对智能体实验评估成本高昂的问题，提出了一种高效迷你智能体评估的计算理论，并证明了泛化误差和因果效应误差的上界。该方法通过元学习器处理异质智能体空间，在12个场景（包括个体医学）上将评估误差降低了24.1%至99.0%，为医疗智能体的基准测试提供了一种可迁移的理论框架和实用工具。"
source: NeurIPS-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1432, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 594, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1403, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1404, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1392, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1384, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 993, \"height\": 781, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1426, \"height\": 210, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dsjxcoa0co/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1451, \"height\": 1523, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1437, \"height\": 590, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 652, \"height\": 185, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1446, \"height\": 510, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1333, \"height\": 1152, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1220, \"height\": 552, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1322, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1319, \"height\": 2079, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1445, \"height\": 2342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 605, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1433, \"height\": 68, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1274, \"height\": 635, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1103, \"height\": 636, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1102, \"height\": 635, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1275, \"height\": 634, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1330, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1435, \"height\": 508, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dsjxcoa0co/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1437, \"height\": 490, \"label\": \"Table\"}]"
motivation: 为降低智能体实验评估的高昂成本，亟需一种能加速评估流程并保证因果一致性的计算理论。
method: 提出评估模型的计算理论，证明误差上界，并设计元学习器以处理异质智能体空间，从而学习条件评估模型。
result: "在12个场景（包括个体医学）上，条件评估模型相比现有方法降低了24.1%至99.0%的评估误差。"
conclusion: 该工作为智能体评估提供了理论基础和高效方法，尤其适用于医疗等领域的智能体性能基准测试。
---

## Abstract
In order to reduce the cost of experimental evaluation for agents, we introduce a computational theory of evaluation for mini agents: build evaluation model to accelerate the evaluation procedures. We prove upper bounds of generalized error and generalized causal effect error of given evaluation models for infinite agents. We also prove efficiency, and consistency to estimated causal effect from deployed agents to evaluation metric by prediction. To learn evaluation models, we propose a meta-learner to handle heterogeneous agents space problem. Comparing with existed evaluation approaches, our (conditional) evaluation model reduced 24.1\% to 99.0\% evaluation errors across 12 scenes, including individual medicine, scientific simulation, social experiment, business activity, and quantum trade. The evaluation time is reduced 3 to 7 order of magnitude comparing with experiments or simulations.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：评估智能体（尤其是无限或高维空间中的 mini agent）的传统方法（如随机对照试验 RCT）成本极高、耗时长，且难以快速迭代。现有集中式 A/B 测试平台虽降低成本，但仍无法处理无限评估主体且存在伦理问题。
- **整体含义**：论文提出一种**计算评估理论**，通过构建评估模型（Evaluation Model）来加速评估流程，并在理论上保证泛化误差和因果效应误差的可控上界。目标是实现高效、低成本且具有因果保证的智能体评估，适用于个体医学、科学模拟、社会实验、商业活动、量化交易等多种场景。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：用计算模型学习评估条件（C）、评估主体（S，即 agent）与评估指标（M）之间的映射关系，从而替代真实实验或仿真。
- **关键假设**：
  - **IIDE**：评估误差独立同分布。
  - **IRIS**：评估主体独立、随机、同分布采样（保证因果可识别）。
  - **CU**：评估模型对给定条件无偏估计。
- **理论结果**：
  - **定理1**：泛化误差上界：`P(E_gen < E_emp + sqrt(12/n ln(1/σ))) ≥ 1-σ`，n为测量次数。
  - **定理2**：因果优势：若模型误差最小化，则因果效应误差也最小化（效率和一致性）。
  - **定理3**（有正性假设）和**定理4**（无正性假设）：给出因果效应误差的界，后者不要求每个主体都有观测样本，适用于无限主体空间。
- **学习算法流程**（见图2）：
  1. 数据分类：按主体类型划分。
  2. 向量化：为每种类型设计不同的张量化函数。
  3. 代理度量计算：利用已有计算方法（如 bootstrap、交叉验证）生成 proxy metric。
  4. 训练基学习器：可选 Linear、RF、MLP、CatBoost、XGBoost、LightGBM、SVR/SVM 等。
  5. 假设检验：评估 IIDE 和无偏性是否成立。
  6. 模型选择：选择上界满足需求且误差最小的模型。

### 3. 实验设计：数据集/场景、基准、对比方法

- **数据集与场景**（共12个场景，11个用于评估模型 + 1个用于条件评估模型）：
  - 个体医学：Alert（AKI）、Withdrawal、TERECO（COVID康复）
  - 科学模拟：NuScale（核反应堆）、kin8nm（机械臂）、Higgs（粒子检测）、Climate（气候模拟）、Grid（电网）
  - 社会实验：Calculus（教学）
  - 商业活动：Insurance（保险推荐）、Ad（广告）
  - 量化交易：A-Share 市场（条件评估）
- **基准方法**：
  - 评估模型：Holdout-100%、Holdout-50%、Holdout-10%、5折CV、10折CV、Bootstrap。
  - 条件评估：基线为 Last10Days（过去10天收益回测）。
- **对比方法**：论文的 HetEM（异质评估模型）使用不同基学习器（Linear、MLP、SVR、RF、LGBM、XGBoost、CatBoost）。
- **评估指标**：ROC-AUC、ACC、RMSE、R²、RoI（量化交易）。

### 4. 资源与算力

- **计算资源**：论文仅提到实验在一台 **13-inch MacBook Pro 2020（Apple M1芯片，16GB内存）** 上运行，总耗时约 **2天**。未使用GPU或其他集群。所有实验均在该单机上进行。
- **未明确说明**：未提供GPU型号、数量、分布式训练等信息，因此无法得知更详细的算力规模。

### 5. 实验数量与充分性

- **实验数量**：
  - 评估模型：在11个场景上重复 **30次**，每次随机采样2000个agent，20%用于测试。
  - 条件评估模型（量化交易）：重复 **5次**，每次200个agent，200只股票。
  - 假设检验：对每个基学习器计算 IIDE 检验和无偏性检验的 p-value比率（表6,7）。
  - 消融与分析：Shapley值解释各模块贡献（图4）。
- **充分性与公平性**：
  - 覆盖了多个领域，场景多样性较高。
  - 与多种经典验证方法对比，且报告了置信区间和标准化误差。
  - 但所有基学习器均使用默认超参数（除量化交易中CatBoost做了网格搜索），未进行广泛的超参数调优，可能未达到最优性能。
  - 未与基于深度学习的因果推断方法（如CEVAE、TARNet等）对比，理由是其不适于小样本且忽略了计算资源限制。

### 6. 论文的主要结论与发现

- **评估模型**：在11个场景上，最佳 HetEM（通常为线性模型）在 RMSE、R²、ROC-AUC、ACC 上分别降低 **94.7%-99.0%**、**81.7%-95.5%**、**24.1%-77.0%**、**39.2%-89.5%** 的评估误差（对比 Holdout-100）。
- **条件评估模型**：在量化交易场景中，HetEM-CatBoost 降低 **89.4%** 的 RoI 预测误差（对比基线 Last10Days）。
- **效率**：计算评估时间比实验/仿真评估加速 **3到7个数量级**（每个主体从数小时/天降低到不足1秒）。
- **理论贡献**：首次给出 mini agent 评估的因果效应误差上界，且无需正性假设，适用于无限主体空间。

### 7. 优点

- **理论支撑扎实**：提供了严格的泛化误差和因果效应误差上界，并考虑了实用假设（IIDE、IRIS、无偏）。
- **处理异质空间**：通过元学习器（分类-向量化-代理度量-独立建模）有效应对 agent 空间异质性。
- **假设可检验**：提出统计方法（D'Agostino-Pearson、KS检验、t检验）评估假设是否成立，可拒绝不可靠的模型。
- **实验覆盖多样**：12个真实/仿真场景涵盖医疗、物理、商业、金融等领域，具有代表性。
- **效率极高**：计算成本远低于传统实验，易于部署和迭代。

### 8. 不足与局限

- **假设依赖性**：IIDE、IRIS、无偏性三个假设在真实世界中可能不成立，尤其是开放环境（如社交实验、市场交易）。实验表明部分基学习器（如SVR、MLP）未能通过检验。
- **高维场景未验证**：论文仅测试了有限维度的 agent（线性+简单MLP），未在类似大语言模型（LLM）的超高维 agent 空间验证。
- **小样本性能受限**：当样本量极小时，误差上界较宽松，可能无法满足实际需求。
- **跨场景泛化**：未探索同一个评估模型能否跨不同场景迁移。
- **度量局限**：主要使用预测性能（如ROC-AUC）作为近似，未收集真实部署后的临床结局（如死亡率）等更高价值的指标。
- **对比不够充分**：未与现有因果推断包（EconML、DoWhy等）或基于深度学习的异质处理效应估计方法直接对比。
- **硬件资源限制**：实验仅在一台MacBook上运行，可能限制了基学习器的复杂性（如深度模型未使用），但这也体现了方法的轻量化优势。

（完）
