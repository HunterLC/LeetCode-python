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

 