# 数据结构

计算机中数据的组织方式。

推荐书目：
《算法导论》

推荐网站：

https://visualgo.net/

https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/index.html

## 线性存储结构

> 考试刚刚结束，班主任需要记录一下每个同学的分数：）

### 数组 Array

使用连续的存储空间存储一系列元素。

* 计算机内存原生使用的数据结构
* 通过空间的连续性保证顺序关系
* 按索引查找
* 增加 / 删除的开销[比较大](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/ListArray.html#listarray)

### 链表 Linked List

离散地存储一系列元素，通过指针表示顺序关系。

* 除了元素本身，还要使用额外的空间存储顺序关系
* 增加 / 删除的开销[比较小](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/ListLinked.html#linked-list-implementation)
* 没有索引，查第n个元素需要依次访问前n个元素
* 扩展：[双向链表](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/ListDouble.html)，循环链表

### 散列表 Hash Table

又叫哈希表。使用连续的空间离散地存储一系列元素，这种结构没有顺序关系。

* 按索引查找
* 解决数组索引范围有限的问题
* 核心是映射函数
* [冲突的解决](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/OpenHash.html)

### [栈 Stack](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/StackArray.html)

三种操作：
* 取栈顶元素的值
* 加入元素至栈顶
* 把栈顶的元素扔出来

特性：
* 可基于链表 / 数组实现
* 先进后出

> 括号匹配

### [队列 Queue](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/Queue.html)

三种操作：
* 取队列首元素的值
* 加入元素至队列尾
* 把队列首的元素扔出来

特性：
* 可基于链表 / 数组实现
* 先进先出
* 扩展：双端队列，循环队列

> 任务调度

## [树 Tree](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/GenTreeIntro.html)

> 新的学期开始了，班主任设计了一套（老掉牙的）收作业的方法：组长从组员处收集作业，课代表从组长处收集作业。

* 特点：无环，连通，有向

概念：
* 父亲，孩子
* 子树
* 根节点：没有父亲的节点
* 叶节点：没有孩子的节点
* 节点高度：节点到根的距离
* 树的高度：高度最大的节点的高度
* 森林，不相交集合森林

### [二叉树 Binary Tree](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/BinaryTree.html)

每个节点最多有两个孩子的树。

* 完全二叉树：从上到下从左到右排满的二叉树
* 满二叉树：每个节点，要么没有孩子，要么有两个孩子
* 完全满二叉树
* 高度为h的节点至多有2^h个
* 非二叉树转换为二叉树的方法

### [二叉树的遍历](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/BinaryTreeTraversal.html)
* 先序遍历：根->左子树->右子树
* 中序遍历：左子树->根->右子树
* 后序遍历：左子树->右子树->根

### [二叉搜索树 Binary Search Tree](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/BST.html)

* 中序遍历有序
* 最多查询树高h次即可知道结果
* 可以动态插入删除元素
* [平衡树](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/BalancedTree.html)：AVL，伸展树，红黑树

### [堆 Heap](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/Heaps.html)

* 所有的父子都满足某种顺序关系的完全二叉树
* 可以动态插入删除元素
* 应用：排序，优先队列

## [图 Graph](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/GraphIntro.html)

> 课间操的时候，你发现隔壁的的小姐姐韩梅梅非常漂亮，心生爱慕。
> 放学之后你想去要个微信，结果却看见你的死党老王和她手挽手一起走。
> 第二天你在厕所里遇见了老王，你质问他为什么要抢你的心上人，他却说那都是假的，他的心里只有你。

* 概念：顶点，边，度，权，环
* 有向图与无向图
* 简单与非简单
* 连通性：强连通，单连通，弱连通，不连通
* 稀疏与稠密，完全图

### [图的遍历](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/GraphTraversal.html)

* 广度优先搜索
* 深度优先搜索

### [最小生成树](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/MCST.html)

* 从点出发：Prim
* 从边出发：Kruskal

### 有向无环图 Directed Acyclic Graph

* [拓扑排序]((https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/GraphTopsort.html))
* 强连通分量

### 单源最短路

* [Dijkstra](https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/GraphShortest.html)
* 解决负权问题：[Bellman-Ford](https://visualgo.net/en/sssp)
* 队列优化：SPFA

### 全局最短路

* Floyd
