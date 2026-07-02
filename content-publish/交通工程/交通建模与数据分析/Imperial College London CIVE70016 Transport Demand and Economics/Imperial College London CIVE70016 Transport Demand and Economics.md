---
type: course
course: Imperial College London CIVE70016 Transport Demand and Economics
course_title: Transport Demand and Economics
course_code: CIVE70016
school: Imperial College London
school_link: "[[Imperial College London]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通建模与数据分析
major_code: 06-交通建模与数据分析
major_link: "[[交通建模与数据分析]]"
teacher: Dr Jacek Pawlak
knowledge_cluster:
  - discrete-choice
  - biogeme
  - policy-impact-analysis
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/05-物流与供应链/Imperial College London-CIVE70016+CIVE70118-Transport Demand and Economics - Discrete Choice Models
tags:
  - course/CIVE70016
  - discipline/traffic-engineering
  - major/transport-modelling-data-analysis
  - school/imperial-college-london
---

# Imperial College London CIVE70016 Transport Demand and Economics


## 00-课程总览

### 课程归属

- 学校：[[Imperial College London]]
- 专业方向：[[交通工程]] / [[交通建模与数据分析]]
- 相关方向：[[物流与供应链]]（源文件夹中包含 DCM/Biogeme 物流系统材料）
- 课程代码：[[CIVE70016]]
- 课程主题：[[Discrete Choice Models]]、[[Biogeme]]、[[Binary Logit]]、[[Multinomial Logit]]、[[Transport Policy Impact Analysis]]
- 教师：Dr Jacek Pawlak
- 评估：Coursework 1，individual report 5-7 pages，占最终成绩 30%，同时含 group presentation。

### 课程定位

该课程以 discrete choice modelling (DCM) 为核心，把出行调查数据、效用函数设定、Biogeme 估计和政策干预评估连成完整工作流。材料中出现 binary logit、multinomial logit、Biogeme notebook、Dataset 1、模型 pickle/iter 输出和政策 impact analysis brief。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/05-物流与供应链/Imperial College London-CIVE70016+CIVE70118-Transport Demand and Economics - Discrete Choice Models`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| Coursework brief | Application of Discrete Choice Models in Policy Impact Analysis | 定义政策题、建模任务、报告要求 |
| 数据与代码 | Dataset1.csv、data.csv、Biogeme notebooks、pickle/iter 输出 | 复现 binary/multinomial logit 估计 |
| 软件说明 | A short introduction to Biogeme、Introduce to Biogeme.ipynb | 学习 Biogeme 数据库、Beta 参数、模型估计 |
| 参考资料 | Disaggregate Models、Modal split | 回接随机效用理论和 mode choice |

## 01-DCM政策评估工作流

Coursework 要求从政策问题出发，估计合适的 travel demand model，再测试 interventions 对概率和 market shares 的影响。完整链条是：

1. Define the challenge：政策目标、动机、stakeholders；
2. Develop conceptual approach：候选干预是否现实、是否可用数据建模；
3. Design DCM：alternatives、variables、utility specification；
4. Estimate specifications：比较模型、检验 nesting 是否需要；
5. Apply scenarios：计算 probabilities / market shares 的变化；
6. Recommend：说明有效性、限制和进一步数据需求。

## 02-Utility Specification

基本效用表达：

$$
U_{ni}=ASC_i+\beta_T T_{ni}+\beta_C C_{ni}+\beta_X X_{ni}+\varepsilon_{ni}
$$

其中 $ASC_i$ 是 alternative specific constant，$T$ 是时间，$C$ 是费用，$X$ 是环境、walkability、bikeability、frequency、access time 等政策变量。

在 Biogeme 中通常用 `Beta()` 定义参数，用 `Database()` 读取样本，用 `models.loglogit()` 或相关函数定义 log likelihood。

## 03-Binary Logit and Multinomial Logit

Binary logit 概率：

$$
P_{n1}=\frac{\exp(V_{n1})}{\exp(V_{n1})+\exp(V_{n2})}
$$

Multinomial logit 概率：

$$
P_{ni}=\frac{\exp(V_{ni})}{\sum_{j\in C_n}\exp(V_{nj})}
$$

Notebook 中的常见步骤包括：读取 Dataset、构造 total car cost、筛选 alternatives、转换为 Biogeme database、定义 Beta 参数、估计 base model / binary logit / multinomial logit。

## 04-Policy Intervention Scenarios

Brief 给了多类政策题，例如：提升 walkability、改善 public transport frequency 或 fare、提升 cycling infrastructure、micromobility access to public transport。建模时应把 intervention 转成效用变量变化，例如：

- reduce walking travel time；
- increase walkability index；
- reduce waiting time；
- reduce fare；
- reduce cycling travel time；
- reduce access time 或 access cost。

政策结果不应只报告“概率上升”，还要按 age、income、gender、car ownership 等群体异质性解释分布影响。

## 20-Coursework案例库

推荐报告结构：

1. Policy challenge and intervention design；
2. Dataset and descriptive checks；
3. Utility specification and model estimation；
4. Model comparison and behavioural interpretation；
5. Scenario simulation and market share impacts；
6. Equity/segment analysis；
7. Limitations and recommendation。

常见扣分点：变量符号解释不清、把相关性当因果、只贴 Biogeme 输出不解释、intervention 无法由数据变量表达、没有说明样本偏差和 IIA 限制。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 模型设定 | mode choice policy | alternatives、ASC、time/cost variables、segment interactions |
| Biogeme估计 | dataset and notebook output | 参数符号、t-stat、log likelihood、rho-square |
| 情景模拟 | fare/frequency/walkability changes | utility change -> probability change -> market share |
| 模型限制 | MNL vs nested | IIA、omitted variables、sample bias、policy realism |

## 40-复习路线

先掌握随机效用和 MNL，再练 Biogeme 基本语法，最后用一套固定模板把政策干预转换为效用变量变化并解释 market share。
