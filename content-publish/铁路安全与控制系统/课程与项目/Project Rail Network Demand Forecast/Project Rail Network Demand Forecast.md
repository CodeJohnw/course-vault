---
type: project
project: Project Rail Network Demand Forecast
project_title: Rail Network Demand Forecast
school: Independent Project
school_link: "[[Independent Project]]"
discipline: 铁路安全与控制系统
discipline_code: 04-铁路安全与控制系统
major: 铁路安全与控制系统
major_code: 04-铁路安全与控制系统
major_link: "[[铁路安全与控制系统]]"
knowledge_cluster:
  - rail-demand-forecast
  - od-analysis
  - train-delay-data
  - graph-neural-network
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/Project-Rail Network Demand Forecast
tags:
  - school/independent-project
  - discipline/railway-safety-control
  - major/railway-safety-control
  - project/rail-demand-forecast
---

# Project Rail Network Demand Forecast


## 00-项目总览

- 资产类型：独立铁路数据分析项目
- 专业方向：[[铁路安全与控制系统]] / [[交通建模与数据分析]]
- 关联知识点：[[Rail Demand Forecast]]、[[OD Matrix]]、[[Train Delay Analysis]]、[[Graph Convolutional Network]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/Project-Rail Network Demand Forecast`

该项目围绕英国铁路 OD / delay 数据展开，包含 Esoterix CSV 原始数据、站点 ID 映射、线路/位置 JSON、数据清洗输出、Jupyter notebook 和客流预测参考论文。Notebook 已经形成批量读取 CSV、合并 DataFrame、清洗、统计 daily/hourly/monthly/season/station/TOC delay、生成 OD counts 的分析管线。

## 01-数据结构

| 数据 | 内容 | 用途 |
| --- | --- | --- |
| `legs-for-trainday-*.csv` | 按日期拆分的列车运行 leg 数据 | 原始运行记录 |
| `ID_Groupings.csv` | station_name 与 station_id 映射 | OD 和站点聚合 |
| `lines.json` / `locations.json` | 线路与位置数据 | 网络/地理结构 |
| `daily_delay_stats.csv` 等 | 清洗后的延误统计 | 可视化与建模输入 |

## 02-分析路线

1. 批量读取每日 CSV；
2. 合并并检查字段、日期、站点 ID；
3. 计算 departure / arrival delay；
4. 按 day、hour、month、season、station、TOC 聚合；
5. 生成 OD counts；
6. 可进一步引入 [[Graph Convolutional Network]] + recurrent model 做时空客流预测。

## 20-案例库

该项目适合挂接到铁路数据分析、客流预测和延误可靠性研究。后续可以补充模型评价指标，如 MAE、RMSE、MAPE，并把线路拓扑作为图结构输入。
