## 三个坑教程：查询天气

### 本周任务说明

在shell窗口查询本地天气数据，实现四个功能：

* 输入help，输出操作说明

* 输入城市名称，输出对应天气

* 输入quit退出

* 输入其他报错

为了实现这些功能，需要做四个步骤

1.读入天气文件

2.将天气文件转换为字典

3.使用字典查询天气

4.流控制

#### 坑一：读入天气文件

天气文件给的是txt格式，参考open\(\)文件函数即可读入相关文件。这一步花了大约两小时，难点在于不熟悉read和open函数。

> print f.read\('weather\_info.txt'\)

得到错误：

> TypeError: an integer is required

折腾了好久才发现只要写成这样就好了。。

> print f.read\(\)

#### 坑二：转换为字典dict

所给文件为txt格式，每行一条城市和天气，中间用逗号隔开。于是我想到了csv文件。有没有什么函数可以直接把csv格式转化为dict呢？google发现果然有！于是这个坑大约一个小时左右搞定了。重点在于熟悉dict的用法，弄懂csv转dict函数怎么用。

#### 坑三：使用字典查询天气

这部分就是要理解MAP（映射）。列表中的城市和天气形成意义映射的关系，即key-value键值对，通过key可以查询相应的value，反之亦然。只要知道这一点，熟悉了dict的方法，就不难做出。

#### 坑四：控制流

这部分需要细心，一个要注意基本的语法，记得在函数定义、if语句、循环语句后面打冒号！另外一个需要特别注意的是缩进。如果缩进不正确，会得到错误

> expected an indented block

其他的逻辑理清后就水到渠成啦！



