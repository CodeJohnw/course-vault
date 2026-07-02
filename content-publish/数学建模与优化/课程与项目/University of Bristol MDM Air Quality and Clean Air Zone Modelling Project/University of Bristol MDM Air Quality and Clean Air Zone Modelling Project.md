---
type: project
course: University of Bristol MDM Air Quality and Clean Air Zone Modelling Project
course_title: Air Quality and Clean Air Zone Modelling Project
course_code: MDM
project: University of Bristol MDM Air Quality and Clean Air Zone Modelling Project
project_title: Air Quality and Clean Air Zone Modelling Project
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数学建模与优化
major_code: 09-数学建模与优化
major_link: "[[数学建模与优化]]"
knowledge_cluster:
  - air-quality-modelling
  - gis-analysis
  - clean-air-zone
  - emissions-data
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Bristol-MDM-Air Quality and Clean Air Zone Modelling Project
tags:
  - school/university-of-bristol
  - discipline/mathematical-modelling-optimization
  - major/mathematical-modelling-optimization
  - project/air-quality-modelling
---
# University of Bristol MDM Air Quality and Clean Air Zone Modelling Project


## 00-项目总览

- 学校：[[University of Bristol]]
- 项目代码：[[MDM]]
- 专业方向：[[数学建模与优化]] / [[交通工程]]
- 关联知识点：[[Air Quality Modelling]]、[[GIS Analysis]]、[[Clean Air Zone]]、[[Emission Inventory]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Bristol-MDM-Air Quality and Clean Air Zone Modelling Project`

该项目围绕 Bristol / London 空气质量与 Clean Air Zone 建模，包含 QGIS 工程、空气质量连续监测数据、AURN 数据、Air Quality Management Areas、monitor points、background pollutant grid、Clean Air Zone、LAEI emissions 数据和 notebook。

## 01-数据地图

| 数据 | 作用 |
| --- | --- |
| AirQualityContinuousLatest / AURN | 监测时间序列 |
| Air_quality_monitors | 监测站点位置 |
| Air_Quality_Management_Areas | 管理区 GIS 边界 |
| Background_pollutant_data_grid | 背景污染浓度空间网格 |
| Clean_Air_Zone | 政策区域边界 |
| LAEI emissions | 道路/区域排放清单 |

## 02-建模路线

先做空间 join 和时间序列清洗，再比较 CAZ 内外污染指标，最后用可视化或回归解释污染源、道路排放和政策区之间的关系。适合连接 [[GIS Analysis]]、[[Regression]] 和 [[Policy Evaluation]]。
