# LeetCode-python
我要刷题冲冲冲

## 基础知识
### 排序算法
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
#### 6.希尔排序
#### 7.堆排序

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
            for num in [1<<x for x in range(10) if 1<<x < 50 ]:
                print(num)


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







###