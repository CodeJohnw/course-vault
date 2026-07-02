---
type: case
case: RSEI Signalling System Time-Distance Graph Case
case_code: RSEI
school: Unknown / Reference Case
school_link: "[[Unknown / Reference Case]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通安全
major_code: 03-交通安全
major_link: "[[交通安全]]"
knowledge_cluster:
  - railway-operations
  - time-distance-graph
  - signalling-system
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Signalling
tags:
  - case/RSEI
  - discipline/traffic-engineering
  - major/traffic-safety
---

# RSEI Signalling System Time-Distance Graph Case

## 00-案例定位

- 资产类型：铁路运营/信号系统案例，不是完整课程。
- 专业方向：[[交通工程]] / [[交通安全]]
- 关联知识点：[[Railway Operations]]、[[Railway Signalling]]、[[Time-Distance Graph]]、[[Capacity and Headway]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Signalling`

## 01-材料内容

该案例包含一个 Python notebook：`Q2_TimeDist_Graph.ipynb`。代码用 `matplotlib` 绘制 Sheffield、Duffield、Derby、Wirksworth 等位置之间的 time-distance graph，包含 intercity、regional、freight 和 branch service 的速度、停站、路径和图例设定。

## 02-核心建模信息

| 元素 | notebook 中的设定 | 含义 |
| --- | --- | --- |
| 距离 | Sheffield、Duffield Main、Duffield Branch、Little Eaton、Derby、Wirksworth | 用线性里程表示站点和支线位置 |
| 速度 | Intercity 180 km/h、Regional 145 km/h、Freight 90 km/h、Branch 75 km/h | 不同列车类型的运行斜率 |
| 停站 | dwell = 0.75 min | 45 秒停站以水平线表示 |
| 图形 | 时间为横轴、距离为纵轴 | 线的交叉/接近可用于检查冲突、追踪间隔和容量约束 |

基本运行时间公式：

$$
t = \frac{d}{v}\times 60
$$

其中 $d$ 为距离（km），$v$ 为速度（km/h），$t$ 为运行时间（min）。

## 03-可复用学习价值

- 可作为 [[Railway Operations]] 中 timetable visualisation 的案例。
- 可连接 [[Railway Signalling]] 中 headway、conflict checking、route occupation 的概念。
- 可作为 Python 绘图模板，用于展示不同服务类型在同一走廊上的运行路径。
- 如果以后整理铁路信号或运营课程，可把这个案例挂到具体课程下，而不是拆成零散代码卡。

## 50-铁路安全与控制系统资料包补充

本次新增来源来自 `04-铁路安全与控制系统` 下的 University of Birmingham RSEI Railway Signalling 文件夹。该资料包补充 written assignment brief、headway Cal.xlsx、New Adlestrop Railway Atlas 和 braking-signals 参考材料；通用课程化整理见 [[University of Birmingham RSEI-SIG Railway Signalling]]。
