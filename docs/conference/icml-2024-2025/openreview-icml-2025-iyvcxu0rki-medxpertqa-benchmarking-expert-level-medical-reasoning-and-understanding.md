---
title: "MedXpertQA: Benchmarking Expert-Level Medical Reasoning and Understanding"
title_zh: MedXpertQA：基准测试专家级医学推理与理解
authors: "Yuxin Zuo, Shang Qu, Yifei Li, Zhang-Ren Chen, Xuekai Zhu, Ermo Hua, Kaiyan Zhang, Ning Ding, Bowen Zhou"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=IyVcxU0RKI"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 专家级医学推理基准，可用于评估医疗智能体
tldr: 该论文介绍MedXpertQA，一个覆盖17个专科、包含4460道多模态问题的医学推理基准。它包含文本和多模态子集，引入专家级考试题目和丰富临床信息（如病历和检查结果），超越现有基准难度。该基准可用于全面评估医疗AI智能体的推理能力，为医疗智能体性能评估提供标准化测试集。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 853, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1775, \"height\": 1021, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 912, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1658, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 853, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1774, \"height\": 630, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 842, \"height\": 568, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 515, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1004, \"height\": 347, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-iyvcxu0rki/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 837, \"height\": 580, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1769, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 855, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1672, \"height\": 613, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 829, \"height\": 574, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 811, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1218, \"height\": 560, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-iyvcxu0rki/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1109, \"height\": 285, \"label\": \"Table\"}]"
motivation: 现有医学基准难度不足，缺乏对AI智能体专家级推理能力的评估。
method: 构建包含多模态、多专科的专家级问答数据集，并采用严格筛选和增强流程。
result: MedXpertQA显著提升了评估难度，揭示了当前模型在专家级医学推理上的局限。
conclusion: MedXpertQA可作为评估医学AI智能体高级推理能力的标准基准。
---

## Abstract
We introduce MedXpertQA, a highly challenging and comprehensive benchmark to evaluate expert-level medical knowledge and advanced reasoning. MedXpertQA includes 4,460 questions spanning 17 specialties and 11 body systems. It includes two subsets, Text for text evaluation and MM for multimodal evaluation. Notably, MM introduces expert-level exam questions with diverse images and rich clinical information, including patient records and examination results, setting it apart from traditional medical multimodal benchmarks with simple QA pairs generated from image captions. MedXpertQA applies rigorous filtering and augmentation to address the insufficient difficulty of existing benchmarks like MedQA, and incorporates specialty board questions to improve clinical relevance and comprehensiveness. We perform data synthesis to mitigate data leakage risk and conduct multiple rounds of expert reviews to ensure accuracy and reliability. We evaluate 18 leading models on MedXpertQA. Moreover, medicine is deeply connected to real-world decision-making, providing a rich and representative setting for assessing reasoning abilities beyond mathematics and code. To this end, we develop a reasoning-oriented subset to facilitate the assessment of o1-like models.

---

## 论文详细总结（自动生成）

# MedXpertQA 论文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有医学 AI 基准（如 MedQA、PubMedQA、VQA-Rad 等）存在三大不足：（1）**难度不足**，当前先进模型（如 o1-preview）在 MedQA 上已达 96%，无法区分顶尖模型水平；（2）**专科覆盖不够**，缺乏对 17 个医学专科的系统评估；（3）**临床真实性差**，多模态基准大多基于图像标题自动生成简单问答，缺乏病历、检查结果等真实临床信息，无法评估专家级推理能力。
- **整体含义**：为了推动医学 AI 向可靠、专家级推理能力发展，需要一个更具挑战性、更全面、更贴近真实临床场景的基准。MedXpertQA 应运而生，旨在填补这一空白，并特别为 o1 类推理模型设计评估推理子集。

## 2. 论文提出的方法论

- **核心思想**：构建一个高度挑战性、覆盖多专科、多模态、包含丰富临床信息的医学多项选择题基准。通过严格的数据筛选、合成和专家审核确保质量和难度。
- **关键技术细节**：
  - **数据收集**：从 USMLE、COMLEX 等执照考试、17 个美国专科委员会考试、以及 NEJM Image Challenge 等图像丰富来源收集 37,543 道题。
  - **难度筛选**：
    - **AI 专家筛选**：使用 8 个模型（基础+高级）投票，移除所有基础模型在 4 次采样中都答对的简单题，保留所有 AI 专家都答错的题。
    - **人类专家筛选**：利用人类答题的 Brier 分数（考虑所有选项选择率）来量化难度，并基于专家标注的难度等级设置自适应阈值进行分层筛选。
    - **相似性筛选**：使用 MedCPT-Query-Encoder 计算语义相似度，结合编辑距离，通过四分位距（IQR）找出高度相似的问题对，移除较简单者。
    - **数据增强**：使用 gpt-4o 和 claude-3.5-sonnet 对问题和选项进行改写与扩充，降低数据泄露风险。文本集选项增至 10 个，多模态集保持 5 个。
    - **专家审核**：拥有医师执照的医学专家对每个问题审核，修正事实错误、格式问题、不合理选项等。
  - **推理子集构建**：使用 GPT-4o 结合专家编写答案和解释，将问题标注为“推理型”或“知识型”，随后由人类专家抽样验证，错误率约 4.3%。

## 3. 实验设计

- **数据集/场景**：MedXpertQA 包含 **Text 子集**（2,455 道文本题）和 **MM 子集**（2,005 道多模态题，共 2,839 张图像），覆盖 17 个专科、11 个人体系统、3 类任务（诊断、治疗、基础医学）。还特别构建了 **Reasoning 子集**。
- **基准对比**：与 VQA-Rad、Path-VQA、Slake、PMC-VQA、OmniMedVQA、GMAI-MMBench、MMMU (H&M)、PubMedQA、MedQA、MedMCQA、MMLU (Medical) 等现有基准比较。MedXpertQA 在问题长度、图像多样性、图像/问题比例、临床场景真实性上均更优。
- **对比方法**：评估了 18 个领先模型（包含专有和开源），分为 LMM 和 LLM 两类，特别包括了 o1、QVQ-72B-Preview、DeepSeek-R1、QwQ-32B-Preview 等推理时扩展模型。使用零样本 CoT 提示，贪婪解码（或模型推荐设置）。

## 4. 资源与算力

- 论文未明确说明训练模型所需的 GPU 型号、数量、训练时长。文中提到使用 API 评估 GPT-4o、Claude-3.5-Sonnet、DeepSeek-R1 等，未报告自定义训练。问题增强阶段使用了两个专有模型（gpt-4o-2024-11-20 和 claude-3-5-sonnet-20241022），属于 API 调用。因此，**算力消耗未明确量化**。

## 5. 实验数量与充分性

- **实验数量**：主要实验包括在 Full MedXpertQA Text 和 MM 上的 18 个模型评测（表 4、表 5）。此外还进行了数据泄露分析（表 6）、推理扩展影响分析（图 4）、系统级医学洞察（图 5）、错误类型分析（图 6）等。
- **充分性**：实验设计较充分：
  - 对比了当前最强模型，涵盖专有/开源、推理/非推理。
  - 分析了不同专科/系统/任务上的表现。
  - 验证了数据增强降低泄露风险的有效性。
  - 人类专家性能作为基线（基于历年考试数据，未重新测试），但样本量充足（大部分问题有 500+ 答题者）。
  - 推理子集的标注经专家抽查，一致性较好。
- **公平性**：保持零样本 CoT 统一设置，但对 o1/DeepSeek-R1 等按建议调整了系统提示，可能引入轻微不一致。价格限制导致对 o1/o3-mini 只采样了 10% 子集，可能影响统计稳定性。

## 6. 主要结论与发现

- MedXpertQA 对当前所有模型均构成显著挑战，**最高准确率仅 44.67%（o1 在文本子集采样）**，远低于人类预估（42.60%），验证了其高难度。
- **推理型问题比知识型问题更难**，所有非推理扩展模型在推理子集上表现更差，但 o1 类模型（如 DeepSeek-R1）的差距明显缩小，表明推理时扩展有助于提升医学推理能力。
- **多模态任务中视觉感知能力至关重要**，例如 Gemini-2.0-Flash 在多模态上表现突出。
- **数据泄露风险较低**，且经过数据增强后进一步降低（困惑度提升、ROUGE-L 和编辑距离下降）。
- **错误分析**表明：主要错误类型是推理过程错误和感知错误，反映模型在医学逻辑链和图像解读上的不足。
- 不同模型的专科弱点不同，例如 GPT-4o 在心血管系统相关问题上表现较差。

## 7. 优点

- **难度极高且区分度好**：能有效评估当前最先进模型的极限，避免天花板效应。
- **真实临床模拟**：首次将专家级考试题与病历、检查结果、多种图像类型（放射、病理、生命体征、图表等）结合，远超以往自动生成的问答对。
- **专科覆盖广泛**：涵盖 17 个专科和 11 个系统，支持细粒度诊断。
- **严格质量控制**：多轮 AI + 人类筛选、相似性去重、数据合成防泄漏、专家审核，确保高准确性和可靠性。
- **推理子集有针对性**：专为 o1 类模型设计，能清晰测试推理能力改进。
- **开源与可复现**：提供代码和在线排行榜，促进社区使用。

## 8. 不足与局限

- **评估方式限制**：仅采用多项选择题形式，与实际开放式诊疗流程有差距，不能全面反映临床决策能力。
- **数据来源偏向美国标准**：主要使用 USMLE、COMLEX、美国专科委员会题目，可能不适用于其他医疗体系。
- **部分模型只采样评估**：o1、o3-mini 因成本仅采样 10%，子集代表性可能不够。
- **人类基线是历史数据**：并非当前在 MedXpertQA 增强版上的实测成绩，增强可能略微影响难度，但论文认为影响较小。
- **标注依赖 LLM**：任务、系统、推理/知识标注使用 GPT-4o 自动完成，虽有专家抽查，但可能仍存在偏差。
- **缺乏模型不确定性输出**：只取贪婪解码或模型默认输出，未评估置信度或多次采样一致性。
- **未考虑输入缺失鲁棒性**：如论文讨论部分提及，未测试临床信息缺失对模型的影响，这在真实场景中很重要。

（完）
