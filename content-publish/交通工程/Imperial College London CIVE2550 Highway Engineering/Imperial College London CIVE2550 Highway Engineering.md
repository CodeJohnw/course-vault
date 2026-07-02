---
type: course
course: Imperial College London CIVE2550 Highway Engineering
course_title: Highway Engineering
course_code: CIVE2550
school: Imperial College London
school_link: "[[Imperial College London]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 交通工程
major_code: 02-交通工程
major_link: "[[交通工程]]"
teacher: Institute for Transport Studies (Leeds ITS collaboration)
level: Undergraduate
assessment:
  tutorials: 视距/平曲线/竖曲线计算练习
  coursework: Highway Engineering.xlsx 综合设计
knowledge_cluster:
  - highway-design
  - sight-distance
  - geometric-design
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/07-毕业论文与项目/Imperial College London-CIVE2550-Highway Engineering
tags:
  - course/CIVE2550
  - school/imperial-college
  - discipline/traffic-engineering
  - major/traffic-engineering
---

# Imperial College London CIVE2550 Highway Engineering

## 00-课程总览

### 课程归属

- 学校：[[Imperial College London]]
- 专业方向：[[交通工程]]
- 课程代码：[[CIVE2550]]
- 课程主题：[[路口设计]]、[[交通流基本图]]
- 教师：Institute for Transport Studies（与 University of Leeds ITS 合作授课）
- 评估：视距/平曲线/竖曲线计算练习 + 综合设计Excel

### 课程定位

本课程是 Imperial College London 开设的本科公路工程核心课程，系统讲授公路几何设计原理。课程基于英国 DMRB（Design Manual for Roads and Bridges）和 AASHTO 标准，涵盖视距设计、平曲线与竖曲线几何设计、设计速度选择以及平纵组合设计等核心内容。课程强调计算实操与设计标准应用。

### 关联知识点

本课程通过以下共享知识点与其他课程连接：[[路口设计]]、[[交通流基本图]]。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/02-交通工程/Imperial College London-CIVE2550-Highway Engineering`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课件 | Lect 2 视距 / Lect 3-4 平曲线 / Lect 5-6 竖曲线 / Lect 7 设计速度 | 核心几何设计理论 |
| 练习与数据 | Highway Engineering.xlsx | 综合设计计算 |
| 试题与评估 | DN-GEO-03031-06.pdf | 设计标准参考 |
| 图纸 | 绘图1.vsdx | 几何设计示意图 |

## 01-视距设计（Sight Distance）

### 停车视距（Stopping Sight Distance, SSD）

停车视距是驾驶员发现障碍物后安全停车所需的最小可见距离，由反应距离和制动距离组成：

$$
SSD(m) = 0.278 \times V \times t + \frac{V^2}{254 \times \left(\frac{a}{9.81} \pm G\right)}
$$

其中 $V$ 为设计速度（km/h），$t$ 为感知-反应时间，$a$ 为减速度（m/s²），$G$ 为纵坡（上坡为正，下坡为负）。

**关键参数**：
- 保守值：$t = 2.5$ s，$a = 3.4$ m/s²
- UK DMRB：$t = 2.0$ s，$a = 2.45$ m/s²

**DMRB 停车视距标准（CD 109）**：

| 设计速度 (km/h) | 理想最小值 (m) | 低一级 (m) |
| --- | --- | --- |
| 120 | 295 | 215 |
| 100 | 215 | 160 |
| 85 | 160 | 120 |
| 60 | 90 | 70 |
| 50 | 70 | 50 |

### 超车视距（Passing/Overtaking Sight Distance, PSD/OSD）

超车视距是双向两车道公路上安全超车所需的最小可见距离，由四段组成：

$$
PSD = D_1 + D_2 + C + D_3
$$

- $D_1$：感知时间 + 加速至与慢车并行（含换道距离）
- $D_2$：占用对向车道行驶距离
- $D_3$：对向来车在 2/3 超车时间内行驶的距离
- $C$：安全间隙（通常 75 m）

**DMRB 全超车视距（FOSD）**：

| 设计速度 (km/h) | FOSD (m) |
| --- | --- |
| 120 | 580 |
| 100 | 490 |
| 85 | 410 |
| 60 | 290 |

**设计权衡**：超车区段占比 > 40% 时，行程时间增加 19% 或速度降低 3.1 km/h（800 veh/h）。

### 减少视距需求的措施

- 降低设计速度
- 改善纵坡（减小坡度）
- 增加摩擦系数（路面处理）
- 拓宽路侧净区

## 02-平曲线设计（Horizontal Alignment）

### 基本公式

平曲线设计基于横向力平衡：

$$
R = \frac{V^2}{127(\mu + e)}
$$

其中 $R$ 为曲线半径（m），$V$ 为速度（km/h），$\mu$ 为侧向摩擦系数，$e$ 为超高率。

### 平曲线要素

- **圆曲线**：基本转向段
- **缓和曲线**：直线与圆曲线之间的过渡段，提供超高渐变
- **弯度（Bendiness）**：单位公里累计转角（°/km），用于评估路线弯曲程度

### 设计约束

$$
A_c = 12 - \frac{VISI}{60} + \frac{2B}{45} \quad \text{（单幅路）}
$$

$$
A_c = 6.6 + \frac{B}{10} \quad \text{（双幅路）}
$$

其中 $A_c$ 为线形约束，$B$ 为弯度，$VISI$ 为调和平均视距。

## 03-竖曲线设计（Vertical Alignment）

### 凸形竖曲线（Crest Curve）

最小长度由视距要求控制：

$$
L_m = \frac{A \times S^2}{120 + 3.5 \times S} \quad \text{（当 } S > L \text{）}
$$

其中 $A$ 为坡度代数差（%），$S$ 为所需视距（m）。

### 凹形竖曲线（Sag Curve）

最小长度由车辆前灯照射距离或乘客舒适度控制：

$$
L_m = \frac{A \times S^2}{120 + 3.5 \times S}
$$

### 竖曲线 K 值

DMRB 使用 K 值（曲率变化率）简化设计：

$$
K = \frac{L}{A}
$$

FOSD 超车视距对应的凹形竖曲线 K 值（120 km/h 设计速度）：400。

## 04-设计速度选择（Design Speed）

### 英国 DMRB 设计速度体系

设计速度与限速的关系：

| 限速 (mph) | 限速 (km/h) | 设计速度 (km/h) |
| --- | --- | --- |
| 30 | 48 | 60B |
| 40 | 64 | 70A |
| 50 | 80 | 85A |
| 60 | 96 | 100A |

设计速度应留有安全余量，使得 85% 驾驶员以设计速度或以下行驶。

### 三因素法

英国农村公路设计速度由三个因素确定：

1. **限速（Speed Limit）**
2. **布局约束（Layout Constraint, Lc）**：取决于道路类型、路侧宽度、接入频率
3. **线形约束（Alignment Constraint, Ac）**：取决于弯度和调和平均视距

通过 Lc-Ac 矩阵查表确定设计速度等级（70A/B ~ 120A/B）。

### 路侧宽度与接入频率

| 道路类型 | 车道宽 (m) | 接入频率 | 标准路侧宽 (m) |
| --- | --- | --- | --- |
| S2（单幅双车道） | 6.0 | L/M/H | 26/23/21 |
| WS2（宽单幅） | 7.3 | M | 19 |
| D2AP（双幅） | 7.3 + 7.3 | L | 10 |
| D3M（三车道高速） | 11 + 11 + 11 | L | 0 |

## 05-横断面设计

### 典型横断面要素

- **行车道（Carriageway）**：标准车道宽 3.65 m（National Highways）
- **硬路肩（Hard Strip/Shoulder）**
- **路侧（Verge）**：含排水、护栏、标志牌
- **中央分隔带（Central Reserve）**：高速公路
- **边坡（Slope/Berm）**

## 06-平纵组合设计

### 核心原则

H（水平）和 V（垂直）线形不应独立设计，必须协调配合。不良组合会增加驾驶员工作负荷，提高事故风险。

### 应避免的组合

- 长直线末端设急弯
- 凸形竖曲线顶部设急弯
- 陡坡/长坡底部或凹形竖曲线底部设急弯
- 凸形竖曲线后接凹形竖曲线（产生"跳跃"效果）
- 水平直线上的连续竖曲线变化（产生"驼峰"视觉）

### 良好实践

- 平曲线与竖曲线重合，且平曲线略长于竖曲线
- 交叉口处平纵曲线尽量平缓
- 确保平纵组合提供足够的超车视距（左弯 + 长凸曲线是典型不良组合）

## 07-设计标准层级

DMRB 三级设计标准：

1. **理想最小值（Desirable Minimum）**：高安全性和舒适度
2. **放宽值（Relaxations）**：设计师酌情使用，低于理想值若干步，仍符合标准
3. **偏离值（Departures）**：极端困难情况下使用，需监督机构批准，可能需增设警告标志

## 20-Coursework案例库

### Highway Engineering.xlsx 综合设计

课程综合设计练习涵盖：
- 给定设计速度，计算停车视距（SSD）
- 给定弯度和视距条件，计算布局约束（Lc）和线形约束（Ac）
- 通过 Lc-Ac 矩阵确定设计速度等级
- 比较计算设计速度与初始设计速度
- 平曲线最小半径计算
- 竖曲线最小长度计算

### Tutorial 练习题

每讲配套计算练习（Q1-Q5），涵盖 SSD/PSD 计算、平曲线半径、竖曲线K值等。

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| SSD 计算 | 给定 40 mph、3% 下坡 | SSD 公式应用、单位换算 |
| PSD 计算 | 两车道超车场景 | D1-D2-D3-C 分段计算 |
| 平曲线半径 | 给定设计速度和超高率 | R = V²/127(μ+e) |
| 竖曲线长度 | 给定坡度差和设计速度 | K 值法或 S-L 关系 |
| 设计速度选择 | 给定 Lc 和 Ac | DMRB CD109 查表 |
| 平纵组合判断 | 给定平面和纵断面 | 识别不良组合并给出改进 |

## 40-复习路线

1. **视距** → SSD 公式推导与计算 → PSD/OSD 分段计算 → DMRB 标准值记忆
2. **平曲线** → 圆曲线半径计算 → 弯度与线形约束 → 缓和曲线
3. **竖曲线** → 凸曲线视距控制 → 凹曲线舒适度控制 → K 值法
4. **设计速度** → 三因素法（限速/Lc/Ac）→ DMRB 矩阵查表
5. **平纵组合** → 不良组合识别 → 改进措施
6. **综合实操** → Highway Engineering.xlsx 完整流程

## 50-毕业论文与项目资料包补充

这批新增来源来自 `07-毕业论文与项目` 中的 Imperial CIVE2550 子文件夹，主要补充视距、平曲线、竖曲线、设计速度、DMRB 几何标准和一个 Excel 综合设计文件。该包更适合作为 [[Highway Geometric Design]]、[[Sight Distance]] 和 [[Design Speed]] 的课程复习补充，而不是单独拆成新课程。
