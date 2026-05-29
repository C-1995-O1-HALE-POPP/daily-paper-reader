---
title: Integrating Drug Substructures and Longitudinal Electronic Health Records for Personalized Drug Recommendation
title_zh: 整合药物亚结构与纵向电子健康记录的个性化药物推荐
authors: "Wenjie Du, Xuqiang Li, Jinke Feng, Shuai Zhang, Wen Zhang, Yang Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ml2TynfZI0"
tags: ["query:ehr-agent"]
score: 4.0
evidence: 使用纵向EHR数据进行药物推荐，与使用EHR的医疗代理相关
tldr: 现有药物推荐方法未充分利用分子亚结构和临床实践。本文提出SubRec框架，融合药物分子结构与患者纵向EHR，通过统一表示学习生成个性化推荐。在真实数据集上，SubRec优于基线，验证了整合EHR与化学结构信息的有效性，为医疗代理利用EHR提供了方法支撑。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 635, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1419, \"height\": 702, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 706, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1359, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 871, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ml2tynfzi0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 594, \"height\": 475, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 458, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 781, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1149, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 458, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 707, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 736, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1359, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ml2tynfzi0/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 884, \"height\": 197, \"label\": \"Table\"}]"
motivation: 现有方法忽略药物分子亚结构和临床实践，推荐质量受限。
method: 提出SubRec框架，联合学习患者EHR表示和药物分子结构表示进行推荐。
result: 在真实EHR数据集上，SubRec在精确度和安全性指标上均优于现有方法。
conclusion: 整合EHR与药物结构信息可显著提升药物推荐效果。
---

## Abstract
Drug recommendation systems aim to identify optimal drug combinations for patient care, balancing therapeutic efficacy and safety. Advances in large-scale longitudinal EHRs have enabled learning-based approaches that leverage patient histories such as diagnoses, procedures, and previously prescribed drugs, to model complex patient-drug relationships. Yet, many existing solutions overlook standard clinical practices that favor certain drugs for specific conditions and fail to fully integrate the influence of molecular substructures on drug efficacy and safety. In response, we propose \textbf{SubRec}, a unified framework that integrates representation learning across both patient and drug spaces. Specifically, SubRec introduces a conditional information bottleneck to extract core drug substructures most relevant to patient conditions, thereby enhancing interpretability and clinical alignment. Meanwhile, an adaptive vector quantization mechanism is designed to generate patient–drug interaction patterns into a condition-aware codebook which reuses clinically meaningful patterns, reduces training overhead, and provides a controllable latent space for recommendation. Crucially, the synergy between condition-specific substructure learning and discrete patient prototypes allows SubRec to make accurate and personalized drug recommendations. Experimental results on the real-world MIMIC III and IV demonstrate our model's advantages.  
The source code is available at \href{https://anonymous.4open.science/r/DrugRecommendation-5173}{https://anonymous.4open.science/}.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有药物推荐系统未能充分利用**临床实践规律**（即特定疾病常对应特定药物，与患者个体差异关系较小）以及**药物分子亚结构**对药效和安全性（如药物‑药物相互作用，DDI）的显著影响。
- **背景**：大规模纵向电子健康记录（EHR）使得基于深度学习的推荐成为可能，但已有方法要么直接建模完整的患者病史导致计算复杂、难以泛化，要么采用规则分解（如BRICS）破坏药物功能性亚结构的完整性，且未根据患者当前病情动态提取相关子结构。
- **研究意义**：提出统一框架 SubRec，同时学习患者‑药物交互表示和分子亚结构表示，以提高推荐准确性、安全性和可解释性。

## 2. 论文提出的方法论

### 核心思想
- **双空间联合表示**：在患者空间，通过 Transformer 编码器融合诊断与操作序列；在药物空间，利用**条件信息瓶颈（CIB）** 提取与当前患者状态最相关的核心分子亚结构。
- **自适应向量量化（VQ）**：将患者‑药物交互模式聚类为离散码本，实现轻量、可复用的原型匹配，避免高维潜变量的变分建模不稳定性。

### 关键技术细节
- **患者表示模块**：分别用单层 Transformer Encoder 建模诊断序列和操作序列，输出嵌入拼接得到患者状态向量 \(e^{(i)}\)。
- **药物表示与亚结构捕获**：
  - 使用 GIN 编码药物分子图得到节点嵌入 \(E\)。
  - 将 \(E\) 与 \(e^{(i)}\) 拼接后经 MLP 得到交互特征 \(H\)。
  - **条件信息瓶颈**：基于噪声注入 + Gumbel-Sigmoid 实现可微的节点级别选择（保留与患者状态相关的节点，替换不重要的节点为高斯噪声），优化目标为最小化预测损失 + 压缩损失（式 15）。
  - 对每个药物 \(d\) 获得亚结构池化表示 \(z_d\)，构成药物嵌入表 \(Z_m^{(i)}\)。
- **向量量化模块**：
  - 维护码本 \(W = \{(e_m, v_m)\}\)，每对包含患者原型和对应药物标签。
  - 对当前患者 \(e^{(i)}\) 最近邻搜索得到码本索引 \(k\)，获取其关联药物 \(v_k\)。
  - 更新码本的损失 \(L_{vq}\) 包含患者嵌入和药物标签的承诺损失（式 18）。
- **推荐预测模块**：
  - 使用注意力读取（式 19）整合患者状态与药物亚结构嵌入。
  - 结合码本药物信息 \(v_k\) 计算 \(o_d^{(i)}\)（式 20）。
  - 最终通过 sigmoid 输出多标签预测 \(\hat{y}^{(i)}\)。
- **损失函数**：总损失 \(L = \alpha (L_{pred} + \beta L_{comp} + \gamma L_{vq}) + (1-\alpha) L_{DDI}\)，其中 \(L_{pred}\) 为二元交叉熵 + 多标签 margin loss，\(L_{DDI}\) 惩罚药物对出现已知交互。

## 3. 实验设计

### 数据集与场景
- **数据集**：MIMIC-III 与 MIMIC-IV 真实世界 ICU 数据库，包含诊断、操作和药物记录。统计信息见附录 B（表 3）。
- **场景**：
  - 主实验：常规多标签药物推荐（表 1）。
  - 额外场景：单药物推荐（表 5，仅极少历史信息）。
  - 落伍场景仿真：仅使用有限次就诊（图 4）。

### Benchmark 与对比方法
- **评估指标**：Jaccard 相似度、PRAUC、F1 分数、DDI 率。
- **基线方法**（共 10 个）：
  - 通用方法：ECC、LEAP、4SDrug
  - 纵向历史方法：RETAIN、VITA、GAMENet、COGNet
  - 分子亚结构方法：SafeDrug、MoleRec

## 4. 资源与算力

- **文中明确说明**：
  - GPU：NVIDIA Tesla V100 16GB（共享环境）。
  - 训练时间：SubRec 约 20.63 小时（主配置，码本大小 32）。
  - 测试时间：10 次平均 4.5 分钟。
  - 内存与参数量：1762 MB / 2.97M 参数（码本 32）。
- **优化策略**：早期停止可缩短至 8.71 小时；专用 GPU 可进一步降至 7.23 小时（表 8）。
- **未明确说明**：GPU 数量（推测单卡）、总能耗、分布式训练情况。

## 5. 实验数量与充分性

- **主实验**：两个数据集（MIMIC-III/IV）各对比 10 个基线，结果带标准误差（表 1）。
- **消融实验**：四个变体（RNN 编码器、去除亚结构模块、去除码本模块、完整 SubRec），展示各模块贡献（表 2）。
- **敏感性分析**：对超参数 \(\beta\)（图 3）、\(\delta\) 与码本大小（图 5 与表 6）、\(\gamma\) 的影响。
- **案例研究**：可视化码本嵌入的 t-SNE 聚类（图 6），并展示诊断‑药物重叠实例。
- **额外场景**：单药物推荐（表 5）、有限历史场景（图 4）。
- **充分性评价**：实验覆盖多个方面（准确率、DDI 安全、模块有效性、参数影响、可解释性），且使用标准数据集和公平的评估协议（t-检验）。但仅在两个相似（MIMIC）数据集上验证，缺乏对跨机构或不同疾病领域的泛化测试。

## 6. 论文的主要结论与发现

1. **SubRec 在准确性和安全性上均达到最优**：在 MIMIC-III/IV 上 Jaccard、PRAUC、F1 均显著优于所有基线，DDI 率低于或持平最佳基线。
2. **患者病情相似度与药物推荐相似度正相关**（Pearson 0.53），验证了利用患者原型进行推荐的合理性。
3. **条件信息瓶颈有效提取与患者状态相关的核心药物亚结构**，避免规则分解破坏功能基团连通性。
4. **向量量化码本** 通过学习离散的患者‑药物原型，提升训练稳定性和推理效率，同时提供可解释性（码本嵌入形成清晰聚类）。
5. **在数据稀疏场景下表现稳健**（单药推荐、有限历史），优于依赖大量历史经验的模型（如 COGNet）。

## 7. 优点

- **创新性**：提出条件信息瓶颈（CIB）用于药物分子子结构提取，首次将患者病情作为条件变量，实现动态、个性化的药物表示。
- **技术亮点**：自适应向量量化（VQ）将无限的患者‑药物组合压缩为有限原型，避免了高维变分建模的不稳定性；结合噪声注入与 Gumbel-Sigmoid 实现可微的子结构选择。
- **临床对齐**：充分考虑临床实践（同类疾病常用相同药物），利用码本原型加速推荐并增强可解释性。
- **安全性控制**：显式 DDI 损失 + 动态超参数 \(\alpha\) 平衡预测与安全。
- **实验严谨**：多维度消融、敏感性分析、统计显著性（t-检验）；公开代码提升可复现性。

## 8. 不足与局限

- **对分布外（OOD）病例适应性有限**：码本仅基于训练数据，当新患者病情模式显著不同时需重新训练或扩展码本。
- **依赖完整分子图信息**：对于无精确分子结构的药物（如中药复方）不适用。
- **计算开销较大**：相比轻量基线（如 GAMENet），参数量和训练时间显著增加（附录 I 表 7），可能限制在资源受限场景的部署。
- **数据集单一**：仅使用 MIMIC（ICU 数据），未在门诊、专科等多样化 EHR 上验证，可能存在领域偏差。
- **可解释性验证不足**：虽然可视化了码本聚类和子结构提取，但未进行专家评估或临床有效性验证（如药理机制验证）。
- **假设忽略患者个体差异的极端情况**：论文强调“相似病情用相似药物”，但部分患者因过敏、共病等需要个体化调整，模型可能过度依赖原型而忽略罕见差异。

（完）
