---
type: course
course: KTH Royal Institute of Technology ID2218 Design of Fault-Tolerant Systems
course_title: Design of Fault-Tolerant Systems
course_code: ID2218
school: KTH Royal Institute of Technology
school_link: "[[KTH Royal Institute of Technology]]"
discipline: 风险可靠性
discipline_code: 03-风险可靠性
major: 风险可靠性
major_code: 03-风险可靠性
major_link: "[[风险可靠性]]"
teacher: Elena Dubrova
knowledge_cluster:
  - fault-tolerant-systems
  - digital-reliability
  - redundancy-coding
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/KTH Royal Institute of Technology-ID2218-Design of Fault-Tolerant Systems
tags:
  - course/ID2218
  - school/kth
  - discipline/risk-reliability
---

# KTH Royal Institute of Technology ID2218 Design of Fault-Tolerant Systems

## 00-课程总览

### 课程归属

- 学校：[[KTH Royal Institute of Technology]]
- 专业方向：[[风险可靠性]]
- 课程代码：[[ID2218]]
- 课程主题：[[Fault-Tolerant Systems]]、[[Fault Detection Coverage]]、[[Stuck-at Faults]]、[[Triple Modular Redundancy]]、[[Markov Reliability Model]]、[[Berger Code]]、[[Redundancy]]
- 教师/教材线索：Elena Dubrova, Fault-Tolerant Design

### 课程定位

ID2218 是面向计算机/嵌入式系统的 fault-tolerant systems design 课程。材料覆盖教材、course material、assignment 1/2/4/5、final exam 2020、fault detection coverage、stuck-at faults、TMR、hot standby redundancy、Markov reliability evaluation 和 Berger code 等容错编码技术。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/03-风险可靠性/KTH Royal Institute of Technology-ID2218-Design of Fault-Tolerant Systems`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课件与教材 | Fault-Tolerant Design textbook、ID2218 course material | 建立系统化容错设计知识框架 |
| 练习与作业 | assignment 1/2/4/5、solutions、辅导要求 | 练习覆盖率、冗余、编码和可靠性计算 |
| 试题与评估 | Final exam 2020、solutions、期末知识点 | 建立考试题型矩阵 |
| 阅读论文与参考 | Berger code、embedded systems fault tolerant techniques | 支撑编码与嵌入式系统容错 |

## 01-Fault Model and Detection Coverage

Final Exam 2020 第一题考 single stuck-at faults 和 test set 的 fault detection coverage。Coverage 可写为：

$$
C = \frac{N_{detected}}{N_{total}}
$$

其中 $N_{detected}$ 是测试集能检测出的故障数，$N_{total}$ 是考虑的总故障数。设计简单等价逻辑电路时，要注意有些冗余逻辑会制造 undetectable faults。

## 02-Reliability and Mission Time

若模块寿命服从指数分布，单模块可靠度为：

$$
R(t)=e^{-\lambda t}
$$

其中 $\lambda=1/MTTF$。考试中出现 controller MTTF、mission time 和 TMR 配置比较。理想 voter 下 TMR 可靠度为：

$$
R_{TMR} = 3R^2 - 2R^3
$$

该式表示 3 个模块中至少 2 个正常即可工作。解题时先算单模块在 mission time 下的 $R$，再代入 TMR，最后比较 mission reliability 是否下降。

## 03-Redundancy, Standby and Markov Reliability

Hot standby redundancy 的可靠性可通过 Markov chain 表达。状态通常表示系统中可用模块数量，转移包括 module failure、repair team repair、switch failure 等。考试题给出 5 modules、failure rate $\lambda$、repair rate $\mu$、2 repair teams、switch failure rate $\lambda_s$ 和 perfect coverage。

建模步骤：

1. 定义状态：例如 5、4、3、2、1、0 个可用模块，以及 switch failed absorbing state；
2. 标注 failure transition：$n\lambda$；
3. 标注 repair transition：$\min(5-n,2)\mu$；
4. 加入 switch failure：$\lambda_s$；
5. 判断系统 failure threshold。

## 04-Coding and Fault-Tolerant Techniques

参考资料包含 Berger code based fault-tolerant techniques。编码容错的核心是用 redundancy 检测或纠正数据错误，例如 parity、checksum、Hamming code、Berger code。Berger code 常用于检测 unidirectional errors，即所有错误位朝同一方向翻转。

容错设计的基本 trade-off：

- hardware redundancy 提高可靠性但增加面积、功耗和成本；
- information redundancy 增加编码/校验开销；
- time redundancy 重复计算但增加延迟；
- software redundancy 增加复杂度和验证负担。

## 20-作业案例库

作业材料可分为：

| 作业/材料 | 核心主题 | 复习用途 |
| --- | --- | --- |
| Assignment 1 | stuck-at faults / coverage | 练 test set 和逻辑电路覆盖率 |
| Assignment 2 | redundancy / reliability | 练可靠度公式和系统结构 |
| Assignment 4/5 | fault-tolerant techniques | 练编码、冗余或 Markov 模型 |
| Final exam 2020 | 综合题 | 建立最终考试题型模板 |

## 30-考试题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| stuck-at coverage | logic circuit and test set | detected/total、minimal test set |
| TMR reliability | controller mission time | exponential reliability、TMR formula |
| Markov chain | hot standby with repair teams | states、failure/repair transition rates |
| coding | Berger code / embedded systems | unidirectional errors、redundancy overhead |
| design trade-off | fault-tolerant architecture | cost、coverage、latency、power |

## 40-复习路线

1. 先掌握 stuck-at fault coverage 的枚举方法。
2. 熟悉 $R(t)=e^{-\lambda t}$ 和 TMR 可靠度公式。
3. 能为 standby redundancy 画 Markov chain。
4. 准备 Berger code、redundancy 类型和容错设计 trade-off。
