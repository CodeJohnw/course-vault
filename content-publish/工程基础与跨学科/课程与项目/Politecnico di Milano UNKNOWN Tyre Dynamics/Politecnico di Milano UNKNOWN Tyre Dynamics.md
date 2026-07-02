---
type: course
course: Politecnico di Milano UNKNOWN Tyre Dynamics
course_title: Tyre Dynamics
course_code: UNKNOWN
school: Politecnico di Milano
school_link: "[[Politecnico di Milano]]"
discipline: 工程基础与跨学科
discipline_code: 00-工程基础与跨学科
major: 车辆动力学
major_code: 00-03
major_link: "[[车辆动力学]]"
knowledge_cluster:
  - vehicle-dynamics
  - tyre-road-contact
  - semiempirical-modelling
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/Politecnico di Milano-UNKNOWN-Tyre Dynamics
tags:
  - course/UNKNOWN
  - school/politecnico-di-milano
  - discipline/engineering-foundations
  - major/vehicle-dynamics
  - topic/tyre-dynamics
---

# Politecnico di Milano UNKNOWN Tyre Dynamics

## 00-课程总览

### 课程归属

- 学校：[[Politecnico di Milano]]
- 学科库：[[工程基础与跨学科]]
- 专业方向：[[车辆动力学]]
- 课程代码：[[UNKNOWN]]
- 关联知识点：[[Tyre Dynamics]]、[[Slip Angle]]、[[Longitudinal Slip]]、[[Magic Formula Tyre Model]]、[[Vehicle Dynamics]]、[[Combined Slip]]

### 课程定位

这组 Politecnico di Milano 资料来自 Vehicle Dynamics and Control 中的 tyre-road contact forces 与 MF Tire model。核心是轮胎作为车辆与路面的接触界面如何产生纵向力、侧向力、自回正力矩，以及如何用 Pacejka Magic Formula 等 semi-empirical model 将运动学条件映射到轮胎力/力矩。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/Politecnico di Milano-UNKNOWN-Tyre Dynamics`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 0 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 8 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 0 | 作业、数据、项目产出与练习 |
| 试题与评估 | 0 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 0 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 0 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 0 | 暂时无法完全确认角色的资料 |

## 01-轮胎-路面接触

轮胎不是刚体接触点，而是有 footprint、tread deformation、adhesion/sliding transition 的柔性结构。纵向 slip 产生 $F_x$，侧偏角 slip angle 产生 $F_y$，vertical load、camber、inflation pressure 和 transient behaviour 都会改变力学响应。

## 02-Slip Angle 与 Lateral Force

slip angle 是 wheel rolling plane 与 wheel path tangent 的夹角。轮胎胎面进入接地区后横向剪切逐步积累，超过摩擦极限后局部滑移，因此侧向力-侧偏角曲线通常先近似线性，随后饱和。

## 03-MF Tire / Magic Formula

MF Tire 是半经验 similarity method：把轮胎看作 black box，用实验数据拟合 algebraic equations，输出 pure slip 与 combined slip 下的力和力矩。优势是计算快、可靠性高，适合 vehicle dynamics simulation；代价是物理解释弱于复杂物理模型。

## 10-核心公式与方法

### Slip Angle

$$
\alpha=-\tan^{-1}\left(\frac{v_y}{v_x}\right)
$$

$v_x$ 与 $v_y$ 是轮心速度在 wheel reference frame 下的纵向/横向分量。

### Longitudinal Slip

$$
\kappa=\frac{R\omega-v_x}{\max(R\omega, v_x)}
$$

表达轮胎圆周速度与车辆纵向速度的相对差，具体符号约定需按课程定义。

### Magic Formula skeleton

$$
y=D\sin\left(C\arctan(Bx-E(Bx-\arctan Bx))\right)
$$

$B,C,D,E$ 分别控制 stiffness、shape、peak 与 curvature，是 Pacejka 型拟合的常见骨架。

## 20-Coursework案例库

适合整理成车辆动力学案例：给定 $v_x,v_y,F_z,\kappa,\alpha$，解释 tyre force generation；对比 empirical、similarity、simple physical、complex physical models；说明为什么 MF Tire 在仿真中常用。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 概念题 | 解释 slip angle 为什么会产生 lateral force | footprint 剪切、adhesion/sliding、饱和 |
| 模型题 | 比较 Magic Formula 与物理轮胎模型 | 速度、实验数据需求、可解释性、仿真用途 |
| 综合题 | 讨论 vertical load/camber/pressure 对轮胎力的影响 | 不要只背方向，要联系接触面积和摩擦极限 |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
