

####  [剑指 Offer 03. 数组中重复的数字](https://leetcode-cn.com/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/)

```c++
#include <iostream>
#include "set"
#include "vector"

using namespace std;

int findRepeatNumber(vector<int>& nums) {
    set<int>s;
    for (int i = 0; i < nums.size(); ++i) {
        if (s.count(nums[i])){
            return nums[i];
        } else{
            s.insert(nums[i]);
        }
    }
}

int main() {
    vector<int>v = {2,3,1,0,2,5,3};
    cout<<findRepeatNumber(v);
}


```

Some problems encountered during the exercise：

![image-20211202103709029](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211202103709029.png)

![image-20211202103818424](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211202103818424.png)

##### Then I tried to translate the cpp code into JS

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var findRepeatNumber = function(nums) {
    const s = new Set();
    for (let i = 0; i < nums.length; i++){
        if (s.has(nums[i])){
            return nums[i];
        }else {
            s.add(nums[i]);
        }
    }
    return 0;
};
```

![image-20211202112929613](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211202112929613.png)