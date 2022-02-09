# 剑指 Offer 05. 替换空格![在这里插入图片描述](https://img-blog.csdnimg.cn/7da3aa66f96c4a3a9e39efb883c65a5f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAQ2h1YW5ZYW5nIENoZW4=,size_20,color_FFFFFF,t_70,g_se,x_16)
##### 题目：
请实现一个函数，把字符串 s 中的每个空格替换成"%20"。
![在这里插入图片描述](https://img-blog.csdnimg.cn/c9bd735edff74a9496f06364e8f4884d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAQ2h1YW5ZYW5nIENoZW4=,size_20,color_FFFFFF,t_70,g_se,x_16)

##### 解题思路：
JS中的`replace()`函数配合正则表达式进行全局搜索替换

正则表达式 + replace使用方法我的另外一篇文章有：
[JS中正则表达式配合split()，search()，match()，replace()](https://blog.csdn.net/weixin_45525653/article/details/122797818?spm=1001.2014.3001.5501)
##### AC代码：

```javascript
var replaceSpace = function(s) {
    return s.replace(/ /g,'%20');
};
```

