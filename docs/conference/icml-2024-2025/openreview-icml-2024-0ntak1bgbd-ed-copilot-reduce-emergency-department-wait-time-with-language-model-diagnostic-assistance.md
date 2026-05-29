---
title: "ED-Copilot: Reduce Emergency Department Wait Time with Language Model Diagnostic Assistance"
title_zh: ED-Copilot：利用语言模型诊断辅助减少急诊科等待时间
authors: "Liwen Sun, Abhineet Agarwal, Aaron Kornblith, Bin Yu, Chenyan Xiong"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=0ntak1BGBd"
tags: ["query:ehr-agent"]
score: 10.0
evidence: 使用EHR基准评估医疗代理性能
tldr: 急诊科拥挤导致患者死亡率上升，现有方法缺乏高效的诊断辅助。本文基于MIMIC-EHR数据构建MIMIC-ED-Assist基准，并开发ED-Copilot代理，通过顺序推荐实验室检查来缩短等待时间并准确预测死亡等关键结局。实验表明ED-Copilot在效率与准确性上显著优于基线，为急诊AI辅助诊断提供了实用基准与方法。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-0ntak1bgbd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 892, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-0ntak1bgbd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1775, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-0ntak1bgbd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 892, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-0ntak1bgbd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 866, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-0ntak1bgbd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 809, \"height\": 386, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 813, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1765, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 418, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1765, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 859, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1776, \"height\": 1106, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1770, \"height\": 1629, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1464, \"height\": 374, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1767, \"height\": 745, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-0ntak1bgbd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1765, \"height\": 685, \"label\": \"Table\"}]"
motivation: 急诊科拥挤影响患者预后，需要高效准确的诊断辅助系统。
method: 基于MIMIC-EHR构建基准并开发ED-Copilot代理，顺序推荐实验室检查。
result: ED-Copilot在减少等待时间和预测关键结局上优于基线方法。
conclusion: EHR驱动的AI代理能有效提升急诊诊断效率与安全性。
---

## Abstract
In the emergency department (ED), patients undergo triage and multiple laboratory tests before diagnosis. This time-consuming process causes ED crowding which impacts patient mortality, medical errors, staff burnout, etc. This work proposes (time) *cost-effective diagnostic assistance* that leverages artificial intelligence systems to help ED clinicians make efficient and accurate diagnoses. In collaboration with ED clinicians, we use public patient data to curate MIMIC-ED-Assist, a benchmark for AI systems to suggest laboratory tests that minimize wait time while accurately predicting critical outcomes such as death. With MIMIC-ED-Assist, we develop ED-Copilot which sequentially suggests patient-specific laboratory tests and makes diagnostic predictions. ED-Copilot employs a pre-trained bio-medical language model to encode patient information and uses reinforcement learning to minimize ED wait time and maximize prediction accuracy. On MIMIC-ED-Assist, ED-Copilot improves prediction accuracy over baselines while halving average wait time from four hours to two hours. ED-Copilot can also effectively personalize treatment recommendations based on patient severity, further highlighting its potential as a diagnostic assistant. Since MIMIC-ED-Assist is a retrospective benchmark, ED-Copilot is restricted to recommend only observed tests. We show ED-Copilot achieves competitive performance without this restriction as the maximum allowed time increases. Our code is available at https://github.com/cxcscmu/ED-Copilot.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 一、核心问题与整体含义

- **研究动机**：急诊科（ED）拥挤是严重医疗挑战，影响患者死亡率、医疗错误和员工倦怠。实验室测试流程是导致ED等待时间延长的关键因素，且有40-60%的实验室测试被认为不必要。
- **整体目标**：提出一种时间-成本效益诊断辅助系统，通过AI建议最佳实验室检查序列，在准确预测关键结局（死亡、ICU转移）和长ED停留的同时，最小化等待时间。
- **意义**：首次将语言模型与强化学习结合用于ED诊断辅助，有望提升ED吞吐量、改善患者预后，并减少医疗资源浪费。

## 二、方法论：核心思想与技术细节

- **核心思想**：将患者三分类信息（人口统计、生命体征、主诉等）和既往实验室结果线性化为文本序列，利用预训练生物医学语言模型（BioGPT）编码，再通过强化学习学习最优测试选择策略。
- **关键技术细节**：
  1. **线性化**：将实验室组结果转换为“test name : test value | test name : test value ...”格式的文本，三分类信息也以类似方式嵌入。
  2. **语言模型骨干**：使用BioGPT（345M参数）对线性化序列编码，得到每个[EOS] token的隐表示，然后通过两个MLP分别预测**下一个实验室组**和**结局标签**。
  3. **两阶段训练**：
     - **阶段1：有监督微调**。同时优化两个任务：自回归预测下一个实验室组（交叉熵损失）、预测结局（二分类交叉熵损失）。
     - **阶段2：强化学习（RL）**。将问题建模为马尔可夫决策过程（MDP）：状态为当前已观测的所有信息；动作空间包括12个实验室组和2个终止动作（预测阳性或阴性结局）；策略网络基于隐状态输出动作概率。使用近端策略优化（PPO）训练，目标为最大化F1分数并最小化总时间成本。奖励函数设计为：`TN(πη) + α·TP(πη) + β·Cost(πη)`，其中α控制敏感性与特异性权衡，β控制准确性与时间成本权衡。
  4. **时间成本计算**：采用各组测试完成时间的累加和作为总时间成本（因为实际ED中测试可以并行也可能串行，论文选择累加作为初步近似）。
- **算法流程**：给定初始三分类信息 → ED-Copilot推荐下一个实验室组 → 获取该组结果（由历史数据提供，或模拟中通过检索或补全得到）→ 更新状态 → 再次推荐，直至选择终止动作并给出风险预测。

## 三、实验设计

- **数据集**：基于MIMIC-IV和MIMIC-IV-ED构建的**MIMIC-ED-Assist**基准数据集。包含32,356次ED就诊，25,714名患者。过滤条件：仅限住院成人患者，排除重复测试（约1.5%），且具备齐全三分类信息。
- **实验室组**：由临床合作者将68种常见测试归为12个临床常见组合（如CBC、CHEM、COAG等），并估计每组平均完成时间（如CBC约30分钟，CHEM约60分钟等）。
- **预测目标**：
  - **关键结局**：住院期间死亡或12小时内转入ICU（正例率9.67%）。
  - **长ED停留**：ED停留超过24小时（正例率6.90%）。
- **对比方法**：
  - 非成本效益基线：随机森林、XGBoost、LightGBM、3层DNN（使用多种缺失值填补方法，取最佳结果报告）。
  - 成本效益基线：SM-DDPO（Yu et al., 2023），使用RL选择固定全局最优测试集，不提供个性化建议。
- **评估指标**：F1、AUC、敏感性、特异性、平均时间成本。
- **消融实验**：
  - 线性化方式（原始测试名 vs. 标准特征名）
  - 特征重要性（去掉三分类、去掉CBC、去掉CHEM）
  - 骨干模型规模（BioGPT vs. GPT2-Medium vs. Pythia 70M；Llama 7B LORA无RL）
  - 超参数α、β的影响
  - 个性化分析（按测试流行度分组评估）
  - 子群分析（性别、年龄）
  - 不受限实验（允许推荐未观测测试）

## 四、资源与算力

- 论文明确说明：所有实验和超参数调优在一张**NVIDIA RTX A6000 GPU**上完成。
- 未提供具体训练时长，但可推测监督微调约15 epoch，RL约10 epoch（每次迭代20000步），整体训练成本在可接受范围内。
- 此外提及使用Hugging Face库实现，RL部分基于stable-baselines3。

## 五、实验数量与充分性

- **数量**：论文围绕两个预测目标（关键结局、长ED停留）展开了：
  - 主实验结果（Table 2）：对比5种基线 + ED-Copilot，3个随机种子取均值和标准差。
  - 不同时间约束下的性能曲线（Figure 2）：展示F1和AUC随最大允许时间变化。
  - 消融实验（Table 3）：覆盖线性化、特征、骨干模型（5种变体）。
  - 超参数分析（Figure 3）：展示α和β对敏感性与特异性、F1与成本的影响。
  - 个性化分析（Table 4, Figure 4）：按测试流行度分为3个队列，比较各模型表现。
  - 子群分析（Table 6）：按性别和三个年龄段分别报告。
  - 不受限建议实验（Figure 5）：比较限制与不限制实验室组选择时的性能。
- **充分性**：实验设计较为全面，覆盖了性能对比、消融、鲁棒性（子群）、个性化能力、约束影响。数据集规模尚可（3.2万就诊）。但缺少外部验证（仅用Beth Israel Deaconess Medical Center数据），且对比基线未包括最新的LLM方案（如直接使用GPT-4等）。实验公平性：树模型使用最佳缺失值处理方式，ED-Copilot与SM-DDPO均使用相同RL框架，训练随机种子报告标准差，整体公平合理。

## 六、主要结论与发现

1. **性能优势**：ED-Copilot在关键结局预测上F1达0.413，比最佳基线LightGBM（0.394）高1.9%；AUC 0.820 vs 0.813；平均时间成本从265分钟降至125分钟（减半）。
2. **长ED停留预测**：F1 0.252 vs 0.217（LightGBM），时间成本降至154分钟。
3. **个性化有效**：对于中高疾病严重度的患者（接受中间6组或最后4组罕见测试），ED-Copilot的F1提升更明显，尤其对高阳性率群体敏感性更高。
4. **模型规模影响**：BioGPT（345M）优于更小的Pythia（70M）和同规模的GPT2，表明生物医学预训练和规模是关键。
5. **特征重要性**：三分类信息对性能贡献最大，CBC比CHEM更重要。
6. **不受限实验**：当允许推荐未观测测试且时间预算充足时，ED-Copilot表现接近受限版本，说明具备合理临床建议能力。

## 七、优点

- **问题定义清晰**：将ED等待时间减少建模为序列测试推荐+风险预测，很有实际价值。
- **方法创新**：首次将语言模型（BioGPT）与强化学习结合用于诊断辅助，利用LLM的表示能力进行个性化推荐。
- **基准构建规范**：与ED临床医生合作定义实验室组、选择预测目标，数据集处理透明。
- **实验全面**：涵盖多种消融、不同患者严重度分析、子群分析、离线与模拟在线对比，论证充分。
- **可复现**：提供代码和数据管道，算法细节详细。

## 八、不足与局限

- **数据偏差**：仅使用住院ED患者数据（因非住院患者缺乏实验室结果），无法代表所有ED人群，且来自单一医学中心，泛化性受限。
- **离线性质**：所有数据回顾性，模型推荐必须适配历史数据（仅推荐已观测测试），缺少在线随机对照试验验证。
- **时间成本近似**：使用累加和简化现实并行与串行混合流程，可能高估或低估真实等待时间。
- **未考虑混杂因素**：如保险政策、医生偏好等外部因素影响测试选择，模型未建模。
- **对比基线不足**：未与最新大型语言模型（如GPT-4、Med-PaLM）直接比较（仅尝试了Llama 7B无RL）。
- **缺乏安全性和错误分析**：未讨论模型错误类型（假阳性/假阴性）对临床决策的潜在影响，也未进行可解释性分析。
- **实验规模有限**：仅一张GPU训练，但模型为345M参数，有可能在更大规模上探索（如更大的LLaMA）但受限于资源。

（完）
