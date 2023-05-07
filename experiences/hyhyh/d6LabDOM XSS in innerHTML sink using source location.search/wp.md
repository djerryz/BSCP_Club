# 题意
![](pic/6-3.png)

与上一题基本一致，只不过sink有所不同，用的是innerHTML属性，它能返回表格行开始和结束标签之间的html。
# 解题思路
step1:打开开发者模式查看源码
![](pic/dev.png)


step2:输入payload
```
<img src=1 onerror=alert(1)>
```
src的值不合法然后抛出异常触发onerror，onerror调用alert()


# 知识点