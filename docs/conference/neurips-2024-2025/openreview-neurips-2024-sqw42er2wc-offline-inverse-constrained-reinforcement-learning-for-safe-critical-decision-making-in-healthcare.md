---
title: Offline Inverse Constrained Reinforcement Learning for Safe-Critical Decision Making in Healthcare
title_zh: 面向医疗安全关键决策的离线逆约束强化学习
authors: "Nan Fang, Guiliang Liu, Wei Gong"
date: 2024-05-13
pdf: "https://openreview.net/pdf?id=SqW42eR2wC"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 离线逆约束强化学习用于医疗安全决策，与医疗代理中的RL相关
tldr: 医疗领域的强化学习常因忽视约束导致不安全决策。本文提出离线逆约束强化学习（ICRL），从专家演示中推断安全约束，避免了在线交互需求。在医疗决策任务中，该方法有效降低了危险动作频率，为医疗代理的安全RL提供了新思路。
source: NeurIPS-2024-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 560, \"height\": 335, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1426, \"height\": 708, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 801, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 784, \"height\": 263, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 393, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1415, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 709, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1435, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 848, \"height\": 645, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 575, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1151, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 586, \"height\": 465, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1153, \"height\": 1995, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-sqw42er2wc/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1181, \"height\": 280, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 587, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 797, \"height\": 666, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 916, \"height\": 253, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1240, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1412, \"height\": 571, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 405, \"height\": 702, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-sqw42er2wc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1132, \"height\": 1088, \"label\": \"Table\"}]"
motivation: 医疗RL代理因忽略常规约束导致不安全决策，且指定成本函数困难。
method: 提出离线逆约束强化学习，从历史治疗数据中推断约束，避免在线交互。
result: 在医疗决策任务中，该方法降低了危险动作，提高了安全性。
conclusion: 离线逆约束强化学习可有效提升医疗代理决策的安全性。
---

## Abstract
Reinforcement Learning (RL) applied in healthcare can lead to unsafe medical decisions and treatment, such as excessive dosages or abrupt changes, often due to agents overlooking common-sense constraints. Consequently, Constrained Reinforcement Learning (CRL) is a natural choice for safe decisions. However, specifying the exact cost function is inherently difficult in healthcare. Recent Inverse Constrained Reinforcement Learning (ICRL) is a promising approach that infers constraints from expert demonstrations. ICRL algorithms model Markovian decisions in an interactive environment. These settings do not align with the practical requirement of a decision-making system in healthcare, where decisions rely on historical treatment recorded in an offline dataset. To tackle these issues, we propose the Constraint Transformer (CT). Specifically, 1) utilize causal attention mechanism to incorporate historical decisions and observations into the constraint modeling and employ a non-Markovian layer for weighted constraints to capture critical states, 2) generative world model to perform exploratory data augmentation, thereby enabling offline RL methods to generate unsafe decision sequences. In multiple medical scenarios, empirical results demonstrate that CT can capture unsafe states and achieve strategies that approximate lower mortality rates, reducing the occurrence probability of unsafe behaviors.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 核心问题与整体含义

- **研究动机**：在医疗领域应用强化学习（RL）时，智能体常常忽略常识性约束（如药物剂量过高、剂量突然变化），导致不安全决策（例如脓毒症治疗中血管加压素剂量>1μg/(kg·min)时死亡率高达90%）。传统的约束强化学习（CRL）需要显式指定成本函数，但在医疗场景中难以设计通用、个性化的约束。逆约束强化学习（ICRL）可通过专家演示推断约束，但现有ICRL方法依赖马尔可夫假设和在线交互环境，不符合医疗决策依赖历史信息和仅能使用离线数据的实际需求。
- **整体含义**：本文提出离线约束变换器（Offline Constraint Transformer, CT），一种新颖的离线逆约束强化学习框架，旨在从离线医疗数据中推断安全约束，从而学习接近最优的低死亡率策略，并消除危险行为（“过高剂量”和“突然变化”）。

## 2. 方法论

- **核心思想**：
  - 利用因果注意力机制（类似Decision Transformer）将历史状态和动作融入约束建模，打破马尔可夫假设。
  - 引入非马尔可夫层（额外注意力层）为每个时间步生成重要性权重，以加权方式定义成本函数，从而捕获关键状态。
  - 为了解决离线训练中缺乏违反约束数据的问题，构建一个基于Transformer的生成式世界模型（model-based offline RL），通过自回归方式生成高奖励导向的违反轨迹（violating data）。
  - 使用最大熵框架，通过对比专家数据和违反数据更新约束变换器（CT），使得约束值在专家轨迹上最小化、在违反轨迹上最大化。

- **关键技术细节**：
  - **Constraint Transformer (CT)**：输入为长度为T的轨迹段（状态和动作嵌入），通过因果Transformer输出嵌入序列，再经非马尔可夫注意力层计算加权成本 \(C(\tau)=\sum_{t=1}^T w_t \cdot c_t\)，其中权重由query-key点积softmax得到。
  - **生成式世界模型**：联合学习策略模型（随机高斯策略，带熵正则化）和世界模型（预测下一状态和奖励）。输入为返回奖励、状态、动作序列，使用因果Transformer自回归建模。训练损失包括负对数似然、熵正则项、状态/奖励预测MSE损失。
  - **生成违反数据**：设置高初始目标奖励 \(\hat{R}_1\)，从专家数据中采样初始状态，通过训练好的世界模型自回归生成轨迹（长度K=10），得到违反数据集 \(D_v\)。
  - **安全策略学习**：将CT推断的成本函数 \(C_\phi(\tau)\) 与任意离线CRL方法（如VOCE、COpiDICE、BCQ-Lag、CDT）结合，通过拉格朗日法最大化奖励同时约束成本。

- **公式**（文字说明）：
  - 约束学习梯度：\(\nabla_\phi \mathcal{L}(\phi) = \mathbb{E}_{\hat\tau \sim D_v}[\nabla_\phi \log C_\phi(\hat\tau)] - \mathbb{E}_{\tau \sim D_e}[\nabla_\phi \log C_\phi(\tau)]\)
  - 策略学习目标：\(\arg\max_\pi \mathbb{E}[\sum \gamma^t r_t],\quad \text{s.t. } \mathbb{E}[\sum \gamma^t c_t] \le \kappa\)

## 3. 实验设计

- **数据集**：Medical Information Mart for Intensive Care III (MIMIC-III) 数据库。提取入住ICU 72小时内数据，每4小时一个时间步。
  - **脓毒症（Sepsis）任务**：状态48维（人口学、实验室、生命体征等），动作2维（静脉输液量、血管加压素最大剂量），奖励基于SOFA分数变化。
  - **机械通气（Mechanical Ventilation）任务**：状态36维，动作离散（7x7=49种PEEP和FiO2组合），奖励基于Apache II评分和终点死亡与否。

- **基准方法**：
  - 脓毒症：DDPG（Huang et al., 2022）作为基线；无成本（cost=0）和自定义成本（基于阈值1和2000）作为对比。
  - 机械通气：DDQN、CQL（Kondrup et al., 2023）作为基线。
  - 在线CRL方法：VOCE、COpiDICE、BCQ-Lag、CDT（均为离线CRL方法），分别与CT结合；同时对比了“无成本”、“自定义成本”、“无注意力层CT”、“仅生成模型”等消融设置。

- **评价指标**：
  - **ω**：从数据集中随机抽取2N个患者（N幸存者+N非幸存者），计算策略推荐与医生策略的差异（DIFF），排序后取前N名，其中幸存者比例即为ω，值越高表示策略越接近最优（低死亡率）。
  - **DIFF与死亡率关系图**：绘制DIFF（策略动作-医生动作）与患者死亡率的关系曲线，DIFF=0时死亡率越低越好。

## 4. 资源与算力

- 论文在附录B.5中说明：使用3块NVIDIA GeForce RTX 3090 GPU，每块24GB内存。训练一个CRL+CT模型通常需要5-6小时。使用Adam优化器，学习率衰减。具体超参数见表6、7。

## 5. 实验数量与充分性

- **实验数量**：
  - 在脓毒症任务上，对4种CRL方法（VOCE、CopiDICE、BCQ-Lag、CDT）分别测试了无成本、自定义成本、CT三种设置，每个条件使用10组随机种子，计算均值和方差（表2）。
  - 机械通气任务上，对比了DDQN、CQL、CDT和CDT+CT四种方法，绘制DIFF-死亡率曲线（图8）。
  - 消融实验：移除CT、移除注意力层、仅用生成模型替代CT（表2下半部分）。
  - 对约束有效性：分析成本与死亡率关系（图5），成本与生理指标关系（图6、13），以及不安全行为比例（表3）。
  - 生成模型评价：预测准确性（图10）、预测误差与轨迹长度关系（图11）、违反数据分布（图12）。

- **充分性讨论**：
  - **优点**：覆盖了两个不同的医疗任务（脓毒症和机械通气），利用了多种离线CRL算法作为基座，消融实验完整，统计使用了随机种子，误差棒已报告。
  - **不足**：
    - 仅依赖MIMIC-III单一数据库，泛化性未验证。
    - 未与现有的离线ICRL方法（几乎没有）或其他生成模型（VAE、GAN、扩散模型）进行直接比较，仅在消融中对比了纯生成模型。
    - 评价指标ω虽然新颖，但依赖医生策略作为“近似最优”的参照，可能引入偏差。

## 6. 主要结论与发现

- **约束有效性**：CT学习的成本函数与患者死亡率呈正相关；能区分安全/不安全状态（如SOFA、乳酸、平均动脉压、心率等指标偏离正常范围时成本升高）；注意力层是关键，移除后成本与死亡率相关性消失。
- **策略性能提升**：CT与多种CRL方法结合后，ω值均高于无成本或自定义成本设置，其中CDT+CT综合最优，ω比DDPG基线提高8.85%。在机械通气任务中，CDT+CT的DIFF-死亡率曲线更合理（DIFF=0时死亡率最低）。
- **安全行为改善**：CT能够将“过高剂量”（vaso>0.75）和“突然变化”（Δvaso>0.75）的发生率降至0%（最大值0.00），而自定义成本虽也消除，但导致用药过少（几乎不用药），可能影响治疗效果。
- **消融结论**：CT和注意力层均不可或缺；基于序列建模的生成模型本身也优于DDPG。

## 7. 优点

- **方法创新**：
  - 首次解决医疗离线逆约束学习问题，提出非马尔可夫约束变换器，利用因果注意力捕获历史依赖。
  - 生成式世界模型在离线环境下自动产生违反数据，无需在线交互。
  - 与任何离线CRL方法兼容，具有通用性。
- **实验设计**：
  - 医疗任务定义贴近真实临床（脓毒症和机械通气），数据来源于权威数据库MIMIC-III。
  - 评价指标ω提供了可量化的策略最优性评估，相比传统FQE更具解释性。
  - 消融实验全面，揭示了各组件贡献。

## 8. 不足与局限

- **理论分析缺失**：论文未对推断的约束集进行形式化定义或理论收敛性分析。
- **计算资源需求高**：Transformer架构导致训练时间长（5-6小时/模型），在资源受限场景可能受限。
- **评价指标局限性**：ω依赖医生策略作为“最优”参照，但医生策略并非绝对最优（表1显示医生也有2.27%的不安全行为）；另外缺乏更多医学专用定量指标（如实际死亡率、不良事件率等）。
- **专家演示假设不现实**：假设专家数据在约束满足和奖励最大化上均最优，但实际医疗数据可能存在 noise 和次优决策，该方法未处理此问题。
- **实验覆盖有限**：仅两个医疗场景，未验证在其他疾病（如麻醉、镇静）或更复杂环境中的表现；与现有其他离线ICRL方法（如基于最大因果熵的Baert et al., 2023）缺乏直接对比。
- **生成模型可能引入偏差**：生成违反数据的方式（高初始奖励）可能导致与真实危险分布不一致，影响CT泛化。

（完）
