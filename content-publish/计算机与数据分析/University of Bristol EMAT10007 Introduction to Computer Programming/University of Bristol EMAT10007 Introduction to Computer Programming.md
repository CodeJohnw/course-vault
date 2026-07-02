---
type: course
course: University of Bristol EMAT10007 Introduction to Computer Programming
course_title: Introduction to Computer Programming
course_code: EMAT10007
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 计算机与数据分析
discipline_code: 11-计算机与数据分析
major: 计算机与数据分析
major_code: 11-计算机与数据分析
major_link: "[[计算机与数据分析]]"
knowledge_cluster:
  - programming-python
  - computational-modelling
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/11-计算机与数据分析/University of Bristol-EMAT10007-Introduction to Computer Programming
tags:
  - course/EMAT10007
  - school/university-of-bristol
  - discipline/computer-data-analysis
  - major/computer-data-analysis
---

# University of Bristol EMAT10007 Introduction to Computer Programming

## 00-课程总览

### 课程归属

- 学校：[[University of Bristol]]
- 学科方向：[[计算机与数据分析]] / [[计算机与数据分析]]
- 课程代码：[[EMAT10007]]
- 课程主题：[[Python Programming]]、[[Control Flow]]、[[Functions]]、[[Modular Programming]]、[[Object-Oriented Programming]]、[[NumPy]]、[[Computational Modelling]]、[[Curve Fitting]]、[[RMSE]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/11-计算机与数据分析/University of Bristol-EMAT10007-Introduction to Computer Programming`

### 课程定位

这门课是面向工程/数据背景学生的 Python 编程入门课。材料重点不是抽象计算机科学理论，而是把现实问题转换为可运行的计算模型：先理解问题中的变量、公式和约束，再用 Python 的数据类型、分支、循环、函数、模块和对象组织程序，最后用表格、图、误差指标和报告解释模型结果。

它和后续数据分析类课程的连接点主要在三处：一是 [[Python Programming]] 的基本语法能力，二是 [[Computational Modelling]] 的“现实问题 -> 数学表达 -> 程序实现 -> 输出解释”流程，三是 [[NumPy]]、曲线拟合和 [[RMSE]] 等科学计算工具。

### 课程材料地图

| 类别 | 主要内容 | 学习用途 |
| --- | --- | --- |
| 课程说明与评估 | 两个 coursework brief，分别覆盖 syntax test 和 building programs | 明确提交物、评分维度、可用包限制、报告要求 |
| 课件 | Week 3-9：loops、data structures、functions、arguments/scope、modules/importing、packages、classes、inheritance、NumPy | 建立 Python 语法和程序组织能力 |
| 练习与数据 | 机器人运动、分子式解析、房间加热、海平面、锂电池温度等数据/文本/流程图 | 把公式、数据和业务规则转为程序 |
| 代码与软件 | Coursework 1/2 的 Python 脚本和更新版本 | 复盘实现方式、调试和报告写作 |
| 待确认 | 一张微信图片 | 需人工确认是否为课程截图 |

## 01-Python 基础语法与程序结构

课程的核心评分维度之一是 data handling。程序不只是“算出答案”，还要能解释为什么选择某种数据结构。例如机器人运动题可以用 list 或 NumPy array 保存角速度、半径和时间序列；分子合成题需要用字符串、列表、字典存储元素符号和原子质量；海平面建模题需要用 CSV 表格、DataFrame 和数组保存年份与相对海平面。

[[Control Flow]] 主要出现在输入合法性检查和模型分支判断中。典型例子包括：分子式输入中系数必须是正整数、元素符号必须在表内、符号不能重复；海平面模型中根据 RMSE 决定使用线性或二次模型；锂电池温度中根据最高温度是否超过 60 摄氏度判断安全性。

机器人运动的基本公式是：

$$
v=r\omega
$$

其中 $r$ 是车轮半径，$\omega$ 是角速度。距离为：

$$
d=vt
$$

其中 $v$ 是线速度，$t$ 是运行时间。

## 02-函数、模块与可复用代码

[[Functions]] 是课程里最重要的 [[Modular Programming]] 工具。函数应当把一个清晰的小任务封装起来，例如 `calculate_distance`、`parse_molecule`、`temperature_at_point`、`rmse`、`battery_temperature`。作业报告中需要说明函数如何减少重复、降低调试难度，并让主程序保持清晰。

Coursework 1 只允许使用 `math` 包或自己写的包，目的是考察基础 Python 能力。Coursework 2 涉及数据分析和绘图，学生代码使用了 `pandas`、`matplotlib`、`scipy.optimize.curve_fit` 和 `numpy`，说明课程后半部分从纯语法转向科学计算。

## 03-面向对象与 NumPy

Week 7 的课件围绕 [[Object-Oriented Programming]]、classes 和 inheritance。对于这门课，面向对象不是为了复杂架构，而是帮助把 robot、battery、country model 这类“有属性、有行为”的计算对象组织起来。

[[NumPy]] 连接了基础 Python 和数值计算。它适合处理时间序列、空间网格和向量化计算。例如房间加热题要在 $10 \times 6$ 个点上计算温度，NumPy 可以减少嵌套循环并让公式更接近数学表达。

房间温度模型为：

$$
T(x,y)=\frac{T_{rad}-T_{air}}{\sqrt{1+(x-x_r)^2+(y-y_r)^2}}+T_{air}
$$

## 04-计算建模案例

分子质量的计算可以写成：

$$
M=\sum_{i=1}^{n} c_i m_i
$$

海平面可用线性或二次函数拟合：

$$
r(t)=it+j
$$

$$
r(t)=it^2+jt+k
$$

用 [[RMSE]] 比较模型：

$$
RMSE=\sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i-\hat y_i)^2}
$$

电池温度模型为：

$$
T(t)=T_{air}+\frac{R I(t)^2}{h_{air}}
$$

## 20-Coursework案例库

| Coursework | 任务结构 | 方法重点 | 报告重点 |
| --- | --- | --- | --- |
| Coursework 1 Syntax Test | 三个小题：机器人运动、分子合成、房间加热 | 基础语法、输入验证、循环、函数、公式实现 | 流程图；selection/repetition/modularity 说明；README 可运行性 |
| Coursework 2 Building Programs | 海平面预测、锂电池温度安全 | CSV 数据读取、曲线拟合、RMSE、绘图、阈值判断 | data handling、selection、repetition、modularity、correct output、best practice |

## 30-考试题型库

| 题型 | 典型语境 | 复习重点 |
| --- | --- | --- |
| 公式转程序 | 机器人、电池、房间加热 | 单位、变量定义、循环结构、输出格式 |
| 字符串解析 | 分子式输入 | 正则/拆分、输入验证、字典查表 |
| 科学计算 | 海平面拟合 | DataFrame、curve fitting、RMSE、模型选择 |
| 报告解释 | coursework documentation | data handling、selection、repetition、modularity |

## 40-复习路线

1. 用小例子复习变量、list、dict、if/else、for loop。
2. 把每个 coursework 公式先手算一组输入，再写成函数。
3. 对每个函数写最小测试，确认输出维度和单位。
4. 复习 NumPy/Pandas/Matplotlib 的最小工作流：读数据、拟合、画图、保存。
5. 最后补报告文字：每段都对应评分维度，不只描述代码做了什么，还解释为什么这样设计。
