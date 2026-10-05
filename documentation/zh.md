<!-- ELUCENIA technical documentation · mascc · zh · no clinical/professional/rights approval -->

# MASCC 指数

[条件、来源与许可](https://elucenia.org/zh/tools/mascc)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 疾病负担（发热发作的症状）

`carga`

- `0` — 重度或濒死
- `3` — 中度
- `5` — 无或轻度

### 低血压（收缩压 \< 90 mmHg）

`hipotensao`

- `0` — 是
- `5` — 否

### 活动性慢性阻塞性肺疾病

`dpoc`

- `0` — 是
- `4` — 否

### 癌症类型

`tumor`

- `0` — 血液肿瘤且既往有真菌感染
- `4` — 实体瘤，或血液肿瘤但无既往真菌感染

### 需静脉补液的脱水

`desidratacao`

- `0` — 是
- `3` — 否

### 发热开始的场所

`local`

- `0` — 住院期间
- `3` — 门诊

### 年龄

`idade`

- `0` — ≥ 60 岁
- `2` — \< 60 岁

## 方法版本

MASCC/Klastersky 2000：7领域，总分0–26，界值≥21；ASCO/IDSA 2018背景

## 已记录的公式

疾病负担：无/轻5，中3，重0 · 无低血压5 · 无COPD 4 · 实体瘤4，或无既往真菌感染的血液系统恶性肿瘤4 · 无脱水3 · 门诊3 · 年龄\<60岁2。最高26。

## 限制与适用人群

MASCC ≥21提示并发症风险较低，但不能单独作为出院、口服抗生素或门诊治疗的依据。在ASCO/IDSA 2018指南的情境下，患者选择取决于临床评估、病情稳定性、合并症、遵守复诊安排的能力，以及家中照护者、电话和交通条件。拟接受门诊治疗的患者应在出院前接受至少4小时观察，并须随访。本实现的低血压标准沿用2000年的原始变量：收缩压\<90 mmHg。

## 参考文献

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
