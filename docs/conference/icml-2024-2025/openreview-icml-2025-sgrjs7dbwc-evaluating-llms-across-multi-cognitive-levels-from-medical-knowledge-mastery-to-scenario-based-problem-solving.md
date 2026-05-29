---
title: "Evaluating LLMs Across Multi-Cognitive Levels: From Medical Knowledge Mastery to Scenario-Based Problem Solving"
title_zh: 跨多认知水平评估大语言模型：从医学知识掌握到场景化问题解决
authors: "Yuxuan Zhou, Xien Liu, Chenwei Yan, Chen Ning, Xiao Zhang, Boxun Li, Xiangling Fu, Shijin Wang, Guoping Hu, Yu Wang, Ji Wu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=sgrJs7dbWC"
tags: ["query:ehr-agent"]
score: 8.0
evidence: 利用现有医学数据集的多认知层次医学LLM评估框架
tldr: 现有医学基准多聚焦于单一认知层次，难以全面评估LLM的医学能力。受Bloom分类法启发，本文提出了一个多认知层次的医学LLM评估框架，整合现有医学数据集并新增场景化问题解决任务，覆盖知识掌握、综合应用和场景推理三个层次。在六大LLM家族上的系统评估揭示了模型在高阶推理方面的显著不足，为医学智能体评估提供了结构化方法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1667, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1672, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 843, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 755, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 862, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 829, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1742, \"height\": 567, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 575, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1239, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1729, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-sgrjs7dbwc/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1753, \"height\": 528, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 848, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1761, \"height\": 1186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 810, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 835, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 834, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 791, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1663, \"height\": 1499, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-sgrjs7dbwc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1691, \"height\": 1280, \"label\": \"Table\"}]"
motivation: 当前医学LLM评估缺乏对多认知层次的全面考量，无法揭示模型在高阶推理上的局限。
method: 基于Bloom分类法构建多认知层次评估框架，整合现有数据集并设计场景化任务，涵盖知识掌握、综合应用和场景推理三个层次。
result: 在Llama、Qwen、GPT等六大LLM家族上实验，发现模型在初步知识掌握上表现良好，但在复杂场景推理上差距明显。
conclusion: 该框架为医学智能体性能评估提供了系统的方法论，尤其突出了高阶认知能力评估的重要性。
---

## Abstract
Large language models (LLMs) have demonstrated remarkable performance on various medical benchmarks, but their capabilities across different cognitive levels remain underexplored. Inspired by Bloom's Taxonomy, we propose a multi-cognitive-level evaluation framework for assessing LLMs in the medical domain in this study. The framework integrates existing medical datasets and introduces tasks targeting three cognitive levels: preliminary knowledge grasp, comprehensive knowledge application, and scenario-based problem solving. Using this framework, we systematically evaluate state-of-the-art general and medical LLMs from six prominent families: Llama, Qwen, Gemma, Phi, GPT, and DeepSeek. Our findings reveal a significant performance decline as cognitive complexity increases across evaluated models, with model size playing a more critical role in performance at higher cognitive levels. Our study highlights the need to enhance LLMs' medical capabilities at higher cognitive levels and provides insights for developing LLMs suited to real-world medical applications.

---

## 论文详细总结（自动生成）

# 跨多认知水平评估大语言模型：从医学知识掌握到场景化问题解决

## 1. 核心问题与整体含义

- **研究动机**：现有医学基准（如 MedQA、MedMCQA）大多采用选择题形式，主要评估 LLM 在记忆和理解层面的“初步知识掌握”能力；而少数场景化基准（如 MIMIC-IV-Ext）聚焦于高阶临床诊断，但缺乏对中间认知层次的覆盖。因此，**当前评估缺乏对 LLM 医学能力在不同认知层次上的系统性理解**。
- **整体含义**：受 Bloom 分类法启发，该论文提出首个跨多认知层次的医学评估框架，旨在揭示 LLM 从基础医学知识到复杂临床推理的全景能力，为真实医疗场景下的 LLM 应用提供诊断性洞见。

## 2. 方法论：核心思想与关键技术

### 2.1 核心思想
- 参照人类医生的认知发展过程（医学生→临床实习生→住院医师），对应 Bloom 分类法中的“记忆/理解→应用/分析→规划/解决”，定义了三个认知层次：
  - **L1（初步知识掌握）**：记忆和理解基本医学知识。
  - **L2（综合知识应用）**：应用知识分析并解决复杂医学问题。
  - **L3（场景化问题解决）**：在真实临床场景中进行多步规划、诊断和治疗决策。
- 遵循三条原则：**任务相关性**（任务与认知层次匹配）、**知识一致性**（不同层次覆盖相同医学知识）、**度量对齐**（归一化指标以便比较）。

### 2.2 关键技术细节
- **L1 任务**：直接使用 MedQA 和 MedMCQA 的原始多选题（MCQ）。
- **L2 任务**：将原始 MCQ 改造成三类新型问题：
  - **陈述验证**：将问题和某个选项转化为真/假陈述，考察精确知识辨别（排除选项线索）。
  - **多步纠正**：先判断给定选项是否正确，若不正确则从剩余选项选出正确答案（模拟真实诊断中的多步推理）。
  - **答案存在判断**：判断正确答案是否存在于选项集中（模拟开放决策空间）。
- **L3 任务**：基于 MIMIC-IV 电子健康记录，构建**全路径临床诊断**任务。模型需要顺序选择检查类型（体格检查、实验室、微生物、影像），获取结果后做出最终诊断。采用“识别-检索”流程确保疾病覆盖与 L1/L2 一致。
- **度量**：L1/L2 使用标准化准确率（消除随机猜测影响）；L3 使用**全路径诊断准确率** = 诊断准确率 × 检查召回率（宏平均），同时考虑过程正确性和结果正确性。

## 3. 实验设计

### 3.1 数据集/场景
- **L1/L2**：MedQA（USMLE，800 题）和 MedMCQA（印度医学考试，2816 题），使用原始题目及改造后的中层任务。
- **L3**：基于 MIMIC-IV 构建的 2176 份入院记录，涵盖 42 种疾病、8 个人体系统。

### 3.2 评估基准与对比方法
- **通用 LLM**：Llama (1/2/3, 7B~70B)、Qwen (1/2/2.5, 7B~72B)、Gemma (1/2, 2B~27B)、Phi (3/4, 3.8B~14B)、GPT (4o-mini, 4o, o3-mini)、DeepSeek (V3, R1) —— 共 32 个模型。
- **医学 LLM**：ClinicalCamel-70B、Med42 (v1, v2)、Meditron (70B, 3-8B/70B)、MMed-Llama3-8B —— 共 8 个模型。
- 总计 40 个模型，参数范围 2B~671B。

### 3.3 实验设置
- L1/L2：5-shot in-context learning，温度 0，重复 5 次。
- L3：zero-shot，温度 0.8，重复 3 次。
- 结果报告均值和标准误。

## 4. 资源与算力
- 论文**未明确说明**使用的 GPU 型号、数量及训练/推理耗时。仅提及对 GPT-4o 和 DeepSeek-V3 等高成本模型采样约 10% 数据评估。

## 5. 实验数量与充分性

- **实验数量**：核心结果表（Table 2）涵盖了 32 个通用模型和 8 个医学模型，包括所有三个认知层次。附加消融实验包括：
  - 模型尺寸影响分析（7B vs 70B 系列，Fig.5）。
  - 医学微调增益分析（Fig.6）。
  - 推理时缩放效果（Table 3）。
  - L2 细粒度任务性能（Table 4）。
  - L3 全路径诊断细节（Table 5）。
  - 跨疾病性能分布（Fig.7）。
  - 临床医生验证（Table 6）。
- **充分性判断**：实验设计**较为充分**，覆盖了多家族、多规模、多认知层次，并进行了统计重复和临床验证。但缺乏跨语言或跨模态扩展，且推理时缩放仅测试了两个代表性模型。

## 6. 主要结论与发现

1. **认知层次越高，性能下降越显著**：最佳模型 GPT-4o 在 L1 上达 78.3%，在 L2 降为 56.96%，在 L3 仅 19.33%。所有模型呈现一致的下滑趋势。
2. **模型尺寸在高认知层次更重要**：70B 模型在 L2/L3 上的优势远大于在 L1 上，说明大参数在复杂推理中更关键。
3. **医学微调主要提升低/中层次**：医学 LLM（如 Med42-v2-70B）在 L1/L2 上比基座模型高 5~15%，但在 L3 上甚至可能低于基座模型（Fig.6）。
4. **推理时缩放有效提升中高层次**：DeepSeek-R1 在 L2 上比 V3 高 23.1%（绝对值），L1 提高 9.8%，L3 提高 7.1%。o3-mini 也有类似效果。
5. **L3 任务中检查召回率是瓶颈**：即使最终诊断准确率（端点）可达 53.6%，加入检查召回后全路径准确率仅 19.4%，说明模型缺乏系统性的信息获取能力。
6. **疾病诊断性能呈长尾分布**：LLM 在常见疾病上表现较好，但对罕见或复杂疾病诊断能力不足。

## 7. 优点

- **评估框架创新性强**：首次将 Bloom 分类法系统应用于医学 LLM 评估，定义了多层认知任务，填补了中间层次评估的空白。
- **知识覆盖一致性保障**：通过“识别-检索”流程确保 L3 的疾病池与 L1/L2 对齐，减少知识覆盖面偏差。
- **指标设计合理**：标准化准确率消除随机猜测影响，全路径准确率兼顾过程和结果。
- **实验设计系统全面**：涵盖 40 个模型、6 大系列、多尺度，并进行了丰富的消融和细粒度分析。
- **临床医生验证**：通过真实医生评估确认任务难度确实随层次递增，保证了框架的生态效度。

## 8. 不足与局限

- **覆盖广度有限**：仅使用 MedQA/MedMCQA 和 MIMIC-IV（英文），未涉及中文或其他语种、未覆盖内外妇儿等全科医学数据。任务多样性也局限于问答和诊断路径。
- **高层任务定义简化**：L3 仅包含“全路径诊断”一种任务，未能涵盖治疗推荐、预后评估等更广泛的临床决策。
- **随机基线处理偏保守**：L3 开放输出设为 0% 随机准确率，在归一化对比时可能低估高层真实难度差异。
- **推理时缩放模型评估不充分**：仅测试了 DeepSeek-R1 和 o3-mini，且因成本仅在全数据集的小部分子集上评估（约 10%），可能引入采样偏差。
- **缺乏对多模态能力的评估**：真实临床场景常需要影像、文本、实验室结果等多模态输入，该框架当前仅基于文本。
- **未披露计算资源消耗**：无法评估方法的可复现性和成本。

（完）
