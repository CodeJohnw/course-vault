---
type: course
course: Chang'an University UNKNOWN Operations Research and Transportation
course_title: Operations Research and Transportation
course_code: UNKNOWN
school: Chang'an University
school_link: "[[Chang'an University]]"
discipline: 能源管理与环境
discipline_code: 10-能源管理与环境
major: 能源管理与环境
major_code: 10-能源管理与环境
major_link: "[[能源管理与环境]]"
knowledge_cluster:
  - operations-research
  - linear-programming
  - duality-sensitivity
  - transportation-optimisation
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/Chang'an University-UNKNOWN-Operations Research and Transportation
tags:
  - course/UNKNOWN
  - school/chang-an-university
  - discipline/energy-management-environment
  - major/energy-management-environment
---

# Chang'an University UNKNOWN Operations Research and Transportation

## 00-课程总览

### 课程归属

- 学校：[[Chang'an University]]
- 专业方向：[[能源管理与环境]] / [[数学建模与优化]]
- 课程代码：[[UNKNOWN]]
- 课程主题：[[Operations Research]]、[[Linear Programming]]、[[Simplex Method]]、[[Duality Theory]]、[[Sensitivity Analysis]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/Chang'an University-UNKNOWN-Operations Research and Transportation`

### 课程定位

课件首页显示课程为 **Operations Research & Transportation**，由长安大学交通工程学院 CHEN Lin 讲授。虽然它位于能源管理与环境父文件夹，但内容本质上是运筹学/优化方法，可通过 [[Linear Programming]]、[[Duality Theory]] 与数学建模、交通网络、供应链和能源系统优化连接。

### 材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课件 | Chapter 2 Linear Programming、Chapter 3 Duality Theory & Sensitivity Analysis | 建立优化建模和线性规划求解基础 |

## 01-Operations Research 方法流程

Operations Research 是面向复杂系统决策的建模和优化方法。课件给出的流程是：problem definition、model formulation、solution procedure、optimality test、solution control、implementation。

一个标准线性规划模型为：

$$
\max z=\sum_{j=1}^{n} c_jx_j
$$

subject to

$$
\sum_{j=1}^{n} a_{ij}x_j\le b_i,\quad i=1,\dots,m
$$

$$
x_j\ge 0
$$

其中 $x_j$ 是决策变量，$c_j$ 是目标函数系数，$a_{ij}$ 是资源消耗系数，$b_i$ 是资源约束。

## 02-Duality and Sensitivity

[[Duality Theory]] 把原问题的资源约束转化为影子价格解释。对 maximization primal，dual 往往是 minimization problem。影子价格可以用于判断资源增加一单位对目标值的边际影响。

Sensitivity Analysis 关注参数变化后原最优基是否仍然有效，常用于回答：资源容量变化、目标系数变化、约束右端项变化时，最优解和最优值如何变化。

## 20-案例迁移

该课程可以迁移到能源管理中的设备容量配置、供应链调度、交通能源消耗优化，也可以迁移到交通工程中的 network flow、signal timing 和 mode/resource allocation。

