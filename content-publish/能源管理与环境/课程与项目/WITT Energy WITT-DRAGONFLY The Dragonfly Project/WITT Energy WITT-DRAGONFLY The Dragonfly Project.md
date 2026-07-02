---
type: project
course: WITT Energy WITT-DRAGONFLY The Dragonfly Project
course_title: The Dragonfly Project
course_code: WITT-DRAGONFLY
school: WITT Energy
school_link: "[[WITT Energy]]"
discipline: 能源管理与环境
discipline_code: 10-能源管理与环境
major: 能源管理与环境
major_code: 10-能源管理与环境
major_link: "[[能源管理与环境]]"
knowledge_cluster:
  - wave-energy-converter
  - renewable-energy-project
  - dynamic-modelling
  - parameter-optimisation
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/WITT Energy-WITT-DRAGONFLY-The Dragonfly Project
tags:
  - project/WITT-DRAGONFLY
  - school/witt-energy
  - discipline/energy-management-environment
  - major/energy-management-environment
---

# WITT Energy WITT-DRAGONFLY The Dragonfly Project

## 00-项目总览

### 项目归属

- 来源：[[WITT Energy]]
- 专业方向：[[能源管理与环境]] / [[可再生能源]]
- 项目代码：[[WITT-DRAGONFLY]]
- 项目主题：[[Wave Energy Converter]]、[[Renewable Energy]]、[[Dynamic Modelling]]、[[Parameter Optimisation]]、[[Energy Harvesting]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/WITT Energy-WITT-DRAGONFLY-The Dragonfly Project`

### 项目定位

WITT Dragonfly 是一个可再生能源/机械能量收集项目，材料描述了一种通过 tacking and heeling motion、bidirectional transmission 和 rectified single output 产生清洁电力的装置。项目任务是理解动态机制、建立简化数学模型、匹配观测、估算能量生成潜力，并做参数研究和几何优化。

### 材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 项目说明 | assignment brief、MDM3_WITT PDFs/templates | 明确任务、背景和输出形式 |
| 数据与素材 | 产品图片、视频、会议记录、输入整理、mindmap | 复盘结构、运动机制和变量 |
| 参考 | submerged cylinder wave energy converter paper | 对比 wave energy converter 建模思路 |
| 代码 | WITT_team.ipynb、blasuis_eq.ipynb | 复现动力学或流体近似计算 |

## 01-机制抽象

项目描述的核心机制是：装置在 airflow / wave-like excitation 下发生 tacking 和 heeling，两种正交方向的往复/摆动输入通过 WITT 传动结构整流为单向输出旋转。

可用简化动力学模型表示为：

$$
I\ddot{	heta}+c\dot{	heta}+k	heta=	au_{wind}(t)-	au_{load}
$$

其中 $I$ 是等效转动惯量，$c$ 是阻尼，$k$ 是恢复刚度，$	au_{wind}$ 是风/流体激励力矩，$	au_{load}$ 是负载力矩。

## 02-参数研究

项目 brief 明确要求研究的变量包括 sail shape / dimension、rudder shape / dimension、rudder distance from centre、counterbalance、minimum wind speed、power output 和 scalability。

输出功率可用：

$$
P=	au\omega
$$

其中 $	au$ 是输出力矩，$\omega$ 是输出角速度。参数优化的目标不是单纯最大功率，还要兼顾启动风速、结构稳定性、疲劳、可制造性和尺度放大。

## 20-项目报告框架

| 部分 | 建议内容 |
| --- | --- |
| Problem framing | WITT device、Dragonfly mechanism、energy harvesting objective |
| Mechanism model | degrees of freedom、input motion、transmission rectification |
| Mathematical model | simplified equations、assumptions、parameters |
| Simulation | notebook model、matching observations、sensitivity study |
| Optimisation | sail/rudder geometry、counterbalance、wind speed range |
| Limitations | fluid-structure coupling simplification、data scarcity、scalability uncertainty |

## 30-迁移价值

该项目连接 [[Renewable Energy]]、[[Fluid Mechanics]]、[[Dynamic Modelling]] 和 [[Parameter Optimisation]]，适合未来作为能源项目案例库，而不是普通课程笔记。

