#### [剑指 Offer II 004. 只出现一次的数字 ](https://leetcode-cn.com/problems/WGki4K/)

给你一个整数数组 `nums` ，除某个元素仅出现 **一次** 外，其余每个元素都恰出现 **三次 。**请你找出并返回那个只出现了一次的元素。

![image-20211226003444627](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211226003444627.png)

该题属于简单题，用到的知识点是Map，三目运算符（非必要知识点）

##### AC代码：

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var singleNumber = function(nums) {
    let numsMap = new Map;
    for (let key in nums){
        numsMap.set(nums[key],numsMap.get(nums[key])===undefined?1:numsMap.get(nums[key])+1);
    }
    let result; // 存放返回结果
    numsMap.forEach(function (value,key) {
        if (value==1){
            result =  key;
        }
    })
    return result;
};
```

