---
type: course
course: University of Glasgow ENG5031 Fault Detection Isolation and Recovery
course_title: Fault Detection Isolation and Recovery
course_code: ENG5031
school: University of Glasgow
school_link: "[[University of Glasgow]]"
discipline: 风险可靠性
discipline_code: 03-风险可靠性
major: 风险可靠性
major_code: 03-风险可靠性
major_link: "[[风险可靠性]]"
teacher: Dr E. McGookin
knowledge_cluster:
  - fault-detection-isolation-recovery
  - fault-diagnosis
  - fault-tolerant-control
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/University of Glasgow-ENG5031-Fault Detection Isolation and Recovery
tags:
  - course/ENG5031
  - school/university-of-glasgow
  - discipline/risk-reliability
---

# University of Glasgow ENG5031 Fault Detection Isolation and Recovery

## 00-课程总览

### 课程归属

- 学校：[[University of Glasgow]]
- 专业方向：[[风险可靠性]]
- 课程代码：[[ENG5031]]
- 课程主题：[[Fault Detection Isolation and Recovery]]、[[Fault Diagnosis]]、[[Fault Tree Analysis]]、[[Event Tree Analysis]]、[[Residual Generation]]、[[Fault-Tolerant Control]]、[[UAV Lateral Dynamics]]
- 教师线索：Dr E. McGookin
- 评估：FDIR technical report，固定翼 UAV heading motion，open-loop 与 closed-loop 两套 FDIR 系统。

### 课程定位

ENG5031 聚焦工程系统中的 fault detection、fault isolation 和 recovery。材料包括 lecture slides、tutorials、2016-2021 past exams、fault diagnosis reference books，以及一个以固定翼 UAV lateral dynamics 为对象的 FDIR 作业。课程同时连接机械安全、控制系统、事件树/故障树和容错控制。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/University of Glasgow-ENG5031-Fault Detection Isolation and Recovery`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | FDIR assignment specification、report guidelines | 明确技术报告任务和评分要求 |
| 课件 | lecture slides topic set | 学习 fault models、detection、classification、inference、recovery |
| 练习与数据 | Tutorials 1-3、solutions、Laplace transform、Mechanical Safety | 练习计算、系统建模和安全分析 |
| 试题与评估 | 2016-2021 ENG5031 exams 与 solutions | 建立考试题型库 |
| 阅读论文与参考 | Fault Diagnosis Systems、Fault-tolerant Flight Control 等 | 支撑模型诊断和容错控制理论 |
| 视频与代码 | Monday lectures mp4 | 课程视频回放 |

## 01-FDIR System Thinking

FDIR 包含三个层次：

- Fault Detection：判断系统是否偏离正常行为；
- Fault Isolation：判断故障发生在 sensor、actuator、process 或 controller 的哪个位置；
- Recovery：通过 reconfiguration、fallback control、sensor substitution、actuator compensation 或 safe mode 维持安全运行。

作业中特别区分 additive faults 与 multiplicative faults。sensor/actuator faults 多表现为 additive stepwise 或 driftwise fault；系统动力学变化则可能是 multiplicative fault。

## 02-UAV Lateral Dynamics Case

作业对象是固定翼 UAV 的 lateral dynamics，状态包括 roll rate $p$、yaw rate $r$、sideslip $\beta$、roll angle $\phi$、yaw angle $\psi$，输入是 aileron deflection $\delta_a$ 和 rudder deflection $\delta_r$。

可用状态空间形式表达：

$$
\dot{x}=Ax+Bu+f(t)+w(t)
$$

其中 $x=[p,r,\beta,\phi,\psi]^T$，$u=[\delta_a,\delta_r]^T$，$f(t)$ 表示 sensor/actuator fault 注入项，$w(t)$ 表示噪声或扰动。

## 03-Open-loop and Closed-loop FDIR

Open-loop 作业任务包括：

1. 建立 UAV continuous-time simulation；
2. 执行 $10^\circ/-10^\circ$ zig-zag heading manoeuvre；
3. 注入 heading sensor step/drift faults；
4. 注入 rudder actuator step/drift faults；
5. 设计 detection/isolation 机制；
6. 加入 $\pm 10^\circ$ heading output white noise 测试鲁棒性。

Closed-loop 任务包括设计 heading controller，使 UAV 完成 $45^\circ$ heading manoeuvre，并在 sensor/actuator faults 下检测、隔离和恢复。

## 04-Residual Generation and Thresholds

FDIR 中常用 residual 表示观测输出和模型预测输出之间的差：

$$
r(t)=y(t)-\hat{y}(t)
$$

若 $|r(t)|>\tau$，则可能触发 fault alarm，其中 $\tau$ 是 threshold。threshold 过低会造成 false alarm，过高会漏检。含噪声场景下要讨论 noise amplitude、filtering、detection delay 和 robustness。

## 20-作业案例库

推荐技术报告结构：

1. System description：UAV lateral dynamics、states、inputs、fault types；
2. Open-loop simulation：zig-zag manoeuvre、baseline response；
3. Fault injection：sensor/actuator step and drift faults；
4. Detection and isolation：residual、threshold、逻辑规则；
5. Recovery strategy：sensor substitution、actuator compensation、controller reconfiguration；
6. Closed-loop controller：heading control design 和 fault scenarios；
7. Noise robustness：white noise test、false alarm / missed detection；
8. Limitations：model uncertainty、noise、fault magnitude、delay、actuator saturation。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| Event Tree | hydrogen fuel cell safety | 成功/失败分支、后果路径 |
| Fault Tree | no electron flow / no water | AND/OR gate、top event、minimal cut sets |
| FDIR design | UAV heading sensor/actuator fault | residual、threshold、isolation logic |
| Control recovery | closed-loop heading manoeuvre | controller、reconfiguration、safe operation |
| Mechanical safety | fault diagnosis references | sensor/actuator/process fault distinction |

## 40-复习路线

1. 先理解 FDIR 三阶段，不要把 detection 和 isolation 混在一起。
2. 用 UAV 作业背熟 state-space、fault injection、residual、threshold 这条链。
3. 准备 event tree / fault tree 的图形化题型。
4. 对 open-loop 和 closed-loop 各准备一套 recovery strategy。
