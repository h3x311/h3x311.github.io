---
title: "Leetcodenote"
date: 2022-05-25T19:32:00+08:00
draft: true
author: "sober"
showToc: true
TocOpen: false
hidemeta: false
comments: true
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
tags:
- leetcode
categories:
- cs
---

> [14 patterns]([https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed](https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed "Linkify Plus Plus"))
- 熟悉的语言
- Lc like gym 除非练过 不然不要想太多

1.Binary Search 2. DFS, BFS，Best FS 
3. Iteration /recursion 4. LinkedList 
4. 5. Graph/tree 6. Queue/Stack/Heap 
5. 7.DP 
6. 7.  9.Bit
7. 9.  11. Sorting  13. Trie etc.
8.  10.Sliding window 12. Multiple pointers 8. Array/String 9. Set/HashMap



链表，二叉树，回溯，深度宽度优先遍历，图，贪心，动规，数组，哈希表……每个Tag由easy到hard，每道题先自己思考，不会的参考了一个开源的解答或者参考论坛或者博客。
- [pythonFunc]([https://docs.python.org/3/library/functions.html#enumerate](https://docs.python.org/3/library/functions.html#enumerate "Linkify Plus Plus"))
- [python格式]([https://pep8.org/](https://pep8.org/ "Linkify Plus Plus"))
- [blind75list]([https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-100-LeetCode-Questions-to-Save-Your-Time-OaM1orEU](https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-100-LeetCode-Questions-to-Save-Your-Time-OaM1orEU "Linkify Plus Plus"))
- [# Short-circuit evaluation]([https://en.wikipedia.org/wiki/Short-circuit_evaluation](https://en.wikipedia.org/wiki/Short-circuit_evaluation "Linkify Plus Plus"))

- draw pic
- use pattern structure
- test your knowledge

# 1_twosum

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC/2022/Pasted%20image%2020220307105831test.png)
### hash table
1. key - val
	1. key - unique
		1. 多对一的关系。
# 2_maxprofig

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC/2022/Pasted%20image%2020220307182026test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220307183152test.png)

- 用双指针，而不是嵌套循环
# 3_duplicate
1. [py3func]([https://docs.python.org/3/tutorial/datastructures.html#sets](https://docs.python.org/3/tutorial/datastructures.html#sets "Linkify Plus Plus"))
2. set()的使用 add()
## 4_mergelist
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220308171648test.png)

## 5_reverselink

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220308192144test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220308195759test.png)

## 6_maxsubarray

用一个变量作为暂存值。
## 7_productExceptSelf
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220309233910test.png)

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220309234057test.png)

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310000141test.png)

这个题的解决办法是将此index两边的product计算分开

其实两个循环合并通过～来计算效率更高

## 8_maxproduct

1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310123050test.png)
   解决办法是找pattern
        1. nums是正数时，很容易解决
             2. 假如都是负数，那就需要在每一个index的地方
             留一个max和min
             再把正负数情况下的max和min列出。
             得把max或min的current数存一下，以防已经更新
### ps
- -math.inf
- [::-1] 顺序相反操作 
- [3::-1] 从下标为3开始翻转
- ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310130302test.png)
	- max里如果是两个数组的和，那就是求并集里的最大值
- [kadane's alg]([https://leetcode.com/problems/maximum-product-subarray/discuss/183483/JavaC%2B%2BPython-it-can-be-more-simple](https://leetcode.com/problems/maximum-product-subarray/discuss/183483/JavaC%2B%2BPython-it-can-be-more-simple "Linkify Plus Plus"))

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310130651test.png)

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310130701test.png)
## 9_3sum
- ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310141239test.png)
- space and time analyse TODO
- sort()
- ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310142502test.png)
pattern --> 把index作为起点，右边第一个为left pointer，右边最后一个为right pointer。
通过判断当前三个数的和与0的大小关系，来移动指针。
当duplicate时候，就continue跳过。
分两个地方: 1. 刚开始遍历。 2. sum为0时的重新开始
- [100%]([https://leetcode.com/problems/3sum/discuss/7482/Fastest-Python-solution-180-ms](https://leetcode.com/problems/3sum/discuss/7482/Fastest-Python-solution-180-ms "Linkify Plus Plus"))
- [hashmap]([https://leetcode.com/problems/3sum/discuss/415468/Python%3A-hashmap-solution-13-lines-900-ms-with-explanations](https://leetcode.com/problems/3sum/discuss/415468/Python%3A-hashmap-solution-13-lines-900-ms-with-explanations "Linkify Plus Plus"))
## 10_linklist_cycle
- ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220310233911test.png)
## 11_remove nth from end
2. TODO 
	1. head 和 dummy 什么区别
	2. ListNode(0, head)什么意思
## 12_invert binary tree
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220312115935test.png)
1. setattr(object, name, value)
## 13_maxdepth of tree
	![](photo/Pasted%20image%2020220312130815.png)
	为什么pop之后继续append 那这样不就是infi循环了
	![](photo/Pasted%20image%2020220312133333.png)
---
- 国内面试主要是牛客网。
	- 和leetcode区别在没有头代码
	- string和array比例很大。
## 14_string  vaild parentheses
stack 和 输入的s是如何连接起来的
![](photo/Pasted%20image%2020220312163710.png)
字符串不一定写成数组的形式。本身就是array
pop() --> del stack[-1]
return 语句的判断 直接 return + 语句， 不写if else

## 15_vaild palindrome
1. [::-1] reverse string
### 1st
1. renew string(清除空格 标点 --> isalnum()
2. Left pointer, Right pointer.
## 16
[https://leetcode.com/problems/longest-palindromic-substring/discuss/2925/Python-O(n2)-method-with-some-optimization-88ms](https://leetcode.com/problems/longest-palindromic-substring/discuss/2925/Python-O(n2)-method-with-some-optimization-88ms "Linkify Plus Plus").
没看懂TODO

## 17_merge
1. 这个题就正常思路解法。
2. 但首先需要排序。
## 20_grooup anagrams
1. 字符排序
2. hashmap
3. ord() --> 获取ascii
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220316195514test.png)

## 21_find min in rotated sorted array
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220319003426test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220319003440test.png)
binary search 
用res作cache 加速
每次都要留下最小值
迭代

## 22_Search in rotated sorted array 
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220319110214test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220319111800test.png)
l <=r 

## 23_reorder list
1. ![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220321211517test.png)
use 2 pointer. one is to med, one is to end.
then reverse the second.
then merge the two.

## 24_Longest Substring Without Repeating Characters
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220322112104test.png)
## 25_Longest Repeating Character Replacement
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220322125223test.png)

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220322130436test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220323001952test.png)
 利用hashmap来存储频率和值
遍历string，更新hashmap
 如果当前窗口长度和出现频率最高的值的差大于k，那就将窗口右移。左指针+1
更新result

## 26numIslands
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220323113942test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220323113950test.png)

## 27_Pacific Atlantic Water Flow
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220324151051test.png)

[graph]([https://www.youtube.com/watch?v=EgI5nU9etnU&list=PLot-Xpze53ldBT_7QA8NVot219jFNr_GI](https://www.youtube.com/watch?v=EgI5nU9etnU&list=PLot-Xpze53ldBT_7QA8NVot219jFNr_GI "Linkify Plus Plus"))
dfs --> 判断两边最大和最小的边界值。并且没被访问过。而且大于起点height。
        参数 
        1. 坐标
        2. visit 
        3. 比较值
        
        假设 m * n 
        遍历列 column
        1. 起点值 (0，c) 或 (n，c）
        反之
        （r，0）或（r,m)

## 28_clonegraph
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220324200446test.png)
没看懂题，代码比较简单。

hashmap来存放node。一个old to new的映射。

如果不在map里，就放到copy里。

再将neighbors遍历，加到copy。递归neibors的Node

# 29 
use a hashmap to store course and the pres.
recure every node of course to find if the pre can be finished.
If it can be finished, the course is done, then empty the pres.
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220325135739test.png)

## 30
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC2/2022/Pasted%20image%2020220325160546test.png)
recurse 

## 31
分3情况
1. one bigger than root, one smaller than root. root
2. two bigger --> right
3. two smaller --> left
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220325200217test.png)

## 32
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220325210248test.png)

## 33

## 34
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220326205925test.png)

## 35 Top K Frequent Elements 
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220328200943test.png)
将nums放在hashmap里。
初始化一个二维数组，来放map中的num的频率。

遍历freq中的每一个第一维，添加。
如果res等于k，返回。

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220328204319test.png)


## 36_Climbing Stairs
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220330225606test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220330225617test.png)
斐波那契的变种。
倒序，one在倒数第二个，two在倒数第一个。range 为n-1
用普通recurse超时。

## 37_House Robber
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220330233356test.png)
比较当前index的rob值和前1个的rob值大小。
当前值是n+rob1
前一个值是rob2
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220330233530test.png)

## 38_Coin Change
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220331002242test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220331002247test.png)

遍历amount从0到最大值，每个值分解为所有的coin，如果不是-1，那就每次取它记录，遍历所有得到最小值。
## 39_LONGEST CONSECUTIVE SEQUENCE

![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220404144935test.png)
先把nums去重
遍历nums，假如没有比当前值更小的，那当前值作为字符串的开头。
每次当前值+1在set中找下一个，返回最大值

## 40_Insert Interval
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220404164926test.png)
2种情况:

1. newinterval和intervals无交集。直接加到头或尾。
	1. 头 --> 直接Return
	2. 尾部 --> 继续和下一个intervals进行比较。
2. 有交集。头取min，尾取max。继续遍历。

## 41_Unique Paths
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220404174311test.png)
[hash table]([http://blog.chapagain.com.np/hash-table-implementation-in-python-data-structures-algorithms/](http://blog.chapagain.com.np/hash-table-implementation-in-python-data-structures-algorithms/ "Linkify Plus Plus"))
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220405232357test.png)
(start, stop, step)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220405232214test.png)
倒推
两个方向，横向最后row都是1，向上，当前是下和右的和。
遍历除了最后row的所有row
遍历当前row的所有column，每一个当前值都是下和右的和。
然后更新row
最后返回row[0] --> 起点

## 42_Jump Game
```
for i in range(len(num), -1, -1)
// 倒序遍历
```
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220406234003test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220406234525test.png)
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220406234531test.png)
初始化的goal是当前末尾的最后一个number
从倒数第2个开始遍历。如果当前值加上当前index无法达到goal，那就继续遍历
如果可以达到，就更新goal为当前index。

## 43_Decode Ways
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220408000558test.png)
和斐波那契相似在，它的每个值都来自之后值的和。
后序遍历，每个值赋给前一个值。
两个数的情况也很简单。但作为分支，需要加上两个数之后的cache值。
返回第一个cache值。

## 44_Word Break
![](https://cdn.jsdelivr.net/gh/h3x311/upic@main/LC3/2022/Pasted%20image%2020220408120328test.png)
类似decode，brute force是决策树。
找和wordict里符合的string
如果符合，那就把尾dp值赋给首dp值
如果dp是true，就继续倒序遍历，如果是false，那就继续下一个word认证
返回首dp值

## 45_




