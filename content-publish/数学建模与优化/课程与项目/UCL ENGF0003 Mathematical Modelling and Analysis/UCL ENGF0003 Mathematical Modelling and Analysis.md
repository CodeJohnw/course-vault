---
type: course
course: UCL ENGF0003 Mathematical Modelling and Analysis
course_title: Mathematical Modelling and Analysis
course_code: ENGF0003
school: UCL
school_link: "[[UCL]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数学建模与优化
major_code: 09-数学建模与优化
major_link: "[[数学建模与优化]]"
level: Undergraduate / MSc support
assessment: coursework / modelling assignments
knowledge_cluster:
  - mathematical-modelling
  - sedis-model
  - social-contagion
  - numerical-simulation
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/UCL-ENGF0003-Mathematical Modelling and Analysis
tags:
  - course/ENGF0003
  - school/ucl
  - discipline/mathematical-modelling-optimization
  - major/mathematical-modelling-optimization
  - topic/mathematical-modelling
---

# UCL ENGF0003 Mathematical Modelling and Analysis


## 00-课程总览

- 学校：[[UCL]]
- 专业方向：[[数学建模与优化]]
- 课程代码：[[ENGF0003]]
- 课程主题：[[SEDIS Model]]、[[Dynamical Systems]]、[[Numerical Simulation]]、[[Fake News Spread]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/UCL-ENGF0003-Mathematical Modelling and Analysis`

该资产是 UCL mathematical modelling and analysis 项目包，主题是利用 SEDIS 模型分析虚假信息在社交媒体中的传播。材料包含 project release、student draft、task notebook、流程图、结果图和报告 PDF。

## 01-SEDIS 建模思路

SEDIS 类模型把人群分成不同状态，例如 susceptible、exposed、doubter、infected、stifler 等，并用状态转移描述信息传播。核心思想类似传染病动力学，但加入 doubters 后可以分析怀疑者对虚假信息传播峰值和持续时间的影响。

典型 compartment model 可写为：

$$
rac{dS}{dt}=-eta SI,\quad rac{dI}{dt}=eta SI-\gamma I
$$

SEDIS 会在此基础上加入更多状态和转移率，用于表达怀疑、遗忘、传播和停止传播。

## 20-Coursework案例库

报告应包含模型假设、变量定义、参数解释、数值模拟、情景对比、图像解释和局限讨论。Notebook 结果图如 impact of doubters 可直接服务于 conclusion，但需要用文字解释政策含义。
