#### [剑指 Offer 10- I. 斐波那契数列](https://leetcode-cn.com/problems/fei-bo-na-qi-shu-lie-lcof/)

❌do not pass

```javascript
/**
 * @param {number} n
 * @return {number}
 */
var fib = function(n) {
  if(n==0){
    return 0;
  }
  if(n==1){
    return 1;
  }
  return (fib(n-1)+fib(n-2))%1000000007
};
```

Cause: There is no optimized recursive algorithm, the program times out

Fix the algorithm：

![image-20211122163303945](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211122163303945.png)

```javascript
var record = new Array(0,1);
var fib = function(n) {
  if(record[n]!=undefined){
    return record[n];
  }
  if (n == 0) {
    return 0;
  }
  if (n == 1) {
    return 1;
  }
  record[n] =  (fib(n - 1) + fib(n - 2)) % 1000000007;
  return record[n];
};
```

![image-20211122165646271](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211122165646271.png)

