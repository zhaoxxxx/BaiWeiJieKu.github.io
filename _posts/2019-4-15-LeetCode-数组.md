---
layout: post
title: "LeetCode-数组"
categories: LeetCode
tags: LeetCode 数组
author: 百味皆苦
music-id: 2602106546
---

* content
{:toc}
### 两数之和

```
给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那两个整数，并返回他们的数组下标。
你可以假设每种输入只会对应一个答案。但是，你不能重复利用这个数组中同样的元素。

示例:
给定 nums = [2, 7, 11, 15], target = 9
因为 nums[0] + nums[1] = 2 + 7 = 9
所以返回 [0, 1]
```



#### 方法一

```java
//从数组两端开始遍历
//时间复杂度O（n^2）
//对于每个元素，我们试图通过遍历数组的其余部分来寻找它所对应的目标元素,耗时O(1)
//空间复杂度：O（1）

class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int head=0;head<nums.length-1;head++ )
        {
            for(int tail=nums.length-1;tail>head;tail--)
            {
                if(nums[head]+nums[tail]==target){
                    return new int[]{head,tail};
                }
            }
        }
		return new int[]{};
    }
}
```



#### 方法二

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer,Integer> map = new HashMap();
        for(int i=0;i<nums.length;i++) {
            //用目标值减数组元素，查看map中是否有这个键
            if(map.containsKey(target-nums[i]))
                return new int[]{i,map.get(target-nums[i])};
            map.put(nums[i],i);
        }
        return new int[]{};
    }
}
//第一次target=9，target-2=7，map中没有这个键，把值和索引装入map中，形成（2：0）
//第二次target-7=2，map中有2这个键，返回i和键2所对应的的值[0,1]
```

```
利用map键值对，键为数组元素，值为数组索引
键   2   7   11   15
值   0   1   2    3
```

```
一遍哈希表
事实证明，我们可以一次完成。在进行迭代并将元素插入到表中的同时，我们还会回过头来检查表中是否已经存在当前元素所对应的目标元素。如果它存在，那我们已经找到了对应解，并立即将其返回。
时间复杂度：O(n)
空间复杂度：O（n）
```

