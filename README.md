# LeetCode-python
因为俺要找工作，所以一些题解会含有java语言解法，QAQ

![](https://img.shields.io/badge/Python%203-Java%208-blue)
![](https://img.shields.io/badge/已覆盖-207题-green)
![](https://img.shields.io/badge/排序算法-7种-red)
![](https://img.shields.io/badge/同向双指针/滑动窗口-Sliding%20Window-orange)
![](https://img.shields.io/badge/宽度/广度优先搜索-Breadth%20First%20Search|BFS-yellow)
![](https://img.shields.io/badge/深度优先搜索-Depth%20First%20Search|DFS-purple)
![](https://img.shields.io/badge/回溯-BackTracking-fuchsia)
![](https://img.shields.io/badge/前缀树/字典树-Trie-seagreen)
![](https://img.shields.io/badge/并查集-Union%20Find-teal)
![](https://img.shields.io/badge/前缀和-Prefix%20Sum-ultramarine)
![](https://img.shields.io/badge/动态规划-Dynamic%20Programming-cornflowerblue)

我要刷题**冲冲冲**

## 目录
+ [1.基础知识](#1基础知识)
    + [1.1排序算法](#11-排序算法java实现)
    + [1.2 同向双指针/滑动窗口](#12-同向双指针滑动窗口)
    + [1.3 宽度优先搜索bfs](#13-宽度优先搜索bfs)
    + [1.4 深度优先搜索dfs](#14-深度优先搜索dfs)
    + [1.5 回溯](#15-回溯)
    + [1.6 字典树](#16-字典树trie)
    + [1.7 并查集](#17-并查集)
    + [1.8 前缀和](#18-前缀和)
    + [1.9 动态规划](#19-动态规划)

+ [2.题目](#2题目)
    + [1.两数之和](#1两数之和)
    + [2.两数相加](#2两数相加)
    + [3.无重复读字符的最长字串](#3无重复字符的最长子串)
    + [4.寻找两个正序数组中的中位数](#4寻找两个正序数组的中位数)
    + [5.最长回文子串](#5最长回文子串)
    + [8.字符串转换整数atoi](#8字符串转换整数atoi)
    + [11.盛水最多的容器](#11盛水最多的容器)
    + [15.三数之和](#15三数之和)
    + [16.最接近的三数之和](#16最接近的三数之和)
    + [17.电话号码的字母组合](#17电话号码的字母组合)
    + [18.四数之和](#18四数之和)
    + [20.有效的括号](#20有效的括号)
    + [22.括号生成](#22括号生成)
    + [23.合并k个升序链表](#23合并k个升序链表)
    + [26.删除有序数组中的重复项](#26删除有序数组中的重复项)
    + [27.移除元素](#27移除元素)
    + [33.搜索旋转排序数组](#33搜索旋转排序数组)
    + [34.在排序数组中查找元素的第一个和最后一个位置](#34-在排序数组中查找元素的第一个和最后一个位置)
    + [37.解数独★](#37解数独)
    + [39.组合总和](#39组合总和)
    + [40.组合总和ⅱ](#40组合总和-ii)
    + [46.全排列](#46全排列)
    + [47.全排列ii](#47全排列ii)
    + [49.字母异位词分组](#49字母异位词分组)
    + [51.N皇后★](#51n皇后)
    + [52.N皇后ii](#52n皇后ii)
    + [53.最大子数组和](#53最大子数组和)
    + [54.螺旋矩阵](#54螺旋矩阵)
    + [56.合并区间](#56合并区间)
    + [69.x的平方根](#69x的平方根)
    + [70.爬楼梯](#70爬楼梯)
    + [72.编辑距离](#72编辑距离)
    + [73.矩阵置零](#73矩阵置零)
    + [74.搜索二维矩阵](#74搜索二维矩阵)
    + [75.颜色分类](#75颜色分类)
    + [76.最小覆盖子串](#76最小覆盖子串)
    + [77.组合](#77组合)
    + [78.子集](#78子集)
    + [79.单词搜索](#79单词搜索)
    + [88.合并两个有序数组](#88合并两个有序数组)
    + [90.子集ii](#90子集-ii)
    + [92.反转链表ii](#92反转链表-ii)
    + [93.复原IP地址](#93复原ip地址)
    + [97.交错字符串](#97交错字符串)
    + [98.验证二叉搜索树](#98验证二叉搜索树)
    + [100.相同的树](#100相同的树)
    + [101.对称二叉树](#101对称二叉树)
    + [102.二叉树的层序遍历](#102二叉树的层序遍历)
    + [103.二叉树的锯齿形层序遍历](#103二叉树的锯齿形层序遍历)
    + [104.二叉树的最大深度](#104二叉树的最大深度)
    + [105.从前序与中序遍历序列构造二叉树](#105从前序与中序遍历序列构造二叉树)
    + [108.将有序数组转换成二叉搜索树](#108将有序数组转换成二叉搜索树)
    + [109.有序链表转换二叉搜索树](#109有序链表转换二叉搜索树)
    + [121.买卖股票的最佳时机](#121买卖股票的最佳时机)
    + [124.二叉树中的最大路径和](#124二叉树中的最大路径和)
    + [125.验证回文串](#125验证回文串)
    + [126.单词接龙ii★](#126单词接龙ii)
    + [127.单词接龙](#127单词接龙)
    + [128.最长连续序列](#128最长连续序列)
    + [130.被围绕的区域★](#130被围绕的区域)
    + [131.分割回文串](#131分割回文串)
    + [133.克隆图★](#133克隆图)
    + [138.复制带随机指针的链表](#138复制带随机指针的链表)
    + [139.单词拆分](#139单词拆分)
    + [140.单词拆分 ii](#140单词拆分-ii)
    + [141.环形链表 i](#141环形链表-i)
    + [142.环形链表 ii](#142环形链表-ii)
    + [146.lru缓存](#146lru缓存)
    + [148.排序链表](#148排序链表)
    + [150.逆波兰表达式求值](#150逆波兰表达式求值)
    + [155.最小栈](#155最小栈)
    + [160.相交链表](#160相交链表)
    + [162.寻找峰值](#162寻找峰值)
    + [167.两数之和 ii 输入有序数组](#167两数之和-ii---输入有序数组)
    + [179.最大数](#179最大数)
    + [200.岛屿数量](#200岛屿数量)
    + [206.反转链表](#206反转链表)
    + [207.课程表](#207课程表)
    + [208.实现trie(前缀树)](#208实现trie前缀树)
    + [210.课程表 ii](#210课程表-ii)
    + [212.单词搜索ii★](#212单词搜索ii)
    + [215.数组中的第k个最大元素](#215数组中的第k个最大元素)
    + [216.组合总和iii](#216组合总和iii)
    + [224.基本计算器](#224基本计算器)
    + [225.用队列实现栈](#225用队列实现栈)
    + [226.翻转二叉树](#226翻转二叉树)
    + [230.二叉搜索树中第k小的元素](#230二叉搜索树中第k小的元素)
    + [232.用栈实现队列](#232用栈实现队列)
    + [235.二叉搜索树的最近公共祖先](#235二叉搜索树的最近公共祖先)
    + [236.二叉树的最近公共祖先](#236二叉树的最近公共祖先)
    + [240.搜索二维矩阵 ii](#240搜索二维矩阵ii)
    + [264.丑数 ii](#264丑数ii)
    + [278.第一个错误版本](#278第一个错误版本)
    + [283.移动零](#283移动零)
    + [285.二叉搜索树中的中序后继(剑指offer ii 053)](#285二叉搜索树中的中序后继剑指offer-ii-053)
    + [290.单词规律](#290单词规律)
    + [295.数据流的中位数](#295数据流的中位数)
    + [297.二叉树的序列化与反序列化](#297二叉树的序列化与反序列化)
    + [299.猜数字游戏](#299猜数字游戏)
    + [301.删除无效的括号★](#301删除无效的括号)
    + [303.区域和检索](#303区域和检索)
    + [304.二维区域和检索-矩阵不可变](#304二维区域和检索-矩阵不可变)
    + [310.最小高度树★](#310最小高度树)
    + [328.奇偶链表](#328奇偶链表)
    + [329.矩阵中的最长递增路径](#329矩阵中的最长递增路径)
    + [341.扁平化嵌套列表迭代器](#341扁平化嵌套列表迭代器)
    + [347.前k个高频元素](#347前k个高频元素)
    + [350.两个数组的交集 ii](#350两个数组的交集ii)
    + [377.组合总和ⅳ](#377组合总和iv)
    + [378.有序矩阵中的第k小的元素](#378有序矩阵中的第k小的元素)
    + [380.o1时间插入删除和获取随机元素](#380o1时间插入删除和获取随机元素)
    + [394.字符串解码★](#394字符串解码)
    + [395.至少有k个重复字符的最长子串](#395至少有-k-个重复字符的最长子串)
    + [399.除法求值★](#399除法求值)
    + [403.青蛙过河](#403青蛙过河)
    + [409.最长回文串](#409最长回文串)
    + [417.太平洋大西洋水流问题](#417太平洋大西洋水流问题)
    + [424.替换后的最长重复字符](#424替换后的最长重复字符)
    + [427.建立四叉树](#427建立四叉树)
    + [433.最小基因变化](#433最小基因变化)
    + [436.寻找右区间](#436寻找右区间)
    + [442.数组中的重复数字](#442数组中的重复数字)
    + [449.序列化和反序列化二叉搜索树](#449序列化和反序列化二叉搜索树)
    + [450.删除二叉搜索树中的节点](#450删除二叉搜索树中的节点)
    + [454.四数相加 ⅱ](#454四数相加ⅱ)
    + [462.最少移动次数使数组元素相等 ii](#462最少移动次数使数组元素相等ii)
    + [464.我能赢吗](#464我能赢吗)
    + [467.环绕字符串中唯一的子字符串](#467环绕字符串中唯一的子字符串)
    + [472.连接词](#472连接词)
    + [518.零钱兑换ii](#518零钱兑换ii)
    + [526.优美的排列](#526优美的排列)
    + [528.按权重随机选择](#528按权重随机选择)
    + [540.有序数组中的单一元素](#540有序数组中的单一元素)
    + [542.01矩阵](#542-01矩阵)
    + [543.二叉树的直径](#543二叉树的直径)
    + [547.省份数量](#547省份数量)
    + [572.另一颗树的子树](#572另一颗树的子树)
    + [647.回文子串 (与题5可做比较)](#647回文子串与题5可做比较)
    + [669.修剪二叉搜索树★](#669修剪二叉搜索树)
    + [675.为高尔夫比赛砍树](#675为高尔夫比赛砍树)
    + [691.贴纸拼词](#691贴纸拼词)
    + [692.前k个高频单词](#692前k个高频单词)
    + [698.划分为k个相等的子集](#698划分为k个相等的子集)
    + [700.二叉搜索树中的搜索](#700二叉搜索树中的搜索)
    + [713.乘积小于k的子数组](#713乘积小于k的子数组)
    + [735.行星碰撞](#735行星碰撞)
    + [752.打开转盘锁★](#752打开转盘锁)
    + [767.重构字符串](#767重构字符串)
    + [812.最大三角形面积](#812最大三角形面积)
    + [815.公交路线★](#815公交路线)
    + [856.括号的分数](#856括号的分数)
    + [863.二叉树中所有距离为k的结点](#863二叉树中所有距离为-k-的结点)
    + [876.链表的中间结点](#876链表的中间结点)
    + [895.最大频率栈](#895最大频率栈)
    + [905.按奇偶排序数组](#905按奇偶排序数组)
    + [933.最近的请求次数](#933最近的请求次数)
    + [942.增减字符串匹配](#942增减字符串匹配)
    + [944.删列造序](#944删列造序)
    + [951.翻转等价二叉树](#951翻转等价二叉树)
    + [953.验证外星语词典](#953验证外星语词典)
    + [961.在长度2n的数组中找出重复n次的元素](#961在长度2n的数组中找出重复n次的元素)
    + [965.单值二叉树](#965单值二叉树)
    + [973.最接近原点的k个点](#973最接近原点的k个点)
    + [987.二叉树的垂序遍历](#987二叉树的垂序遍历)
    + [1004.最大连续1的个数 iii](#1004最大连续1的个数-iii)
    + [1021.删除最外层的括号](#1021删除最外层的括号)
    + [1022.从根到叶的二进制数之和](#1022从根到叶的二进制数之和)
    + [1091.二进制矩阵中的最短路径](#1091二进制矩阵中的最短路径)
    + [1095.山脉数组中查找目标值](#1095山脉数组中查找目标值)
    + [1110.删点成林★](#1110删点成林)
    + [1209.删除字符串中的所有相邻重复项 ii](#1209删除字符串中的所有相邻重复项-ii)
    + [1235.规划兼职工作](#1235规划兼职工作)
    + [1249.移除无效的括号](#1249移除无效的括号)
    + [1293.网格中的最短路径](#1293网格中的最短路径)
    + [1300.转变数组后最接近目标值的数组和](#1300转变数组后最接近目标值的数组和)
    + [1305.两棵二叉搜索树中的所有元素](#1305两棵二叉搜索树中的所有元素)
    + [1376.通知所有员工所需的时间](#1376通知所有员工所需的时间)
    + [1423.可获得的最大点数](#1423可获得的最大点数)
    + [1438.绝对差不超过限制的最长连续子数组](#1438绝对差不超过限制的最长连续子数组)
    + [1472.设计浏览器历史记录](#1472设计浏览器历史记录)
    + [1823.找出游戏的获胜者](#1823找出游戏的获胜者)
+ [3.面试题系列](#3面试题系列)
    + [01.05.一次编辑](#0105一次编辑)
    + [04.06.后继者](#0406后继者)
    + [17.11.单词距离](#1711单词距离)

+ [4.剑指offer](#4剑指offer)
    + [05.替换空格](#05替换空格)
    + [06.从尾到头打印链表](#06从尾到头打印链表)
    + [09.用两个栈实现队列](#09用两个栈实现队列)
    + [10-i.斐波那契数列](#10-i斐波那契数列)
    + [10-ii.青蛙跳台阶问题](#10-ii青蛙跳台阶问题)
    + [18.删除链表的节点](#18删除链表的节点)
    + [22.链表中倒数第k个节点](#22链表中倒数第k个节点)
    + [24.反转链表](#24反转链表)
    + [26.树的子结构](#26树的子结构)
    + [27.二叉树的镜像](#27二叉树的镜像)
    + [28.对称的二叉树](#28对称的二叉树)
    + [30.包含min函数的栈](#30包含min函数的栈)
    + [32-i.从上到下打印二叉树](#32-i从上到下打印二叉树)
    + [32-ii.从上到下打印二叉树ii](#32-ii从上到下打印二叉树ii)
    + [32-iii.从上到下打印二叉树iii](#32-iii从上到下打印二叉树iii)
    + [35.复杂链表的复制](#35复杂链表的复制)
    + [42.连续子数组的最大和](#42连续子数组的最大和)
    + [46.把数字翻译成字符串](#46把数字翻译成字符串)
    + [47.礼物的最大价值](#47礼物的最大价值)
    + [48.最长不含重复字符的子字符串](#48最长不含重复字符的子字符串)
    + [58-ii.左旋转字符串](#58-ii左旋转字符串)
    + [63.股票的最大利润](#63股票的最大利润)
    + [64.求1+2+...+n](#64求12n)
    + [65.不用加减乘除做加法](#65不用加减乘除做加法)
    + [66.构建乘积数组](#66构建乘积数组)
    + [67.把字符串转换成整数](#67把字符串转换成整数)

## 1.基础知识
### 1.1 排序算法（java实现）
#### 1.1.1 选择排序
> 简单选择排序是最简单直观的一种算法，基本思想为每一趟从待排序的数据元素中选择最小（或最大）的一个元素作为首元素，直到所有元素排完为止，简单选择排序是不稳定排序。  
在算法实现时，每一趟确定最小元素的时候会通过不断地比较交换来使得首位置为当前最小，交换是个比较耗时的操作。其实我们很容易发现，在还未完全确定当前最小元素之前，这些交换都是无意义的。我们可以通过设置一个变量min，每一次比较仅存储较小元素的数组下标，当轮循环结束之后，那这个变量存储的就是当前最小元素的下标，此时再执行交换操作即可。 

```java
    public static void selectSort(int[] arr) {
        for (int i = 0; i < arr.length - 1; i++) {
            int min = i;//每一趟循环比较时，min用于存放较小元素的数组下标，这样当前批次比较完毕最终存放的就是此趟内最小的元素的下标，避免每次遇到较小元素都要进行交换。
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[j] < arr[min]) {
                    min = j;
                }
            }
            //进行交换，如果min发生变化，则进行交换
            if (min != i) {
                swap(arr,min,i);
            }
        }
    }
```
#### 1.1.2 冒泡排序
> 冒泡排序的基本思想是，对相邻的元素进行两两比较，顺序相反则进行交换，这样，每一趟会将最小或最大的元素`浮`到顶端，最终达到完全有序 

示例：  
![冒泡排序示例](/image/sort/冒泡排序.png)

```java
    public static void bubbleSort(int[] arr) {
        for (int i = 0; i < arr.length - 1; i++) {
            boolean flag = true;//设定一个标记，若为true，则表示此次循环没有进行交换，也就是待排序列已经有序，排序已然完成。
            for (int j = 0; j < arr.length - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    swap(arr,j,j+1);
                    flag = false;
                }
            }
            if (flag) {
                break;
            }
        }
    }
```
#### 1.1.3插入排序
> 直接插入排序基本思想是每一步将一个待排序的记录，插入到前面已经排好序的有序序列中去，直到插完所有元素为止。  

示例：  
![直接插入排序示例](/image/sort/直接插入排序.png)

```java
    public static void insertionSort(int[] arr) {
        for (int i = 1; i < arr.length; i++) {
            int j = i;
            while (j > 0 && arr[j] < arr[j - 1]) {
                swap(arr,j,j-1);
                j--;
            }
        }
    }
```
#### 1.1.4 快速排序
> 快速排序(Quick Sort)使用分治法策略。  
它的基本思想是：选择一个基准数，通过一趟排序将要排序的数据分割成独立的两部分；其中一部分的所有数据都比另外一部分的所有数据都要小。然后，再按此方法对这两部分数据分别进行快速排序，整个排序过程可以递归进行，以此达到整个数据变成有序序列。  
**快速排序流程**：  
(1) 从数列中挑出一个基准值。  
(2) 将所有比基准值小的摆放在基准前面，所有比基准值大的摆在基准的后面(相同的数可以到任一边)；在这个分区退出之后，该基准就处于数列的中间位置。  
(3) 递归地把"基准值前面的子数列"和"基准值后面的子数列"进行排序。  

示例(**第一轮**)  
![快速排序第一轮示例](/image/sort/快速排序.jpg)

```java
    /*
     * 快速排序
     *
     * 参数说明：
     *     a -- 待排序的数组
     *     l -- 数组的左边界(例如，从起始位置开始排序，则l=0)
     *     r -- 数组的右边界(例如，排序截至到数组末尾，则r=a.length-1)
     */
    public static void quickSort(int[] a, int l, int r) {

        if (l < r) {
            int i,j,x;

            i = l;
            j = r;
            x = a[i];
            while (i < j) {
                while(i < j && a[j] > x)
                    j--; // 从右向左找第一个小于x的数
                if(i < j)
                    a[i++] = a[j];
                while(i < j && a[i] < x)
                    i++; // 从左向右找第一个大于x的数
                if(i < j)
                    a[j--] = a[i];
            }
            a[i] = x;
            quickSort(a, l, i-1); /* 递归调用 */
            quickSort(a, i+1, r); /* 递归调用 */
        }
    }
```

#### 1.1.5 归并排序
> 归并排序（MERGE-SORT）是利用归并的思想实现的排序方法，该算法采用经典的分治（divide-and-conquer）策略:分治法将问题分(divide)成一些小的问题然后递归求解，而治(conquer)的阶段则将分的阶段得到的各答案"修补"在一起，即分而治之。
+ top down
这种结构很像一棵完全二叉树，本文的归并排序我们采用递归去实现（也可采用迭代的方式去实现）。分阶段可以理解为就是递归拆分子序列的过程，递归深度为log2n。  
![归并排序top down总思路](/image/sort/归并排序1.png)  
治阶段，我们需要将两个已经有序的子序列合并成一个有序序列，比如上图中的最后一次合并，要将[4,5,7,8]和[1,2,3,6]两个已经有序的子序列，合并为最终序列[1,2,3,4,5,6,7,8]  
![归并排序top down治思路](/image/sort/归并排序2.png)  
最后  
![归并排序top down思路](/image/sort/归并排序3.png)  

```java
    public static void sort(int []arr){
        int []temp = new int[arr.length];//在排序前，先建好一个长度等于原数组长度的临时数组，避免递归中频繁开辟空间
        sort(arr,0,arr.length-1,temp);
    }
    private static void sort(int[] arr,int left,int right,int []temp){
        if(left<right){
            int mid = (left+right)/2;
            sort(arr,left,mid,temp);//左边归并排序，使得左子序列有序
            sort(arr,mid+1,right,temp);//右边归并排序，使得右子序列有序
            merge(arr,left,mid,right,temp);//将两个有序子数组合并操作
        }
    }
    private static void merge(int[] arr,int left,int mid,int right,int[] temp){
        int i = left;//左序列指针
        int j = mid+1;//右序列指针
        int t = 0;//临时数组指针
        while (i<=mid && j<=right){
            if(arr[i]<=arr[j]){
                temp[t++] = arr[i++];
            }else {
                temp[t++] = arr[j++];
            }
        }
        while(i<=mid){//将左边剩余元素填充进temp中
            temp[t++] = arr[i++];
        }
        while(j<=right){//将右序列剩余元素填充进temp中
            temp[t++] = arr[j++];
        }
        t = 0;
        //将temp中的元素全部拷贝到原数组中
        while(left <= right){
            arr[left++] = temp[t++];
        }
    }
```
+ bottom up
先两个两个的 merge，完成一趟后，再 4 个4个的 merge，直到结束  
> 例如[4,3,1,7,8,9,2,11,5,6]  
step=1: (3->4)->(1->7)->(8->9)->(2->11)->(5->6)  
step=2: (1->3->4->7)->(2->8->9->11)->(5->6)  
step=4: (1->2->3->4->7->8->9->11)->(5->6)  
step=8: (1->2->3->4->5->6->7->8->9->11)  

```
代码参照题目148的链表写法，换汤不换药
```

#### 1.1.6 希尔排序
> 希尔排序是把记录按下标的一定增量分组，对每组使用直接插入排序算法排序；随着增量逐渐减少，每组包含的关键词越来越多，当增量减至1时，整个文件恰被分成一组，算法便终止。  
希尔排序在数组中采用跳跃式分组的策略，通过某个增量将数组元素划分为若干组，然后分组进行插入排序，随后逐步缩小增量，继续按组进行插入排序操作，直至增量为1。希尔排序通过这种策略使得整个数组在初始阶段达到从宏观上看基本有序，小的基本在前，大的基本在后。然后缩小增量，到增量为1时，其实多数情况下只需微调即可，不会涉及过多的数据移动。  
我们来看下希尔排序的基本步骤，在此我们选择增量gap=length/2，缩小增量继续以gap = gap/2的方式，这种增量选择我们可以用一个序列来表示，{n/2,(n/2)/2...1}，称为增量序列。希尔排序的增量序列的选择与证明是个数学难题，我们选择的这个增量序列是比较常用的，也是希尔建议的增量，称为希尔增量，但其实这个增量序列不是最优的。此处我们做示例使用希尔增量。

示例:
![希尔排序示例](/image/sort/希尔排序.png)
```java
    /**
     * 希尔排序 针对有序序列在插入时采用交换法
     * @param arr
     */
    public static void sort(int []arr){
        //增量gap，并逐步缩小增量
       for(int gap=arr.length/2;gap>0;gap/=2){
           //从第gap个元素，逐个对其所在组进行直接插入排序操作
           for(int i=gap;i<arr.length;i++){
               int j = i;
               while(j-gap>=0 && arr[j]<arr[j-gap]){
                   //插入排序采用交换法
                   swap(arr,j,j-gap);
                   j-=gap;
               }
           }
       }
    }

    /**
     * 希尔排序 针对有序序列在插入时采用移动法。
     * @param arr
     */
    public static void sort1(int []arr){
        //增量gap，并逐步缩小增量
        for(int gap=arr.length/2;gap>0;gap/=2){
            //从第gap个元素，逐个对其所在组进行直接插入排序操作
            for(int i=gap;i<arr.length;i++){
                int j = i;
                int temp = arr[j];
                if(arr[j]<arr[j-gap]){
                    while(j-gap>=0 && temp<arr[j-gap]){
                        //移动法
                        arr[j] = arr[j-gap];
                        j-=gap;
                    }
                    arr[j] = temp;
                }
            }
        }
    }
    /**
     * 交换数组元素
     * @param arr
     * @param a
     * @param b
     */
    public static void swap(int []arr,int a,int b){
        arr[a] = arr[a]+arr[b];
        arr[b] = arr[a]-arr[b];
        arr[a] = arr[a]-arr[b];
    }
```

#### 1.1.7 堆排序
> 堆排序是利用堆这种数据结构而设计的一种排序算法，堆排序是一种选择排序，它的最坏，最好，平均时间复杂度均为O(nlogn)，它也是不稳定排序。  

堆是具有以下性质的完全二叉树：每个结点的值都大于或等于其左右孩子结点的值，称为大顶堆；或者每个结点的值都小于或等于其左右孩子结点的值，称为小顶堆。  
![大顶堆、小顶堆](/image/sort/堆排序1.png)  
对堆中的结点按层进行编号，将这种逻辑结构映射到数组中就是下面这个样子  
![数组表示结果](/image/sort/堆排序2.png)  
该数组从逻辑上讲就是一个堆结构，我们用简单的公式来描述一下堆的定义就是  
+ 大顶堆：arr[i] >= arr[2i+1] && arr[i] >= arr[2i+2] 
+ 小顶堆：arr[i] <= arr[2i+1] && arr[i] <= arr[2i+2]

**基本过程(以大顶堆为例)**
> 将待排序序列构造成一个大顶堆，此时，整个序列的最大值就是堆顶的根节点。将其与末尾元素进行交换，此时末尾就为最大值。然后将剩余n-1个元素重新构造成一个堆，这样会得到n个元素的次小值。如此反复执行，便能得到一个有序序列了

step 1: 构造初始堆。将给定无序序列构造成一个大顶堆（一般升序采用大顶堆，降序采用小顶堆)。  
|序号|说明|示意图|
|:-:|-|:-:|
|1|假设给定无序序列结构|![示例](/image/sort/堆排序3.png)|
|2|从最后一个非叶子结点开始（叶结点自然不用调整，第一个非叶子结点 arr.length/2-1=5/2-1=1，也就是下面的6结点），从左至右，从下至上进行调整|![找最后一个非叶子结点](/image/sort/堆排序4.png)|
|3|找到第二个非叶节点4，由于[4,9,8]中9元素最大，4和9交换|![找下一个相邻的非叶子节点](/image/sort/堆排序5.png)|
|4|交换导致了子根[4,5,6]结构混乱，继续调整，[4,5,6]中6最大，交换4和6。我们就将一个无需序列构造成了一个大顶堆|![调整子树](/image/sort/堆排序6.png)|  

step 2: 将堆顶元素与末尾元素进行交换，使末尾元素最大。然后继续调整堆，再将堆顶元素与末尾元素交换，得到第二大元素。如此反复进行交换、重建、交换。  
|序号|说明|示意图|
|:-:|-|:-:|
|1|将堆顶元素9和末尾元素4进行交换|![示例](/image/sort/堆排序7.png)|
|2|重新调整结构，使其继续满足堆定义|![示例](/image/sort/堆排序8.png)|
|3|再将堆顶元素8与末尾元素5进行交换，得到第二大元素8|![示例](/image/sort/堆排序9.png)|
|4|后续过程，继续进行调整，交换，如此反复进行，最终使得整个序列有序|![示例](/image/sort/堆排序10.png)|

```java
    public static void sort(int []arr){
        //1.构建大顶堆
        for(int i=arr.length/2-1;i>=0;i--){
            //从第一个非叶子结点从下至上，从右至左调整结构
            adjustHeap(arr,i,arr.length);
        }
        //2.调整堆结构+交换堆顶元素与末尾元素
        for(int j=arr.length-1;j>0;j--){
            swap(arr,0,j);//将堆顶元素与末尾元素进行交换
            adjustHeap(arr,0,j);//重新对堆进行调整
        }

    }

    /**
     * 调整大顶堆（仅是调整过程，建立在大顶堆已构建的基础上）
     * @param arr
     * @param i
     * @param length
     */
    public static void adjustHeap(int []arr,int i,int length){
        int temp = arr[i];//先取出当前元素i
        for(int k=i*2+1;k<length;k=k*2+1){//从i结点的左子结点开始，也就是2i+1处开始
            if(k+1<length && arr[k]<arr[k+1]){//如果左子结点小于右子结点，k指向右子结点
                k++;
            }
            if(arr[k] >temp){//如果子节点大于父节点，将子节点值赋给父节点（不用进行交换）
                arr[i] = arr[k];
                i = k;
            }else{
                break;
            }
        }
        arr[i] = temp;//将temp值放到最终的位置
    }

    /**
     * 交换元素
     * @param arr
     * @param a
     * @param b
     */
    public static void swap(int []arr,int a ,int b){
        int temp=arr[a];
        arr[a] = arr[b];
        arr[b] = temp;
    }
```

### 1.2 同向双指针/滑动窗口
#### 1.2.1 常用模板
```python
1. 定义需要用到的变量，如快慢指针int slow = 0, int fast = 0; 输入的string s; 
Hashmap char_freq用于记录string s当中slow到fast（包含）之间所有的字母出现的频率；
int longest记录符合题目要求的最长substring长度等

2. 定义双while循环
while fast < len(s)：
    char_freq[s[fast]] = char_freq.get(s[fast], 0) + 1
    ......
    ......
    while 符合slow指针移动的条件:
        char_freq[s[slow]] -= 1
        ......
        ......
        slow += 1
    if 符合某些判断条件:
        longest = max(longest, fast - slow + 1)
    fast += 1
return longest
```
#### 1.2.2 代表题目
395、340、424、76、3、1004、713

### 1.3 宽度优先搜索BFS
> BFS常用于**层序遍历**和**最短路径**

![DFS、BFS示意图](/image/bfs/DFS和BFS示意图1.gif)

#### 1.3.1 二叉树上 `DFS` 与 `BFS` 代码比较  
+ DFS遍历使用**递归**
    ```python
        def dfs(root: TreeNode):
            if not root:
                return 
            dfs(root.left)
            dfs(root.right)
    ```
+ BFS遍历使用**队列**
    ```python
    def bfs(root: TreeNode):
        if not root:
            return
        queue = [root]
        while queue:
            node = queue.pop(0)
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)
    ```

#### 1.3.2 BFS应用1：层序遍历

什么是层序遍历呢？简单来说，层序遍历就是把二叉树分层，然后每一层从左到右遍历：

![BFS示意图](/image/bfs/bfs2.jpg)

乍一看来，这个遍历顺序和 BFS 是一样的，我们可以直接用 BFS 得出层序遍历结果。然而，层序遍历要求的输入结果和 BFS 是不同的。层序遍历要求我们区分每一层，也就是返回一个二维数组。而 BFS 的遍历结果是一个一维数组，无法区分每一层。

![BFS示意图](/image/bfs/bfs3.jpg)

那么，怎么给 BFS 遍历的结果分层呢？我们首先来观察一下 BFS 遍历的过程中，结点进队列和出队列的过程：

![BFS示意图](/image/bfs/bfs4.gif)

截取 BFS 遍历过程中的某个时刻：

![BFS示意图](/image/bfs/bfs5.jpg)

可以看到，此时队列中的结点是 3、4、5，分别来自第 1 层和第 2 层。这个时候，第 1 层的结点还没出完，第 2 层的结点就进来了，而且两层的结点在队列中紧挨在一起，我们无法区分队列中的结点来自哪一层。

因此，我们需要稍微修改一下代码，在每一层遍历开始前，先记录队列中的结点数量 n（也就是这一层的结点数量），然后一口气处理完这一层的 n 个结点。

```python
def bfs(root: TreeNode):
    if not root:
        return
    queue = [root]
    while queue:
        for i in range(len(queue)):
            node = queue.pop(0)
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)
```

这样，我们就将 BFS 遍历改造成了层序遍历。在遍历的过程中，结点进队列和出队列的过程为：

![BFS示意图](/image/bfs/bfs6.gif)

#### 1.3.3 BFS应用2：最短路径/距离

#### 1.3.4 代表题目

130、752、815、1091、542、1293、417、207、210、310、433、675

### 1.4 深度优先搜索DFS
#### 1.4.1 岛屿类问题
1. 好题解  

    [巨好的帖子](https://leetcode-cn.com/problems/number-of-islands/solution/dao-yu-lei-wen-ti-de-tong-yong-jie-fa-dfs-bian-li-/)

2. 代表题目

    200、130、417、951

#### 1.4.2 树类问题
1. 直径长度

> 直径长度是任意两个结点路径长度中的最大值, 这条路径可能穿过也可能不穿过根结点。

2. 路径长度

> 两结点之间的路径长度是以它们之间**边的数目**表示

3. 二叉搜索树

>左子树的所有节点都小于当前节点，右子树的所有节点都大于当前节点，并且每棵子树都具有上述特点

4. 二叉树的深度

> 二叉树的深度为根节点到最远叶子节点的**最长路径**上的**节点数**。

5. 平衡二叉搜索树(AVL树)
    + 平衡二叉搜索树中每个结点的左子树和右子树的高度最多相差`1`
    + 平衡二叉搜索树的子树也是平衡二叉搜索树
    + 一棵存有` n `个结点的平衡二叉搜索树的高度是$O(logn)$

##### 1.4.2.1 代表题目
543、226、101☆、124、236、235、105、104、987、572☆、100☆、863、1110、1376  
二叉搜索树：230、98、669、700、108、109、285、1305、449

注：带☆的题目表示极度相似


#### 1.4.3 图类问题

### 1.5 回溯
#### 1.5.1 代表题目
51、52、126★、93、22、301★、37★、212★、79、131、17、39、40、216、78、90、46、47、77、698、526、1235

### 1.6 字典树Trie 
字典树基础知识看[这里](https://leetcode-cn.com/problems/implement-trie-prefix-tree/solution/gong-shui-san-xie-yi-ti-shuang-jie-er-we-esm9/)
#### 1.6.1 代表题目
208、212★、472

### 1.7 并查集
#### 1.7.1 基本概念
+ 并查集是一种数据结构
+ 并（Union），代表合并
+ 查（Find），代表查找
+ 集（Set），代表这是一个以字典为基础的数据结构，它的基本功能是合并集合中的元素，查找集合中的元素
+ 并查集的典型应用是有关连通分量的问题
+ 并查集解决单个问题（添加，合并，查找）的时间复杂度都是$O(1)$
+ 并查集可以应用到在线算法中

#### 1.7.2 实现
##### 1.7.2.1 数据结构
并查集跟树有些类似，只不过其与树是相反的。在树这个数据结构里面，每个节点会记录它的子节点。在并查集里，每个节点会记录它的父节点  
![并查集](/image/union/union_1.png)

如果节点是相互连通的（从一个节点可以到达另一个节点），那么他们在同一棵树里，或者说在同一个集合里，或者说他们的祖先是相同的

```python
class UnionFind:

    def __init__(self):
        """
        记录每个节点的父节点
        """
        self.father = {}
```
##### 1.7.2.2 初始化
把一个新节点添加到并查集中，它的父节点应该为空  
![并查集之添加](/image/union/union_2.png)

```python
def add(self, x):
        """
        添加新节点
        """
        if x not in self.father:
            self.father[x] = None
```
##### 1.7.2.3 合并两个节点
如果发现两个节点是连通的，那么就要把他们合并，也就是他们的祖先是相同的。这里究竟把谁当做父节点一般是没有区别的。  
![并查集之合并](/image/union/union_3.png)

```python
def merge(self, x, y, val):
        """
        合并两个节点
        """
        root_x, root_y = self.find(x), self.find(y)
        
        if root_x != root_y:
            self.father[root_x] = root_y
```
##### 1.7.2.4 查找祖先
查找祖先的方法是：如果节点的父节点不为空，那就不断迭代。  
![并查集之查找祖先](/image/union/union_4.png)

```python
def find(self, x):
        """
        查找根节点
        """
        root = x

        while self.father[root] != None:
            root = self.father[root]

        return root
```

如果我们树很深，比如说退化成链表，那么每次查询的效率都会非常低。所以我们要做一下**路径压缩**，也就是**把树的深度固定为2**。这么做可行的原因是，并查集只是记录了节点之间的连通关系，而节点相互连通只需要有一个相同的祖先就可以了。路径压缩可以用**递归**，也可以**迭代**。  
|压缩之前|压缩之后|
|:-----:|:-----:|
|![并查集之路径压缩1](/image/union/union_5.png)|![并查集之路径压缩2](/image/union/union_6.png)|
```python
def find(self, x):
        """
        查找根节点
        路径压缩
        """
        root = x

        while self.father[root] != None:
            root = self.father[root]

        # 路径压缩
        while x != root:
            original_father = self.father[x]
            self.father[x] = root
            x = original_father
         
        return root
```

##### 1.7.2.5 两节点是否连通
我们判断两个节点是否处于同一个连通分量的时候，就需要判断它们的祖先是否相同  
```python
def is_connected(self,x,y):
        """
        判断两节点是否相连
        """
        return self.find(x) == self.find(y)
```
#### 1.7.3 总体模板
```python
class UnionFind:
    def __init__(self):
        """
        记录每个节点的父节点
        """
        self.father = {}
    
    def find(self,x):
        """
        查找根节点
        路径压缩
        """
        root = x

        while self.father[root] != None:
            root = self.father[root]

        # 路径压缩
        while x != root:
            original_father = self.father[x]
            self.father[x] = root
            x = original_father
         
        return root
    
    def merge(self,x,y,val):
        """
        合并两个节点
        """
        root_x,root_y = self.find(x),self.find(y)
        
        if root_x != root_y:
            self.father[root_x] = root_y

    def is_connected(self,x,y):
        """
        判断两节点是否相连
        """
        return self.find(x) == self.find(y)
    
    def add(self,x):
        """
        添加新节点
        """
        if x not in self.father:
            self.father[x] = None
```
#### 1.7.4 代表题目
547、399

### 1.8 前缀和
#### 1.8.1 基础概念
> 前缀和本质上是在一个list当中，用O（N）的时间提前算好从第0个数字到第i个数字之和，在后续使用中可以在O（1）时间内计算出第i到第j个数字之和

+ 一维数组
例如数组`[1, 2, 3, 4, 5, 6]`，前缀和`[1, 3, 6, 10, 15, 21]`  
然而，实际我们在编写代码时，结果是`[0, 1, 3, 6, 10, 15, 21]`，这样前缀和的数组`index`就可以和**实际元素个数**对应起来了，比如`pre_sum[1]`代表**第1个**元素的和，`pre_sum[2]`就代表**前2个**元素的和......

+ 二维数组(例如[304.二维区域和检索-矩阵不可变](#304二维区域和检索-矩阵不可变))
    1. 定义` preSum[i][j] `表示 从` [0,0] `位置到` [i,j] `位置的子矩形所有元素之和
    2. `S(O,D) = S(O,C) + S(O,B) − S(O,A) + D`，减去` S(O, A) `的原因是` S(O, C) `和` S(O, B) `中都有` S(O, A) `，即加了两次` S(O, A) `，所以需要减去一次` S(O, A) `。  
    ![前缀和1](/image/prefix/prefix_1.png)

    3. 转换成前缀和，也就是`preSum[i][j] = preSum[i−1][j] + preSum[i][j−1] − preSum[i−1][j−1] + matrix[i][j]`
    4. 如何利用前缀和求解下图呢？  
    ![前缀和2](/image/prefix/prefix_2.png)  
    加上子矩形` S(O, G) `面积的原因是` S(O, E) `和` S(O, F) `中都有` S(O, G) `，即减了两次` S(O, G) `，所以需要加上一次` S(O, G) `
    5. 如果要求` [row1, col1] `到` [row2, col2] `的子矩形的面积的话，用` preSum `对应了递推公式：`preSum[row2][col2] - preSum[row2][col1 - 1] - preSum[row1 - 1][col2] + preSum[row1 - 1][col1 - 1]`


#### 1.8.2 代表题目
+ 一维数组前缀和
    303  
    + 一般语言而言，例如java可以
    ```java
        # 使用前缀和
        int n = nums.length;
        sums = new int[n + 1];
        for (int i = 0; i < n; i++) {
            sums[i + 1] = sums[i] + nums[i];
        }
    ```
    + 对于python而言，可以这么做
    ```python
        # 使用前缀和
        self.sum = [0]
        for i in nums:
            # self.sum[1]是nums第1个元素的和，self.sum[2]存的是nums前2个元素的和...
            self.sum.append(self.sum[-1] + i) 
    ```
+ 二维数组前缀和
    304、427

### 1.9 动态规划
> 这里指的是用`for`循环方式的动态规划，非`Memoization Search`方式。`DP`可以在多项式时间复杂度内解决`DFS`需要指数级别的问题。常见的题目包括找最大最小，找可行性，找总方案数等，一般结果是一个`Integer`或者`Boolean`。

#### 1.9.1 代表题目
139、72(类似**面试题 01.05. 一次编辑**)、377、518、70、97、403、53

## 2.题目
### 1.两数之和
> 给定一个整数数组 `nums` 和一个整数目标值 `target`，请你在该数组中找出 和为目标值 `target`  的那 两个 整数，并返回它们的数组下标。
你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。
你可以按任意顺序返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/two-sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  

```python
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        for i_index,i in enumerate(nums[:-1]):
            for j_index,j in enumerate(nums[i_index+1:],start=i_index+1):
                if i+j == target:
                    return [i_index,j_index]
```

### 2.两数相加
> 给你两个 非空 的链表，表示两个非负的整数。它们每位数字都是按照 逆序 的方式存储的，并且每个节点只能存储 一位 数字。
请你将两个数相加，并以相同形式返回一个表示和的链表。
你可以假设除了数字 0 之外，这两个数都不会以 0 开头。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/add-two-numbers  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
+ 法一 ~~这种写法很烂~~
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
            # 最特殊的情况是不一样长且存在进位
            result = [] # 存结果
            up = 0 # 进位符
            while l1!=None and l2!=None:
                temp = l1.val + l2.val
                if temp >= 10:
                    result.append(ListNode((temp + up) % 10, None))
                    up = 1
                else:
                    if temp == 9 and up == 1:
                        result.append(ListNode(0,None))
                        up = 1
                    else:
                        result.append(ListNode(temp + up,None))
                        up = 0
                l1 = l1.next
                l2 = l2.next
            
            # 假如两个list一样长
            if l1==None and l2==None:
                if up == 1:
                    result.append(ListNode(1,None))
            elif l1==None: # l2更长
                flag = 1
                temp = up + l2.val
                if temp >= 10:
                    while l2 != None:
                        temp = up + l2.val
                        l2.val = temp % 10
                        if flag == 1:
                            flag = 0
                            result.append(l2)
                        if temp >= 10:
                            up = 1
                        else:
                            up = 0
                        if l2.next == None and up == 1:
                            l2.next = ListNode(1,None)
                            break
                        else:
                            l2 = l2.next
                else: # 后续不用进位
                    l2.val = temp
                    result.append(l2)
            else: # l1更长
                flag = 1
                temp = up + l1.val
                if temp >= 10:
                    while l1 != None:
                        temp = up + l1.val
                        l1.val = temp % 10
                        if flag == 1:
                            flag = 0
                            result.append(l1)
                        if temp >= 10:
                            up = 1
                        else:
                            up = 0
                        if l1.next == None and up == 1:
                            l1.next = ListNode(1,None)
                            break
                        else:
                            l1 = l1.next
                else: # 后续不用进位
                    l1.val = temp
                    result.append(l1)


            # 连接ListNode
            for index in range(len(result)-1):
                result[index].next = result[index + 1]
            return result[0]

    ```
+ 法二
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
            # 最特殊的情况是不一样长且存在进位
            root = ListNode(0, None)
            current = root
            up = 0 # 进位符
            while l1 != None or l2 != None or up != 0:
                l1_value = l1.val if l1 != None else 0
                l2_value = l2.val if l2 != None else 0
                sum = l1_value + l2_value + up
                up = int(sum / 10)
                temp = ListNode(sum % 10, None)
                current.next = temp
                current = temp

                if l1 != None:
                    l1 = l1.next
                if l2 != None:
                    l2 = l2.next
            
            return root.next
    ```
### 3.无重复字符的最长子串
> 给定一个字符串` s` ，请你找出其中不含有重复字符的 **最长子串** 的长度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
 
```python
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        if len(s) == 0:
            return 0
        ans = 0
        char_freq = defaultdict(int)
        total = 0
        slow, fast = 0, 0
        while fast < len(s):
            char_freq[s[fast]] += 1
            if char_freq[s[fast]] == 1:
                total += 1
            while total < fast - slow + 1:
                char_freq[s[slow]] -= 1
                if char_freq[s[slow]] == 0:
                    total -= 1
                slow += 1
            ans = max(ans, fast - slow + 1)
            fast += 1
        return ans
```
### 4.寻找两个正序数组的中位数
> 给定两个大小分别为` m `和` n `的正序（从小到大）数组` nums1 `和` nums2`。请你找出并返回这两个正序数组的 `中位数` 。  
算法的时间复杂度应该为` O(log (m+n)) `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/median-of-two-sorted-arrays  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 二分查找 $O(log(m+n)).$
    ```python
    class Solution:
        def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
            # 二分查找
            m = len(nums1)
            n = len(nums2)
            # 求中位数是第几个数字，奇数的时候left和right一样
            left = int((m + n + 1)/2)
            right = int((m + n + 2)/2)
            return (self.getKthElement(nums1, 0, m-1, nums2, 0, n-1, left)+self.getKthElement(nums1, 0, m-1, nums2, 0, n-1, right))/2
        
        def getKthElement(self, nums1, start_1, end_1, nums2, start_2, end_2, k):
            length_1 = end_1 - start_1 + 1
            length_2 = end_2 - start_2 + 1
            if length_1 == 0:
                return nums2[start_2+k-1]
            if length_1 > length_2:
                return self.getKthElement(nums2, start_2, end_2, nums1, start_1, end_1, k)
            if k == 1:
                return min(nums1[start_1],nums2[start_2])
            
            # 比较k/2个元素的大小，小的一方全部排除
            element_1 = min(length_1, int(k/2))
            element_2 = min(length_2, int(k/2))
            if nums1[start_1+element_1-1] < nums2[start_2+element_2-1]:
                return self.getKthElement(nums1, start_1+element_1, end_1, nums2, start_2, end_2, k-element_1)
            else:
                return self.getKthElement(nums1, start_1, end_1, nums2, start_2+element_2, end_2, k-element_2)
            return 0.0

    ```
+ 中位数定义出发 $O(log min(m,n)).$
    ```python
    class Solution:
        def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
            # 二分查找
            m = len(nums1)
            n = len(nums2)
            # 保证muns1的长度最短，就以它为基准
            if m > n:
                return self.findMedianSortedArrays(nums2, nums1)
            # 对于短的nums1而言，长度为m，共有m+1种切割方式，最小是0位置，最大是m位置
            min_i, max_i = 0, m
            while min_i <= max_i:
                i = (max_i + min_i) // 2
                j = (m + n + 1) // 2 - i
                if  i != 0 and j != n and nums1[i-1] > nums2[j]:
                    max_i = i - 1
                elif i != m and j != 0 and nums2[j-1] > nums1[i]:
                    min_i = i + 1
                else:
                    max_left, min_right = 0, 0
                    if i == 0:
                        max_left = nums2[j-1]
                    elif j == 0:
                        max_left = nums1[i-1]
                    else:
                        max_left = max(nums1[i-1], nums2[j-1])
                    if (m + n) % 2 != 0:
                        return float(max_left)

                    if i == m:
                        min_right = nums2[j]
                    elif j == n:
                        min_right = nums1[i]
                    else:
                        min_right = min(nums1[i], nums2[j])
                    return float((max_left + min_right) / 2)
    ```
### 5.最长回文子串
> 给你一个字符串` s`，找到` s `中最长的回文子串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-palindromic-substring/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 动态规划，重点是找状态转移方程
    > `dp[left][right]=True`代表着`left`到`right`是回文串，那么如果`s[left-1]==s[right+1]`,那么`dp[left-1][right+1]=True`

    ```python
    class Solution:
        def longestPalindrome(self, s: str) -> str:
            n = len(s)
            # 构造n*n的状态转移矩阵
            # 想法是dp[left][right]=True代表着left到right是回文串，那么如果s[left-1]==s[right+1],那么dp[left-1][right+1]=True
            dp = [[False]*n for _ in range(n)]
            # 最长回文串长度
            max_l = 1
            # 最长回文串所对应的字符串
            max_s = s[0]
            # 每个字符本身就是回文串，即dp矩阵的对角线是True
            for i in range(n):
                dp[i][i] = True
            
            # 遍历所有可能的回文串长度，即2-n的情况
            for L in range(2, n+1):
                for i in range(n):
                    j = i + L - 1
                    if j > n-1:  # 下标越界了
                        break
                    if s[i] == s[j]:  # 相等即代表是回文串
                        if L > 2:
                            dp[i][j] = dp[i+1][j-1]
                        else:
                            dp[i][j] = True 
                    # 出现了当前的最长回文串
                    if L > max_l and dp[i][j]:
                        max_s = s[i:j+1]
                        max_l = L
            return max_s
    ```
### 8.字符串转换整数(atoi)
> 请你来实现一个` myAtoi(string s) `函数，使其能将字符串转换成一个` 32 `位有符号整数（类似 C/C++ 中的` atoi `函数）。

函数 `myAtoi(string s)` 的算法如下：

1. 读入字符串并丢弃无用的前导空格
2. 检查下一个字符（假设还未到字符末尾）为正还是负号，读取该字符（如果有）。 确定最终结果是负数还是正数。 如果两者都不存在，则假定结果为正。
3. 读入下一个字符，直到到达下一个非数字字符或到达输入的结尾。字符串的其余部分将被忽略。
4. 将前面步骤读入的这些数字转换为整数（即，"123" -> 123， "0032" -> 32）。如果没有读入数字，则整数为 0 。必要时更改符号（从步骤 2 开始）。
5. 如果整数数超过 32 位有符号整数范围 [−231,  231 − 1] ，需要截断这个整数，使其保持在这个范围内。具体来说，小于 −231 的整数应该被固定为 −231 ，大于 231 − 1 的整数应该被固定为 231 − 1 。
6.返回整数作为最终结果。

注意：
+ 本题中的空白字符只包括空格字符 ' ' 。
+ 除前导空格或数字后的其余字符串外，请勿忽略 任何其他字符。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/string-to-integer-atoi  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

![状态机](/image/offer/67.png)

```java
class Solution {
    // 状态机
    class Automaton {
        public String state = "start";
        public long ans;
        public int sign = 1;  // 该数字的正负情况，1代表正，0代表负\
        public Map<String, String[]> table = new HashMap<String, String[]>() {{
            put("start", new String[]{"start", "signed", "in_number", "end"});
            put("signed", new String[]{"end", "end", "in_number", "end"});
            put("in_number", new String[]{"end", "end", "in_number", "end"});
            put("end", new String[]{"end", "end", "end", "end"});
        }};

        public void get(char c) {
            state = table.get(state)[get_col(c)];
            if ("in_number".equals(state)) {
                ans = ans * 10 + c - '0';
                ans = sign == 1 ? Math.min(ans, (long) Integer.MAX_VALUE) : Math.min(ans, -(long) Integer.MIN_VALUE);
            } else if ("signed".equals(state)) {
                sign = c == '+' ? 1 : -1;
            }

        }

        public int get_col(char c) {
            if (c == ' ') {
                return 0;
            }
            if (c == '+' || c == '-') {
                return 1;
            }
            if (Character.isDigit(c)) {
                return 2;
            }
            return 3;

        }
    }

    public int myAtoi(String s) {
        Automaton automaton = new Automaton();
        int length = s.length();
        for (int i = 0; i < length; ++i) {
            automaton.get(s.charAt(i));
        }
        return (int) (automaton.sign * automaton.ans);
    }
}
```
### 11.盛水最多的容器
> 给定一个长度为` n `的整数数组` height `。有` n `条垂线，第` i `条线的两个端点是` (i, 0) `和 `(i, height[i])` 。  
找出其中的两条线，使得它们与` x `轴共同构成的容器可以容纳最多的水。  
返回容器可以储存的最大水量。

说明：你不能倾斜容器

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/container-with-most-water  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def maxArea(self, height: List[int]) -> int:
        # 双指针做法，物理意义代表着容器的左右边界
        left, right = 0, len(height) - 1
        ans = 0
        while left < right:
            area = min(height[left], height[right]) * (right - left)
            ans = max(ans, area)
            # 总是移动短的那根，抛弃掉
            if height[left] <= height[right]:
                left += 1
            else:
                right -= 1
        return ans
```
### 15.三数之和
> 给你一个包含` n `个整数的数组` nums`，判断` nums `中是否存在三个元素` a，b，c `，使得` a + b + c = 0 `？请你找出所有和为` 0 `且不重复的三元组。  
注意：答案中不可以包含重复的三元组。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/3sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        ans = []
        n = len(nums)
        if n < 3:
            return ans
        nums.sort()
        for i in range(n):
            # 第一个元素都大于0了，那和肯定不等于0
            if nums[i] > 0:
                return ans
            if i > 0 and nums[i] == nums[i-1]:
                continue
            left = i + 1
            right = n - 1
            while left < right:
                if nums[i] + nums[left] + nums[right] == 0:
                    ans.append([nums[i], nums[left], nums[right]])
                    while left < right and nums[left] == nums[left+1]:
                        left += 1
                    while left < right and nums[right] == nums[right-1]:
                        right -= 1
                    left += 1
                    right -= 1
                elif nums[i] + nums[left] + nums[right] > 0:
                    right -= 1
                else:
                    left += 1
        return ans
```
### 16.最接近的三数之和
> 给你一个长度为` n `的整数数组`` nums` 和 一个目标值` target`。请你从` nums `中选出三个整数，使它们的和与` target` 最接近。  
返回这三个数的和。  
假定每组输入只存在恰好一个解。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/3sum-closest  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def threeSumClosest(self, nums: List[int], target: int) -> int:
        n = len(nums)
        if n == 3:
            return sum(nums)
        # 先排序，再来枚举并且优化
        nums.sort()
        is_min = float('inf')
        ans = 0
        for i in range(n-2):
            left, right = i+1, n-1
            while left < right:
                three_sum = nums[i] + nums[left] + nums[right]
                if three_sum == target: #有且仅有一个解最接近，毫无疑问就是你了
                    return three_sum
                x = abs(three_sum - target)  # 差值
                if x < is_min:
                    is_min = x
                    ans =  three_sum
                if three_sum > target:
                    right -= 1
                else:
                    left += 1
        return ans
```
### 17.电话号码的字母组合
> 给定一个仅包含数字` 2-9 `的字符串，返回所有它能表示的字母组合。答案可以按 **任意顺序** 返回。  
给出数字到字母的映射如下（与电话按键相同）。注意` 1 `不对应任何字母。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/letter-combinations-of-a-phone-number  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
    ```python
    class Solution:
        def letterCombinations(self, digits: str) -> List[str]:
            if len(digits) == 0:
                return []
            
            # 字符串长度
            n = len(digits)
            ans = []

            def backtracing(tmp, start, n):
                if start == n:
                    ans.append(''.join(tmp))
                    return None
                # 把当前位的字符转成对应的整型数字
                num = int(digits[start])
                # 数字7,9对应的字符有四位，其余对应的字符只有3位
                sequence_length = 4 if num == 7 or num == 9 else 3
                for i in range(sequence_length):
                    # 构造当前字符
                    ch = chr(ord('a') + (num - 2) * 3 + i) if num <= 7 else chr(ord('a') + (num - 2) * 3 + 1 + i)
                    tmp.append(ch)
                    backtracing(tmp, start + 1, n)
                    # 回溯
                    tmp.pop()

            backtracing([], 0, n)
            return ans
    ```
### 18.四数之和
> 给你一个由` n `个整数组成的数组` nums `，和一个目标值` target `。请你找出并返回满足下述全部条件且不重复的四元组` [nums[a], nums[b], nums[c], nums[d]] `（若两个四元组元素一一对应，则认为两个四元组重复）： 
+ 0 <= a, b, c, d < n
+ a、b、c 和 d 互不相同
+ nums[a] + nums[b] + nums[c] + nums[d] == target
你可以按 **任意顺序** 返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/4sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def fourSum(self, nums: List[int], target: int) -> List[List[int]]:
        n = len(nums)
        if n < 4:
            return []
        ans = []
        nums.sort()
        for i in range(n-3):
            # while错了？
            if i > 0 and nums[i] == nums[i-1]:
                i += 1
                continue
            for j in range(i+1, n-2):
                # while错了？
                if j > i + 1 and nums[j] == nums[j-1]:
                    j += 1
                    continue
                left, right = j+1, n-1
                while left < right:
                    # 计算four sum
                    four_sum = nums[i] + nums[j] + nums[left] + nums[right]
                    # 找到了
                    if four_sum == target:
                        ans.append([nums[i], nums[j], nums[left], nums[right]])
                        left += 1
                        right -= 1
                    elif four_sum > target:
                        right -= 1
                    else:
                        left += 1
                    # 新的left or/and right跟上一次的值一样，重复了，不能取
                    while left < right and left > j + 1 and nums[left] == nums[left-1]:
                        left += 1

                    while left < right and right < n-1 and nums[right] == nums[right+1]:
                        right -= 1
        return ans
```
### 20.有效的括号
> 给定一个只包括 '('，')'，'{'，'}'，'['，']' 的字符串` s `，判断字符串是否有效。  
有效字符串需满足：  
左括号必须用相同类型的右括号闭合。  
左括号必须以正确的顺序闭合。  

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/valid-parentheses  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
```python
class Solution:
    def isValid(self, s: str) -> bool:
        stack = []
        for item in s:
            if item in ['(','{','[']:
                stack.append(item)
            else:
                if len(stack) == 0:
                    return False
                top = stack[-1]
                if (item == ')' and top == '(') or (item == '}' and top == '{') or (item == ']' and top == '['):
                    stack.pop()
                    continue
                return False
        return True if len(stack) == 0 else False
```
### 22.括号生成
> 数字` n `代表生成括号的对数，请你设计一个函数，用于能够生成所有可能的并且 **有效的** 括号组合。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/generate-parentheses/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
```python
class Solution:
    def generateParenthesis(self, n: int) -> List[str]:
        ans = []
        count_dict = collections.defaultdict(int)

        def backtracking(tmp, count_dict, start, n):
            # n对括号已经生成完毕
            if start == 2 * n:
                if count_dict['('] == count_dict[')']:
                    ans.append(''.join(tmp))
                return None
            # 右括号开头
            if len(tmp) > 0 and tmp[0] == ')':
                return None
            
            # 左括号或者右括号超过最大值了,或者右括号比左括号多
            if count_dict['('] > n or count_dict[')'] > n or count_dict['('] < count_dict[')']:
                return None

            for i in ['(', ')']:
                tmp.append(i)
                count_dict[i] += 1
                backtracking(tmp, count_dict, start + 1, n)
                # 回溯
                tmp.pop()
                count_dict[i] -= 1
        
        backtracking([], count_dict, 0, n)
        return ans
```
### 23.合并K个升序链表
> 给你一个链表数组，每个链表都已经按升序排列。  
请你将所有链表合并到一个升序链表中，返回合并后的链表。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/merge-k-sorted-lists/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def mergeKLists(self, lists: List[Optional[ListNode]]) -> Optional[ListNode]:
        min_heap = []
        for idx, value in enumerate(lists):
            if value:
                heapq.heappush(min_heap,(value.val,idx))
        dummy_head = ListNode(-1)
        curr = dummy_head
        while min_heap:
            val, idx = heapq.heappop(min_heap)
            curr.next = lists[idx]
            curr = curr.next
            lists[idx] = lists[idx].next
            if lists[idx]:
                heapq.heappush(min_heap,(lists[idx].val,idx))
        return dummy_head.next
```
### 26.删除有序数组中的重复项
> 给你一个 **升序排列** 的数组` nums `，请你**原地**删除重复出现的元素，使每个元素 **只出现一次** ，返回删除后数组的新长度。元素的**相对顺序** 应该保持 一致 。  
由于在某些语言中不能改变数组的长度，所以必须将结果放在数组`nums`的第一部分。更规范地说，如果在删除重复项之后有` k `个元素，那么` nums `的前` k `个元素应该保存最终结果。  
将最终结果插入` nums `的前` k `个位置后返回` k `。  
不要使用额外的空间，你必须在 **原地** 修改输入数组 并在使用` O(1) `额外空间的条件下完成

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/remove-duplicates-from-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        n = len(nums)
        if n < 2:
            return n
        slow, fast = 0, 1
        while fast < n:
            while fast < n and nums[slow] == nums[fast]:
                nums.pop(fast)
                n -= 1
            slow = fast
            fast += 1
        return n
```
### 27.移除元素
> 给你一个数组 `nums` 和一个值 `val`，你需要 `原地` 移除所有数值等于` val `的元素，并返回移除后数组的新长度。不要使用额外的数组空间，你必须仅使用` O(1) `额外空间并` 原地 `修改输入数组。元素的顺序可以改变。你不需要考虑数组中超出新长度后面的元素。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/remove-element  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ 法一：直接使用list自带函数remove
    ```python
    class Solution:
        def removeElement(self, nums: List[int], val: int) -> int:
            for i in range(nums.count(val)):
                nums.remove(val)
            return len(nums)
    ```

+ 法二：双指针做法
    ```python
    class Solution:
        def removeElement(self, nums: List[int], val: int) -> int:
            # 双指针做法
            start = 0
            end = len(nums) - 1
            if end < 0 or (end == 0 and nums[0] == val):
                return 0 # 要返回0 不能啥也不返回
            while start <= end:
                if nums[end] == val:
                    end = end - 1
                    continue
                if nums[start] == val:
                    nums[start] = nums[end]
                    nums[end] = val
                    end = end - 1
                start = start + 1
            return start
    ```
### 33.搜索旋转排序数组
> 整数数组` nums `按升序排列，数组中的值 **互不相同** 。  
在传递给函数之前，`nums `在预先未知的某个下标` k（0 <= k < nums.length）`上进行了 `旋转`，使数组变为 `[nums[k], nums[k+1], ..., nums[n-1], nums[0], nums[1], ..., nums[k-1]]`（下标 从 `0 `开始 计数）。例如， `[0,1,2,4,5,6,7] `在下标 `3 `处经旋转后可能变为` [4,5,6,7,0,1,2] `。  
给你 **旋转后** 的数组` nums `和一个整数` target `，如果 `nums` 中存在这个目标值` target` ，则返回它的下标，否则返回` -1 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/search-in-rotated-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 时间复杂度不符合要求
    ```python
    class Solution:
        def search(self, nums: List[int], target: int) -> int:
            length = len(nums)
            if length == 1:
                return 0 if target == nums[0] else -1

            left, right = 0, length -1
            # 可能整个数组都是单调的，这样必须判断left <= right，不然就越界了
            while left <= right and nums[left] > target:
                left += 1
            while left <= right and nums[right] < target:
                right -= 1

            while left <= right:
                # 左右区间已经固定好
                mid = (left + right) // 2
                if nums[mid] == target:
                    return mid
                elif nums[mid] < target:
                    left = mid + 1
                else:
                    right = mid - 1
            return -1
    ```
+ 虽然不能直接二分查找，但是算mid之后总有一半是有序的
    ```python
    class Solution:
        def search(self, nums: List[int], target: int) -> int:
            length = len(nums)
            if length == 1:
                return 0 if target == nums[0] else -1

            left, right = 0, length -1

            while left <= right:
                # 左右区间已经固定好
                mid = (left + right) // 2
                if nums[mid] == target:
                    return mid
                # 左边的区间是有序的
                if nums[left] <= nums[mid]:
                    if nums[left] <= target < nums[mid]:  # 值在区间内
                        right = mid - 1
                    else:
                        left = mid + 1
                # 右边的区间是有序的
                else:
                    if nums[mid] < target <= nums[right]:  # 值在区间内
                        left = mid + 1
                    else:
                        right = mid - 1
            return -1
    ```
### 34. 在排序数组中查找元素的第一个和最后一个位置
> 给定一个按照升序排列的整数数组` nums`，和一个目标值` target`。找出给定目标值在数组中的开始位置和结束位置。  
如果数组中不存在目标值` target`，返回` [-1, -1]`。

进阶：  
你可以设计并实现时间复杂度为` O(log n) `的算法解决此问题吗？

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def searchRange(self, nums: List[int], target: int) -> List[int]:
        def binarySearchLeft(nums, target):
            left = 0
            right = len(nums)   
            while left < right:
                mid = (right + left) // 2
                if nums[mid] < target:
                    left = mid + 1
                else:
                    right = mid
            return left
        
        if not nums:
            return [-1,-1]

        start = binarySearchLeft(nums,target)
        end = binarySearchLeft(nums,target+1) - 1
        if start == len(nums) or nums[start] != target:
            return [-1,-1]
        return [start,end]
```
### 37.解数独★
> 编写一个程序，通过填充空格来解决数独问题。

数独的解法需遵循如下规则：

+ 数字` 1-9 `在每一行只能出现一次。
+ 数字` 1-9 `在每一列只能出现一次。
+ 数字` 1-9 `在每一个以粗实线分隔的` 3x3 `宫内只能出现一次。

数独部分空格内已填入了数字，空白格用` '.'` 表示。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sudoku-solver  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
```python
class Solution:
    def solveSudoku(self, board: List[List[str]]) -> None:
        """
        Do not return anything, modify board in-place instead.
        """
        def is_valid(board, row, col, val):
            #判断行是否冲突
            for i in range(9):
                if board[i][col] == val:
                    return False
            #判断列是否冲突
            for i in range(9):
                if board[row][i] == val:
                    return False
            # 判断3*3的格子里是否冲突
            start_i = (row // 3) * 3
            start_j = (col // 3) * 3
            for i in range(start_i, start_i+3):
                for j in range(start_j, start_j+3):
                    if board[i][j] == val:
                        return False
            return True
        
        def backtracking(board): 
            for i in range(len(board)):
                for j in range(len(board[0])):
                    if board[i][j] != '.':
                        continue
                    # 数字是从1-9
                    for val in range(1, 10):
                        # 如果能把这个数字填进去，就进行下一个数字的填写
                        if is_valid(board, i, j, str(val)):
                            board[i][j] = str(val)
                            # 只要找到一个满足的条件，就可以return了
                            if backtracking(board):
                                return True
                            board[i][j] = '.'
                    # 说明1-9的数字都不能填到board[i][j]里面
                    return False
            return True

        backtracking(board)
```
### 39.组合总和
> 给你一个 **无重复元素** 的整数数组 `candidates` 和一个目标整数 `target` ，找出 `candidates` 中可以使数字和为目标数 `target` 的 **所有** 不同组合 ，并以列表形式返回。你可以按 **任意顺序** 返回这些组合。

`candidates` 中的 **同一个** 数字可以 无限制重复被选取 。如果至少一个数字的被选数量不同，则两种组合是不同的。   
对于给定的输入，保证和为` target `的不同组合数少于` 150 `个。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/combination-sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def combinationSum(self, candidates: List[int], target: int) -> List[List[int]]:
        # 回溯
        if min(candidates) > target:
            return []
        ans = []
        def is_valid(total, i):
            if total + i <= target:
                return True
            return False

        def backtracing(tmp, total, target):
            if total == target:
                res = sorted(tmp)
                if res not in ans:
                    ans.append(res)
                return None
            # 当前值+最小值都大于target了
            if min(candidates) + total > target:
                return None
            for i in candidates:
                if is_valid(total, i):
                    tmp.append(i)
                    backtracing(tmp, total + i, target)
                    tmp.pop()

        tmp = list()
        backtracing(tmp, 0, target)
        return ans
```
### 40.组合总和 II
> 给定一个候选人编号的集合` candidates `和一个目标数` target `，找出` candidates `中所有可以使数字和为` target `的组合。  
`candidates `中的每个数字在每个组合中只能使用 **一次** 。

注意：解集不能包含重复的组合。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/combination-sum-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯(这道题核心是剪枝，防止重复组合纳入结果中。首先需要对数组排序，其次就是`i > start`的理解，即`1，1`不跳过，`1，1，1`就要跳过)
```python
class Solution:
    def combinationSum2(self, candidates: List[int], target: int) -> List[List[int]]:
        # 回溯
        candidates.sort()
        ans = []
        def backtracing(tmp, start, total, n):
            if total == target:
                ans.append(tmp.copy())
                return None

            if total > target or start == n:
                return None
            
            for i in range(start, n):
                # 数组自增，当前都大于target了，往后的结果只会更大
                if total + candidates[i] > target:
                    break
                # i > start是核心(同一层的相邻且相同元素砍掉，相邻层的相邻相同元素保留)，这样1，1，6的第二个1可以正常拿进去，并且1，1，1，6的第三个1会跳过
                if i > start and candidates[i] == candidates[i-1]:
                    continue
                tmp.append(candidates[i])
                backtracing(tmp, i + 1, total + candidates[i], n)
                tmp.pop()

        backtracing([], 0, 0, len(candidates))

        return ans
```
### 46.全排列
> 给定一个不含重复数字的数组` nums `，返回其 所有可能的全排列 。你可以 **按任意顺序** 返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/permutations/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python回溯
    ```python
    class Solution:
        def permute(self, nums: List[int]) -> List[List[int]]:
            ans = []
            def backtracking(start, n):
                if start == n:
                    ans.append(nums[:])
                    return None
                for i in range(start, n):
                    nums[start] , nums[i] = nums[i], nums[start] 
                    backtracking(start + 1, n)
                    nums[start] , nums[i] = nums[i], nums[start] 

            backtracking(0, len(nums))
            return ans
    ```
+ java回溯
    ```java
    class Solution {

        public List<List<Integer>> permute(int[] nums) {
            List<List<Integer>> ans = new ArrayList<List<Integer>>();
            List<Integer> tmp = new ArrayList<Integer>();

            for(int item: nums)
                tmp.add(item);
            int n = nums.length;
            backtracking(ans, tmp, 0, n);
            return ans;
        }

        public void backtracking(List<List<Integer>> ans, List<Integer> tmp, int start, int n){
            if (start == n){
                ans.add(new ArrayList<Integer>(tmp));
                return ;
            }
            for(int i = start; i < n; i++){
                Collections.swap(tmp, start, i);
                backtracking(ans, tmp, start + 1, n);
                Collections.swap(tmp, start, i);
            }
        }

    }
    ```
### 47.全排列II
> 给定一个可包含重复数字的序列` nums `，按**任意顺序** 返回所有不重复的全排列。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/permutations-ii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 回溯
    ```python
    class Solution:
        def permuteUnique(self, nums: List[int]) -> List[List[int]]:
            # 给数组排序
            nums.sort()

            ans  = []
            visited = [False for _ in range(len(nums))]

            def backtracking(tmp, n):
                if len(tmp) == n:
                    ans.append(tmp[:])
                    return None
                for i in range(n):
                    if visited[i]:
                        continue
                    # 去重
                    if i > 0 and nums[i] == nums[i-1] and not visited[i-1]:
                        continue
                    tmp.append(nums[i])
                    visited[i] = True
                    backtracking(tmp, n)
                    tmp.pop()
                    visited[i] = False

            backtracking([], len(nums))
            return ans
    ```
### 49.字母异位词分组
> 给你一个字符串数组，请你将 **字母异位词** 组合在一起。可以按任意顺序返回结果列表。  
**字母异位词** 是由重新排列源单词的字母得到的一个新单词，所有源单词中的字母通常恰好只用一次。
 
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/group-anagrams  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        result = collections.defaultdict(list)
        for i in strs:
            key = ''.join(sorted(i))
            result[key].append(i)

        return list(result.values())
```
### 51.N皇后★
> **n皇后问题** 研究的是如何将` n `个皇后放置在` n×n `的棋盘上，并且使皇后彼此之间不能相互攻击。  
给你一个整数` n `，返回所有不同的**n皇后问题** 的解决方案。

每一种解法包含一个不同的 **n 皇后问题** 的棋子放置方案，该方案中` 'Q' `和` '.' `分别代表了皇后和空位。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/n-queens  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 回溯法
    ```python
    class Solution:
        def solveNQueens(self, n: int) -> List[List[str]]:
            # 回溯法，构造棋盘树，节点的子树数量等于列数，树的高度为行数
            if not n: 
                return []
            # 用点来初始化二位矩阵，后面再放置Q
            board = [['.'] * n for _ in range(n)]
            ans = []

            def is_vaild(board, row, col):
                # 在放置Q之前先检查一下是否合法
                # 判断同一列是否冲突
                for i in range(row):
                    if board[i][col] == 'Q':
                        return False

                # 判断左上角是否冲突
                i = row -1
                j = col -1
                while i >= 0 and j >= 0:
                    if board[i][j] == 'Q':
                        return False
                    i -= 1
                    j -= 1

                # 判断右上角是否冲突
                i = row - 1
                j = col + 1
                while i >= 0 and j < len(board):
                    if board[i][j] == 'Q':
                        return False
                    i -= 1
                    j += 1

                return True

            def backtracking(board, row, n):
                # 每一行都摆放完毕，而且可行，就记录答案
                if row == n:
                    temp_ans = []
                    for temp in board:
                        temp_str = "".join(temp)
                        temp_ans.append(temp_str)
                    ans.append(temp_ans)
                    return None
                for col in range(n):
                    if not is_vaild(board, row, col):
                        continue
                    board[row][col] = 'Q'
                    backtracking(board, row+1, n)
                    board[row][col] = '.'  # 回溯

            backtracking(board, 0, n)
            return ans
    ```
### 52.N皇后II
> **n 皇后问题** 研究的是如何将` n `个皇后放置在` n × n `的棋盘上，并且使皇后彼此之间不能相互攻击。  
给你一个整数` n `，返回**n 皇后问题** 不同的解决方案的数量。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/n-queens-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def totalNQueens(self, n: int) -> int:
        # 回溯法
        ans = 0
        board = [['.']*n for _ in range(n)]

        def is_valid(board, row, col):
            # 检查同一列是否含有皇后
            for i in range(row):
                if board[i][col] == 'Q':
                    return False
            # 检查左上角是否含有皇后
            i, j = row - 1, col - 1
            while i >= 0 and j >= 0:
                if board[i][j] == 'Q':
                    return False
                i -= 1
                j -= 1
            # 检查右上角是否含有皇后
            i, j = row - 1, col + 1
            while i >= 0 and j < n:
                if board[i][j] == 'Q':
                    return False
                i -= 1
                j += 1
            return True

        def backtracking(board, row):
            # 棋盘都摆放完毕了
            if row == n:
                nonlocal ans
                ans += 1
                return None
            for i in range(n):
                if not is_valid(board, row, i):
                    continue
                board[row][i] = 'Q'
                backtracking(board, row + 1)
                # 回溯
                board[row][i] = '.'
   
        backtracking(board, 0)
        return ans
```
### 53.最大子数组和
> 给你一个整数数组` nums `，请你找出一个具有最大和的连续子数组（子数组最少包含一个元素），返回其最大和。  
**子数组** 是数组中的一个连续部分。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/maximum-subarray/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。 

+ java 动态规划
```java
class Solution {
    public int maxSubArray(int[] nums) {
        int pre = 0;  // 计算
        int ans = nums[0];  // 最大值默认初始化
        for (int num: nums){
            pre = Math.max(num, pre + num);
            ans = Math.max(ans, pre);
        }
        return ans;
    }
}
```
### 54.螺旋矩阵
> 给你一个` m `行` n `列的矩阵` matrix `，请按照**顺时针**螺旋顺序 ，返回矩阵中的所有元素。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/spiral-matrix/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。 

```python
class Solution:
    def spiralOrder(self, matrix: List[List[int]]) -> List[int]:
        i, j = 0, len(matrix)-1
        result = []
        # 每转一圈只需要四步，直到转完
        while len(matrix[i]) > 0 and i <= j:
            # 第一步：往右到底，不用判断，直接拿进去
            result += matrix[i]
            i += 1
            if i > j:
                break
            # 第二步：往下直到倒数第二层，取最后一个值
            for idx in range(i,j):
                result.append(matrix[idx].pop())
            # 第三步：最后一层往左到底
            matrix[j].reverse()
            result += matrix[j]
            # 第四步：从底往上取第一个数
            j -= 1
            for idx in range(j,i-1,-1):
                # 得判断第一个数存不存在
                if len(matrix[idx]) == 0:
                    break
                result.append(matrix[idx].pop(0))
        return result
```
### 56.合并区间
> 以数组`intervals`表示若干个区间的集合，其中单个区间为`intervals[i] = [starti, endi]`。请你合并所有重叠的区间，并返回`一个不重叠的区间数组`，该数组需恰好覆盖输入中的所有区间。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/merge-intervals  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  

+ 快速排序
    ```python
    class Solution:
        def merge(self, intervals: List[List[int]]) -> List[List[int]]:
            if len(intervals) <= 1 :
                return intervals
            
            # 快速排序
            # import sys
            # sys.setrecursionlimit(1000000) # 修改python的递归深度限制
            self.quick_sort(intervals,0,len(intervals)-1)

            result = []
            # 两两配对
            for i in range(len(intervals)-1):
                # 前一个区间的最大值大于等于紧邻后者区间的最小值
                if intervals[i][1] >= intervals[i+1][0]:
                    # 因为可以合并，所以前一个区间看可以理解为没用了，只更新后者
                    intervals[i+1][0] = intervals[i][0]
                    intervals[i+1][1] = max(intervals[i][1],intervals[i+1][1])
                else: #不能合并
                    result.append(intervals[i])
            result.append(intervals[-1])

            return result

        def quick_sort(self, intervals, start, end):
            # 快速排序
            if start > end:
                return

            # 选择基准值
            base = intervals[start]
            l = start
            r = end

            # 把小于基准值的数放左边，大于基准值的放右边
            while l < r:
                while l < r:
                    if intervals[r][0] > base[0]:
                        r = r - 1
                    else:
                        intervals[l] = intervals[r]
                        l = l + 1
                        break
                while l < r:
                    if intervals[l][0] < base[0]:
                        l = l + 1
                    else:
                        intervals[r] = intervals[l]
                        r = r - 1
                        break
            intervals[l] = base
            # 左右递归求解
            self.quick_sort(intervals,start,l-1)
            self.quick_sort(intervals,l+1,end)
    ```
### 69.x的平方根
> 给你一个非负整数` x `，计算并返回` x `的 **算术平方根** 。  
由于返回类型是整数，结果只保留 **整数部分** ，小数部分将被 **舍去** 。  
注意：不允许使用任何内置指数函数和算符，例如 `pow(x, 0.5)` 或者 `x ** 0.5 `

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sqrtx  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def mySqrt(self, x: int) -> int:
        # 直接在0到x之间使用二分查找
        if x == 0:
            return 0
        left, right = 1, x
        ans = -1
        while left <= right:
            mid = left + (right - left) // 2
            if mid * mid <= x:
                ans = mid
                left = mid + 1
            else:
                right = mid - 1
        return ans
```
### 70.爬楼梯
> 假设你正在爬楼梯。需要` n `阶你才能到达楼顶。  
每次你可以爬` 1 `或` 2 `个台阶。你有多少种不同的方法可以爬到楼顶呢？

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/climbing-stairs/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 动态规划
    ```java
    class Solution {
        public int climbStairs(int n) {
            // 动态规划
            int[] dp = new int[n + 1];
            int[] nums = {1, 2};
            dp[0] = 1;
            for (int i = 0; i <= n; i++)
                for (int num: nums)
                    if (i - num >= 0)
                        dp[i] += dp[i - num];
            return dp[n];
        }
    }
    ```
### 72.编辑距离
> 给你两个单词` word1 `和` word2`， 请返回将` word1 `转换成 `word2 `所使用的最少操作数  。

你可以对一个单词进行如下三种操作：

+ 插入一个字符
+ 删除一个字符
+ 替换一个字符

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/edit-distance  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 记忆化搜索DFS
    ```java
    class Solution {
        public int minDistance(String word1, String word2) {
            // 记忆化DFS
            int[][] memo = new int[word1.length() + 1][word2.length() + 1];
            // 初始化记忆数组，值为-1，不能为0，因为0代表不需要操作，具有特殊含义
            // memo[i][j]代表word1的下标为i的字符与word2的下标为j的字符为起点需要的最小操作数
            for (int i = 0; i <= word1.length(); i++)
                for (int j = 0; j <= word2.length(); j++)
                    memo[i][j] = -1;

            return dfs(word1, 0, word2, 0, memo);
        }

        private int dfs(String w1, int i, String w2, int j, int[][] memo) {
            if (memo[i][j] != -1)
                // 当前位置之前已经计算过，直接返回记录
                return memo[i][j];
            if (i == w1.length())
                // word1已经遍历完毕，word2剩下的长度就是需要操作的长度
                return memo[i][j] = w2.length() - j;
            if (j == w2.length())
                // word2已经遍历完毕，word1剩下的长度就是需要操作的长度
                return memo[i][j] = w1.length() - i;
            if (w1.charAt(i) == w2.charAt(j))
                // 当前位置的两个元素相同，分别往后走一位
                return memo[i][j] = dfs(w1, i + 1, w2, j + 1, memo);
            // 当前位置不同，那么就有三种操作：1.word1替换一个，匹配成功，所以大家都往后走一位
            return memo[i][j] = Math.min(dfs(w1, i + 1, w2, j + 1, memo),
                                        // 2.word1删除一个就算匹配成功，然后word1下一个字符再来匹配  
                                Math.min(dfs(w1, i + 1, w2, j, memo), 
                                        // 3.word1插入一个就算匹配成功，然后word2下一个字符再来匹配
                                        dfs(w1, i, w2, j + 1, memo))) + 1;
        }

    }
    ```
+ java动态规划
    ```java
    class Solution {
        public int minDistance(String word1, String word2) {
            // 动态规划
            // dp[i][j]表示word1中前i个字符变成word2中前j个字符需要的最小操作次数
            int[][] dp = new int[word1.length() + 1][word2.length() + 1];

            // word1全部为空
            for (int i = 1; i <= word2.length(); i++)
                dp[0][i] = i;

            // word2全部为空
            for (int j = 1; j <= word1.length(); j++)
                dp[j][0] = j;

            // memo[i][j]代表word1的下标为i的字符与word2的下标为j的字符为起点需要的最小操作数
            for (int i = 1; i <= word1.length(); i++)
                for (int j = 1; j <= word2.length(); j++)
                    if (word1.charAt(i - 1) == word2.charAt(j - 1))
                        dp[i][j] = dp[i-1][j-1];
                    else
                        // dp[i-1][j-1] 替换
                        // dp[i-1][j]   删除
                        // dp[i][j-1]   插入
                        dp[i][j] = Math.min(dp[i-1][j-1], Math.min(dp[i-1][j], dp[i][j-1])) + 1;

            return dp[word1.length()][word2.length()];
        }

    }
    ```
### 73.矩阵置零
> 给定一个` m x n `的矩阵，如果一个元素为` 0 `，则将其所在行和列的所有元素都设为` 0 `。请使用 **原地** 算法。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/set-matrix-zeroes/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def setZeroes(self, matrix: List[List[int]]) -> None:
        """
        Do not return anything, modify matrix in-place instead.
        """
        # 使用O(1)的空间完成，说到底就是时间换空间
        # 查看第一行是不是存在0
        row_flag = True if 0 in matrix[0] else False
        # 查看第一列是不是存在0
        col_flag = False
        for idx in range(len(matrix)):
            if matrix[idx][0] == 0:
                col_flag = True
                break
        
        # 从第二行第二列开始遍历,遇到0就给对应的行和列做标记
        for i in range(1,len(matrix)):
            for j in range(1,len(matrix[0])):
                if matrix[i][j] == 0:
                    matrix[i][0] = matrix[0][j] = 0
        # 开始置0
        for i in range(1,len(matrix)):
            for j in range(1,len(matrix[0])):
                if matrix[0][j] == 0 or matrix[i][0] == 0:
                    matrix[i][j] = 0
        if row_flag:
            for idx in range(len(matrix[0])):
                matrix[0][idx] = 0
        
        if col_flag:
            for idx in range(len(matrix)):
                matrix[idx][0] = 0
```
### 74.搜索二维矩阵
> 编写一个高效的算法来判断` m x n `矩阵中，是否存在一个目标值。该矩阵具有如下特性：  
每行中的整数从左到右按升序排列。
每行的第一个整数大于前一行的最后一个整数。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/search-a-2d-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def searchMatrix(self, matrix: List[List[int]], target: int) -> bool:
        def binary_search(nums, left, right, target):
            while left <= right:
                mid = left + (right - left) // 2
                if nums[mid] == target:
                    return True
                if nums[mid] < target:
                    left = mid + 1
                else:
                    right = mid - 1
            return False

        m, n = len(matrix), len(matrix[0])
        for i in range(m):
            if target > matrix[i][n - 1]:
                continue
            else:
                return binary_search(matrix[i], 0, n-1, target)
        return False
```
### 75.颜色分类
> 给定一个包含红色、白色和蓝色、共 n 个元素的数组 nums ，原地对它们进行排序，使得相同颜色的元素相邻，并按照红色、白色、蓝色顺序排列。  
我们使用整数 0、 1 和 2 分别表示红色、白色和蓝色。  
必须在不使用库的sort函数的情况下解决这个问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sort-colors  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ 单指针
    ```python
    class Solution:
        def sortColors(self, nums: List[int]) -> None:
            """
            Do not return anything, modify nums in-place instead.
            """
            ptr = 0
            # 先排0，再排1
            for i in range(len(nums)):
                if nums[i] == 0:
                    self.swap(nums,i,ptr)
                    ptr += 1
            for i in range(ptr,len(nums)):
                if nums[i] == 1:
                    self.swap(nums,i,ptr)
                    ptr += 1
        
        def swap(self, nums, a, b):
            nums[a], nums[b] = nums[b], nums[a]
    ```
+ 双指针(0、1交换)
    ```python
    class Solution:
        def sortColors(self, nums: List[int]) -> None:
            """
            Do not return anything, modify nums in-place instead.
            """
            p_r, p_w = 0, 0
            for i in range(len(nums)):
                if nums[i] == 0:
                    self.swap(nums,i,p_r)
                    if p_r < p_w:  # 说明0后面已经有1排好了，上一行的swap把一个已经排好的1交换到i位置了，如果不继续交换，那么下次循环就到i+1位置了，这个1就被跳过了
                        self.swap(nums,i,p_w)
                    p_r += 1
                    p_w += 1
                elif nums[i] == 1:
                    self.swap(nums,i,p_w)
                    p_w += 1
        
        def swap(self, nums, a, b):
            nums[a], nums[b] = nums[b], nums[a]
    ```
+ 双指针(0、2交换)
    ```python
    class Solution:
        def sortColors(self, nums: List[int]) -> None:
            """
            Do not return anything, modify nums in-place instead.
            """
            n = len(nums)
            p_r, p_b = 0, n-1
            for i in range(n):
                if i > p_b:  # 这是元素已经被排过了
                    break
                while i <= p_b and nums[i] == 2:
                    self.swap(nums,i,p_b)
                    p_b -= 1
                if nums[i] == 0:
                    self.swap(nums,i,p_r)
                    p_r += 1
        
        def swap(self, nums, a, b):
            nums[a], nums[b] = nums[b], nums[a]
    ```
+ 三指针
    ```python
    class Solution:
        def sortColors(self, nums: List[int]) -> None:
            """
            Do not return anything, modify nums in-place instead.
            """
            p_r, p_w, p_b = 0, 0, 0   # 三个指针分别指向数组中下一个红、白、蓝应该插入的位置
            for color in nums:
                if color == 0:   # 当前元素是红色
                    nums[p_b] = 2
                    nums[p_w] = 1
                    nums[p_r] = 0
                    p_r = p_r + 1  # 最后一个红色位置后移1位
                    p_w = p_w + 1  # 最后一个白色位置后移1位
                    p_b = p_b + 1  # 最后一个蓝色位置后移1位
                elif color == 1: # 当前元素是白色
                    nums[p_b] = 2
                    nums[p_w] = 1
                    p_w = p_w + 1  # 最后一个白色位置后移1位
                    p_b = p_b + 1  # 最后一个蓝色位置后移1位
                else:            # 当前元素是蓝色
                    nums[p_b] = 2
                    p_b = p_b + 1  # 最后一个蓝色位置后移1位
    ```
### 76.最小覆盖子串
> 给你一个字符串` s `、一个字符串` t `。返回` s `中涵盖` t `所有字符的最小子串。如果` s `中不存在涵盖` t `所有字符的子串，则返回空字符串` "" `。

注意：  
+ 对于` t `中重复字符，我们寻找的子字符串中该字符数量必须不少于` t `中该字符数量。
+ 如果` s `中存在这样的子串，我们保证它是唯一的答案。
 
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/minimum-window-substring  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def minWindow(self, s: str, t: str) -> str:
        ans = ''
        if len(s) < len(t):
            return ans

        counter_t = collections.Counter(t)
        len_c_t = len(counter_t)
        slow, fast = 0, 0
        while fast < len(s):
            # 向右侧移动,让t中的字母都在窗口里出现且个数满足
            while len_c_t and fast < len(s):
                if s[fast] in counter_t:
                    counter_t[s[fast]] -= 1
                    if counter_t[s[fast]] == 0:
                        len_c_t -= 1
                fast += 1

            if fast == len(s) and len_c_t: break # 如果右侧指针到了结尾，且此刻不构成答案

            while not len_c_t and slow < fast:
                if s[slow] in counter_t:
                    counter_t[s[slow]] += 1
                    if counter_t[s[slow]] == 1:
                        len_c_t += 1
                slow += 1
            if not ans or len(ans) > fast - slow: # 更新答案
                ans = s[slow-1:fast]
        return ans
```
### 77.组合
> 给定两个整数` n `和` k`，返回范围` [1, n] `中所有可能的` k `个数的组合。  
你可以按 **任何顺序** 返回答案。

来源：力扣（LeetCode）  
https://leetcode-cn.com/problems/combinations/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ Java回溯
    ```java
    class Solution {
        public List<List<Integer>> combine(int n, int k) {
            List<List<Integer>> ans = new ArrayList<List<Integer>>();
            List<Integer> tmp = new ArrayList<Integer>();
            backtracking(ans, tmp, 1, n, k);
            return ans;
        }

        public void backtracking(List<List<Integer>> ans, List<Integer> tmp, int start, int n, int k){
            if(tmp.size() == k){
                //长度满足k了
                ans.add(new ArrayList<Integer>(tmp));
                return ;
            }
            for(int i = start; i <= n; i++){
                tmp.add(i);
                backtracking(ans, tmp, i + 1, n, k);
                tmp.remove(tmp.size()-1);
            }
        }
    }
    ```
### 78.子集
> 给你一个整数数组` nums `，数组中的元素 **互不相同** 。返回该数组所有可能的子集（幂集）。

解集 **不能** 包含重复的子集。你可以按 **任意顺序** 返回解集。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/subsets/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS
    ```python
    class Solution:
        def subsets(self, nums: List[int]) -> List[List[int]]:
            ans = []
            n = len(nums)
            
            def dfs(start, tmp):
                ans.append(tmp)
                for i in range(start, n):
                    dfs(i + 1, tmp + [nums[i]])
                    
            dfs(0, [])
            return ans
    ```
### 79.单词搜索
> 给定一个` m x n `二维字符网格` board `和一个字符串单词` word `。如果` word `存在于网格中，返回 `true `；否则，返回` false `。

单词必须按照字母顺序，通过相邻的单元格内的字母构成，其中“相邻”单元格是那些水平相邻或垂直相邻的单元格。同一个单元格内的字母不允许被重复使用。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/word-search  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
```python
class Solution:
    def exist(self, board: List[List[str]], word: str) -> bool:
        # 回溯
        def is_valid(position, start):
            x, y = position
            # 没有越界，并且没有访问过
            if 0 <= x < m and 0 <= y < n and position not in visited:
                return True
            return False
        
        def backtracing(position, start):
            x, y = position
            # 当前单词不匹配
            if board[x][y] != word[start]:
                return False
            # word的每一个单词都已经查找完毕了
            if start == len(word) - 1:
                return True
            # word中某个字符的总数量比board中该字符的总数量多，则不可能查找出来
            if word_count[word[start]] > board_count[word[start]]:
                return False
            ans = False
            visited.add((x, y))
            for new_x, new_y in [(x+1,y), (x-1, y), (x, y+1), (x, y-1)]:
                # 检查这个位置是否合法
                if is_valid((new_x, new_y), start):
                    if backtracing((new_x, new_y), start + 1):
                        ans = True
                        break
            visited.remove((x, y))
            return ans


        m, n = len(board), len(board[0])
        visited = set()
        # 统计board的字母词频
        board_count = collections.defaultdict(int)
        for i in range(m):
            for j in range(n):
                board_count[board[i][j]] += 1
        
        # 统计word的字母词频
        word_count = collections.Counter(word)

        for i in range(m):
            for j in range(n):
                if backtracing((i, j), 0):
                    return True
        return False
```
### 88.合并两个有序数组
> 给你两个按 **非递减顺序** 排列的整数数组` nums1 `和` nums2`，另有两个整数` m `和` n `，分别表示 `nums1 `和 `nums2` 中的元素数目。

请你 **合并** `nums2` 到 `nums1` 中，使合并后的数组同样按 **非递减顺序** 排列。

**注意：**最终，合并后数组不应由函数返回，而是存储在数组 `nums1` 中。为了应对这种情况，`nums1` 的初始长度为` m + n`，其中前` m `个元素表示应合并的元素，后` n `个元素为` 0` ，应忽略。`nums2 `的长度为` n `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/merge-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def merge(self, nums1: List[int], m: int, nums2: List[int], n: int) -> None:
        """
        Do not return anything, modify nums1 in-place instead.
        """
        p1, p2 = m-1, n-1
        tail = m + n - 1
        while p1 >= 0 or p2 >=0:
            if p1 < 0:
                nums1[tail] = nums2[p2]
                p2 -= 1
            elif p2 < 0:
                break
            elif nums1[p1] < nums2[p2]:
                nums1[tail] = nums2[p2]
                p2 -= 1
            else:
                nums1[tail] = nums1[p1]
                p1 -= 1
            tail -= 1
```
### 90.子集 II
> 给你一个整数数组` nums `，其中可能包含重复元素，请你返回该数组所有可能的子集（幂集）。

解集 **不能** 包含重复的子集。返回的解集中，子集可以按**任意顺序**排列。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/subsets-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python回溯
    ```python
    class Solution:
        def subsetsWithDup(self, nums: List[int]) -> List[List[int]]:
            # 先排序，转换成树型结构就是同一层的节点值不能相同
            nums.sort()
            ans = []
            n = len(nums)

            def backtracing(tmp, start):
                ans.append(tmp[:])
                for i in range(start, n):
                    if i > start and nums[i] == nums[i - 1]:
                        continue
                    tmp.append(nums[i])
                    backtracing(tmp, i + 1)
                    tmp.pop()

            backtracing([], 0)
            return ans
    ```

+ java回溯
    ```java
    class Solution {
        //保存答案
        public List<List<Integer>> ans = new ArrayList<List<Integer>>();
        public int n = 0;

        public List<List<Integer>> subsetsWithDup(int[] nums) {
            this.n = nums.length;
            List<Integer> tmp = new ArrayList<Integer>();
            Arrays.sort(nums);
            backtracking(tmp, nums, 0);
            return ans;
        }

        public void backtracking(List<Integer> tmp, int[] nums, int start){
            ans.add(new ArrayList<Integer>(tmp));
            for(int i = start; i < n; i ++){
                if (i > start && nums[i] == nums[i-1])
                    continue;
                tmp.add(nums[i]);
                backtracking(tmp, nums, i + 1);
                tmp.remove(tmp.size()-1);
            }
        }
    }
    ```
### 92.反转链表 II
> 给你单链表的头指针` head `和两个整数` left `和` right `，其中` left <= right `。请你反转从位置` left `到位置` right `的链表节点，返回**反转后的链表**

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/reverse-linked-list-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
+ 自己的解答 
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def reverseBetween(self, head: ListNode, left: int, right: int) -> ListNode:
            if left == right:
                return head
            p, q = head, head.next
            pre = tail = None
            count = 1
            while q:
                if count < left:
                    if count == left - 1:
                        pre = p
                    p = p.next
                    q = q.next
                    count += 1
                elif count >= left and count <= right:
                    if count == left:
                        tail = p
                    temp = q.next
                    q.next = p
                    p = q
                    q = temp
                    count += 1
                    if count == right:
                        break
            if pre:
                pre.next = p
                tail.next = q
                return head
            else:
                tail.next = q
                return p   
    ```
+ 官方解答更好
    ```python
    class Solution:
        def reverseBetween(self, head: ListNode, left: int, right: int) -> ListNode:
            # 设置 dummyNode 是这一类问题的一般做法
            dummy_node = ListNode(-1)
            dummy_node.next = head
            pre = dummy_node
            for _ in range(left - 1):
                pre = pre.next

            cur = pre.next
            for _ in range(right - left):
                next = cur.next
                cur.next = next.next
                next.next = pre.next
                pre.next = next
            return dummy_node.next
    ```
### 93.复原IP地址
> **有效 IP 地址** 正好由四个整数（每个整数位于` 0 `到` 255 `之间组成，且不能含有前导` 0`），整数之间用` '.' `分隔。  
例如：`"0.1.2.201" `和` "192.168.1.1"` 是 **有效** `IP` 地址，但是 `"0.011.255.245"`、`"192.168.1.312"` 和 `"192.168@1.1"` 是 **无效** `IP` 地址。  
给定一个只包含数字的字符串` s `，用以表示一个` IP `地址，返回所有可能的**有效 IP 地址**，这些地址可以通过在` s `中插入` '.' `来形成。你 **不能** 重新排序或删除` s `中的任何数字。你可以按 **任何** 顺序返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/restore-ip-addresses  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
    ```python
    class Solution:
        def restoreIpAddresses(self, s: str) -> List[str]:
            if len(s) < 4 or len(s) > 12:
                return []
            
            ans = []
            
            def is_valid(ch):
                # 0为先导
                if len(ch) > 1 and ch[0] == '0':
                    return False
                # 大于了255
                if len(ch) > 1 and int(ch) > 255:
                    return False
                return True

            def backtracking(tmp, split_times, n):
                # 本次递归开始处理的下标位置已经越界
                if n == len(s):
                    # 分了四次，说明成功了
                    if split_times == 4:
                        ans.append('.'.join(tmp))
                    return None
                
                # 如果还未处理的字符长度在规定次数内不够分，或者不能在规定次数内分割完
                # 比如字符是22143，现在是221.,可以看到剩余43再怎么分也分不出3段，这就是不够分
                # 比如字符是1112345，现在是1.1.1.,可以看到剩余2345再怎么分也不能在最后一次内分割完毕，这就是分不完
                if len(s) - n < (4 - split_times) or len(s) - n > 3 * (4 - split_times):
                    return None
                for i in range(3):
                    if n + i >= len(s):
                        break
                    ch = s[n: n+i+1]
                    if is_valid(ch):
                        tmp.append(ch)
                        backtracking(tmp, split_times +  1, n + i + 1)
                        # 回溯
                        tmp.pop()

            backtracking([], 0, 0)    
            return ans
    ```
### 97.交错字符串
> 给定三个字符串` s1、s2、s3`，请你帮忙验证` s3 `是否是由` s1 `和` s2 `**交错** 组成的。

两个字符串` s `和` t `交错 的定义与过程如下，其中每个字符串都会被分割成若干 **非空** 子字符串：

+ `s = s1 + s2 + ... + sn`
+ `t = t1 + t2 + ... + tm`
+ `|n - m| <= 1`
+ **交错** 是 `s1 + t1 + s2 + t2 + s3 + t3 + ... `或者` t1 + s1 + t2 + s2 + t3 + s3 + ...`

注意：`a + b `意味着字符串` a `和` b `连接。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/interleaving-string  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 动态规划
```java
class Solution {
    public boolean isInterleave(String s1, String s2, String s3) {
        // 定义字符的长度
        int len_1 = s1.length();
        int len_2 = s2.length();
        int len_3 = s3.length();
        if (len_1 + len_2 != len_3)
            return false;
        // dp[i][j]代表s1的前i个字符和s2的前j个字符能否组成s3的前i+j个字符
        boolean[][] dp  = new boolean[len_1 + 1][len_2 + 1];
        dp[0][0] = true;  // "" + "" = ""，当然可以

        //对dp数组的第一列进行处理
        //即由s1构成s3
        for (int i = 1; i <= len_1; i++)
            if (dp[i-1][0] && s1.charAt(i-1) == s3.charAt(i-1))
                dp[i][0] = true;
        
        //对dp数组的第一行进行处理
        //即由s2构成s3
        for (int i = 1; i <= len_2; i++)
            if (dp[0][i-1] && s2.charAt(i-1) == s3.charAt(i-1))
                dp[0][i] = true;

        for (int i = 1; i <= len_1; i++)
            for (int j = 1; j <= len_2; j++)
                //s1的前i-1和s2的前j个可以组合成s3的前i+j-1个，或者s1的前i和s2的前j-1个可以组合成s3的前i+j-1个
                if ((dp[i-1][j] && s1.charAt(i-1) == s3.charAt(i+j-1)) || (dp[i][j-1] && s2.charAt(j-1) == s3.charAt(i+j-1)))
                    dp[i][j] = true;
        
        return dp[len_1][len_2];

    }
}
```
### 98.验证二叉搜索树
> 给你一个二叉树的根节点` root `，判断其是否是一个有效的二叉搜索树。

**有效**二叉搜索树定义如下：

+ 节点的左子树只包含 **小于** 当前节点的数。
+ 节点的右子树只包含 **大于** 当前节点的数。
+ 所有左子树和右子树自身必须也是二叉搜索树。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/validate-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 中序遍历
    ```python
    # Definition for a binary tree node.
    # class TreeNode:
    #     def __init__(self, val=0, left=None, right=None):
    #         self.val = val
    #         self.left = left
    #         self.right = right
    class Solution:
        def isValidBST(self, root: TreeNode) -> bool:
            # 中序遍历
            # 错误：然后sort，判断sort前后数组是否相等即可,不行，比如树是2，2，2不是递增
            # 正确：遍历的时候就判断
            stack = []
            inorder = float('-inf')
            while root or stack:
                while root:
                    stack.append(root)
                    root = root.left
                root = stack.pop()
                # 如果中序遍历得到的节点的值小于等于前一个 inorder，说明不是二叉搜索树
                if root.val <= inorder:
                    return False
                inorder = root.val
                root = root.right

            return True
    ```
+ 递归
    ```python
    # Definition for a binary tree node.
    # class TreeNode:
    #     def __init__(self, val=0, left=None, right=None):
    #         self.val = val
    #         self.left = left
    #         self.right = right
    class Solution:
        def isValidBST(self, root: TreeNode) -> bool:
            # 递归
            def helper(node, lower = float('-inf'), upper = float('inf')) -> bool:
                if not node:
                    return True
                
                val = node.val
                if val <= lower or val >= upper:
                    return False

                if not helper(node.right, val, upper):
                    return False
                if not helper(node.left, lower, val):
                    return False
                return True

            return helper(root)

    ```
### 100.相同的树
> 给你两棵二叉树的根节点 `p `和 `q `，编写一个函数来检验这两棵树是否相同。

如果两个树在结构上相同，并且节点具有相同的值，则认为它们是相同的。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/same-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def isSameTree(self, p: TreeNode, q: TreeNode) -> bool:
        # 两棵树都为空
        if not p and not q:
            return True
        if not p or not q:
            return False
        
        return p.val == q.val and self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)
```
### 101.对称二叉树
> 给你一个二叉树的根节点` root `， 检查它是否轴对称。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/symmetric-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def isSymmetric(self, root: Optional[TreeNode]) -> bool:
        def check(first, second):
            if not first and not second:
                # 两棵树都是空
                return True
            if not first or not second:
                # 其中一棵树为空
                return False

            return first.val == second.val and check(first.left, second.right) and check(first.right, second.left)

        # 直接复制一棵树，然后来比
        return check(root, root)
```
### 102.二叉树的层序遍历
> 给你二叉树的根节点` root `，返回其节点值的 **层序遍历** 。 （即逐层地，从左到右访问所有节点）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/binary-tree-level-order-traversal/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def levelOrder(self, root: TreeNode) -> List[List[int]]:
        # 空，这棵树没有节点
        if not root:
            return []
        # queue队列用来添加节点，按照先进先出的顺序依次判断
        queue, ans = [root], []
        while queue:
            # layer用来存放每一层的输出结果
            layer = []
            for i in range(len(queue)):
                # 队头出
                node = queue.pop(0)
                if node.left:  # 这个节点有左孩子
                    queue.append(node.left)
                if node.right:  # 这个节点有右孩子
                    queue.append(node.right)
                layer.append(node.val)
            ans.append(layer)
        return ans
```
### 103.二叉树的锯齿形层序遍历
> 给你二叉树的根节点` root `，返回其节点值的 **锯齿形层序遍历** 。（即先从左往右，再从右往左进行下一层遍历，以此类推，层与层之间交替进行）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def zigzagLevelOrder(self, root: TreeNode) -> List[List[int]]:
        if not root:
            return []
        queue, ans = collections.deque(), []
        queue.append(root)
        while queue:
            layer = []
            for i in range(len(queue)):
                node = queue.popleft()
                if node.left:
                    queue.append(node.left)
                if node.right:
                    queue.append(node.right)
                layer.append(node.val)
            ans.append(layer)
        for idx in range(len(ans)): # 因为要求是锯齿遍历，所以要把偶数行给翻转一下
            if idx % 2 == 1: # 因为索引是从0开始的，所以这边判断余数是否为1
                ans[idx].reverse() # 如果是第偶数行，翻转，reverse是一个自带的反转函数，蛮好用的
        return ans
```
### 104.二叉树的最大深度
> 给定一个二叉树，找出其最大深度。  
二叉树的深度为根节点到最远叶子节点的最长路径上的节点数。

说明: 叶子节点是指没有子节点的节点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def maxDepth(self, root: Optional[TreeNode]) -> int:

        ans = 0

        def dfs(root):
            if not root:
                return 0
            left = dfs(root.left)
            right = dfs(root.right)
            nonlocal ans
            ans = max(ans, 1 + max(left, right))
            return 1 + max(left, right)

        dfs(root)
        return ans
```
### 105.从前序与中序遍历序列构造二叉树
> 给定两个整数数组` preorder `和` inorder` ，其中` preorder` 是二叉树的先序遍历，` inorder `是同一棵树的中序遍历，请构造二叉树并返回其根节点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def buildTree(self, preorder: List[int], inorder: List[int]) -> TreeNode:
        # 先序遍历结果[根节点，[左子树先序遍历结果]，[右子树先序遍历结果]]
        # 中序遍历结果[[左子树中序遍历结果]，根节点，[右子树中序遍历结果]]

        # 递归中止条件：树为空
        if not preorder or not inorder:
            return None
  
        # 根节点的值为前序遍历的第一个元素值
        root_val = preorder[0]
        # 创建根节点
        root = TreeNode(root_val)
  
        # 用根节点的值去中序数组中查找对应元素下标
        root_in = inorder.index(root_val)
  
        # 找出中序遍历的左子树和右子树
        # 左子树区间为 [0, root_in),右子树区间为[root_in+1，n-1]
        in_left = inorder[: root_in]
        in_right = inorder[root_in + 1:]
  
        # 找出前序遍历的左子树和右子树
        # 前序遍历和中序遍历的左子树和右子树长度相等，所以可以通过中序遍历左右子树的长度来确定前序遍历左右子树的位置
        pre_left = preorder[1: len(in_left) + 1]
        pre_right = preorder[len(in_left) + 1:]
  
        # 递归遍历左子树
        root.left = self.buildTree(pre_left, in_left)
        # 递归遍历右子树
        root.right = self.buildTree(pre_right, in_right)
  
        return root
```
### 108.将有序数组转换成二叉搜索树
> 给你一个整数数组` nums `，其中元素已经按 **升序** 排列，请你将其转换为一棵 **高度平衡** 二叉搜索树。

**高度平衡** 二叉树是一棵满足「每个节点的左右两个子树的高度差的绝对值不超过` 1` 」的二叉树。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/convert-sorted-array-to-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def sortedArrayToBST(self, nums: List[int]) -> Optional[TreeNode]:
        # 获取长度，根节点处于数组的中间
        if len(nums) == 0:
            return None
        mid = len(nums) // 2
        # 建立根节点
        root = TreeNode(nums[mid])
        root.left = self.sortedArrayToBST(nums[: mid])
        root.right = self.sortedArrayToBST(nums[mid + 1:])
        return root
```
### 109.有序链表转换二叉搜索树
> 给定一个单链表的头节点`  head `，其中的元素 **按升序排序** ，将其转换为高度平衡的二叉搜索树。

本题中，一个高度平衡二叉树是指一个二叉树每个节点 的左右两个子树的高度差不超过` 1`。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/convert-sorted-list-to-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def sortedListToBST(self, head: Optional[ListNode]) -> Optional[TreeNode]:
        if not head:
            return None

        if not head.next:
            return TreeNode(head.val)

        # 寻找链表中点
        mid = self.find_mid(head)
        root = TreeNode(mid.val)
        root.left = self.sortedListToBST(head)
        root.right = self.sortedListToBST(mid.next)
        return root

    def find_mid(self, head):
        pre, slow, fast = head, head.next, head.next.next
        while fast and fast.next:
            fast = fast.next.next
            slow = slow.next
            pre = pre.next
        # 把链表断开
        pre.next = None
        return slow
```
### 121.买卖股票的最佳时机
> 给定一个数组 prices ，它的第 i 个元素 prices[i] 表示一支给定股票第 i 天的价格。  
你只能选择 某一天 买入这只股票，并选择在 未来的某一个不同的日子 卖出该股票。设计一个算法来计算你所能获取的最大利润。  
返回你可以从这笔交易中获取的最大利润。如果你不能获取任何利润，返回 0 

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/best-time-to-buy-and-sell-stock  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public int maxProfit(int[] prices) {
        if (prices.length == 0) return 0;
        int buy = Integer.MAX_VALUE;
        int profit = 0;

        for (int price: prices) {
            // 我们需要最低价格买入
            buy = Math.min(buy, price);
            // 我们需要最高的利润
            profit = Math.max(profit, price - buy);
        }
        return profit;
    }
}
```
### 124.二叉树中的最大路径和
> **路径** 被定义为一条从树中任意节点出发，沿父节点-子节点连接，达到任意节点的序列。同一个节点在一条路径序列中 **至多出现一次** 。该路径 **至少包含一个** 节点，且不一定经过根节点。  
**路径和** 是路径中各节点值的总和。

给你一个二叉树的根节点` root `，返回其 **最大路径和** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/binary-tree-maximum-path-sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def maxPathSum(self, root: Optional[TreeNode]) -> int:

        ans = float('-inf')

        def dfs(root):
            if not root:
                return 0
            # 递归求解
            left_node = dfs(root.left)
            right_node = dfs(root.right)
            # 当前的最大路径
            nonlocal ans
            left = max(left_node, 0)
            right = max(right_node, 0)
            ans = max(ans, root.val + left + right)
            # 返回的是当前根节点作为子树所能提供的最大路径
            return root.val + max(left, right)
        
        dfs(root)
        return ans

```
### 125.验证回文串
> 给定一个字符串，验证它是否是回文串，只考虑字母和数字字符，可以忽略字母的大小写。  
说明：本题中，我们将空字符串定义为有效的回文串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/valid-palindrome/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
 
```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        n = len(s)
        left, right = 0, n-1
        while left < right:
            while left < right and not (s[left].isalpha() or s[left].isdigit()):
                left += 1
            while left < right and not (s[right].isalpha() or s[right].isdigit()):
                right -= 1
            if left < right:
                # 数字相等也是回文
                # 大小写字母对应的差值为32（0和P也是，妈的，有坑）
                if (s[left].isalpha() and s[right].isdigit()) or (s[left].isdigit() and s[right].isalpha()) or not (ord(s[left]) + 32 == ord(s[right]) or ord(s[left]) - 32 == ord(s[right]) or s[left] == s[right]):
                    return False
                else:
                    left += 1
                    right -= 1
        return True
```
### 126.单词接龙II★
> 按字典` wordList` 完成从单词 `beginWord` 到单词 `endWord` 转化，一个表示此过程的**转换序列** 是形式上像 `beginWord -> s1 -> s2 -> ... -> sk` 这样的单词序列，并满足：

+ 每对相邻的单词之间仅有单个字母不同。
+ 转换过程中的每个单词` si（1 <= i <= k）`必须是字典` wordList `中的单词。注意，`beginWord `不必是字典` wordList` 中的单词。
+ `sk == endWord`

给你两个单词 `beginWord` 和 `endWord` ，以及一个字典` wordList` 。请你找出并返回所有从 `beginWord` 到 `endWord` 的 **最短转换序列** ，如果不存在这样的转换序列，返回一个空列表。每个序列都应该以单词列表 `[beginWord, s1, s2, ..., sk] `的形式返回。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/word-ladder-ii 
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ BFS+DFS+回溯+队列
```python
class Solution:
    def findLadders(self, beginWord: str, endWord: str, wordList: List[str]) -> List[List[str]]:
        # 结尾单词并不存在于单词序列中
        if not endWord in wordList:
            return []
        word_set, level, has_sequence = set(wordList), 0, False
        # {word: a list of next words}
        word_next = collections.defaultdict(list)
        # {word: level of the word}
        word_level = {beginWord: level}
        # BFS 搜索队列
        queue = collections.deque([beginWord])

        # BFS构建word_next和word_level词典
        while queue:
            level += 1
            # 取出同一level的word
            for _ in range(len(queue)):
                w = queue.popleft()
                wl = list(w)
                for idx, c in enumerate(wl):
                    for j in range(26):
                        wl[idx] = chr(ord("a") + j)
                        nw = "".join(wl)
                        # 出现了新词
                        if nw != w and nw in word_set:
                            word_next[w].append(nw)
                            if nw not in word_level:
                                word_level[nw] = level
                                # 不是结尾单词，就加进队列
                                if nw != endWord:
                                    queue.append(nw)
                    # 字符还原
                    wl[idx] = c

        def backtrack(word, path):
            if word == endWord:
                return [list(path)]
            res = []
            for nw in word_next[word]:
                # level提升才继续回溯，否则就是同一层的词，没必要，显然不是最短路径
                if word_level[nw] == word_level[word] + 1:
                    path.append(nw)
                    res.extend(backtrack(nw, path))
                    path.pop()
            return res

        return backtrack(beginWord, [beginWord])
```
### 127.单词接龙
> 字典` wordList `中从单词` beginWord `和` endWord `的 **转换序列** 是一个按下述规格形成的序列 `beginWord -> s1 -> s2 -> ... -> sk`：  
+ 每一对相邻的单词只差一个字母。  
+ 对于 `1 <= i <= k` 时，每个 `si` 都在 `wordList` 中。注意， `beginWord` 不需要在 `wordList` 中。
+ `sk == endWord`  

给你两个单词 `beginWord` 和 `endWord` 和一个字典 `wordList` ，返回 从 `beginWord` 到 `endWord` 的 **最短转换序列** 中的 **单词数目** 。如果不存在这样的转换序列，返回` 0 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/word-ladder  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def ladderLength(self, beginWord: str, endWord: str, wordList: List[str]) -> int:
        def addWord(word: str):
            if word not in wordId:
                nonlocal nodeNum
                wordId[word] = nodeNum
                nodeNum += 1
        
        def addEdge(word: str):
            addWord(word)
            id1 = wordId[word]
            chars = list(word)
            for i in range(len(chars)):
                tmp = chars[i]
                chars[i] = "*"
                newWord = "".join(chars)
                addWord(newWord)
                id2 = wordId[newWord]
                edge[id1].append(id2)
                edge[id2].append(id1)
                chars[i] = tmp

        wordId = dict()
        edge = collections.defaultdict(list)
        nodeNum = 0

        for word in wordList:
            addEdge(word)
        
        addEdge(beginWord)
        if endWord not in wordId:
            return 0
        
        dis = [float("inf")] * nodeNum
        beginId, endId = wordId[beginWord], wordId[endWord]
        dis[beginId] = 0

        que = collections.deque([beginId])
        while que:
            x = que.popleft()
            if x == endId:
                return dis[endId] // 2 + 1
            for it in edge[x]:
                if dis[it] == float("inf"):
                    dis[it] = dis[x] + 1
                    que.append(it)
        
        return 0
```
### 128.最长连续序列
> 给定一个未排序的整数数组` nums `，找出数字连续的最长序列（不要求序列元素在原数组中连续）的长度。  
请你设计并实现时间复杂度为` O(n) `的算法解决此问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-consecutive-sequence  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        link = {}
        max_length = 0
        for num in nums:
            if num not in link:
                # 取当前数的左右两个近邻数字的区间大小
                left = link.get(num-1, 0)
                right = link.get(num+1, 0)
                # 当前数字所处区间的大小
                current = 1 + left + right
                if current > max_length:
                    max_length = current
                # 把当前区间的边界给重新赋值，确保新进来的数字一定不是已有区间内的值
                link[num] = current
                link[num - left] = current
                link[num + right] = current
        return max_length
```
### 130.被围绕的区域★
> 给你一个` m x n `的矩阵` board `，由若干字符 `'X' `和` 'O' `，找到所有被` 'X' `围绕的区域，并将这些区域里所有的` 'O' `用` 'X' `填充。

来源：力扣（LeetCode）   
链接：https://leetcode-cn.com/problems/surrounded-regions/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS
    ```python
    class Solution:
        def solve(self, board: List[List[str]]) -> None:
            """
            Do not return anything, modify board in-place instead.
            """
            # DFS解法
            if not board:
                return
            
            n, m = len(board), len(board[0])

            def dfs(x, y):
                if not 0 <= x < n or not 0 <= y < m or board[x][y] != 'O':
                    return
                # 对这个O做上标记
                board[x][y] = "A"
                dfs(x + 1, y)
                dfs(x - 1, y)
                dfs(x, y + 1)
                dfs(x, y - 1)
            
            # 以最外面一圈为起点，进行DFS
            for i in range(n):
                dfs(i, 0)
                dfs(i, m - 1)
            
            for i in range(m - 1):
                dfs(0, i)
                dfs(n - 1, i)
            
            for i in range(n):
                for j in range(m):
                    if board[i][j] == "A":
                        board[i][j] = "O"
                    elif board[i][j] == "O":
                        board[i][j] = "X"
    ```
+ BFS
    ```python
    class Solution:
        def solve(self, board: List[List[str]]) -> None:
            """
            Do not return anything, modify board in-place instead.
            """
            # BFS解法
            if not board:
                return
            
            n, m = len(board), len(board[0])
            que = collections.deque()
            for i in range(n):
                if board[i][0] == "O":
                    que.append((i, 0))
                    board[i][0] = "A"
                if board[i][m - 1] == "O":
                    que.append((i, m - 1))
                    board[i][m - 1] = "A"
            for i in range(m - 1):
                if board[0][i] == "O":
                    que.append((0, i))
                    board[0][i] = "A"
                if board[n - 1][i] == "O":
                    que.append((n - 1, i))
                    board[n - 1][i] = "A"
            
            while que:
                x, y = que.popleft()
                for mx, my in [(x - 1, y), (x + 1, y), (x, y - 1), (x, y + 1)]:
                    if 0 <= mx < n and 0 <= my < m and board[mx][my] == "O":
                        que.append((mx, my))
                        board[mx][my] = "A"
            
            for i in range(n):
                for j in range(m):
                    if board[i][j] == "A":
                        board[i][j] = "O"
                    elif board[i][j] == "O":
                        board[i][j] = "X"
    ```
### 131.分割回文串
> 给你一个字符串` s`，请你将` s `分割成一些子串，使每个子串都是 **回文串** 。返回` s `所有可能的分割方案。

**回文串** 是正着读和反着读都一样的字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/palindrome-partitioning/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def partition(self, s: str) -> List[List[str]]:
        if len(s) == 1:
            return [[s]]
        
        ans = []
        
        def is_palindrome(sequence):
            # 判断是否是回文串
            if len(sequence) == 1:
                return True
            left, right = 0, len(sequence) - 1
            while left <= right:
                if sequence[left] != sequence[right]:
                    return False
                left += 1
                right -= 1

            return True

        def backtracing(tmp, ans, start, n):
            if start == n:
                # s中的字符全部被分完了
                # 这里不用copy函数会有问题
                ans.append(tmp.copy())

            for i in range(1, n - start + 1):
                if is_palindrome(s[start: start + i]):
                    tmp.append(s[start: start + i])
                    backtracing(tmp, ans, start + i, n)
                    tmp.pop()

        backtracing([], ans, 0, len(s))
        return ans
```
### 133.克隆图★
> 给你无向 **连通** 图中一个节点的引用，请你返回该图的 **深拷贝**（克隆）。  
图中的每个节点都包含它的值` val（int）` 和其邻居的列表`（list[Node]）`。 
```java
class Node {
    public int val;
    public List<Node> neighbors;
}
```

测试用例格式：  
简单起见，每个节点的值都和它的索引相同。例如，第一个节点值为` 1（val = 1）`，第二个节点值为` 2（val = 2）`，以此类推。该图在测试用例中使用邻接列表表示。  
**邻接列表** 是用于表示有限图的无序列表的集合。每个列表都描述了图中节点的邻居集。  
给定节点将始终是图中的第一个节点（值为 1）。你必须将 **给定节点的拷贝** 作为对克隆图的引用返回。

来源：力扣（LeetCode）   
链接：https://leetcode-cn.com/problems/clone-graph  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ BFS
    ```python
    class Solution:
        def cloneGraph(self, node: 'Node') -> 'Node':
            if not node:
                return node
            # BFS 写法

            # 记录已经访问过的节点
            visited = {}
            queue = collections.deque([node])
            visited[node] = Node(node.val, [])
            while queue:
                curr = queue.popleft()
                for neighbor in curr.neighbors:
                    if neighbor not in visited:
                        visited[neighbor] = Node(neighbor.val, [])
                        queue.append(neighbor)
                    visited[curr].neighbors.append(visited[neighbor])
            return visited[node]
    ```
+ DFS
    ```python
    class Solution:
        def cloneGraph(self, node: 'Node') -> 'Node':        
            # DFS 写法
            # 记录已经访问过的节点
            visited = {}

            def dfs(node):
                if not node:
                    return node
                if node in visited:
                    return visited[node]
                clone = Node(node.val, [])
                visited[node] = clone
                for neighbor in node.neighbors:
                    clone.neighbors.append(dfs(neighbor))
                return clone

            return dfs(node)
    ```
### 138.复制带随机指针的链表
> 给你一个长度为` n `的链表，每个节点包含一个额外增加的随机指针` random `，该指针可以指向链表中的任何节点或空节点。  
构造这个链表的 **深拷贝**。 深拷贝应该正好由` n `个 **全新** 节点组成，其中每个新节点的值都设为其对应的原节点的值。新节点的` next `指针和` random `指针也都应指向复制链表中的新节点，并使原链表和复制链表中的这些指针能够表示相同的链表状态。复制链表中的指针都不应指向原链表中的节点 。  
例如，如果原链表中有` X `和` Y `两个节点，其中` X.random --> Y `。那么在复制链表中对应的两个节点` x `和` y `，同样有` x.random --> y `。  
返回复制链表的头节点。

用一个由` n `个节点组成的链表来表示输入/输出中的链表。每个节点用一个` [val, random_index] `表示：

+ `val`：一个表示 Node.val 的整数。
+ `random_index`：随机指针指向的节点索引（范围从` 0` 到` n-1`）；如果不指向任何节点，则为  `null `。
你的代码 **只** 接受原链表的头节点` head `作为传入参数。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/copy-list-with-random-pointer  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/*
// Definition for a Node.
class Node {
    int val;
    Node next;
    Node random;

    public Node(int val) {
        this.val = val;
        this.next = null;
        this.random = null;
    }
}
*/
class Solution {
    // 记录节点
    public Map<Node, Node> listCache = new HashMap<>();

    public Node copyRandomList(Node head) {
        // 当前节点为空
        if (head == null)
            return head;
        // 查看当前的节点是否已经存在
        if (!listCache.containsKey(head)) {
            Node newHead = new Node(head.val);
            listCache.put(head, newHead);
            newHead.next = copyRandomList(head.next);
            newHead.random = copyRandomList(head.random);
        }
        return listCache.get(head);
    }
}
```
### 139.单词拆分
> 给你一个字符串` s `和一个字符串列表` wordDict `作为字典。请你判断是否可以利用字典中出现的单词拼接出` s `。

注意：不要求字典中出现的单词全部都使用，并且字典中的单词可以重复使用。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/word-break  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python记忆化DFS
    ```python
    class Solution:
        def wordBreak(self, s: str, wordDict: List[str]) -> bool:
            length = len(s)
            memory = [None] * (length+1)  # default state
            memory[-1] = True

            def dfs(start):
                nonlocal length, memory
                # 记忆化DFS
                if memory[start] is not None:
                    return memory[start]
                    
                for end in range(start+1, length+1):
                    if s[start:end] in wordDict and dfs(end):
                        memory[start] = True
                        return True
                memory[start] = False
                return False
                        
            return dfs(0)
    ```
+ java动态规划
    ```java
    class Solution {
        public boolean wordBreak(String s, List<String> wordDict) {
            int length = s.length();
            //状态转移，dp[i]=true代表s的前i位可以被wordDict表示出来
            boolean[] dp = new boolean[length + 1];

            dp[0] = true;
            for (int i = 0; i < length; i++) {
                if (!dp[i])
                    continue;
                for (String word : wordDict)
                    if (word.length() + i <= s.length() && s.startsWith(word, i))
                        //这里的意思是s的前i位可以被表示了，并且i到i+word.length()这里也可以被表示，那么也就是说前i+word.length()都可以被表示了
                        dp[i + word.length()] = true;
            }
            //返回最后一位的状态，如果true就代表是整个s都可以被表示
            return dp[length];
        }
    }
    ```
### 140.单词拆分 II
> 给定一个字符串` s `和一个字符串字典` wordDict `，在字符串` s `中增加空格来构建一个句子，使得句子中所有的单词都在词典中。以任意顺序 返回所有这些可能的句子。

注意：词典中的同一个单词可能在分段中被重复使用多次。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/word-break-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python记忆化dfs
    ```python
    class Solution:
        def wordBreak(self, s: str, wordDict: List[str]) -> List[str]:
            # 记忆体，如果遇到重复子问题就可以直接取出答案
            memory = [None] * (len(s) + 1)

            # 记忆化回溯是需要定义返回值的
            def dfs(start):
                if memory[start] != None:
                    return memory[start]
                if start == len(s):
                    return [[]]
                ans = []
                for end in range(start, len(s)):
                    word = s[start: end + 1]
                    if word in wordDict:
                        rest_ans = dfs(end + 1)
                        for i in rest_ans:
                            ans.append([word] + i)
                memory[start] = ans
                return ans

            return [" ".join(i) for i in dfs(0)]
    ```
### 141.环形链表 I
> 给你一个链表的头节点` head `，判断链表中是否有环。  
如果链表中有某个节点，可以通过连续跟踪` next `指针再次到达，则链表中存在环。 为了表示给定链表中的环，评测系统内部使用整数` pos `来表示链表尾连接到链表中的位置（索引从 0 开始）。注意：`pos `不作为参数进行传递 。仅仅是为了标识链表的实际情况。  
如果链表中存在环 ，则返回` true `。 否则，返回` false `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/linked-list-cycle  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def hasCycle(self, head: Optional[ListNode]) -> bool:
        slow = fast = head
        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            if fast == slow:
                return True         
        return False
```
### 142.环形链表 II
> 给定一个链表的头节点`  head `，返回链表开始入环的第一个节点。 如果链表无环，则返回` null`。  
如果链表中有某个节点，可以通过连续跟踪` next `指针再次到达，则链表中存在环。 为了表示给定链表中的环，评测系统内部使用整数` pos `来表示链表尾连接到链表中的位置（索引从 0 开始）。如果` pos `是 -1，则在该链表中没有环。注意：`pos `不作为参数进行传递，仅仅是为了标识链表的实际情况。  
不允许修改 链表。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/linked-list-cycle-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def detectCycle(self, head: ListNode) -> ListNode:
        # 假设未循环部分长a,循环部分长b
        slow = fast = head
        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            # 第一次相遇， f = 2s = s + nb, 即s = nb
            if fast == slow:
                # 走到开头位置需要 a + nb 步，现在slow已经走了nb步了，只需要再走a步就到开头
                fast = head
                while True:
                    # 第二次相遇时，恰好走a次
                    if fast == slow:
                        return slow
                    fast = fast.next
                    slow = slow.next         
        return None
```
### 146.LRU缓存
> 请你设计并实现一个满足`  LRU (最近最少使用) 缓存` 约束的数据结构。

实现` LRUCache `类：  
+ `LRUCache(int capacity)` 以 `正整数` 作为容量 `capacity` 初始化 `LRU `缓存
+ `int get(int key) `如果关键字` key `存在于缓存中，则返回关键字的值，否则返回` -1 `。
+ `void put(int key, int value)` 如果关键字` key `已经存在，则变更其数据值` value `；如果不存在，则向缓存中插入该组` key-value `。如果插入操作导致关键字数量超过` capacity `，则应该` 逐出 `最久未使用的关键字。
+ 函数` get `和` put `必须以` O(1) `的平均时间复杂度运行。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/lru-cache  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class DLinkedNode:
    # 双向链表
    def __init__(self, key=0, value=0):
        self.key = key
        self.value = value
        self.prev = None
        self.next = None

class LRUCache:

    def __init__(self, capacity: int):
        self.cache = {}
        self.dummy_head = DLinkedNode()
        self.dummy_tail = DLinkedNode()
        # 构造头尾相连
        self.dummy_head.next = self.dummy_tail
        self.dummy_tail.prev = self.dummy_head
        self.capacity = capacity
        self.size = 0


    def get(self, key: int) -> int:
        if key not in self.cache:
            return -1
        node = self.cache[key]
        # 最近使用，放到头节点
        self.move_to_head(node)
        return node.value

    def put(self, key: int, value: int) -> None:
        if key not in self.cache:
            # 新建node
            node = DLinkedNode(key,value)
            self.cache[key] = node
            if self.size == self.capacity:
                temp = self.remove_tail()
                del self.cache[temp.key]
                self.add_to_head(node)
            else:
                self.size += 1
                self.add_to_head(node)
        else:
            node = self.cache[key]
            node.value = value
            # 最近使用，放到头节点
            self.move_to_head(node)
    
    def add_to_head(self, node):
        node.next = self.dummy_head.next
        self.dummy_head.next.prev = node
        node.prev = self.dummy_head
        self.dummy_head.next = node

    def remove_node(self, node):
        node.prev.next = node.next
        node.next.prev = node.prev

    def move_to_head(self, node):
        self.remove_node(node)
        self.add_to_head(node)

    def remove_tail(self):
        node = self.dummy_tail.prev
        self.remove_node(node)
        return node


# Your LRUCache object will be instantiated and called as such:
# obj = LRUCache(capacity)
# param_1 = obj.get(key)
# obj.put(key,value)
```
### 148.排序链表
> 给你链表的头结点`head`，请将其按**升序**排列并返回**排序后的链表**

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sort-list/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  

+ 归并排序 top down
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def sortList(self, head: Optional[ListNode]) -> Optional[ListNode]:
            if head == None or head.next == None:  # 排序列表为空 or 只有一个元素， 不需要排
                return head
            # 链表含有多个元素,使用递归的方式将链表一分为二
            slow = head
            fast = head.next
            while fast != None and fast.next != None:
                slow = slow.next
                fast = fast.next.next
            # slow已经到了链表的中间位置
            mid = slow.next
            slow.next = None
            return self.merge(self.sortList(head), self.sortList(mid))

        def merge(self, l1, l2):
            root = ListNode(0, None) # 使用root节点从小到大连接我们需要的节点
            current = root
            while l1 != None and l2 != None:
                if l1.val > l2.val: # 以l1为基础，让它的元素变成小的
                    current.next = l2
                    l2 = l2.next
                else:
                    current.next = l1
                    l1 = l1.next
                current = current.next

            # 或者while这么写
            # while l1 != None and l2 != None:
            #     if l1.val > l2.val: # 以l1为基础，让它的元素变成小的
            #         temp = l1
            #         l1 = l2
            #         l2 = temp
            #     current.next = l1
            #     l1 = l1.next
            #     current = current.next

            if l1 != None:
                current.next = l1
            elif l2 != None:
                current.next = l2
            return root.next
    ```

+ 归并排序 bottom up
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def sortList(self, head: Optional[ListNode]) -> Optional[ListNode]:
            if head == None or head.next == None:  # 排序列表为空 or 只有一个元素， 不需要排
                return head
            # 统计列表长度
            len = 1
            current = head
            while current != None:
                current = current.next
                len = len + 1

            dummy = ListNode(0)
            dummy.next = head
            n = 1
            #  for n in [1<<x for x in range(10) if 1<<x < len ]:
            while n < len:
                current = dummy.next
                tail = dummy
                while current != None:
                    left = current
                    right = self.split(left,n)
                    current = self.split(right,n)
                    tail.next, tail = self.merge(left,right)
                n = n << 1
                
            return dummy.next

        # 将列表分割为两个部分，前部分含有n个元素，返回剩余部分的第一个节点位置
        def split(self, head, n):
            # 分割前n个元素
            while n > 1 and head != None:
                head = head.next
                n = n - 1
            # 如果还剩下其余元素，就把下一个位置地址记录，即rest部分的开头
            rest = head.next if head != None else None
            # 断尾操作，前部分的最后指向空
            if head != None:
                head.next = None
            return rest


        # 合并列表，并返回合并结果的队头和队尾
        def merge(self, l1, l2):
            root = ListNode(0, None) # 使用root节点从小到大连接我们需要的节点
            tail = root
            while l1 != None and l2 != None:
                if l1.val > l2.val: # 以l1为基础，让它的元素变成小的
                    tail.next = l2
                    l2 = l2.next
                else:
                    tail.next = l1
                    l1 = l1.next
                tail = tail.next
            if l1 != None:
                tail.next = l1
            elif l2 != None:
                tail.next = l2
            # 将tail移动到队尾
            while tail.next != None:
                tail = tail.next
            return root.next, tail
    ```
### 150.逆波兰表达式求值
> 根据 逆波兰表示法，求表达式的值。

有效的算符包括` +、-、*、/ `。每个运算对象可以是整数，也可以是另一个逆波兰表达式。  
注意 两个整数之间的除法只保留整数部分。  
可以保证给定的逆波兰表达式总是有效的。换句话说，表达式总会得出有效数值且不存在除数为 0 的情况。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/evaluate-reverse-polish-notation  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

> 逆波兰表达式：  
逆波兰表达式是一种后缀表达式，所谓后缀就是指算符写在后面。 
> + 平常使用的算式则是一种中缀表达式，如` ( 1 + 2 ) * ( 3 + 4 ) `。
> + 该算式的逆波兰表达式写法为` ( ( 1 2 + ) ( 3 4 + ) * ) `。  

逆波兰表达式主要有以下两个优点：  
+ 去掉括号后表达式无歧义，上式即便写成` 1 2 + 3 4 + * `也可以依据次序计算出正确结果。  
+ 适合用栈操作运算：遇到数字则入栈；遇到算符则取出栈顶两个数字进行计算，并将结果压入栈中  

```python
class Solution:
    def evalRPN(self, tokens: List[str]) -> int:
        def add(pre, succ):
            return pre + succ

        def subtract(pre, succ):
            return pre - succ

        def multiply(pre, succ):
            return pre * succ

        def divide(pre, succ):
            result = pre / succ
            # 注意python和C语言对于负数取整的区别
            return math.floor(result) if result > 0 else math.ceil(result)

        compute_stack = []
        operator = {'+':add,'-':subtract,'*':multiply,'/':divide}
        while tokens:
            temp = tokens.pop(0)
            if len(temp) > 1 or (ord(temp) >= ord('0') and ord(temp) <= ord('9')):  # 数字
                compute_stack.append(int(temp))
            else:
                succ = compute_stack.pop()
                pre = compute_stack.pop()
                compute_stack.append(operator.get(temp)(pre, succ))
        return compute_stack[0]
```
### 155.最小栈
> 设计一个支持` push `，`pop `，`top `操作，并能在常数时间内检索到最小元素的栈。

+ `push(x)` —— 将元素 x 推入栈中。
+ `pop()` —— 删除栈顶的元素。
+ `top()` —— 获取栈顶元素。
+ `getMin()` —— 检索栈中的最小元素。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/min-stack  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class MinStack:

    def __init__(self):
        self.stack = []
        self.min_stack = []

    def push(self, val: int) -> None:
        self.stack.append(val)
        if len(self.min_stack) == 0:
            self.min_stack.append(val)
        else:
            self.min_stack.append(min(val,self.min_stack[-1]))

    def pop(self) -> None:
        self.stack.pop()
        self.min_stack.pop()

    def top(self) -> int:
        return self.stack[-1]

    def getMin(self) -> int:
        return self.min_stack[-1]


# Your MinStack object will be instantiated and called as such:
# obj = MinStack()
# obj.push(val)
# obj.pop()
# param_3 = obj.top()
# param_4 = obj.getMin()
```
### 160.相交链表
> 给你两个单链表的头节点` headA `和` headB `，请你找出并返回两个单链表相交的起始节点。如果两个链表不存在相交节点，返回` null `。  
题目数据` 保证 `整个链式结构中不存在环。  
注意，函数返回结果后，链表必须 保持其原始结构。

来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/intersection-of-two-linked-lists/    
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处  
![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/link/link_160.png)

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
        A, B = headA, headB
        while A != B :
            A = A.next if A else headB
            B = B.next if B else headA
        return A
```
### 162.寻找峰值
> 峰值元素是指其值严格大于左右相邻值的元素。  
给你一个整数数组` nums`，找到峰值元素并返回其索引。数组可能包含多个峰值，在这种情况下，返回 **任何一个峰值** 所在位置即可。  
你可以假设 `nums[-1] = nums[n] = -∞ `。  
你必须实现时间复杂度为` O(log n) `的算法来解决此问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-peak-element  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def findPeakElement(self, nums: List[int]) -> int:
        n = len(nums)

        # 辅助函数，输入下标 i，返回 nums[i] 的值
        # 方便处理 nums[-1] 以及 nums[n] 的边界情况
        def get(i: int) -> int:
            if i == -1 or i == n:
                return float('-inf')
            return nums[i]
        
        left, right, ans = 0, n - 1, -1
        while left <= right:
            mid = (left + right) // 2
            if get(mid - 1) < get(mid) > get(mid + 1):
                ans = mid
                break
            if get(mid) < get(mid + 1):
                left = mid + 1
            else:
                right = mid - 1
        
        return ans

```
### 167.两数之和 II - 输入有序数组
> 给你一个下标从` 1 `开始的整数数组` numbers `，该数组已按 **非递减顺序排列**  ，请你从数组中找出满足相加之和等于目标数` target`的两个数。如果设这两个数分别是` numbers[index1] `和` numbers[index2]` ，则` 1 <= index1 < index2 <= numbers.length `。  
以长度为` 2 `的整数数组` [index1, index2] `的形式返回这两个整数的下标` index1 `和` index2`。  
你可以假设每个输入 **只对应唯一的答案** ，而且你 **不可以** 重复使用相同的元素。  
你所设计的解决方案必须只使用常量级的额外空间。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/two-sum-ii-input-array-is-sorted  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        ans = []
        for idx, num in enumerate(numbers):
            key = target-num
            find_key = bisect_left(numbers[idx+1:], key)
            if idx+find_key+1 < len(numbers) and key == numbers[idx+find_key+1]:
                ans = [idx+1, idx+find_key+2]
                break
        return ans
```
### 179.最大数

> 给定一组非负整数 nums，重新排列每个数的顺序（每个数不可拆分）使之组成一个最大的整数。  
注意：输出结果可能非常大，所以你需要返回一个字符串而不是整数。

来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/largest-number/    
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处

```python
class Solution:
    def largestNumber(self, nums: List[int]) -> str:
        import functools
        nums_str=list(map(str,nums))
        compare=lambda x,y: 1 if x+y<y+x else -1
        nums_str.sort(key=functools.cmp_to_key(compare))
        res=''.join(nums_str)
        if res[0]=='0':
            res='0'
        return res
```
### 200.岛屿数量
> 给你一个由` '1'`（陆地）和` '0'`（水）组成的的二维网格，请你计算网格中岛屿的数量。  
岛屿总是被水包围，并且每座岛屿只能由水平方向和/或竖直方向上相邻的陆地连接形成。  
此外，你可以假设该网格的四条边均被水包围。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/number-of-islands  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ BFS
    ```python
    class Solution:
        def numIslands(self, grid: List[List[str]]) -> int:
            # BFS解法
            def bfs(i, j):
                queue = collections.deque()
                queue.append((i, j))
                # 当前节点已经走过了
                visited.add((i, j))
                while queue:
                    i, j = queue.popleft()
                    for x, y in [[-1, 0], [1, 0], [0, -1], [0, 1]]:
                        temp_x = i + x
                        temp_y = j + y
                        # 没出界，是陆地，且没有走过
                        if 0 <= temp_x < row and 0 <= temp_y < col and grid[temp_x][temp_y] == '1' and (temp_x, temp_y) not in visited:
                            visited.add((temp_x, temp_y))
                            queue.append((temp_x, temp_y))

            # 记录行、列数
            row, col = len(grid), len(grid[0])
            visited = set()
            ans = 0

            for i in range(row):
                for j in range(col):
                    if grid[i][j] == '1' and (i, j) not in visited:
                        bfs(i, j)
                        ans += 1
            
            return ans
    ```
+ DFS
    ```python
    class Solution:
        def numIslands(self, grid: List[List[str]]) -> int:
            # DFS解法
            def dfs(i, j):
                # 判断不在格子里、不是岛屿、之前已经走过了
                if not inArea(i, j) or grid[i][j] != '1' or (i, j) in visited:
                    return
                visited.add((i, j))  # 将格子标记为「已遍历过」
                # 访问上、下、左、右四个相邻结点
                for x, y in [[-1, 0], [1, 0], [0, -1], [0, 1]]:
                    temp_x = i + x
                    temp_y = j + y
                    dfs(temp_x, temp_y)

            # 判断坐标 (i, j) 是否在网格中
            def inArea(i, j):
                return 0 <= i < len(grid) and 0 <= j < len(grid[0])

            ans = 0    
            visited = set()
            for i in range(len(grid)):
                for j in range(len(grid[0])):
                    if grid[i][j] == '1' and (i, j) not in visited:
                        dfs(i, j)
                        ans += 1
            return ans
    ```
### 206.反转链表
> 给你单链表的头节点` head `，请你反转链表，并返回反转后的链表。
 
来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/reverse-linked-list/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处

+ 迭代法
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def reverseList(self, head: ListNode) -> ListNode:
            pre, tail = None, head
            while tail != None:
                temp = tail.next
                tail.next = pre
                pre = tail
                tail = temp
            return pre
    ```
+ 递归法
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def reverseList(self, head: ListNode) -> ListNode:
            return self.reverse(None, head)
        
        def reverse(self, first, second):
            if not second:
                return first
            temp = second.next
            second.next = first
            return self.reverse(second, temp)
    ```
### 207.课程表
> 你这个学期必须选修` numCourses `门课程，记为` 0 `到` numCourses - 1 `。  
在选修某些课程之前需要一些先修课程。 先修课程按数组` prerequisites `给出，其中` prerequisites[i] = [ai, bi] `，表示如果要学习课程` ai` 则 **必须** 先学习课程 ` bi `。

+ 例如，先修课程对 [0, 1] 表示：想要学习课程 0 ，你需要先完成课程 1 。

请你判断是否可能完成所有课程的学习？如果可以，返回` true `；否则，返回` false `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/course-schedule  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def canFinish(self, numCourses: int, prerequisites: List[List[int]]) -> bool:
        # 按照先修课程数组构造有向图
        edges = defaultdict(list)
        # 记录每个课程节点的入度数量
        in_degree = [0] * numCourses

        for prerequisite in prerequisites:
            # 构造边
            edges[prerequisite[1]].append(prerequisite[0])
            # 记录入度
            in_degree[prerequisite[0]] += 1

        # 首先入度为0 的节点先进队列
        queue = deque([i for i in range(numCourses) if in_degree[i] == 0])
        # 统计当前按照先修要求可以学习的课程门数
        visited = 0

        while queue:
            course = queue.popleft()
            visited += 1
            # 当前course可以修，此时从有向图中删去该课程以及边
            for node in edges[course]:
                # 对于该课程所对应的下一门课程，入度减一
                in_degree[node] -= 1
                if in_degree[node] == 0:
                    queue.append(node)

        return True if visited == numCourses else False
```
### 208.实现Trie(前缀树)
> `Trie`（发音类似 `"try"`）或者说 **前缀树** 是一种树形数据结构，用于高效地存储和检索字符串数据集中的键。这一数据结构有相当多的应用情景，例如自动补完和拼写检查。

请你实现` Trie `类：

+ `Trie()` 初始化前缀树对象。
+ `void insert(String word)` 向前缀树中插入字符串 `word` 。
+ `boolean search(String word)` 如果字符串 `word `在前缀树中，返回` true`（即，在检索之前已经插入）；否则，返回 `false` 。
+ `boolean startsWith(String prefix)` 如果之前已经插入的字符串` word `的前缀之一为` prefix `，返回` true `；否则，返回 `false` 。
 

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/implement-trie-prefix-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java
```java
class Trie {

    class TrieNode {
        boolean isEnd;  // 当前节点是否是一个单词的最终节点
        TrieNode[] next;  // 当前节点的下一个后续节点

        public TrieNode(){
            this.isEnd = false;
            this.next = new TrieNode[26];
        }
    }

    public TrieNode root;  // 根节点

    public Trie() {
        this.root = new TrieNode();
    }
    
    public void insert(String word) {
        TrieNode node = root;
        for (char c: word.toCharArray()){
            if (node.next[c - 'a'] == null)
                node.next[c - 'a'] = new TrieNode();
            node = node.next[c - 'a'];
        }
        // 插入的是一个单词，所以这个设置节点是true
        node.isEnd = true;
    }
    
    public boolean search(String word) {
        TrieNode node = root;
        for (char c: word.toCharArray()){
            if (node.next[c - 'a'] == null)
                return false;
            node = node.next[c - 'a'];
        }
        return node.isEnd;
    }
    
    public boolean startsWith(String prefix) {
        TrieNode node = root;
        for (char c: prefix.toCharArray()){
            if (node.next[c - 'a'] == null)
                return false;
            node = node.next[c - 'a'];
        }
        return true;
    }
}

/**
 * Your Trie object will be instantiated and called as such:
 * Trie obj = new Trie();
 * obj.insert(word);
 * boolean param_2 = obj.search(word);
 * boolean param_3 = obj.startsWith(prefix);
 */
```

+ python
```python
class Trie(object):
    def __init__(self):
        """
        Initialize your data structure here.
        """
        self.root = TrieNode()

    def insert(self, word):
        """
        Inserts a word into the trie.
        :type word: str
        :rtype: None
        """
        node = self.root
        for i in range(len(word)):
            if not node.containsKey(word[i]):
                node.put(word[i], TrieNode())
            node = node.get(word[i])
        node.isEnd = True

    def searchPrefix(self, word):
        node = self.root
        for i in range(len(word)):
            if node.containsKey(word[i]):
                node = node.get(word[i])
            else:
                return None
        return node

    def search(self, word):
        """
        Returns if the word is in the trie.
        :type word: str
        :rtype: bool
        """
        node = self.searchPrefix(word)
        return node is not None and node.isEnd

    def startsWith(self, prefix):
        """
        Returns if there is any word in the trie that starts with the given prefix.
        :type prefix: str
        :rtype: bool
        """
        node = self.searchPrefix(prefix)
        return node is not None


class TrieNode:
    def __init__(self):
        self.__R = 26
        self.isEnd = False
        self.links = [None] * self.__R

    def containsKey(self, ch):
        return self.links[ord(ch) - ord('a')] is not None

    def get(self, ch):
        return self.links[ord(ch) - ord('a')]

    def put(self, ch, node):
        self.links[ord(ch) - ord('a')] = node
```
### 210.课程表 II
> 你这个学期必须选修` numCourses `门课程，记为` 0 `到` numCourses - 1 `。  
在选修某些课程之前需要一些先修课程。 先修课程按数组` prerequisites `给出，其中` prerequisites[i] = [ai, bi] `，表示如果要学习课程` ai` 则 **必须** 先学习课程 ` bi `。

+ 例如，先修课程对 [0, 1] 表示：想要学习课程 0 ，你需要先完成课程 1 。

返回你为了学完所有课程所安排的学习顺序。可能会有多个正确的顺序，你只要返回 **任意一种** 就可以了。如果不可能完成所有课程，返回 **一个空数组** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/course-schedule-ii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```python
class Solution:
    def findOrder(self, numCourses: int, prerequisites: List[List[int]]) -> List[int]:
        # 按照先修课程数组构造有向图
        edges = defaultdict(list)
        # 记录每个课程节点的入度数量
        in_degree = [0] * numCourses

        for prerequisite in prerequisites:
            # 构造边
            edges[prerequisite[1]].append(prerequisite[0])
            # 记录入度
            in_degree[prerequisite[0]] += 1

        # 首先入度为0 的节点先进队列
        queue = deque([i for i in range(numCourses) if in_degree[i] == 0])
        # 统计当前按照先修要求可以学习的课程
        visited = []

        while queue:
            course = queue.popleft()
            visited.append(course)
            # 当前course可以修，此时从有向图中删去该课程以及边
            for node in edges[course]:
                # 对于该课程所对应的下一门课程，入度减一
                in_degree[node] -= 1
                if in_degree[node] == 0:
                    queue.append(node)

        return visited if len(visited) == numCourses else []
```
### 212.单词搜索II★
> 给定一个` m x n` 二维字符网格 `board` 和一个单词（字符串）列表 `words`， 返回所有二维网格上的单词 。

单词必须按照字母顺序，通过 **相邻的单元格** 内的字母构成，其中“相邻”单元格是那些水平相邻或垂直相邻的单元格。同一个单元格内的字母在一个单词中不允许被重复使用。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/word-search-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ 字典树(官方题解)
    ```python
    class Trie:
        def __init__(self):
            self.children = defaultdict(Trie)
            self.word = ""

        def insert(self, word):
            cur = self
            for c in word:
                cur = cur.children[c]
            cur.is_word = True
            cur.word = word


    class Solution:
        def findWords(self, board: List[List[str]], words: List[str]) -> List[str]:

            # 构造字典树
            trie = Trie()
            for word in words:
                trie.insert(word)

            def dfs(now, i1, j1):
                if board[i1][j1] not in now.children:
                    return

                ch = board[i1][j1]

                now = now.children[ch]
                if now.word != "":
                    ans.add(now.word)

                board[i1][j1] = "#"
                for i2, j2 in [(i1 + 1, j1), (i1 - 1, j1), (i1, j1 + 1), (i1, j1 - 1)]:
                    if 0 <= i2 < m and 0 <= j2 < n:
                        dfs(now, i2, j2)
                board[i1][j1] = ch

            ans = set()
            m, n = len(board), len(board[0])

            for i in range(m):
                for j in range(n):
                    dfs(trie, i, j)

            return list(ans)
    ```
+ DFS+回溯(~~虽然剪枝了一部分，但是python超时，过不了，垃圾python~~)
    ```python
    class Solution:
        def findWords(self, board: List[List[str]], words: List[str]) -> List[str]:

            def backtracking(word, start, position, visited):
                if start == len(word):
                    # word中所有字符都搜索到了
                    return True
                x, y = position
                if x < 0 or y < 0 or x >= m or y >= n or position in visited:
                    # 越界了，或者当前位置已经被搜索了
                    return False
                
                if board[x][y] == word[start]:
                    visited.add(position)
                    for new_x, new_y in [(x-1, y), (x+1, y), (x, y-1), (x, y+1)]:
                        if backtracking(word, start + 1, (new_x, new_y), visited):
                            return True
                    # 回溯
                    visited.remove(position)
                return False

            m, n = len(board), len(board[0])
            board_count = collections.defaultdict(int)
            # 统计board中的字符出现次数
            for i in range(m):
                for j in range(n):
                    board_count[board[i][j]] += 1
            
            ans = []
            # 从给定词表开始查找
            for word in words:
                # 统计当前词的单词频数
                word_count = collections.Counter(word)
                exist = True  # 当前word是否有几率存在于board中
                for ch in word:
                    # 当前word的某个字符比board中总的这个字符都多，肯定搜索不到，word不存在
                    if word_count[ch] > board_count[ch]:
                        exist = False
                        break
                # 当前word不存在就跳过这个单词
                if not exist:
                    continue
                
                find = False  # 当前词是否可以搜索到
                for i in range(m):
                    for j in range(n):
                        if backtracking(word, 0, (i, j), set()):
                            ans.append(word)
                            find = True
                            break
                    # 找到了，直接结束这个词的搜索
                    if find:
                        break
            return ans       
    ``
### 215.数组中的第k个最大元素
> 给定整数数组 nums 和整数 k，请返回数组中第 k 个最大的元素。  
请注意，你需要找的是数组排序后的第 k 个最大的元素，而不是第 k 个不同的元素。

来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/kth-largest-element-in-an-array/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处

+ 调库(~~毫无意义~~)
    ```python
    class Solution:
        def findKthLargest(self, nums: List[int], k: int) -> int:
            nums.sort(reverse = True)
            return nums[k-1]
    ```

+ 大顶堆
    ```python
    class Solution:
        def findKthLargest(self, nums: List[int], k: int) -> int:
            # python的heapq库只实现了小顶堆，这里使用大顶堆合适一些
            # heapq.heappush(maxHeap, -i)当然非要用的话，可以通过加‘-’号构建大顶堆
            # 所以自己造轮子，自己写堆排序
            n = len(nums)
            if n == 1:
                return nums[0]
            # 第一个非叶子节点
            node = int(n / 2) - 1
            # 创建大顶堆
            for i in range(node,-1,-1):
                self.adjustHeap(nums, i, n)
            count = 0
            if count == k-1:
                return nums[0] 
            else:
                # 交换队头、队尾，并调整大顶堆
                for i in range(n-1,0,-1):
                    # 不能写在这里，因为在判断之前可能for循环都进不来了
                    # if count == k-1:
                    #     return nums[0]
                    self.swap(nums, 0, i)
                    self.adjustHeap(nums, 0, i)
                    count += 1
                    # 如果换在这里，需要提前考虑题目判断点是不是第一大
                    # 如果是问的是第一大，在这里的时候就已经swap了，那么结果肯定不对了
                    if count == k-1:
                        return nums[0]

        def adjustHeap(self, nums, node, length):
            """
            调整大顶堆
            """
            temp = nums[node]
            # 从当前节点的第一个(左)孩子节点开始
            i = 2 * node + 1
            while i < length:
                if i+1 < length and nums[i] < nums[i+1]: # 右孩子存在且比左孩子更大
                    i += 1 # 指向右孩子
                if nums[i] > temp:
                    nums[node] = nums[i]
                    node = i
                else:
                    break
                i = 2 * i + 1
            nums[node] = temp


        def swap(self, nums, a, b):
            nums[a], nums[b] = nums[b], nums[a]
    ```
### 216.组合总和III
> 找出所有相加之和为` n `的` k `个数的组合，且满足下列条件：

+ 只使用数字`1`到`9`
+ 每个数字 **最多使用一次** 

返回 **所有可能的有效组合的列表** 。该列表不能包含相同的组合两次，组合可以以任何顺序返回。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/combination-sum-iii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
    ```python
    class Solution:
        def combinationSum3(self, k: int, n: int) -> List[List[int]]:
            # 数字列表1-9
            nums = range(1, 10)
            # 最小结果都大于目标，或者最大结果都小于目标
            if sum(nums[:k]) > n or sum(nums[-k:]) < n:
                return []

            def backtracing(tmp, start, k, n, ans):
                if len(tmp) == k and sum(tmp) == n:
                    # 和为n，满足题意
                    ans.append(tmp.copy())
                    return None 
                for i in range(start, 10):
                    if sum(tmp) + i > n:
                        break
                    tmp.append(i)
                    backtracing(tmp, i + 1, k, n, ans)    
                    tmp.pop()

            ans = []
            backtracing([], 1, k, n, ans)
            return ans
    ```
### 224.基本计算器
> 给你一个字符串表达式` s `，请你实现一个基本计算器来计算并返回它的值。  
注意:不允许使用任何将字符串作为数学表达式计算的内置函数，比如` eval() `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/basic-calculator/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```python
class Solution:
    def calculate(self, s: str) -> int:
        # 可以转成后缀表达式，再参考150求解
        num_stack = []
        operator_stack = []
        s = s.replace(" ", "")
        num = ''
        # TMD题目的意思说明并不一定是一位数
        for idx in range(0,len(s)):
            char = s[idx]
            if char.isdigit():
                num += char
                if idx == len(s)-1 or not s[idx+1].isdigit():
                    num_stack.append(int(num))
                    num = ''
                else:
                    continue
            elif char in ['+','-','(']:
                # 考虑比较特殊的-号，即用作负数的这种情况
                if char == '-'and (idx == 0 or s[idx-1] == '('):
                    num_stack.append(0)
                operator_stack.append(char)
            else: # 右括号
                temp_op = []
                temp_num = []
                # 取符号
                while operator_stack:
                    curr_op = operator_stack.pop()
                    if curr_op == '(':
                        break
                    else:
                        temp_op.append(curr_op)
                # 取数字
                for _ in range(0,len(temp_op)+1):
                    temp_num.append(num_stack.pop())
                # 计算结果
                while temp_op:
                    if temp_op.pop() == '+':
                        temp_num.append(temp_num.pop()+temp_num.pop())
                    else:
                        temp_num.append(temp_num.pop()-temp_num.pop())
                num_stack.append(temp_num[0])
            if '(' not in operator_stack and len(num_stack)>1:# 该计算了
                    succ = num_stack.pop()
                    pre = num_stack.pop()
                    if operator_stack.pop() == '+':
                        num_stack.append(pre + succ)
                    else:
                        num_stack.append(pre - succ)
        return num_stack[0]

```
### 225.用队列实现栈
> 请你仅使用两个队列实现一个后入先出（LIFO）的栈，并支持普通栈的全部四种操作（push、top、pop 和 empty）。

实现 MyStack 类：

+ `void push(int x)` 将元素` x `压入栈顶。
+ `int pop()` 移除并返回栈顶元素。
+ `int top()` 返回栈顶元素。
+ `boolean empty()` 如果栈是空的，返回` true `；否则，返回` false `。

注意：

你只能使用队列的基本操作 —— 也就是` push to back、peek/pop from front、size `和` is empty `这些操作。  
你所使用的语言也许不支持队列。 你可以使用 ` list `（列表）或者 `deque`（双端队列）来模拟一个队列 , 只要是标准的队列操作即可。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/implement-stack-using-queues  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 一个队列实现
    ```python
    class MyStack:

        def __init__(self):
            self.my_stack = []
            self.size = 0

        def push(self, x: int) -> None:
            self.my_stack.append(x)
            self.size += 1
            n = self.size
            # 确保栈的后进先出，即把刚刚append进来的元素保存在第一个位置，这样pop就没问题了
            while n > 1:
                self.my_stack.append(self.my_stack.pop(0))
                n -= 1

        def pop(self) -> int:
            self.size -= 1
            return self.my_stack.pop(0)

        def top(self) -> int:
            return self.my_stack[0]

        def empty(self) -> bool:
            return True if self.size == 0 else False
    ```
+ 两个队列实现
    ```python
    class MyStack:

        def __init__(self):
            self.my_stack = []
            self.help = []

        def push(self, x: int) -> None:
            self.help.append(x)
            while self.my_stack:
                self.help.append(self.my_stack.pop(0))
            self.my_stack, self.help = self.help, self.my_stack

        def pop(self) -> int:
            return self.my_stack.pop(0)

        def top(self) -> int:
            return self.my_stack[0]

        def empty(self) -> bool:
            return True if len(self.my_stack) == 0 else False



    # Your MyStack object will be instantiated and called as such:
    # obj = MyStack()
    # obj.push(x)
    # param_2 = obj.pop()
    # param_3 = obj.top()
    # param_4 = obj.empty()
    ```
### 226.翻转二叉树
> 给你一棵二叉树的根节点` root `，翻转这棵二叉树，并返回其根节点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/invert-binary-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 自身函数递归
```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def invertTree(self, root: TreeNode) -> TreeNode:
        # 该树为空
        if not root:
            return root
        left = self.invertTree(root.left)
        right = self.invertTree(root.right)
        # 左右交换
        root.left, root.right = right, left
        return root
```
+ 新建dfs函数递归
```python
class Solution:
    def invertTree(self, root: TreeNode) -> TreeNode:

        def dfs(node):
            # 该树为空
            if not node:
                return node
            left = dfs(node.left)
            right = dfs(node.right)
            # 左右交换
            node.left, node.right = right, left
            return node

        root = dfs(root)
        return root
```
### 230.二叉搜索树中第K小的元素
> 给定一个二叉搜索树的根节点` root `，和一个整数` k `，请你设计一个算法查找其中第` k `个最小元素（从` 1 `开始计数）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 中序遍历
    ```python
    # Definition for a binary tree node.
    # class TreeNode:
    #     def __init__(self, val=0, left=None, right=None):
    #         self.val = val
    #         self.left = left
    #         self.right = right
    class Solution:
        def kthSmallest(self, root: Optional[TreeNode], k: int) -> int:
            # 中序遍历二叉搜索树的结果就是从小到大递增的
            stack = []
            while root or stack:
                # 左子树走到底，记录这一路上遇到的节点
                # 说白了就是pop的时候可以拿到父节点，然后去右子树罢了
                while root:
                    stack.append(root)
                    root = root.left
                root = stack.pop()
                k -= 1
                if k == 0:
                    return root.val
                root = root.right
    ```

+ 记录子树的结点数(官方题解)
    ```python
    class MyBst:
        def __init__(self, root: TreeNode):
            self.root = root

            # 统计以每个结点为根结点的子树的结点数，并存储在哈希表中
            self._node_num = {}
            self._count_node_num(root)

        def kth_smallest(self, k: int):
            """返回二叉搜索树中第k小的元素"""
            node = self.root
            while node:
                left = self._get_node_num(node.left)
                if left < k - 1:
                    node = node.right
                    k -= left + 1
                elif left == k - 1:
                    return node.val
                else:
                    node = node.left

        def _count_node_num(self, node) -> int:
            """统计以node为根结点的子树的结点数"""
            if not node:
                return 0
            self._node_num[node] = 1 + self._count_node_num(node.left) + self._count_node_num(node.right)
            return self._node_num[node]

        def _get_node_num(self, node) -> int:
            """获取以node为根结点的子树的结点数"""
            return self._node_num[node] if node is not None else 0


    class Solution:
        def kthSmallest(self, root: TreeNode, k: int) -> int:
            bst = MyBst(root)
            return bst.kth_smallest(k)

    ```
### 232.用栈实现队列
> 请你仅使用两个栈实现先入先出队列。队列应当支持一般队列支持的所有操作（push、pop、peek、empty）：

实现 MyQueue 类：

+ `void push(int x)` 将元素 x 推到队列的末尾
+ `int pop()` 从队列的开头移除并返回元素
+ `int peek()` 返回队列开头的元素
+ `boolean empty()` 如果队列为空，返回 true ；否则，返回 false
说明：

你**只能**使用标准的栈操作 —— 也就是只有` push to top`,` peek/pop from top`,` size`, 和 `is empty `操作是合法的。
你所使用的语言也许不支持栈。你可以使用` list` 或者` deque`（双端队列）来模拟一个栈，只要是标准的栈操作即可。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/implement-queue-using-stacks  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class MyQueue:

    def __init__(self):
        self.input_stack = []
        self.output_stack = []

    def push(self, x: int) -> None:
        self.input_stack.append(x)

    def pop(self) -> int:
        if not self.output_stack:
            while self.input_stack:
                self.output_stack.append(self.input_stack.pop())
        return self.output_stack.pop()

    def peek(self) -> int:
        if not self.output_stack:
            while self.input_stack:
                self.output_stack.append(self.input_stack.pop())
        return self.output_stack[-1]

    def empty(self) -> bool:
        if not self.input_stack and not self.output_stack:
            return True
        return False


# Your MyQueue object will be instantiated and called as such:
# obj = MyQueue()
# obj.push(x)
# param_2 = obj.pop()
# param_3 = obj.peek()
# param_4 = obj.empty()
```
### 235.二叉搜索树的最近公共祖先
> 给定一个二叉搜索树, 找到该树中两个指定节点的最近公共祖先。

百度百科中最近公共祖先的定义为：“对于有根树 T 的两个结点 p、q，最近公共祖先表示为一个结点 x，满足 x 是 p、q 的祖先且 x 的深度尽可能大（一个节点也可以是它自己的祖先）。”

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        # pq在左子树
        if p.val < root.val and q.val < root.val:
            return self.lowestCommonAncestor(root.left, p, q)
        # pq在右子树
        elif p.val > root.val and q.val > root.val:
            return self.lowestCommonAncestor(root.right, p, q)
        else:
            return root
```
### 236.二叉树的最近公共祖先
> 给定一个二叉树, 找到该树中两个指定节点的最近公共祖先。

**百度百科**中最近公共祖先的定义为：“对于有根树 T 的两个节点 p、q，最近公共祖先表示为一个节点 x，满足 x 是 p、q 的祖先且 x 的深度尽可能大（一个节点也可以是它自己的祖先）。”

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        # 如果p、q在同一棵子树，谁在前面谁就是答案，如果不在一棵树，就是两者所在子树的根节点
        if not root or root == p or root == q:
            return root

        # 在左子树里面找pq
        left = self.lowestCommonAncestor(root.left, p, q)
        # 在右子树里面找pq
        right = self.lowestCommonAncestor(root.right, p, q)

        # 左右子树都能找到，说明一边一个，显然当前根节点就是最近的祖先
        if left and right:
            return root

        # pq都在左子树
        if left:
            return left

        # pq都在右子树
        if right:
            return right
            
        return None
```
### 240.搜索二维矩阵II
> 编写一个高效的算法来搜索` m x n `矩阵` matrix `中的一个目标值` target `。该矩阵具有以下特性：  
每行的元素从左到右升序排列。
每列的元素从上到下升序排列。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/search-a-2d-matrix-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def searchMatrix(self, matrix: List[List[int]], target: int) -> bool:
        def binary_search(nums, left, right, target):
            while left <= right:
                mid = left + (right - left) // 2
                if nums[mid] == target:
                    return True
                if nums[mid] < target:
                    left = mid + 1
                else:
                    right = mid - 1
            return False

        m, n = len(matrix), len(matrix[0])
        for i in range(m):
            if matrix[i][0] > target or matrix[i][-1] < target:
                continue
            ans = binary_search(matrix[i], 0, n-1, target)
            if ans:
                return ans
        return False
```
### 264.丑数II
> 给你一个整数` n `，请你找出并返回第` n `个 **丑数** 。  
**丑数** 就是只包含质因数` 2、3 和/或 5 `的正整数

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/ugly-number-ii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def nthUglyNumber(self, n: int) -> int:
        min_heap = []
        heapq.heappush(min_heap, 1)
        count = 0
        while count < n:
            temp = heapq.heappop(min_heap)
            if 2*temp not in min_heap:
                heapq.heappush(min_heap, 2*temp)
            if 3*temp not in min_heap:
                heapq.heappush(min_heap, 3*temp)
            if 5*temp not in min_heap:
                heapq.heappush(min_heap, 5*temp) 
            count += 1
            if count == n:
                return temp
        return 0
```
### 278.第一个错误版本
> 你是产品经理，目前正在带领一个团队开发新的产品。不幸的是，你的产品的最新版本没有通过质量检测。由于每个版本都是基于之前的版本开发的，所以错误的版本之后的所有版本都是错的。  
假设你有` n `个版本` [1, 2, ..., n]`，你想找出导致之后所有版本出错的第一个错误的版本。

你可以通过调用` bool isBadVersion(version) `接口来判断版本号` version `是否在单元测试中出错。实现一个函数来查找第一个错误的版本。你应该尽量减少对调用` API `的次数。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/first-bad-version  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# The isBadVersion API is already defined for you.
# @param version, an integer
# @return an integer
# def isBadVersion(version):

class Solution:
    def firstBadVersion(self, n):
        """
        :type n: int
        :rtype: int
        """
        l = 0
        r = n
        while l < r:
            mid = l + (r - l) // 2
            if not isBadVersion(mid):
                l = mid + 1
            else:
                r = mid
        return r
```
### 283.移动零
> 给定一个数组` nums`，编写一个函数将所有` 0 `移动到数组的末尾，同时保持非零元素的相对顺序。  
请注意 ，必须在不复制数组的情况下原地对数组进行操作。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/move-zeroes/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        # 同向快慢指针
        n = len(nums)
        if n > 1:
            slow, fast = 0, 1
            while fast < n:
                while slow < n-1 and nums[slow] != 0:
                    # 找到slow第一个为0的位置
                    slow += 1
                # fast则为slow的下一个位置
                fast = slow + 1 
                # 找到fast第一个不为0的位置   
                while fast < n and nums[fast] == 0:
                    fast += 1
                if slow < fast and fast < n:
                    nums[slow], nums[fast] = nums[fast], nums[slow] 
```
### 285.二叉搜索树中的中序后继(剑指Offer II 053)
> 给定一棵二叉搜索树和其中的一个节点` p `，找到该节点在树中的中序后继。如果节点没有中序后继，请返回` null `。

节点` p `的后继是值比` p.val `大的节点中键值最小的节点，即按中序遍历的顺序节点` p `的下一个节点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/P5rCT8  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def inorderSuccessor(self, root: 'TreeNode', p: 'TreeNode') -> 'TreeNode':
        # 中序遍历
        stack = []
        pre = None
        while root or stack:
            while root:
                stack.append(root)
                root = root.left
            root = stack.pop()
            if pre == p:
                return root
            else:
                pre = root
            root = root.right
        return None
```
### 290.单词规律
> 给定一种规律` pattern `和一个字符串` s `，判断` s `是否遵循相同的规律。

这里的 **遵循** 指完全匹配，例如，` pattern `里的每个字母和字符串` str `中的每个非空单词之间存在着双向连接的对应规律。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/word-pattern  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def wordPattern(self, pattern: str, s: str) -> bool:
        word2ch = dict()
        ch2word = dict()
        words = s.split()
        if len(pattern) != len(words):
            return False
        
        for ch, word in zip(pattern, words):
            if (word in word2ch and word2ch[word] != ch) or (ch in ch2word and ch2word[ch] != word):
                return False
            word2ch[word] = ch
            ch2word[ch] = word
    
        return True
```
### 295.数据流的中位数
> 中位数是有序列表中间的数。如果列表长度是偶数，中位数则是中间两个数的平均值。  
例如，  
[2,3,4] 的中位数是 3  
[2,3] 的中位数是 (2 + 3) / 2 = 2.5

设计一个支持以下两种操作的数据结构：  
+ `void addNum(int num)` - 从数据流中添加一个整数到数据结构中。
+ `double findMedian()` - 返回目前所有元素的中位数。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-median-from-data-stream  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class MedianFinder:

    def __init__(self):
        self.min_heap = [] # 存放后半部分的值
        self.max_heap = [] # 存放前半部分的值

    def addNum(self, num: int) -> None:
        # 当插入值为奇数时，我们需要前半部分比后半部分多1
        if len(self.min_heap) == len(self.max_heap): # 当前值插入前，已经插入0个或偶数个值了
            if len(self.min_heap) == 0: # 还没插入值
                heapq.heappush(self.max_heap, -num)
            elif num < -self.max_heap[0]: # 当前值比前半部分的最大值小，说明这个值应该放在前面，满足奇数
                heapq.heappush(self.max_heap, -num)
            elif num >= -self.max_heap[0]: # 当前值比前半部分的最大值大，说明这个值应该放在后面，为满足奇数需要把后面的最小值放到前面去
                heapq.heappush(self.max_heap, -heapq.heappushpop(self.min_heap, num))
        else: # 当前值插入前，已经插入奇数个值了
            if len(self.min_heap) == 0: # 还没插入值
                heapq.heappush(self.min_heap, -heapq.heappushpop(self.max_heap, -num))
            elif num < -self.max_heap[0]: # 当前值比前半部分的最大值小，说明这个值应该放在前面，为满足偶数需要把前面的最大值放到后面去
                heapq.heappush(self.min_heap, -heapq.heappushpop(self.max_heap, -num))
            elif num >= -self.max_heap[0]: # 当前值比前半部分的最大值大，说明这个值应该放在后面
                heapq.heappush(self.min_heap, num)

    def findMedian(self) -> float:
        if len(self.min_heap) == len(self.max_heap):
            # 偶数
            return (self.min_heap[0] - self.max_heap[0]) / 2
        return -self.max_heap[0]


# Your MedianFinder object will be instantiated and called as such:
# obj = MedianFinder()
# obj.addNum(num)
# param_2 = obj.findMedian()
```
### 297.二叉树的序列化与反序列化
> 序列化是将一个数据结构或者对象转换为连续的比特位的操作，进而可以将转换后的数据存储在一个文件或者内存中，同时也可以通过网络传输到另一个计算机环境，采取相反方式重构得到原数据。  
请设计一个算法来实现二叉树的序列化与反序列化。这里不限定你的序列 / 反序列化算法执行逻辑，你只需要保证一个二叉树可以被序列化为一个字符串并且将这个字符串反序列化为原始的树结构。

提示: 输入输出格式与` LeetCode `目前使用的方式一致，详情请参阅` LeetCode `序列化二叉树的格式。你并非必须采取这种方式，你也可以采用其他的方法解决这个问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/serialize-and-deserialize-binary-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ BFS
```python
# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Codec:

    def serialize(self, root):
        """Encodes a tree to a single string.
        
        :type root: TreeNode
        :rtype: str
        """

        # BFS解法
        if not root:
            return ''
        queue = collections.deque([root])
        ans = []
        while queue:
            node = queue.popleft()
            if node:
                ans.append(str(node.val))
                queue.append(node.left)
                queue.append(node.right)
            else:
                ans.append('None')
        return '[' + ','.join(ans) + ']'
        

    def deserialize(self, data):
        """Decodes your encoded data to tree.
        
        :type data: str
        :rtype: TreeNode
        """
        if not data:
            return []
        # 去掉中括号
        node_list = data[1:-1].split(',')
        root = TreeNode(int(node_list[0]))
        queue = collections.deque([root])
        idx = 1
        while queue and idx < len(node_list):
            node = queue.popleft()
            # 有左节点        
            if node_list[idx] != 'None':
                node.left = TreeNode(int(node_list[idx]))
                queue.append(node.left)
            idx += 1
            # 有右节点
            if node_list[idx] != 'None':
                node.right = TreeNode(int(node_list[idx]))
                queue.append(node.right)
            idx += 1
        return root
# Your Codec object will be instantiated and called as such:
# ser = Codec()
# deser = Codec()
# ans = deser.deserialize(ser.serialize(root))
```
+ DFS
```python
class Codec:

    def serialize(self, root):
        """Encodes a tree to a single string.
        
        :type root: TreeNode
        :rtype: str
        """
        if not root:
            return 'None'
        return str(root.val) + ',' + str(self.serialize(root.left)) + ',' + str(self.serialize(root.right))
        
    def deserialize(self, data):
        """Decodes your encoded data to tree.
        
        :type data: str
        :rtype: TreeNode
        """
        def dfs(dataList):
            val = dataList.pop(0)
            if val == 'None':
                return None
            root = TreeNode(int(val))
            root.left = dfs(dataList)
            root.right = dfs(dataList)
            return root

        dataList = data.split(',')
        return dfs(dataList)
```
### 299.猜数字游戏
> 你在和朋友一起玩` 猜数字（Bulls and Cows）`游戏，该游戏规则如下：  
写出一个秘密数字，并请朋友猜这个数字是多少。朋友每猜测一次，你就会给他一个包含下述信息的提示：  
猜测数字中有多少位属于数字和确切位置都猜对了（称为 "Bulls"，公牛），有多少位属于数字猜对了但是位置不对（称为 "Cows"，奶牛）。也就是说，这次猜测中有多少位非公牛数字可以通过重新排列转换成公牛数字。  
给你一个秘密数字` secret `和朋友猜测的数字` guess` ，请你返回对朋友这次猜测的提示。  
提示的格式为` "xAyB" `，`x` 是公牛个数，` y` 是奶牛个数，`A `表示公牛，`B `表示奶牛。  
请注意秘密数字和朋友猜测的数字都可能含有重复数字。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/bulls-and-cows  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def getHint(self, secret: str, guess: str) -> str:
        dict_secret = collections.defaultdict(list)
        dict_guess_count = collections.Counter(guess)
        a = b = 0
        for idx, val in enumerate(secret):
            dict_secret[val].append(idx)
        for idx, letter in enumerate(guess):
            if letter in dict_secret:
                if idx in dict_secret[letter]:
                    a += 1
                    dict_secret[letter].remove(idx)
                    dict_guess_count[letter] -= 1
        for key, value in dict_guess_count.items():
            if key in dict_secret:
                b += min(value,len(dict_secret[key]))
        return str(a)+'A'+str(b)+'B'
```
### 301.删除无效的括号★
> 给你一个由若干括号和字母组成的字符串` s `，删除最小数量的无效括号，使得输入的字符串有效。  
返回所有可能的结果。答案可以按 **任意顺序** 返回。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/minimum-height-trees  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS+回溯
```python
class Solution:
    def removeInvalidParentheses(self, s: str) -> List[str]:
        ans = []
        # 需要移除的左右括号数目
        left, right = 0, 0

        # 统计s中需要移除的左右括号数目
        for ch in s:
            if ch == '(':
                left += 1
            elif ch == ')':
                if left == 0:
                    right += 1
                else:
                    left -= 1

        def is_valid(s):
            # 判断当前字符是否合法
            count = 0
            for ch in s:
                if ch == '(':
                    count += 1
                elif ch == ')':
                    count -= 1
                    # 右括号比左括号多就不合法
                    if count < 0:
                        return False 
            return True if count == 0 else False

        def backtracking(s, start, left, right):
            if left == 0 and right == 0:
                if is_valid(s):
                    ans.append(s)
                return None
            for i in range(start, len(s)):
                # 如果剩余的字符长度都不足删去，则不合法
                if i > start and s[i] == s[i-1]:
                    continue
                if len(s) - i < left + right:
                    break
                if left > 0 and s[i]  == '(':
                    backtracking(s[:i] + s[i+1:], i, left - 1, right)
                if right > 0 and s[i]  == ')':
                    backtracking(s[:i] + s[i+1:], i, left, right - 1)
        
        backtracking(s, 0, left, right)
        return ans
```
### 303.区域和检索
> 给定一个整数数组` nums`，处理以下类型的多个查询:  
计算索引` left `和` right` （包含` left` 和` right`）之间的` nums `元素的 **和** ，其中 `left <= right`  

实现 `NumArray `类：

+ `NumArray(int[] nums)` 使用数组 `nums` 初始化对象
+ `int sumRange(int i, int j)` 返回数组 `nums` 中索引 `left` 和 `right` 之间的元素的 **总和** ，包含 `left` 和 `right` 两点（也就是 `nums[left] + nums[left + 1] + ... + nums[right]` )

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/range-sum-query-immutable  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class NumArray:

    def __init__(self, nums: List[int]):
        # 使用前缀和
        self.sum = [0]
        for i in nums:
            # self.sum[1]是nums第1个元素的和，self.sum[2]存的是nums前2个元素的和...
            self.sum.append(self.sum[-1] + i) 

    def sumRange(self, left: int, right: int) -> int:
        # 算索引left到right，就是算第left+1个值到第right+1个值
        # self.sum[right+1] - self.sum[left]
        return self.sum[right+1] - self.sum[left]


# Your NumArray object will be instantiated and called as such:
# obj = NumArray(nums)
# param_1 = obj.sumRange(left,right)
```
### 304.二维区域和检索-矩阵不可变
> 给定一个二维矩阵` matrix`，以下类型的多个请求：  
计算其子矩形范围内元素的总和，该子矩阵的 **左上角** 为 `(row1, col1)` ，**右下角** 为 `(row2, col2)` 。

实现 `NumMatrix` 类：  
+ `NumMatrix(int[][] matrix)` 给定整数矩阵 `matrix` 进行初始化
+ `int sumRegion(int row1, int col1, int row2, int col2)` 返回 **左上角** `(row1, col1)` 、**右下角** `(row2, col2) `所描述的子矩阵的元素 **总和** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/range-sum-query-2d-immutable  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class NumMatrix:

    def __init__(self, matrix: List[List[int]]):
        if not matrix or not matrix[0]:
            m, n = 0, 0
        else:
            m, n = len(matrix), len(matrix[0])

        self.sum = [[0] * (n + 1) for _ in range(m + 1)]
        for i in range(m):
            for j in range(n):
                self.sum[i+1][j+1] = self.sum[i][j+1] + self.sum[i+1][j] - self.sum[i][j] + matrix[i][j]


    def sumRegion(self, row1: int, col1: int, row2: int, col2: int) -> int:
        return self.sum[row2+1][col2+1] - self.sum[row1][col2+1] - self.sum[row2+1][col1] + self.sum[row1][col1]


# Your NumMatrix object will be instantiated and called as such:
# obj = NumMatrix(matrix)
# param_1 = obj.sumRegion(row1,col1,row2,col2)
```
### 310.最小高度树★
> 树是一个无向图，其中任何两个顶点只通过一条路径连接。 换句话说，一个任何没有简单环路的连通图都是一棵树。  
给你一棵包含` n `个节点的树，标记为` 0 `到` n - 1 `。给定数字` n `和一个有` n - 1 `条无向边的` edges `列表（每一个边都是一对标签），其中` edges[i] = [ai, bi] `表示树中节点` ai `和` bi `之间存在一条无向边。  
可选择树中任何一个节点作为根。当选择节点` x `作为根节点时，设结果树的高度为` h `。在所有可能的树中，具有最小高度的树（即，`min(h)`）被称为 **最小高度树** 。

请你找到所有的 **最小高度树** 并按 **任意顺序** 返回它们的根节点标签列表。  
树的 **高度** 是指根节点和叶子节点之间最长向下路径上边的数量。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/remove-invalid-parentheses/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 拓扑排序+BFS
```python
class Solution:
    def findMinHeightTrees(self, n: int, edges: List[List[int]]) -> List[int]:
        # 如果针对每个节点都来作为根节点计算树高度，时间性能就不好
        # 所以我们从叶子节点出发，倒着去找根，而叶子节点明显就是度为1
        # 特殊情况，只有一个节点
        if n == 1:
            return [0]

        ans = []

        # 统计节点度和边的情况
        degree = [0] * n 
        edges_dict = defaultdict(list)
        for edge in edges:
            degree[edge[0]] += 1
            degree[edge[1]] += 1
            edges_dict[edge[0]].append(edge[1])
            edges_dict[edge[1]].append(edge[0])
        
        # 初始化队列，把所有叶子节点放进去
        queue = deque([i for i in range(n) if degree[i] == 1])

        while queue:
            # ans重新赋值，为的就是最后输出的是最后一层添加进去的node，前面添加的不是根节点
            ans = []
            for i in range(len(queue)):
                node = queue.popleft()
                ans.append(node)
                for edge in edges_dict[node]:
                    degree[edge] -= 1
                    # 当前节点是叶子点了
                    if degree[edge] == 1:
                        queue.append(edge)
        
        return ans
```

+ [最大距离BFS/DFS](https://leetcode-cn.com/problems/minimum-height-trees/solution/zui-xiao-gao-du-shu-by-leetcode-solution-6v6f/)

### 328.奇偶链表
> 给定单链表的头节点` head `，将所有索引为奇数的节点和索引为偶数的节点分别组合在一起，然后返回重新排序的列表。  
第一个节点的索引被认为是` 奇数 `， 第二个节点的索引为` 偶数 `，以此类推。  
请注意，偶数组和奇数组内部的相对顺序应该与输入时保持一致。  
你必须在` O(1) `的额外空间复杂度和` O(n) `的时间复杂度下解决这个问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/odd-even-linked-list  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def oddEvenList(self, head: ListNode) -> ListNode:
        if head == None or head.next == None:
            return head
        odd = head
        even = succ = head.next
        while odd.next and even.next:
            odd.next = even.next
            odd = even.next
            even.next = odd.next
            even = even.next
        odd.next = succ
        return head
```
### 329.矩阵中的最长递增路径
> 给定一个` m x n `整数矩阵` matrix `，找出其中 **最长递增路径** 的长度。  
对于每个单元格，你可以往上，下，左，右四个方向移动。 你 **不能**在 **对角线** 方向上移动或移动到 边界外（即不允许环绕）。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/longest-increasing-path-in-a-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 记忆化搜索
```java
class Solution {
    public int[][] memory; // 记忆化搜索
    public int[][] steps = {{0, 1}, {1, 0}, {0, -1}, {-1, 0}};

    public int longestIncreasingPath(int[][] matrix) {
        if (matrix == null || matrix.length == 0 || matrix[0].length == 0)
            return 0;
        int m = matrix.length;  // 行数
        int n = matrix[0].length;  //列数

        memory = new int[m][n]; // memory[i][j]代表着数组下标为i, j开始的最长路径
        int ans = 0;

        // 每一个位置作为起点进行搜索
        for (int i = 0; i < m; i++)
            for (int j = 0; j < n; j++)
                ans = Math.max(ans, dfs(matrix, i, j, m, n));
        
        return ans;
    }

    public int dfs(int[][] matrix, int x, int y, int m, int n){
        if (memory[x][y] != 0)
            return memory[x][y];  // 之前已经计算过了
        int res = 1;
        // 每一个方向
        for (int[] step: steps){
            int i = x + step[0];
            int j = y + step[1];
            if (isValid(matrix, i, j) && matrix[i][j] > matrix[x][y])
                res = Math.max(res, dfs(matrix, i, j, m, n) + 1);
        }
        memory[x][y] = res;
        return res;
    }

    public boolean isValid(int[][] matrix, int x, int y){
        if (x < 0 || x >= matrix.length || y < 0 || y >= matrix[0].length)
            return false;
        return true;
    }
}
```
### 341.扁平化嵌套列表迭代器
> 给你一个嵌套的整数列表` nestedList `。每个元素要么是一个整数，要么是一个列表；该列表的元素也可能是整数或者是其他列表。请你实现一个迭代器将其扁平化，使之能够遍历这个列表中的所有整数。

实现扁平迭代器类` NestedIterator `：

+ `NestedIterator(List<NestedInteger> nestedList)` 用嵌套列表` nestedList` 初始化迭代器。
+ `int next()` 返回嵌套列表的下一个整数。
+ `boolean hasNext()` 如果仍然存在待迭代的整数，返回 `true` ；否则，返回 `false` 。

你的代码将会用下述伪代码检测：
```
initialize iterator with nestedList
res = []
while iterator.hasNext()
    append iterator.next() to the end of res
return res
```

如果` res `与预期的扁平化列表匹配，那么你的代码将会被判为正确。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/flatten-nested-list-iterator  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 递归
    ```python
    # """
    # This is the interface that allows for creating nested lists.
    # You should not implement it, or speculate about its implementation
    # """
    #class NestedInteger:
    #    def isInteger(self) -> bool:
    #        """
    #        @return True if this NestedInteger holds a single integer, rather than a nested list.
    #        """
    #
    #    def getInteger(self) -> int:
    #        """
    #        @return the single integer that this NestedInteger holds, if it holds a single integer
    #        Return None if this NestedInteger holds a nested list
    #        """
    #
    #    def getList(self) -> [NestedInteger]:
    #        """
    #        @return the nested list that this NestedInteger holds, if it holds a nested list
    #        Return None if this NestedInteger holds a single integer
    #        """

    class NestedIterator:
        def __init__(self, nestedList: [NestedInteger]):
            self.queue = deque()
            self.__dfs(nestedList)
            
        
        def next(self) -> int:
            return self.queue.popleft()
        
        def hasNext(self) -> bool:
            return True if len(self.queue) > 0 else False
        
        def __dfs(self, nestedList):
            for item in nestedList:
                # 是数字，直接添加
                if item.isInteger():
                    self.queue.append(item.getInteger())
                else:
                    # 是列表, 递归求解
                    self.__dfs(item.getList())
                    
    # Your NestedIterator object will be instantiated and called as such:
    # i, v = NestedIterator(nestedList), []
    # while i.hasNext(): v.append(i.next())
    ```

+ 迭代
    ```python
    # """
    # This is the interface that allows for creating nested lists.
    # You should not implement it, or speculate about its implementation
    # """
    #class NestedInteger:
    #    def isInteger(self) -> bool:
    #        """
    #        @return True if this NestedInteger holds a single integer, rather than a nested list.
    #        """
    #
    #    def getInteger(self) -> int:
    #        """
    #        @return the single integer that this NestedInteger holds, if it holds a single integer
    #        Return None if this NestedInteger holds a nested list
    #        """
    #
    #    def getList(self) -> [NestedInteger]:
    #        """
    #        @return the nested list that this NestedInteger holds, if it holds a nested list
    #        Return None if this NestedInteger holds a single integer
    #        """

    class NestedIterator:
        def __init__(self, nestedList):
            self.stack = []
            # 把nestedList中的元素逆序放进栈里
            for i in range(len(nestedList) - 1, -1, -1):
                self.stack.append(nestedList[i])
            

        def next(self):
            # next方法调用的时候必为Integer
            return self.stack.pop().getInteger()

        def hasNext(self):
            while self.stack:
                # 访问栈顶元素
                cur = self.stack[-1]
                # 是Integer，不用处理，直接next调用就好了
                if cur.isInteger():
                    return True
                # 是list，那就把list再次拿出来，逆序放进栈里
                cur = self.stack.pop()
                for i in range(len(cur.getList()) - 1, -1, -1):
                    self.stack.append(cur.getList()[i])
            return False

    # Your NestedIterator object will be instantiated and called as such:
    # i, v = NestedIterator(nestedList), []
    # while i.hasNext(): v.append(i.next())
    ```
### 347.前K个高频元素
> 给你一个整数数组` nums `和一个整数` k `，请你返回其中出现频率前` k `高的元素。你可以按 **任意顺序** 返回答案。

 来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/top-k-frequent-elements/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]:
        # 构造小顶堆
        count_dict = collections.Counter(nums)
        value_key_dict = collections.defaultdict(list)
        for key, value in count_dict.items():
            value_key_dict[value].append(key)
        
        # 总共的元素个数
        n = len(value_key_dict)
        min_heap = []
        ans = []
        count = 0
        for key in value_key_dict:
            if count < k:
                heapq.heappush(min_heap,key)
            else:
                heapq.heappushpop(min_heap,key)
            count += 1
        for i in sorted(min_heap,reverse=True):
            ans += value_key_dict[i]
            if len(ans) == k:
                return ans
        return ans
```
### 350.两个数组的交集II
> 给你两个整数数组` nums1 `和` nums2` ，请你以数组形式返回两数组的交集。返回结果中每个元素出现的次数，应与元素在两个数组中都出现的次数一致（如果出现次数不一致，则考虑取较小值）。可以不考虑输出结果的顺序。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/intersection-of-two-arrays-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def intersect(self, nums1: List[int], nums2: List[int]) -> List[int]:
        my_dict_1 = collections.Counter(nums1)
        my_dict_2 = collections.Counter(nums2)
        result = []
        for key, value in my_dict_2.items():
            if key in my_dict_1:
                for _ in range(min(my_dict_1[key],value)):
                    result.append(key)
        return result
```
### 377.组合总和IV
> 给你一个由 **不同** 整数组成的数组` nums `，和一个目标整数` target `。请你从` nums `中找出并返回总和为` target `的元素组合的个数。

题目数据保证答案符合` 32 `位整数范围。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/combination-sum-iv  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 记忆化搜索
    ```java
    class Solution {
        public int combinationSum4(int[] nums, int target) {
            // 记忆化递归
            // memory[i]表示组合总数为i的情况有多少种
            int[] memory = new int[target + 1];
            Arrays.fill(memory, -1);
            // 加入当前轮次递归到寻找组合总数为0的情况时，说明此时已经找到了一种解了
            memory[0] = 1;
            int ans = dfs(memory, nums, target);
            return ans;
        }

        public int dfs(int[] memory, int[] nums, int target){
            if (target < 0)
                // 当前轮次寻找的总和已经小于0了，说明不存在
                return 0;
            if (memory[target] != -1)
                // 当前轮次的计算结果已经存在了
                return memory[target];
            int ans = 0;
            for (int num: nums)
                ans += dfs(memory, nums, target - num);
            memory[target] = ans;
            return ans;
        }
    }
    ```
+ java 动态规划
    ```java
    class Solution {
        public int combinationSum4(int[] nums, int target) {
            // 动态规划
            // dp[i]表示组合总数为i的情况有多少种
            int[] dp = new int[target + 1];
            // 寻找组合总数为0的情况时
            dp[0] = 1;
            for (int i = 0; i <= target; i++)
                for (int num: nums)
                    if (i - num >= 0)
                        dp[i] += dp[i - num];
            return dp[target];
        }

    }
    ```
### 378.有序矩阵中的第K小的元素
> 给你一个` n x n `矩阵` matrix `，其中每行和每列元素均按升序排序，找到矩阵中第` k `小的元素。  
请注意，它是 **排序后** 的第` k `小元素，而不是第` k `个 **不同** 的元素。  
你必须找到一个内存复杂度优于` O(n2) `的解决方案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/kth-smallest-element-in-a-sorted-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```python
class Solution:
    def kthSmallest(self, matrix: List[List[int]], k: int) -> int:
        # 使用大小为K个元素的大顶堆
        max_heap = []
        count = 0
        for i in range(len(matrix)):
            for j in range(len(matrix[0])):
                if count < k:
                    heapq.heappush(max_heap,-matrix[i][j])
                    count += 1
                else:
                    heapq.heappushpop(max_heap,-matrix[i][j])
        return -heapq.heappop(max_heap)
```
### 380.O(1)时间插入、删除和获取随机元素
实现`RandomizedSet `类：

+ `RandomizedSet()` 初始化 `RandomizedSet` 对象
+ `bool insert(int val)` 当元素` val `不存在时，向集合中插入该项，并返回` true `；否则，返回` false `。
+ `bool remove(int val)` 当元素 `val` 存在时，从集合中移除该项，并返回` true `；否则，返回` false `。
+ `int getRandom()` 随机返回现有集合中的一项（测试用例保证调用此方法时集合中至少存在一个元素）。每个元素应该有 **相同的概率** 被返回。

你必须实现类的所有函数，并满足每个函数的 **平均** 时间复杂度为 `O(1) `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/insert-delete-getrandom-o1  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class RandomizedSet:

    def __init__(self):
        # 存储键值对，val-index_in_list
        self.val_dict = {}
        # 存val，生成index
        self.val_list = []

    def insert(self, val: int) -> bool:
        if val in self.val_dict:
            return False
        self.val_list.append(val)
        self.val_dict[val] = len(self.val_list) - 1
        return True

    def remove(self, val: int) -> bool:
        if val not in self.val_dict:
            return False
        tail, val_idx = self.val_list[-1], self.val_dict[val]
        self.val_dict[tail], self.val_list[val_idx] = val_idx, tail
        self.val_list.pop()
        del self.val_dict[val]
        return True

    def getRandom(self) -> int:
        return random.choice(self.val_list)



# Your RandomizedSet object will be instantiated and called as such:
# obj = RandomizedSet()
# param_1 = obj.insert(val)
# param_2 = obj.remove(val)
# param_3 = obj.getRandom()
```
### 394.字符串解码★
> 给定一个经过编码的字符串，返回它解码后的字符串。  
编码规则为: `k[encoded_string]`，表示其中方括号内部的` encoded_string `正好重复` k `次。注意` k `保证为正整数。

你可以认为输入字符串总是有效的；输入字符串中没有额外的空格，且输入的方括号总是符合格式要求的。

此外，你可以认为原始数据不包含数字，所有的数字只表示重复的次数` k `，例如不会出现像` 3a `或` 2[4] `的输入。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/decode-string  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 栈
    ```python
    class Solution:
        def decodeString(self, s: str) -> str:
            # 典型的括号匹配问题，自然就联想到栈
            stack, ans, multi = [], "", 0
            for c in s:
                if c == '[':
                    # 遇到左括号的时候，直接将前面记录的系数和字符压入栈里
                    stack.append([ans, multi])
                    # 系数和字符重新置零
                    ans, multi = "", 0
                elif c == ']':
                    # 遇到右括号，取出最近的系数和字符进行拼接答案
                    last_ans, cur_multi = stack.pop()
                    ans = last_ans + cur_multi * ans
                elif '0' <= c <= '9':
                    # 遇到数字，拼接成int型
                    multi = multi * 10 + int(c)            
                else:
                    # 遇到字母，拼接
                    ans += c
            return ans
    ```

+ 递归
    ```python
    class Solution:
        def decodeString(self, s: str) -> str:
            # 其实括号里面的内容可以当作最原始的字符串处理，也就是递归
            def dfs(s, i):
                # s为待处理的字符串，i为字符串该递归轮次开始处理的下标位置
                ans, multi = "", 0
                # 字符串还没处理完时
                while i < len(s):
                    if '0' <= s[i] <= '9':
                        # 遇到数字，组合int型系数
                        multi = multi * 10 + int(s[i])
                    elif s[i] == '[':
                        # 遇到左括号，说明新一轮处理该开始了，递归
                        i, tmp = dfs(s, i + 1)
                        # 更新字符
                        ans += multi * tmp
                        # 系数置零
                        multi = 0
                    elif s[i] == ']':
                        # 遇到右括号，代表这一个括号里的部分结束处理
                        return i, ans
                    else:
                        # 字符拼接
                        ans += s[i]
                    i += 1
                return ans
            return dfs(s, 0)

    ```
### 395.至少有 K 个重复字符的最长子串
> 给你一个字符串` s `和一个整数` k `，请你找出` s `中的最长子串， 要求该子串中的每一字符出现次数都不少于` k `。返回这一子串的长度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-substring-with-at-least-k-repeating-characters/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def longestSubstring(self, s: str, k: int) -> int:
        n = len(s)
        longest = 0  # 记录符合题目要求的最长substring长度
        for chr_kind in range(1, 27):   # 每次要固定一个变量
            char_freq = defaultdict(int)  # 记录string s当中slow到fast（包含）之间所有的字母出现的频率
            slow, fast = 0, 0
            total, less = 0, 0  # total:窗口内字母的种类  less:个数小于k的种类
            while fast < n: # 滑动窗口
                char_freq[s[fast]] += 1
                # 当字母频率为1时
                if char_freq[s[fast]] == 1:
                    total += 1  # 字母种类加一
                    less += 1   # 小于k的种类加一
                # 当字母频率达到k时
                if char_freq[s[fast]] == k:
                    less -= 1  # 小于k的种类减一
                # 符合slow指针移动的条件
                while total > chr_kind:
                    char_freq[s[slow]] -= 1
                    if char_freq[s[slow]] == k - 1:
                        less += 1
                    if char_freq[s[slow]] == 0:
                        total -= 1
                        less -= 1
                    slow += 1
                # 符合某些判断条件
                if less == 0:
                    longest = max(longest, fast - slow + 1)
                fast += 1
        return longest
```
### 399.除法求值★
> 给你一个变量对数组` equations `和一个实数值数组` values `作为已知条件，其中` equations[i] = [Ai, Bi] `和` values[i] `共同表示等式` Ai / Bi = values[i] `。每个 `Ai `或 `Bi` 是一个表示单个变量的字符串。  
另有一些以数组 `queries` 表示的问题，其中` queries[j] = [Cj, Dj] `表示第 `j` 个问题，请你根据已知条件找出` Cj / Dj = ? `的结果作为答案。  
返回 **所有问题的答案** 。如果存在某个无法确定的答案，则用 `-1.0 `替代这个答案。如果问题中出现了给定的已知条件中没有出现的字符串，也需要用` -1.0` 替代这个答案。

注意：输入总是有效的。你可以假设除法运算中不会出现除数为` 0` 的情况，且不存在任何矛盾的结果。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/evaluate-division  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
+ 并查集
    ```python
    class UnionFind:
        def __init__(self):
            # 记录每个节点的父节点
            self.father = {}
            # 记录每个节点到根节点的值
            self.values = {}

        def add(self, x):
            if x not in self.father:
                self.father[x] = None
                self.values[x] = 1.0

        def merge(self, x, y, val):
            root_x, root_y = self.find(x), self.find(y)
            if root_x != root_y:
                self.father[root_x] = root_y
                self.values[root_x] = self.values[y] * val / self.values[x]
        
        def find(self, x):
            root = x
            # 倍数
            base = 1
            while self.father[root] is not None:
                root = self.father[root]
                base *= self.values[root]
            
            while root != x:
                origin_father = self.father[x]
                # 更新倍数
                self.values[x] *= base
                base /= self.values[origin_father]
                self.father[x] = root
                x = origin_father

            return root

        def is_connected(self, x, y):
            return x in self.values and y in self.values and self.find(x) == self.find(y)

    class Solution:
        def calcEquation(self, equations: List[List[str]], values: List[float], queries: List[List[str]]) -> List[float]:
            union = UnionFind()
            # 遍历算式
            for (a, b), val in zip(equations, values):
                union.add(a)
                union.add(b)
                union.merge(a, b, val)
        
            res = [-1.0] * len(queries)

            for i, (a, b) in enumerate(queries):
                if union.is_connected(a, b):
                    res[i] = union.values[a] / union.values[b]
            return res
    ```
### 403.青蛙过河
> 一只青蛙想要过河。 假定河流被等分为若干个单元格，并且在每一个单元格内都有可能放有一块石子（也有可能没有）。 青蛙可以跳上石子，但是不可以跳入水中。  
给你石子的位置列表` stones`（用单元格序号 升序 表示）， 请判定青蛙能否成功过河（即能否在最后一步跳至最后一块石子上）。开始时， 青蛙默认已站在第一块石子上，并可以假定它第一步只能跳跃` 1 `个单位（即只能从单元格` 1 `跳至单元格` 2 `）。  
如果青蛙上一步跳跃了` k `个单位，那么它接下来的跳跃距离只能选择为` k - 1、k `或` k + 1 `个单位。 另请注意，青蛙只能向前方（终点的方向）跳跃。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/frog-jump  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 记忆化搜索
```java
class Solution {
    // 记忆化搜索
    public Map<Integer, Boolean> memory = new HashMap<>();

    public boolean canCross(int[] stones) {
        return dfs(stones, 0, 0);
    }

    public boolean dfs(int[] stones, int k, int index){
        // 成功走到最后一块石子
        if (index == stones.length - 1)
            return true;
        int key = index * 1000 + k;  // 构造hash
        // 如果为true，就代表着之前这里已经计算过了，如果真的可以跳到终点的话已经就返回了，就不会再执行这里了，所以说明此路不通，直接false
        if (memory.containsKey(key))
            return false;
        memory.put(key, true);
        for (int i = index + 1; i < stones.length; i++){
            // 计算下一块石头和当前石头的距离
            int dist = stones[i] - stones[index];
            // 只能走k-1,k,k+1步
            if (k - 1 <= dist && dist <= k + 1)
                if (dfs(stones, dist, i))
                    return true;
            // 跳最远都上不了下一块石头，后续更远的就更不可能了
            else if (dist > k + 1)
                break;
        }
        return false;
    }
}
```
### 409.最长回文串
> 给定一个包含大写字母和小写字母的字符串` s `，返回 通过这些字母构造成的 **最长的回文串** 。  
在构造过程中，请注意 **区分大小写** 。比如` "Aa" `不能当做一个回文字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-palindrome  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def longestPalindrome(self, s: str) -> int:
        if len(s) == 1:
            return 1
        ans = 0
        has_odd = False
        count_dict = collections.Counter(s)
        for key, value in count_dict.items():
            if value % 2 == 0: # 这个字母是偶数个，肯定可以两边拆开放
                ans += value
            else:  # 奇数个
                has_odd = True
                if value != 1: # 去掉一个又成偶数了
                    ans += (value - 1)
        if has_odd:
            ans += 1
        return ans
```
### 417.太平洋大西洋水流问题
> 有一个` m × n `的矩形岛屿，与 **太平洋** 和 **大西洋** 相邻。 “太平洋” 处于大陆的左边界和上边界，而 “大西洋” 处于大陆的右边界和下边界。  
这个岛被分割成一个由若干方形单元格组成的网格。给定一个` m x n `的整数矩阵` heights `，` heights[r][c] `表示坐标` (r, c) `上单元格 **高于海平面的高度** 。  
岛上雨水较多，如果相邻单元格的高度 小于或等于 当前单元格的高度，雨水可以直接向北、南、东、西流向相邻单元格。水可以从海洋附近的任何单元格流入海洋。

返回 **网格坐标** `result` 的 `2D`列表 ，其中 `result[i] = [ri, ci]` 表示雨水可以从单元格` (ri, ci)` 流向 **太平洋和大西洋** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/pacific-atlantic-water-flow  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def pacificAtlantic(self, heights: List[List[int]]) -> List[List[int]]:
        # BFS, 从海洋出发，逆向思维水往高处流，两边海洋都能去的点就是答案
        m, n = len(heights), len(heights[0])
        
        visited = set()
        queue = deque()
        ans = []

        def bfs(ocean=None):
            while queue:
                i, j = queue.popleft()
                # 东南西北四个方向
                for x, y in [(i+1, j), (i-1, j), (i, j+1), (i, j-1)]:
                    # 水往高处流
                    if 0 <= x < m and 0 <= y < n and heights[x][y] >= heights[i][j] and ((x, y), ocean) not in visited:
                        visited.add(((x, y), ocean))
                        queue.append((x, y))

        # pacific ocean水往高处流
        for i in range(m):
            # set集是((坐标)，海洋类型)
            visited.add(((i, 0), 0))
            queue.append((i, 0))
        for i in range(1, n):
            visited.add(((0, i), 0))
            queue.append((0, i))
        bfs(ocean=0)

        # atlantic ocean水往高处流
        for i in range(m):
            # set集是((坐标)，海洋类型)
            visited.add(((i, n-1), 1))
            queue.append((i, n-1))
        for i in range(n-1):
            visited.add(((m-1, i), 1))
            queue.append((m-1, i))
        bfs(ocean=1)

        # 如果两边都在，就说明这个点可以到达
        for i in range(m):
            for j in range(n):
                if ((i, j), 0) in visited and ((i, j), 1) in visited:
                    ans.append([i, j])
        
        return ans
```
### 424.替换后的最长重复字符
> 给你一个字符串` s `和一个整数` k `。你可以选择字符串中的任一字符，并将其更改为任何其他大写英文字符。该操作最多可执行` k `次。  
在执行上述操作后，返回包含相同字母的最长子字符串的长度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-repeating-character-replacement  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def characterReplacement(self, s: str, k: int) -> int:
        n = len(s)
        slow, fast = 0, 0
        char_freq = collections.Counter()
        longest = 0
        while fast < n:
            char_freq[s[fast]] += 1
            # 达到slow的右移条件,即除去出现最多的字符之外，其余的字符出现次数大于k
            while fast - slow + 1 - char_freq.most_common(1)[0][1] > k:
                char_freq[s[slow]] -= 1
                slow += 1
            # 符合条件
            longest = max(longest, fast - slow + 1)
            fast += 1
        return longest
```
### 427.建立四叉树
> 给你一个` n * n `矩阵` grid` ，矩阵由若干` 0 `和 `1 `组成。请你用四叉树表示该矩阵` grid `。  
你需要返回能表示矩阵的 **四叉树** 的根结点。

注意，当` isLeaf `为 `False` 时，你可以把` True `或者` False `赋值给节点，两种值都会被判题机制 **接受** 。

四叉树数据结构中，每个内部节点只有四个子节点。此外，每个节点都有两个属性：

+ `val`：储存叶子结点所代表的区域的值。`1 `对应` True`，`0 `对应 `False`；
+ `isLeaf`: 当这个节点是一个叶子结点时为` True`，如果它有` 4 `个子节点则为` False` 。
```java
class Node {
    public boolean val;
    public boolean isLeaf;
    public Node topLeft;
    public Node topRight;
    public Node bottomLeft;
    public Node bottomRight;
}
```

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/construct-quad-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 递归+前缀和
    ```python
    """
    # Definition for a QuadTree node.
    class Node:
        def __init__(self, val, isLeaf, topLeft, topRight, bottomLeft, bottomRight):
            self.val = val
            self.isLeaf = isLeaf
            self.topLeft = topLeft
            self.topRight = topRight
            self.bottomLeft = bottomLeft
            self.bottomRight = bottomRight
    """

    class Solution:
        def construct(self, grid: List[List[int]]) -> 'Node':
            # 前缀和数组
            n = len(grid)
            pre = [[0]*(n + 1) for _ in range(n + 1)]
            for i in range(1, n + 1):
                for j in range(1, n + 1):
                    # 构造二位前缀和
                    pre[i][j] = pre[i-1][j] + pre[i][j-1] - pre[i-1][j-1] + grid[i-1][j-1]
            
            def get_sum(a, b, c, d):
                # 代表矩阵左上角位置为(a, b)，右下角位置为(c, d)
                return pre[c+1][d+1] - pre[a][d+1] - pre[c+1][b] + pre[a][b]
            
            def dfs(a, b, c, d):
                # 当前矩阵的总和
                curr_sum = get_sum(a, b, c, d)
                # 当前矩阵的总格子数
                total_grids = (c - a + 1) * (d - b + 1)
                # 格子内全为0或者全为1，叶子节点
                if curr_sum == 0 or curr_sum == total_grids:
                    return Node(grid[a][b] == 1, True)
                
                root = Node(grid[a][b] == 1, False)
                root.topLeft = dfs(a, b, (a + c) // 2, (b + d) // 2)
                root.topRight = dfs(a, (b + d) // 2 + 1, (a + c) // 2, d)
                root.bottomLeft = dfs((a + c) // 2 + 1, b, c, (b + d) // 2)
                root.bottomRight = dfs((a + c) // 2 + 1, (b + d) // 2 + 1, c, d)
                return root

            return dfs(0, 0, n -1, n - 1)
    ```
### 433.最小基因变化
> 基因序列可以表示为一条由` 8 `个字符组成的字符串，其中每个字符都是` 'A'、'C'、'G' `和` 'T' `之一。  
假设我们需要调查从基因序列` start `变为` end `所发生的基因变化。一次基因变化就意味着这个基因序列中的一个字符发生了变化。  
例如，`"AACCGGTT" --> "AACCGGTA" `就是一次基因变化。  
另有一个基因库` bank `记录了所有有效的基因变化，只有基因库中的基因才是有效的基因序列。  
给你两个基因序列` start `和` end `，以及一个基因库` bank `，请你找出并返回能够使` start `变化为` end `所需的最少变化次数。如果无法完成此基因变化，返回` -1 `。

注意：起始基因序列` start `默认是有效的，但是它并不一定会出现在基因库中。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/minimum-genetic-mutation  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java的BFS
```java
class Solution {
    //记录基本的基因组成字符
    public static char[] base = {'A', 'C', 'G', 'T'};

    public int minMutation(String start, String end, String[] bank) {
        //把bank转成set，这样子查找元素更快
        Set<String> bank_set = new HashSet<>();
        for(String s: bank)
            bank_set.add(s);
        //定义队列
        Deque<String> queue = new ArrayDeque<>();
        queue.addLast(start);
        //记录变化步数
        Map<String, Integer> map = new HashMap<>();
        map.put(start, 0);

        while(!queue.isEmpty()){
            //获取队列当前元素长度
            int size = queue.size();
            while(size > 0){
                String s = queue.pollFirst();
                char[] char_s = s.toCharArray();
                int step = map.get(s);
                //对于基因序列里面的每一个字符
                for(int i = 0; i < 8; i++)
                    // 替换每一个字符为其他的三种基本字符
                    for(char c: base){
                        if(char_s[i] == c) continue;
                        char[] clone = char_s.clone();
                        //字符替换
                        clone[i] = c;
                        String sub = String.valueOf(clone);
                        //不在有效基因列表里面
                        if(!bank_set.contains(sub)) continue;
                        //该形式的基因序列之前已经遍历到了，不需要再重复遍历了
                        if(map.containsKey(sub)) continue;
                        //获取到最终基因了
                        if(sub.equals(end))
                            return step + 1;
                        map.put(sub, step + 1);
                        queue.addLast(sub);
                    }
                size--;
            }
        }

        return -1;
    }
}
```
### 436.寻找右区间
> 给你一个区间数组` intervals `，其中` intervals[i] = [starti, endi] `，且每个` starti `都 **不同** 。  
区间` i `的 **右侧区间** 可以记作区间` j `，并满足` startj >= endi `，且` startj `最小化 。

返回一个由每个区间` i `的 **右侧区间** 的最小起始位置组成的数组。如果某个区间` i `不存在对应的 右侧区间 ，则下标` i `处的值设为` -1 `。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/find-right-interval  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def findRightInterval(self, intervals: List[List[int]]) -> List[int]:
        for i, interval in enumerate(intervals):
            interval.append(i)
        intervals.sort()

        n = len(intervals)
        ans = [-1] * n
        for _, end, id in intervals:
            i = bisect_left(intervals, [end])
            if i < n:
                ans[id] = intervals[i][2]
        return ans
```
### 442.数组中的重复数字
> 给你一个长度为` n `的整数数组` nums `，其中` nums `的所有整数都在范围` [1, n] `内，且每个整数出现 **一次** 或 **两次** 。请你找出所有出现 **两次** 的整数，并以数组形式返回。

你必须设计并实现一个时间复杂度为` O(n) `且仅使用**常量额外空间**的算法解决此问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-all-duplicates-in-an-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java原地哈希(数字i定义到数组下标为i-1的位置)
    ```java
    class Solution {
        public List<Integer> findDuplicates(int[] nums) {
            int n = nums.length;

            for (int i = 0; i < n; ++i) {
                //把数i放置在数组中下标为i-1的位置，放置到一个不冲突的位置
                while (nums[i] != nums[nums[i] - 1]) {
                    swap(nums, i, nums[i] - 1);
                }
            }

            List<Integer> ans = new ArrayList<Integer>();
            for (int i = 0; i < n; ++i) {
                if (nums[i] - 1 != i) {
                    ans.add(nums[i]);
                }
            }

            return ans;
        }

        public void swap(int[] nums, int a, int b){
            int tmp = nums[a];
            nums[a] = nums[b];
            nums[b] = tmp;
        }
    }
    ```
### 449.序列化和反序列化二叉搜索树
> 序列化是将数据结构或对象转换为一系列位的过程，以便它可以存储在文件或内存缓冲区中，或通过网络连接链路传输，以便稍后在同一个或另一个计算机环境中重建。

设计一个算法来序列化和反序列化 **二叉搜索树** 。 对序列化/反序列化算法的工作方式没有限制。 您只需确保二叉搜索树可以序列化为字符串，并且可以将该字符串反序列化为最初的二叉搜索树。

**编码的字符串应尽可能紧凑**。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/serialize-and-deserialize-bst  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ java
    ```java
    /**
    * Definition for a binary tree node.
    * public class TreeNode {
    *     int val;
    *     TreeNode left;
    *     TreeNode right;
    *     TreeNode(int x) { val = x; }
    * }
    */
    public class Codec {

        // Encodes a tree to a single string.
        public String serialize(TreeNode root) {
            List<String> vals = new ArrayList<>();
            preOrder(vals, root);
            StringBuilder sb = new StringBuilder();
            // 使用逗号拼接
            for(int i = 0; i < vals.size(); i++){
                sb.append(vals.get(i));
                if (i != vals.size() - 1)
                    sb.append(",");
            }

            return sb.toString();
        }

        // Decodes your encoded data to tree.
    public TreeNode deserialize(String s) {
            if (s == null || s.equals("")) return null;
            String[] ss = s.split(",");
            return dfs(0, ss.length - 1, ss);
        }

        public TreeNode dfs(int l, int r, String[] ss) {
            if (l > r) return null;
            int j = l + 1, t = Integer.parseInt(ss[l]);
            TreeNode ans = new TreeNode(t);
            while (j <= r && Integer.parseInt(ss[j]) <= t) j++;
            ans.left = dfs(l + 1, j - 1, ss);
            ans.right = dfs(j, r, ss);
            return ans;
        }

        public void preOrder(List<String> vals, TreeNode root){
            if(root == null)
                return ;
            vals.add(String.valueOf(root.val));
            preOrder(vals, root.left);
            preOrder(vals, root.right);
        }

    }

    // Your Codec object will be instantiated and called as such:
    // Codec ser = new Codec();
    // Codec deser = new Codec();
    // String tree = ser.serialize(root);
    // TreeNode ans = deser.deserialize(tree);
    // return ans;
    ```
+ python
    ```python
    # Definition for a binary tree node.
    # class TreeNode:
    #     def __init__(self, x):
    #         self.val = x
    #         self.left = None
    #         self.right = None

    class Codec:

        def serialize(self, root: TreeNode) -> str:
            """Encodes a tree to a single string.
            """
            # 采用前序遍历将二叉搜索树节点遍历完整，使用逗号拼接
            vals = []
            def pre_order(root):
                if root:
                    # 前序遍历
                    vals.append(root.val)
                    pre_order(root.left)
                    pre_order(root.right)
            
            pre_order(root)
            return ','.join(map(str, vals))


        def deserialize(self, data: str) -> TreeNode:
            """Decodes your encoded data to tree.
            """
            if not data or data == '':
                return None
            vals = list(map(int, data.split(',')))
            root = TreeNode(vals[0])
            left_vals = [x for x in vals if x < vals[0]]
            right_vals = [x for x in vals if x > vals[0]]
            root.left = self.deserialize(','.join(map(str, left_vals)))
            root.right = self.deserialize(','.join(map(str, right_vals)))
            return root
    # Your Codec object will be instantiated and called as such:
    # Your Codec object will be instantiated and called as such:
    # ser = Codec()
    # deser = Codec()
    # tree = ser.serialize(root)
    # ans = deser.deserialize(tree)
    # return ans
    ```

### 450.删除二叉搜索树中的节点
> 给定一个二叉搜索树的根节点 root 和一个值 key，删除二叉搜索树中的 key 对应的节点，并保证二叉搜索树的性质不变。返回二叉搜索树（有可能被更新）的根节点的引用。

一般来说，删除节点可分为两个步骤：

1. 首先找到需要删除的节点；
2. 如果找到了，删除它。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/delete-node-in-a-bst  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public TreeNode deleteNode(TreeNode root, int key) {
        if (root == null) return null;
        if (root.val == key) {
            if (root.left == null) return root.right;
            if (root.right == null) return root.left;
            TreeNode t = root.left;
            while (t.right != null) t = t.right;
            t.right = root.right;
            return root.left;
        } else if (root.val < key) root.right = deleteNode(root.right, key);
        else root.left = deleteNode(root.left, key);
        return root;
    }
}
```
### 454.四数相加Ⅱ
> 给你四个整数数组` nums1`、`nums2`、`nums3` 和` nums4 `，数组长度都是` n `，请你计算有多少个元组` (i, j, k, l) `能满足：

+ `0 <= i, j, k, l < n`
+ `nums1[i] + nums2[j] + nums3[k] + nums4[l] == 0`

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/4sum-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def fourSumCount(self, nums1: List[int], nums2: List[int], nums3: List[int], nums4: List[int]) -> int:
        # 两两分组，妙啊
        countAB = collections.Counter(u + v for u in nums1 for v in nums2)
        ans = 0
        for u in nums3:
            for v in nums4:
                if -u - v in countAB:
                    ans += countAB[-u - v]
        return ans

```
### 462.最少移动次数使数组元素相等II
> 给你一个长度为` n `的整数数组` nums `，返回使所有数组元素相等需要的最少移动数。  
在一步操作中，你可以使数组中的一个元素加` 1 `或者减` 1 `。

Tip：一个优秀的题解，核心在于目标[为什么是中位数](https://leetcode.cn/problems/minimum-moves-to-equal-array-elements-ii/solution/by-fuxuemingzhu-13z3/)

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/minimum-moves-to-equal-array-elements-ii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python双指针
```python
class Solution:
    def minMoves2(self, nums: List[int]) -> int:
        nums.sort()
        left, right, ans = 0, len(nums) - 1, 0
        while left < right:
            ans += nums[right] - nums[left]
            left += 1
            right -= 1

        return ans
```
### 464.我能赢吗
> 在 "100 game" 这个游戏中，两名玩家轮流选择从 1 到 10 的任意整数，累计整数和，先使得累计整数和 **达到或超过**  100 的玩家，即为胜者。  
如果我们将游戏规则改为 “玩家 **不能** 重复使用整数” 呢？  
例如，两个玩家可以轮流从公共整数池中抽取从 1 到 15 的整数（不放回），直到累计整数和 >= 100。  
给定两个整数` maxChoosableInteger` （整数池中可选择的最大数）和 desiredTotal（累计和），若先出手的玩家是否能稳赢则返回 `true `，否则返回` false `。假设两位玩家游戏时都表现 **最佳** 。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/can-i-win  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 记忆化搜索
```java
class Solution {
     public boolean canIWin(int maxChoosableInteger, int desiredTotal) {
        //总长度不满足目标值
        if (maxChoosableInteger * (maxChoosableInteger + 1) < (desiredTotal * 2)) {
            return false;
        }
        //存储state的变量值，state一共有2^maxChoosableInteger种
        Map<Integer, Boolean> memory = new HashMap<>(1 << maxChoosableInteger);
        //开始遍历整个树
        return dfs(maxChoosableInteger, 0, desiredTotal, 0, memory);
    }

    private boolean dfs(int maxChoosableInteger, int state, int desiredTotal, int curTotal, Map<Integer, Boolean> memory) {
        if (!memory.containsKey(state)) {
            boolean ans = false;
            for (int i = 0; i < maxChoosableInteger; i++) {
                //state的第i位表示 第i+1个数字被使用
                if (((state >> i) & 1) == 1) {
                    continue;
                }
                //先手取i看 能不能赢 不能赢则轮到对手取数字
                if (curTotal + i + 1 >= desiredTotal) {
                    ans = true;
                    break;
                }
                //轮到对手取数字 若对手不能赢（必然输掉的状态） 则我方赢
                //state | (1 << i), 将state的第i位置为已使用
                if (!dfs(maxChoosableInteger, state | (1 << i), desiredTotal, curTotal + i + 1, memory)) {
                    ans = true;
                    break;
                }
            }
            memory.put(state, ans);
        }
        return memory.get(state);
    }
}
```
### 467.环绕字符串中唯一的子字符串
> 把字符串` s `看作是` “abcdefghijklmnopqrstuvwxyz” `的无限环绕字符串，所以` s `看起来是这样的：

+ `"...zabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcd...."` . 

现在给定另一个字符串` p `。返回` s `中 **唯一** 的` p `的 **非空子串** 的数量 。 

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/unique-substrings-in-wraparound-string  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python 滑动窗口
```python
class Solution:
    def findSubstringInWraproundString(self, p: str) -> int:
        p = '^' + p  # 确保p字符串的长度是≥2的，这样下面的for循环才能处理只有一位长的字符串p
        # 这个map代表着以某个字母结尾的最大连续长度
        len_mapper = collections.defaultdict(lambda: 0)
        w = 1
        for i in range(1,len(p)):
            if ord(p[i])-ord(p[i-1]) == 1 or ord(p[i])-ord(p[i-1]) == -25:
                w += 1
            else:
                w = 1
            len_mapper[p[i]] = max(len_mapper[p[i]], w)

        return sum(len_mapper.values())
```
### 472.连接词
> 给你一个**不含重复**单词的字符串数组` words `，请你找出并返回` words `中的所有 **连接词** 。

**连接词** 定义为：一个完全由给定数组中的至少两个较短单词组成的字符串。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/concatenated-words  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 字典树+记忆化搜索
```java
class Solution {
    class TrieNode{
        boolean isEnd;
        TrieNode[] next;

        public TrieNode(){
            this.isEnd = false;
            this.next = new TrieNode[26];
        }
    }

    // 定义根节点
    public TrieNode root = new TrieNode();

    public List<String> findAllConcatenatedWordsInADict(String[] words) {
        List<String> ans = new ArrayList<>();  // 定义最终答案
        Arrays.sort(words, (a, b) -> a.length() - b.length());
        for (String word: words){
            // 该词长度为0，直接跳过
            if (word.length() == 0)
                continue;
            boolean[] visited = new boolean[word.length()];
            if (dfs(word, 0, visited))
                ans.add(word);
            else
                insert(word);
        }
        return ans;
    }

    public boolean dfs(String word, int start, boolean[] visited){
        // 判断完了，是一个连接词
        if (word.length() == start)
            return true;
        if (visited[start])
            return false;
        visited[start] = true;
        TrieNode node = this.root;
        for (int i = start; i < word.length(); i++){
            char c = word.charAt(i);
            node = node.next[c - 'a'];
            if (node == null)
                return false;
            if (node.isEnd)
                if (dfs(word, i + 1, visited))
                    return true;
        }
        return false;
    }

    public void insert(String word){
        TrieNode node = this.root;
        for (char c: word.toCharArray()){
            if (node.next[c - 'a'] == null)
                node.next[c - 'a'] = new TrieNode();
            node = node.next[c - 'a'];
        }
        node.isEnd = true;
    }
}
```
### 518.零钱兑换II
> 给你一个整数数组` coins `表示不同面额的硬币，另给一个整数 `amount `表示总金额。  
请你计算并返回可以凑成总金额的硬币组合数。如果任何硬币组合都无法凑出总金额，返回` 0 `。  
假设每一种面额的硬币有无限个。 

题目数据保证结果符合` 32 `位带符号整数

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/coin-change-2  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java 动态规划
```java
class Solution {
    public int change(int amount, int[] coins) {
        // dp[i]代表总额i存在的兑换方法种数
        int[] dp = new int[amount + 1];
        dp[0] = 1;
        for (int coin: coins)
            for (int i = 0; i <= amount; i++)
                if (i - coin >= 0)
                    dp[i] += dp[i - coin];
        return dp[amount];
    }
}
```
### 526.优美的排列
> 假设有从` 1 `到` n `的` n `个整数。用这些整数构造一个数组` perm`（下标从` 1 `开始），只要满足下述条件**之一** ，该数组就是一个 **优美的排列** ：

+ `perm[i]` 能够被` i `整除
+ `i `能够被` perm[i] `整除

给你一个整数` n `，返回可以构造的 **优美排列**的 **数量** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/beautiful-arrangement  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java回溯
    ```java
    class Solution {
        //因为n个整数不重复，所以需要记录当前数字是否已经被使用了
        public boolean[] visited;
        //先预处理，保存每个位置可能满足整除条件的结果
        public List<Integer>[] possible;
        //优美排列的数量
        public int ans = 0;

        public int countArrangement(int n) {
            //初始化数据结构
            visited = new boolean[n + 1];
            possible = new List[n + 1];
            for(int i = 0; i <= n; i++)
                possible[i] = new ArrayList<Integer>();
            //预处理，计算可能解
            for(int i = 1; i <= n; i++)
                for(int j = 1; j <= n; j++)
                    //可能的解
                    if(i % j == 0 || j % i == 0)
                        possible[i].add(j);
            
            backtracking(1, n);
            return ans;
        }

        public void backtracking(int start, int n){
            if(start > n){
                ans++;
                return ;
            }
            //遍历该位置的所有可能解
            for(int num: possible[start])
                if(!visited[num]){
                    visited[num] = true;
                    backtracking(start + 1, n);
                    visited[num] = false;
                } 
        }
    }
    ```
### 528.按权重随机选择
> 给你一个 下标从` 0 `开始 的正整数数组` w `，其中` w[i] `代表第` i `个下标的权重。  
请你实现一个函数` pickIndex `，它可以 随机地 从范围` [0, w.length - 1]` 内（含 `0` 和` w.length - 1`）选出并返回一个下标。选取下标` i` 的 概率 为` w[i] / sum(w)` 。

例如，对于` w = [1, 3]`，挑选下标` 0 `的概率为` 1 / (1 + 3) = 0.25 `（即，`25%`），而选取下标` 1 `的概率为` 3 / (1 + 3) = 0.75`（即，`75%`）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/random-pick-with-weight  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:

    def __init__(self, w: List[int]):
        # 计算前缀和，这样可以生成一个随机数，根据数的大小对应分布的坐标
        self.presum = list(accumulate(w))

    def pickIndex(self) -> int:
        x = random.randint(1, self.presum[-1])
        return bisect_left(self.presum, x)



# Your Solution object will be instantiated and called as such:
# obj = Solution(w)
# param_1 = obj.pickIndex()
```
### 540.有序数组中的单一元素
> 给你一个仅由整数组成的有序数组，其中每个元素都会出现两次，唯有一个数只会出现一次。  
请你找出并返回只出现一次的那个数。  
你设计的解决方案必须满足` O(log n) `时间复杂度和` O(1) `空间复杂度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/single-element-in-a-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def singleNonDuplicate(self, nums: List[int]) -> int:
        length = len(nums)
        if length == 1:
            return nums[0]
        left, right = 0, length - 1
        ans = -1
        while left < right:
            mid = left + (right - left) // 2
            is_odd = True if (right - mid) % 2 == 1 else False
            if nums[mid] == nums[mid-1]:  
                if is_odd:  # 说明单独的那一个在右边
                    left = mid + 1
                    ans = nums[left]
                else:  # 说明单独的那一个在左边
                    right = mid - 2
                    ans = nums[right]
            elif nums[mid] == nums[mid+1]:
                if is_odd:  # 说明单独的那一个在左边
                    right = mid - 1
                    ans = nums[right]      
                else:  # 说明单独的那一个在右边
                    left = mid + 2
                    ans = nums[left]
            else:
                return nums[mid]
        return ans
```
### 542. 01矩阵
> 给定一个由` 0 `和` 1 `组成的矩阵` mat `，请输出一个大小相同的矩阵，其中每一个格子是` mat `中对应位置元素到最近的` 0 `的距离。  
两个相邻元素间的距离为` 1 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/01-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def updateMatrix(self, mat: List[List[int]]) -> List[List[int]]:
        # 看见最近距离，就联想到BFS
        m, n = len(mat), len(mat[0])
        # 把等于0的位置的点放进队列里面去作为起点，去搜寻最近的1
        zero = [(i, j) for i in range(m) for j in range(n) if mat[i][j]  == 0]
        queue = deque(zero)
        # 已经访问过的点不再去考虑
        visited = set(zero)
        # 记录距离
        dist = [[0]*n for _ in range(m)]

        while queue:
            i, j = queue.popleft()
            # 对上下左右四个方向进行搜索
            for x, y in [(i-1, j), (i+1, j), (i, j-1), (i, j+1)]:
                if 0 <= x < m and 0 <= y < n and (x, y) not in visited:
                    visited.add((x, y))
                    dist[x][y] = dist[i][j] + 1
                    queue.append((x, y))
        
        return dist
```
### 543.二叉树的直径
> 给定一棵二叉树，你需要计算它的直径长度。一棵二叉树的直径长度是任意两个结点路径长度中的最大值。这条路径可能穿过也可能不穿过根结点。

注意：两结点之间的路径长度是以它们之间**边的数目**表示。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/diameter-of-binary-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def diameterOfBinaryTree(self, root: TreeNode) -> int:
        # 看见最大值，联想到DFS

        # 这里不能初始化为0，假如测试用例的树为空，那直径就是-1了
        ans = 1

        def dfs(root):
            if not root:
                return 0
            left = dfs(root.left)
            right = dfs(root.right)
            # 我们需要求解的最大直径长度是左右子树分别最大值+自己
            nonlocal ans
            ans = max(ans, left + right + 1)
            return max(left, right) + 1  # 对于某个节点而言，他的高度等于他左右子树的最大高度+自己

        dfs(root)
        return ans - 1
```
### 547.省份数量
> 有` n `个城市，其中一些彼此相连，另一些没有相连。如果城市` a `与城市` b `直接相连，且城市` b `与城市` c `直接相连，那么城市` a `与城市` c `间接相连。  
**省份** 是一组直接或间接相连的城市，组内不含其他没有相连的城市。  
给你一个` n x n `的矩阵` isConnected `，其中` isConnected[i][j] = 1 `表示第` i `个城市和第` j `个城市直接相连，而` isConnected[i][j] = 0 `表示二者不直接相连。

返回矩阵中 **省份** 的数量

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/number-of-provinces  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 并查集
    ```python
    class UnionFind:
        def __init__(self): 
            self.father = {}
            self.num_set = 0

        def find(self, x):
            root = x
            while self.father[root] is not None:
                root = self.father[root]
            
            # 路径压缩
            while root != x:
                origin_father = self.father[x]
                self.father[x] = root
                x = origin_father
            
            return root
        
        def merge(self, x, y):
            root_x, root_y = self.find(x), self.find(y)
            if root_x != root_y:
                self.father[root_x] = root_y
                self.num_set -= 1

        def add(self, x):
            if x not in self.father:
                self.father[x] = None
                self.num_set += 1

    class Solution:
        def findCircleNum(self, isConnected: List[List[int]]) -> int:
            union = UnionFind()
            for i in range(len(isConnected)):
                union.add(i)
                for j in range(i):
                    if isConnected[i][j] == 1:
                        union.merge(i, j)
            return union.num_set
    ```
### 572.另一颗树的子树
> 给你两棵二叉树` root `和 `subRoot` 。检验 `root` 中是否包含和 `subRoot` 具有相同结构和节点值的子树。如果存在，返回 `true` ；否则，返回` false` 。

二叉树` tree `的一棵子树包括` tree `的某个节点和这个节点的所有后代节点。`tree` 也可以看做它自身的一棵子树。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/subtree-of-another-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def isSubtree(self, root: TreeNode, subRoot: TreeNode) -> bool:
        # 两棵树都为空
        if not root and not subRoot:
            return True
        if not root or not subRoot:
            return False
        
        return self.isSame(root, subRoot) or self.isSubtree(root.left, subRoot) or self.isSubtree(root.right, subRoot)
    
    def isSame(self, root, subRoot):
        # 两棵树都为空
        if not root and not subRoot:
            return True
        if not root or not subRoot:
            return False
        
        return root.val == subRoot.val and self.isSame(root.left, subRoot.left) and self.isSame(root.right, subRoot.right)
```
### 647.回文子串（与题5可做比较）
> 给你一个字符串` s `，请你统计并返回这个字符串中 **回文子串** 的数目。  
**回文字符串** 是正着读和倒过来读一样的字符串。  
**子字符串** 是字符串中的由连续字符组成的一个序列。  
具有不同开始位置或结束位置的子串，即使是由相同的字符组成，也会被视作不同的子串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/palindromic-substrings  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 法一：中心扩散
    ```python
    class Solution:
        def countSubstrings(self, s: str) -> int:
            ans = 0
            for i in range(len(s)):
                # 每个字母本身就是一个回文串，所以直接加1
                ans += 1
                left = right = i
                # 假入这种情况是abba, i=1时,其实这里就相当是中心是两个一样的值
                while right < len(s) - 1 and s[right] == s[right+1]:
                    ans += 1
                    right += 1
                # 如果确定这个回文串中心是两个值，再从两端扩散，否则中心就是一个值，再扩散
                while left > 0 and right < len(s) - 1 and s[left-1] == s[right+1]:
                    ans += 1
                    left -= 1
                    right += 1
            return ans
    ```
+ 法二：动态规划
    ```python
    class Solution:
        def countSubstrings(self, s: str) -> int:
            ans = 0
            n = len(s)
            # 构造n*n的状态转移矩阵
            # 想法是dp[left][right]=True代表着left到right是回文串，那么如果s[left-1]==s[right+1],那么dp[left-1][right+1]=True
            dp = [[False]*n for _ in range(n)]
            for j in range(n):
                for i in range(j+1):
                    # j - i < 2是因为我们的回文中心最初只会有一个字符或者两个字符
                    # 例如三个字符为中心的情况其实就是以一个字符为中心扩散的情况
                    # 当超过两个字符时，就开始利用状态转移方程了
                    # aba是回文了，如果两边又出现一样的字符c,那肯定就是回文咯，例如cabac
                    # 所以cabac（i=0,j=4）是不是回文取决于aba(i=1,j=3)，即（i+1，j-1）是不是回文
                    if s[i] == s[j] and (j - i < 2 or dp[i+1][j-1]):
                        dp[i][j] = True
                        ans += 1
            return ans
    ```
### 669.修剪二叉搜索树★
> 给你二叉搜索树的根节点` root `，同时给定最小边界`low `和最大边界 `high`。通过修剪二叉搜索树，使得所有节点的值在`[low, high]`中。修剪树 **不应该** 改变保留在树中的元素的相对结构 (即，如果没有被移除，原有的父代子代关系都应当保留)。 可以证明，存在 **唯一**的答案 。

所以结果应当返回修剪好的二叉搜索树的新的根节点。注意，根节点可能会根据给定的边界发生改变。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/trim-a-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def trimBST(self, root: Optional[TreeNode], low: int, high: int) -> Optional[TreeNode]:
        if not root:
            return None
        
        if root.val < low:
            root = self.trimBST(root.right, low, high)
        elif root.val > high:
            root = self.trimBST(root.left, low, high)
        else:
            root.left = self.trimBST(root.left, low, high)
            root.right = self.trimBST(root.right, low, high)
        return root
```
### 675.为高尔夫比赛砍树
> 你被请来给一个要举办高尔夫比赛的树林砍树。树林由一个` m x n `的矩阵表示， 在这个矩阵中：

+ `0 `表示障碍，无法触碰
+ `1 `表示地面，可以行走
+ 比` 1 `大的数 表示有树的单元格，可以行走，数值表示树的高度
每一步，你都可以向上、下、左、右四个方向之一移动一个单位，如果你站的地方有一棵树，那么你可以决定是否要砍倒它。

你需要按照树的高度从低向高砍掉所有的树，每砍过一颗树，该单元格的值变为` 1`（即变为地面）。

你将从` (0, 0) `点开始工作，返回你砍完所有树需要走的最小步数。 如果你无法砍完所有的树，返回` -1 `。

可以保证的是，没有两棵树的高度是相同的，并且你至少需要砍倒一棵树。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/cut-off-trees-for-golf-event  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ BFS
    ```python
    class Solution:
        def cutOffTree(self, forest: List[List[int]]) -> int:
        
            def bfs(sx, sy, ti, tj):
                queue = deque([(0, sx, sy)])
                m, n = len(forest), len(forest[0])  # 记录树林的长、宽
                visited = set()  # 标记已经访问过的节点
                visited.add((sx, sy))
                while queue:
                    step, x, y = queue.popleft()
                    if x == ti and y == tj:
                        return step
                    for nx, ny in [(x + 1, y), (x, y + 1), (x - 1, y), (x, y - 1)]:
                        # 越界了
                        if 0 <= nx < m and 0 <= ny < n and (nx, ny) not in visited and forest[nx][ny]:
                            visited.add((nx, ny))  # 添加到已经访问的节点
                            queue.append((step + 1, nx, ny))
                return -1
            
            trees = sorted((h, i, j) for i, row in enumerate(forest) for j, h in enumerate(row) if h > 1)
            ans = preI = preJ = 0
            for _, i, j in trees:
                d = bfs(preI, preJ, i, j)
                if d < 0:
                    return -1
                ans += d
                preI, preJ = i, j

            return ans
    ```
### 691.贴纸拼词
> 我们有` n `种不同的贴纸。每个贴纸上都有一个小写的英文单词。  
您想要拼写出给定的字符串` target `，方法是从收集的贴纸中切割单个字母并重新排列它们。如果你愿意，你可以多次使用每个贴纸，每个贴纸的数量是无限的。  
返回你需要拼出` target `的最小贴纸数量。如果任务不可能，则返回 `-1 `。

注意：在所有的测试用例中，所有的单词都是从` 1000 `个最常见的美国英语单词中随机选择的，并且` target `被选择为两个随机单词的连接。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/stickers-to-spell-word  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  

+ java记忆化搜索+状态压缩
    ```java
    class Solution {
        public int minStickers(String[] stickers, String target) {
            int m = target.length();
            //用数组保存状态的min，减少重复计算
            int[] memo = new int[1 << m];
            //设置状态初始值
            Arrays.fill(memo, -1);
            //递归终点，所有target字符都给撞完了
            memo[0] = 0;
            //开始递归调用
            int res = dfs(stickers, target, memo, (1 << m) - 1);
            //如果res 是m+则说明遇到了无法撞击完的情况 则返回-1
            return res <= m ? res : -1;
        }

        public int dfs(String[] stickers, String target, int[] memo, int mask) {
            int m = target.length();
            if (memo[mask] < 0) {
                //res初始值
                int res = m + 1;
                for (String sticker : stickers) {
                    int left = mask;
                    int[] cnt = new int[26];
                    //记录当前sticker的字符出现次数
                    for (int i = 0; i < sticker.length(); i++) {
                        cnt[sticker.charAt(i) - 'a']++;
                    }
                    // 匹配target
                    for (int i = 0; i < target.length(); i++) {
                        char c = target.charAt(i);
                        //如果还有这个位则 判断条件1成立
                        if (((mask >> i) & 1) == 1 && cnt[c - 'a'] > 0) {
                            //当前字符数量匹配成功，使用一次，总量减少
                            cnt[c - 'a']--;
                            //对应消耗了 target的哪一位。
                            left ^= 1 << i;
                        }
                    }
                    //如果没有发生撞击则直接下一个字符串
                    if (left < mask) {
                        //如果发生了撞击，则根据当前结果，递归撞击下去，只当为0。
                        //（其中如果递归以后遇到无法撞击的结果则会反回m+1。
                        res = Math.min(res, dfs(stickers, target, memo, left) + 1);
                    }
                }
                //记录当前长度最小消耗量
                memo[mask] = res;
            }
            //返回当前位置的最小值
            return memo[mask];
        }
    }
    ```
### 692.前K个高频单词
> 给定一个单词列表` words `和一个整数` k `，返回前` k `个出现次数最多的单词。  
返回的答案应该按单词出现频率由高到低排序。如果不同的单词有相同出现频率， 按**字典顺序** 排序。  

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/top-k-frequent-words  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Pair:
    def __init__(self, key: str, value: int):
        self.key = key
        self.value = value

    def __lt__(self, other):
        # 使用 < 符号时会调用此方法
        if self.value == other.value:
            # 当词频相同时，key值大的就小
            return self.key > other.key
        else:
            # 词频不同时，词频小的就小
            return self.value < other.value

class Solution:
    def topKFrequent(self, words: List[str], k: int) -> List[str]:
        count_dict = collections.Counter(words)
        count = 0
        ans = []
        for key, value in count_dict.items():
            pair = Pair(key, value)
            if count < k:
                heapq.heappush(ans,pair)
            else:
                heapq.heappushpop(ans,pair)
            count += 1
        ans.sort(reverse=True)
        return [i.key for i in ans]
```
### 698.划分为k个相等的子集
> 给定一个整数数组`  nums `和一个正整数` k`，找出是否有可能把这个数组分成` k `个非空子集，其总和都相等。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/partition-to-k-equal-sum-subsets/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java回溯
    ```java
    class Solution {
        // 备忘录，存储 used 的状态
        private HashMap<Integer, Boolean> memo = new HashMap<>();

        public boolean canPartitionKSubsets(int[] nums, int k) {
            int sum = 0;
            // 先求数组的总和，如果数组的总和不能平均分，那就说明不可能划分相等的子集
            for (int i = 0; i < nums.length; i++) sum += nums[i];
            if (sum % k != 0) return false;

            int target = sum / k;
            // 使用位图技巧
            int used = 0;
            int[] bucket = new int[k + 1];
            return backtrack(nums, 0, bucket, k, target, used);
        }

        private boolean backtrack(int[] nums, int start, int[] bucket, int k, int target, int used) {
            // k 个桶均装满
            if (k == 0) return true;

            // 当前桶装满了，开始装下一个桶
            if (bucket[k] == target) {
                // 注意：桶从下一个开始；球从第一个开始
                boolean res = backtrack(nums, 0, bucket, k - 1, target, used);
                memo.put(used, res);
                return res;
            }

            if (memo.containsKey(used))
                // 如果当前状态曾今计算过，就直接返回，不要再递归穷举了
                return memo.get(used);

            // 第 k 个桶开始对每一个球选择进行选择是否装入
            for (int i = start; i < nums.length; i++) {
                // 如果当前球已经被装入，则跳过
                if (((used >> i) & 1) == 1) continue;
                // 如果装入当前球，桶溢出，则跳过
                if (bucket[k] + nums[i] > target) continue;

                // 装入 && 标记已使用
                bucket[k] += nums[i];
                // 将第 i 位标记为 1
                used |= 1 << i;

                // 开始判断是否选择下一个球
                // 注意：桶依旧是当前桶；球是下一个球
                // 注意：是 i + 1
                if (backtrack(nums, i + 1, bucket, k, target, used)) return true;

                // 拿出 && 标记未使用
                bucket[k] -= nums[i];
                // 将第 i 位标记为 0
                used ^= 1 << i;
            }
            // 如果所有球均不能使所有桶刚好装满
            return false;
        }
    }
    ```
### 700.二叉搜索树中的搜索
> 给定二叉搜索树（BST）的根节点` root `和一个整数值` val`。  
你需要在` BST `中找到节点值等于` val `的节点。 返回以该节点为根的子树。 如果节点不存在，则返回 `null `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/search-in-a-binary-search-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def searchBST(self, root: TreeNode, val: int) -> TreeNode:
        if not root:
            return None
        if root.val < val:
            return self.searchBST(root.right, val)
        elif root.val > val:
            return self.searchBST(root.left, val)
        else:
            return root
```
### 713.乘积小于K的子数组
> 给你一个整数数组` nums `和一个整数` k `，请你返回子数组内所有元素的乘积严格小于` k `的连续子数组的数目。
 
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/subarray-product-less-than-k/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def numSubarrayProductLessThanK(self, nums: List[int], k: int) -> int:
        if k <= 1:
            return 0
        # 同向双指针指向开头位置
        left, right = 0, 0
        ans = 0
        mul = 1
        while right < len(nums):
            mul *= nums[right]
            while mul >= k:
                mul //= nums[left]
                left += 1
            ans += right - left + 1
            right += 1
        return ans
```
### 735.行星碰撞
> 给定一个整数数组` asteroids`，表示在同一行的行星。  
对于数组中的每一个元素，其绝对值表示行星的大小，正负表示行星的移动方向（正表示向右移动，负表示向左移动）。每一颗行星以相同的速度移动。  
找出碰撞后剩下的所有行星。碰撞规则：两个行星相互碰撞，较小的行星会爆炸。如果两颗行星大小相同，则两颗行星都会爆炸。两颗移动方向相同的行星，永远不会发生碰撞。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/asteroid-collision  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def asteroidCollision(self, asteroids: List[int]) -> List[int]:
        stack = []
        pre = curr = 1 # 记录前一位的符号，1代表正，0代表负
        for idx, num in enumerate(asteroids):
            if not stack:
                stack.append(num)
                pre = 1 if num > 0 else 0
                continue
            curr = 1 if num > 0 else 0
            if curr == pre or (pre == 0 and curr == 1 ):
                pre = curr
                stack.append(num)
            else:
                while True:
                    if curr == pre or (pre == 0 and curr == 1 ):
                        stack.append(num)
                        break
                    temp = stack.pop()
                    # 右边爆炸
                    if abs(temp) > abs(num):
                        stack.append(temp)
                        break
                    # 左边爆炸
                    elif abs(temp) < abs(num):
                        if stack:
                            pre = 1 if stack[-1] > 0 else 0
                        else:
                            stack.append(num)
                            pre = curr
                            break
                    # 一起爆炸
                    else:
                        if stack:
                            pre = 1 if stack[-1] > 0 else 0
                        break
        return stack
```

### 752.打开转盘锁★
> 你有一个带有四个圆形拨轮的转盘锁。每个拨轮都有`10`个数字： `'0', '1', '2', '3', '4', '5', '6', '7', '8', '9'` 。每个拨轮可以自由旋转：例如把 `'9' `变为` '0'`，`'0'` 变为 `'9'` 。每次旋转都只能旋转一个拨轮的一位数字。  
锁的初始数字为` '0000' `，一个代表四个拨轮的数字的字符串。  
列表` deadends `包含了一组死亡数字，一旦拨轮的数字和列表里的任何一个元素相同，这个锁将会被永久锁定，无法再被旋转。  
字符串` target `代表可以解锁的数字，你需要给出解锁需要的最小旋转次数，如果无论如何不能解锁，返回` -1 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/open-the-lock  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。


```python
class Solution:
    def openLock(self, deadends: List[str], target: str) -> int:
        # 最小旋转次数，可能就是最短路径，联想到BFS
        if target == "0000":
            return 0

        dead = set(deadends)
        if "0000" in dead:
            return -1
        
        def num_prev(x: str) -> str:
            return "9" if x == "0" else str(int(x) - 1)
        
        def num_succ(x: str) -> str:
            return "0" if x == "9" else str(int(x) + 1)
        
        # 枚举 status 通过一次旋转得到的数字
        def get(status: str) -> Generator[str, None, None]:
            s = list(status)
            for i in range(4):
                num = s[i]
                s[i] = num_prev(num)
                yield "".join(s)
                s[i] = num_succ(num)
                yield "".join(s)
                s[i] = num

        q = deque([("0000", 0)])
        seen = {"0000"}
        while q:
            status, step = q.popleft()
            for next_status in get(status):
                if next_status not in seen and next_status not in dead:
                    if next_status == target:
                        return step + 1
                    q.append((next_status, step + 1))
                    seen.add(next_status)
        
        return -1
```
### 767.重构字符串
> 给定一个字符串`S`，检查是否能重新排布其中的字母，使得两相邻的字符不同。  
若可行，输出任意可行的结果。若不可行，返回空字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/reorganize-string/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def reorganizeString(self, s: str) -> str:
        length = len(s)
        if length < 2:
            return s
        count_dict = collections.Counter(s)
        # 找到出现频率最大的那个
        max_count = max(count_dict.items(),key=lambda x: x[1])[1]
        if max_count > (length + 1) // 2:
            return ""
        max_heap= [(-x[1],x[0]) for x in count_dict.items()]
        heapq.heapify(max_heap)
        ans = []

        while len(max_heap) > 1: # 一次拿两个
            _, first = heapq.heappop(max_heap)
            _, second = heapq.heappop(max_heap)
            ans += [first,second]
            # 将两个字母对应的数量减掉一次
            count_dict[first] -= 1
            count_dict[second] -= 1
            # 如果该字母还有，那么继续进入大顶堆
            if count_dict[first] > 0:
                heapq.heappush(max_heap, (-count_dict[first], first))
            if count_dict[second] > 0:
                heapq.heappush(max_heap, (-count_dict[second], second))
        # 可能还剩下一个
        if max_heap:
            ans.append(heapq.heappop(max_heap)[1])
        return "".join(ans)
```
### 812.最大三角形面积
> 给定包含多个点的集合，从其中取三个点组成三角形，返回能组成的最大三角形的面积。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/largest-triangle-area/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def largestTriangleArea(self, points):
        """
        :type points: List[List[int]]
        :rtype: float
        """
        res = 0
        N = len(points)
        for i in range(N - 2):
            for j in range(i + 1, N - 1):
                for k in range(i + 2, N):
                    (x1, y1), (x2, y2), (x3, y3) = points[i], points[j], points[k]
                    res = max(res, 0.5 * abs(x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2)))
        return res
```
### 815.公交路线★
> 给你一个数组` routes `，表示一系列公交线路，其中每个` routes[i] `表示一条公交线路，第` i `辆公交车将会在上面循环行驶。  
例如，路线` routes[0] = [1, 5, 7] `表示第` 0 `辆公交车会一直按序列` 1 -> 5 -> 7 -> 1 -> 5 -> 7 -> 1 -> ... `这样的车站路线行驶。  
现在从` source `车站出发（初始时不在公交车上），要前往` target `车站。 期间仅可乘坐公交车。  
求出 **最少乘坐的公交车数量** 。如果不可能到达终点车站，返回` -1 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/bus-routes  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def numBusesToDestination(self, routes: List[List[int]], source: int, target: int) -> int:
        # 看见最少乘坐公交车数量，可以推断出这又是一道基于BFS的题目
        # 把每一条公交路线看成一个点，因为我们只需要考虑换多少班公交车，不考虑每班公交车上我们坐了多少站
        # 针对每一个车站，我们需要记录这个车站可以到哪些路线
        # 如果公交路线上有相同的站，就对这两个点（公交路线）连边
        def bfs() -> int:
            dict_to = defaultdict(set)  # 记录每个车站可以进入的路线
            queue = Deque()  # 队列存的是经过的路线

            # 哈希表记录的进入该路线所使用的距离
            # 起始时将「起点车站」所能进入的「路线」进行入队，每次从队列中取出「路线」时，
            # 查看该路线是否包含「终点车站」：包含「终点车站」：返回进入该线路所花费的距离
            # 不包含「终点车站」：遍历该路线所包含的车站，将由这些车站所能进入的路线，进行入队
            # 由于是求最短路，同一路线重复入队是没有意义的，因此将新路线入队前需要先判断是否曾经入队。

            step_num = defaultdict(int)  # 存储进入某条路线所需要花费的步数

            for i in range(len(routes)):
                for station in routes[i]:
                    #将从起点可以进入的路线加入队列
                    if station == source:
                        queue.append(i)
                        step_num[i] = 1  # 到达i这条路线的步数
                    
                    # 更新当前车站可以到达的路线
                    dict_to[station].add(i)

            while queue:
                # 取出当前所在的路线，与进入该路线所花费的距离
                node = queue.popleft()
                step = step_num[node]
                # 遍历该路线所包含的车站
                for station in routes[node]:
                    # 查看该路线是否包含「终点车站」：包含「终点车站」：返回进入该线路所花费的距离
                    if station == target: 
                        return step
                    lines = dict_to[station]
                    # 将由该线路的车站发起的路线，加入队列
                    if lines == None:
                        continue
                    for line in lines:
                        # 对于当前车站可选择的每一条路线而言
                        if line not in step_num:
                            step_num[line] = step + 1
                            queue.append(line)
            return -1

        if source == target: 
            return 0
        return bfs()
```
### 856.括号的分数
> 给定一个平衡括号字符串` S`，按下述规则计算该字符串的分数：

+ `()` 得 `1` 分。
+ `AB` 得 `A + B` 分，其中` A `和 `B `是平衡括号字符串。
+ `(A)` 得 `2 * A` 分，其中` A `是平衡括号字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/score-of-parentheses  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def scoreOfParentheses(self, s: str) -> int:
        stack = [0]
        for x in s:
            if x == '(':
                stack.append(0)
            else:
                value = stack.pop()
                stack[-1] += max(2 * value, 1)

        return stack.pop()
```
### 863.二叉树中所有距离为 K 的结点
> 给定一个二叉树（具有根结点` root`）， 一个目标结点` target` ，和一个整数值 `k `。

返回到目标结点` target` 距离为` k `的所有结点的值的列表。 答案可以以 **任何顺序** 返回。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/all-nodes-distance-k-in-binary-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def distanceK(self, root: TreeNode, target: TreeNode, k: int) -> List[int]:
        # 记录每个节点的父节点
        parent = {}
        # 记录答案
        ans = []

        # 寻找每个节点的父亲节点
        def record_parent(root):
            if root.left:
                parent[root.left.val] = root
                record_parent(root.left)
            if root.right:
                parent[root.right.val] = root
                record_parent(root.right)
        
        # 从target开始，找距离为k的节点,node_from代表当前循环的node是从哪里进来的
        def find_dist_k(node, step, k, node_from):
            # 树为空
            if not node:
                return None
            if step == k:
                # 找到了,不需要再找node节点的后面那些点了
                ans.append(node.val)
                return None
            if node.left != node_from:
                find_dist_k(node.left, step + 1, k, node)
            if node.right != node_from:
                find_dist_k(node.right, step + 1, k, node)
            # 不要使用parent[node.val]，因为在创建字典的时候root节点是没有父节点的，使用get才会返回None
            # 虽然root没有父节点，但是他有子节点，所以当然可以跨左右子树循环咯
            if parent.get(node.val) != node_from:
                find_dist_k(parent.get(node.val), step + 1, k, node)
        
        record_parent(root)
        find_dist_k(target, 0, k, None)
        return ans
```
### 876.链表的中间结点
> 给定一个头结点为` head `的非空单链表，返回链表的中间结点。  
如果有两个中间结点，则返回第二个中间结点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/middle-of-the-linked-list/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 快慢指针
    ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def middleNode(self, head: ListNode) -> ListNode:
            slow, fast = head, head
            while fast and fast.next:
                slow = slow.next
                fast = fast.next.next
            return slow
    ```

### 895.最大频率栈
> 设计一个类似堆栈的数据结构，将元素推入堆栈，并从堆栈中弹出出现频率最高的元素。

实现` FreqStack `类:

+ `FreqStack()` 构造一个空的堆栈。
+ `void push(int val)` 将一个整数 val 压入栈顶。
+ `int pop()` 删除并返回堆栈中出现频率最高的元素。
如果出现频率最高的元素不只一个，则移除并返回最接近栈顶的元素。
 
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/maximum-frequency-stack  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class FreqStack:

    def __init__(self):
        self.freq = collections.defaultdict(lambda: 0)
        self.freq_stack = collections.defaultdict(list)
        self.max_freq = 0
        
    def push(self, x: int) -> None:
        self.freq[x] += 1
        if self.freq[x] > self.max_freq:
            self.max_freq = self.freq[x]
        self.freq_stack[self.freq[x]].append(x)    
        
    def pop(self) -> int:
        ans = self.freq_stack[self.max_freq].pop()
        self.freq[ans] -= 1
        if not self.freq_stack[self.max_freq]:
            self.max_freq -= 1
        return ans



# Your FreqStack object will be instantiated and called as such:
# obj = FreqStack()
# obj.push(val)
# param_2 = obj.pop()
```
### 905.按奇偶排序数组
> 给你一个整数数组` nums`，将` nums `中的的所有偶数元素移动到数组的前面，后跟所有奇数元素。  
返回满足此条件的 **任一数组** 作为答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sort-array-by-parity/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def sortArrayByParity(self, nums: List[int]) -> List[int]:
        if len(nums) == 1:
            return nums
        n = len(nums)
        left, right = 0, n - 1
        while left < right:
            # 找到第一个奇数
            while left < n and nums[left] % 2 == 0:
                left += 1
            # 找到第一个偶数
            while right >= 0 and nums[right] % 2 == 1:
                right -= 1
            if left < right:
                nums[left], nums[right] = nums[right], nums[left]
                left += 1
                right -= 1
        
        return nums
```
### 933.最近的请求次数
> 写一个` RecentCounter `类来计算特定时间范围内最近的请求。

请你实现` RecentCounter `类：

+ `RecentCounter() `初始化计数器，请求数为` 0 `。
+ `int ping(int t)` 在时间` t `添加一个新请求，其中` t `表示以毫秒为单位的某个时间，并返回过去` 3000 `毫秒内发生的所有请求数（包括新请求）。确切地说，返回在` [t-3000, t] `内发生的请求数。

保证 每次对` ping `的调用都使用比之前更大的` t `值。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/number-of-recent-calls  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java队列
    ```java
    class RecentCounter {
        //定义队列
        public Queue<Integer> queue;

        public RecentCounter() {
            Queue<Integer> queue = new ArrayDeque<Integer>();
            this.queue = queue;
        }
        
        public int ping(int t) {
            //新的请求入队列
            queue.offer(t);
            while(queue.peek() < t - 3000)
                queue.poll();
            return queue.size();
        }
    }

    /**
    * Your RecentCounter object will be instantiated and called as such:
    * RecentCounter obj = new RecentCounter();
    * int param_1 = obj.ping(t);
    */
    ```
### 942.增减字符串匹配
> 由范围` [0,n] `内所有整数组成的` n + 1 `个整数的排列序列可以表示为长度为` n `的字符串` s `，其中:
+ 如果` perm[i] < perm[i + 1] `，那么` s[i] == 'I' `
+ 如果` perm[i] > perm[i + 1] `，那么` s[i] == 'D' `

给定一个字符串` s `，重构排列` perm `并返回它。如果有多个有效排列`perm`，则返回其中 **任何一个** 。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/di-string-match  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java贪心构造
    ```java
    class Solution {
        public int[] diStringMatch(String s) {
            int n = s.length();
            int left = 0, right = n;
            // 记录答案
            int[] ans = new int[n + 1];
            int idx = 0;
            for(int i = 0; i < n; i++)
                ans[idx++] = s.charAt(i) == 'I' ? left++ : right--;
            
            //处理最后一位
            ans[idx] = left;
            return ans;
        }
    }
    ```
### 944.删列造序
> 给你由` n `个小写字母字符串组成的数组` strs`，其中每个字符串长度相等。  
这些字符串可以每个一行，排成一个网格。例如，`strs = ["abc", "bce", "cae"] `可以排列为：
```
abc
bce
cae
```
你需要找出并删除 不是**按字典序升序排列的** 列。在上面的例子（下标从` 0 `开始）中，列` 0（'a', 'b', 'c'）`和列` 2（'c', 'e', 'e'）`都是按升序排列的，而列` 1（'b', 'c', 'a'）`不是，所以要删除列` 1 `。

返回你需要删除的列数。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/delete-columns-to-make-sorted  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java模拟
    ```java
    class Solution {
        public int minDeletionSize(String[] strs) {
            int n = strs.length, m = strs[0].length(), ans = 0;
            out:for (int i = 0; i < m; i++) {
                for (int j = 0, cur = -1; j < n; j++) {
                    int t = (int) strs[j].charAt(i);
                    if (t < cur && ++ans >= 0) continue out;
                    cur = t;
                }
            }
            return ans;
        }
    }
    ```
### 951.翻转等价二叉树
> 我们可以为二叉树` T `定义一个 **翻转操作** ，如下所示：选择任意节点，然后交换它的左子树和右子树。  
只要经过一定次数的翻转操作后，能使` X `等于` Y`，我们就称二叉树` X `翻转 **等价** 于二叉树` Y`。

这些树由根节点` root1 `和` root2 `给出。如果两个二叉树是否是翻转 **等价** 的函数，则返回 `true `，否则返回 `false` 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/flip-equivalent-binary-trees  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def flipEquiv(self, root1: Optional[TreeNode], root2: Optional[TreeNode]) -> bool:
        if not root1 and not root2:
            return True
        if not root1 or not root2:
            return False
 
        # 等价的条件是根节点的val相等，然后要么两个根节点的左右子树分别对应相等(左=左，右=右)，要么两个根节点的左右子树相反相等(左=右，右=左)
        return root1.val == root2.val and ((self.flipEquiv(root1.left, root2.right) and self.flipEquiv(root1.right, root2.left)) or (self.flipEquiv(root1.left, root2.left) and self.flipEquiv(root1.right, root2.right)))
```
### 953.验证外星语词典
> 某种外星语也使用英文小写字母，但可能顺序` order `不同。字母表的顺序`（order）`是一些小写字母的排列。  
给定一组用外星语书写的单词` words`，以及其字母表的顺序` order`，只有当给定的单词在这种外星语中按字典序排列时，返回` true`；否则，返回 `false`。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/verifying-an-alien-dictionary  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def isAlienSorted(self, words: List[str], order: str) -> bool:
        mapping = dict()
        for i,v in enumerate(order):
            mapping[v] = i
        decrypt = []
        for word in words:
            tmp = "".join([chr(ord('a')+(mapping[x])) for x in word])
            decrypt.append(tmp)
        return sorted(decrypt) == decrypt
```
### 961.在长度2N的数组中找出重复N次的元素
> 给你一个整数数组 nums ，该数组具有以下属性：
+ `nums.length == 2 * n`.
+ `nums` 包含` n + 1 `个 **不同的** 元素
+ `nums` 中恰有一个元素重复` n `次

找出并返回重复了` n `次的那个元素。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/n-repeated-element-in-size-2n-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java
```java
class Solution {
    public int repeatedNTimes(int[] nums) {
        Arrays.sort(nums);
        int len = nums.length;
        return nums[len/2 + 1] == nums[len/2] ? nums[len/2] : nums[len/2 - 1];
    }
}
```
### 965.单值二叉树
> 如果二叉树每个节点都具有相同的值，那么该二叉树就是单值二叉树。  
只有给定的树是单值二叉树时，才返回` true`；否则返回` false`。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/univalued-binary-tree/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def isUnivalTree(self, root: TreeNode) -> bool:
        if not root:
            return True
        
        if root.left:
            if root.val != root.left.val or not self.isUnivalTree(root.left):
                return False
        
        if root.right:
            if root.val != root.right.val or not self.isUnivalTree(root.right):
                return False
        
        return True
```

### 973.最接近原点的K个点
> 给定一个数组` points `，其中` points[i] = [xi, yi] `表示` X-Y `平面上的一个点，并且是一个整数` k `，返回离原点` (0,0) `最近的` k `个点。  
这里，平面上两点之间的距离是 `欧几里德距离（ √(x1 - x2)2 + (y1 - y2)2 ）`。  
你可以按 **任何顺序** 返回答案。除了点坐标的顺序之外，答案 **确保** 是 **唯一** 的。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/k-closest-points-to-origin  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 小顶堆(这样做不省空间，相当是所有的点都放进去算了之后选了前K个顶点)
    ```python
    import heapq

    class Solution:
        def kClosest(self, points: List[List[int]], k: int) -> List[List[int]]:
            # 使用小顶堆来取得值
            distance_dict = collections.defaultdict(list)
            max_heap = []
            result = []
            for point in points:
                distance = math.sqrt(point[0]**2 + point[1]**2)
                # 构造小顶堆
                heapq.heappush(max_heap,distance)
                distance_dict[distance].append(point)
            
            for _ in range(k):
                temp = heapq.heappop(max_heap)
                result.append(distance_dict[temp].pop())
            return result
    ```
+ 大顶堆(省空间，构造K个节点的大顶堆，对剩余的n-k个点分别与堆顶点比，只要其余值小，就弹出堆顶点，把这个值插进去，最后大顶堆里面的k个元素就是所需的)
    ```python
    class Solution:
        def kClosest(self, points: List[List[int]], k: int) -> List[List[int]]:
            q = [(-x ** 2 - y ** 2, i) for i, (x, y) in enumerate(points[:k])]
            heapq.heapify(q)
            
            n = len(points)
            for i in range(k, n):
                x, y = points[i]
                dist = -x ** 2 - y ** 2
                heapq.heappushpop(q, (dist, i))
            
            ans = [points[identity] for (_, identity) in q]
            return ans
    ```
### 987.二叉树的垂序遍历
> 给你二叉树的根结点 `root` ，请你设计算法计算二叉树的 **垂序遍历** 序列。 
对位于 `(row, col)` 的每个结点而言，其左右子结点分别位于` (row + 1, col - 1) `和 `(row + 1, col + 1)` 。树的根结点位于` (0, 0)` 。

二叉树的 **垂序遍历** 从最左边的列开始直到最右边的列结束，按列索引每一列上的所有结点，形成一个按出现位置从上到下排序的有序列表。如果同行同列上有多个结点，则按结点的值从小到大进行排序。

返回二叉树的 **垂序遍历** 序列。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/vertical-order-traversal-of-a-binary-tree  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS + 最小堆
```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def verticalTraversal(self, root: TreeNode) -> List[List[int]]:
        # 记录每个节点的行号和列号
        # 首先按照列号从小到大排，同一列不同行的按照行号从小到大排，同一行同一列的按照值进行从小到大排
        min_heap = []

        def dfs(root, row, col):
            if not root:
                return None
            dfs(root.left, row + 1, col - 1)
            dfs(root.right, row + 1, col + 1)
            # 构造小顶堆
            heapq.heappush(min_heap, (col, row, root.val))
        
        dfs(root, 0, 0)

        ans = []
        col_change = float('-inf')
        
        while min_heap:
            col, row, value = heapq.heappop(min_heap)
            # 列号改变了，说明需要重新分组
            if col != col_change:
                ans.append([])
                col_change = col
            ans[-1].append(value)

        return ans
```
### 1004.最大连续1的个数 III
> 给定一个二进制数组` nums `和一个整数` k `，如果可以翻转最多`k `个` 0` ，则返回 **数组中连续` 1 `的最大个数** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/max-consecutive-ones-iii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def longestOnes(self, nums: List[int], k: int) -> int:
        # 同向双指针
        slow, fast = 0, 0
        num_freq = defaultdict(int)
        longest =0
        while fast < len(nums):
            num_freq[nums[fast]] += 1
            while num_freq[0] > k:
                num_freq[nums[slow]] -= 1
                slow += 1
            longest = max(longest, fast - slow + 1)
            fast += 1
        return longest
```
### 1021.删除最外层的括号
> 有效括号字符串为空` ""、"(" + A + ")" `或` A + B `，其中` A `和` B `都是有效的括号字符串，`+ `代表字符串的连接。  
例如，`""，"()"，"(())()"` 和` "(()(()))" `都是有效的括号字符串。  
如果有效字符串 s 非空，且不存在将其拆分为` s = A + B `的方法，我们称其为**原语**（primitive），其中` A `和` B `都是非空有效括号字符串。  
给出一个非空有效字符串` s`，考虑将其进行原语化分解，使得：`s = P_1 + P_2 + ... + P_k`，其中` P_i `是有效括号字符串原语。  
对` s `进行原语化分解，删除分解中每个原语字符串的最外层括号，返回` s `。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/remove-outermost-parentheses  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 栈模拟
```java
class Solution {
    public String removeOuterParentheses(String s) {
        StringBuffer ans = new StringBuffer();
        Deque<Character> stack = new ArrayDeque<Character>();
        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            if (c == ')')
                stack.pop();
            if (!stack.isEmpty())
                ans.append(c);
            if (c == '(')
                stack.push(c);
        }
        return ans.toString();
    }
}
```
### 1022.从根到叶的二进制数之和
> 给出一棵二叉树，其上每个结点的值都是 0 或 1 。每一条从根到叶的路径都代表一个从最高有效位开始的二进制数。  
例如，如果路径为 0 -> 1 -> 1 -> 0 -> 1，那么它表示二进制数 01101，也就是 13 。  
对树上的每一片叶子，我们都要找出从根到该叶子的路径所表示的数字。  
返回这些数字之和。题目数据保证答案是一个 32 位 整数。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/sum-of-root-to-leaf-binary-numbers  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public int sumRootToLeaf(TreeNode root) {
        return dfs(root, 0);
    }

    public int dfs(TreeNode root, int val) {
        if (root == null) {
            return 0;
        }
        val = (val << 1) | root.val;
        if (root.left == null && root.right == null) {
            return val;
        }
        return dfs(root.left, val) + dfs(root.right, val);
    }
}
```
### 1091.二进制矩阵中的最短路径
> 给你一个` n x n `的二进制矩阵` grid `中，返回矩阵中**最短 畅通路径** 的长度。如果不存在这样的路径，返回` -1 `。  

二进制矩阵中的 **畅通路径** 是一条从 **左上角** 单元格（即，`(0, 0)`）到 **右下角** 单元格（即，`(n - 1, n - 1)`）的路径，该路径同时满足下述要求：  
+ 路径途经的所有单元格都的值都是` 0 `。
+ 路径中所有相邻的单元格应当在` 8 `个方向之一 上连通（即，相邻两单元之间彼此不同且共享一条边或者一个角）。  

**畅通路径的长度** 是该路径途经的单元格总数。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/shortest-path-in-binary-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def shortestPathBinaryMatrix(self, grid: List[List[int]]) -> int:
        # 看到最短畅通路径，就知道是BFS
        if grid[0][0] != 0 or grid[len(grid)-1][len(grid)-1] != 0:
            return -1
        if len(grid) == 1:
            return 1
        steps = defaultdict(int)
        queue = deque([((0, 0), 1)])
        steps[(0, 0)] = 1

        while queue:
            (i, j), step = queue.popleft()
            for x, y in [(1, 1), (0, 1), (1, 0), (1, -1), (0, -1), (-1, 1), (-1, 0), (-1, -1)]:
                new_x = i + x
                new_y = j + y
                if 0 <= new_x < len(grid) and 0 <= new_y < len(grid) and grid[new_x][new_y] != 1:
                    # 当前格子没有来过
                    if (new_x, new_y) not in steps:
                        # 到达右下角格子了
                        if new_x == len(grid) - 1 and new_y  == len(grid) - 1:
                            return step + 1
                        steps[(new_x, new_y)] = step + 1
                        queue.append(((new_x, new_y), steps[(new_x, new_y)]))
        
        return -1
```
### 1095.山脉数组中查找目标值
> （这是一个 交互式问题 ）  
给你一个 **山脉数组**` mountainArr`，请你返回能够使得` mountainArr.get(index)` 等于` target `**最小** 的下标 `index` 值。  
如果不存在这样的下标` index`，就请返回` -1`。

何为山脉数组？如果数组` A `是一个山脉数组的话，那它满足如下条件：  
1. 首先，`A.length >= 3 ` 
2. 其次，在` 0 < i < A.length - 1 `条件下，存在` i `使得：  
    + A[0] < A[1] < ... A[i-1] < A[i]
    + A[i] > A[i+1] > ... > A[A.length - 1]
 

你将 **不能**直接访问该山脉数组，必须通过 `MountainArray `接口来获取数据：  
+ `MountainArray.get(k)` - 会返回数组中索引为`k `的元素（下标从` 0 `开始）
+ `MountainArray.length()` - 会返回该数组的长度
 

注意：  
对` MountainArray.get` 发起超过` 100 `次调用的提交将被视为错误答案。此外，任何试图规避判题系统的解决方案都将会导致比赛资格被取消。  
为了帮助大家更好地理解交互式问题，我们准备了一个样例 [“答案”](https://leetcode-cn.com/playground/RKhe3ave)，请注意这 **不是**一个正确答案

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-in-mountain-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# """
# This is MountainArray's API interface.
# You should not implement it, or speculate about its implementation
# """
#class MountainArray:
#    def get(self, index: int) -> int:
#    def length(self) -> int:

class Solution:
    def findInMountainArray(self, target: int, mountain_arr: 'MountainArray') -> int:
        def binary_search(mountain, target, l, r, key=lambda x: x):
            target = key(target)
            while l <= r:
                mid = (l + r) // 2
                cur = key(mountain.get(mid))
                if cur == target:
                    return mid
                elif cur < target:
                    l = mid + 1
                else:
                    r = mid - 1
            return -1
 
        left, right = 0, mountain_arr.length() - 1
        # 寻找峰值
        while left < right:
            mid = (left + right) // 2
            if mountain_arr.get(mid) < mountain_arr.get(mid + 1): # 说明峰值在mid+1到right之间
                left = mid + 1
            else:
                right = mid  # 说明峰值在left到mid之间
        peak = left
        # 搜索左半部分
        index = binary_search(mountain_arr, target, 0, peak)
        if index != -1:
            return index
        # 左半部分没有，那就搜索右半部分，key函数相当于继续使用从小到大的排列
        index = binary_search(mountain_arr, target, peak + 1, mountain_arr.length() - 1, lambda x: -x)
        return index
```
### 1110.删点成林★
> 给出二叉树的根节点` root`，树上每个节点都有一个不同的值。  
如果节点值在` to_delete `中出现，我们就把该节点从树上删去，最后得到一个森林（一些不相交的树构成的集合）。  
返回森林中的每棵树。你可以按任意顺序组织答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/delete-nodes-and-return-forest  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def delNodes(self, root: TreeNode, to_delete: List[int]) -> List[TreeNode]:
        # 把list转成set，速度更快
        to_delete_set = set(to_delete)
        ans = []

        def dfs(root, is_root):
            # 树为空
            if not root:
                return None
            # 如果节点的值在删除集里面，那么这个节点就需要删除
            root_deleted = root.val in to_delete_set
            if is_root and not root_deleted:
                ans.append(root)
            root.left = dfs(root.left, root_deleted)
            root.right = dfs(root.right, root_deleted)
            return None if root_deleted else root
            
        dfs(root, True)
        return ans
```
### 1209.删除字符串中的所有相邻重复项 II
> 给你一个字符串` s`，「k 倍重复项删除操作」将会从` s `中选择` k `个相邻且相等的字母，并删除它们，使被删去的字符串的左侧和右侧连在一起。  
你需要对` s `重复进行无限次这样的删除操作，直到无法继续为止。  
在执行完所有删除操作后，返回最终得到的字符串。  
本题答案保证唯一。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/remove-all-adjacent-duplicates-in-string-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def removeDuplicates(self, s: str, k: int) -> str:
        if len(s) < k:
            return s
        stack = []
        pre = curr = 0
        count = 0
        for char in s:
            stack.append(char)
            curr = len(stack) - 1
            if len(stack) == 1 or stack[curr] != stack[pre]:
                pre = curr
                count = 1
            else:
                count += 1
            if count == k:
                while count > 0:
                    stack.pop()
                    count -= 1
                # 重新找pre的位置
                if len(stack) > 1:
                    count = 1
                    for idx in range(pre-1,0,-1):
                        if stack[idx] != stack[idx-1]:
                            pre = idx
                            break
                        count += 1
                else:
                    count = 1
                    pre = 0
        return ''.join(stack)
```
### 1235.规划兼职工作
> 你打算利用空闲时间来做兼职工作赚些零花钱。  
这里有` n `份兼职工作，每份工作预计从` startTime[i] `开始到` endTime[i] `结束，报酬为` profit[i]`。  
给你一份兼职工作表，包含开始时间` startTime`，结束时间` endTime `和预计报酬 `profit `三个数组，请你计算并返回可以获得的最大报酬。

注意，时间上出现重叠的` 2 `份工作不能同时进行。  
如果你选择的工作在时间` X `结束，那么你可以立刻进行在时间` X `开始的下一份工作。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/maximum-profit-in-job-scheduling  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python 记忆化搜索
    ```python
    class Solution:
        def jobScheduling(self, startTime, endTime, profit):
            # 工作数量
            size = len(startTime)
            # 将每种工作的的开始，结束，收益放置在一起，并以开始时间排序
            sep = [[startTime[i], endTime[i], profit[i]] for i in range(size)]
            sep.sort(key=lambda x: x[0])

            memory = dict()

            def findjob(index, pre_chose_end):
                if index == size:
                    return 0
                if pre_chose_end in memory:
                    return memory[pre_chose_end]
                curprofit = 0
                # 二分搜索优化，找到下一个可以开始的工作
                left = index
                right = size - 1
                while left < right:
                    mid = (left + right) // 2
                    if sep[mid][0] < pre_chose_end:
                        left = mid + 1
                    else:
                        right = mid

                for i in range(left, size):
                    if sep[i][0] > sep[left][1]:
                        break
                    if sep[i][0] >= pre_chose_end:
                        curprofit = max(sep[i][2] + findjob(index + 1, sep[i][1]), curprofit)

                memory[pre_chose_end] = curprofit
                return curprofit

            return findjob(0, 0)
    ```
### 1249.移除无效的括号
> 给你一个由` '('、')' `和小写字母组成的字符串` s`。  
你需要从字符串中删除最少数目的` '(' `或者` ')' `（可以删除任意位置的括号)，使得剩下的「括号字符串」有效。  
请返回任意一个合法字符串。  

有效「括号字符串」应当符合以下` 任意一条 `要求：  
+ 空字符串或只包含小写字母的字符串
+ 可以被写作` AB`（A 连接 B）的字符串，其中` A `和` B `都是有效「括号字符串」
+ 可以被写作` (A) `的字符串，其中` A `是一个有效的「括号字符串」

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/minimum-remove-to-make-valid-parentheses  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def minRemoveToMakeValid(self, s: str) -> str:
        stack = [] # 存放s
        left_stack = [] # 存放遇到的左括号索引
        right_index = [] # 存放没配对的右括号索引
        for idx, char in enumerate(s):
            # 遇到的都存进去，后面记录位置删去
            stack.append(char)
            # 遇到左括号，记录位置
            if char == '(':
                left_stack.append(idx)
            # 遇到右括号，开始匹配
            elif char == ')':
                if left_stack:
                    left_stack.pop()  # 匹配成功一对
                else:
                    right_index.append(idx)  # 没匹配成功，记录位置后面删除
        # 汇总需要删除的位置
        right_index += left_stack
        for idx in right_index:
            stack[idx] = ''
        return ''.join(stack)
```
### 1293.网格中的最短路径
> 给你一个` m * n `的网格，其中每个单元格不是` 0`（空）就是` 1`（障碍物）。每一步，您都可以在空白单元格中上、下、左、右移动。  
如果您 最多 可以消除` k `个障碍物，请找出从左上角` (0, 0) `到右下角` (m-1, n-1) `的最短路径，并返回通过该路径所需的步数。如果找不到这样的路径，则返回` -1 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/shortest-path-in-a-grid-with-obstacles-elimination  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def shortestPath(self, grid: List[List[int]], k: int) -> int:
        m, n = len(grid), len(grid[0])
        if m == 1 and n == 1:
            return 0
        
        k = min(k, m + n - 3)

        # （（坐标），剩余破墙次数）
        begin = ((0, 0), k)
        visited = set([begin])
        queue = deque([begin])
        step = 0
        while queue:
            step += 1
            for _ in range(len(queue)):
                (i, j), chance = queue.popleft()
                for x, y in [(i-1, j), (i+1, j), (i, j-1), (i, j+1)]:
                    if 0 <= x < m and 0 <= y < n:
                        if grid[x][y] == 0 and ((x, y), chance) not in visited:
                            if  x == m - 1 and y == n - 1:
                                return step
                            visited.add(((x, y), chance))
                            queue.append(((x, y), chance))
                        elif grid[x][y] == 1 and chance > 0 and ((x, y), chance-1) not in visited:
                            visited.add(((x, y), chance-1))
                            queue.append(((x, y), chance-1))
        return -1
```
### 1300.转变数组后最接近目标值的数组和
> 给你一个整数数组` arr `和一个目标值` target `，请你返回一个整数` value `，使得将数组中所有大于` value `的值变成` value `后，数组的和最接近`  target `（最接近表示两者之差的绝对值最小）。  
如果有多种使得和最接近 target 的方案，请你返回这些整数中的最小值。  
请注意，答案不一定是 arr 中的数字

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sum-of-mutated-array-closest-to-target  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class Solution:
    def findBestValue(self, arr: List[int], target: int) -> int:
        # 前缀和、二分查找
        arr.sort()
        n = len(arr)
        # 计算前缀和
        prefix = [0]
        for num in arr:
            prefix.append(prefix[-1] + num)

        # value的下界是0，因为如果value<0了，sum只会越来越小，sum与target绝对差值变大
        # value的上界是arr数组的最大值，即原版arr全部加起来sum最大，高于这个值的value不会引起arr变化了
        left, right, ans = 0, arr[-1], -1
        while left <= right:
            mid = left + (right - left) // 2   # 相当于搜索一个[0,arr[-1]]递增的数组
            # 检索替换位置
            it = bisect_left(arr, mid)
            # 大于mid的值替换后的前缀和
            curr = prefix[it] + (n - it) * mid
            if curr <= target:
                ans = mid
                left = mid + 1
            else:
                right = mid - 1
        
        small = sum(ans if num >= ans else num for num in arr)
        big = sum(ans + 1 if num >= ans + 1 else num for num in arr)
        return ans if abs(small - target) <= abs(big - target) else ans + 1
```
### 1305.两棵二叉搜索树中的所有元素
> 给你` root1 `和` root2 `这两棵二叉搜索树。请你返回一个列表，其中包含 **两棵树** 中的所有整数并按 **升序** 排序。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/all-elements-in-two-binary-search-trees/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
+ 中序遍历+归并
    ```python
    # Definition for a binary tree node.
    # class TreeNode:
    #     def __init__(self, val=0, left=None, right=None):
    #         self.val = val
    #         self.left = left
    #         self.right = right
    class Solution:
        def getAllElements(self, root1: TreeNode, root2: TreeNode) -> List[int]:
            # 二叉搜索树的中序遍历就是升序，两个数组在归并即可
            if not root1 and not root2:
                return []

            def in_order(tmp, root):
                if root:
                    in_order(tmp, root.left)
                    tmp.append(root.val)
                    in_order(tmp, root.right)

            
            # 两棵树的升序集合
            root1_list, root2_list = [], []
            in_order(root1_list, root1)
            in_order(root2_list, root2)

            if not root1_list:
                return root2_list

            if not root2_list:
                return root1_list

            # 合并两个数组     
            merged = []
            p1, n1 = 0, len(root1_list)
            p2, n2 = 0, len(root2_list)
            while True:
                if p1 == n1:
                    merged.extend(root2_list[p2:])
                    break
                if p2 == n2:
                    merged.extend(root1_list[p1:])
                    break
                if root1_list[p1] < root2_list[p2]:
                    merged.append(root1_list[p1])
                    p1 += 1
                else:
                    merged.append(root2_list[p2])
                    p2 += 1
            return merged
    ```
### 1376.通知所有员工所需的时间
> 公司里有` n `名员工，每个员工的` ID `都是独一无二的，编号从` 0 `到` n - 1`。公司的总负责人通过` headID `进行标识。  
在` manager `数组中，每个员工都有一个直属负责人，其中` manager[i] `是第` i `名员工的直属负责人。对于总负责人，`manager[headID] = -1`。题目保证从属关系可以用树结构显示。  
公司总负责人想要向公司所有员工通告一条紧急消息。他将会首先通知他的直属下属们，然后由这些下属通知他们的下属，直到所有的员工都得知这条紧急消息。  
第` i `名员工需要` informTime[i] `分钟来通知它的所有直属下属（也就是说在` informTime[i] `分钟后，他的所有直属下属都可以开始传播这一消息）。

返回通知所有员工这一紧急消息所需要的 **分钟数** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/time-needed-to-inform-all-employees  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ DFS
    ```python
    class Solution:
        def numOfMinutes(self, n: int, headID: int, manager: List[int], informTime: List[int]) -> int:
            def dfs(root, total):
                # 没有直属下属了
                if not tree_dict[root]:
                    nonlocal ans
                    ans = max(ans, total)
                    return None

                for i in tree_dict[root]:
                    dfs(i, informTime[root] + total)

            # 构造树型结构,从上到下官职减小
            tree_dict = collections.defaultdict(list)
            for id, leader in enumerate(manager):
                tree_dict[leader].append(id)
            
            ans = 0
            dfs(headID, 0)        
            return ans
    ```
### 1423.可获得的最大点数
> 几张卡牌 **排成一行**，每张卡牌都有一个对应的点数。点数由整数数组` cardPoints `给出。  
每次行动，你可以从行的开头或者末尾拿一张卡牌，最终你必须正好拿` k `张卡牌。  
你的点数就是你拿到手中的所有卡牌的点数之和。  
给你一个整数数组` cardPoints `和整数` k`，请你返回可以获得的最大点数。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/maximum-points-you-can-obtain-from-cards  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ java滑动窗口
```java
class Solution {
    public int maxScore(int[] cardPoints, int k) {
        // 由于只能拿第一张或者最后一张，所以当k次卡牌全被选择完之后，剩下的n-k张卡牌是连续的
        int n = cardPoints.length;
        int windowSize = n - k;
        int sum = 0;
        for (int i = 0; i < windowSize;  i++){
            sum += cardPoints[i];
        }
        // 当前的最小值初始化为前n-k个元素
        int minSum = sum;
        for (int i = windowSize; i < n; i++){
            sum = sum + cardPoints[i] - cardPoints[i - windowSize];
            minSum = Math.min(minSum, sum);
        }

        return Arrays.stream(cardPoints).sum() - minSum;
    }

}
```
### 1438.绝对差不超过限制的最长连续子数组
> 给你一个整数数组` nums `，和一个表示限制的整数` limit`，请你返回最长连续子数组的长度，该子数组中的任意两个元素之间的绝对差必须小于或者等于` limit `。  
如果不存在满足条件的子数组，则返回` 0 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 单调双端队列法 `collections.deque`
    ```python
    class Solution:
        def longestSubarray(self, nums: List[int], limit: int) -> int:
            length = len(nums)
            # 创建两个单调双端队列
            min_queue, max_queue = collections.deque(), collections.deque()
            # 定义滑动窗口左右边界、结果
            left = right = ans = 0

            while right < length: # 滑到最右边结束
                # 我们需要找窗口区间内的最大值和最小值，只要最值都小于等于limit了，其余值肯定满足
                while min_queue and min_queue[-1] > nums[right]: # 如果min_queue有元素,那就把比右窗口大的数去掉，因为我们想要的是这个区间的最小值
                    min_queue.pop()
                while max_queue and max_queue[-1] < nums[right]: # 如果max_queue有元素，那就把比当前滑动窗口右端的值小的数去掉，我们需要区间的最大值
                    max_queue.pop()
                # 把右窗口的值放进去
                min_queue.append(nums[right])
                max_queue.append(nums[right])
                # 如果最值都大于limit了，那么我们的左窗口应该向右移
                while min_queue and max_queue and max_queue[0] - min_queue[0] > limit:
                    if nums[left] == min_queue[0]:
                        min_queue.popleft()
                    if nums[left] == max_queue[0]:
                        max_queue.popleft()
                    left += 1
                ans = max(ans, right - left + 1)
                right += 1
            return ans
    ```
+ python底层并不是平衡树的`sortedcontainers.SortedList`，**内部有序**
    ```python
    class Solution:
        def longestSubarray(self, nums: List[int], limit: int) -> int:
            from sortedcontainers import SortedList
            s = SortedList()
            left, right = 0, 0
            res = 0
            while right < len(nums):
                s.add(nums[right])
                while s[-1] - s[0] > limit:
                    s.remove(nums[left])
                    left += 1
                res = max(res, right - left + 1)
                right += 1
            return res
    ```
+ 使用堆来维护`heapq`
    ```python
    class Solution:
        def longestSubarray(self, nums: List[int], limit: int) -> int:
            from heapq import heappop, heappush
            max_ = []
            min_ = []
            res = 0
            l = 0
            for r, num in enumerate(nums):
                # 大根堆 max_
                heappush(max_, [-num, r])
                # 小根堆 min_
                heappush(min_, [num, r])
                # l 为左指针位置
                while -max_[0][0] - min_[0][0] > limit:
                    # 条件判断需要max,min[0][0]存的索引不在 l 左侧
                    # 删除不在 l 右侧的元素
                    while min_[0][1] <= l:
                        heappop(min_)
                    while max_[0][1] <= l:
                        heappop(max_)
                    # 移动 l
                    l += 1
                # 找到最长的符合要求的窗口长度
                if r - l + 1 > res:
                    res = r - l + 1
            return res
    ```
### 1472.设计浏览器历史记录
> 你有一个只支持单个标签页的` 浏览器 `，最开始你浏览的网页是` homepage `，你可以访问其他的网站` url `，也可以在浏览历史中后退` steps `步或前进` steps `步。

请你实现` BrowserHistory `类：

+ `BrowserHistory(string homepage) `，用` homepage `初始化浏览器类。
+ `void visit(string url)` 从当前页跳转访问` url `对应的页面  。执行此操作会把浏览历史前进的记录全部删除。
+ `string back(int steps)` 在浏览历史中后退` steps `步。如果你只能在浏览历史中后退至多` x `步且` steps > x `，那么你只后退` x `步。请返回后退至多`  steps `步以后的` url `。
+ `string forward(int steps)` 在浏览历史中前进` steps `步。如果你只能在浏览历史中前进至多` x `步且` steps > x `，那么你只前进` x` 步。请返回前进 至多 `steps`步以后的` url `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/design-browser-history  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
class BrowserHistory:

    def __init__(self, homepage: str):
        self.history = [homepage]
        self.curr_idx = 0
        self.len = 1

    def visit(self, url: str) -> None:
        # 当前元素处于栈顶
        if self.curr_idx != self.len - 1:
            for _ in range(0,self.len-self.curr_idx-1):
                self.history.pop()
        self.history.append(url)
        self.curr_idx += 1
        self.len = len(self.history)

    def back(self, steps: int) -> str:
        if self.curr_idx+1 <= steps:
            self.curr_idx = 0
            return self.history[0]
        else:
            while steps:
                steps -= 1
                self.curr_idx -= 1
            return self.history[self.curr_idx]

    def forward(self, steps: int) -> str:
        if self.curr_idx+1+steps > self.len:
            self.curr_idx = self.len -1 
            return self.history[-1]
        else:
            while steps:
                steps -= 1
                self.curr_idx += 1
            return self.history[self.curr_idx]



# Your BrowserHistory object will be instantiated and called as such:
# obj = BrowserHistory(homepage)
# obj.visit(url)
# param_2 = obj.back(steps)
# param_3 = obj.forward(steps)
```
### 1823.找出游戏的获胜者
> 共有` n `名小伙伴一起做游戏。小伙伴们围成一圈，按 **顺时针顺序** 从` 1 `到` n `编号。确切地说，从第` i `名小伙伴顺时针移动一位会到达第` (i+1) `名小伙伴的位置，其中` 1 <= i < n `，从第 `n `名小伙伴顺时针移动一位会回到第` 1 `名小伙伴的位置。

游戏遵循如下规则：

1. 从第` 1 `名小伙伴所在位置 **开始** 。
2. 沿着顺时针方向数` k `名小伙伴，计数时需要 **包含** 起始时的那位小伙伴。逐个绕圈进行计数，一些小伙伴可能会被数过不止一次。
3. 你数到的最后一名小伙伴需要离开圈子，并视作输掉游戏。
4. 如果圈子中仍然有不止一名小伙伴，从刚刚输掉的小伙伴的 顺时针下一位 **小伙伴** 开始，回到步骤` 2 `继续执行。
5. 否则，圈子中最后一名小伙伴赢得游戏。

给你参与游戏的小伙伴总数` n `，和一个整数` k `，返回游戏的获胜者。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/find-the-winner-of-the-circular-game  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 模拟+队列
    ```python
    # python
    class Solution:
        def findTheWinner(self, n: int, k: int) -> int:
            q = deque(range(1, n + 1))
            while len(q) > 1:
                for _ in range(k - 1):
                    q.append(q.popleft())
                q.popleft()
            return q[0]
    

    //java
    class Solution {
        public int findTheWinner(int n, int k) {
            Queue<Integer> queue = new ArrayDeque<Integer>();
            // 编号入队列
            for(int i = 1; i <= n; i++)
                queue.offer(i);
            
            while (queue.size() > 1){
                for(int i = 1; i <= k-1; i++)
                    queue.offer(queue.poll());
                queue.poll();
            }

            return queue.peek();
        }
    }
    ```
+ 递归
    ```python
    class Solution:
        def findTheWinner(self, n: int, k: int) -> int:
            if n <= 1:
                return n
            ans = (self.findTheWinner(n - 1, k) + k) % n
            return n if ans == 0 else ans
    ```
+ 迭代    解释看[这里](https://blog.csdn.net/u011500062/article/details/72855826)
    ```python
    class Solution:
        def findTheWinner(self, n: int, k: int) -> int:
            ans = 0
            for i in range(2, n + 1):
                ans = (ans + k) % i
            return ans + 1
    ```

## 3.面试题系列
### 01.05.一次编辑
> 字符串有三种编辑操作:插入一个字符、删除一个字符或者替换一个字符。 给定两个字符串，编写一个函数判定它们是否只需要一次(或者零次)编辑。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/one-away-lcci/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ python双指针
    ```python
    class Solution:
        def oneEditAway(self, first: str, second: str) -> bool:
            m, n = len(first), len(second)
            # 字母长度差距大于1
            if abs(m - n) > 1:
                return False
            if not first or not second:
                return True
            # 保证一般性，让first长度大于等于second
            if m < n:
                first, second = second, first
                m, n = n, m
            # 最多只有一次插入、替换、删除机会
            chance = 1
            p_m,  p_n = 0, 0
            while p_m < m:
                if p_n < n and first[p_m] != second[p_n]:
                    chance -= 1
                    p_m += 1
                    if m == n:
                        p_n += 1
                else:
                    p_m += 1
                    p_n += 1
                if chance < 0:
                    return False

            return True
    ```
### 04.06.后继者
> 设计一个算法，找出二叉搜索树中指定节点的“下一个”节点（也即中序后继）。  
如果指定节点没有对应的“下一个”节点，则返回`null`。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/successor-lcci/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def inorderSuccessor(self, root: TreeNode, p: TreeNode) -> TreeNode:
        st, pre, cur = [], None, root
        while st or cur:
            while cur:
                st.append(cur)
                cur = cur.left
            cur = st.pop()
            if pre == p:
                return cur
            pre = cur
            cur = cur.right
        return None
```

### 17.11.单词距离
> 有个内含单词的超大文本文件，给定任意两个不同的单词，找出在这个文件中这两个单词的最短距离(相隔单词数)。如果寻找过程在这个文件中会重复多次，而每次寻找的单词不同，你能对此优化吗?

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/find-closest-lcci  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 直接模拟
```java
class Solution {
    public int findClosest(String[] words, String word1, String word2) {
        // 使用双指针来进行距离的计算
        int pFirst = -1, pSecond = -1;
        int n = words.length;
        int ans = Integer.MAX_VALUE;  // 初始化当前的最小值为最大值

        for (int i = 0; i < n; i++) {
            // 找到第一个词的位置
            if (words[i].equals(word1))
                pFirst = i;
            // 找到第二个词的位置
            if (words[i].equals(word2))
                pSecond = i;
            if (pFirst != -1 && pSecond != -1)
                ans = Math.min(ans, Math.abs(pFirst-pSecond));
        }
        return ans;
    }
}
```

## 4.剑指Offer
### 05.替换空格
> 请实现一个函数，把字符串` s `中的每个空格替换成"%20"。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/ti-huan-kong-ge-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public String replaceSpace(String s) {
        // 空串
        if (s == null || s.equals(""))
            return s;
        StringBuffer ans = new StringBuffer();
        for (int i = 0; i  < s.length(); i++) {
            char c = s.charAt(i);
            if (Character.isSpace(c))
                ans.append("%20");
            else
                ans.append(c);
        }
        return ans.toString();
    }
}
```
### 06.从尾到头打印链表
> 输入一个链表的头节点，从尾到头反过来返回每个节点的值（用数组返回）

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/cong-wei-dao-tou-da-yin-lian-biao-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 使用栈的后进先出特性来做
```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public int[] reversePrint(ListNode head) {
        // 使用栈来保存我们遇到的数字
        LinkedList<Integer> stack = new LinkedList<>();
        while (head != null){
            stack.addLast(head.val);
            head = head.next;
        }
        // 最终答案
        int[] ans = new int[stack.size()];
        int i = 0;
        while (!stack.isEmpty()) {
            ans[i++] = stack.removeLast();
        }
        return ans;
    }
}
```
### 09.用两个栈实现队列
> 用两个栈实现一个队列。队列的声明如下，请实现它的两个函数` appendTail `和` deleteHead `，分别完成在队列尾部插入整数和在队列头部删除整数的功能。(若队列中没有元素，`deleteHead` 操作返回` -1 `)

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/yong-liang-ge-zhan-shi-xian-dui-lie-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class CQueue {
    // 实现队列，即实现先进先出
    //不推荐使用Stack，Java官方已经弃用，使用LinkedList

    public LinkedList<Integer> stackOne; // 只进元素
    public LinkedList<Integer> stackTwo;  //非空就移除，空就把one的元素加进来

    public CQueue() {
        stackOne = new LinkedList<>();
        stackTwo = new LinkedList<>();
    }
    
    public void appendTail(int value) {
        // stack one 的作用就是往里面添加元素
        stackOne.addLast(value);
    }
    
    public int deleteHead() {
        if (!stackTwo.isEmpty())
            return stackTwo.removeLast();
        else{
            // 先把stack one中的元素全部移到stack two中间去
            while (!stackOne.isEmpty()){
                stackTwo.addLast(stackOne.removeLast());
            }
            // 如果现在stack two是空，就代表着两个栈都是空的了，那就不能delete
            // 否则就把stack two的最后一个元素移除
            return stackTwo.isEmpty() ? -1 : stackTwo.removeLast();
        }
    }
}

/**
 * Your CQueue object will be instantiated and called as such:
 * CQueue obj = new CQueue();
 * obj.appendTail(value);
 * int param_2 = obj.deleteHead();
 */
```

### 10-I.斐波那契数列
> 写一个函数，输入 n ，求斐波那契（Fibonacci）数列的第 n 项（即 F(N)）。斐波那契数列的定义如下：

+ F(0) = 0,   F(1) = 1
+ F(N) = F(N - 1) + F(N - 2), 其中 N > 1.

斐波那契数列由 0 和 1 开始，之后的斐波那契数就是由之前的两数相加而得出。

答案需要取模 1e9+7（1000000007），如计算初始结果为：1000000008，请返回 1。

 

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/fei-bo-na-qi-shu-lie-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public int fib(int n) {
        if (n <= 1)
            return n;
        int mod = (int)1e9 + 7;
        int a = 0, b = 1;
        for (int i = 2; i <= n; i++) {
            int c = a + b;
            c %= mod;
            a = b;
            b = c;
        }
        return b;
    }
}
```

### 10-II.青蛙跳台阶问题
> 一只青蛙一次可以跳上1级台阶，也可以跳上2级台阶。求该青蛙跳上一个 n 级的台阶总共有多少种跳法。

答案需要取模 1e9+7（1000000007），如计算初始结果为：1000000008，请返回 1。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/qing-wa-tiao-tai-jie-wen-ti-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public int numWays(int n) {
        // f(n) = f(n-1) + f(n-2)
        // 青蛙跳上第n阶的情况是由青蛙跳上第n-1的情况数加上青蛙跳上n-2的情况数
         if (n <= 1)
            return 1;
        int mod = (int)1e9 + 7;
        int[] dp = new int[n+1];
        dp[0] = 1;
        dp[1] = 1;
        for (int j = 2; j < dp.length; j++)
            dp[j] = (dp[j-1] + dp[j-2]) % mod;
        return dp[n];
    }
}
```
### 18.链表中倒数第k个节点
> 给定单向链表的头指针和一个要删除的节点的值，定义一个函数删除该节点。  
返回删除后的链表的头节点。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/shan-chu-lian-biao-de-jie-dian-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode deleteNode(ListNode head, int val) {
        if(head.val == val) return head.next;
        ListNode pre = head, cur = head.next;
        while(cur != null && cur.val != val) {
            pre = cur;
            cur = cur.next;
        }
        if(cur != null) pre.next = cur.next;
        return head;
    }
}
```
### 22.链表中倒数第k个节点
> 输入一个链表，输出该链表中倒数第k个节点。为了符合大多数人的习惯，本题从1开始计数，即链表的尾节点是倒数第1个节点。  
例如，一个链表有 6 个节点，从头节点开始，它们的值依次是 1、2、3、4、5、6。这个链表的倒数第 3 个节点是值为 4 的节点。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/lian-biao-zhong-dao-shu-di-kge-jie-dian-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode getKthFromEnd(ListNode head, int k) {
        ListNode former = head, latter = head;
        for(int i = 0; i < k; i++)
            former = former.next;
        while(former != null) {
            former = former.next;
            latter = latter.next;
        }
        return latter;
    }
}
```
### 24.反转链表
> 定义一个函数，输入一个链表的头节点，反转该链表并输出反转后链表的头节点。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/fan-zhuan-lian-biao-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 指针迭代
```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode reverseList(ListNode head) {
        if (head == null)
            return head;
        // 添加一个dummy head
        ListNode dummyHead = new ListNode(0);
        dummyHead.next = head;
        // p节点永远指向之前链表的第一个节点，origin不断指向新链表的开头位置，q一直往后走处理新节点
        ListNode origin = dummyHead.next, p = dummyHead.next, q = dummyHead.next.next;
        while (p != null && q != null) {
            //连接新节点
            dummyHead.next = q;
            //为下一次连接新节点做准备
            q = q.next;
            //把新节点连接到之前链表的开头
            dummyHead.next.next = origin;
            //链表的结尾指向下一个新节点
            p.next = q;
            // 指向当前新链表的开头
            origin = dummyHead.next;
        }
        return dummyHead.next;
    }
}
```

### 26.树的子结构
> 输入两棵二叉树A和B，判断B是不是A的子结构。(约定空树不是任意一个树的子结构)B是A的子结构， 即 A中有出现和B相同的结构和节点值。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/shu-de-zi-jie-gou-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isSubStructure(TreeNode A, TreeNode B) {
        // 当前起始点就是子结构的开始or在左子树or在右子树
        return (A != null && B != null) && (recur(A, B) || isSubStructure(A.left, B) || isSubStructure(A.right, B));
    }
    boolean recur(TreeNode A, TreeNode B) {
        if(B == null) return true;
        if(A == null || A.val != B.val) return false;
        return recur(A.left, B.left) && recur(A.right, B.right);
    }
}
```

### 27.二叉树的镜像
> 请完成一个函数，输入一个二叉树，该函数输出它的镜像。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/er-cha-shu-de-jing-xiang-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode mirrorTree(TreeNode root) {
        if (root == null) {
            return null;
        }
        TreeNode leftRoot = mirrorTree(root.right);
        TreeNode rightRoot = mirrorTree(root.left);
        root.left = leftRoot;
        root.right = rightRoot;
        return root;
    }
}
```

### 28.对称的二叉树
> 请实现一个函数，用来判断一棵二叉树是不是对称的。如果一棵二叉树和它的镜像一样，那么它是对称的。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/dui-cheng-de-er-cha-shu-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isSymmetric(TreeNode root) {
        if (root == null)
            return true;
        return dfs(root.left, root.right);
    }

    public boolean dfs(TreeNode p, TreeNode q) {
        if ( p == null && q == null)
            return true;
        if ( p == null || q == null)
            return false;
        return p.val == q.val && dfs(p.left, q.right) && dfs(p.right, q.left);
    }
}
```

### 30.包含min函数的栈
> 定义栈的数据结构，请在该类型中实现一个能够得到栈的最小元素的 min 函数在该栈中，调用` min`、`push` 及` pop `的时间复杂度都是` O(1)`。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/bao-han-minhan-shu-de-zhan-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class MinStack {

    public LinkedList<Integer> minStack;
    public LinkedList<Integer> min;  // 保存全局最小值

    /** initialize your data structure here. */
    public MinStack() {
        minStack = new LinkedList<>();
        min = new LinkedList<>();
    }
    
    public void push(int x) {
        minStack.addLast(x);
        // 维护最小值栈
        if (min.isEmpty())
            min.addFirst(x);
        else {
            if (min.peek() > x)
                min.addFirst(x);
            else
                min.addFirst(min.peek());
        }
    }
    
    public void pop() {
        minStack.removeLast();
        min.pop();
    }
    
    public int top() {
        return minStack.peekLast();
    }
    
    public int min() {
        return min.peek();
    }
}

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack obj = new MinStack();
 * obj.push(x);
 * obj.pop();
 * int param_3 = obj.top();
 * int param_4 = obj.min();
 */
```

### 32-I.从上到下打印二叉树
> 从上到下打印出二叉树的每个节点，同一层的节点按照从左到右的顺序打印。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/cong-shang-dao-xia-da-yin-er-cha-shu-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public int[] levelOrder(TreeNode root) {
        // 层序遍历二叉树，也就是BFS
        List<Integer> ans = new ArrayList<>();
        if ( root == null)
            return ans.stream().mapToInt(Integer::valueOf).toArray();

        Deque<TreeNode> queue = new ArrayDeque<>();
        queue.addLast(root);

        while (!queue.isEmpty()) {
            int n = queue.size();
            for (int i = 0; i < n; i++) {
                TreeNode node = queue.removeFirst();
                ans.add(node.val);
                if ( node.left != null) {
                    queue.addLast(node.left);
                }

                if ( node.right != null) {
                    queue.addLast(node.right);
                }

            }
        }
        return ans.stream().mapToInt(Integer::valueOf).toArray();
    }
}
```

### 32-II.从上到下打印二叉树II
> 从上到下按层打印二叉树，同一层的节点按从左到右的顺序打印，每一层打印到一行。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/cong-shang-dao-xia-da-yin-er-cha-shu-ii-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<List<Integer>> levelOrder(TreeNode root) {
        List<List<Integer>> ans = new ArrayList<>();
        if (root == null)
            return ans;
        Deque<TreeNode> queue = new ArrayDeque<>();
        queue.addLast(root);

        while (!queue.isEmpty()) {
            int n = queue.size();
            List<Integer> temp = new ArrayList<>();
            for (int i = 0; i < n; i++) {
                TreeNode node = queue.removeFirst();
                temp.add(node.val);
                if (node.left != null)
                    queue.addLast(node.left);
                if (node.right != null)
                    queue.addLast(node.right);
            }
            ans.add(temp);
        }
        return ans;
    }
}
```

### 32-III.从上到下打印二叉树III
> 请实现一个函数按照之字形顺序打印二叉树，即第一行按照从左到右的顺序打印，第二层按照从右到左的顺序打印，第三行再按照从左到右的顺序打印，其他行以此类推。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/cong-shang-dao-xia-da-yin-er-cha-shu-iii-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<List<Integer>> levelOrder(TreeNode root) {
        List<List<Integer>> ans = new ArrayList<>();
        if (root == null)
            return ans;
        Deque<TreeNode> queue = new ArrayDeque<>();
        queue.addLast(root);
        boolean isEven = true;  //判断当前行是否是偶数行

        while (!queue.isEmpty()) {
            int n = queue.size();
            isEven = !isEven;
            List<Integer> temp = new ArrayList<>();
            for (int i = 0; i < n; i++) {
                TreeNode node = queue.removeFirst();
                temp.add(node.val);
                if (node.left != null)
                    queue.addLast(node.left);
                if (node.right != null)
                    queue.addLast(node.right);
            }
            if (isEven)
                Collections.reverse(temp);
            ans.add(temp);         
        }
        return ans;
    }
}
```
### 35.复杂链表的复制
> 请实现 copyRandomList 函数，复制一个复杂链表。在复杂链表中，每个节点除了有一个 next 指针指向下一个节点，还有一个 random 指针指向链表中的任意节点或者 null。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/fu-za-lian-biao-de-fu-zhi-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 哈希表+递归
```java
/*
// Definition for a Node.
class Node {
    int val;
    Node next;
    Node random;

    public Node(int val) {
        this.val = val;
        this.next = null;
        this.random = null;
    }
}
*/
class Solution {
    // 记录节点
    public Map<Node, Node> listCache = new HashMap<>();

    public Node copyRandomList(Node head) {
        // 当前节点为空
        if (head == null)
            return head;
        // 查看当前的节点是否已经存在
        if (!listCache.containsKey(head)) {
            Node newHead = new Node(head.val);
            listCache.put(head, newHead);
            newHead.next = copyRandomList(head.next);
            newHead.random = copyRandomList(head.random);
        }
        return listCache.get(head);
    }
}
```
### 42.连续子数组的最大和
> 输入一个整型数组，数组中的一个或连续多个整数组成一个子数组。求所有子数组的和的最大值。  
要求时间复杂度为O(n)。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/lian-xu-zi-shu-zu-de-zui-da-he-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 动态规划
```java
class Solution {
    public int maxSubArray(int[] nums) {
        int n = nums.length;
        int dp = nums[0];
        int max = dp;
        for (int i = 1; i < n; i++) {
            // 如果前一个dp是正数，那么以接下来元素结尾的最大值就是前dp加上现有的元素值
            // 负数的话就直接取现在这个值
            dp = Math.max(dp + nums[i], nums[i]);
            max = Math.max(max, dp);
        }
        return max;
    }
}
```

### 46.把数字翻译成字符串
> 给定一个数字，我们按照如下规则把它翻译为字符串：0 翻译成 “a” ，1 翻译成 “b”，……，11 翻译成 “l”，……，25 翻译成 “z”。一个数字可能有多个翻译。请编程实现一个函数，用来计算一个数字有多少种不同的翻译方法。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/ba-shu-zi-fan-yi-cheng-zi-fu-chuan-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 动态规划
```java
class Solution {
    public int translateNum(int num) {
        String s = String.valueOf(num);
        int a = 1, b = 1;
        for(int i = 2; i <= s.length(); i++) {
            String tmp = s.substring(i - 2, i);
            int c = tmp.compareTo("10") >= 0 && tmp.compareTo("25") <= 0 ? a + b : a;
            b = a;
            a = c;
        }
        return a;
    }
}
```

### 47.礼物的最大价值
> 在一个 m*n 的棋盘的每一格都放有一个礼物，每个礼物都有一定的价值（价值大于 0）。你可以从棋盘的左上角开始拿格子里的礼物，并每次向右或者向下移动一格、直到到达棋盘的右下角。给定一个棋盘及其上面的礼物的价值，请计算你最多能拿到多少价值的礼物？

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/li-wu-de-zui-da-jie-zhi-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 动态规划
```java
class Solution {
    public int maxValue(int[][] grid) {
        int m = grid.length, n = grid[0].length;
        for(int i = 0; i < m; i++) {
            for(int j = 0; j < n; j++) {
                if(i == 0 && j == 0) continue;
                if(i == 0) grid[i][j] += grid[i][j - 1] ;
                else if(j == 0) grid[i][j] += grid[i - 1][j];
                else grid[i][j] += Math.max(grid[i][j - 1], grid[i - 1][j]);
            }
        }
        return grid[m - 1][n - 1];
    }
}
```

### 48.最长不含重复字符的子字符串
> 请从字符串中找出一个最长的不包含重复字符的子字符串，计算该最长子字符串的长度。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/zui-chang-bu-han-zhong-fu-zi-fu-de-zi-zi-fu-chuan-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 滑动窗口
```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        // 滑动窗口
        if (s.length() == 0)
            return 0;
        Map<Character, Integer> map = new HashMap<>();
        int maxLength = 1;
        int left = 0, right = 0;
        int total = 0; // 窗口内的字符类别总数
        while (right < s.length()) {
            char ch = s.charAt(right);
            // 新进入窗口的字符数加1
            map.put(ch, map.getOrDefault(ch, 0) + 1);
            // 当某个字符长度等于1的时候，就代表着字母的种类数增加了
            if (map.get(ch) == 1)
                total++;
            // 如果窗口内的字符长度大于字符类别总数，说明肯定就存在着重复字符了
            // 左指针右移
            while (total < right - left + 1) {
                map.put(s.charAt(left), map.get(s.charAt(left)) - 1);
                if (map.get(s.charAt(left)) == 0)
                    total--;
                left++;
            }
            maxLength = Math.max(maxLength, right - left + 1);
            right++;
        }
        return maxLength;
    }
}
```

### 58-II.左旋转字符串
> 字符串的左旋转操作是把字符串前面的若干个字符转移到字符串的尾部。请定义一个函数实现字符串左旋转操作的功能。比如，输入字符串"abcdefg"和数字2，该函数将返回左旋转两位得到的结果"cdefgab"。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/zuo-xuan-zhuan-zi-fu-chuan-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public String reverseLeftWords(String s, int n) {
        if (s == null || s.equals(""))
            return s;

        StringBuffer ans = new StringBuffer();
        for (int i = n; i < s.length(); i++) {
            ans.append(s.charAt(i));
        }
        for (int i = 0; i < n; i++) {
            ans.append(s.charAt(i));
        }
        return ans.toString();
    }
}
```
### 63.股票的最大利润
> 假设把某股票的价格按照时间先后顺序存储在数组中，请问买卖该股票一次可能获得的最大利润是多少？

 来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/gu-piao-de-zui-da-li-run-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public int maxProfit(int[] prices) {
        if (prices.length == 0) return 0;
        int buy = Integer.MAX_VALUE;
        int profit = 0;

        for (int price: prices) {
            // 我们需要最低价格买入
            buy = Math.min(buy, price);
            // 我们需要最高的利润
            profit = Math.max(profit, price - buy);
        }
        return profit;
    }
}
```
### 64.求1+2+...+n
> 求 1+2+...+n ，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A?B:C）。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/qiu-12n-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 短路与的考察，秀的我头皮发麻
```java
class Solution {
    public int sumNums(int n) {
        boolean flag = n > 0 && (n += sumNums(n - 1)) > 0;
        return n;
    }
}
```

### 65.不用加减乘除做加法
> 写一个函数，求两个整数之和，要求在函数体内不得使用 “+”、“-”、“*”、“/” 四则运算符号。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/bu-yong-jia-jian-cheng-chu-zuo-jia-fa-lcof/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 考察位运算
```java
class Solution {
    public int add(int a, int b) {
        if (b == 0)
            return a;
        // a^b代表着异或，代表着没有进位的加法，但是数字中间可能某一位对应都是1，这样就遗漏掉了进位
        // a&b按位与，就是为了找到发生进位的位置，然后 <<1 左移一位就代表着这个进位的最终位置
        // 这个时候没进位的+进位的就是答案，所以递归求解，直到没有进位为止，这个时候的异或就是真正的答案
        // 注意结合性，<<的优先级比&高
        return add(a^b, (a&b) << 1);
    }
}
```

### 66.构建乘积数组
> 给定一个数组` A[0,1,…,n-1]`，请构建一个数组` B[0,1,…,n-1]`，其中` B[i] `的值是数组` A `中除了下标` i `以外的元素的积, 即` B[i]=A[0]×A[1]×…×A[i-1]×A[i+1]×…×A[n-1]`。不能使用除法。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/gou-jian-cheng-ji-shu-zu-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```java
class Solution {
    public int[] constructArr(int[] a) {
        // 边界判断，我是没想到的，题目里面没有特殊提到的话多半就是存在这样的case
        if (a == null || a.length == 0)
            return a;
        int[] ans = new int[a.length];
        int[] left = new int[a.length];
        int[] right = new int[a.length];

        // 对于每个位置的左边进行计算
        left[0] = 1;
        for (int i = 1; i < a.length; i++){
            left[i] = left[i-1] * a[i-1];
        }
        //对于每个位置的右边进行计算
        right[a.length - 1] = 1;
        for (int i = a.length - 2; i >= 0 ; i--) {
            right[i] = right[i+1] * a[i+1];
        }

        //对应位置的元素直接相乘，就可以获得该位置的最终结果
        for (int i = 0; i < a.length; i++) {
            ans[i] = left[i] * right[i];
        }
        return ans;
    }
}
```
### 67.把字符串转换成整数
> 写一个函数 StrToInt，实现把字符串转换成整数这个功能。不能使用 atoi 或者其他类似的库函数。

 

首先，该函数会根据需要丢弃无用的开头空格字符，直到寻找到第一个非空格的字符为止。

当我们寻找到的第一个非空字符为正或者负号时，则将该符号与之后面尽可能多的连续数字组合起来，作为该整数的正负号；假如第一个非空字符是数字，则直接将其与之后连续的数字字符组合起来，形成整数。

该字符串除了有效的整数部分之后也可能会存在多余的字符，这些字符可以被忽略，它们对于函数不应该造成影响。

注意：假如该字符串中的第一个非空格字符不是一个有效整数字符、字符串为空或字符串仅包含空白字符时，则你的函数不需要进行转换。

在任何情况下，若函数不能进行有效的转换时，请返回 0。

说明：

假设我们的环境只能存储 32 位大小的有符号整数，那么其数值范围为 [−231,  231 − 1]。如果数值超过这个范围，请返回  INT_MAX (231 − 1) 或 INT_MIN (−231) 。

来源：力扣（LeetCode）  
链接：https://leetcode.cn/problems/ba-zi-fu-chuan-zhuan-huan-cheng-zheng-shu-lcof  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 状态机的使用，是一种比较好的思想

![状态机图示](/image/offer/67.png)

```java
class Solution {
    // 状态机
    class Automaton {
        public String state = "start";
        public long ans;
        public int sign = 1;  // 该数字的正负情况，1代表正，0代表负\
        public Map<String, String[]> table = new HashMap<String, String[]>() {{
            put("start", new String[]{"start", "signed", "in_number", "end"});
            put("signed", new String[]{"end", "end", "in_number", "end"});
            put("in_number", new String[]{"end", "end", "in_number", "end"});
            put("end", new String[]{"end", "end", "end", "end"});
        }};

        public void get(char c) {
            state = table.get(state)[get_col(c)];
            if ("in_number".equals(state)) {
                ans = ans * 10 + c - '0';
                ans = sign == 1 ? Math.min(ans, (long) Integer.MAX_VALUE) : Math.min(ans, -(long) Integer.MIN_VALUE);
            } else if ("signed".equals(state)) {
                sign = c == '+' ? 1 : -1;
            }

        }

        public int get_col(char c) {
            if (c == ' ') {
                return 0;
            }
            if (c == '+' || c == '-') {
                return 1;
            }
            if (Character.isDigit(c)) {
                return 2;
            }
            return 3;

        }
    }

    public int strToInt(String str) {
        Automaton automaton = new Automaton();
        int length = str.length();
        for (int i = 0; i < length; ++i) {
            automaton.get(str.charAt(i));
        }
        return (int) (automaton.sign * automaton.ans);
    }
}
```