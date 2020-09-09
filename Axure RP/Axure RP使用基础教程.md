# 一、Axure界面介绍

## 1、页面导航面板（Pages）

​    Axure的页面管理采用类似操作系统的文件夹和页面文件的管理方式，不同点是，页面文件可以存在子页面，这一点是考虑了页面与页面跳转或者嵌套页面等网页特点。

![img](https:////upload-images.jianshu.io/upload_images/8945890-cc2597e5b4e46eb8.png?imageMogr2/auto-orient/strip|imageView2/2/w/579/format/webp)

页面文件管理导航面板

## 2、元件库（Libaries）

​    Axure的元件库，类似与PPT的模板，或者是Office提供的各种形状、图标，可以通过拖拽的方式，帮助我们快速创建原型。

![img](https:////upload-images.jianshu.io/upload_images/8945890-049fdc8e3d909149.png?imageMogr2/auto-orient/strip|imageView2/2/w/243/format/webp)

Axure的元件库导航

### 2.1元件库导入

​    Axure提供了多种元件库的导入功能，包含官网下载，本地导入、导入共享原件、手工创建等方式。其中手工创建可将我们日常用到较多的图形、样式、效果等管理成元件库，使用是，可直接拖拽到画布中，这里的原件不是简单的图形、形状、样式，还包含了网页所支持的特效，如渐进渐出、隐藏显示、幻灯片、链接跳转等

![img]()

元件库管理

### 2.2 元件库使用

元件库提供了方便的导航筛选和元件名称搜索功能。



![img]()

元件库筛选

![img](https:////upload-images.jianshu.io/upload_images/8945890-473f4cf922e1db87.png?imageMogr2/auto-orient/strip|imageView2/2/w/226/format/webp)

元件库检索

![img](https:////upload-images.jianshu.io/upload_images/8945890-8b28454e60bf3fe0.png?imageMogr2/auto-orient/strip|imageView2/2/w/654/format/webp)

拖拽使用元件

## 3.工具栏（ToolBar）

工具栏提供了常用按钮的快捷入口，既可以通过鼠标点击激活，也可以通过快捷键激活。

> 选择有两种模式，相交模式：鼠标按住拖动选择多个元素时，只要鼠标滑过的区域与元素有相交，该元素即被选中；包含模式：鼠标按住拖动选择多个元素时，只有鼠标滑过的区域完全覆盖了该元素，该元素才能被选中。

默认为相交模式，该模式类似与PPT中的选中模式。

锁定位置的作用主要是将元素锁定在特定位置，以方便处理其他元素，元素一旦锁定后，变无法拖动位置。

![img](https:////upload-images.jianshu.io/upload_images/8945890-1de2bb13a581426c.png?imageMogr2/auto-orient/strip|imageView2/2/w/918/format/webp)

工具栏

预览功能是将当前涉及的原型发布到浏览器浏览，其原理是Axure搭建了一个小型的静态文件服务器，创建的原型转成HTML文件，发布到服务器上，浏览器进行访问预览。

发布功能是将设计的原型图转成HTML静态文件，如果设置了各类动作，Axure会自动生成js的方法帮助实现HTML中的特效。

![img](https:////upload-images.jianshu.io/upload_images/8945890-a7c6bc9a8f718781.png?imageMogr2/auto-orient/strip|imageView2/2/w/239/format/webp)

工具栏

## 4.检视器面板（Inspector）

在画布中，选中元素，右侧可看到样式面板，包含了三部分：样式，类似与CSS所需的各类属性；。

### 4.1 样式面板（Style）

面板提供了元素所需的各种样式属性设置功能，包含了元素名称、盒子模型中的边框、内外边距、圆角、透明度、字体、着重号、对齐方式等

![img]()

样式面板

### 4.2备注面板（Notes）

可对元素设置元素备注，备注后效果如下图：

![img]()

元素备注

### 4.3交互面板（Properties）

属性面板提供了完整的web页面所需的各类事件绑定所需的设置，如点击事件、双击事件、显示、隐藏、链接等。



![img]()

属性设置面板

## 5、大纲面板（Outline）

Axure提供了所有元素的大纲导航面板，类似于PS中的图层管理面板，可完成各个元素的组合，取消组合，元素压盖顺序调整，元素名称命名，组名称命名，删除、选中、多选等操作。为控制多个图层、元素提供了边界的入口。

![img]()

大纲面板

# 二、基础操作

## 1.使用元件

### 1.1设置元件名称

可通过检视面板修改元素名称，也可以通过大纲面板，选中修改。

![img]()

设置元件名称

### 1.2设置元件大小、位置、角度

在样式面板可设置元件的大小，位置，也可以通过拖动的方式设置。

> x：从左侧到右侧的距离，单位px
>
> y：从上到下的距离，单位px
>
> w：元件的宽度，单位px
>
> h：元件的长度，单位px
>
> R：元件的角度，单位度
>
> T：文字的角度，单位度



![img]()

设置元件大小、位置、角度

### 1.3设置元件的颜色和透明度

​    选择要改变颜色的元件，点击快捷功能区中的背景颜色设置按钮，选取相应的颜色，或者在元件样式中进行设置。

![img]()

设置元件的颜色和透明度

### 1.4设置元件的盒子模型属性

Axure完美的支持Web页面的布局中的盒子模型属性的设置。

![img]()

盒子模型中的各个属性设置

### 1.5设置元件默认隐藏

​    在检视的样式面板中，右上角的隐藏选择框，如果勾上，则该元件默认为隐藏，在画布中则以浅色的形式存在。

![img]()

默认隐藏元件

### 1.6标记元件文字

对需要添加文字的元件，双击该元件，即可输入文字。

![img]()

双击添加文字

## 2、元件交互

### 2.1设置元件的类型、Tips、约束

可以通过检视面板中的属性面面板，设置元件的类型（如Text、Email、Password）、占位符、Tips、长度、是否隐藏边框、是否只读、是否禁用、表单提交按钮等信息

![img]()

表单交互基本属性设置

### 2.2 元件事件设置

选择元件后在检视的交互属性界面，选择事件类型（点击、双击、右键、鼠标滑过、点击后等），在弹出的对话框中，可设计页面跳转、界面元素显示隐藏、渐入渐出效果等各类动作。

![img]()

事件设置

### 2.3设置下拉列表值

通过元件库选择List Box元件，在检视的交互属性面板点击添加项菜单，可以批量添加下拉值。



![img](https:////upload-images.jianshu.io/upload_images/8945890-2c85f0a0ace34892.png?imageMogr2/auto-orient/strip|imageView2/2/w/855/format/webp)

下拉列表值设定

### 2.4单选按钮唯一选中

可以对多个单选按钮设置唯一选中效果，选中多个单选按钮，设置按钮组名即可。



![img](https:////upload-images.jianshu.io/upload_images/8945890-55864f0ad1315aee.png?imageMogr2/auto-orient/strip|imageView2/2/w/582/format/webp)

单选按钮唯一选中

## 3.其他常用操作

### 3.1转换元件为图片

右键中可支持元件转化为图片的操作



![img](https:////upload-images.jianshu.io/upload_images/8945890-a3d9f50185d85697.png?imageMogr2/auto-orient/strip|imageView2/2/w/328/format/webp)

转为组件为图片

### 3.2 元件组合和取消组合

在实际的原型绘制过程中，需要将多个元件组合成一个整体，比如多个单选框需要组成一组、文字描述和按钮元件、页面的header、footer、导航条等。



![img]()

组合



![img]()

取消组合

### 3.3 调整元件的层级

类似与HTML中的Z-index一样，多个元件存在压盖的层级顺序，默认的顺序是先拖入的元件被后拖入的元件压盖，也即后来居上。可通过右键调整层级，也可以在概要(Outline)处拖拽调整，概要出的层级是靠上部的元件压盖靠近下部的元件。

![img]()

右键调整元件层级



![img]()

概要(Outline)拖拽调整

### 3.4 添加事件执行的条件

在事件设置页面，可通过添加条件的方式，来满足复杂的交互

![img]()

设置条件的入口

![img](https:////upload-images.jianshu.io/upload_images/8945890-48ded866c48c541b.png?imageMogr2/auto-orient/strip|imageView2/2/w/787/format/webp)

条件设置面板

3.5 设置变量

![img](https:////upload-images.jianshu.io/upload_images/8945890-0388941eec192df4.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

局部变量



![img](https:////upload-images.jianshu.io/upload_images/8945890-a2c1d185f206aacf.png?imageMogr2/auto-orient/strip|imageView2/2/w/249/format/webp)

全局变量

## 4、常用功能设置

### 4.1 设置形状并排显示时边框是否重叠



![img](https:////upload-images.jianshu.io/upload_images/8945890-d2beb1e3daef5b85.png?imageMogr2/auto-orient/strip|imageView2/2/w/910/format/webp)

边界重合设置

### 4.2 显示和隐藏交互和说明编号

一个元件设置了备注或者添加了交互时间后，默认显示编号，可设置显示或不显示



![img](https:////upload-images.jianshu.io/upload_images/8945890-ebf78191c1182e5d.png?imageMogr2/auto-orient/strip|imageView2/2/w/533/format/webp)

脚注序号显示隐藏

### 4.3 显示/隐藏两侧的功能面板

点击可展开左侧或右侧的面板

![img]()

左右侧面板开关

### 4.4 响应式布局设置

​    通过设置自适应视图，使得原型HTML在多种分辨率设备中查看时，系统会根据自身分辨率，自动与分辨率相适合的原型进行匹配，并显示出来。

![img](https:////upload-images.jianshu.io/upload_images/8945890-70201740c65ce111.png?imageMogr2/auto-orient/strip|imageView2/2/w/243/format/webp)

自适应视图

![img](https:////upload-images.jianshu.io/upload_images/8945890-99fb6b5932fdc40f.png?imageMogr2/auto-orient/strip|imageView2/2/w/501/format/webp)

多终端分辨率设置

# 三、Axure RP撰写需求文档

需求文档的撰写已经从最开始的纯文字，逐渐转变到图文结合，再到线框图，再到原型图，再到JS高仿真Demo等形式，为的是保证客户需求的传达和落地不偏离，环节交接无抛接。

**总的来说，需求文档有三个作用：**

**1. 传达客户、功能、应用、产品开发需求；**

**2. 保证各环节沟通有理有据**

**3. 软件及产品质量控制有具体标准**

​    很多程序猿在开发时，一般都是看着效果图和原型图写代码，只有在遇到问题时，才会查看word文档。也就是说，开发需要一边写代码，一边看效果图，一边看原型，还要时不时查看文档。

​    而且，大多数程序猿都不会逐字逐句去读产品经理的长篇大论。那需求写word真的合适吗？这样的用户体验真的好吗？花费大量时间写word真的有价值吗？在Axure画原型的同时，我们为什么不能直接在旁边标注呢？这样岂不是方便快捷很多吗？

​    其实，流行一种直接在原型图上标注的需求文档撰写方式。在新版的Axure8中，也已经推荐了原型加标注的需求文档样式。Axure8新增了一组部件—不干贴，就是方便产品设计人员进行功能标注。

以下方式仅供参考



![img](https:////upload-images.jianshu.io/upload_images/8945890-bcf1ee229a2c497a.png?imageMogr2/auto-orient/strip|imageView2/2/w/272/format/webp)

需求文档结构

![img](https:////upload-images.jianshu.io/upload_images/8945890-721237c5ad472500.png?imageMogr2/auto-orient/strip|imageView2/2/w/976/format/webp)

脚注模式



![img](https:////upload-images.jianshu.io/upload_images/8945890-a84e12308fd5e7d8.png?imageMogr2/auto-orient/strip|imageView2/2/w/718/format/webp)

不干胶模式



作者：落霞__孤鹜
链接：https://www.jianshu.com/p/97fd99e38d71
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。