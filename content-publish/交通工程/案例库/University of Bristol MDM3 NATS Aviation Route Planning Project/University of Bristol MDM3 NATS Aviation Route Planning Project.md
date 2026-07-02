---
type: project
course: University of Bristol MDM3 NATS Aviation Route Planning Project
course_title: NATS Aviation Route Planning Project
course_code: MDM3
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通规划
major_code: 01-交通规划
major_link: "[[交通规划]]"
knowledge_cluster:
  - aviation-route-planning
  - nats
  - flight-trajectory-optimisation
  - dijkstra
  - opensky-era5
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/01-交通规划/University of Bristol-MDM3-NATS Aviation Route Planning Project
tags:
  - project/MDM3
  - school/university-of-bristol
  - discipline/traffic-engineering
  - major/traffic-planning
  - aviation/route-planning
---

# University of Bristol MDM3 NATS Aviation Route Planning Project

## 00-项目总览

### 项目归属

- 学校：[[University of Bristol]]
- 专业方向：[[交通工程]] / [[交通规划]]
- 项目代码：[[MDM3]]
- 主题：[[Air Route Planning]]、[[Flight Trajectory Optimisation]]、[[Dijkstra Algorithm]]、[[OpenSky Data]]、[[ERA5 Weather Data]]、[[Agent-Based Model]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/01-交通规划/University of Bristol-MDM3-NATS Aviation Route Planning Project`

### 项目定位

该项目围绕 North Atlantic Tracks / NATS 的航空路径规划和飞机分配展开，材料包含项目报告、evaluation framework、teamwork 文件、路线截图、OpenSky 航迹 CSV、NAT waypoint JSON、ERA5/GRIB weather data、Dijkstra routing、Mesa agent-based model 和多个 notebook。它是一个典型的“交通网络 + 气象场 + 路径优化 + 分配仿真”综合案例。

### 材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 项目说明与草稿 | project1_redacted、Report-Evaluation-Framework、Week2_teamwork、LR | 理解任务背景、评价框架和团队分工 |
| 数据 | NAT waypoints/tracks、OpenSky flight tracks、ERA5/GRIB weather、wind components | 构建路径网络与风场约束 |
| 代码 | getweather_v3.py、method2.ipynb、Dijkstra_algorithm、model_v1.py、mdm3_abm_v1.ipynb | 复现数据获取、路径成本计算、飞机分配和仿真 |
| 参考文献 | trajectory optimisation、dynamic airway/robust routing 等论文 | 支撑方法选择和报告讨论 |

## 01-问题抽象：航空路径规划

航空路径规划可以抽象为带约束的网络最短路问题。节点是 waypoints，边是可飞行航段，边权不只是地理距离，还可以加入风、燃油、时间、冲突风险、容量和 weather hazard。

基础形式：

$$
\min_{p \in \mathcal{P}_{od}} C(p)=\sum_{(i,j)\in p} c_{ij}
$$

其中 $p$ 是从 origin 到 destination 的路径，$c_{ij}$ 是航段 $(i,j)$ 的综合成本。若考虑风场，成本可写成：

$$
c_{ij}=lpha d_{ij}+eta h_{ij}+\gamma r_{ij}
$$

其中 $d_{ij}$ 为距离或飞行时间，$h_{ij}$ 为 headwind / tailwind 影响，$r_{ij}$ 为 weather hazard 或运营风险项。

## 02-数据与方法流程

1. **NAT network construction**：读取 `nat_waypoints.json` 和 `nat_data.json`，将 track 的 waypoint 转为节点与边。
2. **Flight track observation**：从 OpenSky 获取英国/爱尔兰至北美航班轨迹，用 CSV 记录真实飞行路径。
3. **Weather field modelling**：用 Open-Meteo / ERA5 获取 wind speed 与 wind direction，并转成 $u/v$ 风向分量。
4. **Route generation**：用 [[Dijkstra Algorithm]] 或备选启发式生成低成本路径。
5. **Aircraft assignment**：用 agent-based model / Mesa 模拟飞机在 track 上的分配、拥堵或冲突。
6. **Evaluation**：比较 baseline route 与 optimized route 在 distance、travel time、wind penalty、hazard exposure、network robustness 上的差异。

## 03-风场建模要点

代码中将 meteorological wind direction 转换为 east/north components：

$$
u=-s\sin(	heta), \qquad v=-s\cos(	heta)
$$

其中 $s$ 是风速，$	heta$ 是气象风向角；$u$ 表示 eastward component，$v$ 表示 northward component。路径航向向量与风向向量的点积可用于估计 headwind / tailwind effect。

## 04-Agent-Based Plane Assignment

`model_v1.py` 将 NAT tracks 读取为 network/track objects，并定义 weather field、CSV wind interpolation 和 aircraft assignment 逻辑。它适合讨论：

- 单架飞机的路径选择如何受风场影响；
- 多架飞机同时选择路径时是否会集中到少数 track；
- route optimisation 与 airspace capacity / conflict management 之间的张力；
- deterministic shortest path 与 stochastic / agent-based assignment 的差异。

## 20-项目报告框架

| 报告部分 | 建议内容 |
| --- | --- |
| Problem framing | NATS、跨大西洋航线、气象和容量对路径规划的影响 |
| Data | NAT waypoints、OpenSky tracks、ERA5/weather、航班样本范围 |
| Method | graph construction、wind field、Dijkstra / optimisation、ABM assignment |
| Evaluation | distance/time/fuel proxy、weather exposure、robustness、computational feasibility |
| Limitations | 数据时效、航路管制规则简化、风场高度层、冲突检测缺失、真实 ATC 约束 |

## 30-迁移价值

该项目可以和 [[四阶段法]] 的 assignment 概念联系：航空路径虽然不是城市交通 OD demand，但同样涉及 network representation、cost function、route choice 和 assignment。它也能和 [[Transport Data Collection]]、[[Network Flow]]、[[Traffic Assignment]] 形成图谱连接。

