---
type: dissertation
dissertation: University of Leeds Dissertation Bottleneck Road User Behaviour and Tolling
dissertation_title: Bottleneck Road User Behaviour and Tolling
school: University of Leeds
school_link: "[[University of Leeds]]"
discipline: 交通工程
discipline_code: 02-交通工程
major: 毕业论文与项目
major_code: 07-毕业论文与项目
major_link: "[[毕业论文与项目]]"
knowledge_cluster:
  - bottleneck-model
  - departure-time-choice
  - congestion-pricing
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/07-毕业论文与项目/University of Leeds-Dissertation-Bottleneck Road User Behaviour and Tolling
tags:
  - dissertation/bottleneck-tolling
  - school/university-of-leeds
  - discipline/traffic-engineering
  - major/dissertation-project
---

# University of Leeds Dissertation Bottleneck Road User Behaviour and Tolling

## 00-项目总览

- 学校：[[University of Leeds]]
- 专业方向：[[交通工程]] / [[毕业论文与项目]]
- 关联专题：[[Bottleneck Road User Behaviour and Tolling Case]]
- 关联知识点：[[Bottleneck Model]]、[[Departure Time Choice]]、[[Road Pricing]]、[[User Equilibrium]]、[[Social Optimum]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/02-交通工程/07-毕业论文与项目/University of Leeds-Dissertation-Bottleneck Road User Behaviour and Tolling`

该 dissertation 资产研究早高峰瓶颈道路上的用户行为、出发时间选择、同质/异质用户差异和动态收费策略。材料包含 Jupyter notebooks、LaTeX、文献综述、论文结构和多个论文版本。

## 01-理论基础

经典 Vickrey bottleneck model 假设所有通勤者希望在同一理想到达时间到达目的地，瓶颈容量固定，若出发率超过瓶颈服务率便形成排队。出行总成本：

$$
C(t,x)=lpha(x)T(t)+eta(x)SDE(t)+\gamma(x)SDL(t)+Toll(t)
$$

队列演化：

$$
rac{dD(t)}{dt}=r(t)-s
$$

其中 $D(t)$ 是队列长度，$r(t)$ 是到达瓶颈的出发率，$s$ 是瓶颈通行能力。

## 02-研究目标

对比同质用户与异质用户行为，分析 user equilibrium 与 social optimum 的成本差异，研究动态收费如何重新分配出发时间，降低排队延误和社会总成本。

## 20-案例库

本笔记作为 dissertation 版本；通用模型和代码素材继续挂接到 [[Bottleneck Road User Behaviour and Tolling Case]]。
