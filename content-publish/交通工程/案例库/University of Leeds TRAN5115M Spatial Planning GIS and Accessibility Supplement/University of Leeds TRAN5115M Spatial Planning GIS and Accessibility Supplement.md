---
type: case
course: University of Leeds TRAN5115M Spatial Planning GIS and Accessibility Supplement
course_title: Spatial Planning GIS and Accessibility Supplement
course_code: TRAN5115M
school: University of Leeds
school_link: "[[University of Leeds]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通规划
major_code: 01-交通规划
major_link: "[[交通规划]]"
knowledge_cluster:
  - gis-accessibility
  - qgis
  - rail-job-accessibility
  - continuous-accessibility
  - sustainable-spatial-planning
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/01-交通规划/University of Leeds-TRAN5115M-Spatial Planning GIS and Accessibility Supplement
tags:
  - case/TRAN5115M
  - school/university-of-leeds
  - discipline/traffic-engineering
  - major/traffic-planning
  - gis/accessibility
---

# University of Leeds TRAN5115M Spatial Planning GIS and Accessibility Supplement

## 00-补充包总览

### 资产归属

- 学校：[[University of Leeds]]
- 专业方向：[[交通工程]] / [[交通规划]]
- 课程代码：[[TRAN5115M]]
- 对应主课程：[[University of Leeds TRAN5115M Sustainable Spatial Planning and Analysis]]
- 主题：[[GIS Analysis]]、[[QGIS]]、[[可达性（Accessibility）]]、[[Rail Job Accessibility]]、[[Deterrence Function]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/01-交通规划/University of Leeds-TRAN5115M-Spatial Planning GIS and Accessibility Supplement`

### 补充包定位

这是 TRAN5115M 的 GIS / Accessibility 实操补充包，包含 QGIS workshop、sustainable transportation lectures、land-use transport relationships、accessibility measures、rail job accessibility practical、Leeds LSOA boundary、UK train station、GJT、deterrence function、jobs data 等。它应作为 TRAN5115M 主笔记的案例/实操扩展，而不是另建一门独立课程。

### 材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课程说明 | Coursework 2 Guidance | 理解 GIS 空间分析作业要求 |
| 课件 | sustainability、land-use transport relationships、accessibility measures | 衔接理论与计算指标 |
| 数据与实操 | QGIS workshop、Coursework 2 GIS data、rail job accessibility practical | 练习空间 join、最近站点、GJT、deterrence function、地图表达 |
| 参考 | Cycle parking paper、GIS dataset guidance、example reports | 支撑报告和方法解释 |

## 01-QGIS 与空间分析流程

QGIS workshop 主要训练将空间边界、设施点、人口/就业 CSV 和路网数据组织到统一 CRS 下，并通过 spatial join / attribute join / nearest feature 形成可分析图层。对交通规划来说，GIS 的价值不只是画图，而是把 accessibility、exposure、equity 变成可计算和可沟通的空间指标。

## 02-连续可达性指标

Rail job accessibility practical 的核心任务是计算 Leeds LSOA 到全国就业机会的 rail accessibility，并比较三个场景：base scenario、Leeds-Manchester GJT 减少 20 分钟、Leeds-London GJT 减少 40 分钟。

典型连续可达性可写为：

$$
A_i=\sum_j O_j f(c_{ij})
$$

其中 $A_i$ 是 origin $i$ 的可达性，$O_j$ 是 destination $j$ 的机会数量（如 jobs），$c_{ij}$ 是广义出行成本或 generalized journey time，$f(c_{ij})$ 是随成本递减的 deterrence function。

若使用指数衰减函数：

$$
f(c_{ij})=e^{-eta c_{ij}}
$$

$eta$ 越大，远距离/高成本目的地的权重衰减越快。

## 03-Rail Job Accessibility 工作流

1. 导入 UK train station、Leeds LSOA boundary、England/Wales LSOA centroid、Scotland Data Zone centroid；
2. 为每个 origin / destination 找最近 rail station；
3. 合并 access/egress GJT 与 station-to-station GJT；
4. 构建 OD generalized journey time；
5. 应用 deterrence function 计算 jobs 加权可达性；
6. 聚合到 Leeds LSOA 并制图；
7. 比较 base 与 Manchester/London GJT 改善场景的差值。

## 20-案例库：GIS Accessibility Report

| 报告部分 | 建议内容 |
| --- | --- |
| Aim | 说明要评估 rail job accessibility 和政策场景 |
| Data | LSOA、Data Zone、station、GJT、jobs、deterrence function |
| Method | nearest station、OD matrix、deterrence weighting、aggregation、mapping |
| Results | base accessibility map、scenario difference map、空间不均衡 |
| Discussion | 解释哪些地区受益、为什么、局限和政策含义 |

## 30-与主课程连接

该补充包把 [[土地利用-交通互动]] 和 [[可达性（Accessibility）]] 具体化为 GIS 计算。它和 [[TOD（以公交为导向的开发）]]、[[5Ds（建成环境五维度）]] 的关系在于：空间结构影响出行成本，出行成本影响机会可达性，可达性又反过来影响土地价值、居住选择和交通需求。

