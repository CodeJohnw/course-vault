---
type: course
course: University of Edinburgh INFR11218 Algorithmic Game Theory and its Applications
course_title: Algorithmic Game Theory and its Applications
course_code: INFR11218
school: University of Edinburgh
school_link: "[[University of Edinburgh]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 算法博弈论与优化
major_code: 09-02
major_link: "[[算法博弈论与优化]]"
knowledge_cluster:
  - algorithmic-game-theory
  - complexity
  - mechanism-design
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Edinburgh-INFR11218-Algorithmic Game Theory and its Applications
tags:
  - course/INFR11218
  - school/university-of-edinburgh
  - discipline/mathematical-modelling
  - major/algorithmic-game-theory
  - topic/game-theory
---

# University of Edinburgh INFR11218 Algorithmic Game Theory and its Applications

## 00-课程总览

### 课程归属

- 学校：[[University of Edinburgh]]
- 学科库：[[数学建模与优化]]
- 专业方向：[[算法博弈论与优化]]
- 课程代码：[[INFR11218]]
- 关联知识点：[[Algorithmic Game Theory]]、[[Nash Equilibrium]]、[[Congestion Games]]、[[Braess Paradox]]、[[Mechanism Design]]、[[Computational Complexity]]、[[Linear Programming]]

### 课程定位

INFR11218 关注 game theory 的算法视角：如何建模多主体战略互动，均衡是否存在，均衡或机制能否高效计算，以及机制设计在资源分配、拍卖、路由和拥塞网络中的应用。课程明确包含两次 written coursework，各占 10%，期末考试占 80%。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Edinburgh-INFR11218-Algorithmic Game Theory and its Applications`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 0 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 17 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 21 | 作业、数据、项目产出与练习 |
| 试题与评估 | 26 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 1 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 0 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 0 | 暂时无法完全确认角色的资料 |

## 01-课程主线

前半部分建立 normal-form / extensive-form games、dominant strategy、best response、mixed strategy、Nash equilibrium 等基础；中段引入 linear programming、duality 和算法复杂度；后半部分进入 congestion games、inefficiency of equilibria、mechanism design、VCG、auction 与 Bayesian games。

## 02-拥塞博弈与交通类连接

Congestion game 将资源视为 edges/resources，玩家策略是资源集合或路径，个人成本由所使用资源的负载决定。Braess' Paradox 展示新增高速连接可能让 Nash equilibrium 下所有人更差，这一点可与交通工程中的 user equilibrium / system optimum 连接。

## 03-复杂度视角

材料中特别整理了 Lecture 1-19 的 complexity 线索：support enumeration 和 Lemke-Howson 可出现指数复杂度，PNE/MNE 计算与 PLS、PPAD 等复杂度类相关；LP 可多项式求解，但 ILP、组合拍卖福利最大化、某些均衡计算可能 NP-hard 或更难。

## 10-核心公式与方法

### 拥塞博弈个人成本

$$
\operatorname{cost}_i(s)=\sum_{r\in s_i} c_r(n_r(s))
$$

$s_i$ 是玩家 $i$ 使用的资源集合，$n_r(s)$ 是资源 $r$ 在策略组合 $s$ 下的使用人数。

### Price of Anarchy

$$
\operatorname{PoA}=\frac{\max_{s\in NE} C(s)}{C(s^*)}
$$

衡量最坏 Nash equilibrium 的社会成本相对最优社会成本的损失。

## 20-Coursework案例库

Coursework 与 tutorial 解答集中在 equilibrium calculation、复杂度判断、congestion game、mechanism / auction 证明题。整理时应按“定义 - 形式化模型 - 均衡/最优性 - 复杂度 - 反例”写答案，而不是只给结论。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 均衡计算 | 给定 payoff matrix 求 best response / mixed Nash | 列 indifference 条件，检查 support 与概率合法性 |
| 拥塞博弈 | 判断路径选择是否为 Nash equilibrium | 计算每条路径负载成本，说明单个玩家是否有 profitable deviation |
| 复杂度论述 | 说明为什么存在性不等于可计算性 | 联系 PPAD/PLS/NP-hard、输入表示和算法收敛 |
| 机制设计 | 分析 VCG 或 auction 是否 truthful / efficient | 区分社会福利最大化、支付规则和计算瓶颈 |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
