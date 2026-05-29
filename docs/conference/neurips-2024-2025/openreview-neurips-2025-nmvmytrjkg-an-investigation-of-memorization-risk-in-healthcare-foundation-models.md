---
title: An Investigation of Memorization Risk in Healthcare Foundation Models
title_zh: 医疗基础模型记忆化风险研究
authors: "Sana Tonekaboni, Lena Stempfle, Adibvafa Fallahpour, Walter Gerych, Marzyeh Ghassemi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=NMvMYtRjkg"
tags: ["query:ehr-agent"]
score: 5.0
evidence: 评估基于EHR训练的医疗模型的记忆化风险，与使用EHR的医疗AI评估相关
tldr: 基于EHR的医疗基础模型可能记忆患者隐私信息。本文设计了一套黑盒评估测试，从嵌入层和生成层检测记忆化风险，并区分泛化与有害记忆。在公开EHR数据集上验证了方法的有效性，为医疗AI的隐私评估提供了工具。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1401, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 239, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1332, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1440, \"height\": 836, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1437, \"height\": 429, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nmvmytrjkg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1361, \"height\": 865, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1496, \"height\": 650, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1464, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 741, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1492, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1531, \"height\": 651, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nmvmytrjkg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1454, \"height\": 396, \"label\": \"Table\"}]"
motivation: 医疗基础模型记忆患者信息引发隐私担忧，现有评估方法不足。
method: 提出黑盒记忆化评估套件，包括嵌入级和生成级检测方法。
result: 在公开EHR数据上成功识别记忆化风险，并能区分泛化与有害记忆。
conclusion: 该评估框架有助于确保医疗AI的隐私安全性。
---

## Abstract
Foundation models trained on large-scale de-identified electronic health records (EHRs) hold promise for clinical applications. However, their capacity to memorize patient information raises important privacy concerns. In this work, we introduce a suite of black-box evaluation tests to assess privacy-related memorization risks in foundation models trained on structured EHR data. Our framework includes methods for probing memorization at both the embedding and generative levels, and aims to distinguish between model generalization and harmful memorization in clinically relevant settings. We contextualize memorization in terms of its potential to compromise patient privacy, particularly for vulnerable subgroups. We validate our approach on a publicly available EHR foundation model and release an open-source toolkit to facilitate reproducible and collaborative privacy assessments in healthcare AI.

---

## 论文详细总结（自动生成）

# 中文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：基于电子健康记录（EHR）训练的基础模型（EHR-FM）虽然在临床应用中前景广阔，但可能记忆并暴露患者的隐私信息，即使数据已经过去标识化处理。现有关于记忆化的工作多关注大语言模型（LLM），对EHR结构化数据模型的隐私风险评估不足，且忽略了临床部署的上下文背景。
- **核心问题**：如何系统性地评估EHR-FM的记忆化风险，并区分“良性泛化”（如根据症状合理推断疾病）与“有害记忆化”（如无临床依据地泄露患者敏感属性）？
- **整体含义**：该研究旨在为医疗AI提供一套实用、可复现的隐私评估框架，帮助开发者在模型发布前识别和缓解记忆化风险，从而保护患者隐私。

## 2. 论文提出的方法论

- **核心思想**：针对EHR-FM（通常以黑盒提示形式访问），设计六项测试（T1–T6），从“生成记忆化”（模型生成的代码序列与训练样本的相似度）和“嵌入记忆化”（从模型嵌入中恢复训练信息）两个维度量化记忆化，并进一步评估其隐私风险。
- **关键技术细节**：
  - **生成记忆化**：定义3.1——给定提示p，模型生成的序列s与训练样本x中的[p || s]部分一致。
  - **嵌入记忆化**：定义3.2——从模型嵌入z中可恢复训练样本x的信息。
  - **六项测试**：
    - **T1（轨迹记忆化）**：比较生成序列与真实轨迹的相似度。使用改进的Earth Mover’s Distance（EMD）度量，其中嵌入h(·)由MedBERT（专门针对EHR语料预训练的BERT）生成，并加入时间惩罚项（公式1）。
    - **T2（敏感属性测试）**：排除敏感属性相关代码后，评估模型在生成序列中泄露这些属性的概率（如HIV、药物滥用、心理健康诊断）。
    - **T3（探测测试）**：训练一个分类器g(·)，从冻结的模型嵌入中预测敏感属性。在高精度下认为嵌入泄露了隐私。
    - **T4（成员推断测试）**：基于模型对生成序列的置信度（如最小概率token的对数概率期望）判断样本是否属于训练集。
    - **T5（扰动测试）**：修改个人信息（如年龄）后重新生成，观察敏感属性是否消失，从而区分个体级记忆化与群体级泛化。
    - **T6（子群体测试）**：针对稀有诊断、高龄等易识别子群体，应用T1–T5评估其隐私风险。
- **算法流程**（文字说明）：以黑盒方式向模型输入不同级别的提示（随机、静态属性、前N个代码），获取生成序列或嵌入，依次执行上述测试。若模型在无合理临床依据的情况下泄露敏感信息，则标记为“有害记忆化”。

## 3. 实验设计

- **数据集**：MIMIC-IV（公开可获取的EHR数据集），包含结构化医疗代码（诊断、用药、检查等）及时间戳。
- **基准模型**：EHRMamba2——同时支持患者嵌入学习和EHR生成（预测）的开源EHR-FM，训练在MIMIC-IV上，架构细节公开。
- **对比方法**：本文未与其他记忆化检测方法进行直接对比，主要展示所提测试框架在单一模型上的效果。但通过不同提示级别（随机、静态、10/20/50代码）及不同敏感属性类别，进行了内部分析。
- **评估指标**：AUROC、AUPRC、精确率、召回率、距离度量（d_EMD）、预测概率分布等。

## 4. 资源与算力

- 论文**未明确说明**训练或测试所用的GPU型号、数量、训练时长等具体资源信息。仅在附录中指出计算资源需求取决于EHR-FM的推理成本，因为方法依赖于模型生成序列进行评价。
- 因此，无法量化报告算力消耗。

## 5. 实验数量与充分性

- **实验组数**：
  - T1：在3K样本上对不同提示级别（随机、静态、10/20/50代码）各生成100个代码，比较距离分布。
  - T2：对三类敏感属性（传染病、物质滥用、心理健康）在不同提示长度下报告AUROC、AUPRC、精确率、召回率及阳性预测案例数。
  - T3：使用不同比例的训练数据（0.1%、10%、20%）训练探测分类器，报告多个指标。
  - T4：在10K训练/测试样本上比较成员检测得分分布。
  - T5：对识别出的危险样本（如T2中阳性案例）进行年龄扰动实验，观察敏感属性概率变化。
  - T6：对稀有诊断（出现仅一次）和高龄（>85岁）子群体执行T2测试。
- **充分性与公平性**：
  - 实验覆盖了生成和嵌入两个层面，并考虑了不同攻击者知识（提示长度、数据量）。
  - 但仅使用单一模型（EHRMamba2）和单一数据集（MIMIC-IV），缺少跨模型、跨数据集的验证，可能限制结论的泛化性。
  - 未与现有记忆化检测方法（如Carlini等人的提取攻击）进行定量比较，实验对比性不足。

## 6. 论文的主要结论与发现

- **T1（轨迹记忆化）**：提示信息越多，生成序列与真实轨迹越相似（距离越小）。但表现最好的样本往往是常见代码（如常规实验室正常值），不直接对应高风险泄露。
- **T2（敏感属性）**：仅凭年龄等静态属性无法泄露敏感信息；但增加提示代码后，模型可能泄露敏感诊断。部分泄露具有合理临床依据（如低CD8计数预测HIV），但也发现无相关线索仍预测药物滥用的案例（如仅因摔倒就诊）。
- **T3（嵌入探测）**：从嵌入中直接提取敏感属性非常困难，AUROC约0.5，无显著记忆化信号。
- **T4（成员推断）**：基于模型置信度的成员检测得分在训练集与测试集间差异不显著，表明模型未明显泄露成员身份。
- **T5（扰动测试）**：对某些样本，改变年龄后敏感属性预测概率变化不大，说明模型依赖泛化模式而非个体记忆（如年龄-疾病关联）。但若小改动导致预测突变，则表明个体级记忆化（高风险）。
- **T6（子群体测试）**：罕见代码（仅出现一次）并未导致普遍的高泄露风险，但发现了两个案例（镇静剂依赖、轻度躁狂发作）可能因统计关联被高概率预测，需进一步验证。高龄子群体同样未检测到明显记忆化。
- **总体**：当前基准模型在多数测试中表现良好，但存在少数高风险案例（尤其是T2中无基预测、T5中年龄敏感样本），需在模型发布前进行后处理或再训练。

## 7. 优点

- **上下文感知评估**：区别于传统“是否泄露”的二元判断，引入了临床上下文（如合理的基于症状的推断 vs 无关联的记忆）。
- **多维覆盖**：同时评估生成级和嵌入级记忆化，并区分群体泛化与个体记忆。
- **实用性**：针对黑盒、仅提示访问的场景设计，贴近实际部署；提供开源工具包，便于复现和扩展。
- **关注弱势群体**：明确评估稀有诊断、高龄等高风险子群体，体现对隐私公平性的重视。

## 8. 不足与局限

- **实验覆盖面有限**：仅在单个模型（EHRMamba2）和单个数据集（MIMIC-IV）上验证，结论的泛化性未知。
- **缺乏对比基线**：未与现有记忆化/隐私攻击方法（如Carlini的提取、Shokri的成员推断）进行定量比较，难以定位所提框架的优劣。
- **攻击者模型假设简化**：假设攻击者只能进行黑盒提示访问，未考虑更强大的白盒或灰盒攻击。
- **计算资源未报告**：无法评估方法在实际部署中的成本。
- **测试未穷尽**：如时间依赖性、多模态数据等复杂情况未涉及；敏感属性分类示例性，且可能因数据集而异。
- **依赖模型架构**：部分测试（如T3嵌入探测）依赖于模型是否提供嵌入，对于纯解码器模型需调整。
- **隐私风险评估的主观性**：T5中“小扰动导致预测突变”的阈值未明确量化，可能依赖专家判断。

（完）
