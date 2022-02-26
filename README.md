# LeetCode-python
![](https://img.shields.io/badge/Python%20Version-3.7-blue)
![](https://img.shields.io/badge/排序算法-7种-red)

我要刷题**冲冲冲**

## 基础知识
### 排序算法（java实现）
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
### 876.链表的中间结点
> 给定一个头结点为` head `的非空单链表，返回链表的中间结点。  
如果有两个中间结点，则返回第二个中间结点。
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