---
type: course
course: UCL COMP0083 Introductory Convex Optimisation
course_title: Introductory Convex Optimisation
course_code: COMP0083
school: UCL
school_link: "[[UCL]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数学建模与优化
major_code: 09-数学建模与优化
major_link: "[[数学建模与优化]]"
level: Undergraduate / MSc support
assessment: coursework / modelling assignments
knowledge_cluster:
  - convex-optimisation
  - duality
  - gradient-methods
  - constrained-optimization
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/UCL-COMP0083-Introductory Convex Optimisation
tags:
  - course/COMP0083
  - school/ucl
  - discipline/mathematical-modelling-optimization
  - major/mathematical-modelling-optimization
  - topic/convex-optimisation
---

# UCL COMP0083 Introductory Convex Optimisation


## 00-课程总览

- 学校：[[UCL]]
- 专业方向：[[数学建模与优化]]
- 课程代码：[[COMP0083]]
- 课程主题：[[Convex Optimisation]]、[[Duality]]、[[Gradient Descent]]、[[KKT Conditions]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/UCL-COMP0083-Introductory Convex Optimisation`

该课程资产包含 Introductory Convex Optimisation syllabus 和 ICO lectures 1-8。它适合做机器学习、运筹优化、统计估计和工程优化的基础模块。

## 01-核心框架

标准凸优化问题：

$$
\min_x f_0(x) \quad 	ext{s.t.}\quad f_i(x)\le 0,\; h_j(x)=0
$$

其中 $f_0$ 和 $f_i$ 是凸函数，$h_j$ 通常是仿射等式约束。凸性带来的关键好处是局部最优即全局最优。

## 02-复习重点

- convex set / convex function 的定义和判别；
- first-order / second-order condition；
- Lagrangian、dual function、weak/strong duality；
- KKT conditions；
- gradient descent、Newton method、projected methods；
- 正则化和机器学习中的优化解释。

## 30-题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 证明凸性 | norm、quadratic、log-sum-exp | Jensen / Hessian |
| 构造对偶 | constrained minimisation | Lagrangian 与 dual feasibility |
| KKT 求解 | inequality constraints | stationarity、complementary slackness |
| 算法收敛 | gradient method | step size、Lipschitz gradient |
