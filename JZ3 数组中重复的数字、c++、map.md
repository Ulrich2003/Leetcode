﻿# JZ3 数组中重复的数字（使用map解决）
## 描述

在一个长度为n的数组里的所有数字都在0到n-1的范围内。 数组中某些数字是重复的，但不知道有几个数字是重复的。也不知道每个数字重复几次。请找出数组中任意一个重复的数字。 例如，如果输入长度为7的数组[2,3,1,0,2,5,3]，那么对应的输出是2或者3。存在不合法的输入的话输出-1

数据范围：
0 ≤ n ≤ 10000

```cpp
class Solution {
public:
    /**
     * 代码中的类名、方法名、参数名已经指定，请勿修改，直接返回方法规定的值即可
     *
     * 
     * @param numbers int整型vector 
     * @return int整型
     */
    int duplicate(vector<int>& numbers) {
        map<int,int> m1;
        for (int i = 0; i < numbers.size(); ++i) {
            m1[numbers[i]]++;
            if (m1[numbers[i]]!=1){
                return numbers[i];
            }
        }
        return -1;
    }
};
```

