---
title: 「python基础」task2
date: 2019-06-22 23:02:16
tags:
- python
---
列表、元组和字符串是python中常见的数据结构，它们的共同点是都储存了有序的对象。字符串只能包含字符，而列表和元组则可以含有各种类型的对象。列表和元组比较像数组。元组与字符串一样，是不能修改的（immutable）。而列表则可以随意增长或者缩短。

## 列表 lists

### 标志

用中括号表示。

```l = [1, 2, "a"]```


### 基本操作

```python
>>> l = [1, 3, 3]
>>> l[0]
1
>>> l.append(1)
>>> l
[1, 3, 3, 1]
>>> l.append([1, 2, 3])
>>> l
[1, 3, 3, 1, [1, 2, 3]]
>>> l.append(1, 2, 3)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: append() takes exactly one argument (3 given)
>>> l.extend([1, 2, 3])
>>> l
[1, 3, 3, 1, [1, 2, 3], 1, 2, 3]
>>> l.index(1)
0
>>> l.index(1,2)
3
>>> l.insert(2,'c')
>>> l
[1, 3, 'c', 3, 1, [1, 2, 3], 1, 2, 3]
>>> l.remove([1, 2, 3])
>>> l
[1, 3, 'c', 3, 1, 1, 2, 3]
>>> l.pop()
3
>>> l
[1, 3, 'c', 3, 1, 1, 2]
>>> l.count(1)
3
>>> l.sort()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: '<' not supported between instances of 'str' and 'int'
>>> l.remove('c')
>>> l.sort()
>>> l
[1, 1, 1, 2, 3, 3]
>>> l.sort(reverse=True)
>>> l
[3, 3, 2, 1, 1, 1]
>>> l.reverse()
>>> l
[1, 1, 1, 2, 3, 3]
>>> l += [4, 5, 6]
>>> l
[1, 1, 1, 2, 3, 3, 4, 5, 6]
>>> l *= 2
>>> l
[1, 1, 1, 2, 3, 3, 4, 5, 6, 1, 1, 1, 2, 3, 3, 4, 5, 6]
>>> l[10:]
[1, 1, 2, 3, 3, 4, 5, 6]
>>> l[:10]
[1, 1, 1, 2, 3, 3, 4, 5, 6, 1]
>>> l[11:-4]
[1, 2, 3]
>>> l[::5]
[1, 3, 1, 4]
>>> [i for i in range(10) if i % 2 == 0]
[0, 2, 4, 6, 8]
>>> li = [1, 2]
>>> [elem*2 for elem in li if elem>1]
[4]
>>> l.pop(0)
1
>>> 
```

## 元组 turples

### 标志

用小括号表示.

```t = (1, 2, "a")```
### 基本操作

```python
>>> l = (1, 2, 3)
>>> l[0]
1
>>> l = 1, 2
>>> l
(1, 2)
>>> (1, )*5
(1, 1, 1, 1, 1)
>>> s1 = 1,0
>>> s1 += 1,
>>> s1
(1, 0, 1)
>>> s1.count(1)
2
>>> s1.index(0)
1
>>> s1.pop()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'tuple' object has no attribute 'pop'
>>> x = 1, y = 2
  File "<stdin>", line 1
SyntaxError: can't assign to literal
>>> x , y = 1, 2
>>> x, y = y, x
>>> x
2
>>> y
1
>>> len(s1)
3
>>> str(s1)
'(1, 0, 1)'
>>> s1
(1, 0, 1)
>>> s1 = 1, 3, 2
>>> max(s1)
3
```

## 字符串 strings
```python
>>> text = """a string with special character " and ' inside."""
>>> text
'a string with special character " and \' inside.'
>>> u"\u0041"
'A'
>>> r" \textbf{this is bold text in LaTeX} "
' \\textbf{this is bold text in LaTeX} '
>>> print("%s" % "some text")
some text
>>> print ("this is a percent sign: %%")
this is a percent sign: %%
>>> "{a}!={b}".format(a=2,b=1)
'2!=1'
>>> t = 'This is a test'
>>> t2 = t+ t
>>> t2
'This is a testThis is a test'
>>> t3 = t*3
>>> t3
'This is a testThis is a testThis is a test'
>>> "Zhxinc".istitle()
True
>>> t3.count('s')
9
>>> len(t3)
42
>>> t3.title()
'This Is A Testthis Is A Testthis Is A Test'
>>> t3.capitalize()
'This is a testthis is a testthis is a test'
>>> t3.lower()
'this is a testthis is a testthis is a test'
>>> t3.rjust(30, '-')
'This is a testThis is a testThis is a test'
>>> t3.zfill(30)
'This is a testThis is a testThis is a test'
>>> 
```