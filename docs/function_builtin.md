# 内建函数

## 内建函数列表

官方文档：https://docs.python.org/2/library/functions.html

### 

|函数        |含义                                   |
|-----------|--------------------------------------|
|abs		||
|all		||
|any 		||
|basestring	||
|bin 		||
|bool 		||
|bytearray  ||
|callable   ||
|chr 		||
|classmethod||
|cmp 		||
|compile	||
|complex 	||
|delattr	|删除对象的属性|
|dict 		||
|dir 		||
|divmod 	||
|enumerate  |生成可枚举对象|
|eval 		||
|execfile	||
|file 		||
|filter 	||
|float 		||
|format 	||
|frozenset 	||
|getattr 	|获取对象的属性|
|globals 	||
|hasattr	|检查对象的属性是否存在|
|hash 		||
|help 		||
|hex 		||
|id 		||
|input 		||
|int 		||
|isinstance |判断一个对象是否为指定类的实例对象或者是指定类的子类的实例对象|
|issubclass	|判断一个类是否为另一个类的子类或者子孙类|
|iter 		||
|len 		||
|list 		||
|locals 	||
|long 		||
|map 		||
|max 		||
|memoryview ||
|min 		||
|next 		||
|object 	||
|oct 		||
|open 		|打开文件|
|ord		||
|pow		||
|print		||
|property	||
|range		|创建列表   |
|raw_input  ||
|reduce 	||
|reload 	|重新导入模块|
|repr 		||
|reversed 	||
|round 		||
|set 		||
|setattr 	|设置一个属性。如果属性不存在，会创建一个新属性。|
|slice 		||
|sorted		||
|staticmethod||
|str 		||
|sum 		||
|super 		||
|tuple 		||
|type 		||
|unichr 	||
|unicode 	||
|vars 		||
|xrange 	||
|zip 		|压缩序列/迭代器|
|\_\_import\_\_ |NA|


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
|zip(sequence1, ...)        |压缩序列/迭代器                         |
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

### delattr

#### 示例

```
emp1 = Employee("Zara", 2000)
emp1.age = 7  # 添加一个 'age' 属性
delattr(emp1, 'age')  # 删除 'age' 属性
```


### enumerate

#### 示例：将列表转换为带索引的列表

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


#### 示例：使用enumerate简化for循环

```python
>>> seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, seq[i]
... 
0 one
1 two
2 three
```


### getattr

#### 示例

```
emp1 = Employee("Zara", 2000)
emp1.age = 7  # 添加一个 'age' 属性
print getattr(emp1, 'age')  // 7
```


### hasattr

#### 示例

```
emp1 = Employee("Zara", 2000)
emp1.age = 7  # 添加一个 'age' 属性
print hasattr(emp1, 'age')  // True
```


### id

#### 示例：打印对象的id

```
print id(obj)
```


### isinstance

#### 示例

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


### len

len可以用于一切可以计算其元素数量的对象，不仅限于元组和列表，其它类型（如：字符串、字典、集合等）都可以使用。

#### 示例：获取命令行入参的个数

```
print len(sys.argv)
```


### range

#### 示例：创建一个包含10个数字的列表

python2:

```python
>>> range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

python3:

```python
>>> range(10)
range(0, 10)
>>> list(range(10))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```


### reload

#### 示例：设置输出文件的默认编码

```
reload(sys)
sys.setdefaultencoding('utf-8')
```


### repr

#### 示例

```
obj = (1, 2, 3)
print repr(obj)
```
```
(1, 2, 3)
```


### set

#### 示例：将字符串拆解为字符集合并计算集合的交集、并集和差集

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


### setattr

#### 示例

```
emp1 = Employee("Zara", 2000)
setattr(emp1, 'age', 7)  # 添加一个 'age' 属性
```


### zip

#### 示例：两个列表压缩为一个，新列表中的元素为元组

<font color="red">
说明：结果列表中的元素个数与最短的列表长度一致。
</font>

```
>>> a = [1, 2, 3]
>>> b = [4, 5, 6, 7]
>>> zip(a, b)
[(1, 4), (2, 5), (3, 6)]
```


#### 示例：解压元组列表，返回二维矩阵模式。

```
>>> zipped = [(1, 4), (2, 5), (3, 6)]
>>> zip(*zipped)
[(1, 2, 3), (4, 5, 6)]
```

提取出原始列表：

```
>>> a, b = zip(*zipped)
>>> a
(1, 2, 3)
>>> b
(4, 5, 6)
>>> list(a)
[1, 2, 3]
>>> list(b)
[4, 5, 6]
```


#### 示例：三个列表的压缩和解压

```
>>> a = [1, 2, 3]
>>> b = [4, 5, 6]
>>> c = [7, 8, 9]
>>> zipped = zip(a, b, c)
>>> zipped
[(1, 4, 7), (2, 5, 8), (3, 6, 9)]
>> zip(*zipped)
[(1, 2, 3), (4, 5, 6), (7, 8, 9)]
>>> x, y, z = zip(*zipped)
>>> x
(1, 2, 3)
>>> y
(4, 5, 6)
>>> z
(7, 8, 9)
>>> list(x)
[1, 2, 3]
>>> list(y)
[4, 5, 6]
>>> list(z)
[7, 8, 9]
```


#### 示例：解压字符串列表，返回二维矩阵模式。

<font color="red">
说明：结果列表中的元素个数与最短的字符串长度一致。
</font>

```
>>> strs = ['Hello world', 'Hello jay', 'Hello morning']
>>> zip(*strs)
[('H', 'H', 'H'), ('e', 'e', 'e'), ('l', 'l', 'l'), ('l', 'l', 'l'), ('o', 'o', 'o'), (' ', ' ', ' '), ('w', 'j', 'm'), ('o', 'a', 'o'), ('r', 'y', 'r')]
```




