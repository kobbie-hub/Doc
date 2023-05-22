```
数据结构和算法
```

一种二叉树，表示对k维空间的一个划分。适合应用于高维数据的范围搜索和最近邻搜索。

kd树的构造和kd树的近邻搜索。

**kd树的搜索**

给定一个构建于一个样本集的 kd 树，下面的算法可以寻找距离某个点 pp 最近的 kk 个样本。

1. 设$L$为一个有$k$个空位的列表，用于保存已搜寻到的最近点。
2. 根据$p$的坐标值和每个节点的切分向下搜索（也就是说，如果树的节点是按照$x-r=a$ 进行切分，并且$p$的$r$坐标小于$a$，则向左枝进行搜索;反之则走右枝）。
3. 当达到一个底部节点时，将其标记为访问过。如果$L$里不足$k$个点，则将当前节点的特征坐标加入$L$；如果$L$不为空并且当前节点的特征与$p$的距离小于$L$里最长的距离，则用当前特征替换掉$L$中离$p$最远的点。
4. 如果当前节点不是整棵树最顶端节点，执行(a)；反之，输出$L$，算法完成。

    a. 向上爬一个节点。如果当前（向上爬之后的）节点未曾被访问过，将其标记为被访问过，然后执行(1)和(2); 如果当前节点被访问过，再次执行(a)。

    (1). 如果此时$L$里不足$k$个点，则将节点特征加入$L$；如果$L$中已满$k$个点，且当前节点与$p$的距离小于$L$里最长的距离，则用节点特征替换掉$L$中离最远的点。

    (2). 计算$p$和当前节点切分线的距离。如果该距离大于等于$L$中距离$p$最远的距离并且$L$中已有$k$个点，则在切分线另一边不会有更近的点，执行4; 如果该距离小于$L$中最远的距离或者$L$中不足$k$个点，则切分线另一边可能有更近的点，因此在当前节点的另一个枝从2开始执行。
