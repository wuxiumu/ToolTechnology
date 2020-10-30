发布于: 2020 年 09 月 17 日

﻿

极客时间架构训练营第 1 期第一周作业

﻿

**食堂就餐卡系统设计**

﻿

- 系统中每个消费者都有一张卡，在管理中心注册缴费，卡内记着消费者的身份、余额。
- 使用时将卡插入收款机则显示卡上金额，服务员按收款机上数字键，收款机自动计算并显示消费额及余额。
- 管理中心的管理员监视每一笔消费，可打印出消费情况的相关统计数据。

﻿

请设计系统用例图，组件图，组件时序图，部署图。

﻿

> 没有设计文档就没有软件设计，没有软件设计就没有技术进步

﻿

没有 UML 图，就没有设计文档

﻿

**用例图**

![img](https://static001.geekbang.org/infoq/e6/e691c30acc4c598f46e241edcba19f0e.jpeg?x-oss-process=image/resize,p_80/auto-orient,1)

用例图

在用例图里面，除了注册和缴费之外，给消费者增加了查询余额、挂失和退卡的用例；

收款机的用例有读卡、显示余额、消费扣款、显示消费额；

服务员的用例只有输入消费金额；

管理员的用例有统计和监督；

﻿

**组件图**

![img](https://static001.geekbang.org/infoq/5c/5c1cc782e2dda4ef8afe8dce0e5eb62d.jpeg?x-oss-process=image/resize,p_80/auto-orient,1)

组件图

一共有 7 个组件，除了服务员终端、消费者终端和管理员终端之外，增加了一个用户终端（Client Console），提供用户注册和缴费的功能。

其他 3 个组件分别为读卡器（收款机）、账户管理（AccountMgmt）和账户数据库（AccountDb）

﻿

**组件时序图**

![img](https://static001.geekbang.org/infoq/8f/8feb792f62f4dd09c035c858d16e3c77.jpeg?x-oss-process=image/resize,p_80/auto-orient,1)

时序图

﻿

时序图画起来比较复杂，主要是因为发起者比较多（消费者、服务员、管理员），但是如果认真画一下，对于整个系统就会理解的更深入一些。

﻿

**部署图**

![img](https://static001.geekbang.org/infoq/ed/edfc8808a7c65e6f1ca6f3ebec26a44e.jpeg?x-oss-process=image/resize,p_80/auto-orient,1)

部署图

除了部署多个收款机（在图中显示为 3 个），另外部署一个后台数据库（AccountDB），一个账户管理后台服务器（AccountMgmt）和一台账户管理 Web 服务器（AccountWeb），其中数据库、后台和 Web 三个服务器可以合并为一台。