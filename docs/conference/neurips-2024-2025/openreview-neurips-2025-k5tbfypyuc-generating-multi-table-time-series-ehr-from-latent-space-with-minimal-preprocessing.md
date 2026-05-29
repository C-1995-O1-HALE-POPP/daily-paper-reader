---
title: Generating Multi-Table Time Series EHR from Latent Space with Minimal Preprocessing
title_zh: 从潜空间生成最少预处理的多表时间序列电子健康记录
authors: "Eunbyeol Cho, Jiyoun Kim, Minjae Lee, Sungjin Park, Edward Choi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=k5TbfYPYuc"
tags: ["query:ehr-agent"]
score: 7.0
evidence: 生成合成多表时间序列电子健康记录，可用于医疗智能体评估
tldr: 针对电子健康记录隐私限制导致数据共享难的问题，提出了RawMed框架，首次能生成接近原始记录的多表时间序列合成EHR数据，采用文本表示与压缩技术捕捉复杂结构，为医疗智能体的评估提供了高质量合成数据，有利于隐私保护下的性能测试。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5tbfypyuc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1426, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5tbfypyuc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 256, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5tbfypyuc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1412, \"height\": 946, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5tbfypyuc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1224, \"height\": 2165, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 579, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 956, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1460, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 655, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 741, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 681, \"height\": 456, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1493, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1249, \"height\": 799, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 790, \"height\": 497, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 1102, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1449, \"height\": 677, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1492, \"height\": 660, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 626, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 563, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 997, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5tbfypyuc/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1322, \"height\": 258, \"label\": \"Table\"}]"
motivation: 隐私法规限制真实EHR共享，需合成数据支撑医疗研究但现有方法只能生成简单特征。
method: 提出RawMed框架，使用文本表示和压缩技术从潜空间生成多表时间序列合成EHR。
result: 生成的合成EHR在统计相似性和下游任务性能上接近真实数据，支持医疗智能体评估。
conclusion: RawMed提供了可行的隐私保护EHR合成方案，助力医疗AI研究。
---

## Abstract
Electronic Health Records (EHR) are time-series relational databases that record patient interactions and medical events over time, serving as a critical resource for healthcare research and applications. However, privacy concerns and regulatory restrictions limit the sharing and utilization of such sensitive data, necessitating the generation of synthetic EHR datasets.
Unlike previous EHR synthesis methods—which typically generate medical records consisting of expert-chosen features (e.g., a few vital signs, structured codes only)—we introduce RawMed, the first framework to synthesize multi-table, time-series EHR data that closely resembles raw EHRs.
Using text-based representation and compression techniques, RawMed captures complex structures and temporal dynamics with minimal lossy preprocessing. 
We also propose a new evaluation framework for multi-table time-series synthetic EHRs, assessing distributional similarity, inter-table relationships, temporal dynamics, and privacy. Validated on two open-source EHR datasets, RawMed outperforms baseline models in fidelity and utility. The code is available at [https://github.com/eunbyeol-cho/RawMed](https://github.com/eunbyeol-cho/RawMed)

---

## 论文详细总结（自动生成）

# 论文中文详细总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：电子健康记录（EHR）是时间序列关系数据库，包含患者历史医疗事件，对医疗AI研究至关重要。但EHR包含敏感个人信息，受隐私法规限制难以共享和利用。
- **现有方法不足**：已有合成EHR方法通常仅生成专家选择的少量特征（如少数生命体征、结构化代码），严重依赖特征选择和复杂有损预处理（如数值分箱、聚合、术语归一化），导致数据失真且限制了下游任务的灵活性。
- **本文目标**：提出RawMed，第一个能够生成**多表时间序列原始EHR**（保留所有列和原始值）的框架，以最小预处理代价保留真实数据结构和时序动态，同时保护隐私。

## 2. 方法：核心思想、关键技术细节、流程
### 2.1 数据表示与预处理
- 将每个患者的事件序列表示为 `[e_1, e_2, ..., e_{np}]`，每个事件包括时间戳 `t_pi`、事件类型 `ϵ_pi`（如实验室、处方、输注）和一组列-值对 `a_pi`。
- 采用**文本表示**：将每个事件序列化为字符串，如 "lab item Glucose value 95 uom mg/dL"。用Bio+Clinical BERT tokenizer分词，加上类型嵌入和数字位置嵌入，得到嵌入 `x_pi ∈ R^{L×F}`（L=128, F=256）。

### 2.2 事件级压缩（Event-level Compression）
- 使用**残差量化（Residual Quantization, RQ）** 对文本嵌入进行压缩，克服标准VQ-VAE在低相关、独立分布列（如体重）上的失真。
- 编码器（五层1D CNN）将 `x_pi` 映射到潜空间 `ẑ_pi ∈ R^{L_z×F_z}`（L_z=4, F_z=256）。
- RQ将每个潜向量分解为D个分量（D=2），每个分量通过查表量化到码本（K=1024），最终得到 `z_pi = sum_{d=1}^D lut(k_d)`。
- 解码器（转置CNN）重建文本、类型和数字位置嵌入，损失函数为重建损失 + 承诺损失。

### 2.3 时间序列建模（Temporal Inter-event Modeling）
- 将每个事件替换为压缩后的离散索引：`k_pi ∈ [K]^{L_z×D}`（4×2=8个索引）。
- 时间戳表示为固定长度数字序列（10分钟分辨率，如720分钟→[7,2]）。
- 构建统一序列：`[τ_1, k_1, τ_2, k_2, ..., τ_n, k_n]`，总长度≈事件数×(2+8)。
- 使用**TempoTransformer**（12层Transformer，因果注意力）对该序列进行自回归建模，优化负对数似然。

### 2.4 采样与后处理
- 用Top-k采样生成合成序列，应用两类后处理：
  1. **事件级验证**：检查表名、列名有效性（Levenshtein距离纠错），去除数值中的非法字符。
  2. **患者级验证**：丢弃包含无效事件的患者；检查时间顺序与观察窗（如12小时），移除乱序或超界事件。
  3. **列级约束**：数值限制在真实数据范围内；类别值映射到最近有效值。

### 2.5 条件生成扩展
- 可将静态特征（年龄、性别、入院诊断）或初始部分事件作为条件，与事件序列一起建模。

## 3. 实验设计
### 3.1 数据集
- **主要数据集**：MIMIC-IV（62,704患者，约7M行）和eICU（143,812患者，约7M行），均使用三个时间序列表：实验室、处方、输入事件。观察窗设为12小时（部分实验用6h/24h）。
- **额外数据集**：MIMIC-IV-ED（急诊科，6小时观察窗），验证泛化性。

### 3.2 基线方法
- **无压缩基线**：RealTabFormer（基于LLaMA 3.1-8B+QLoRA），直接在文本空间建模。
- **多表生成基线**：SDV（高斯Copula）、RC-TGAN（GAN）、ClavaDDPM（扩散模型）。
- **真实数据**作为上界参考。

### 3.3 评估框架（首次系统评估原始多表时间序列EHR）
- **单表评估**：
  - 列密度估计（CDE）和物品级CDE（I-CDE）
  - 列对相关性（PCC）和物品级PCC（I-PCC）
  - 预测相似性（XGBoost，ER和SMAPE）
- **多表时间序列评估**：
  - 临床效用（11个下游预测任务，用GenHPF和MEDS-TAB两种表示，AUROC）
  - 时序保真（时间间隔分布KS、事件数量分布KS）
  - 下一个事件预测（LSTM多标签分类F1）
  - 隐私评估（成员推断攻击MIA准确率）

## 4. 资源与算力
- **原文明确说明**：
  - 事件压缩模块：单张NVIDIA A6000 GPU，训练<24小时。
  - TempoTransformer：MIMIC-IV用3张A6000 GPU，eICU用1张A6000，均<48小时。
  - RealTabFormer基线：单张RTX 3090，MIMIC-IV约10天，eICU约20天。
  - 其他基线训练时间：ClavaDDPM<3小时（单A6000），RC-TGAN<10小时（单RTX 3090），SDV未明确。
- **总体算力**：中等规模，未使用大规模集群。

## 5. 实验数量与充分性
- **覆盖多个数据集**：两个主要ICU数据集（MIMIC-IV, eICU）加一个急诊数据集（MIMIC-IV-ED），不同观察窗（6h/12h/24h）。
- **消融实验**：
  - RQ vs. VQ对比（图2、表14）
  - 移除时间令牌化/时间分离/残差量化的组件消融（表6）
  - 压缩 vs. 非压缩对比（表5）
  - 条件生成实验（表17）
  - 可扩展性实验（不同观察窗，表15）
- **多维度评估**：单表、多表、时序、隐私、下游任务，指标全面。
- **统计可靠性**：部分结果报告多次运行均值和标准差（表4、11、12、13）。
- **结论**：实验充分、客观，对比了最相关的基线方法，公平性可接受（虽然基线方法原本不支持原始数据生成，但文章尽量适配和对比）。

## 6. 主要结论与发现
- RawMed在单表指标（CDE、I-CDE、PCC、I-PCC、预测相似性）上全面优于所有基线。
- 在多表时间序列评估中，RawMed显著优于基线，尤其是在时间间隔分布（KS低至0.01-0.03）和下一个事件预测（F1接近真实数据）上。
- 临床效用AUROC与真实数据差距很小（MIMIC: 0.87 vs 0.90；eICU: 0.83 vs 0.87），远好于ClavaDDPM（0.68/0.66）等基线。
- 隐私保护强（MIA准确率≈0.5，接近随机猜测）。
- 压缩相比非压缩（RealTabFormer）显著降低序列长度（84%减少）且提升保真度。
- 残差量化RQ优于VQ，能更好保留独立分布的数值列。
- 条件生成（加入静态或初始事件）能进一步提升生成质量。

## 7. 优点
- **首创性**：第一个生成多表时间序列原始EHR（保留所有列和原始值）的框架，突破现有方法特征选择与有损预处理的局限。
- **通用性**：文本表示+压缩方法可适配不同数据库模式，无需领域特定工程。
- **高效**：通过潜空间压缩大幅降低序列长度（84%），使自回归建模可行。
- **评估体系**：提出完整的原始EHR评估框架，涵盖分布相似性、表间关系、时序动态、隐私等，填补了该领域空白。
- **全面的消融与对比**：与多种基线（非压缩、多表GAN/扩散）系统对比，证明压缩和时序建模的有效性。
- **可复现**：代码开源，实验细节充足。

## 8. 不足与局限
- **表数量有限**：当前仅聚焦三个主要时间序列表（实验室、处方、输注），未能覆盖数十个表的完整数据库，扩展性有待验证。
- **不支持完整条件生成**：作为初始工作，仅实现无条件生成，虽扩展了静态条件，但更复杂的条件控制（如特定疾病、人口统计生成）未充分探索。
- **后处理过滤率高**：患者级拒绝率较高（MIMIC-IV达54.53%），说明生成数据质量仍有提升空间，可能影响合成样本量。
- **错误分析不足**：虽观察到拼写错误等问题，但未深入分析错误模式来源和影响，缺乏对生成文本语义准确性的评估。
- **计算资源消耗**：TempoTransformer训练仍需多GPU，对资源有限团队可能不够友好。
- **对比局限**：基线方法（SDV, RC-TGAN, ClavaDDPM）并非设计用于原始多表时间序列数据，虽然尽力适配，但公平性可能略有偏差。
- **隐私评估单一**：仅使用MIA，缺少差分隐私或更严格的隐私攻击（如属性推断）评估。

（完）
