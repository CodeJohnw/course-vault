---
type: course
course: University of Birmingham RMC Railway Management and Control
course_title: Railway Management and Control
course_code: RMC
school: University of Birmingham
school_link: "[[University of Birmingham]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通工程
major_code: 02-交通工程
major_link: "[[交通工程]]"
teacher: Dr. Marcelo Blumenfeld
level: MSc
assessment:
  group_coursework: HS2 Signalling System Design (ETCS-2 + ATO GoA2)
  written_exam: Unknown
knowledge_cluster:
  - railway-management-and-control
  - train-control-systems
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Management and Control Train Control System
tags:
  - course/RMC
  - school/university-of-birmingham
  - discipline/traffic-engineering
  - major/traffic-engineering
---

# University of Birmingham RMC Railway Management and Control

## 00-课程总览

### 课程归属

- 学校：[[University of Birmingham]]
- 专业方向：[[交通工程]]
- 课程代码：RMC
- 课程主题：[[Railway Planning]]、[[Railway Operations]]、[[Railway Signalling]]、[[ETCS]]、[[Automatic Train Operation]]
- 教师：Dr. Marcelo Blumenfeld（Assistant Professor in Future Transport Systems, BCRRE）
- 评估：HS2 Signalling System Design Coursework（ETCS-2 + ATO GoA2 方案设计报告）
- 级别：MSc

### 课程定位

本课程为 University of Birmingham（伯明翰大学）铁路研究与教育中心（BCRRE）开设的硕士课程，系统讲授铁路管理与控制两大核心模块：**Railway Management and Control (RMC)** 覆盖铁路规划、运营、管理、系统工程的宏观决策体系；**Train Control** 覆盖故障安全原则、信号元件、轨道电路、联锁、ETCS、ATP、交通管理等底层信号控制技术。两模块互补，形成从战略规划到技术落地的完整铁路系统知识链。课程与 HS2 真实工程案例深度联动，大作业要求为 HS2 高速铁路设计 ETCS-2 + ATO GoA2 信号系统方案。

### 关联知识点

本课程与[[University of Leeds TRAN5020M Principles of Transport Modelling]]共享四阶段法、离散选择模型等交通建模知识；与[[Imperial College London CIVE70015 Traffic Engineering]]共享交通流理论与数据采集方法；与交通流基础材料共享 Greenshields 模型等基础理论。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/04-铁路安全与控制系统/University of Birmingham-RSEI-Railway Management and Control Train Control System`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | RMC Timetable、Coursework Brief（HS2 SIG Design） | 了解课程结构、作业要求、评分标准 |
| 课件 — RMC 模块 | RMC_L1 PlanningRailways、RMC_L2 ManagingOperations、RMC_L3 ManagingPerformance、RMC_L4 ManagingPerformance、RMC_L5 SystemsEngineering、RMC_L6 SE.pdf | 铁路规划四阶段法、GJT/GJC模型、成本效益分析、系统工程 |
| 课件 — Train Control 模块 | L01 Fail-safe 至 L10 Traffic Management（共10讲） | 信号系统从元件到系统的完整知识链 |
| 练习与数据 | HS2 SIG Coursework 全套参考文档（8+份）、HS2 Scope Document、Technical Specifications | HS2 真实工程参数用于大作业设计 |
| R代码 | Final Code（HS2方案设计计算代码） | 信号设计参数计算和容量分析 |

## 01-Railway Management and Control（RMC 模块）

**讲师**：Dr. Marcelo Blumenfeld，Assistant Professor in Future Transport Systems, BCRRE

### Lecture 1 — Railway Planning

**核心问题**：为什么人们出行？出行是派生需求（derived demand）。出行时间预算约70分钟/天，决定了城市的物理边界。

**外部成本**（EUR-cents/passenger-km）：

| 成本类别 | Car | Electric Train | Diesel Train |
| --- | --- | --- | --- |
| Accident | 4.5 | 0.5 | 0.5 |
| Air Pollution | 0.71 | 0.01 | 0.8 |
| Climate Change | 1.18 | 0 | 0.34 |
| Noise | 0.6 | 0.8 | 1.4 |
| Congestion | 5.12 | 0 | 0 |
| **TOTAL** | **23.54** | **2.68** | **3.99** |

铁路的**正外部性**：土地价值捕获（LVC）、诱导投资、就业效应、健康生活质量提升。

**车站接入距离**：巴士400m、铁路800m。超过此距离，乘客步行意愿显著下降（<30%乘客愿走超过400m）。

**Door-to-door 速度**比最大运行速度更重要。站间距 D 与接入距离 d 存在矛盾：站间距越大，最大速度越高，但接入距离越长。

**在途时间公式**：

$$
T_v = \sum \left[ \frac{D_{ij}}{V} + \frac{V}{2} \left(\frac{1}{\alpha} + \frac{1}{\beta}\right) + nT_j + T_d \right]
$$

其中 V 为最大线速度(m/s)，α 为加速度(m/s²)，β 为制动减速度(m/s²)，T_d 为停站时间，T_j 为加加速度过渡时间。

### Lecture 2 — Railway Operations（需求预测与评估）

**四阶段交通模型**（Four-Stage Transport Model）：

1. **Trip Generation**：基于土地利用、家庭人口统计、社会经济因素估算各空间单元的出行产生/吸引量
2. **Trip Distribution**：空间交互模型（重力模型），考虑 O/D 间距离/时间/成本阻力，输出流量矩阵
3. **Modal Split**：基于离散选择模型（Discrete Choice Models），由 SP/RP 分析校准
4. **Traffic Assignment**：将所有出行分配到交通网络，用户最小化出行时间；容量超限时反馈调整前三阶段

**广义时间函数 (GJT)**：

$$
\text{GJT} = a_1 t_j + 2(a_2 t_a) + a_3 t_w + a_4 t_i + a_5 t_d
$$

权重：在途时间 a₁=1、接入时间 a₂=1.5-2、等待时间 a₃=1.5-2、换乘时间 a₄=2-3、延误 a₅≈3。

**广义成本函数 (GJC)**：

$$
\text{GJC} = \frac{\text{fare}}{a_0} + \text{GJT}
$$

a₀ 为出行者时间价值（£/min），UK DfT 2015 标准：通勤汽车 £7.62/h、铁路通勤 £24.72/h（<20 miles）。

**项目评估**（Appraisal）：UK 使用 Transport Analysis Guideline (TAG)；European Investment Bank 开发 RailPAG。成本效益分析（CBA）量化可货币化的成本与效益，但对非货币化效益（舒适度、社会公平）有限制。评估需包含至少 Do-minimum 和 Do-something 两种方案。

### Lecture 3 — Managing Performance

铁路系统性能管理框架：可靠性、准点率、容量利用率、服务质量多维指标体系。关注系统级 view：集成、互操作性、网络效应。

### Lecture 4 — Managing Infrastructure

基础设施管理：资产管理、维护策略、生命周期成本。铁路系统需要对轨道、信号、供电、通信等子系统进行协调管理。

### Lecture 5-6 — Systems Engineering

系统工程方法论：从需求定义到系统设计、集成验证、运营维护的全生命周期。铁路作为 system-of-systems 需要跨学科、跨子系统的整体视角。采用 V-model 和 INCOSE 标准流程。

## 02-Train Control Systems（信号控制模块）

完整覆盖铁路信号系统从元件到系统的知识链（Lectures 1-10）。

### L1 — Fail-Safe Principles

**故障安全原则**（Fail-Safe）：系统故障时自动进入安全状态。铁路信号系统要求任何单点故障不得导致危险状态。核心设计原则包括冗余设计、故障检测、graceful degradation。信号系统安全完整性等级（SIL4）是最高安全要求。

### L2 — Signals and Signalling Elements

**信号元件**分类：信号机类型（进站、出站、通过、调车）、信号灯颜色含义（红=停止、黄=注意/减速、绿=通行）、信号显示序列。色灯信号（Colour-light Signalling）vs 传统臂板信号。

### L3 — Signalling Displays

**信号显示**规范：英国信号系统显示规则（Route Signalling vs Speed Signalling）、信号机布置原则（制动距离、前方路段条件）、多灯信号组合含义。

### L4 — Relays

**继电器**：铁路信号系统的基本逻辑构建元件。继电器联锁逻辑实现进路安全控制。关键特性：高可靠性、fail-safe 设计（重力释放型继电器）、电气隔离。

### L5 — Track Circuits & Axle Counters

**轨道电路**：利用钢轨作为导电回路，检测列车占用状态。基本原理：发送端→钢轨→接收端；列车占用时轮对短路，接收端电压降为零。

$$
\text{Track Occupancy Detection: } V_{\text{receive}} = \begin{cases} V_{\text{normal}} & \text{no train} \\ 0 & \text{train occupies} \end{cases}
$$

**轴计数器**（Axle Counters）：替代轨道电路的现代方案。入口计数+出口计数，差值为0时区间空闲。优势：不受轨道污染（生锈、落叶）影响、无需绝缘节、适合长区间。

### L6 — Interlocking

**联锁**（Interlocking）：确保进路、信号、道岔间的安全逻辑约束。核心规则：
- 信号开放前必须锁闭进路（道岔位置正确并锁闭）
- 敌对进路不得同时开放
- 进路占用期间信号不得开放敌对进路

联锁系统演进：机械联锁 → 继电联锁 → 电子联锁（Solid State Interlocking, SSI）→ 计算机联锁（CBI）。

### L7 — Cab Signalling & ATP

**驾驶室信号**（Cab Signalling）：将信号显示从轨旁转移到司机驾驶室显示屏。优势：消除视线遮挡和天气影响、支持更高速度运行（人眼在>200km/h难以可靠识别轨旁信号）。

**列车自动防护**（ATP — Automatic Train Protection）：持续监控列车速度，自动施加制动防止超速和冒进。ATP 功能包括：速度监督、制动曲线计算、临时限速执行。

**制动曲线**：

$$
v_{\text{max}} = \sqrt{v_{\text{current}}^2 - 2a_{\text{brake}} d_{\text{remaining}}}
$$

### L8 — ETCS Levels & Architecture

**ERTMS/ETCS**（European Rail Traffic Management System / European Train Control System）：欧洲统一铁路信号标准。

| ETCS Level | 通信方式 | 轨旁设备 | 核心特征 |
| --- | --- | --- | --- |
| **Level 0** | — | 无/传统系统 | 在未装备ETCS线路运行 |
| **Level NTC** | — | 国别系统 | ETCS作为传统ATP系统的界面 |
| **Level 1** | 点式（Eurobalise） | 轨旁信号+应答器 | 叠加在传统信号系统上，间歇通信 |
| **Level 2** | 连续（GSM-R/FRMCS） | 可无轨旁信号 | RBC连续发送行车许可，轨旁仍保留列车检测 |
| **Level 3（已合并入L2）** | 连续 | 无轨道电路 | 列车自报位置+完整性，虚拟/移动闭塞；CCS TSI 2023 已合并入 Level 2 |

**ETCS Level 2 为什么是高速铁路首选**：
1. 技术成熟可靠，已在意大利、荷兰、德国、法国、比利时、瑞士等国广泛部署
2. 轨旁列车检测设备提供冗余安全保障
3. 支持更高运行速度和更小行车间隔（headway）
4. 成本较 Level 1 更低（可取消轨旁信号机），且可平滑升级至含移动闭塞功能

### L9 — Automatic Train Operation (ATO)

**ATO 自动化等级（GoA）**：

| GoA | 启动 | 停车 | 门控 | 应急 | 描述 |
| --- | --- | --- | --- | --- | --- |
| GoA0 | 司机 | 司机 | 司机 | 司机 | 无 ATP，目视行车 |
| GoA1 | 司机 | 司机 | 司机 | 司机 | ATP 防护，司机驾驶 |
| GoA2 | 自动 | 自动 | 司机 | 司机 | **半自动化运行**（HS2 选择） |
| GoA3 | 自动 | 自动 | 自动 | 乘务员 | 无人驾驶，车上乘务员 |
| GoA4 | 自动 | 自动 | 自动 | 自动 | 完全无人驾驶（UTO） |

HS2 采用 **ATO GoA2 over ETCS Level 2**：列车自动控制启停和速度调节，司机负责关门和应急处理。Thameslink 已实现 ATO+ETCS 集成，为 HS2 提供>10年经验积累。

### L10 — Traffic Management

**交通管理系统（TMS）**：基于实时运行数据优化列车调度。功能包括：
- 冲突检测与解决（Conflict Detection & Resolution）
- 列车运行图调整（Timetable Rescheduling）
- 延误传播预测
- 与 CCS 信号系统联动

HS2 TMS 功能要求：Enterprise Service Bus (ESB)、Possession Management System (PMS)、Adhesion Management System (AMS)、Weather Monitoring System (WMS)。

## 20-Coursework 案例库 — HS2 Signalling System Design

**大作业**：为 HS2 Phase One（London Euston → Birmingham Curzon Street，~220km）设计信号与列车控制系统方案。

### HS2 Phase One 核心参数

| 参数 | 数值 |
| --- | --- |
| 线路长度 | ~220km（含 50km 隧道、16km 高架桥） |
| 最大运营速度 | 360 km/h（设计速度从最初400kph降低，节省成本+能源+降噪） |
| 目标运量 | 18 tph（双向，每小时18对列车） |
| 车站 | 4座（Euston 6台、Old Oak Common 6台、Birmingham Interchange 4台、Curzon Street 7台） |
| 列车编组 | 200m 单组 / 400m 重联 |
| 运营时间 | 周一至六 05:00-23:59，周日 08:00-23:59 |
| 技术行车间隔 | 120 秒（平线） |
| 平均延误目标 | ≤30 秒/列车 |
| 预算 | £450 亿（Phase One） |

### 推荐方案：ETCS Level 2 + ATO GoA2

**信号系统选择理由**：

1. **ETCS-2 成熟可靠**：已在欧洲多国高速铁路验证，支持 360km/h 连续通信和行车许可更新
2. **取消轨旁信号**：ETCS-2 通过 RBC→GSM-R→驾驶室 DMI 传输信号，消除恶劣天气/高速运行时的视认困难
3. **ATO GoA2 保障 18 tph**：自动速度控制配合 120s headway 实现高频运营
4. **容量优势**：ETCS-2 相比传统 ATC 系统总容量消耗更低
5. **可平滑升级**：ETCS-2 可向移动闭塞/Hybrid Level 3 演进，无需重构基础设施

**CCS & TM 系统架构**（Siemens 承建）：

- **RBC**（Radio Block Centre）：通过 GSM-R/FRMCS 持续发送 MA（Movement Authority）
- **ATO**：GoA2 等级，通过 ERTMS 接收 ATO 数据，仅在 Full Supervision MA 下启用
- **TMS**：高级交通管理，含 ESB/PMS/AMS/WMS
- **列车检测**：轴计数器（Axle Counters）
- **最小无线配置**：3台 GSM-R/GPRS EDOR（2台 ETCS + 1台 ATO，ETCS 第二台用于与第二 RBC 通信）
- **基线规范**：ETCS Baseline 3 Release 2（CCS TSI 附录 A）
- **车轮校准**：自动重校准（车轮磨损补偿），Eurobalise 精度 Q_LOCACC

**传统网络过渡**：列车进入 CRN（Conventional Rail Network）时改用 AWS/TPWS + 轨旁色灯信号 + 手动驾驶模式 + C-DAS 驾驶建议。

### 系统架构图

```
ETCS Level 2 (GoA2):

  ┌──────────┐     GSM-R/FRMCS     ┌──────────┐
  │   RBC    │◄───────────────────►│ On-board │
  │ (Radio   │    Movement         │  EVC +   │
  │  Block   │    Authority +      │  ATO +   │
  │  Center) │    Train Position   │  DMI     │
  └────┬─────┘                     └────┬─────┘
       │                                │
  ┌────▼─────┐                     ┌────▼─────┐
  │Interlocking│◄──Train Detection─│Track-side│
  │  (CBI)   │    (Axle Counters) │ Balises  │
  └──────────┘                    └──────────┘
```

### 容量分析

**最小 headway（ETCS L2 固定闭塞）**：

容量消耗（CC）分级：
- CC > 100%：无剩余容量（拥挤区段）
- 80% < CC < 100%：低剩余容量
- CC < 80%：充足剩余容量

HS2 120s headway 目标下需在 ETCS-2 continuous MA 更新模式下进行微观仿真验证。

### 方案设计报告建议结构

1. **Introduction** — 项目背景、HS2 概况、设计目标
2. **Signalling and Train Control Systems Design** — ETCS 等级比选、ATO 方案论证、CCS & TM 子系统设计
3. **Operational Capacity Analysis and Timetable Design** — 最小 headway 计算、容量消耗评估、运行图设计
4. **Conclusions** — 方案总结、风险与限制

**References**（关键来源）：HS2 Scope Document Compendium Version、HS2 Rolling Stock Technical Specification、HS2 Railway Systems Contracts、Impact of signalling system on capacity (2022)、Review of Technical Specification for High Speed Rail in the UK 等。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| 广义成本计算 | 给定出行参数计算 GJT/GJC | GJT/GJC 公式及权重取值 |
| ETCS 等级比选 | 给定运营场景选择最优 ETCS Level | Level 0/1/2 特征对比，适用场景判断 |
| 故障安全分析 | 信号元件失效时的安全状态 | Fail-safe 原则、轨道电路/轴计数器原理 |
| 四阶段模型 | 给定土地利用数据构建出行需求 | 四阶段法各步骤输入输出和典型模型 |
| 容量分析 | 给定 headway 和速度计算线路容量 | 最小 headway 公式、CC 指标 |

## 40-复习路线

1. **RMC 模块**（规划→运营→性能→系统工程）：重点掌握四阶段法流程、GJT/GJC 公式及参数权重、外部成本表、CBA 评估框架
2. **Train Control 模块**：按课件顺序从下到上——继电器→轨道电路/轴计数器→联锁→ATP→ETCS→ATO→TMS，理解每层如何依赖下层
3. **HS2 Coursework**：熟记 HS2 Phase One 核心参数，理解 ETCS-2 + ATO GoA2 方案的技术论证逻辑，能用 ETCS Level 选择矩阵回答设计问题

## 50-铁路安全与控制系统资料包补充

本次新增来源来自 `04-铁路安全与控制系统` 下的 RSEI Railway Management and Control / Train Control System 资料包。它补充了 HS2 SIG assignment、ETCS Level 2 + ATO GoA2 方案、capacity calculation notebook、时刻表和信号系统参考文献。该资料包仍挂接到本 RMC 主笔记，避免重复建课。
