---
title: "MDAgents: An Adaptive Collaboration of LLMs for Medical Decision-Making"
title_zh: MDAgents：用于医疗决策的LLM自适应协作
authors: "Yubin Kim, Chanwoo Park, Hyewon Jeong, Yik Siu Chan, Xuhai Xu, Daniel McDuff, Hyeonhoon Lee, Marzyeh Ghassemi, Cynthia Breazeal, Hae Won Park"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=EKdk4vxKO4"
tags: ["query:ehr-agent"]
score: 9.0
evidence: MDAgents是一种用于医疗决策的多代理LLM框架，并在真实医疗任务上进行了基准测试
tldr: 该论文提出MDAgents，一种自适应多代理LLM框架，根据医疗任务复杂度自动选择单代理或多代理协作结构，模拟现实医疗决策过程。在多项真实医疗知识和临床基准上评估，展示了优于单一LLM和固定协作方法的性能。该工作直接服务于医疗代理的基准测试与性能评估。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 731, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 401, \"height\": 186, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 742, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 647, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 661, \"height\": 457, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 864, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1440, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1453, \"height\": 1406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1434, \"height\": 1360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1392, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 220, \"height\": 170, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1322, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 342, \"height\": 240, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1448, \"height\": 1480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ekdk4vxko4/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1422, \"height\": 926, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1485, \"height\": 475, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1470, \"height\": 1155, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 937, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 588, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 720, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1517, \"height\": 153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 842, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 734, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1468, \"height\": 1276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1470, \"height\": 1209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1460, \"height\": 514, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1472, \"height\": 1067, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ekdk4vxko4/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 901, \"height\": 222, \"label\": \"Table\"}]"
motivation: 现有LLM在复杂医疗任务中的最佳协作方式未知，需要自适应分配。
method: 基于任务复杂度自动分配单代理或组协作结构，模拟真实医疗决策流程。
result: 在多个真实医疗基准上，MDAgents优于单一LLM和固定协作基线。
conclusion: MDAgents为医疗决策中的LLM协作提供了有效框架，并可作为医疗代理评估的基准方法。
---

## Abstract
Foundation models are becoming valuable tools in medicine. Yet despite their promise, the best way to leverage Large Language Models (LLMs) in complex medical tasks remains an open question. We introduce a novel multi-agent framework, named **M**edical **D**ecision-making **Agents** (**MDAgents**) that helps to address this gap by automatically assigning a collaboration structure to a team of LLMs. The assigned solo or group collaboration structure is tailored to the medical task at hand, a simple emulation inspired by the way real-world medical decision-making processes are adapted to tasks of different complexities. We evaluate our framework and baseline methods using state-of-the-art LLMs across a suite of real-world medical knowledge and clinical diagnosis benchmarks, including a comparison of
LLMs’ medical complexity classification against human physicians. MDAgents achieved the **best performance in seven out of ten** benchmarks on tasks requiring an understanding of medical knowledge and multi-modal reasoning, showing a significant **improvement of up to 4.2\%** ($p$ < 0.05) compared to previous methods' best performances. Ablation studies reveal that MDAgents effectively determines medical complexity to optimize for efficiency and accuracy across diverse medical tasks. Notably, the combination of moderator review and external medical knowledge in group collaboration resulted in an average accuracy **improvement of 11.8\%**. Our code can be found at https://github.com/mitmedialab/MDAgents.

---

## 论文详细总结（自动生成）

# MDAgents: 用于医疗决策的LLM自适应协作——论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：大语言模型（LLM）在医学领域展现出巨大潜力，但如何将其有效应用于复杂的医疗决策任务仍是一个开放问题。现实中的医疗决策过程具有层级性和协作性：简单病例由初级保健医生（PCP）独立处理，复杂病例则需要多学科团队（MDT）或综合护理团队（ICT）协作。现有LLM方法要么是单一模型独立推理，要么是固定数量的多智能体协作（如投票、辩论），缺乏根据任务复杂度动态调整协作结构的能力。
- **核心问题**：如何让LLM系统像真实临床实践一样，自适应地选择单人决策或团队协作模式，从而在保持效率的同时提升诊断准确性？
- **整体含义**：论文提出的MDAgents框架首次将“自适应复杂度分配”引入多LLM协作医疗决策，模拟了现实医疗中的分诊与转诊机制，为LLM在临床中的应用提供了更接近实际、更灵活高效的范式。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想
MDAgents是一个自适应多智能体框架，根据医疗查询的复杂度自动分配协作结构。复杂度分为三级：
- **低复杂度**：由单一初级保健医生（PCP）代理独立回答。
- **中复杂度**：由多学科团队（MDT）进行多轮协作讨论，达成共识。
- **高复杂度**：由综合护理团队（ICT）分阶段生成报告，最终由审查团队综合决策。

### 2.2 关键技术细节（算法流程，共4步）
1. **医疗复杂度检查（Complexity Check）**：一个扮演全科医生（GP）的“主持人”（Moderator）代理评估查询，将其分为低、中、高三级。该分类基于症状严重程度、多系统受累、是否需要多学科协作等临床标准。
2. **专家招募（Recruitment）**：一个“招募者”（Recruiter）代理根据复杂度等级，选择：
   - 低：单个PCP代理
   - 中：MDT（多个专科代理，如病理科、放射科、外科等）
   - 高：ICT（多个子团队，如初始评估团队、诊断团队、最终审查团队）
3. **分析与综合（Analysis & Synthesis）**：
   - 低：PCP使用思维链（CoT）或少样本提示直接推理。
   - 中：MDT进行最多R轮迭代讨论，每轮中代理交换意见，若未达成共识，“主持人”提供反馈，然后进入下一轮。直到收敛或达到最大轮数。
   - 高：ICT中每个子团队独立生成报告（包含分析和建议），然后由最终决策团队综合所有报告。
4. **最终决策（Decision Making）**：决策者代理整合所有输入（低：直接输出；中：对话历史；高：多份报告），通过集成方法（如温度集成、多数投票）得出最终答案。

### 2.3 关键算法伪代码（文字说明）
算法1（附录C.2）描述了完整流程：
- 输入：问题Q
- 1. 复杂度检查得到复杂度等级。
- 2. 若为低：招募PCP代理，直接回答。
- 3. 若为中：招募MDT团队，进行迭代讨论（最多R轮），每轮收集意见，主持人检查共识，若不达成则提供反馈并更新代理，记录交互日志。最终主持人基于交互日志给出答案。
- 4. 若为高：招募ICT（多个子团队），每个团队生成报告，汇总后由最终决策者整合生成答案。

## 3. 实验设计

### 3.1 数据集与Benchmark
共使用**10个医疗基准**，覆盖三大类：
- **医学知识问答（文本）**：MedQA、PubMedQA、JAMA、MedBullets
- **临床诊断推理（文本）**：DDXPlus、SymCat
- **医学视觉理解（图像/视频+文本）**：Path-VQA、PMC-VQA、MIMIC-CXR、MedVidQA

每个数据集随机采样50个样本（部分实验扩展至100或全量），并测试3个随机种子以报告标准差。

### 3.2 对比方法
- **Solo（单代理）**：Zero-shot、Few-shot、Chain-of-Thought（CoT）、CoT+Self-Consistency（SC）、Ensemble Refinement（ER）、Medprompt
- **Group（多代理，固定结构）**：Majority Voting、Weighted Voting、Borda Count、MedAgents、Meta-Prompting、ReConcile、AutoGen、DyLAN
- **Adaptive（本文方法）**：MDAgents（自适应选择单人/团队）

### 3.3 模型
主要使用GPT-4(V)（文本+图像），部分实验用Gemini-Pro(Vision)（视频+文本）和GPT-3.5、GPT-4o mini等。所有实验基于API调用，未进行微调。

## 4. 资源与算力

- **文中未明确说明**具体的GPU型号、数量或训练时长。因为所有实验均通过API调用商业LLM（如OpenAI的GPT-4、Gemini），不涉及本地训练或微调。
- 仅提及估算的API调用成本（附录D.2）：完整测试集运行MDAgents的总成本约**17.27万美元**（基于GPT-4(V)），远高于基线方法的5.89万美元，但性能提升显著。算力开销主要由API提供商承担。
- 推理时间：低复杂度平均14.7秒，中复杂度95.5秒，高复杂度226秒。

## 5. 实验数量与充分性

- **实验数量充足**：在10个基准上，每个基准对比了多种Solo和Group方法，共报告数十组结果。主要实验（表2）涵盖了所有方法在10个数据集上的结果。
- 额外进行了**消融实验**（表3）：
  - 复杂度选择的影响（固定低/中/高 vs. 自适应）
  - 主持人回顾与RAG知识增强的效果
  - 不同代理数量的影响（图6）
  - 温度鲁棒性（低T=0.3 vs. 高T=1.2）
  - 共识熵收敛趋势（图7）
  - 人类医师与LLM复杂度分类对比（附录F）
- **充分性评估**：实验设计全面，覆盖不同模态和难度，报告了均值与标准差，进行了显著性检验（p<0.05）。但部分实验仅用50个样本，可能不足以代表完整分布（后续补充了100样本和全量MedQA实验）。总体而言，实验设计客观公平。

## 6. 主要结论与发现

1. **自适应方法显著优于固定结构**：MDAgents在10个基准中的7个上取得最佳准确率，提升最高达4.2%（p<0.05）。
2. **复杂度分类有效**：LLM作为复杂度分类器能以81%的概率选择最优复杂度等级（图3）。自适应方法优于任何固定复杂度分配（图5）。
3. **主持人回顾+RAG组合效果最优**：结合外部医学知识（MedRAG）和主持人回顾，准确率提升11.8%（表3）。
4. **代理数量并非越多越好**：MDAgents在N=3时达到最优，更少的代理意味着更少的API调用，实现效率与准确度的最佳平衡（图6a,b）。
5. **温度鲁棒性强**：MDAgents在高温度下反而受益，利用多样性提升决策，而Solo和Group方法在高温度下性能下降（图6c）。
6. **共识收敛趋势**：多模态任务中代理意见熵随时间下降，表明协作有助于达成一致（图7）。

## 7. 优点

- **创新性**：首次提出自适应多智能体协作框架，模拟真实医疗分诊流程，填补了固定结构方法的空白。
- **全面性**：覆盖文本、图像、视频多种模态，在10个基准上严格评估，消融实验丰富。
- **实用导向**：注重效率（API调用数）与准确率的权衡，且对温度变化鲁棒，适合实际部署。
- **可解释性**：通过案例研究展示了协作过程（图11、12），代理间对话透明。
- **开源**：代码公开，便于复现和扩展。

## 8. 不足与局限

- **数据集采样有限**：主要实验仅用50个样本/数据集，虽然补充了100样本和全量测试，但部分基准（如MedVidQA）样本量仍偏少，可能影响统计稳定性。
- **未涉及真实患者交互**：当前框架仅基于静态选择题回答，未实现与患者的对话交互，缺乏真实临床中的信息收集和随访能力。
- **复杂度分类可能不准确**：附录F显示LLM与人类医师的复杂度分类相关性较低（最高0.11），表明LLM对医疗复杂度的理解尚与人类专家有差距，可能影响自适应决策的质量。
- **仅使用商业模型**：未测试开源或医疗专用模型（如Med-PaLM、Med-Gemini），限制了泛化性和成本分析。
- **潜在风险**：医疗幻觉和错误信息风险未被充分解决，仅提及可结合自纠正机制，但未实现。
- **算力成本高**：多代理协作导致API调用次数和成本显著高于单代理方法，可能限制资源有限场景的应用。

（完）
