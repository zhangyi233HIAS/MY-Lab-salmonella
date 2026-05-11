# 方法与图表描述 (Methods & Figure Legends)

## Materials and Methods

### 数据来源与预处理

本研究对 211 株鸽源细菌分离株进行全基因组测序分析。原始元数据包含 787 个字段（Metadata_with_Tier_Stratification.csv），经预处理提取 18 个基础元数据列、7 个派生列、30 个质粒 Inc/Col 类型列及 702 个 AMR/毒力基因二进制列，生成精简数据集 metadata_small.csv（211 行 × 757 列）。派生变量包括批次代码（batch_code: 0910/1012）、鸽场类型（Farm: Egg/Meat）、月份（Month: Sep/Oct）、物种分组（Species_Group: Top5 + Other）、AMR 基因携带总数（AMR_Count）及质粒类型数（Plasmid_Count）。

### Module 05: MALDI-TOF 鉴定准确率评估

以全基因组测序（WGS）鉴定结果为金标准，评估 MALDI-TOF 质谱鉴定的准确性。排除 9 株 MALDI-TOF 未鉴定（Species_MS = '-'）的样本后，对 202 株有效样本进行分析。种水平准确率定义为 MALDI-TOF 鉴定结果与基因组鉴定结果完全一致的比例。构建核心 4 物种（E. coli, K. pneumoniae, A. baumannii, P. aeruginosa）的混淆矩阵，计算各物种的灵敏度（Sensitivity）、特异度（Specificity）、阳性预测值（PPV）及阴性预测值（NPV）。采用 Wilson 法计算准确率的 95% 置信区间，并通过单样本 z 检验比较总体准确率与 95% 文献阈值的差异。所有统计分析使用 Python 3.11（scipy 1.x）完成。

### Module 06: 富集 vs 非富集比较

将 206 株有效样本（排除 5 株 Enrichment_Status = '-'）分为富集组（Enrichment, n=100）和非富集组（Non-enriched, n=106）。采用卡方检验比较两组的物种组成差异。AMR 基因丰度和质粒携带率的组间比较使用 Mann-Whitney U 检验。基因组质量指标（Completeness, Contamination, Genome_Size, N50）的组间差异同样采用 Mann-Whitney U 检验。按物种分层后，比较 E. coli 和 K. pneumoniae 中两组的 AMR 基因负担差异。单个质粒类型的携带率差异使用 Fisher 精确检验。

### Module 07: 蛋鸽 vs 肉鸽比较

比较蛋鸽厂（Egg, n=187, 9月+10月）和肉鸽厂（Meat, n=24, 仅9月）分离株的差异。物种组成差异采用卡方检验。AMR 基因负担和质粒携带率的组间比较使用 Mann-Whitney U 检验。MDR/XDR 比例差异采用 Fisher 精确检验。按药物类别（9 类）比较耐药率差异。为控制时间混杂因素，额外进行了仅 9 月批次的亚组分析（Egg n=60, Meat n=24）。药物类别耐药率的组间比较使用 Fisher 精确检验。

### Module 08: 质粒谱分析

对 30 种质粒 Inc/Col 类型进行流行率分析。构建质粒 × 物种携带率矩阵，识别在 ≥2 个核心物种中携带率 >10% 的跨物种共享质粒。基于 Jaccard 相似度构建质粒共现矩阵（仅纳入流行率 ≥5% 的 8 种活跃质粒），识别强共现对（Jaccard > 0.3）。采用 Fisher 精确检验评估质粒与 AMR 基因的关联（p < 0.01），对每个主要质粒报告其关联最强的 Top 3 AMR 基因。网络可视化使用 matplotlib 实现，节点大小按流行率缩放，边宽度按 Jaccard 相似度缩放。

### 统计分析

所有统计分析使用 Python 3.11 完成，主要依赖 pandas（数据处理）、scipy.stats（假设检验）和 matplotlib（可视化）。多重比较未进行校正，以探索性分析为主要目的。显著性水平设定为 α = 0.05。

---

## Figure Legends

### Figure 1 (Module 05). MALDI-TOF 质谱鉴定准确率评估。

**(A)** 核心 4 物种的 MALDI-TOF 鉴定准确率（Wilson 95% CI）。虚线表示 95% 文献阈值。E. coli: 98.0% (95%CI: 93.1–99.5%); K. pneumoniae: 89.4% (77.4–95.4%); A. baumannii: 100%; P. aeruginosa: 85.7% (48.7–97.4%)。**(B)** MALDI-TOF 鉴定结果分布：正确鉴定（绿色）、错误鉴定（红色）、未鉴定（灰色）。n=211。

### Figure 2 (Module 05). MALDI-TOF vs WGS 物种鉴定混淆矩阵。

热图显示 MALDI-TOF 鉴定结果（列）与 WGS 基因组鉴定结果（行）的对应关系。对角线为正确鉴定，非对角线为误鉴定。核心 4 物种 + Other 类别。n=202（排除 9 株 MALDI 未鉴定）。蓝色边框标识对角线（正确鉴定）。

### Figure 3 (Module 06). 富集 vs 非富集组比较。

**(A)** 物种组成差异（分组条形图）。Chi²=31.5, p<0.001。富集组 K. pneumoniae 显著偏多（38 vs 11），非富集组 A. baumannii 全部来自非富集组（11 株）。**(B)** AMR 基因携带数分布（小提琴图）。Mann-Whitney U p=0.81，无显著差异。**(C)** 质粒类型数分布（小提琴图）。Mann-Whitney U p=0.84，无显著差异。**(D)** 基因组完整性分布（直方图）。富集组 Completeness 显著更高（p=0.001）。Enrichment: n=100; Non-enriched: n=106。

### Figure 4 (Module 06). 富集效应对质粒与 AMR 的影响。

**(A)** 富集差异显著的质粒类型携带率（Fisher p<0.1）。IncFIA(HI1) 在富集组中显著偏高（5.0% vs 0%, p=0.026）。**(B)** 按物种分层的 AMR 基因负担比较。E. coli: p=0.12; K. pneumoniae: p=0.20，均无显著差异。

### Figure 5 (Module 07). 蛋鸽 vs 肉鸽比较。

**(A)** 物种组成差异。Chi²=31.7, p<0.001。P. aeruginosa 集中在肉鸽（5/7），K. pneumoniae 集中在蛋鸽（48/49）。**(B)** AMR 基因携带数分布。肉鸽 mean=86.5, 蛋鸽 mean=43.6, p=0.014。**(C)** MDR/XDR 状态分布。肉鸽 100% MDR+（24/24），蛋鸽 73.8%（138/187），Fisher p=0.002。**(D)** 质粒携带数分布。p=0.57，无显著差异。Egg: n=187; Meat: n=24。

### Figure 6 (Module 07). 蛋鸽 vs 肉鸽药物类别耐药率。

9 类抗菌药物的耐药率比较。Tetracycline: 蛋鸽 39.0% vs 肉鸽 12.5% (p=0.012); Macrolide: 蛋鸽 33.7% vs 肉鸽 12.5% (p=0.037)。其余类别无显著差异。

### Figure 7 (Module 08). 质粒 Inc 类型流行率。

水平条形图显示 211 株菌中 30 种质粒类型的流行率。Top 5: IncFIB(AP001918) 30.8%, IncI1 Alpha 21.3%, IncX1 19.9%, IncFIC(FII) 17.1%, IncHI2/IncHI2A 13.3%。136/211 (64.5%) 株菌携带至少 1 种质粒。

### Figure 8 (Module 08). 质粒 × 物种携带率热图。

热图显示 18 种活跃质粒（任一物种中 >5%）在 5 个核心物种中的携带率。颜色深度表示携带率（%）。IncFIB(AP001918) 在 E. coli 中携带率最高（59.0%）；IncX1 在 Salmonella 中携带率为 100%；IncHI2/IncHI2A 在 E. coli (15.2%) 和 K. pneumoniae (16.3%) 中携带率几乎相同。

### Figure 9 (Module 08). 质粒共现网络。

节点表示 8 种活跃质粒类型（流行率 ≥5%），节点大小按流行率缩放。边表示 Jaccard 相似度 >0.15 的共现关系，边宽度按 Jaccard 值缩放。强共现对: IncHI2 ↔ IncHI2A (Jaccard=1.0, 完全共现); IncFIB(AP001918) ↔ IncFIC(FII) (0.507); IncR ↔ IncHI1B(pNDM-MAR) (0.5)。

### Figure 10 (Module 08). 质粒-耐药基因关联热图。

热图显示与各质粒类型显著关联的 AMR 基因（Fisher p<0.01）。每个质粒展示关联最强的 Top 2 基因。数值表示该质粒携带者中 AMR 基因的携带率（%）。共识别 137 个显著关联对。关键关联: IncHI2 — blaTEM-1B (53.6%), ARR-3 (71.4%); IncR — rmtB (61.5%), aac(3)-IId (92.3%); IncHI1B — blaSHV-110 (100%), dfrA12 (72.7%)。

---

## Supplementary Tables

### Table S1 (Module 05). MALDI-TOF 错配清单。

24 株 MALDI-TOF 与 WGS 鉴定不一致的分离株列表，包含 Strain_ID、基因组鉴定结果、MALDI-TOF 鉴定结果、组织来源、鸽场类型。

### Table S2 (Module 05). MALDI-TOF 准确率统计。

核心 4 物种的灵敏度、特异度、PPV、NPV 及 95% CI。

### Table S3 (Module 06). 富集比较统计检验汇总。

所有 Mann-Whitney U 检验和卡方检验的结果汇总，包含检验统计量和 p 值。

### Table S4 (Module 07). 蛋鸽 vs 肉鸽药物类别比较。

9 类抗菌药物的耐药率、Fisher 精确检验 p 值。

### Table S5 (Module 08). 跨物种共享质粒清单。

在 ≥2 个核心物种中携带率 >10% 的质粒类型及其在各物种中的携带率。

### Table S6 (Module 08). 质粒共现矩阵。

8 种活跃质粒两两之间的 Jaccard 相似度矩阵。

### Table S7 (Module 08). 质粒-耐药基因关联。

137 个显著关联对（Fisher p<0.01），包含质粒名称、AMR 基因名称、有/无质粒时的携带率及 p 值。
