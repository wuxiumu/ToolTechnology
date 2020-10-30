## Forest 种树 app 建模练习

本博客针对 [Forest 种树 app](https://github.com/Owl-Movies-Ticket-System/Dashboard/blob/gh-pages/XX1-Forest应用.pdf) 的业务功能来进行用例建模、活动建模、领域建模、状态建模与系统序列建模。

### 用例建模

![这里写图片描述](https://img-blog.csdn.net/20180515113632172?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0phY2tfQ0pa/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 活动建模

针对种树这个主要业务流程进行活动图建模：

![这里写图片描述](https://img-blog.csdn.net/20180513191956219?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0phY2tfQ0pa/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 领域建模

![这里写图片描述](https://img-blog.csdn.net/20180513192130877?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0phY2tfQ0pa/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 状态建模

针对种树这个主要用例进行活动建模：

![这里写图片描述](https://img-blog.csdn.net/20180513192154707?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0phY2tfQ0pa/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 系统序列建模

#### 操作协议

- 操作：chooseTreeType(type: string)

  交叉引用：用例：选择种树类型

  前置条件：用户已经解锁要选择的树类型

  后置条件：

  - 创建了一个相应类型为 type 的 Tree 实例 tree
  - tree 与当前的 User 关联

- 操作：specifyDuration(time: time)

  交叉引用：用例：确定种树时间

  前置条件：用户已经选择了要种的树

  后置条件：

  - 创建了一个 Planter 实例 pt
  - pt 的 timer 赋值为 time

- 操作：startPlanting()

  交叉引用：用例：种树

  前置条件：用户已经选择了要种的树并确定了种树时间

  后置条件：

  - pt 与当前的 tree 关联
  - pt 的 timer 开始每隔一个固定时间减 1
  - pt 的 state 赋值为 “planting”

- 操作：succeedToPlant(award: integer)

  交叉引用：用例：完成种树

  前置条件：用户已经专注种树并过了种树时间

  后置条件：

  - pt 的 state 赋值为 “planted”
  - 用户的钱包增加 award 个金币。

#### 系统序列图

![这里写图片描述](https://img-blog.csdn.net/20180513192729586?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0phY2tfQ0pa/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)