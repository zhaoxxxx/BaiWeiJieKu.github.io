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



### 移除元素

```
给定一个排序数组，你需要在原地删除重复出现的元素，使得每个元素只出现一次，返回移除后数组的新长度。
不要使用额外的数组空间，你必须在原地修改输入数组并在使用 O(1) 额外空间的条件下完成。
```

```
给定数组 nums = [1,1,2], 

函数应该返回新的长度 2, 并且原数组 nums 的前两个元素被修改为 1, 2。 

你不需要考虑数组中超出新长度后面的元素。
```

```
给定 nums = [0,0,1,1,1,2,2,3,3,4],

函数应该返回新的长度 5, 并且原数组 nums 的前五个元素被修改为 0, 1, 2, 3, 4。

你不需要考虑数组中超出新长度后面的元素。
```



#### 方法一

```java
利用双指针遍历数组

class Solution {
    public int removeDuplicates(int[] nums) {
        if(nums.length<=0) {
            return 0;
        }
        int mov=0; //赋值指针指针
        int res=1; //统计不重复元素的个数
        for(int i=0;i<nums.length;i++) { //i相当于移动指针
            if(nums[mov]==nums[i]) {
                continue; //两个指针从数组第一个元素开始比较，如果相同，跳过本次循环
            }else {
                mov++; //当两个指针指的位置元素不相等就表示是一个新元素
                nums[mov]=nums[i]; //把赋值指针向后移动一位，把新元素赋值给赋值指针位置
                res++; //元素个数加一
            }
        }
        return res;
    }
}
```

```
时间复杂度：O(n)， 假设数组的长度是 nn，那么 ii 和 jj 分别最多遍历 nn 步。
空间复杂度：O(1)。
```

```
nums = [0,0,1,1,1,2,2,3,3,4]

第一次mov=0,i=0  两个位置都是0且元素相等，
第二次mov=0,i=1  两个位置都是0且元素相等,
第三次mov=0,i=2  0!=1,所以mov++,mov=1,nums[mov]=nums[i],res=2
第四次mov=1,i=3  两个位置都是1且元素相等,
.
.
.
```

