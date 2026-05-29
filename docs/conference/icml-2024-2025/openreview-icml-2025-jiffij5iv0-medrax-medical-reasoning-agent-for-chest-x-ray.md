---
title: "MedRAX: Medical Reasoning Agent for Chest X-ray"
title_zh: MedRAX：胸部X光医学推理智能体
authors: "Adibvafa Fallahpour, Jun Ma, Alif Munim, Hongwei Lyu, BO WANG"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=JiFfij5iv0"
tags: ["query:ehr-agent"]
score: 9.0
evidence: 医学推理智能体及其基准，使用临床查询数据
tldr: 该论文提出MedRAX，一个整合先进胸部X光分析工具和多模态大语言模型的通用智能体。为评估其性能，构建了包含2500个复杂医学查询的ChestAgentBench基准。实验表明MedRAX能有效处理多种临床推理任务，且无需额外训练。该工作为基于影像数据的医疗智能体评估提供了直接范例，其框架可推广至基于EHR的智能体。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jiffij5iv0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 809, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jiffij5iv0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 853, \"height\": 1226, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jiffij5iv0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1726, \"height\": 1030, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jiffij5iv0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1781, \"height\": 548, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jiffij5iv0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1615, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jiffij5iv0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1613, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jiffij5iv0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1616, \"height\": 384, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jiffij5iv0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 820, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jiffij5iv0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 537, \"label\": \"Table\"}]"
motivation: 现有胸部X光分析模型相互孤立，缺乏统一整合与评估。
method: 构建集成多工具和大语言模型的智能体，并设计多类别查询基准进行评测。
result: MedRAX在复杂医学查询上表现优异，验证了智能体框架的有效性。
conclusion: MedRAX为医疗智能体设计提供了可扩展框架，其评估方法可直接用于EHR场景。
---

## Abstract
Chest X-rays (CXRs) play an integral role in driving critical decisions in disease management and patient care. While recent innovations have led to specialized models for various CXR interpretation tasks, these solutions often operate in isolation, limiting their practical utility in clinical practice. We present MedRAX, the first versatile AI agent that seamlessly integrates state-of-the-art  CXR analysis tools and multimodal large language models into a unified framework. MedRAX dynamically leverages these models to address complex medical queries without requiring additional training. To rigorously evaluate its capabilities, we introduce ChestAgentBench, a comprehensive benchmark containing 2,500 complex medical queries across 7 diverse categories. Our experiments demonstrate that MedRAX achieves state-of-the-art performance compared to both open-source and proprietary models, representing a significant step toward the practical deployment of automated CXR interpretation systems. Data and code have been publicly available at https://github.com/bowang-lab/MedRAX

---

## 论文详细总结（自动生成）

# MedRAX: Medical Reasoning Agent for Chest X-ray 论文总结

## 1. 核心问题与整体含义
- **研究动机**：胸部 X 光（CXR）是疾病管理中的关键影像检查，但现有 AI 模型（分类、分割、报告生成等）相互孤立，缺乏统一框架，限制了临床实用性和整体性能。
- **整体含义**：首次提出一个能够动态集成多种 CXR 分析工具和多模态大语言模型（如 GPT-4o）的通用 AI 智能体框架 MedRAX，无需额外训练即可处理复杂医学查询，为自动化 CXR 解释系统的实用部署迈出重要一步。

## 2. 方法论
- **核心思想**：采用 **ReAct（Reasoning and Acting）循环**，由 LLM 驱动，将复杂查询分解为观察、思考、行动等迭代步骤，动态选择合适的专业工具并整合结果。
- **关键技术细节**：
  - **推理引擎**：GPT-4o（支持多模态）作为核心，负责解析用户查询、决定是否使用工具及生成最终回答。
  - **工具集合**：集成 7 类下游任务专用模型：
    - 视觉问答（VQA）：CheXagent、LLaVA-Med
    - 分割：MedSAM、PSPNet（基于 ChestX-Det）
    - 接地（Grounding）：Maira-2
    - 报告生成：基于 CheXpert Plus 的 SwinV2+BERT
    - 疾病分类：TorchXRayVision（DenseNet-121）
    - CXR 生成：RoentGen
    - 工具类：图像处理、可视化
  - **工作流程**（算法 1）：
    1. 初始化：观察用户查询、输入图像和记忆。
    2. 循环（直到超时或生成回答）：
       - **Reason**：LLM 分析当前状态，决定是否回答、询问用户或选择工具。
       - **Act**：若需工具，则并行执行选定的工具（ExecuteParallel），返回结果。
       - **Observe**：更新记忆（缓存结果），继续循环。
    3. 输出最终回答或超时响应。
  - **架构**：基于 LangChain/LangGraph 实现模块化，工具独立封装，LLM 可任意替换（开源/闭源），支持本地部署和云部署，满足隐私需求。

## 3. 实验设计
- **数据集与场景**：
  - **ChestAgentBench**（自建）：25,000 个六选一问题（原文为 2,500 个），源自 675 个 Eurorad 临床病例，覆盖 7 个推理类别（检测、分类、定位、比较、关系、诊断、表征）。
  - **CheXbench**：238 个 VQA 问题（Rad-Restruct、SLAKE）和 380 个图像-文本推理问题（OpenI）。
  - **MIMIC-CXR**：3,858 张胸部 X 光片，评估报告生成的 CheXbert F1（14 种/5 种关键发现）。
  - **SLAKE VQA**：114 个胸部 X 光闭式问答样本（英文）。
- **对比方法**：
  - 直接对比：LLaVA-Med、CheXagent、Llama-3.2-90B、GPT-4o。
  - 通过文献引用对比：RadFM、MAIRA-1、LLaVA-Rad、Med-PaLM M 84B、M4CXR。
- **评估指标**：准确率（主要）、召回率（SLAKE VQA）、微平均/宏平均 F1（MIMIC-CXR）。

## 4. 资源与算力
- 文中明确提到：MedRAX 使用 **GPT-4o** 作为核心 LLM，部署在 **单张 NVIDIA RTX 6000 GPU** 上运行工具模型（非训练，仅推理）。
- 未提及具体训练时长（因框架无需额外训练），也未说明推理时具体吞吐量。工具模型本身（如 CheXagent、MedSAM）预先训练好，作者只负责集成。

## 5. 实验数量与充分性
- **实验组数**：总计 4 大基准（ChestAgentBench、CheXbench、MIMIC-CXR、SLAKE VQA），其中 ChestAgentBench 有 7 个细分类别，CheXbench 有 2 个子集，MIMIC-CXR 有 4 个 F1 指标。
- **是否充分**：
  - **优点**：覆盖了 VQA、报告生成、细粒度推理等多任务，对比了 8+ 种基线（含通用和专用模型）。
  - **不足**：
    - **缺乏消融实验**：未分析各工具对性能的贡献，也未评估不同 LLM 作为推理引擎的影响。
    - **仅评估 CXR**：未扩展到其他影像模态（如 CT、MRI）。
    - **依赖闭源模型**：主要结果基于 GPT-4o，开源版本（如使用 Llama 作推理引擎）效果未知。
- **公平性**：所有基线使用官方实现和推荐配置，重试机制处理无效输出，指标清晰，对比较为客观。

## 6. 主要结论与发现
- **MedRAX 在所有基准上达到 SOTA**：
  - ChestAgentBench 整体准确率 63.1%，显著优于 GPT-4o（56.4%）和 Llama-3.2-90B（57.9%）。
  - CheXbench VQA 平均 68.1%（最高）；MIMIC-CXR 微平均 F1-14 达 79.1%；SLAKE VQA 准确率 90.35%。
- **通用模型优于专用模型**：GPT-4o 和 Llama-3.2-90B 表现优于 CheXagent 和 LLaVA-Med，说明医学专用预训练可能牺牲泛化推理能力。
- **工具集成提升效果**：ReAct 循环可分解复杂查询、利用专用工具补足 LLM 短板，且能解决工具冲突（案例研究显示）。
- **报告生成中微平均高分但宏平均较低**：说明对常见病检测好，对罕见病（如心影增大）识别仍有不足。

## 7. 优点
- **新颖性**：首个统一 CXR 多种分析工具的 LLM 智能体框架，无需额外训练。
- **模块化与灵活性**：工具可随时增删、替换；支持并行执行；LLM 可切换（开源/闭源），适应不同隐私需求。
- **全面基准 ChestAgentBench**：2,500 个多步推理问题，7 个类别，基于专家审核病例，评估更贴近临床。
- **透明化交互**：用户界面显示中间工具输出，提供可解释性。
- **开源共享**：代码、数据、模型权重均已公开，促进可重复性。

## 8. 不足与局限
- **实验局限性**：
  - 未进行消融实验（如去掉某个工具或更换 LLM 的影响）。
  - 仅测试胸部 X 光，未拓展至其他模态或全身影像。
  - 主要依赖 GPT-4o，若更换为较弱 LLM 可能性能大幅下降。
- **技术局限**：
  - **矛盾工具输出处理弱**：当多个工具给出冲突结果时，系统有时难以有效集成。
  - **计算开销大**：多个工具顺序或并行执行导致推理延迟高于端到端模型。
  - **缺乏不确定性量化**：无法告知用户结果的置信度。
  - **未进行临床验证**：仅在公共数据集上评估，未在真实工作流中测试。
- **偏差风险**：
  - 基准数据来自 Eurorad（病例报告），可能存在发表偏倚（更偏好罕见/典型病例）。
  - 工具模型自身可能有训练数据偏差（如 MIMIC-CXR 以欧美人群为主）。

（完）
