---
title: Democratizing Clinical Risk Prediction with Cross-Cohort Cross-Modal Knowledge Transfer
title_zh: 通过跨队列跨模态知识迁移实现临床风险预测的民主化
authors: "Qiannan Zhang, Manqi Zhou, Zilong Bai, Chang Su, Fei Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=7dJfwHG3GN"
tags: ["query:ehr-agent"]
score: 5.0
evidence: 利用电子健康记录进行临床风险预测
tldr: 针对资源有限临床机构难以训练复杂多模态模型的问题，提出了跨队列跨模态知识迁移框架，仅使用电子健康记录数据即可有效部署临床风险预测模型，通过迁移多模态模型知识提升了预测性能，促进了医疗AI的普惠化。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 826, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1237, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 653, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 656, \"height\": 238, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 653, \"height\": 234, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 696, \"height\": 249, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7djfwhg3gn/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 575, \"height\": 252, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-7djfwhg3gn/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1431, \"height\": 809, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7djfwhg3gn/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1451, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7djfwhg3gn/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 797, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7djfwhg3gn/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 338, \"label\": \"Table\"}]"
motivation: 多数临床机构缺乏多模态数据和计算资源，需利用仅有的EHR数据进行有效预测。
method: 提出跨队列跨模态知识迁移框架，将预训练多模态模型的知识迁移至仅使用EHR的单模态模型。
result: 在多个临床风险预测任务上，该方法在仅使用EHR条件下达到了接近多模态模型的性能。
conclusion: 知识迁移能有效提升低资源场景下基于EHR的临床预测模型表现。
---

## Abstract
Clinical risk prediction plays a crucial role in early disease detection and personalized intervention. While recent models increasingly incorporate multimodal data, their development typically assumes access to large-scale, multimodal datasets and substantial computational resources. In practice, however, most clinical sites operate under resource constraints, with access limited to  EHR data alone and insufficient capacity to train complicated models. This gap highlights the urgent need to democratize clinical risk prediction by enabling effective deployment in data- and resource-limited local clinical settings. In this work, we propose a cross-cohort cross-modal knowledge transfer framework that leverages the multimodal model trained on a nationwide cohort and adapts it to local cohorts with only EHR data. We focus on EHR and genetic data as representative multimodal inputs and address two key challenges. First, to mitigate the influence of noisy or less informative biological signals, we propose a novel mixture-of-aggregations design to enhance the modeling of informative and relevant genetic features. Second,  to support rapid model adaptation in low-resource sites, we develop a lightweight graph-guided fine-tuning method that adapts pretrained phenotypical EHR representations to target cohorts using limited patient data. 
Extensive experiments on real-world clinical data validate the effectiveness of our proposed model.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：临床风险预测对早期疾病检测和个性化干预至关重要。当前许多模型依赖多模态数据（如电子健康记录 EHR、基因数据等），并假设拥有大规模多模态数据集和充足计算资源。然而，实际情况中大多数临床机构（尤其是地方性机构）资源有限，只能访问 EHR 数据，缺乏计算能力和多模态数据来训练复杂模型。
- **研究问题**：如何利用在国家级队列（如 All of Us 研究计划）上训练的多模态模型，将其知识迁移到仅拥有 EHR 数据的资源受限的地方队列，实现准确的临床风险预测，同时不共享敏感患者信息？
- **核心挑战**：
  - 多模态数据（尤其是基因数据）存在噪声和不精确性，难以有效建模。
  - 跨队列的分布偏移（人口特征、数据收集协议等差异）导致模型需要适应目标队列，但地方队列数据量和计算资源有限，难以进行有效微调。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **整体框架**：提出名为 C3M 的跨队列跨模态知识迁移框架，包含三个核心组件：
  1. **基因编码与混合聚合（Mixture-of-Aggregations）**：
     - 对每个患者，将基因视为 token 并嵌入连续空间。
     - 引入多个（M个）可学习的聚合 token，每个作为“专家”，通过多头注意力对不同基因 token 进行加权，生成专家特定的基因表示。
     - 使用共享 Transformer 编码器，输出聚合后的基因表示 h_G 和基因特征重建 logits。
     - 引入基因特征重建损失（加权交叉熵），鼓励聚合 token 关注信息性基因，抑制噪声。
     - 多个专家输出通过平均得到最终基因表示。
  2. **图引导的表型表示微调（Graph-Guided Phenotypical Representation Fine-Tuning）**：
     - 使用预训练的 EHR 基础模型 MOTOR 生成患者初始表型嵌入 h_E。
     - 构建患者-医疗概念二分图，节点包括患者和 EHR 中的医疗概念（如诊断、药物）。边表示患者有该概念记录。
     - 应用图神经网络（GNN）进行消息传递，更新患者嵌入，适应目标队列的分布特征，而无需微调 MOTOR 本身（轻量级）。
  3. **跨模态知识迁移与蒸馏（Cross-Modal Knowledge Transfer with Distillation）**：
     - 使用教师-学生蒸馏框架。教师在源队列上使用基因和 EHR 数据训练，学生仅使用 EHR 数据。
     - 教师模型输入 [h_G; h_E] 输出 logits，学生模型输入 h_E 输出 logits。
     - 学生训练损失：交叉熵 + KL 散度蒸馏损失，超参数 λ_KD 平衡。
- **训练流程**：在源队列上迭代：先微调 MOTOR 表示得到适应后的 h_E，同时编码基因得到 h_G；训练教师模型（分类 + 重建损失 L_rec）；固定教师参数，训练学生模型；训练收敛后将学生模型和图网络迁移到目标队列，使用有限的目标患者数据微调学生模型（仅交叉熵损失）。

## 3. 实验设计：数据集、场景、基准与对比方法

- **数据集**：
  - **源队列**：全国性 All of Us 研究计划，包含 EHR 和基因数据（217 个 ADRD 相关基因），共 11,356 名患者，基因缺失率 26.7%。
  - **目标队列**：三个地方队列：
    - LocalEHR（6,548 名患者）
    - INSIGHT-A（19,062 名患者）
    - INSIGHT-B（17,424 名患者）
  - 所有队列均针对阿尔茨海默病及相关痴呆症（ADRD）预测，预测时间为发病前一年。
- **场景**：源队列训练多模态模型，目标队列仅 EHR 数据可用，且数据分布不同。目标队列仅使用少量（如 500 名）患者进行微调。
- **对比方法**：
  - **模态插补方法**：CMAE、MVAE、GAN、SMIL（通过生成模型补全基因特征）。
  - **模态鲁棒学习方法**：MUSE、MoMKE、DrFuse、CMKD（处理模态缺失但不完全适合本场景）。
- **评估指标**：AUROC、F1 分数、敏感性（95% 特异性）、阳性预测值 PPV（95% 特异性）。
- **实验设置**：源队列按 6:2:2 拆分训练/验证/测试。目标队列随机抽取 500 名患者微调，在 CPU 环境下完成以模拟资源受限。所有方法使用相同的 MOTOR 基础嵌入，进行公平比较。

## 4. 资源与算力

- **明确说明**：目标队列的微调和评估均在 **仅 CPU 环境** 下进行，以模拟实际部署的算力限制。
- **未明确说明**：源队列训练的 GPU 型号、数量、训练时长等具体信息未提及。论文仅提及使用 Adam 优化器，未详细描述训练硬件。

## 5. 实验数量与充分性

- **主要实验**：
  - 在 1 个源队列和 3 个目标队列上与 8 种基线方法对比（表 1），重复 3 次报告均值和标准差。
  - 消融实验（表 2）：去除混合聚合、去除图引导微调、去除 MOTOR、去除基因数据四个变体。
  - 超参数研究：聚合 token 数量（1-4）、Transformer 层数（1-4）、重建损失权重 β、蒸馏权重 λ_KD、微调患者数量（100-500）。
  - 对比图构建策略（是否将基因加入图）。
  - 分析迁移模型 vs. 从头训练的效果（表 4）。
- **充分性与公平性**：
  - 实验覆盖了多种数据集、基线、超参数，消融充分，统计显著性通过标准差体现。
  - 基线方法已按问题设置适配，使用相同基础嵌入，比较公平。
  - 但所有实验仅针对 ADRD 一个疾病，未在其他疾病上验证，可能限制泛化性。

## 6. 论文的主要结论与发现

- C3M 在所有指标上均显著优于基线方法，在源队列（AUROC 79.94%）和三个目标队列（AUROC 71.82%–75.39%）均表现最佳。
- 消融研究表明每个组件（混合聚合、图引导微调、MOTOR、基因数据）均对性能有贡献。
- 混合聚合（2-3 个 token）优于单 token，说明多视角聚合能更好捕捉基因信息；但过多 token（4 个）可能引入冗余噪声。
- 图引导微调有效适应分布偏移，比直接使用 MOTOR 嵌入更好。
- 知识蒸馏成功将基因知识迁移到仅 EHR 的学生模型。
- 即使使用少量目标患者（如 100 名）微调，C3M 仍取得良好性能，且迁移模型显著优于从头训练。

## 7. 优点：方法或实验设计上的亮点

- **方法创新性**：
  - 混合聚合设计（Mixture-of-Aggregations）：通过多个专家注意力与重建损失，从噪声基因数据中提取信息性特征，比单 token 更强。
  - 轻量图引导微调：利用患者-概念二分图和 GNN 调整预训练嵌入，无需微调基础模型，适合资源受限场景。
  - 跨队列跨模态蒸馏：实现从多模态到单模态的知识迁移，保护隐私（无需数据共享）。
- **实验设计**：
  - 使用多个真实世界队列（全国性+地方性），模拟实际分布偏移和资源限制。
  - 基线方法经过适配，对比全面。
  - 消融和超参数研究充分探究组件作用。
  - 在 CPU 环境下微调，验证了低资源可行性。

## 8. 不足与局限

- **疾病范围局限**：仅针对阿尔茨海默病和相关痴呆症，未在其他慢性疾病（如帕金森病、心血管病等）上验证泛化能力。论文本身在结论中承认这一限制。
- **基因数据使用**：仅考虑了二元基因突变指示，未利用基因多效性或连续值（如多基因风险评分），可能丢失信息。
- **假设与简化**：
  - 假设目标队列有少量有标签数据可供微调，但实际情况中标签获取可能困难。
  - 基因数据仅从 GWAS 目录选取 ADRD 相关基因，可能忽略其他重要基因。
- **算力信息不完整**：未报告源模型训练的 GPU 配置和时间，不利于复现和资源评估。
- **公平性与偏差**：论文讨论了更广泛的社会影响（促进公平），但未分析模型在不同亚群（如种族、性别）上的表现差异，可能存在公平性风险。
- **比较基线**：虽然对比了多种方法，但这些基线原本并非为跨队列跨模态缺失设计，可能未能完全体现其最优性能。

（完）
