---
type: course
course: University of Bristol MENGM0038 Uncertainty and Risk Management
course_title: Uncertainty and Risk Management
course_code: MENGM0038
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 风险可靠性
discipline_code: 03-风险可靠性
major: 风险可靠性
major_code: 03-风险可靠性
major_link: "[[风险可靠性]]"
teacher: Professor Julian Booker
knowledge_cluster:
  - uncertainty-risk-management
  - reliability-analysis
  - quality-tools
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/University of Bristol-MENGM0038-Uncertainty and Risk Management
tags:
  - course/MENGM0038
  - school/university-of-bristol
  - discipline/risk-reliability
---

# University of Bristol MENGM0038 Uncertainty and Risk Management

## 00-课程总览

### 课程归属

- 学校：[[University of Bristol]]
- 专业方向：[[风险可靠性]]
- 课程代码：[[MENGM0038]]
- 课程主题：[[Uncertainty and Risk Management]]、[[Reliability Analysis]]、[[FMEA]]、[[Event Tree Analysis]]、[[Design of Experiments]]、[[Sensitivity Analysis]]、[[Quality Loss Function]]
- 教师线索：Professor Julian Booker

### 课程定位

这门课关注工程设计与质量管理中的 uncertainty、risk、reliability 和 decision-making。材料显示考试覆盖 Quality Loss、Design of Experiments、tube thickness / force calculation、Event Tree、FMEA、Pareto chart、Variance and Sensitivity Analysis，以及质量管理 tools and techniques。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/University of Bristol-MENGM0038-Uncertainty and Risk Management`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | MENG-M0038R Uncertainty and Risk Management PDF | 课程总体说明；主 PDF 加密，正文读取受限 |
| 课件 | URM section slides、Quality 4.0、probabilistic risk 等 | 构建不确定性、可靠性、风险与质量管理框架 |
| 练习与数据 | class exercises、templates、FMEA spreadsheets、FastFitter 工具 | 练习 FMEA、统计拟合、质量工具和风险分析 |
| 试题与评估 | Exam feedback、考试重做版、考试题材料 | 识别高频考试题型和常见失分点 |
| 作业案例库 | MENGM0038 报告、URM mindmap、材料汇总 | 建立答题框架和工具使用案例 |

## 01-Uncertainty and Risk Management Framework

Uncertainty 是工程系统中无法完全确定的输入、模型、环境、制造偏差或使用条件；risk 通常需要同时考虑事件概率和后果。课程的核心能力不是只会算概率，而是能选择合适的 risk management tool：当问题是产品质量偏差时用 quality loss；当问题是失效模式排序时用 FMEA/Pareto；当问题是事件序列时用 event tree；当问题是输入变量贡献时用 sensitivity analysis。

工程风险可写为：

$$
Risk = \sum_i P_i C_i
$$

其中 $P_i$ 是事件或失效场景概率，$C_i$ 是后果。实际报告中应说明概率和后果如何估计，以及不确定性来自数据、模型还是专家判断。

## 02-Quality Loss and Design of Experiments

考试反馈显示 Question 1 涉及 Quality Loss equation 和 Design of Experiments。Taguchi quality loss function 可写为：

$$
L(y)=k(y-m)^2
$$

其中 $y$ 是实际性能值，$m$ 是目标值，$k$ 是损失系数。这个公式强调“偏离目标即产生损失”，不是只有超出规格限才有质量问题。

DOE 答题不能只说“做实验”，要说明如何改进实验设计：factor selection、levels、replication、randomisation、blocking、interaction effects 和 response measurement。

## 03-FMEA, Pareto and Risk Mitigation

FMEA 用于识别 failure modes、effects、causes、controls 和 improvement actions。常用排序指标是 Risk Priority Number：

$$
RPN = S \times O \times D
$$

其中 $S$ 是 severity，$O$ 是 occurrence，$D$ 是 detection。考试反馈提示：很多人能列出 failure modes 并画 Pareto chart，但失分在没有说明如何降低评分主观性，以及没有提出 risk mitigation routes。

高质量 FMEA 应包括：

- 明确系统边界和功能；
- 每个 failure mode 对应 effect 与 cause；
- 评分标准一致，不随意给分；
- Pareto 用于识别优先处理对象；
- mitigation 应对应 severity、occurrence 或 detection 中的具体改进。

## 04-Event Tree and Sensitivity Analysis

Event Tree 适合描述初始事件后各防护层成功/失败的路径。路径概率是分支概率乘积：

$$
P(path)=\prod_k p_k
$$

考试反馈显示 Event Tree 常见问题是 branch 设置错误、概率分配错误和最终概率计算不完整。答题时先列 initiating event，再按 safety barrier 或 event sequence 从左到右展开，并确保每一层分支概率互补。

Sensitivity Analysis 关注输入变量对输出方差或风险结果的贡献。一个简单方差传播近似是：

$$
Var(Y) \approx \sum_i \left(\frac{\partial f}{\partial x_i}\right)^2 Var(X_i)
$$

其中 $Y=f(X)$。解释时要区分 parameter uncertainty、model uncertainty 和 measurement uncertainty。

## 20-作业案例库

可把课程案例组织成四类：

| 案例 | 方法 | 输出 |
| --- | --- | --- |
| 质量偏差 | Quality Loss / DOE | 损失计算、实验改进方案 |
| 系统失效 | FMEA / Pareto | failure modes、RPN 排序、改进措施 |
| 事故路径 | Event Tree | 分支路径、最终概率、关键屏障 |
| 输入不确定性 | Variance / Sensitivity | 关键变量、贡献度、设计建议 |

## 30-考试题型库

| 题型 | 高频要求 | 复习重点 |
| --- | --- | --- |
| Quality Loss | 计算损失或目标偏差 | $L(y)=k(y-m)^2$、单位与目标值 |
| DOE | 解释实验设计如何改进 | factors、levels、replication、interaction |
| Event Tree | 画树并算路径概率 | 分支互补、路径乘积、最终后果 |
| FMEA | 列 failure modes 并排序 | S/O/D、RPN、Pareto、mitigation |
| Sensitivity | 解释变量贡献 | 方差贡献、关键参数、管理含义 |

## 40-复习路线

1. 先把 Quality Loss、FMEA、Event Tree 三个工具的输入/输出记清楚。
2. 用考试反馈逐条对照常见失分点：概率树分支、FMEA 主观性、改进措施、DOE 解释。
3. 练习把任意工程系统写成 failure modes -> risk ranking -> mitigation -> residual risk。
