---
type: course
course: University of Pennsylvania ESE5030 Simulation Modeling and Analysis
course_title: Simulation Modeling and Analysis
course_code: ESE5030
school: University of Pennsylvania
school_link: "[[University of Pennsylvania]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 仿真建模与随机过程
major_code: 09-03
major_link: "[[仿真建模与随机过程]]"
knowledge_cluster:
  - simulation-modelling
  - stochastic-processes
  - monte-carlo
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Pennsylvania-ESE5030-Simulation Modeling and Analysis
tags:
  - course/ESE5030
  - school/university-of-pennsylvania
  - discipline/mathematical-modelling
  - major/simulation-modelling
  - topic/monte-carlo
---

# University of Pennsylvania ESE5030 Simulation Modeling and Analysis

## 00-课程总览

### 课程归属

- 学校：[[University of Pennsylvania]]
- 学科库：[[数学建模与优化]]
- 专业方向：[[仿真建模与随机过程]]
- 课程代码：[[ESE5030]]
- 关联知识点：[[Simulation Modeling]]、[[Poisson Process]]、[[Monte Carlo Simulation]]、[[Exponential Distribution]]、[[Discrete Event Simulation]]、[[Random Variables]]

### 课程定位

ESE5030 资料集中在 stochastic simulation：Poisson process、随机变量分布、Monte Carlo、homework 和 in-class exam。课程材料适合建立“概率分布 - 随机过程 - 仿真估计 - exam probability computation”的复习链条。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Pennsylvania-ESE5030-Simulation Modeling and Analysis`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 0 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 5 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 7 | 作业、数据、项目产出与练习 |
| 试题与评估 | 1 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 0 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 0 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 0 | 暂时无法完全确认角色的资料 |

## 01-Poisson Process

Poisson process 用 counting function $N(t)$ 表示到时间 $t$ 为止的到达数，核心假设是单次到达、stationary increments 和 independent increments。适用于顾客到达、网页点击、故障事件等随机到达过程。

## 02-Monte Carlo 思路

Monte Carlo 通过重复随机抽样估计概率、期望或复杂事件频率。资料中有 coin overlap simulator，可作为从解析概率转向仿真估计的案例：定义随机输入、重复试验、统计指标、置信/误差解释。

## 03-考试结构

In-class exam 要求从 6 题中选四题，题目给出 Uniform、Geometric、Exponential、Binomial、Discrete Uniform、Pascal 等分布公式，重点考概率计算、期望方差、独立随机变量组合和到达/成熟时间问题。

## 10-核心公式与方法

### Poisson count

$$
P(N(t)=n)=e^{-\lambda t}\frac{(\lambda t)^n}{n!}
$$

$\lambda$ 是单位时间平均到达率，$t$ 是观察长度。

### Exponential distribution

$$
F_X(x)=1-e^{-\lambda x},\quad x\ge 0
$$

Poisson process 的 interarrival time 服从 exponential distribution。

### Monte Carlo estimator

$$
\hat{\theta}=\frac{1}{R}\sum_{r=1}^{R} g(X_r)
$$

$R$ 是重复仿真次数，$g(X_r)$ 是第 $r$ 次仿真的统计量或指标函数。

## 20-Coursework案例库

作业资料包含 homework solutions、Monte Carlo coin overlap simulator 和 Excel 模型。解题应写清随机变量定义、分布选择、独立性假设、目标概率/期望，并说明仿真估计与解析计算的关系。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 分布计算 | 由 exponential/geometric/binomial 求概率、期望、方差 | 先识别随机变量和参数，再代公式 |
| Poisson过程 | 给定 arrival rate 求区间到达数或等待时间 | 区分 count distribution 与 interarrival distribution |
| Monte Carlo | 设计仿真估计某事件概率 | 随机输入、重复次数、估计量、误差解释 |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
