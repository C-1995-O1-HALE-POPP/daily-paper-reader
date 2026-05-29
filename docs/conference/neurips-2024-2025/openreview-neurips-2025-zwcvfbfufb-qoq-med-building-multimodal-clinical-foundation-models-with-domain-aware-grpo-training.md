---
title: "QoQ-Med: Building Multimodal Clinical Foundation Models with Domain-Aware GRPO Training"
title_zh: QoQ-Med：使用领域感知GRPO训练构建多模态临床基础模型
authors: "Wei Dai, Peilin Chen, Chanakya Ekbote, Paul Pu Liang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ZwCVFBFUFb"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 使用强化学习训练的多模态临床基础模型，与医疗AI中的强化学习和语言模型相关
tldr: 该论文提出QoQ-Med，首个开放通用临床基础模型，通过领域感知的相对策略优化（GRPO）训练，能够联合推理医学图像、时间序列信号和文本报告。该方法属于强化学习与语言模型在医疗中的应用，但并非直接针对代理评估。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1420, \"height\": 1088, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1432, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1356, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1465, \"height\": 1721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 378, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 378, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 431, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 377, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 379, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 428, \"height\": 429, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 379, \"height\": 287, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zwcvfbfufb/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 376, \"height\": 375, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1433, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 758, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1435, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1518, \"height\": 1496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1436, \"height\": 736, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 1463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1434, \"height\": 1464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1434, \"height\": 1464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1432, \"height\": 1465, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1433, \"height\": 1464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1432, \"height\": 1465, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zwcvfbfufb/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1433, \"height\": 1465, \"label\": \"Table\"}]"
motivation: 现有多模态语言模型在临床领域泛化能力不足，需要能够处理异构数据的通用模型。
method: 提出领域感知相对策略优化（DRPO），根据领域稀有度和模态难度分级缩放奖励，缓解数据分布不平衡问题。
result: 在9个临床专业的多模态任务上，QoQ-Med显著优于现有模型。
conclusion: QoQ-Med为临床多模态推理设立了新基准，但其主要贡献是模型训练而非代理评估框架。
---

## Abstract
Clinical decision‑making routinely demands reasoning over heterogeneous data, yet existing multimodal language models (MLLMs) remain largely vision‑centric and fail to generalize across clinical specialties. To bridge this gap, we introduce QoQ-Med-7B/32B, the first open generalist clinical foundation model that jointly reasons across medical images, time‑series signals, and text reports. QoQ-Med is trained with Domain‑aware Relative Policy Optimization (DRPO), a novel reinforcement‑learning objective that hierarchically scales normalized rewards according to domain rarity and modality difficulty, mitigating performance imbalance caused by skewed clinical data distributions. Trained on 2.61 million instruction tuning pairs spanning 9 clinical domains, we show that DRPO training boosts diagnostic performance by 43% in macro‑F1 on average across all visual domains as compared to other critic-free training methods like GRPO. Furthermore, with QoQ-Med trained on intensive segmentation data, it is able to highlight salient regions related to the diagnosis, with an IoU 10x higher than open models while reaching the performance of OpenAI o4-mini. To foster reproducibility and downstream research, we release (i) the full model weights, (ii) the modular training pipeline, and (iii) all intermediate reasoning traces.

---

## 论文详细总结（自动生成）

# 论文总结：QoQ-Med：使用领域感知GRPO训练构建多模态临床基础模型

## 1. 核心问题与整体含义（研究动机和背景）
*   **问题**：临床诊断需要推理多模态异构数据（如1D心电图、2D X光/MRI、3D CT、文本报告），但现有多模态语言模型（MLLMs）主要是视觉中心化的，无法在多个临床专科间泛化，且缺乏可解释性（“黑箱”问题）。
*   **意义**：本文首次提出一个开放通用的临床基础模型 **QoQ-Med**（7B/32B），能够联合推理医学图像、时间序列信号（ECG）和文本报告，并通过新的强化学习目标 **DRPO**（Domain-aware Relative Policy Optimization）缓解数据分布不平衡问题，同时生成推理链和边界框以提高可解释性。

## 2. 方法论
### 核心思想：DRPO——领域感知的层次化优势缩放
*   **背景**：GRPO（Group Relative Policy Optimization）在每组内对奖励进行归一化，但无法处理跨领域的不平衡（大量数据域主导训练）。
*   **关键步骤**：
    *   **阶段1：域内聚类**。在每个训练迭代中，对每个领域内的奖励向量（每个问题对应多个rollout的奖励）使用K-means聚类（通过肘部法自动确定簇数），将问题按难度分组。
    *   **阶段2：层次缩放**。计算域级温度因子 T(g,t) 和簇级温度因子 T(c,g,t)，分别基于领域/簇的大小和平均难度（奖励均值）。将GRPO归一化后的优势除以这两个温度因子，使得稀有/困难的数据获得更大的权重。
    *   **KL感知正则化**：对高优势且高KL散度的响应进行线性阻尼，防止异常值主导更新。
    *   **公式**：最终优势 ˆA_DRPO = m(i,t)·s(q,i,t) / (T(g,t)·T(c,g,t))，再缩放回单位标准差。

### 模型架构
*   **骨干**：Qwen2.5-VL（7B/32B），包含图像编码器、线性投影层、LLM。
*   **时序编码**：新增预训练的ECG-JEPA编码器，输出经线性投影后与图像patch、文本token按原始顺序交错输入LLM。
*   **训练流程**：
    *   **阶段1**：模态对齐（使用DRPO训练）。
    *   **阶段2**：全多模态微调（使用DRPO）。

### 奖励设计
*   **准确率奖励**：F1 score（按标签为无序集合计算）。
*   **语义对齐奖励**：模型生成边界框与真实分割掩膜的IoU最大值。
*   **辅助奖励**：格式奖励（要求每个预测标签都有对应边界框）、视觉一致性奖励（多视图时）。

## 3. 实验设计
### 数据集
*   **主实验**：CLIMB数据集（2.61M条指令对，33个公开数据集，9个临床领域：Chest X-ray, Mammography, Dermoscopy, CT, Fundus, Ultrasound, MRI, Pathology, ECG）。
*   **多模态融合**：MIMIC-IV（胸部X光+12导联ECG+电子病历），任务为住院时长预测（4类）和48小时院内死亡率预测（二分类）。
*   **对比方法**：SFT、PPO、ReMax、REINFORCE++、RLOO、GRPO。
*   **模型对比**：开源（LLaVa-Med、Med-R1）、闭源（GPT-4o、o4-mini）。
*   **评价指标**：Balanced Accuracy、Macro-F1。

### 消融实验
*   聚类数量（1,3,10,20）。
*   奖励成分权重（Acc:IoU = 0.6:0.2 vs 0.2:0.6）。
*   是否包含域级缩放（DomainOnly vs Full DRPO）。
*   是否包含KL正则化。

## 4. 资源与算力
*   **硬件**：8×NVIDIA A100（80GB SXM）或8×H200。
*   **训练时长**：
    *   7B模型：约2天（8×A100）。
    *   32B模型：超过2周（8×H200）。
*   **框架**：FSDP + VeRL（vLLM加速推理）。
*   **能源消耗**：7B约182.4 kWh；32B约571.2 kWh（基于TDP估算）。

## 5. 实验数量与充分性
*   **主实验数量**：8个视觉模态 + 1个ECG诊断实验 + 2个多模态融合任务，共约11个对比方向。
*   **统计可靠性**：每个实验运行4次不同种子，报告均值±标准差（附录表7）。
*   **消融实验**：包含聚类数、奖励权重、域缩放、KL正则化等，覆盖面广。
*   **公平性**：所有RL方法使用相同超参数、相同base模型、相同数据顺序。
*   **充分性**：实验比较全面，但ECG领域的对比仅出现在RQ2的融合任务中，单独ECG诊断的对比不充分（仅列出DRPO与GRPO的对比图，缺少与其他RL方法的数值表格）。此外，推理痕迹质量仅由少量临床专家主观标注（未提供标注者间信度）。

## 6. 主要结论与发现
*   **DRPO显著优于其他RL方法**：在所有视觉域上平均F1比GRPO提升43%，在6/8个视觉域取得最佳F1。
*   **多模态融合有效**：在MIMIC-IV上，完整输入（ECG+视觉+文本）优于任何单模态消融，表明模型能有效聚合多源信息。
*   **可解释性提升**：边界框IoU超过所有开源模型，达到o4-mini水平；推理痕迹经临床专家审查，大部分内容与诊断高度相关。
*   **模型规模扩展性**：QoQ-Med-32B在多数域上超越7B，且显著优于所有开源临床MLLMs。

## 7. 优点
*   **创新性**：DRPO是首个针对多领域异构临床数据的分层强化学习训练方法，有效解决了数据不平衡问题。
*   **全面性**：模型涵盖1D时间序列、2D/3D图像和文本，是首个同时处理ECG与多种影像的通用临床MLLM。
*   **可解释性**：通过协变推理链和边界框输出，便于临床医生审查，增强了信任。
*   **开放性与可复现性**：公开了模型权重、训练管道和2.61M条推理痕迹，促进了后续研究。
*   **实验严谨性**：多次运行、报告标准差、全面的对比与消融，且开源代码。

## 8. 不足与局限
*   **推理质量局限**：推理过程是无监督学习的，缺乏高质量的监督信号，导致有时推理正确但最终预测错误（如Figure 4c）。样本效率有限。
*   **ECG性能相对较弱**：虽然模型整合了ECG，但在MIMIC-IV中，ECG对最终任务的贡献小于视觉和文本，表明ECG编码器或训练数据可能还需优化。
*   **训练轮次不足**：仅训练1个epoch，可能未充分收敛（尤其对于32B大模型）。
*   **领域覆盖不均衡**：虽然涵盖9个领域，但部分领域（如超声、ECG）的数据量远小于Chest X-ray，可能导致间接受益有限（DRPO已尽力缓解但未完全消除）。
*   **临床实用性验证不足**：推理痕迹评估仅由少数专家手动标注，缺乏大规模用户研究或临床环境下的鲁棒性测试。
*   **计算资源需求高**：32B模型训练需8×H200两周以上，对部分研究团队可能构成门槛。

（完）
