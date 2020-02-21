# 概要
使用面向对象理论、泛型编程思想、C++语言中重载、继承、接口、多态和模板等技术，实现相关的数据结构和常规算法，打造了一个可复用的数据结构类私有库。其中创建了线性表的顺序存储、数组、单/双向/循环链表、栈、队列、通用树、二叉树、图等模板；递归、排序、kmp、八皇后问题等算法的实现；顶层弗列、单一继承树、异常安全等经典架构设计准则；以及单例模式、代理模式、工厂模式等设计模式也都运用其中。

# 详述
1. 创建异常类组使用异常处理机制分离正常逻辑和异常逻辑，创建顶层弗列 Object 保证单一继承树和规范动态内存申请行为；
2. 数组类和线性表类的 插入、删除、查找、获取、设置、遍历、反转、长度、清空等操作的实现，包括线性表的静态/动态顺序存储结构类、线性表的单/上向/循环链式存储结构类；
3. 创建智能指针类可以有效规避多重释放和内存泄漏的 Bug;
4. 创建栈类族，包含顺序栈和链式栈存储结构类，有栈创建、销毁、清空、进栈、出栈、栈顶元素获取、栈大小；
5. 创建队列类族，包含顺序队列和链式队列存储结构类，有队列创建、销毁、清空、进队、出队、获取队头、队列长度、判断队列是否为空，以及栈与队列的相互转换；
6. 创建字符串类族、重载实现其比较、加法、赋值、[]、插入、判断、区孔等操作；
7. KMP 算法、递归思想的应用实现链表反转、排序合并、八皇后问题；
8. 排序类的实现，选择排序、插入排序、冒泡排序，希尔排序，归并排序，快速排序等排序算法的实现；
9. 通用树类的实现，实现了树的查找、插入、清除、删除、节点数/高度/度的获取、树的层次遍历等操作；
10. 二叉树类的实现，实现树的查找、插入、清除、删除、节点数/高度/度的获取、树的层次遍历和典型遍历、克隆、比较、相加、线索化等操作；
11. 图类的实现，其中有图的遍历、最小生成树、最短路径算法的实现。

所有类及其算法全部利用泛型编程封装进入自定义命名空间，采用迭代开发的过程，设计时在细节和整体上就有充分考虑其健壮性和拓展性，棵适用于任意数据类型，做到可复用可移植。

```
第0课 - 启航，新的目标！

第1课 - 进阶高手的大门

第2课 - 数据的艺术

第3课 - 初识程序的灵魂

第4课 - 程序灵魂的审判

第5课 - 算法的时间复杂度

第6课 - 算法效率的度量

第7课 - 课程学习小问答

第8课 - 泛型编程简介

第9课 - 智能指针示例

第10课 - C++异常简介

第11课 - 异常类构建

第12课 - 顶层父类的创建

第13课 - 类族结构的进化

第14课 - 线性表的本质和操作

第15课 - 线性表的顺序存储结构

第16课 - 顺序存储结构的抽象实现

第17课 - StaticList 和 DynamicList

第18课 - 顺序存储线性表的分析

第19课 - 数组类的创建（上）

第20课 - 数组类的创建（下）

第21课 - 线性表的链式存储结构

第22课 - 单链表的具体实现

第23课 - 顺序表和单链表的对比分析

第24课 - 单链表的遍历与优化

第25课 - 静态单链表的实现

第26课 - 典型问题分析（Bugfix）

第27课 - 再论智能指针（上）

第28课 - 再论智能指针（下）

第29课 - 循环链表的实现

第30课 - 双向链表的实现

第31课 - 老生常谈的两个宏（Linux）

第32课 - Linux内核链表剖析

第33课 - 双向循环链表的实现

第34课 - 栈的概念及实现（上）

第35课 - 栈的概念及实现（下）

第36课 - 队列的概念及实现（上）

第37课 - 队列的概念及实现（下）

第38课 - 两个有趣的问题

第39课 - 字符串类的创建（上）

第40课 - 字符串类的创建（下）

第41课 - KMP 子串查找算法

第42课 - KMP 算法的应用

第43课 - 递归的思想与应用（上）

第44课 - 递归的思想与应用（中）

第45课 - 递归的思想与应用（下）

第46课 - 排序的基本概念

第47课 - 选择排序和插入排序

第48课 - 冒泡排序和希尔排序

第49课 - 归并排序和快速排序

第50课 - 排序的工程应用示例

第51课 - 树的定义与操作

第52课 - 树的存储结构与实现

第53课 - 树中结点的查找操作

第54课 - 树中结点的插入操作

第55课 - 树中结点的清除操作

第56课 - 树中结点的删除操作

第57课 - 树中属性操作的实现

第58课 - 树形结构的层次遍历

第59课 - 树到二叉树的转换

第60课 - 二叉树的深层特性

第61课 - 二叉树的存储结构设计

第62课 - 二叉树中的结点查找操作

第63课 - 二叉树中的结点插入操作

第64课 - 二叉树中的结点删除与清除

第65课 - 二叉树中属性操作的实现

第66课 - 二叉树结构的层次遍历

第67课 - 二叉树的典型遍历方式

第68课 - 二叉树的比较与相加

第69课 - 二叉树的线索化实现

第70课 - 二叉树的经典面试题分析

第71课 - 图的定义与操作

第72课 - 图的存储结构（上）

第73课 - 图的存储结构（下）

第74课 - 图的遍历（BFS）

第75课 - 图的遍历（DFS）

第76课 - 最小生成树（Prim）

第77课 - 最小生成树（Kruskal）

第78课 - 最短路径（Dijkstra）

第79课 - 最短路径（Floyd）

第80课 - 最长不下降序列（完结
```
