# 剑指 Offer 11. 旋转数组的最小数字

**题目：**
把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。

给你一个可能存在 重复 元素值的数组 numbers ，它原来是一个升序排列的数组，并按上述情形进行了一次旋转。请返回旋转数组的最小元素。例如，数组 [3,4,5,1,2] 为 [1,2,3,4,5] 的一次旋转，该数组的最小值为1。  
[来源：力扣（LeetCode）](https://leetcode-cn.com/problems/xuan-zhuan-shu-zu-de-zui-xiao-shu-zi-lcof)
![在这里插入图片描述](https://img-blog.csdnimg.cn/127a87a69dbb45b4bcf4a86e55885881.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAQ2h1YW5ZYW5nIENoZW4=,size_20,color_FFFFFF,t_70,g_se,x_16)


**✅ 运行结果：**
![在这里插入图片描述](https://img-blog.csdnimg.cn/12c77182efdf4b79b3be27e45f600756.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAQ2h1YW5ZYW5nIENoZW4=,size_20,color_FFFFFF,t_70,g_se,x_16)
**解题思路：**
一开始感觉这题挺考察我语文水平的，但抓住题目中的「原来是一个**升序排列**的数组，并按上述情形进行了**一次**旋转」，猜是只要遍历一遍出现不是增序的数字就是最小的数了。

**AC代码：**

```javascript
/**
 * @param {number[]} numbers
 * @return {number}
 */
var minArray = function(numbers) {
    let min = numbers[0];
    for (let i in numbers){
        if (numbers[i] < min){
            return numbers[i];
        }else {
            min = numbers[i];
        }
    }
    return numbers[0];
};
```

