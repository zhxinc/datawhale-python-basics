# [python]基础 task4
## 函数
### 函数是什么

函数是只有在被调用时才会运行的代码块。可以将数据（参数）传入一个函数中，函数也可以将数据作为返回结果。

### 定义函数
    def my_function():
        print("Hello from a function")

以冒号结尾，函数内部的代码块要缩进。

### 调用一个函数
    my_function()

### 参数

传入函数的信息叫做参数，参数的数量可以有任意多个。

```python
    def my_function(fname):
        print(fname + " Refsnes")

    my_function("Emil")
    my_function("Tobias")
    my_function("Linus")
```

- 默认参数值

```python
    def my_function(country = "Norway")
        print("I am from " + country)

    my_function("Sweden")
    my_function("India")
    my_function()
    my_function("Brazil")
```
### 返回值

```python
    def my_function(x):
       return 5 * x

    print(my_function(3))
    print(my_function(5))
    print(my_function(9))
```
### 作用域

变量分为局部变量和全局变量。定义在函数内部的变量只能在其被声明的函数中访问，而全局变量可以在整个程序范围内访问。

## 文件操作

### open()函数

```python
    f = open('workfile', 'w')
    #open(filename, mode)
```
mode一般有r/w/r+/a。（读/写/读+写/附加）

### 文件的常用操作
    f.read()
    f.readline()
    for line in f:
        print(line, end='')
    f.write(string)
    #非字符串的值需要先转换为字符串再写入。

### 读取csv和excel

    import pandas as pd
    df = pd.read_excel('filename.xlsx')
    df = pd.read_csv('filename.csv')
    df.to_csv('filename.csv')
    df.to_excel('filename.xlsx')

[csv](https://realpython.com/python-csv/#where-do-csv-files-come-from)

[excel](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html)

## 模块
### os
    # 查看当前目录的绝对路径:
    >>> os.path.abspath('.')
    '/Users/michael'
    # 在某个目录下创建一个新目录，
    # 首先把新目录的完整路径表示出来:
    >>> os.path.join('/Users/michael', 'testdir')
    '/Users/michael/testdir'
    # 然后创建一个目录:
    >>> os.mkdir('/Users/michael/testdir')
    # 删掉一个目录:
    >>> os.rmdir('/Users/michael/testdir')
[os](https://www.liaoxuefeng.com/wiki/897692888725344/923055916315360)

### datetime
    >>> from datetime import datetime
    >>> now = datetime.now() # 获取当前datetime
    >>> print(now)
    2015-05-18 16:28:07.198690
    >>> print(type(now))
    <class 'datetime.datetime'>
[datetime](https://www.liaoxuefeng.com/wiki/1016959663602400/1017648783851616)