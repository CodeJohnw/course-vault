---
type: course
course: University of Birmingham RSEI-ETS Electric Traction Systems
course_title: Electric Traction Systems
course_code: RSEI-ETS
school: University of Birmingham
school_link: "[[University of Birmingham]]"
discipline: 铁路安全与控制系统
discipline_code: 04-铁路安全与控制系统
major: 铁路安全与控制系统
major_code: 04-铁路安全与控制系统
major_link: "[[铁路安全与控制系统]]"
level: MSc
assessment: coursework / project based
knowledge_cluster:
  - electric-traction
  - traction-package-design
  - rail-decarbonisation
  - adhesion-management
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Electric Traction Systems
tags:
  - course/RSEI-ETS
  - school/university-of-birmingham
  - discipline/railway-safety-control
  - major/railway-safety-control
  - topic/electric-traction
---

# University of Birmingham RSEI-ETS Electric Traction Systems


## 00-课程总览

- 学校：[[University of Birmingham]]
- 专业方向：[[铁路安全与控制系统]]
- 课程代码：[[RSEI-ETS]]
- 课程主题：[[Electric Traction Systems]]、[[Traction Package Design]]、[[Railway Decarbonisation]]、[[BEMU]]、[[Adhesion Management]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Electric Traction Systems`

该模块围绕铁路电气牵引系统展开，覆盖 AC/DC electrification、autotransformer、高压电气安全、牵引电机、power electronic controllers、多模式车辆、rail batteries、traction decarbonisation 和能耗/排放分析。

## 01-材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课件 | AC/DC electrification、batteries in rail、traction machines、power electronics、adhesion、emissions | 建立牵引系统和脱碳技术主线 |
| 作业 | spreadsheet traction package design、Class 156 decarbonisation written assignment | 从计算工具到概念设计 |
| 数据模型 | train_traction_v1.0.xlsx | 牵引计算和车辆参数模板 |

## 02-牵引包设计

Spreadsheet assignment 要求做一个高层 traction package design 工具。输入至少包括车辆数、轴数、质量、惯性质量、要求加速度、最高速度、可用黏着、持续坡度和轮径；输出包括驱动轴配置、轮周扭矩、电机轴扭矩、传动比、可持续速度和最高电机转速。

牵引力基本关系：

$$
F=m_{eq}a+R(v)+mg\sin	heta
$$

其中 $m_{eq}$ 为含旋转惯量折算后的等效质量，$a$ 为加速度，$R(v)$ 为运行阻力，$	heta$ 为坡度角。

## 20-Coursework案例库

- **Spreadsheet design**：强调单位、颜色区分、公式可见、无隐藏单元格、输出验证。
- **Written assignment**：面向 Class 156 或类似车辆提出牵引与制动系统脱碳概念方案。
- **Validation**：用既有车辆、行业经验或 rule of thumb 对输出做 sanity check。
