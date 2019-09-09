---
title: 高等物理实验教程
date: 2019-06-22 15:12:35
categories: Research
tags: 实验
---
<p></p>
<center>2016 张渝宁</center>

Code for modeling and data analysis of PHYS128 AL. For Demonstration.

@ 材料来自 UC Santa Barbara PHYS 128AL 高等物理实验

教科书-实验误差分析：
Bevington.pdf & Taylor.pdf

文件夹：
- ./Mathematica_Sample/ 包含Mathematica的画图实例。
- ./Experiment#/code/ 代码，用于数据分析和基本计算画图。包含Mathematica(.nb)和Python Jupyter Notebook(.ipynb)的计算笔记本。
- ./Experiment/data/ 原始实验数据

实验类型：
1. Experiment1: 卡文迪许扭称实验 
2. Experiment2: 密立根油滴实验
3. Experiment3: 海平面mu介子寿命和通量测量
4. Experiment4: 使用云室观察alpha散射

Experiment# 文件夹下相关与实验名称相同的pdf为实验的介绍文档，Lab_Report.pdf 为最终实验报告（无本地文件，使用Overleaf在线完成），Lab_Note为实验过程中所做的笔记（对于复现实验来说非常重要）。



鉴于官网还没人维护，鸽了几个月的实验Post就先写在这里了



## 1. 实验设计和物理原理
设计实验之前一定要对研究目标和背景理论有清晰的认知，理论准备充分才能有良好的实验设计。
**当你可以清晰地用白板presentation展示出**
- 基本理论
- 你希望测量的物理量
- 实验设计（set up）和技术细节
- 数据处理方式和可能误差
- 实验的核心创意和亮点

**的时候，你距离一个优秀的物理实验就不远了。**

![Presentation](/asset/images/presentation.png)

通常团队合作对于实验设计非常重要，因为实验设计依赖综合性的知识背景和能力（物理，工程经验，机械和电子技术，代码和编程），
而且实验仪器的构建需要不同领域的工程师和科学家合作。团队沟通，设计论证对于实验来说非常重要。

实验是一个迭代的过程，一个良好的实验设计通常是在反复尝试，不断试错和debug过程中逐渐形成的。比起物理理论本身，实验更像是工程学，因为其更依赖经验和实践反馈而不是科学直觉。


### 设计基本原则：
- 原理清晰，简单（大大简化计算误差传递的过程）
- 减小误差，通过设计规避或者消除噪声（例如扭称实验）
- **数据获取自动化**，尽可能使用传感器和数字电路（极大的减少工作量并提高效率，让你的时间专注在有意义的事情上）


了解并欣赏经典实验设计可以给你的实验提供良好的直觉，例如Cavendish使用扭称规避地球引力并通过多次转化放大物理量（LIGO测量引力波其实是同样思路），或者Millikan通过操作电场中的带电油雾观察到电荷的量子化特性（Stern-Gerlach实验展现自旋量子性）。



参考 
- [Wiki: Millikan Experiment](https://en.wikipedia.org/wiki/Oil_drop_experiment)
- [Wiki: Cavendish Experiment](https://en.wikipedia.org/wiki/Cavendish_experiment)
- [知乎：引力波探测的原理](https://www.zhihu.com/question/24079693/answer/38549900)

## 2. 实验仪器搭建
这是一个工程师的话题，如果你不能找到程序员，机械工程师，电子电气工程师帮助你实现实验装置，那就自己学吧，你会发现你秃了也变强了（#滑稽），祝好运。

还是那句话，团队对于实验来说非常重要，（想象一下CERN或者LIGO的几千人实验组），最重要的原因就是团队分工和合作可以提高效率（人类作为社会性动物的根本优势）。

![LIGO 团队](/asset/images/LIGO_group.jpg)

最简单的例子：
- A同学搭建实验仪器的机械结构，
- B同学构建测量电路，
- C同学负责代码和数据处理，
- D同学负责整体设计和理论误差分析。


当然对于小团队来说，分工绝对不是明确的，每个人一定要对彼此的工作有一定的了解（50%以上）才能有效地沟通合作。而且最好的合作是并行式的（Parallel-并联电路）而不是序列式的（Sequential-串联电路），不要以为你是一个程序员就可以在你的队友搭电路的时候袖手旁观。


同样，记住工程和技术只是为你的实验服务的，你的焦点在于如何快速实现实验设计而不是工程细节（比如这个PCB是怎么做出来的，为什么这个焊点又掉了），再一次强调快速学习能力的重要。快速地开始你的实验搭建，边做边学，反复迭代试错是最好的实践模式。如果你要学完一整本数字电路和单片机系统（或者Python数据分析和可视化）之后才开始搭建实验仪器（分析实验数据），大概你只能参加下一届CUPT了（不，真相是你到了毕业都学不完的，没错哪怕是研究生毕业#滑稽）。


不会就问，尽可能的利用网络和实验室的各种资源（学长，指导老师，各种文件资料）快速学习，这样你才有可能在一个月里搞定这些题目。


参考
- [实验室里用的仪器，都是科学家自己设计的吗？](https://daily.zhihu.com/story/9168349)
- [Building Scientific Apparatus](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/John%20H.%20Moore%2C%20Christopher%20C.%20Davis%2C%20Michael%20A.%20Coplan%2C%20Sandra%20C.%20Greer%20-%20Building%20Scientific%20Apparatus%20(2009%2C%20Cambridge%20University%20Press).pdf) -ps: 这本书可以当字典用，不会就查，看完是不可能看完的 



## 3. 实验过程
**实验过程是非常重要的！！！！！！！**
**实验笔记（LAB NOTE）是非常重要的！！！！！**

千万不要以为你的实验设计完了就高枕无忧了，独立设计实验跟国内大学手把手跟着做实验课完全是两码事！就算是你已经有了完整详细的实验手册（当然这是不可能的），实验依然是一个非常非常容易出BUG的环节。任何一个细节的失误，例如一根搭错的电线，一个型号不对的电容（**请参考0.1uF学弟何同学的光荣事迹**），都足以葬送你的整个实验观测。当Debug一个月头都秃了之后你最终发现了问题的原因，心里面的mmp是一定忍不住的。

为了避免这样的故事，请一定在实验中秉承严谨认真的态度，留意每一个细节。同时使用**实验记录**来保存实验的第一手资料，**这一点非常重要**。


实验记录应该包含：
- 基本的原始信息，实验时间，合作队友等。
- 实验细节，例如相关仪器参数，环境参数
- 实验基本操作，例如 1.测量了哪些物理量，2.装置调节过程和方法，参数设置 
- 原始数据和基本的演算，对初步结果的评估
- 实验中遇到的问题和bug，以及相关分析
- 对误差的评估，以及减小误差的思路


总之实验记录源于工程实践的经验，就像是工程中的开发文档，测试记录。
301之前这一方面做的很差，因为完全没有意识。大量的第一手计算手稿都是随手一划，惨遭丢弃。实验进程全靠反复试错后的个人经验积累，效率低下。实验记录也是在国内本科生的实验课程体系中是几乎被忽视的一个环节，因为详实可靠的实验记录需要很高的时间成本。但实际上磨刀不误砍柴工，经过系统整理的实验报告，可以大大提高你的效率：

![Lab Note 举例](/asset/images/labnote.jpg)

- 有效降低实验失误的几率，避免了大量无谓的debug和重复实验的时间。
- 可以从过去的实验笔记中不断总结问题，并且改进实验设计
- 还原实验细节，提供可复现性，即便出问题也可以加快debug进度
- 展示和报告，你可以通过原始试验记录快速构建实验报告或者presentation

实验记录举例
- [Muon Lab Note](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/Experiment3/Muon_Lab_Note.pdf)
- [卓越杯摸鱼记录](https://github.com/Neuromancer43/Ultraino/blob/master/Test_Log/test_log.txt)


参考
- [MIT: How to use your Lab Notebook](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/labnotebooks.pdf)
- [NIH: Keeping a Lab Notebook](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/Lab_Notebook_508_(new).pdf)

## 4. 数据处理和误差分析

数据处理的目的在于通过数据检验你的理论是否正确，简单来说就是通过数据计算某些理论可预测量，并进行对比。
例如，引力常数测量值 
<a href="https://www.codecogs.com/eqnedit.php?latex=$(6.68\pm&space;0.21)&space;\times&space;10^{-11}$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$(6.68\pm&space;0.21)&space;\times&space;10^{-11}$" title="$(6.68\pm 0.21) \times 10^{-11}$" /></a> 
对比实际值
<a href="https://www.codecogs.com/eqnedit.php?latex=$&space;6.67048&space;\times&space;10^{-11}$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$&space;6.67048&space;\times&space;10^{-11}$" title="$ 6.67048 \times 10^{-11}$" /></a>。

*计算误差是数据处理最容易被忽视的部分，也是物理实验最重要的部分，没有误差和不确定度的测量结果毫无意义。*

实验的可信度完全来自误差的分析，例如可能你的测量非常精确，与理论标准值仅差距0.01% ，但标准值却在测量的3 sigma范围之外，这仍然说明你的测量存在系统误差，实验设计并不合理。或者你的结果与实验非常接近，但是测量标准差非常大，可能是差距的五到十倍，那很有可能这次测量只是运气的结果。总之，请一定注意**严谨的误差讨论是实验的灵魂。**

参考: 
[科学中的5 sigma 原则](https://blogs.scientificamerican.com/observations/five-sigmawhats-that/?redirect=1)

那么如何处理数据并进行误差分析？
通常使用Python工具栈数据处理是最高效的，目前科学界的主流数据分析工具是**Jupyter Notebook**。
如果你以后有志于学术界，那么这项技能是**必备**的（有意见认为Jupyter将是下一代数字化科技论文的标准格式）。
这里就体现出了自动化数据记录的重要性——如果你是用传感电路获取数据，那么你的计算过程将非常简单愉快。

例如 Python 笔记本（原始文件位于本库同名文件夹
）：
- [Muon 数据分析](https://nbviewer.jupyter.org/github/Neuromancer43/Advanced-Laboratory/blob/master/Experiment3/Muon_Physics.ipynb)
- [Millikan 数据分析](https://nbviewer.jupyter.org/github/Neuromancer43/Advanced-Laboratory/blob/master/Experiment2/Millikan_Droplet.ipynb)
- [Cloud Chamber 数据分析](https://nbviewer.jupyter.org/github/Neuromancer43/Advanced-Laboratory/blob/master/Experiment4/Cloud%20Chamber.ipynb)

当然，你也可以使用Mathematica Notebook来分析实验数据，或者进行基本的误差分析（Error Propagation）
- [Cavendish 数据分析](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/Experiment1/expriment_1.nb)

当然，如果你需要解微分方程或者引入物理学常数，那么通常Mathematica是更好的选择（简单快速，熟练），但是实际上Python的Sympy(Symbolic Python)包可以提供同样可靠的计算机代数系统。关于科学计算的更多消息请移步网站相关帖子。
参见
- [Wiki: Project Jupyter](https://en.wikipedia.org/wiki/Project_Jupyter)
- [Anaconda科学计算环境](https://www.anaconda.com/distribution/)

![](https://jupyter.org/assets/jupyterpreview.png)

实验数据分析通常包括
- 导入格式化数据（csv,tsv,txt,xlsx）等等
- 进行基本处理，例如求平均值，做差，聚类，线性回归等等
- 将处理过的数据带入你的理论模型（通常是一个公式，或者数值微分方程，带入数据和参数计算你需要的结果）
- **使用误差传递公式，计算测量误差和不确定度**

参考：[Wiki: 不确定度传递](https://en.wikipedia.org/wiki/Propagation_of_uncertainty)


不同形式实验数据的误差大不相同，这取决于具体的实验和理论，如果模型中最终有积分或者曲线拟合这样的操作，那么简单的线性误差公式就不再适用。
例如，计数数据的不确定度是<a href="https://www.codecogs.com/eqnedit.php?latex=\sqrt{N}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\sqrt{N}" title="\sqrt{N}" /></a>。而曲线拟合的不确定度通常可由程序得出[StackOverflow: Getting standard errors on fitted parameters using the optimize.leastsq method in python](https://stackoverflow.com/questions/14581358/getting-standard-errors-on-fitted-parameters-using-the-optimize-leastsq-method-i)。

更多关于数据分析和不确定度的讨论请见参考书
- [An Introduction to Data Analysis-Taylor](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/Taylor.pdf)
- [Data Reduction and Error Analysis-Bevington](https://github.com/Neuromancer43/Advanced-Laboratory/blob/master/Bevington.pdf)

暂时到这，原文挂在[我的Github上](https://github.com/Neuromancer43/Advanced-Laboratory)，如果各位学弟学妹有问题欢迎在Issue部分提问，顺带求点赞（Star）+关注（Follow）#滑稽。


June.4th at University of California, Santa Barbara

