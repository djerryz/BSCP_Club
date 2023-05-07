# 题意
![](pic/11-3.png)
与上一题一样，也是搜索功能有XSS漏洞，并且尖括号被编码。利用漏洞唤起alert()即可。
# 解题思路
step1:
输入测试字符串123abc>
![](pic/test.png)
可以看到>被编码。

step2:
尝试跳出单引号：
![](pic/dev.png)

![](pic/dev1.png)

可以看到两种方法都成功跳出了单引号。

step3:
输入payload
```
';-alert(1)//

'-alert(1)-'
```

两种都可以

![](pic/res.png)

![](pic/res1.png)
# 知识点