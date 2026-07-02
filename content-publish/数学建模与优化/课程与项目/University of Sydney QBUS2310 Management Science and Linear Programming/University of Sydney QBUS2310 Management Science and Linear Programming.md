---
type: course
course: University of Sydney QBUS2310 Management Science and Linear Programming
course_title: Management Science and Linear Programming
course_code: QBUS2310
school: University of Sydney
school_link: "[[University of Sydney]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数学建模与优化
major_code: 09-数学建模与优化
major_link: "[[数学建模与优化]]"
level: Undergraduate / MSc support
assessment: coursework / modelling assignments
knowledge_cluster:
  - linear-programming
  - integer-programming
  - network-flow
  - duality
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Sydney-QBUS2310-Management Science and Linear Programming
tags:
  - course/QBUS2310
  - school/university-of-sydney
  - discipline/mathematical-modelling-optimization
  - major/mathematical-modelling-optimization
  - topic/linear-programming
---

# University of Sydney QBUS2310 Management Science and Linear Programming


## 00-课程总览

- 学校：[[University of Sydney]]
- 专业方向：[[数学建模与优化]]
- 课程代码：[[QBUS2310]]
- 课程主题：[[Linear Programming]]、[[Integer Programming]]、[[Network Flow]]、[[LP Duality]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Sydney-QBUS2310-Management Science and Linear Programming`

该课程资产是管理科学和线性规划资料包，包含 LP building、modelling、geometry、integer programming、network flow、LP duality，以及 assignment notebook。它的核心价值是把业务/管理问题转化成决策变量、目标函数和约束。

## 01-线性规划模板

标准 LP 形式：

$$
\max \; c^T x \quad 	ext{s.t.}\quad Ax\le b,\; x\ge 0
$$

其中 $x$ 是决策变量，$c$ 是目标收益/成本系数，$A$ 和 $b$ 表示资源、容量、需求或逻辑约束。

## 02-整数规划与网络流

整数规划用于排课、选址、匹配和二元决策。网络流模型把问题表达为 nodes、arcs、capacity、flow conservation 和 cost。资料中的排课最大流和骑士巡逻二分匹配 notebook 是非常好的案例。

## 20-Coursework案例库

- Assignment 1：LP formulation、几何解释、notebook 求解。
- Assignment 2：integer programming、network flow、duality、最大流/匹配模型。
- 报告写法：变量定义必须先于公式，约束要逐条解释业务含义。
