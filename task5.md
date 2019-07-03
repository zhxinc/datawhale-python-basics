# 「python」基础 task5
## **类**和**对象**
变量分为几个不同的**类**。类代表这个对象可以进行操作以及可能的值。

要获知变量的类可以使用type()函数，但更加好用的是isinstance()函数，因为它支持继承，也就是可以判断子类（比如str和unicode都是basestring的子类）。一个常见的应用是这样：

```python
if isinstance(x, basestring)
    return treatasscalar(x)
try:
    return treatasiter(iter(x))
except TypeError:
    return treatasscalar(x)
```
python中的信息全部都是以**对象**的形式保存，不管是python内部的对象或是我们自己建立的对象。基本上就是一段储存空间，里面存放着值和相关的运算法则。

## 正则表达式

正则表达式（Regular Expression）可以用来判断某个字符串是否包含某种特征。

re模块：```import re```

```python
import re

#Check if the string starts with "The" and ends with "Spain":

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)

if (x):
  print("YES! We have a match!")
else:
  print("No match")
```
### re模块包含的函数

|函数|功能|
|---|----|
|findall|返回所有符合条件的字符串所构成的列表|
|search|如果能成功匹配，就返回一个「匹配对象」|
|split|返回被切分后的字符串形成的列表|
|sub|将匹配的结果用某个字符串替换|

### 有特殊意义的字符（metacharacters）
|字符|含义|例子|
|----|----|--|
|[]|一系列字符|"[a-m]"|
|\\|表示一个特殊序列（也可以用于消除特殊字符）|"\d"|
|.|代表任意字符（换行符除外）|"he..o"|
|^|以...开始|“^hello”|
|$|以...结束|“world$”|
|*|出现任意次|"aix*"|
|+|至少出现一次|"aix+"|
|{}|出现特定次数|"al{2}"|
|\||或者|"falls|stays"|

[W3C school](https://www.w3schools.com/python/python_regex.asp)

[google教程](https://developers.google.com/edu/python/regular-expressions)

## http请求
是HTTP中所定义的，在某一给定来源进行某种操作的一些请求。
|请求名称|用途|
|----|---|
|GET|请求指定的页面信息|
|HEAD|类似于GET但返回中没有具体内容|
|POST|向指定资源提交数据进行处理请求，通常会导致服务器中的状态变化|
|PUT|从客户端向服务器传送的数据取代指定文档的内容|
|DELETE|请求服务器删除指定页面|
|OPTIONS|查看服务器的性能|
