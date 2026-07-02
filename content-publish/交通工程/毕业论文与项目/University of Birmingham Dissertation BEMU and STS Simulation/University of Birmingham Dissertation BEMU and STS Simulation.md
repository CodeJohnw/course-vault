---
type: dissertation
dissertation: University of Birmingham Dissertation BEMU and STS Simulation
dissertation_title: BEMU and STS Simulation
school: University of Birmingham
school_link: "[[University of Birmingham]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 毕业论文与项目
major_code: 07-毕业论文与项目
major_link: "[[毕业论文与项目]]"
knowledge_cluster:
  - railway-decarbonisation
  - battery-electric-multiple-unit
  - single-train-simulation
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-Dissertation-BEMU and STS Simulation
tags:
  - dissertation/bemu-sts
  - school/university-of-birmingham
  - discipline/traffic-engineering
  - major/dissertation-project
---

# University of Birmingham Dissertation BEMU and STS Simulation

## 00-项目总览

- 学校：[[University of Birmingham]]
- 专业方向：[[交通工程]] / [[毕业论文与项目]]
- 研究主题：将 Class 507/508 改造成 [[BEMU]]，并用 [[STS Simulation]] 在 Llangollen Railway 线路上测试运行表现。
- 关联知识点：[[Railway Decarbonisation]]、[[Battery Electric Multiple Unit]]、[[Single Train Simulator]]、[[Railway Traction Energy]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-Dissertation-BEMU and STS Simulation`

该论文资产的核心问题是：在既有第三轨动车组结构基础上，是否可以通过加装电池系统形成 battery powered train，并在非电气化或局部电气化线路上保持可接受的运行性能、能耗和安全边界。

## 01-材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 项目说明 | 需求描述、Central Topic | 明确设计任务和导师反馈点 |
| 数据与模型 | STS / STS 507 / STS 2 MATLAB 脚本、route_Llangollen、Class 508 技术资料 | 复现单列车仿真和车辆参数设定 |
| 文献与参考 | BEMU、traction decarbonisation 相关资料 | 支撑背景和技术路线 |
| 论文与展示 | 论文版本、poster、海报提交 | 形成最终汇报模板 |

## 02-STS 仿真工作流

Single Train Simulator 的主脚本使用 `vehicle_507_Battery` 设定车辆，载入 `route_Llangollen` 线路，并通过距离步长推进速度、牵引、制动、时间和能耗计算。核心流程是：选择车辆参数、载入线路、前向速度计算、后向制动曲线、合并速度包络、计算时间和 SOC / 能耗曲线。

阻力可按 Davis equation 表达：

$$
R(v)=A+Bv+Cv^2
$$

其中 $A$ 表示滚动和机械阻力常数项，$Bv$ 表示速度相关阻力，$Cv^2$ 表示空气阻力项。

## 03-BEMU 改造思路

初步设想是在车辆两端加入 battery power source，但需要进一步考虑 contact shoe、功率、规格、质量、空间、充电方式和安全保护。成熟设计至少要覆盖电池容量与峰值功率、电池质量对制动距离和能耗的影响、第三轨集电靴改造、再生制动、线路坡度、站间距和 charging strategy。

## 20-案例库

该资产可作为铁路低碳化项目的技术案例：用既有车辆资料建立车辆参数，用 STS 建立线路运行仿真，用能耗和 SOC 输出判断 BEMU 改造边界。

## 50-铁路安全与控制系统资料包补充

本次新增来源来自 `04-铁路安全与控制系统` 下的 BEMU and STS Simulation 文件夹，内容与既有 BEMU dissertation 一致但来源路径已整理；补充了 Class 508、STS 仿真、traction decarbonisation、poster 和论文版本的集中结构。
