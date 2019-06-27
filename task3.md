## 字典 dict

### 定义
一种可变容器模型，可存储任意类型的对象。
使用键-值存储(key-value)，查找速度极快。

### 创建

	d = {key1 : value1, key2:value2}
键一般是唯一的，而值不需要唯一。 为同一个键赋不同的值以最后一次为准。值可以取任何数据类型，而键必须是不可变的（比如字符串、数字、元组）

### 字典的有关使用方法
#### 访问

	print(dict['Name'])

#### 更新与添加

	dict['Name'] = alice

#### 删除

	del dict['Name'] #删除一个key-value条目
	dict.clear()     #清空整个字典
	del dict         #删除字典
#### 其他内置函数
| 函数 | 描述 |
| ---- | ----|
|  ||

## 集合 set
### 特性

和dict类似，也是一组键的集合，但并不储存值。由于key不能重复，所以在set中没有重复的键。

### 创建
需要提供一个list作为输入集合。

	s = set([1, 2, 3])

重复元素会自动被过滤。

	s.add(4)

可以添加元素。

	s.remove(4)

可以删除元素。

### 方法

可以做一些数学运算，如```s1 & s2``` ```s1|s2``` 等。

## 判断语句

- 多条件判断
- 
		if a and b:
    	if a or b:
		if not a xor b:
		elif a == 2:

## 三目表达式
	a = 1
	b = 2
	h = ""
	h = a-b if a>b else a+b
	print(h)
如果符合前一个条件，就赋为前面那个值否则赋为后面那个值。

## 循环语句
	while i < n:
	for i in range(1, 10):
		print(i)