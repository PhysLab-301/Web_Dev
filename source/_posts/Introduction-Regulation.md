---
title: 网站介绍 & 文档规范建议
date: 2018-10-08 13:51:11
categories: 运营维护
tags: 操作规范
---
# PhysLab@301介绍

## 设计目标：
1. 各类文档的归纳整理
2. 实验室数字和实体资源集中整合
3. 纳新，宣传和引导

## 计划内容：
- 各类比赛档案，代码，ppt
- 技术总结，经验分享
- 运营，维护的规范建议
- 成员个人体验，经历

## 技术架构

**关键词：建立网站，Web开发**

[知乎-如何搭建个人网站](https://www.zhihu.com/question/19774219)
[简书-VPS部署Hexo网站](https://www.jianshu.com/p/5cf20649f328)
相关知识技术背景请移步CS专业，ps：希望301每年都有程序员做技术维护。。。

- VPS：[Bandwagon](https://bandwagonhost.com)
- 域名购买：[NameCheap](https://www.namecheap.com/)
- DNS解析：[DNSPod](https://www.dnspod.cn/)
- 博客框架：[Hexo](https://hexo.io/zh-cn/)
- 自动部署：[git](https://git-scm.com/)
  
## 如何更新博客

### 书写
[如何使用Hexo写作](https://hexo.io/zh-cn/docs/writing)，Markdown了解一下**

修改 About 部分的宣传文章请编辑source/about/index.md
其余主页栏为hexo主题自动生成

### 设置
请在项目源路径下编辑_config.yml文件，参见[如何配置博客]](https://hexo.io/zh-cn/docs/configuration)

同理，配置页面视觉效果请修改对应主题的相应配置文件_config.yml

### 部署
[Hexo博客部署](https://hexo.io/zh-cn/docs/deployment.html)

请在301主机使用命令行
```
hexo clean
hexo g
hexo d
```
VPS添加了301主机的[SSH公钥](http://www.ruanyifeng.com/blog/2011/12/ssh_remote_login.html)，`hexo d` 
将调用githook自动部署

### 附注
维护技术问题可联系301相关学长

# 文档规范建议

## 专业&技术性文案

**简洁，客观，专业**

- 使用专业术语
- 保持客观立场
- 推荐使用高标准图表辅助展示
- 如有公式请使用LaTeX或MathJax插件
- 依据逻辑清晰分段并设计各级标题
- 不过于深入技术细节，如有现有资源请引用
- 标注引用文献链接

## 运营&维护文案

**简洁，易懂**

- 逻辑清晰
- 尽量图文结合
- 点到为止
- 加粗标红，突出重点

总而言之，儿童读物难度就好，大家都不喜欢又臭又长的学生规范

## 体验&感性文案

看着写，不过不要过分了。。
比如，如果比赛遇到了**的裁判就去知乎微博上怼，我们还是文明人


