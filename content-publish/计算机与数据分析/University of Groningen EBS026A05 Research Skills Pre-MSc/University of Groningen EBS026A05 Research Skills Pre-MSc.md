---
type: course
course: University of Groningen EBS026A05 Research Skills Pre-MSc
course_title: Research Skills Pre-MSc
course_code: EBS026A05
school: University of Groningen
school_link: "[[University of Groningen]]"
discipline: 计算机与数据分析
discipline_code: 11-计算机与数据分析
major: 计算机与数据分析
major_code: 11-计算机与数据分析
major_link: "[[计算机与数据分析]]"
knowledge_cluster:
  - research-methods
  - data-analysis
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/11-计算机与数据分析/University of Groningen-EBS026A05-Research Skills Pre-MSc
tags:
  - course/EBS026A05
  - school/university-of-groningen
  - discipline/computer-data-analysis
  - major/computer-data-analysis
---

# University of Groningen EBS026A05 Research Skills Pre-MSc

## 00-课程总览

### 课程归属

- 学校：[[University of Groningen]]
- 学科方向：[[计算机与数据分析]] / [[计算机与数据分析]]
- 课程代码：[[EBS026A05]]
- 课程主题：[[Research Question]]、[[Conceptual Model]]、[[Operationalization]]、[[Hypothesis Testing]]、[[Regression Analysis]]、[[Moderation Effect]]、[[Descriptive Statistics]]、[[Empirical Cycle]]、[[Qualitative Research]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/11-计算机与数据分析/University of Groningen-EBS026A05-Research Skills Pre-MSc`

### 课程定位

这门课是 Pre-MSc 阶段的研究方法训练课，目标是帮助学生完成从研究问题到概念模型、从概念模型到假设、再从数据分析到结论写作的完整研究流程。课程材料同时覆盖定性研究、定量研究、文献嵌入、概念分析、操作化、描述性统计和回归分析。

### 课程材料地图

| 类别 | 主要内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | Assignment 1/2 要求、翻译版要求、反馈文档 | 明确 conceptual analysis 和 empirical analysis 两个作业的结构 |
| 课件 | Lecture 1 research questions/conceptual models；Lecture 2 literature embedding；Lecture 4 qualitative research；Lecture 5 data analysis basics | 搭建研究流程和分析方法 |
| 练习与数据 | 2-way linear interactions、group report、数据集说明、Assignment 2 思维导图 | 复盘描述统计、回归、交互效应和报告结构 |

## 01-研究问题与概念模型

[[Research Question]] 是整篇研究的控制中心。Lecture 2 强调 research question 决定研究焦点、文献综述、方法、分析和报告。好的 RQ 不是“某概念如何定义”这种百科式问题，而是围绕一个可研究问题，明确 population、variables、problem 和研究边界。

Assignment 1 要求构建一个 [[Conceptual Model]]，其中包含一个 dependent variable、两个 independent variables / factors、两个 moderators、因素和中心概念之间的 propositions，以及简短的数据收集计划。概念模型不只是图，正文还要解释每条关系背后的 explanatory mechanism，并用 peer-reviewed literature 支撑。

## 02-文献嵌入与理论论证

Lecture 2 的主题是把研究问题嵌入文献。核心逻辑是：先知道已有研究知道什么，再说明还不知道什么，然后证明你的研究问题值得研究。Assignment 1 要求使用 peer-reviewed articles 定义 central concept、factors、moderators，并支撑 explanatory mechanism。

## 03-研究设计与操作化

[[Operationalization]] 是把概念变成可测变量。Assignment 2 明确要求检查 central concept 是否是 interval-level variable，independent variables / moderators 是否是 interval 或 binary variables。

[[Empirical Cycle]] 包括提出研究问题、建立理论预期、设计研究方法、收集与分析数据、总结结论，并根据结果修正理论。

## 04-定量与定性方法

[[Qualitative Research]] 的价值在于深入理解机制和情境，尤其适合探索性问题；定量方法更适合检验变量关系和假设。课程按 track 区分 SPSS/R/STATA/NVivo 等软件路径。

## 05-描述统计、回归与调节效应

Assignment 2 要求对数据集进行 [[Descriptive Statistics]]，报告 mean、median、standard deviation、minimum、maximum 和 number of observations。

均值：

$$
\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_i
$$

样本标准差：

$$
s=\sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i-\bar{x})^2}
$$

基础多元回归：

$$
Y=\beta_0+\beta_1X_1+\beta_2X_2+\epsilon
$$

Study motivation 案例：

$$
StudyMotivation=\beta_0+\beta_1InterestSubj+\beta_2PriorSuccess+\epsilon
$$

[[Moderation Effect]] 交互项模型：

$$
Y=\beta_0+\beta_1X+\beta_2M+\beta_3(X\times M)+\epsilon
$$

[[Hypothesis Testing]] 的核心不是机械地看 p-value，而是把统计结果翻译回理论命题。

## 20-Coursework案例库

| Assignment | 任务结构 | 方法重点 | 输出要求 |
| --- | --- | --- | --- |
| Assignment 1 Conceptual Analysis | 选择 central concept；定义两个 factors 和两个 moderators；提出 propositions；写数据收集计划 | 文献检索、概念定义、概念模型、理论机制 | 2000 words；主文包含 conceptual model；科学写作风格 |
| Assignment 2 Empirical Analysis | 将 A1 命题转为 hypotheses；做描述统计；运行回归和交互效应模型；写结论 | operationalization、descriptive statistics、regression、moderation | 800-1200 words；包含 introduction、hypotheses、testing、conclusion 和软件输出附录 |

## 30-考试题型库

| 题型 | 典型问题 | 复习重点 |
| --- | --- | --- |
| Research question 判断 | 是否是好的 RQ | population、variables、problem、scope |
| Conceptual model 构建 | DV、IV、moderator 如何连接 | 箭头方向、理论机制、变量层级 |
| Regression interpretation | 如何解释 beta/p/R-square | 方向、显著性、解释力、假设结论 |
| Moderation | 如何解释 interaction | 交互项、简单斜率、可视化 |

## 40-复习路线

1. 先画出 Assignment 1 的 conceptual model，确认变量类型。
2. 为每个变量写一句 literature-based definition。
3. 把 propositions 改写成 hypotheses。
4. 做描述统计表，先解释数据范围和样本特征。
5. 运行基础回归，再加入 moderator 和 interaction term。
6. 把统计结果翻译成理论结论，避免只罗列软件输出。
