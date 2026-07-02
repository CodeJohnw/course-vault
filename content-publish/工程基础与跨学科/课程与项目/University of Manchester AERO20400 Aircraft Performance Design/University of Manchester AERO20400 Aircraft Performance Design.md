---
type: course
course: University of Manchester AERO20400 Aircraft Performance Design
course_title: Aircraft Performance Design
course_code: AERO20400
school: University of Manchester
school_link: "[[University of Manchester]]"
discipline: 工程基础与跨学科
discipline_code: 00-工程基础与跨学科
major: 航空工程与性能设计
major_code: 00-01
major_link: "[[航空工程与性能设计]]"
knowledge_cluster:
  - aircraft-performance
  - engineering-design
  - mission-analysis
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Manchester-AERO20400-Aircraft Performance Design
tags:
  - course/AERO20400
  - school/university-of-manchester
  - discipline/engineering-foundations
  - major/aerospace-engineering
  - topic/aircraft-design
---

# University of Manchester AERO20400 Aircraft Performance Design

## 00-课程总览

### 课程归属

- 学校：[[University of Manchester]]
- 学科库：[[工程基础与跨学科]]
- 专业方向：[[航空工程与性能设计]]
- 课程代码：[[AERO20400]]
- 关联知识点：[[Aircraft Performance]]、[[Aircraft Configuration Design]]、[[Payload Range Diagram]]、[[Constraint Analysis]]、[[Weight Estimation]]、[[Engine Performance]]

### 课程定位

AERO20400 是飞机性能与概念设计课程，材料覆盖 atmosphere model、flight instruments、lift/drag coefficient、trim、engine powerplants、engine performance、mission segments、weight estimation、constraints analysis、payload-range 和 aircraft configuration design。CW4 是 aircraft configuration design presentation，占 10%。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/待整理/University of Manchester-AERO20400-Aircraft Performance Design`

### 课程材料地图

| 类别 | 文件数 | 学习用途 |
| --- | ---: | --- |
| 课程说明与评估 | 10 | 课程要求、项目 brief、rubric、反馈 |
| 课件 | 56 | 主体知识点、公式、课堂讲义 |
| 练习与数据 | 8 | 作业、数据、项目产出与练习 |
| 试题与评估 | 3 | 考试题型、tutorial、solution、past paper |
| 阅读论文与参考 | 0 | 参考讲义、外部阅读、补充理论 |
| 代码与软件 | 10 | MATLAB / notebook / spreadsheet / software artefacts |
| 待确认 | 0 | 暂时无法完全确认角色的资料 |

## 01-性能计算链条

课程从飞行环境和气动基础出发，把 lift/drag、engine thrust/power available、mission profile、weight estimation 串成 aircraft sizing。关键不是单个公式，而是把市场航线、任务剖面、法规限制和局部机场约束转化为 wing area、thrust、weight 与 payload-range 图。

## 02-推进与发动机性能

发动机部分区分 thrust available、power available、Mach number、density ratio 与高度影响。资料中包含 MATLAB solution scripts 和 mission data，可用于计算各 mission segment 的 fuel/weight 变化。

## 03-设计表达

CW4 要求用 10 分钟组内汇报解释 aircraft sizing 与 configuration decisions，包括 route/market background、mission table、constraints analysis、payload-range chart、wing/fuselage layout、revenue potential 与 CAD rendering。

## 10-核心公式与方法

### Lift

$$
L=\frac{1}{2}\rho V^2 S C_L
$$

$\rho$ 是空气密度，$V$ 是速度，$S$ 是翼面积，$C_L$ 是升力系数。

### Drag

$$
D=\frac{1}{2}\rho V^2 S C_D
$$

用于阻力估算、所需推力和约束分析。

### Thrust-to-weight 约束

$$
\frac{T}{W}=f\left(\frac{W}{S},\text{mission},\text{regulation}\right)
$$

概念设计中常通过 wing loading 与 thrust-to-weight trade-off 选择设计点。

## 20-Coursework案例库

CW4 报告/汇报框架：1. 市场与航线机会；2. mission table 与假设；3. initial weight and sizing；4. constraints analysis；5. payload-range chart；6. wing/fuselage/engine configuration；7. revenue-generating potential；8. 风险与局限。评分重点是设计选择是否由工程分析支撑，而不是图表堆砌。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 性能计算 | 给定高度、速度、机翼面积和系数计算 lift/drag | 单位、空气密度、动压和系数意义 |
| 发动机/任务 | 计算 thrust/power available 随高度或 Mach 的变化 | 区分 jet thrust 与 turboprop power |
| 概念设计 | 解释 payload-range 或 constraints chart | 把图上的设计点转化为 configuration decision |

## 40-复习路线

1. 先按课程总览确认材料结构和考核/项目目标。
2. 把上面的核心公式手写一遍，并给每个符号写中文解释。
3. 用课程案例或作业复现一个完整 calculation / argument chain。
4. 最后用考试题型库检查自己是否能从题目识别模型、公式和论证结构。
