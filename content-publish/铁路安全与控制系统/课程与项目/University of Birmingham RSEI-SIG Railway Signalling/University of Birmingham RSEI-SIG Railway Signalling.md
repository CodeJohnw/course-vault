---
type: course
course: University of Birmingham RSEI-SIG Railway Signalling
course_title: Railway Signalling
course_code: RSEI-SIG
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
  - railway-signalling
  - headway
  - time-distance-graph
  - braking-distance
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Signalling
tags:
  - course/RSEI-SIG
  - school/university-of-birmingham
  - discipline/railway-safety-control
  - major/railway-safety-control
  - topic/railway-signalling
---

# University of Birmingham RSEI-SIG Railway Signalling


## 00-课程总览

- 学校：[[University of Birmingham]]
- 专业方向：[[铁路安全与控制系统]]
- 课程代码：[[RSEI-SIG]]
- 课程主题：[[Railway Signalling]]、[[Time-Distance Graph]]、[[Capacity and Headway]]、[[Braking Distance]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Signalling`

该资产是铁路信号与运行图专题，围绕 Derby-Sheffield Railway、headway 计算、time-distance graph 和 braking signals 展开。它与已有 [[RSEI Signalling System Time-Distance Graph Case]] 是同一知识簇的课程化版本。

## 01-材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 作业 | written assignment brief、Derby-Sheffield Railway mind map | 信号系统方案与走廊分析 |
| 数据模型 | headway Cal.xlsx | 追踪间隔和能力计算 |
| 代码工具 | Q2_TimeDist_Graph.ipynb | 绘制时距图、检查冲突 |
| 参考 | New Adlestrop Railway Atlas、braking-signals | 线路和制动信号参考 |

## 02-Headway 与时距图

时距图把时间放在横轴、距离放在纵轴，不同列车的斜率表示速度。若两条线太接近或交叉，就说明存在追踪间隔、会让、越行或冲突风险。基本运行时间：

$$
t=rac{d}{v}	imes 60
$$

其中 $d$ 为距离 km，$v$ 为速度 km/h，$t$ 为分钟。

## 20-Coursework案例库

本资产适合作为铁路信号小案例：用 atlas 和运行参数定义线路，Excel 做 headway，Notebook 出图，再用 braking signals 解释信号间距和安全裕度。
