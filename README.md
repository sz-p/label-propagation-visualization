# label-propagation-visualization

## 简介

对标签传播算法的结果做了一个可视化。数据包含`College Football 网络`,`Zachary karate club`,`d3 blocks Force`数据详情见 `参考 & 引用` 1 2，这里的数据均无标签。

这里标签传播算法的运行方式为初始化时对所有节点初始化一个随机标签，根据连接信息开始传播，从已连接的节点中选择标签最多的那个作为本节点的标签。迭代运行得到最周已收敛的标签集合。

核心算法见[npm包](https://www.npmjs.com/package/layered-label-propagation)

## 截屏

![](https://img.sz-p.cn/lpv-1.png)

![](https://img.sz-p.cn/lpv-2.png)

## 安装 & 启动

安装`node.js`,`yarn`

```shell
yarn install
yarn start
```

## 思考 & TODO

这里仅仅对标签传播算法的结果进行了一个简单的可视化、由于本质上数据的无标签，以及数据和标签传播算法本身的特性、笔者对迭代次数做过一些调整，但效果并不明显所以未开放参数调整。因为以上问题以及笔者采用的第三方包封装问题，所以未对传播过程做可视化。

从图1、图2中观察、笔者认为力学图布局本身也可以作为一个算法去做`聚类`或`社区发现`。力学图的布局结果其实是对节点赋了坐标信息，根据坐标信息结合`k-means`算法应该可以实现一个较好的聚类效果，而且所见即所得。

关于力学图布局算法见[力学图布局算法](https://sz-p.com/d3layoutdoc/%E5%8A%9B%E5%AD%A6%E5%9B%BEForce.html)，关于`k-means`见 [k-means算法](https://sz-p.cn/blog/index.php/2020/05/14/296.html)

这里下一步，一方面可以手动实现一遍标签传播算法，实现基于有标签的数据的传播，将每次迭代的结果抛出，对传播过程做个可视化。

一方面可以针对力学图算法以及`k-means`算法实现一个新的`聚类`算法。

这两个方向是笔者认为相对有探究价值，欢迎感兴趣的从业者共同参与。

## 参考 & 引用

http://bl.ocks.org/mbostock/afecf1ce04644ad9036ca146d2084895

https://blog.csdn.net/wzgang123/article/details/51089521
