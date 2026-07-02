---
type: course
course: ETH Zurich UNKNOWN Numerical Methods for EE
course_title: Numerical Methods for EE
course_code: UNKNOWN
school: ETH Zurich
school_link: "[[ETH Zurich]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数值方法与仿真
major_code: 09-01
major_link: "[[数值方法与仿真]]"
knowledge_cluster:
  - numerical-methods
  - differential-equations
  - simulation
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/ETH Zurich-UNKNOWN-Numerical Methods for EE
tags:
  - course/UNKNOWN
  - school/eth-zurich
  - discipline/mathematical-modelling
  - major/numerical-methods
  - topic/splitting-methods
---

# ETH Zurich UNKNOWN Numerical Methods for EE

## 00-课程总览

### 课程归属

- 学校：[[ETH Zurich]]
- 学科库：[[数学建模与优化]]
- 专业方向：[[数值方法与仿真]]
- 课程代码：[[UNKNOWN]]
- 关联知识点：[[Splitting Methods]]、[[Lie-Trotter Splitting]]、[[Strang Splitting]]、[[Differential Equations]]、[[Symplectic Integration]]、[[Numerical Simulation]]

### 课程定位

这门资料包围绕电气工程与动力系统中的 numerical methods 展开，核心是 4.5 Splitting-Verfahren / splitting methods：把复杂 ODE/PDE 的右端拆成若干可单独求解的子流，再按一定顺序组合成整体近似。材料包含辅导讲义、NumMeth Script、脑图、npde-notes，以及 Jupyter notebooks。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/ETH Zurich-UNKNOWN-Numerical Methods for EE`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 0 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 1640 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 0 | 作业、数据、项目产出与练习 |
| 试题与评估 | 0 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 1 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 5 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 1 | 暂时无法完全确认角色的资料 |

## 01-Splitting 的建模直觉

一个复杂系统常可写成 $y'=f(y)=f_a(y)+f_b(y)$。如果整体 $f$ 难解，但 $f_a$ 与 $f_b$ 的 flow 可以解析或高效数值求解，就可以先分别推进子系统再组合。工程上这对应把刚性线性项、非线性反应项、机械/电气子过程拆开处理。

## 02-Lie-Trotter 与 Strang

Lie-Trotter 是一阶组合，思路是一步 $a$ 后一步 $b$；Strang 是二阶对称组合，半步 $a$、一步 $b$、半步 $a$。Jupyter notebook 用 log-log convergence plot 对比误差阶，Lie-Trotter 斜率约为 1，Strang 约为 2。

## 03-结构保持与 Verlet

Newton 方程可拆成位置更新与速度更新，Strang 型组合会导出 Störmer-Verlet / Verlet 方法。对 Hamiltonian 系统，symplectic splitting 的价值不是短期误差最小，而是长期能量漂移较小，适合摆、轨道、分子动力学等长期仿真。

## 10-核心公式与方法

### Lie-Trotter Splitting

$$
\Psi_h=\Phi^b_h\circ\Phi^a_h
$$

先沿 $f_a$ 的 flow 推进一步，再沿 $f_b$ 的 flow 推进一步；全局误差通常是一阶。

### Strang Splitting

$$
\Psi_h=\Phi^a_{h/2}\circ\Phi^b_h\circ\Phi^a_{h/2}
$$

对称半步结构抵消部分低阶误差，因此通常达到二阶精度。

## 20-Coursework案例库

代码练习以 notebook 为主：实现 evolution operators、计算不同步长下的终值误差、在双对数图中验证 $O(h)$ 与 $O(h^2)$ 收敛，并解释子问题不能精确求解时 Euler/midpoint 子方法如何影响整体精度。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 概念解释 | 解释为什么要把 ODE/PDE 分裂为多个 flow | 说明可解性、刚性处理和工程效率 |
| 方法比较 | 比较 Lie-Trotter 与 Strang 的推进顺序和误差阶 | 记住一阶/二阶、对称性、log-log 斜率 |
| 应用推导 | 从 Newton 方程推导 Verlet 型更新 | 区分位置半步、速度整步和能量守恒意义 |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
