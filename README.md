# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# ssm196基于Java框架失物招领信息交互平台的设计与实现+vue

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1T48XecE9G?p=190)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

失物招领信息交互平台工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。失物招领信息交互平台的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、用户信息实体图如图4-3所示：

![](/md/blog.014.png)

图4-3用户信息实体图

2、失物招领信息实体图如图4-4所示：

![](/md/blog.015.png)

`       `图4-4失物招领信息实体图

3、物品挂失信息实体图如图4-5所示：

![](/md/blog.016.png)

`     `图4-5物品挂失信息实体图
### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


`  `表4-2 shiwurenling表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|shiwubianhao|varchar|50|default NULL|
|wupinmingcheng|varchar|50|default NULL|
|wupinleixing|varchar|50|default NULL|
|wupintupian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|yonghu|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|renlingshijian|varchar|50|default NULL|
|renlingmiaoshu|varchar|50|default NULL|
|sfsh|varchar|50|default NULL|
|shhf|varchar|50|default NULL|

表4-3：shiwuzhaoling表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|shiwubianhao|varchar|50|default NULL|
|wupinmingcheng|varchar|50|default NULL|
|wupinleixing|varchar|50|default NULL|
|`      `wupintupian|varchar|50|default NULL|
|shiyishijian|varchar|50|default NULL|
|`     `shiyididian|varchar|50|default NULL|
|`     `wupinzhuangtai|varchar|50|default NULL|
|xiangqing|varchar|50|default NULL|


表4-4：wupinguashi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|wupinmingcheng|varchar|50|default NULL|
|wupinleixing|varchar|50|default NULL|
|wupintupian|varchar|50|default NULL|
|yishishijian|varchar|50|default NULL|
|yishididian|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|yonghu|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|yishixiangqing|varchar|50|default NULL|

表4-5：yonghu表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|zhanghao|varchar|50|default NULL|
|mima|varchar|50|default NULL|
|yonghu|varchar|50|default NULL|
|xingbie|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|youxiang|varchar|50|default NULL|
|touxiang|varchar|50|default NULL|

#########
# 5系统界面实现
## 5.1 管理员登录
管理员输入个人的用户名、密码和角色登录系统，这时候系统的数据库就会在进行查找相关的信息，如果我们输入的用户名、密码和角色不正确，数据库就会提示出错误的信息提示，同时会提示管理员重新输入自己的用户名、密码、角色，直到用户名、密码输入成功后，会提登录成功的信息。网站管理员登录效果图如图5-1所示：

![](/md/blog.017.png)     
图5-1管理员登录界面

## 5.2  管理员功能模块     
### 5.2.1 用户管理
管理员对用户管理进行查看账号、用户、性别、手机、邮箱、头像并进行详情、删除、修改等操作。程序成效图如下图5-2所示:

![](/md/blog.018.png)

图5-2用户管理界面图
### 5.2.2失物招领管理
管理员对失物招领管理进行查看失物编号、物品名称、物品类型、物品图片、拾遗时间、拾遗地点、物品状态等信息并可以进行详情、删除、修改操作。程序效果图如下图5-3所示：

![](/md/blog.019.png)

图5-3失物招领管理界面
### 5.2.3 物品类型管理
管理员对物品类型管理进行查看物品类型等信息并可以进行详情、删除、修改操作。程序效果图如下图5-4所示：

![](/md/blog.020.png) 

图5-4物品类型管理界面

### 5.2.4失物认领管理
管理员对失物认领管理进行查看失物编号、物品名称、物品类型、物品图片、账号、用户、手机、认领时间、审核回复、审核状态、审核等进行详情、删除、修改操作。程序效果图如下图5-5所示：

![](/md/blog.021.png)

图5-5失物认领管理界面
### 5.2.5物品挂失管理
管理员对物品挂失管理进行查看物品名称、物品类型、物品图片、遗失时间、遗失地点、账号、用户、手机等信息并可以进行详情、删除、修改操作。程序效果图如下图5-6所示：

![](/md/blog.022.png) 

图5-6物品挂失管理界面
### 5.2.6寻物论坛
管理员对寻物论坛进行查看帖子标题、用户名、状态等信息并可以进行详情、删除、修改操作。程序效果图如下图5-7所示：

![](/md/blog.023.png) 

图5-7寻物论坛界面


### 5.2.7网站资讯
管理员对网站资讯进行查看标题、图片等信息并可以进行详情、删除、修改操作。程序效果图如下图5-8所示：

![](/md/blog.024.png) 

图5-8网站资讯界面




## 5.3 前台首页功能模块
前台首页详情页面首页、失物招领、物品挂失、寻物论坛、网站资讯、个人中心、后台管理等功能操作。程序效果图如下图5-9所示：

![](/md/blog.025.png)

图5-9前台首页功能界面
## 5.3.1用户注册、用户登录
用户在线填写账号、密码、用户、手机、邮箱等信息进行注册、登录操作。程序效果图如下图5-10所示：

![](/md/blog.026.png)

![](/md/blog.027.png)

图5-10用户登录、用户注册界面
## 5.3.2个人中心
用户进入个人中心可以填写账号、密码、用户、性别、手机、邮箱等信息，并可以进行更新信息、退出登录操作。程序效果图如下图5-11所示：

![](/md/blog.028.png)


图5-11个人中心界面
## 5.3.3失物招领
用户进入失物招领可以查看失物编号、物品名称、物品类型、物品图片、拾遗时间、拾遗地点、物品状态等信息进行认领操作。程序效果图如下图5-12所示：

![](/md/blog.029.png)

图5-12失物招领界面

## 5.4 用户功能模块

## 5.4.1失物招领管理
用户进入失物招领管理可以查看失物编号、物品名称、物品类型、物品图片、拾遗时间、拾遗地点、物品状态等信息进行详情。程序效果图如下图5-13所示：

![](/md/blog.030.png)

图5-13失物招领管理界面
## 5.4.2物品挂失管理
用户进入物品挂失管理可以查看物品名称、物品类型、物品图片、遗失时间、遗失地点、账号、用户、手机并可以进行详情、删除等操作。程序效果图如下图5-14所示：

![](/md/blog.031.png)

图5-14物品挂失管理界面













