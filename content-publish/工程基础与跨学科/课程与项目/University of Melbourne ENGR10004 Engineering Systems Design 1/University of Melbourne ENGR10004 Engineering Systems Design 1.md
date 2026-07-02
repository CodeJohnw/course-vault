---
type: course
course: University of Melbourne ENGR10004 Engineering Systems Design 1
course_title: Engineering Systems Design 1
course_code: ENGR10004
school: University of Melbourne
school_link: "[[University of Melbourne]]"
discipline: 工程基础与跨学科
discipline_code: 00-工程基础与跨学科
major: 工程系统设计
major_code: 00-02
major_link: "[[工程系统设计]]"
knowledge_cluster:
  - engineering-systems-design
  - fluid-mechanics
  - project-management
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Melbourne-ENGR10004-Engineering Systems Design 1
tags:
  - course/ENGR10004
  - school/university-of-melbourne
  - discipline/engineering-foundations
  - major/engineering-design
  - topic/fluid-systems
---

# University of Melbourne ENGR10004 Engineering Systems Design 1

## 00-课程总览

### 课程归属

- 学校：[[University of Melbourne]]
- 学科库：[[工程基础与跨学科]]
- 专业方向：[[工程系统设计]]
- 课程代码：[[ENGR10004]]
- 关联知识点：[[Engineering Systems Design]]、[[Pipe Flow]]、[[Engineering Bernoulli Equation]]、[[Pump Design]]、[[Water Distribution Network]]、[[MATLAB]]

### 课程定位

ENGR10004 Engineering Systems Design 1 / Engineering Technology and Society 是项目制工程系统课程。设计项目围绕 water distribution / treatment system，模块包括 impeller and pump design、water treatment and disinfection、inline image monitoring、pipe distribution network，并配套 MATLAB、Fusion、team/project management 和 workshop assessments。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Melbourne-ENGR10004-Engineering Systems Design 1`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 7 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 30 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 8 | 作业、数据、项目产出与练习 |
| 试题与评估 | 0 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 0 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 10 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 1 | 暂时无法完全确认角色的资料 |

## 01-项目系统结构

项目不是单一流体力学题，而是把泵、管网、膜/水处理、监测、制造与团队管理整合成工程系统。材料中的 Project Description 明确列出 system modules、workshops、project deliverables、team management plan、video presentation、data report/reflection 和 final report。

## 02-Pipe Flow

Pipe flow 讲义要求用 MATLAB 实现 if-else 与 loop 来计算 pressure drop。核心流程是由 flow rate 得到 velocity 和 Reynolds number，再根据 laminar/turbulent 选择 friction factor，最后计算压降。

## 03-Pumps 与 EBE

Pumps 部分用 Engineering Bernoulli Equation 把 elevation、pressure、kinetic energy、losses 和 pump work 连成 energy balance；复杂管路通过 pipe losses、fittings K values、pump head 与系统曲线组合分析。

## 10-核心公式与方法

### Reynolds Number

$$
Re=\frac{\rho v D}{\mu}
$$

$\rho$ 为密度，$v$ 为平均流速，$D$ 为管径，$\mu$ 为动力黏度。

### Laminar friction factor

$$
f=\frac{64}{Re}
$$

课程材料以 $Re<2000$ 作为 laminar flow 判断。

### Darcy-Weisbach pressure drop

$$
\Delta P=\frac{\rho f L v^2}{2D}
$$

用于把管长、管径、流速和摩擦因子转化为 pressure drop。

### Engineering Bernoulli Equation

$$
\alpha_1\frac{v_1^2}{2g}+h_1+\frac{p_1}{\rho g}=\alpha_2\frac{v_2^2}{2g}+h_2+\frac{p_2}{\rho g}+h_L-h_P
$$

$h_L$ 表示损失，$h_P$ 表示泵加入的 head；符号方向需按课程约定检查。

## 20-Coursework案例库

案例库应围绕水系统项目：team management plan、workshop tasks、pump/impeller CAD、pipe flow MATLAB、pump scale-up、data report、final report。推荐报告按 Context - Requirements - Module design - Calculation - Prototype/testing - Risk - Cost/sustainability - Reflection 组织。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| MATLAB计算 | 用数组和循环计算不同流量下压降 | 单位换算、if-else 选择 friction factor、图表标签 |
| 管流计算 | 给定 Q、D、L、roughness 计算 Re、f、Delta P | laminar/turbulent 判别和公式选择 |
| 系统设计 | 解释泵、管网、水处理和监测之间的接口 | 从模块功能转向系统级 trade-off |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
