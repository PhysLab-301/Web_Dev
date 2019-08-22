*Website of PhysLab301 @Chongqing University*

*Constructed from Nov. 2018*

*Maintained by Physlab@301 Undergraduate Tech Group*

*For Knowledge & Science*


# PhysLab301官方网站 [![online yes](https://img.shields.io/badge/online-yes-brightgreen)](https://www.physlab.science/)

本网站为重庆大学物理系PhysLab301本科生实验室官网，由2016级CUPT成员建于2018年11月，目前由应届301本科生技术组进行维护。

网站总结整理了竞赛相关资源和档案，旨在为物理学院本科生参与学术竞赛和科学研究提供帮助。

- 网站目前正在进一步建设中，如有不足之处请多见谅，欢迎各位的批评反馈。

- 对于各届参赛队员，如果你有任何希望表达的想法和想要分享的知识或资源，欢迎投稿或提供修改建议。

联系方式如下。

- 邮箱： PhysLab301@outlook.com

- 项目代码库:  https://github.com/PhysLab301/Web_Dev

- PhysLab301 技术组群 https://jq.qq.com/?_wv=1027&k=5lsyRSO

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
相关知识技术背景请移步CS专业
PS：希望301每年都有程序员进行技术维护。

- VPS：[Bandwagon](https://bandwagonhost.com)
- 域名注册：[NameCheap](https://www.namecheap.com/)
- DNS解析：[CloudFlare](https://www.dnspod.cn/)
- 博客框架：[Hexo](https://hexo.io/zh-cn/)
- 自动部署：[githook](https://git-scm.com/)
- 安全证书：[WildCard](https://letsencrypt.org/)
  
## 如何更新博客

### 书写
[如何使用Hexo写作](https://hexo.io/zh-cn/docs/writing)

修改 About 部分的宣传文章请编辑source/about/index.md
其余主页栏为hexo主题自动生成

### 设置
请在项目源路径下编辑_config.yml文件，参见[如何配置博客](https://hexo.io/zh-cn/docs/configuration)

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
维护技术问题可联系301相关学长。

# 文档规范建议

## 专业&技术性文案 Techology/Research

**简洁，客观，专业**

- 使用专业术语
- 保持客观立场
- 推荐使用高标准图表辅助展示
- 如有公式请使用LaTeX或MathJax插件
- 依据逻辑清晰分段并设计各级标题
- 不过于深入技术细节，如有现有资源请引用
- 标注引用文献链接

## 运营&维护文案 Maintenance

**简洁，易懂**

- 逻辑清晰
- 尽量图文结合
- 点到为止
- 加粗标红，突出重点


## 归档&新闻文案 Archive/News

**真实记录**

- 基本信息和背景
- 相关代码/数据/图片/幻灯片，整理打包为项目压缩文件
- 文件规范命名

## 体验&感性文案 Experience

**个人体验部分因人而异，基本原则如下：**

- 可以有主观表达，但避免过度情绪化
- 请提出有意义的观点和思考
- 保证积极的态度
- 保证学术讨论部分的严谨



