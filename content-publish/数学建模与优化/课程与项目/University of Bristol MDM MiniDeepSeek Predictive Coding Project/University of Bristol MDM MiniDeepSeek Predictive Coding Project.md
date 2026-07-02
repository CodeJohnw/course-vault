---
type: project
course: University of Bristol MDM MiniDeepSeek Predictive Coding Project
course_title: MiniDeepSeek Predictive Coding Project
course_code: MDM
project: University of Bristol MDM MiniDeepSeek Predictive Coding Project
project_title: MiniDeepSeek Predictive Coding Project
school: University of Bristol
school_link: "[[University of Bristol]]"
discipline: 数学建模与优化
discipline_code: 09-数学建模与优化
major: 数学建模与优化
major_code: 09-数学建模与优化
major_link: "[[数学建模与优化]]"
knowledge_cluster:
  - predictive-coding
  - neural-network
  - poisson-model
  - machine-learning
source_parent_folder: /Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Bristol-MDM-MiniDeepSeek Predictive Coding Project
tags:
  - school/university-of-bristol
  - discipline/mathematical-modelling-optimization
  - major/mathematical-modelling-optimization
  - project/predictive-coding
---
# University of Bristol MDM MiniDeepSeek Predictive Coding Project


## 00-项目总览

- 学校：[[University of Bristol]]
- 项目代码：[[MDM]]
- 专业方向：[[数学建模与优化]]
- 关联知识点：[[Predictive Coding]]、[[Neural Networks]]、[[Poisson Model]]、[[Machine Learning]]
- 母文件夹来源：`/Users/johnwong/Documents/00 Course File/03-专业课程/09-数学建模与优化/University of Bristol-MDM-MiniDeepSeek Predictive Coding Project`

该项目以 MiniDeepSeek / predictive coding 为主题，包含 notebook、神经网络文本、项目 PDF、脑图、课堂截图和 Nature Neuroscience 相关参考材料。它适合作为“从生物启发学习机制到小型神经网络实验”的项目案例。

## 01-建模重点

Predictive coding 的核心思想是模型不断预测输入，并用 prediction error 更新内部表示。抽象形式可以写成：

$$
\epsilon = y - \hat{y}
$$

其中 $y$ 是观测输入，$\hat{y}$ 是模型预测，$\epsilon$ 是预测误差。训练过程围绕最小化误差或能量函数展开。

## 20-案例库

Notebook 适合按 neural network、Poisson、predictive coding 三条线复盘：先解释模型结构，再展示训练/推断过程，最后说明它与 backpropagation 或生物可塑性学习的关系。
