# 217. 存在重复元素

## 题目描述
[217. 存在重复元素](https://leetcode.cn/problems/contains-duplicate/)
```
给你一个整数数组 nums 。如果任一值在数组中出现 至少两次 ，返回 true ；如果数组中每个元素互不相同，返回 false 。
示例 1：
输入：nums = [1,2,3,1] 输出：true
示例 2：
输入：nums = [1,2,3,4] 输出：false
示例 3：
输入：nums = [1,1,1,3,3,4,3,2,4,2] 输出：true
```
## Java
- 使用HashMap求解
- 思路：创建一个哈希表，判断数值在哈希表中是否存在，若不存在，将该数值放入哈希表；若存在则说明数值重复，返回真
```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        int n=nums.length;
        HashMap<Integer, Integer> hashmap = new HashMap<Integer, Integer>();
        for(int i=0;i<n;i++){
            if(hashmap.containsKey(nums[i])){
                return true;
            }
            hashmap.put(nums[i],i)
        }
        return false;
    }
}
// 作者：lemonsi-c
// 链接：https://leetcode.cn/problems/contains-duplicate/solution/by-lemonsi-c-4tca/
```

