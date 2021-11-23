#### [剑指 Offer 67. 把字符串转换成整数](https://leetcode-cn.com/problems/ba-zi-fu-chuan-zhuan-huan-cheng-zheng-shu-lcof/)

- ☑️该函数会根据需要丢弃无用的开头空格字符
- 该字符串除了有效的整数部分之后也可能会存在多余的字符，可忽略
- ☑️ 1⃣️ 假如该字符串中的第一个非空格字符不是一个有效整数字符 2⃣️ 字符串为空或字符串仅包含空白字符时，则你的函数不需要进行转换
- ☑️ 不能有效转化返回0

```javascript
/**
 * @param {string} str
 * @return {number}
 */
var strToInt = function(str) {
  var b = 1; // 1 indicates greater or equal than 0, 0 indicates smaller than 0
  var newStr = ""; // NewStr is actually a splicing integer
  var z = 0; // z is used to determind whether the first valid character is 0
  str = str.trim();
  if (str.length == 0) {
    return 0;
  }
  if (str[0] == '+') {
    b = 1;
  } else if (str[0] == '-') {
    b = 0;
  } else if (isNaN(str[0])) {
    return 0;
  }
  for (i = 0; i < str.length; i++) {
    if (i == 0 && str[i] == '+') {
      continue;
    } else if (i == 0 && str[i] == '-') {
      continue;
    }
    if (isNaN(str[i])||str[i]==' ') {
      if (b == 0) {
        newStr =  -newStr
      }
      if (newStr <= -2147483648) {
        return -2147483648;
      } else if (newStr >= 2147483647) {
        return 2147483647;
      }
      return newStr; //!!!!!
    } else {
      newStr += str[i];
    }
  }
  if (b == 0) {
    newStr =  -newStr
  }
  if (newStr <= -2147483648) {
    return -2147483648;
  } else if (newStr >= 2147483647) {
    return 2147483647;
  }
  return newStr;
};
```

⚠️ The problem encountered

**isNaN(' ') == flase**

This means ' ' is a Number

![image-20211123210427934](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211123210427934.png)

![image-20211123210534118](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211123210534118.png)