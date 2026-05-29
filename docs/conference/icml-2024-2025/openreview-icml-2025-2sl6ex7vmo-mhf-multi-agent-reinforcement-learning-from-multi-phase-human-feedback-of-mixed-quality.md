---
title: "M³HF: Multi-agent Reinforcement Learning from Multi-phase Human Feedback of Mixed Quality"
title_zh: M³HF：来自混合质量的多阶段人类反馈的多智能体强化学习
authors: "Ziyan Wang, Zhicheng Zhang, Fei Fang, Yali Du"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=2Sl6Ex7Vmo"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 多智能体强化学习结合人类反馈用于智能体训练和评估
tldr: 该论文提出M3HF框架，解决多智能体强化学习中奖励函数设计困难的问题。通过引入多阶段、混合质量的人类反馈，利用大语言模型解析反馈并迭代优化智能体策略。实验证明该方法能有效提升多智能体系统的协同性能。该框架为智能体训练与评估提供了一种利用人类反馈的可扩展范式，可迁移至医疗智能体场景。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1699, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1710, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1727, \"height\": 889, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1057, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 667, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1697, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2sl6ex7vmo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1620, \"height\": 904, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-2sl6ex7vmo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 888, \"height\": 185, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2sl6ex7vmo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 885, \"height\": 157, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2sl6ex7vmo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 855, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2sl6ex7vmo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 884, \"height\": 492, \"label\": \"Table\"}]"
motivation: 多智能体强化学习中奖励函数设计困难，现有方法难以处理混合质量的人类反馈。
method: 提出M³HF框架，在训练过程中暂停智能体学习，收集多阶段、不同质量的人类反馈，并用大语言模型解析。
result: 在多个多智能体协同环境中验证了该方法能有效提升策略性能。
conclusion: M³HF为利用混合质量人类反馈训练多智能体系统提供了有效框架。
---

## Abstract
Designing effective reward functions in multi-agent reinforcement learning (MARL) is a significant challenge, often leading to suboptimal or misaligned behaviors in complex, coordinated environments. We introduce Multi-agent Reinforcement Learning from Multi-phase Human Feedback of Mixed Quality ($\text{M}^3\text{HF}$), a novel framework that integrates multi-phase human feedback of mixed quality into the MARL training process. By involving humans with diverse expertise levels to provide iterative guidance, $\text{M}^3\text{HF}$ leverages both expert and non-expert feedback to continuously refine agents' policies. During training, we strategically pause agent learning for human evaluation, parse feedback using large language models to assign it appropriately and update reward functions through predefined templates and adaptive weights by using weight decay and performance-based adjustments. Our approach enables the integration of nuanced human insights across various levels of quality, enhancing the interpretability and robustness of multi-agent cooperation. Empirical results in challenging environments demonstrate that $\text{M}^3\text{HF}$ significantly outperforms state-of-the-art methods, effectively addressing the complexities of reward design in MARL and enabling broader human participation in the training process.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：多智能体强化学习（MARL）中奖励函数设计极为困难，尤其是在稀疏奖励或复杂协同任务中，传统的手工设计往往导致策略次优或行为偏离目标。
- **背景**：单一靠环境奖励不足，人类反馈（RLHF）在单智能体领域已取得成效，但现有方法（如PbMARL）通常局限于离线、单阶段、标量的偏好比较，无法处理在线、多阶段、不同质量（混合质量）的人类自然语言反馈。
- **研究目标**：提出一个能够融合多阶段、混合质量（专家与非专家）人类反馈的MARL框架，使智能体能够利用非完美人类指导持续改进策略。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将MARL训练划分为多个“代”（generation），每代训练后暂停，生成回放视频供人类评估；人类提供自然语言反馈，由大语言模型（LLM）解析并分配给特定智能体或全体；再根据预定义模板生成新的奖励函数，并通过自适应权重组合到原有的奖励池中。
- **关键步骤**：
  1. **多阶段人类反馈马尔可夫博弈（MHF-MG）**：扩展标准马尔可夫博弈，加入人类话语集 \(U\) 和人类策略 \(\pi_h\)，每个代内智能体与环境交互，人类基于回放视频提供反馈 \(u_k\)。
  2. **反馈解析**：使用LLM（GPT-4o）将人类反馈 \(u_k\) 解析为针对各智能体或全体指令。
  3. **奖励模板与生成**：预置距离型、动作型、状态型等模板，LLM根据解析结果选择并参数化模板，生成新奖励函数 \(R_{ik}\)，加入每个智能体的奖励池 \(P_i\)。
  4. **权重调整**：对新奖励函数赋初权，之后应用指数衰减（权重衰减）以及基于原始奖励性能变化的调整（提升则加权，下降则减权），最后归一化得到最终奖励 \(\hat{R}_{ik+1}\)。
- **公式/算法**：
  - 回放轨迹收集：\(\tau_k^{(x)} = \{(s_t, a_t, r_t)\}_{t=0}^{H-1}\)
  - 回报估计：\(\hat{J}_{X,H}(\pi_k) = \frac{1}{X}\sum_x G_H^{(x)}\)
  - 奖励更新：\(\hat{R}_{ik+1}(s,a) = \sum_j w_{i,j} R_{ij}(s,a)\)
  - 权重衰减：\(w_{i,m} = w_{i,m} \cdot \alpha^{M-m}\)，然后归一化。
  - 性能调整：若新奖励下的原始回报高于前一代，则 \(w_{i,M} += \beta\)，否则 \(\max(0, w_{i,M} - \beta)\)。
- **理论分析**：证明了性能估计的一致性（Proposition 4.1）；提出了对低质量反馈的鲁棒性保证（Proposition 4.2），指出算法只会因单次低质量反馈造成有界退化，而能累积高质量反馈的收益。

## 3. 实验设计

- **环境**：基于Overcooked的多智能体协同烹饪任务，三种厨房布局（A、B、C，难度递增）和两种沙拉配方（番茄-生菜、番茄-生菜-洋葱）。智能体采用宏动作（macro-action），部分可观测（5×5视野）。原始奖励非常稀疏：只有交付正确沙拉得+200，交付错误或丢菜得-50，其他惩罚步骤时间。
- **基准方法**：
  - MAPPO（共享策略+集中值函数）
  - IPPO（独立策略）
  - Mac-Based Baseline（来自Xiao et al.的工作，取两个最佳方法Mac-IAICC和Mac-CAC的平均值）
  - 消融变体：Raw Feedback（无解析）、LLM Parsing Only（无权重调整）、单阶段反馈
  - 内在奖励方法：IRAT的三个变体（rw1、rw2、rw3）
  - VLM反馈替代：使用Gemini-1.5-Pro-002
- **实验规模**：共6个任务组合（3布局×2配方），每个任务训练1000次迭代（约25k episodes），每代200次迭代。每个设置用3个随机种子运行，绘制均值与标准差。

## 4. 资源与算力

- 论文明确指出实验在异构计算集群上进行，使用**3块NVIDIA A30 GPU**，以及多种CPU（如Intel Xeon E5-2650等），系统内存500GB，CPU核心180个。
- 未明确说明单次训练时长或总GPU小时数，但提到环境模拟加速（1分钟游戏=3秒实际时间），整个实验覆盖多个配置与3个随机种子。

## 5. 实验数量与充分性

- **充分性**：共完成6个主要任务（布局×配方）的10万级episode训练；还进行了3项消融实验（反馈解析与权重、单阶段vs多阶段、内在奖励对比）以及VLM反馈评估和Google Football的扩展验证。实验覆盖了不同难度、不同反馈质量、不同架构变体。
- **客观公平**：所有基线均经过超参数调优（学习率、批大小等），采用与原文一致的最好超参数。结果报告均值和标准差，置信区间合理。
- **不足**：仅在一个游戏环境（Overcooked）上进行了主要实验，Google Football作为补充但简单。缺少在其他连续控制或真实环境上的验证。

## 6. 论文的主要结论与发现

- **总体性能**：M3HF在所有6个任务上均显著优于MAPPO、IPPO和Mac-Based Baseline，尤其在复杂布局下优势更明显。
- **多阶段有效性**：多阶段反馈优于单阶段反馈，平均回报从43.1提升至102.7。
- **鲁棒性**：面对低质量（虚假肯定）反馈，M3HF仅略低于基线IPPO，性能未严重退化，验证了理论鲁棒性。
- **VLM替代**：当前VLM（Gemini-1.5-Pro）提供的反馈不够具体，无法显著提升性能，但未来改进潜力大。
- **内在奖励对比**：IRAT虽有一定提升，但远低于M3HF，因为M3HF能从人类反馈中针对性地纠正协同失败。

## 7. 优点

- **创新性**：首次将多阶段、混合质量人类自然语言反馈引入MARL在线训练，并设计了完整的反馈解析-奖励生成-权重调整管道。
- **理论支撑**：给出了性能估计一致性和低质量反馈鲁棒性的定理证明。
- **实用性**：仅需少量人类交互（最多5次），降低了专家依赖，使非专家也能参与训练。
- **泛化性**：方法可迁移至其他MARL环境（如Google Football），且框架可灵活更换LLM和反馈源。

## 8. 不足与局限

- **环境单一**：主要实验仅基于Overcooked（离散网格世界），未在连续控制、物理仿真等更复杂环境上验证。
- **反馈质量依赖**：尽管对低质量反馈有鲁棒性，但理想人类反馈仍是性能关键，VLM替代效果尚不理想。
- **资源开销**：每代需要生成大量回放视频供人类评估，人力成本虽低但计算开销（LLM调用、视频存储）未详细量化。
- **超参数敏感**：权重衰减系数α、调整因子β等需要手动设定，可能影响鲁棒性。
- **可扩展性分析有限**：仅在10智能体足球上做了初步验证，更大规模（如上百智能体）尚未测试。

（完）
