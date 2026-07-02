---
type: course
course: Imperial College London CIVE60008 Transport Systems
course_title: Transport Systems
course_code: CIVE60008
school: Imperial College London
school_link: "[[Imperial College London]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 物流与供应链
major_code: 05-物流与供应链
major_link: "[[物流与供应链]]"
knowledge_cluster:
  - transport-systems
  - logistics-optimization
  - supply-chain-networks
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/07-毕业论文与项目/Imperial College London-CIVE60008-Transport Systems
tags:
  - course/CIVE60008
  - school/imperial-college-london
  - discipline/traffic-engineering
  - major/logistics-supply-chain
---

# Imperial College London CIVE60008 Transport Systems

## 00-课程总览

### 课程归属

- 学校：[[Imperial College London]]
- 专业方向：[[交通工程]] / [[物流与供应链]]
- 课程代码：[[CIVE60008]]
- 课程主题：[[Transport Systems]]、[[Network Algorithms]]、[[Mathematical Programming]]、[[Logistics]]、[[Supply Chain Networks]]、[[Facility Location Problem]]

### 课程定位

CIVE60008 是一门把 transport systems、network analysis、optimization 和 logistics/supply chain networks 串起来的课程。它不是单纯物流管理课，而是用算法和数学规划处理交通与供应链系统中的路径、网络、设施选址、聚类和容量配置问题。

### 母文件夹来源

`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/05-物流与供应链/Imperial College London-CIVE60008-Transport Systems`

### 课程材料地图

| 类别 | 内容 | 学习用途 |
| --- | --- | --- |
| 课件 | Week 01 Introduction to Transport、Week 02 Network Algorithms、Week 03 Mathematical Programming、Week 04 Introduction to Logistics、Week 05 Supply Chain Networks | 建立 transport systems 到 logistics networks 的知识主线 |
| 练习与数据 | network analysis tutorials、Dijkstra guidance、mathematical programming tutorial、Excel solver | 练习路径算法和优化建模 |
| 代码与模型 | Fibonacci/Python/Jupyter/MATLAB、week notebooks、PuLP notebooks | 复现算法、线性规划和供应链优化 |
| 阅读论文与参考 | CFLP、capacitated/general facility location、genfac | 支撑 facility location 和 supply chain network design |
| Coursework案例库 | data preparation and clustering、PuLP with E/P、coursework 数据包 | 形成从数据预处理、聚类到设施选址优化的完整案例 |

## 01-Transport Systems as Networks

课程第一周把 transport 放在 infrastructure、cities、people、freight 的交叉位置。交通系统可抽象为由 nodes、links、flows、costs 和 constraints 组成的网络。对物流而言，nodes 可能是仓库、港口、客户区、生产点；links 是道路、铁路、海运或配送通道；flows 是订单、货物、车辆或服务频次。

## 02-Network Algorithms

Network algorithms 用于在图结构中寻找路径、连通性和最小成本方案。最常见的最短路问题可写成：

$$
\min \sum_{(i,j)\in A} c_{ij}x_{ij}
$$

其中 $c_{ij}$ 是 link cost，$x_{ij}$ 表示路径是否经过该 link。Dijkstra algorithm 的核心思想是维护已确定最短距离节点和 loose ends，逐步扩展当前最小累计成本节点。

### 复习重点

- 图的节点、边、权重和路径；
- shortest path 与 least cost path；
- Dijkstra loose-end table；
- 算法实现中的 performance considerations；
- 交通网络和供应链网络之间的抽象一致性。

## 03-Mathematical Programming

Mathematical programming 将业务问题转化为 objective function、decision variables 和 constraints。课程以 blending problem 和 spreadsheet solver / Python notebook 引入线性规划。

一般线性规划形式：

$$
\max \; z = \sum_j c_jx_j
$$

$$
\text{s.t.}\quad \sum_j a_{ij}x_j \le b_i,\quad x_j\ge 0
$$

在 logistics 中，$x_j$ 可以表示发运量、设施是否开启、车辆分配或产品混合；$b_i$ 可表示容量、需求、预算或服务约束。

## 04-Introduction to Logistics

Logistics 关注物品、信息和资源从供应端到需求端的有效流动。Supply Chain Management 更强调跨企业、跨环节的协调：采购、生产、库存、运输、仓储、订单履约和客户服务。课程中 logistics 与 transport systems 的连接点在于：运输不是孤立成本项，而是库存、服务水平、设施布局和供应链韧性之间的 trade-off。

## 05-Supply Chain Networks and Facility Location

Supply chain network design 需要决定设施位置、服务范围、运输路径和容量配置。Capacitated Facility Location Problem (CFLP) 可写成：

$$
\min \sum_i f_i y_i + \sum_i\sum_j c_{ij}x_{ij}
$$

$$
\sum_i x_{ij} = d_j,\quad \sum_j x_{ij} \le K_i y_i,\quad y_i\in\{0,1\}
$$

其中 $y_i$ 表示设施 $i$ 是否开启，$x_{ij}$ 表示设施 $i$ 服务需求点 $j$ 的数量，$f_i$ 是固定开启成本，$K_i$ 是容量，$d_j$ 是需求。该模型连接课程中的 facility location 论文、PuLP notebook 和 coursework clustering。

## 20-Coursework案例库

### Data Preparation and Clustering

Coursework part 1 使用订单与区域数据，读取 `orders_regions.csv` 和 CFS area shapefile，按进口/出口、地区和货物类别聚合，形成空间数据分析基础。关键步骤包括：

1. 读取订单数据和地理边界；
2. 区分 import/export/domestic flows；
3. 按 DMS origin/destination 聚合；
4. 补齐区域编码并与 shapefile join；
5. 可视化区域需求或供给；
6. 使用 KMeans 等方法进行区域聚类。

### PuLP Optimization

Coursework part 2 使用 PuLP 建模，适合 facility location 或 allocation 问题。报告/代码应讲清楚：变量、目标函数、约束、求解器、结果解释，以及为什么该方案在成本、距离、容量或服务水平上更优。

## 30-题型库

| 题型 | 样题语境 | 复习重点 |
| --- | --- | --- |
| shortest path | 城市/物流网络路径选择 | Dijkstra table、link cost、path reconstruction |
| LP formulation | blending / allocation | objective、decision variables、constraints |
| facility location | warehouse/customer network | fixed cost、capacity、assignment、binary variable |
| clustering | order regions | features、KMeans、spatial interpretation |
| supply chain design | network redesign | cost-service trade-off、capacity、resilience |

## 40-复习路线

1. 先把 network abstraction 和 Dijkstra 算法讲清楚。
2. 用一个线性规划模板表达 blending/allocation 问题。
3. 掌握 CFLP 公式和变量解释。
4. 把 coursework 串成 data preparation -> clustering -> PuLP optimization -> result interpretation。

## 50-毕业论文与项目资料包补充

这批新增来源来自 `07-毕业论文与项目` 中的 Imperial CIVE60008 子文件夹，包含课件、coursework、试题、最终文件和大量 transport / logistics 参考包。它强化了 [[Network Algorithms]]、[[Mathematical Programming]]、[[Facility Location Problem]]、[[Supply Chain Networks]] 的案例属性。
