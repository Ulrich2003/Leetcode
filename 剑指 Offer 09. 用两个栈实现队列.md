#### [剑指 Offer 09. 用两个栈实现队列](https://leetcode-cn.com/problems/yong-liang-ge-zhan-shi-xian-dui-lie-lcof/)

题目：

用两个栈实现一个队列。队列的声明如下，请实现它的两个函数 appendTail 和 deleteHead ，分别完成在队列尾部插入整数和在队列头部删除整数的功能。(若队列中没有元素，deleteHead 操作返回 -1 )

测试用例：

![image-20211222105611958](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211222105611958.png)

AC代码：

```javascript
var CQueue = function() {
    this.queue = new Array();
};

/**
 * @param {number} value
 * @return {void}
 */
CQueue.prototype.appendTail = function(value) {
    this.queue.push(value);
};

/**
 * @return {number}
 */
CQueue.prototype.deleteHead = function() {
    let deleted;
    if (this.queue.length==0){
        return -1;
    }else {
        deleted = this.queue[0];
        this.queue.splice(0,1);
    }
    return deleted;
};
```

运行结果：

![image-20211222105519476](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211222105519476.png)

