---
title: "Leetcodenote"
date: 2022-05-25T19:32:00+08:00
draft: false
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
> [14 patterns](https://hackernoon.com/14-patterns-to-ace-any-coding-interview-question-c5bb3357f6ed)
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
- [pythonFunc](https://docs.python.org/3/library/functions.html#enumerate)
- [python格式](https://pep8.org/)
- [blind75list](https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-100-LeetCode-Questions-to-Save-Your-Time-OaM1orEU)
- [# Short-circuit evaluation](https://en.wikipedia.org/wiki/Short-circuit_evaluation)

- draw pic
- use pattern structure
- test your knowledge

# 1_twosum

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220307105831.png?token=AJNWEYOIZ5NQREMSGV6NMNLCRYIKG)
### hash table
1. key - val
	1. key - unique
		1. 多对一的关系。
# 2_maxprofig

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220307182026.png?token=AJNWEYMXUFX4TQQKKUVI7K3CRYIKW)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220307183152.png?token=AJNWEYOBBJNW34IQURVMSADCRYILO)

- 用双指针，而不是嵌套循环
# 3_duplicate
1. [py3func](https://docs.python.org/3/tutorial/datastructures.html#sets)
2. set()的使用 add()
## 4_mergelist

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220308171648.png?token=AJNWEYNYSUN4SR5XDANFP4DCRYIL6)

## 5_reverselink
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220308192144.png?token=AJNWEYKRNNHPXFS52UF5JZLCRYINQ)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220308195759.png?token=AJNWEYMWKRRAZPMDVW5PZODCRYIOO)

## 6_maxsubarray
用一个变量作为暂存值。
## 7_productExceptSelf

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220309233910.png?token=AJNWEYLSD55TTGAP5CVHFKLCRYIO4)

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc/Pasted%2520image%252020220309234057.png?token=AJNWEYNPBWOTQR6ZYSZXI33CRYIPM)

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310000141.png?token=AJNWEYOGAPWVHEJUDO32BSDCRYIYA)

这个题的解决办法是将此index两边的product计算分开

其实两个循环合并通过～来计算效率更高

## 8_maxproduct
1. ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310123050.png?token=AJNWEYOSTABLAKTK3LSXPCLCRYIYY)
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
- ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310130302.png?token=AJNWEYIIPMZQEDUD7XCWFODCRYIZI)
	- max里如果是两个数组的和，那就是求并集里的最大值
- [kadane's alg](https://leetcode.com/problems/maximum-product-subarray/discuss/183483/JavaC%2B%2BPython-it-can-be-more-simple)

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310130651.png?token=AJNWEYJMKHZ73HTO2CJVTYLCRYIZU)

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310130701.png?token=AJNWEYKID5MEQOIHTFIWGRLCRYI2I)
## 9_3sum
- ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310141239.png?token=AJNWEYNQL5T2HKDV5HYQSBDCRYI4K)
- space and time analyse TODO
- sort()
- ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310142502.png?token=AJNWEYJSZ7TIYR5BXZWFGW3CRYI44)
pattern --> 把index作为起点，右边第一个为left pointer，右边最后一个为right pointer。
通过判断当前三个数的和与0的大小关系，来移动指针。
当duplicate时候，就continue跳过。
分两个地方: 1. 刚开始遍历。 2. sum为0时的重新开始
- [100%](https://leetcode.com/problems/3sum/discuss/7482/Fastest-Python-solution-180-ms)
- [hashmap](https://leetcode.com/problems/3sum/discuss/415468/Python%3A-hashmap-solution-13-lines-900-ms-with-explanations)
## 10_linklist_cycle
- ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220310233911.png?token=AJNWEYJVBM446TPNVSVV6RTCRYI5O)
## 11_remove nth from end
2. TODO 
	1. head 和 dummy 什么区别
	2. ListNode(0, head)什么意思
## 12_invert binary tree
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220312115935.png?token=AJNWEYNARSY27NJNCPDQU33CRYI6G)
1. setattr(object, name, value)
## 13_maxdepth of tree
![Hxy3ze](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Hxy3ze.jpg?token=AJNWEYOGTIXFJ5MCXEZU42DCRYKP4)
	为什么pop之后继续append 那这样不就是infi循环了
	![38cK4Q](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/38cK4Q.png?token=AJNWEYM6N5O4QNT6HAD5NL3CRYKRQ)
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
https://leetcode.com/problems/longest-palindromic-substring/discuss/2925/Python-O(n2)-method-with-some-optimization-88ms.
没看懂TODO

## 17_merge
1. 这个题就正常思路解法。
2. 但首先需要排序。
## 20_grooup anagrams
1. 字符排序
2. hashmap
3. ord() --> 获取ascii
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220316195514.png?token=AJNWEYNPO4FBQRFFMM4H47TCRYI74)

## 21_find min in rotated sorted array

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220319003426.png?token=AJNWEYPWUHWYQHUANT26DETCRYJAW)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220319003440.png?token=AJNWEYLJC2NL3K24EONGVADCRYJCG)
binary search 
用res作cache 加速
每次都要留下最小值
迭代

## 22_Search in rotated sorted array

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220319110214.png?token=AJNWEYLVTT3Y2IEH2JBEDZLCRYJD6)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc1/Pasted%2520image%252020220319111800.png?token=AJNWEYPAVAAWOLYT5UEBS63CRYJFI)
l <=r 

## 23_reorder list
1. ![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220321211517.png?token=AJNWEYI7GTKDNDO5O2VRFELCRYJL2)
use 2 pointer. one is to med, one is to end.
then reverse the second.
then merge the two.

## 24_Longest Substring Without Repeating Characters
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220322112104.png?token=AJNWEYNSDLKU67C7UERDCMLCRYJMM)
## 25_Longest Repeating Character Replacement
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220322125223.png?token=AJNWEYNYQDA6RRV3V5VXCJDCRYJM6)

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220322130436.png?token=AJNWEYPIW466IDAIQOYYZITCRYJNU)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220323001952.png?token=AJNWEYJXA32ZF5AQTSQVFLDCRYJOK)
 利用hashmap来存储频率和值
遍历string，更新hashmap
 如果当前窗口长度和出现频率最高的值的差大于k，那就将窗口右移。左指针+1
更新result

## 26numIslands

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220323113942.png?token=AJNWEYMUG2KC7CYLIT2Y2NTCRYJQO)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220323113950.png?token=AJNWEYLYMZAQ4D3DEHR7W6TCRYJRC)

## 27_Pacific Atlantic Water Flow
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220324151051.png?token=AJNWEYKXWO5H3GJ5WGLMBU3CRYJRU)

[graph](https://www.youtube.com/watch?v=EgI5nU9etnU&list=PLot-Xpze53ldBT_7QA8NVot219jFNr_GI)
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
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220324200446.png?token=AJNWEYKAHRELNBLWZYAINNLCRYJSK)
没看懂题，代码比较简单。

hashmap来存放node。一个old to new的映射。

如果不在map里，就放到copy里。

再将neighbors遍历，加到copy。递归neibors的Node

# 29 
use a hashmap to store course and the pres.
recure every node of course to find if the pre can be finished.
If it can be finished, the course is done, then empty the pres.
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220325135739.png?token=AJNWEYODAAB3U4FNQNO4IK3CRYJTE)

## 30
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220325160546.png?token=AJNWEYPS3UQX5VL7SOW3TOLCRYJTY)
recurse 

## 31
分3情况
1. one bigger than root, one smaller than root. root
2. two bigger --> right
3. two smaller --> left
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220325200217.png?token=AJNWEYP3IF4EE5KFYZOEALLCRYJUO)

## 32
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220325210248.png?token=AJNWEYN3E44YTHOQOZV74QDCRYJU6)

## 33

## 34
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220326205925.png?token=AJNWEYISJHL57YDMHX3KMW3CRYJVO)

## 35 Top K Frequent Elements 
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220328200943.png?token=AJNWEYJOVFUBP2D4KASROKTCRYJWG)
将nums放在hashmap里。
初始化一个二维数组，来放map中的num的频率。

遍历freq中的每一个第一维，添加。
如果res等于k，返回。

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc2/Pasted%2520image%252020220328204319.png?token=AJNWEYKTVD2ZD4ZDQFZFXF3CRYJWY)


## 36_Climbing Stairs
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220330225606.png?token=AJNWEYJQTN4QOL27VKVR3PTCRYJ4C)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220330225617.png?token=AJNWEYJE5IG3XZACJNTCPQTCRYJ4O)
斐波那契的变种。
倒序，one在倒数第二个，two在倒数第一个。range 为n-1
用普通recurse超时。

## 37_House Robber
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220330233356.png?token=AJNWEYKTZDPHRH4UQLCOODLCRYJ5E)
比较当前index的rob值和前1个的rob值大小。
当前值是n+rob1
前一个值是rob2
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220330233530.png?token=AJNWEYMRIF453N4FOGAQ2OLCRYJ5W)

## 38_Coin Change
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220331002242.png?token=AJNWEYINJJYZ43BI2MJWTI3CRYJ74)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220331002247.png?token=AJNWEYJEMPO47UNTXABJ7ZLCRYKA4)

遍历amount从0到最大值，每个值分解为所有的coin，如果不是-1，那就每次取它记录，遍历所有得到最小值。
## 39_LONGEST CONSECUTIVE SEQUENCE

![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220404144935.png?token=AJNWEYPGS3CGDHCATH4OKILCRYKB2)
先把nums去重
遍历nums，假如没有比当前值更小的，那当前值作为字符串的开头。
每次当前值+1在set中找下一个，返回最大值

## 40_Insert Interval
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220404164926.png?token=AJNWEYMNOTEIAHBIUIUHPCDCRYKCM)
2种情况:

1. newinterval和intervals无交集。直接加到头或尾。
	1. 头 --> 直接Return
	2. 尾部 --> 继续和下一个intervals进行比较。
2. 有交集。头取min，尾取max。继续遍历。

## 41_Unique Paths
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220404174311.png?token=AJNWEYK6HOOMSWZEJP6BSGTCRYKC4)
[hash table](http://blog.chapagain.com.np/hash-table-implementation-in-python-data-structures-algorithms/)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220405232357.png?token=AJNWEYNYDN4ZRJP46OIRZODCRYKDM)
(start, stop, step)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220405232214.png?token=AJNWEYLAI2LJOCHPCB5UWXLCRYKEE)
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
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220406234003.png?token=AJNWEYPKMT3VFZ3ARMWNHLLCRYKE6)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220406234525.png?token=AJNWEYIGQBMTESOFTQLWERTCRYKFM)
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220406234531.png?token=AJNWEYO7DYEXQNKB4PJNPTTCRYKGA)
初始化的goal是当前末尾的最后一个number
从倒数第2个开始遍历。如果当前值加上当前index无法达到goal，那就继续遍历
如果可以达到，就更新goal为当前index。

## 43_Decode Ways
![](https://raw.githubusercontent.com/zerone0x/upic/main/lc3/Pasted%2520image%252020220408000558.png?token=AJNWEYKLJUGYVUYFEZWYP5DCRYKG4)
和斐波那契相似在，它的每个值都来自之后值的和。
后序遍历，每个值赋给前一个值。
两个数的情况也很简单。但作为分支，需要加上两个数之后的cache值。
返回第一个cache值。

## 44_Word Break

![](photo/Pasted%20image%2020220408120328.png)
类似decode，brute force是决策树。
找和wordict里符合的string
如果符合，那就把尾dp值赋给首dp值
如果dp是true，就继续倒序遍历，如果是false，那就继续下一个word认证
返回首dp值

## 45_


