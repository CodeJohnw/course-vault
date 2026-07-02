---
type: course
course: University of Bristol EENG30013 Power Electronics Machines and Drive Technologies
course_title: Power Electronics Machines and Drive Technologies
course_code: EENG30013
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 能源管理与环境
discipline_code: 10-能源管理与环境
major: 能源管理与环境
major_code: 10-能源管理与环境
major_link: "[[能源管理与环境]]"
knowledge_cluster:
  - power-electronics
  - electric-machines
  - drive-technologies
  - pwm-inverter
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/University of Bristol-EENG30013-Power Electronics, Machines & Drive Technologies
tags:
  - course/EENG30013
  - school/university-of-bristol
  - discipline/energy-management-environment
  - major/energy-management-environment
---

# University of Bristol EENG30013 Power Electronics Machines and Drive Technologies

## 00-课程总览

### 课程归属

- 学校：[[University of Bristol]]
- 专业方向：[[能源管理与环境]] / [[电力与能源系统]]
- 课程代码：[[EENG30013]]
- 课程主题：[[Power Electronics]]、[[Electric Machines]]、[[Drive Technologies]]、[[PWM Inverter]]、[[DC Link]]、[[Switching Losses]]
- 评估：coursework parts 1-4，individual open-book submission
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/10-能源管理与环境/University of Bristol-EENG30013-Power Electronics, Machines & Drive Technologies`

### 课程定位

EENG30013 聚焦 power electronics、machines 和 drive technologies。Coursework 要求从 system-level requirements 推导 machine requirements，分析 DC-link capacitance、filter inductance 和 PWM pattern 对 drive operation 的影响，计算 switches losses 并评估 heatsink / thermal design。

### 材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | Full Coursework Parts 1 to 4 | 明确四个设计任务和提交要求 |
| 课件 | Week 3-5 slides、PEMD W7/W8 recorded notes | 复习 machines、converters、switches |
| 练习与数据 | Activity sheets、Part1 slx、参数计算过程 | 复盘仿真和计算流程 |
| 待确认 | 微信截图 | 可能是计算或仿真问题截图 |

## 01-Machines and Drive Requirements

Part 1 的关键是把系统需求转化为机器需求，例如 torque、speed、power、efficiency 和 operating envelope。基本机械功率关系为：

$$
P=T\omega
$$

其中 $P$ 是机械功率，$T$ 是转矩，$\omega$ 是角速度。驱动系统设计需要同时满足峰值需求、连续运行、热约束和效率目标。

## 02-Converters, DC Link and PWM

Part 2 关注三相 inverter、DC-link capacitance、filter inductance 和 PWM sampling / harmonic analysis。DC-link 的作用是平衡输入输出瞬态功率并抑制电压纹波。电容基本关系为：

$$
i_C=Crac{dv_C}{dt}
$$

PWM 分析的重点是 switching pattern 如何影响 harmonic spectrum、current ripple、losses 和 drive quality。

## 03-Switches and Thermal Design

Part 3 关注 semiconductor switches 的 conduction loss、switching loss 和 heatsink suitability。损耗越高，junction temperature 越高，必须通过 thermal resistance chain 评估：

$$
T_j=T_a+P_{loss}R_{	heta ja}
$$

其中 $T_j$ 是 junction temperature，$T_a$ 是 ambient temperature，$P_{loss}$ 是器件损耗，$R_{	heta ja}$ 是结到环境热阻。

## 20-Coursework案例库

| Part | 任务 | 输出 |
| --- | --- | --- |
| Part 1 Machines | system requirements -> machine requirements | short deliverable + working simulation |
| Part 2 Converters | DC link / filter / PWM impact | calculation, harmonic interpretation, simulation |
| Part 3 Switches | losses and heatsink design | loss budget, thermal suitability |
| Part 4 Design study | assigned theme deeper exploration | design analysis and engineering justification |

## 40-复习路线

先整理四个 Part 的输入、模型、输出和单位，再检查每个计算是否能被仿真复现。高风险点是引用/AI 政策：所有外部资料、模型结构、代码和公式来源都必须透明说明。

