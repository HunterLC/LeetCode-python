# LeetCode-python
![](https://img.shields.io/badge/Python%20Version-3.7-blue)
![](https://img.shields.io/badge/已覆盖-74题-green)
![](https://img.shields.io/badge/排序算法-7种-red)
![](https://img.shields.io/badge/同向双指针-滑动窗口-orange)
![](https://img.shields.io/badge/宽度优先搜索-BFS-yellow)

我要刷题**冲冲冲**

## 基础知识
### No.1 排序算法（java实现）
#### 1.选择排序
> 简单选择排序是最简单直观的一种算法，基本思想为每一趟从待排序的数据元素中选择最小（或最大）的一个元素作为首元素，直到所有元素排完为止，简单选择排序是不稳定排序。  
在算法实现时，每一趟确定最小元素的时候会通过不断地比较交换来使得首位置为当前最小，交换是个比较耗时的操作。其实我们很容易发现，在还未完全确定当前最小元素之前，这些交换都是无意义的。我们可以通过设置一个变量min，每一次比较仅存储较小元素的数组下标，当轮循环结束之后，那这个变量存储的就是当前最小元素的下标，此时再执行交换操作即可。 

```
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
#### 2.冒泡排序
> 冒泡排序的基本思想是，对相邻的元素进行两两比较，顺序相反则进行交换，这样，每一趟会将最小或最大的元素`浮`到顶端，最终达到完全有序 

示例：  
![冒泡排序示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/冒泡排序.png)

```
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
#### 3.插入排序
> 直接插入排序基本思想是每一步将一个待排序的记录，插入到前面已经排好序的有序序列中去，直到插完所有元素为止。  

示例：  
![直接插入排序示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/直接插入排序.png)

```
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
#### 4.快速排序
> 快速排序(Quick Sort)使用分治法策略。  
它的基本思想是：选择一个基准数，通过一趟排序将要排序的数据分割成独立的两部分；其中一部分的所有数据都比另外一部分的所有数据都要小。然后，再按此方法对这两部分数据分别进行快速排序，整个排序过程可以递归进行，以此达到整个数据变成有序序列。  
**快速排序流程**：  
(1) 从数列中挑出一个基准值。  
(2) 将所有比基准值小的摆放在基准前面，所有比基准值大的摆在基准的后面(相同的数可以到任一边)；在这个分区退出之后，该基准就处于数列的中间位置。  
(3) 递归地把"基准值前面的子数列"和"基准值后面的子数列"进行排序。  

示例(**第一轮**)  
![快速排序第一轮示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/快速排序.jpg)

```
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

#### 5.归并排序
> 归并排序（MERGE-SORT）是利用归并的思想实现的排序方法，该算法采用经典的分治（divide-and-conquer）策略:分治法将问题分(divide)成一些小的问题然后递归求解，而治(conquer)的阶段则将分的阶段得到的各答案"修补"在一起，即分而治之。
+ top down
这种结构很像一棵完全二叉树，本文的归并排序我们采用递归去实现（也可采用迭代的方式去实现）。分阶段可以理解为就是递归拆分子序列的过程，递归深度为log2n。  
![归并排序top down总思路](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/归并排序1.png)  
治阶段，我们需要将两个已经有序的子序列合并成一个有序序列，比如上图中的最后一次合并，要将[4,5,7,8]和[1,2,3,6]两个已经有序的子序列，合并为最终序列[1,2,3,4,5,6,7,8]  
![归并排序top down治思路](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/归并排序2.png)  
最后  
![归并排序top down思路](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/归并排序3.png)  

```
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

#### 6.希尔排序
> 希尔排序是把记录按下标的一定增量分组，对每组使用直接插入排序算法排序；随着增量逐渐减少，每组包含的关键词越来越多，当增量减至1时，整个文件恰被分成一组，算法便终止。  
希尔排序在数组中采用跳跃式分组的策略，通过某个增量将数组元素划分为若干组，然后分组进行插入排序，随后逐步缩小增量，继续按组进行插入排序操作，直至增量为1。希尔排序通过这种策略使得整个数组在初始阶段达到从宏观上看基本有序，小的基本在前，大的基本在后。然后缩小增量，到增量为1时，其实多数情况下只需微调即可，不会涉及过多的数据移动。  
我们来看下希尔排序的基本步骤，在此我们选择增量gap=length/2，缩小增量继续以gap = gap/2的方式，这种增量选择我们可以用一个序列来表示，{n/2,(n/2)/2...1}，称为增量序列。希尔排序的增量序列的选择与证明是个数学难题，我们选择的这个增量序列是比较常用的，也是希尔建议的增量，称为希尔增量，但其实这个增量序列不是最优的。此处我们做示例使用希尔增量。

示例:
![希尔排序示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/希尔排序.png)
```
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

#### 7.堆排序
> 堆排序是利用堆这种数据结构而设计的一种排序算法，堆排序是一种选择排序，它的最坏，最好，平均时间复杂度均为O(nlogn)，它也是不稳定排序。  

堆是具有以下性质的完全二叉树：每个结点的值都大于或等于其左右孩子结点的值，称为大顶堆；或者每个结点的值都小于或等于其左右孩子结点的值，称为小顶堆。  
![大顶堆、小顶堆](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序1.png)  
对堆中的结点按层进行编号，将这种逻辑结构映射到数组中就是下面这个样子  
![数组表示结果](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序2.png)  
该数组从逻辑上讲就是一个堆结构，我们用简单的公式来描述一下堆的定义就是  
+ 大顶堆：arr[i] >= arr[2i+1] && arr[i] >= arr[2i+2] 
+ 小顶堆：arr[i] <= arr[2i+1] && arr[i] <= arr[2i+2]

**基本过程(以大顶堆为例)**
> 将待排序序列构造成一个大顶堆，此时，整个序列的最大值就是堆顶的根节点。将其与末尾元素进行交换，此时末尾就为最大值。然后将剩余n-1个元素重新构造成一个堆，这样会得到n个元素的次小值。如此反复执行，便能得到一个有序序列了

step 1: 构造初始堆。将给定无序序列构造成一个大顶堆（一般升序采用大顶堆，降序采用小顶堆)。  
|序号|说明|示意图|
|:-:|-|:-:|
|1|假设给定无序序列结构|![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序3.png)|
|2|从最后一个非叶子结点开始（叶结点自然不用调整，第一个非叶子结点 arr.length/2-1=5/2-1=1，也就是下面的6结点），从左至右，从下至上进行调整|![找最后一个非叶子结点](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序4.png)|
|3|找到第二个非叶节点4，由于[4,9,8]中9元素最大，4和9交换|![找下一个相邻的非叶子节点](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序5.png)|
|4|交换导致了子根[4,5,6]结构混乱，继续调整，[4,5,6]中6最大，交换4和6。我们就将一个无需序列构造成了一个大顶堆|![调整子树](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序6.png)|  

step 2: 将堆顶元素与末尾元素进行交换，使末尾元素最大。然后继续调整堆，再将堆顶元素与末尾元素交换，得到第二大元素。如此反复进行交换、重建、交换。  
|序号|说明|示意图|
|:-:|-|:-:|
|1|将堆顶元素9和末尾元素4进行交换|![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序7.png)|
|2|重新调整结构，使其继续满足堆定义|![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序8.png)|
|3|再将堆顶元素8与末尾元素5进行交换，得到第二大元素8|![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序9.png)|
|4|后续过程，继续进行调整，交换，如此反复进行，最终使得整个序列有序|![示例](https://github.com/HunterLC/LeetCode-python/blob/main/image/sort/堆排序10.png)|

```
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

### No.2 同向双指针/滑动窗口
1. 常用模板
```
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
2. 代表题目
    395、340、424、76、3、1004

### No.3 宽度优先搜索BFS
> BFS常用于**层序遍历**和**最短路径**

![DFS、BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/DFS和BFS示意图1.gif)

1. 二叉树上 `DFS` 与 `BFS` 代码比较  
    + DFS遍历使用**递归**
    ```
    def dfs(root: TreeNode):
        if not root:
            return 
        dfs(root.left)
        dfs(root.right)
    ```
    + BFS遍历使用**队列**
    ```
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

2. BFS应用一：层序遍历

什么是层序遍历呢？简单来说，层序遍历就是把二叉树分层，然后每一层从左到右遍历：

![BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/bfs2.jpg)

乍一看来，这个遍历顺序和 BFS 是一样的，我们可以直接用 BFS 得出层序遍历结果。然而，层序遍历要求的输入结果和 BFS 是不同的。层序遍历要求我们区分每一层，也就是返回一个二维数组。而 BFS 的遍历结果是一个一维数组，无法区分每一层。

![BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/bfs3.jpg)

那么，怎么给 BFS 遍历的结果分层呢？我们首先来观察一下 BFS 遍历的过程中，结点进队列和出队列的过程：

![BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/bfs4.gif)

截取 BFS 遍历过程中的某个时刻：

![BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/bfs5.jpg)

可以看到，此时队列中的结点是 3、4、5，分别来自第 1 层和第 2 层。这个时候，第 1 层的结点还没出完，第 2 层的结点就进来了，而且两层的结点在队列中紧挨在一起，我们无法区分队列中的结点来自哪一层。

因此，我们需要稍微修改一下代码，在每一层遍历开始前，先记录队列中的结点数量 n（也就是这一层的结点数量），然后一口气处理完这一层的 n 个结点。

```
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

![BFS示意图](https://github.com/HunterLC/LeetCode-python/blob/main/image/bfs/bfs6.gif)


## 题目
### 1.两数之和
> 给定一个整数数组 `nums` 和一个整数目标值 `target`，请你在该数组中找出 和为目标值 `target`  的那 两个 整数，并返回它们的数组下标。
你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。
你可以按任意顺序返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/two-sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  

```
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
    ```
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
    ```
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
 
```
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
    ```
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
    ```
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

    ```
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
### 11.盛水最多的容器
> 给定一个长度为` n `的整数数组` height `。有` n `条垂线，第` i `条线的两个端点是` (i, 0) `和 `(i, height[i])` 。  
找出其中的两条线，使得它们与` x `轴共同构成的容器可以容纳最多的水。  
返回容器可以储存的最大水量。

说明：你不能倾斜容器

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/container-with-most-water  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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

```
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
### 18.四数之和
> 给你一个由` n `个整数组成的数组` nums `，和一个目标值` target `。请你找出并返回满足下述全部条件且不重复的四元组` [nums[a], nums[b], nums[c], nums[d]] `（若两个四元组元素一一对应，则认为两个四元组重复）： 
+ 0 <= a, b, c, d < n
+ a、b、c 和 d 互不相同
+ nums[a] + nums[b] + nums[c] + nums[d] == target
你可以按 **任意顺序** 返回答案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/4sum  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
```
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
### 23.合并K个升序链表
> 给你一个链表数组，每个链表都已经按升序排列。  
请你将所有链表合并到一个升序链表中，返回合并后的链表。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/merge-k-sorted-lists/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
    ```
    class Solution:
        def removeElement(self, nums: List[int], val: int) -> int:
            for i in range(nums.count(val)):
                nums.remove(val)
            return len(nums)
    ```

+ 法二：双指针做法
    ```
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
    ```
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
    ```
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

```
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
### 49.字母异位词分组
> 给你一个字符串数组，请你将 **字母异位词** 组合在一起。可以按任意顺序返回结果列表。  
**字母异位词** 是由重新排列源单词的字母得到的一个新单词，所有源单词中的字母通常恰好只用一次。
 
来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/group-anagrams  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        result = collections.defaultdict(list)
        for i in strs:
            key = ''.join(sorted(i))
            result[key].append(i)

        return list(result.values())
```
### 54.螺旋矩阵
> 给你一个` m `行` n `列的矩阵` matrix `，请按照**顺时针**螺旋顺序 ，返回矩阵中的所有元素。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/spiral-matrix/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。 

```
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
    ```
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

```
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
### 73.矩阵置零
> 给定一个` m x n `的矩阵，如果一个元素为` 0 `，则将其所在行和列的所有元素都设为` 0 `。请使用 **原地** 算法。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/set-matrix-zeroes/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
    ```
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
    ```
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
    ```
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
    ```
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

```
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
### 88.合并两个有序数组
> 给你两个按 **非递减顺序** 排列的整数数组` nums1 `和` nums2`，另有两个整数` m `和` n `，分别表示 `nums1 `和 `nums2` 中的元素数目。

请你 **合并** `nums2` 到 `nums1` 中，使合并后的数组同样按 **非递减顺序** 排列。

**注意：**最终，合并后数组不应由函数返回，而是存储在数组 `nums1` 中。为了应对这种情况，`nums1` 的初始长度为` m + n`，其中前` m `个元素表示应合并的元素，后` n `个元素为` 0` ，应忽略。`nums2 `的长度为` n `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/merge-sorted-array  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 92.反转链表 II
> 给你单链表的头指针` head `和两个整数` left `和` right `，其中` left <= right `。请你反转从位置` left `到位置` right `的链表节点，返回**反转后的链表**

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/reverse-linked-list-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
+ 自己的解答 
    ```
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
    ```
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
### 102.二叉树的层序遍历
> 给你二叉树的根节点` root `，返回其节点值的 **层序遍历** 。 （即逐层地，从左到右访问所有节点）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/binary-tree-level-order-traversal/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
### 125.验证回文串
> 给定一个字符串，验证它是否是回文串，只考虑字母和数字字符，可以忽略字母的大小写。  
说明：本题中，我们将空字符串定义为有效的回文串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/valid-palindrome/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
 
```
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
### 128.最长连续序列
> 给定一个未排序的整数数组` nums `，找出数字连续的最长序列（不要求序列元素在原数组中连续）的长度。  
请你设计并实现时间复杂度为` O(n) `的算法解决此问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-consecutive-sequence  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 141.环形链表 I
> 给你一个链表的头节点` head `，判断链表中是否有环。  
如果链表中有某个节点，可以通过连续跟踪` next `指针再次到达，则链表中存在环。 为了表示给定链表中的环，评测系统内部使用整数` pos `来表示链表尾连接到链表中的位置（索引从 0 开始）。注意：`pos `不作为参数进行传递 。仅仅是为了标识链表的实际情况。  
如果链表中存在环 ，则返回` true `。 否则，返回` false `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/linked-list-cycle  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。  
```
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
```
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

```
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
    ```
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
    ```
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

```
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

```
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

```
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

```
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

```
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

```
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
### 206.反转链表
> 给你单链表的头节点` head `，请你反转链表，并返回反转后的链表。
 
来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/reverse-linked-list/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处

+ 迭代法
    ```
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
    ```
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
### 215.数组中的第k个最大元素
> 给定整数数组 nums 和整数 k，请返回数组中第 k 个最大的元素。  
请注意，你需要找的是数组排序后的第 k 个最大的元素，而不是第 k 个不同的元素。

来源：力扣（LeetCode）    
链接：https://leetcode-cn.com/problems/kth-largest-element-in-an-array/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处

+ 调库(~~毫无意义~~)
    ```
    class Solution:
        def findKthLargest(self, nums: List[int], k: int) -> int:
            nums.sort(reverse = True)
            return nums[k-1]
    ```

+ 大顶堆
    ```
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
### 224.基本计算器
> 给你一个字符串表达式` s `，请你实现一个基本计算器来计算并返回它的值。  
注意:不允许使用任何将字符串作为数学表达式计算的内置函数，比如` eval() `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/basic-calculator/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```
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
```
void push(int x) 将元素 x 压入栈顶。
int pop() 移除并返回栈顶元素。
int top() 返回栈顶元素。
boolean empty() 如果栈是空的，返回 true ；否则，返回 false 。
```
注意：

你只能使用队列的基本操作 —— 也就是` push to back、peek/pop from front、size `和` is empty `这些操作。  
你所使用的语言也许不支持队列。 你可以使用 ` list `（列表）或者 `deque`（双端队列）来模拟一个队列 , 只要是标准的队列操作即可。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/implement-stack-using-queues  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 一个队列实现
    ```
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
    ```
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

```
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
### 240.搜索二维矩阵II
> 编写一个高效的算法来搜索` m x n `矩阵` matrix `中的一个目标值` target `。该矩阵具有以下特性：  
每行的元素从左到右升序排列。
每列的元素从上到下升序排列。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/search-a-2d-matrix-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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

```
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

```
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

```
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

```
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
### 328.奇偶链表
> 给定单链表的头节点` head `，将所有索引为奇数的节点和索引为偶数的节点分别组合在一起，然后返回重新排序的列表。  
第一个节点的索引被认为是` 奇数 `， 第二个节点的索引为` 偶数 `，以此类推。  
请注意，偶数组和奇数组内部的相对顺序应该与输入时保持一致。  
你必须在` O(1) `的额外空间复杂度和` O(n) `的时间复杂度下解决这个问题。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/odd-even-linked-list  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 347.前K个高频元素
> 给你一个整数数组` nums `和一个整数` k `，请你返回其中出现频率前` k `高的元素。你可以按 **任意顺序** 返回答案。

 来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/top-k-frequent-elements/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
### 378.有序矩阵中的第K小的元素
> 给你一个` n x n `矩阵` matrix `，其中每行和每列元素均按升序排序，找到矩阵中第` k `小的元素。  
请注意，它是 **排序后** 的第` k `小元素，而不是第` k `个 **不同** 的元素。  
你必须找到一个内存复杂度优于` O(n2) `的解决方案。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/kth-smallest-element-in-a-sorted-matrix  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```
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

```
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
### 395.至少有 K 个重复字符的最长子串
> 给你一个字符串` s `和一个整数` k `，请你找出` s `中的最长子串， 要求该子串中的每一字符出现次数都不少于` k `。返回这一子串的长度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-substring-with-at-least-k-repeating-characters/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 409.最长回文串
> 给定一个包含大写字母和小写字母的字符串` s `，返回 通过这些字母构造成的 **最长的回文串** 。  
在构造过程中，请注意 **区分大小写** 。比如` "Aa" `不能当做一个回文字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-palindrome  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 424.替换后的最长重复字符
> 给你一个字符串` s `和一个整数` k `。你可以选择字符串中的任一字符，并将其更改为任何其他大写英文字符。该操作最多可执行` k `次。  
在执行上述操作后，返回包含相同字母的最长子字符串的长度。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-repeating-character-replacement  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 454.四数相加Ⅱ
> 给你四个整数数组` nums1`、`nums2`、`nums3` 和` nums4 `，数组长度都是` n `，请你计算有多少个元组` (i, j, k, l) `能满足：

+ `0 <= i, j, k, l < n`
+ `nums1[i] + nums2[j] + nums3[k] + nums4[l] == 0`

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/4sum-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 528.按权重随机选择
> 给你一个 下标从` 0 `开始 的正整数数组` w `，其中` w[i] `代表第` i `个下标的权重。  
请你实现一个函数` pickIndex `，它可以 随机地 从范围` [0, w.length - 1]` 内（含 `0` 和` w.length - 1`）选出并返回一个下标。选取下标` i` 的 概率 为` w[i] / sum(w)` 。

例如，对于` w = [1, 3]`，挑选下标` 0 `的概率为` 1 / (1 + 3) = 0.25 `（即，`25%`），而选取下标` 1 `的概率为` 3 / (1 + 3) = 0.75`（即，`75%`）。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/random-pick-with-weight  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
### 647.回文子串（与题5可做比较）
> 给你一个字符串` s `，请你统计并返回这个字符串中 **回文子串** 的数目。  
**回文字符串** 是正着读和倒过来读一样的字符串。  
**子字符串** 是字符串中的由连续字符组成的一个序列。  
具有不同开始位置或结束位置的子串，即使是由相同的字符组成，也会被视作不同的子串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/palindromic-substrings  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 法一：中心扩散
    ```
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
    ```
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
### 692.前K个高频单词
> 给定一个单词列表` words `和一个整数` k `，返回前` k `个出现次数最多的单词。  
返回的答案应该按单词出现频率由高到低排序。如果不同的单词有相同出现频率， 按**字典顺序** 排序。  

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/top-k-frequent-words  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 735.行星碰撞
> 给定一个整数数组` asteroids`，表示在同一行的行星。  
对于数组中的每一个元素，其绝对值表示行星的大小，正负表示行星的移动方向（正表示向右移动，负表示向左移动）。每一颗行星以相同的速度移动。  
找出碰撞后剩下的所有行星。碰撞规则：两个行星相互碰撞，较小的行星会爆炸。如果两颗行星大小相同，则两颗行星都会爆炸。两颗移动方向相同的行星，永远不会发生碰撞。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/asteroid-collision  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 767.重构字符串
> 给定一个字符串`S`，检查是否能重新排布其中的字母，使得两相邻的字符不同。  
若可行，输出任意可行的结果。若不可行，返回空字符串。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/reorganize-string/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 876.链表的中间结点
> 给定一个头结点为` head `的非空单链表，返回链表的中间结点。  
如果有两个中间结点，则返回第二个中间结点。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/middle-of-the-linked-list/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 快慢指针
    ```
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

```
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
### 973.最接近原点的K个点
> 给定一个数组` points `，其中` points[i] = [xi, yi] `表示` X-Y `平面上的一个点，并且是一个整数` k `，返回离原点` (0,0) `最近的` k `个点。  
这里，平面上两点之间的距离是 `欧几里德距离（ √(x1 - x2)2 + (y1 - y2)2 ）`。  
你可以按 **任何顺序** 返回答案。除了点坐标的顺序之外，答案 **确保** 是 **唯一** 的。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/k-closest-points-to-origin  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 小顶堆(这样做不省空间，相当是所有的点都放进去算了之后选了前K个顶点)
    ```
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
    ```
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
### 1004.最大连续1的个数 III
> 给定一个二进制数组` nums `和一个整数` k `，如果可以翻转最多`k `个` 0` ，则返回 **数组中连续` 1 `的最大个数** 。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/max-consecutive-ones-iii/  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
### 1209.删除字符串中的所有相邻重复项 II
> 给你一个字符串` s`，「k 倍重复项删除操作」将会从` s `中选择` k `个相邻且相等的字母，并删除它们，使被删去的字符串的左侧和右侧连在一起。  
你需要对` s `重复进行无限次这样的删除操作，直到无法继续为止。  
在执行完所有删除操作后，返回最终得到的字符串。  
本题答案保证唯一。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/remove-all-adjacent-duplicates-in-string-ii  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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

```
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
### 1300.转变数组后最接近目标值的数组和
> 给你一个整数数组` arr `和一个目标值` target `，请你返回一个整数` value `，使得将数组中所有大于` value `的值变成` value `后，数组的和最接近`  target `（最接近表示两者之差的绝对值最小）。  
如果有多种使得和最接近 target 的方案，请你返回这些整数中的最小值。  
请注意，答案不一定是 arr 中的数字

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/sum-of-mutated-array-closest-to-target  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```
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
### 1438.绝对差不超过限制的最长连续子数组
> 给你一个整数数组` nums `，和一个表示限制的整数` limit`，请你返回最长连续子数组的长度，该子数组中的任意两个元素之间的绝对差必须小于或者等于` limit `。  
如果不存在满足条件的子数组，则返回` 0 `。

来源：力扣（LeetCode）  
链接：https://leetcode-cn.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit  
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

+ 单调双端队列法 `collections.deque`
    ```
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
    ```
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
    ```
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

```
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