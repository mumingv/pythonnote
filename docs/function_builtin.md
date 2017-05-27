# 内建函数

## 内建函数总结

###  

#### 类型/数值转换

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|type(object)               |返回给定对象的类型                     |
|int(object[, radix])       |将字符串或数字（可以提供基数）转换为整数   |
|long(object[, radix])      |将字符串或数字（可以提供基数）转换为长整型 |
|float(object)              |将字符串或数字转换为浮点数             |
|str(object)                |返回表示给定对象object的格式化好的字符串   |
|unicode(object,[ encoding[, errors]])|返回给定对象的Unicode编码版本    |
|bool(object)               |返回True或False，取决于Object的布尔值  |
|chr(number)                |返回ASCII码为给定数字的字符            |
|ord(char)                  |返回给定单字符的ASCII值                |
|list([sequence])           |构造一个列表                           |
|tuple([sequence])          |构造一个元组                           |
|zip(sequence1, ...)        |返回元组的列表                         |
|map(function, sequence, ...)|返回由给定函数function应用到所提供列表sequence每个项目时返回的值组成的列表   |
|dict([mapping-or-sequence])|构造一个字典                           |
|set([iterable])            |返回从iterable生成的不重复元素集合           |
|-                          |-                                      |
|hex(number)                |将数字转换为16进制表示的字符串         |


#### 数学计算

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|abs(number)                |返回一个数的绝对值                     |
|pow(x, y[, z])             |返回x的y次方，可选择模除z              |
|divmod(a, b)               |返回(a//b, a%b)                        |


#### 其他

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|len(object)                |返回给定对象的长度（项的个数）         |
|raw_input([prompt])        |返回给定对象的长度（项的个数）         |
|range([start, ]stop[, step])|通过一组访问器创建属性                |
|isinstance(object, classinfo)|检查对象是否为类的一个实例           |
|repr(object)               |返回表示对象的字符串                   |
|enumerate(sequence, [start=0])|返回一个带索引和数据的枚举对象      |


## 内建函数示例

###  

#### enumerate

示例：将列表转换为带索引的列表

```
>>> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
>>> list(enumerate(seasons))
[(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
```

<font color="red">
注意：直接将enumerate作用于列表，不会得到期望的结果。
</font>

```
>>> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
>>> enumerate(seasons)
<enumerate object at 0x7fd397205230>
```

示例：使用enumerate简化for循环

```python
>>> seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, seq[i]
... 
0 one
1 two
2 three
```


#### isinstance

```
obj = (1, 2, 3)
if isinstance(obj, tuple):
    print 'true'
else:
    print 'false'
```
```
true
```


#### repr

```
obj = (1, 2, 3)
print repr(obj)
```
```
(1, 2, 3)
```

#### set

示例：将字符串拆解为字符集合并计算集合的交集、并集和差集

<font color="red">
说明：生成的字符集合中没有重复元素。
</font>

```python
>>> x = set('runoob')
>>> x
set(['b', 'r', 'u', 'o', 'n'])
>>> y = set('google')
>>> y
set(['e', 'o', 'g', 'l'])
>>> x, y
(set(['b', 'r', 'u', 'o', 'n']), set(['e', 'o', 'g', 'l']))
>>> x & y
set(['o'])
>>> x | y
set(['b', 'e', 'g', 'l', 'o', 'n', 'r', 'u'])
>>> x - y
set(['r', 'b', 'u', 'n'])
```


#### zip

示例：两个列表压缩为一个，新列表中的元素为元组。 
```
>>> a = [1, 2, 3]
>>> b = [4, 5, 6, 7]
>>> zip(a, b)
[(1, 4), (2, 5), (3, 6)]
```

示例：解压元组列表，返回二维矩阵模式。

```
>>> zipped = [(1, 4), (2, 5), (3, 6)]
>>> zip(*zipped)
[(1, 2, 3), (4, 5, 6)]
```

示例：解压字符串列表，返回二维矩阵模式。

<font color="red">
结果列表中的元素个数与最短的字符串长度一致。
</font>

```
>>> strs = ['Hello world', 'Hello jay', 'Hello morning']
>>> zip(*strs)
[('H', 'H', 'H'), ('e', 'e', 'e'), ('l', 'l', 'l'), ('l', 'l', 'l'), ('o', 'o', 'o'), (' ', ' ', ' '), ('w', 'j', 'm'), ('o', 'a', 'o'), ('r', 'y', 'r')]
```




