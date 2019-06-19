---
title: 计算与数据科学入门
date: 2018-12-11 13:08:11
categories: Technology
tags: 科学计算
---

2016张渝宁


首先声明-
**我们是Scientist！科学家！! 不是程序猿！**

我们使用完全不同的工具集和方法论，并且着眼于完全不同的目标。
对科学家而言，代码和软件只是解决问题的工具，而非目的本身。

参见
[科学计算的程序编写和通常所说的码农的编程有多大的区别？](https://www.zhihu.com/question/33515914/answer/57060509)



鉴于这一领域的知识实在过于庞大,在此仅作简单介绍汇总,希望大家有一个简略的印象.

## 那些写代码的科学家在干什么？

百科
[Wikipedia: Scientific-Computation](https://en.wikipedia.org/wiki/Computational_science)
[Wikipedia: Copmputational-Physics](https://en.wikipedia.org/wiki/Computational_physics)

ps: 英文阅读有困难请在wiki中选择中文

如果你选修过数学实验这门课程，你大概已经对这个领域有所了解。随着计算机科学的不断发展，**计算**已经成为了现代科研体系中与**实验**和**理论**并列的第三大研究范式。这是数学-物理-计算机的交叉处，主要实践是科学家和工程师通过编写程序处理实验或者测试数据，或进行数值分析来解决研究或工程实践中的复杂问题。


![ATLAS 对撞机](/asset/images/atlas-collider.jpg)

驱动这一领域发展的动力如下
1. 科研中面临的问题非常困难以至于很难通过传统数学分析求解（例如，流体力学，量子化学，非线性动力系统-天气系统、三体系统）。机器可以做到人类做不到事情（解偏微分方程，不需要数学物理方法，只需要算法）。
2. 现代研究中不断膨胀的数据量，无法再手动处理。（例如，CERN欧洲核子碰撞中心使用机器学习从TB级数据中检测Higgs粒子，或者LIGO天文台从TB级的天文数据中寻找引力波）
3. 将大部分工作流程自动化，极大提高工作效率。让科研狗有时间和妹子约会 XD。（误）

**简而言之，现代研究遇到的大多数问题都及其复杂，只靠人类大脑的计算处理能力已经捉襟见肘。因此科学家理所当然地借助人类有史以来发明的最为强大的生产力工具-计算机，计算和编程是每一个现代科研工作者所必须掌握地基本技能。**


## 你可以用计算机做什么？

首要功能当然是让自己看起来很Cooooooooool（逃）
![](/asset/images/code-monkey.png)

事实上**你从课本中学到的所有数学分析方法都有对应计算工具。有数学的地方就有计算,研究的每一步都会用到大量的计算和分析,用到代码**

### 1. 数据分析 

*Mathematical Statistics*

- 数据处理（去除错误数据，滤波，插值等等）
- 数据分析（相关性，因果性，统计数值特征，回归，拟合）
- 数据可视化（眼见为实，给出物理图像和直觉）

基本包含数理统计的所有工具，指标和特征分析，回归拟合，可视化，特征提取

### 2. 科学计算

*Mathematical Analysis*

- 数值计算 (插值 拟合 数值求解微分/偏微分方程 数值积分/微分 优化 随机过程模拟)
- 符号计算 (自动化公式推导 符号微分/积分 级数展开分析 微分方程求解)

基本包含数学分析的所有工具（微积分，级数和递归，微分方程，频谱分析）

## 我需要使用什么样的科学计算工具？

本章节所用到的所有计算工具都强大且复杂，完整的掌握任意之一都需要多年的学习时间和专业知识，**后续会有更多Post对每一种工具进行详细介绍。**

**Recommended**
### [Mathemtaica"](http://www.wolfram.com/mathematica/)
地表最强数学软件没有之一，物理系圣剑，优势在于微分方程和符号计算，以及良好的可视化
- [知乎： Mathematica有多厉害](https://www.zhihu.com/question/27834147/answer/38337425)
- [学习： Wolfram U](http://www.wolfram.com/wolfram-u/)
- [学习： Elementary Language Introduction](http://www.wolfram.com/language/elementary-introduction/2nd-ed/?source=nav)
- [Wolfram Alpha](http://m.wolframalpha.com/)

### [Python"](https://www.python.org/) 
Anaconda科学计算发行版，学界和产业界的主流通用科学计算解决方案，优势在于通用计算，可以完全取代MATLAB

- [Python: Anaconda](https://www.anaconda.com/)
- [The Wonderful World of Scientific Computing with Python | SciPy 2014](https://www.youtube.com/watch?v=A9tv7WBIwyM)
- [Edx: Introduction to computational thinking](https://www.edx.org/course/introduction-computational-thinking-data-mitx-6-00-2x-7)
- [Coursera: Computational Thinking for Problem Solving](https://www.coursera.org/learn/computational-thinking-problem-solving)

### Microsoft Excel
小学生都可以玩的溜的数据处理，快速数据分析，可视化。Python（Pandas）和Mathematica支持对XLSX文件进行分析。
实际上专业数据和计算软件的复杂功能和特性很少会用到，Excel才是日常记录实验数据使用最多的工具。

- [Edx: Analyzing and Visualizing Data with Excel](https://courses.edx.org/courses/course-v1:Microsoft+DAT206x+1T2018/course/)
- [知乎：Excel Top Answers](https://www.zhihu.com/topic/19567930/top-answers)

### [COMSOL"](https://www.comsol.com/comsol-multiphysics)
多物理场有限元模拟（FEM Simulation）领域顶级商业软件，功能非常强大。正版价格及其昂贵。

- [官网：COMSOL学习中心](https://cn.comsol.com/learning-center)
- [官网：多物理场百科](https://cn.comsol.com/multiphysics)

**Optional**
### [C/C++"](http://www.mingw.org/) 
最为广泛使用的高级语言，全面的第三方库，高性能计算/并行计算
C/C++的在CUPT中应用并不广泛，实际科研中主要用于计算密集型任务的工具库的底层开发，顶层封装基本使用Python

### [MATLAB/Octave"](https://www.gnu.org/software/octave/)
不用多说，大家都懂，数值计算，实际上更多的是画图工具

### [Origin"](https://www.originlab.com/)
科学绘图软件，出版物级别的数据绘图

### [Julia"](https://julialang.org/)
新兴的高性能科学计算语言，语法介于Fortran和Python之间，具有媲美C/Fortran的速度


## 如何提高编程和计算能力？

请执行如下命令
```
while True:
    practice()
```
**Talk is cheap, show me the code!**

计算机是实践学科，在研究实践中用各种程序工具帮你解决棘手的问题，用自动化的代码帮你节省时间是最好的学习方式。
懒是驱动编程能力进步的第一动力，让计算机帮你做事，然后享受敲代码的快乐。

To be continue...




