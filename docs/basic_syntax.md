# 基本语法

## 注释

单行注释，使用Shell风格的注释。

```
# ...
```

多行注释：使用一对'''(三个单引号)，或者使用一对"""(三个双引号)包含注释信息

```python
'''
comment...
'''
```

```python
"""
comment...
"""
```


## 类型


## 变量


## 函数

###  

#### 函数定义与调用

```python
def hello(name):
    return 'Hello, ' + name + '!';
print hello('Jay');
```
```python
Hello, Jay!
```


#### 位置参数收集

```python
def printPositionParams(*params):
    print params

printPositionParams(1, 2, 3)
```
```python
(1, 2, 3)
```


#### 关键字参数收集

```python
def printKeywordParams(**params):
    print params

printKeywordParams(foo = 1, bar = 2, test = 3)
```
```python
{'test': 3, 'foo': 1, 'bar': 2}
```


#### 混合参数收集

```python
def printCompoundParams(title, *posParams, **keyParams):
    print title
    print posParams
    print keyParams

printCompoundParams('Params test:', 1, 2, 3, foo = 4, bar = 5, test = 6)
```
```python
Params test:
(1, 2, 3)
{'test': 6, 'foo': 4, 'bar': 5}
```


#### 调用函数时使用元组作为实参

```python
def add(x, y): 
    return x + y 

params = (1, 2)
print add(*params)
```
```python
3
```


#### 调用函数时使用字典作为实参

```python
def hello2(name='Guy', greeting='Welcome'):
    print greeting + ' ' + name + '!';
    
params = {'name': 'Jay', 'greeting': 'Hello'}
hello2(**params)
```
```python
Hello Jay!
```


## 类

###  

#### 类的定义与使用

```python
class Person:
    def setName(self, name):
        self.name = name
    def getName(self):
        return self.name
    def sayHello(self):
        print "Hello, world! I'm %s." % self.name

foo = Person()
foo.setName('Jay')
foo.sayHello()
```
```python
Hello, world! I'm Jay.
```


#### 类的构造函数

```python
class ListNode(object):
    def __init__(self, x): 
        self.val = x 
        self.next = None

node = ListNode(0)
print node.val
print node.next
```
```python
0
None
```


#### 派生类的定义

示例：定义类Handler，其派生自StreamRequestHandler

```python
class Handler(StreamRequestHandler):
  
    def handle(self):          
        addr = self.request.getpeername()
        print 'Got connection from', addr
        self.wfile.write('Thank you for connecting')
```


## 序列

通用序列操作主要包括：索引(indexing)、分片(slicing)、加(adding)、乘(multiplying)、成员资格(in)。


## 序列：列表


## 序列：元组


## 序列：字符串

###  

#### 索引

```python
>>> foo = 'Hello World!'
>>> foo[1]
'e'
```


#### 分片

<font color="red">
说明：分片索引遵循“包头不包尾”原则。
</font>

示例：获取字符串中的单词

```python
>>> foo = 'Hello World!'
>>> foo[6:-1]
'World'
```

示例：未指定开始索引，则默认从字符串头部开始

```python
>>> foo = 'Hello World!'
>>> foo[:5]             
'Hello'
```

示例：未指定结束索引，则默认到字符串尾部结束

```python
>>> foo = 'Hello World!'
>>> foo[6:]
'World!'
```


#### 加

<font color="red">
说明：加在这里表示连接字符串。
</font>

```python
>>> 'Hello' + 'World' + '!'
'HelloWorld!'
```


#### 乘

<font color="red">
说明：乘在这里表示重复字符串。
</font>

```python
>>> 'Hello' * 3
'HelloHelloHello'
```


#### 成员资格

```python
>>> 'o' in 'Hello World!'
True
>>> 'a' in 'Hello World!' 
False
```


## 映射：字典

###  

#### 定义

```python
people = { 
    'Alice': {
        'phone': '2341',
        'addr': 'Foo drive 23'
    },  
    'Beth': {
        'phone': '9102',
        'addr': 'Bar street 42'
    },  
    'Cecil': {
        'phone': '3158',
        'addr': 'Baz avenue 90'
    }   
}
```


## 集合：集合


## 分支语句 `if`

######  

<font color="red">
注意：分支语句不支持else if关键字。
</font>

### if语句的三种基本结构

#### if...

```python
number = 3
if number > 0:
    print 'positive'
```


#### if...else...

```python
number = -3
if number > 0:
    print 'positive'
else:
    print 'negative'
```


#### if...elif...else...

```python
number = 3
if number < 0:
    print 'negative'
elif number < 10:
    print 'positive little'
else:
    print 'positive big'
```


### 特殊用法

#### 赋值

```python
>>> x = -123
>>> sign = -1 if x < 0 else 1
>>> print sign
-1
```


## 循环语句 `for` `while`

### 循环语句 for...in...

#### 遍历字符串

```python
string = 'Hello'
for c in string:
    print c
```
```python
H
e
l
l
o
```


#### 遍历字符串列表

方式一：

```python
words = ['this', 'is', 'python', 'note']
for word in words:
    print word
```

方式二：

```python
>>> seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, seq[i]
... 
0 one
1 two
2 three
```


#### 遍历数字列表

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
for number in numbers:
    print number
```

```python
for number in range(0, 10):
    print number
```


#### 遍历字典

<font color="red">
说明：遍历的是字典的key，而不是value。
</font>

```python
dict = {'x': 1, 'y': 2, 'z': 3}
for key in dict:
    print key, 'corresponds to', dict[key]
```
```python
y corresponds to 2
x corresponds to 1
z corresponds to 3
```


### 循环语句 for...in...else...

####  

<font color="red">
说明：else会在for语句正常执行完（即：没有break）的情况下执行。
</font>

```python
>>> for c in 'abc':
...     print c
... else:
...     print 'Finished!'
... 
a
b
c
Finished!
```


### 循环语句 while

```python
x = 1
while x < 10:
    print x
    x += 1
```


### 循环语句 while...else...

####  

<font color="red">
说明：else会在for语句正常执行完（即：没有break）的情况下执行。
</font>

```python
>>> x = 1
>>> while x <= 3:
...     print x  
...     x += 1
... else:
...     print 'Finished!'
... 
1
2
3
Finished!
```


## 操作符

###  

#### 除 /

如果除数和被除数都是整数，则除法操作默认为整除操作。

```python
>>> 1 / 2
0
```

如果除数和被除数有一个是浮点数，则除法操作默认为普通除法操作。

```python
>>> 1.0 / 2
0.5
>>> 1.0 / 2.0
0.5
```
```python
>>> 1. / 2
0.5
>>> 1. / 2.
0.5
```

补充：对于除数和被除数都是整数，如果也想执行普通除法操作的话，可以使用下面两个方法。

1.使用特殊语句

```python
>>> from __future__ import division
>>> 1 / 2
0.5
```

2.使用命令行参数

```python
$ python -Qnew
>>> 1 / 2
0.5
```

#### 整除 //

不管除数和被除数是整数还是浮点数，//均执行整除操作。

```python
>>> 1 // 2
0
>>> 1.0 // 2
0.0
>>> 1.0 // 2.0
0.0
```


## 关键字

###  

#### False

False表示真值。


###  

#### from

from用于导入模块或导入模块中的类或函数。

示例：导入模块

```
>>> import math
>>> math.floor(32.9)
32.0
```

示例：导入模块中的函数

```
>>> from math import floor
>>> floor(32.9)
32.0
```


###  

#### import

import用于导入模块或导入模块中的类或函数。

示例：导入模块中的类

```
from SocketServer import TCPServer, StreamRequestHandler
```


###  

#### None

None是一个内建常量，通常用来表示变量值的缺失。


###  

#### not

not是逻辑非运算符。

示例：判断列表是否为空

```python
list1 = []
if not list1:
    print 'empty list'
```
```python
empty list
```


###  

#### or

or是逻辑或运算符。

示例：判断列表是否为空

```python
if not (readable or writable or exceptional):
    break
```


###  

#### print

示例：输出空行

```python
>>> print

>>> 
```

示例：输出字符串

```python
>>> print 'Hello world!'
Hello world!
```
```python
>>> print 'Bli ' * 2 + 'Xiaomoxian!'
Bli Bli Xiaomoxian!
```


###  

#### self

self表示类自身。

示例：类的定义与使用

```python
class Person:
    def setName(self, name):
        self.name = name
    def getName(self):
        return self.name
    def sayHello(self):
        print "Hello, world! I'm %s." % self.name

foo = Person()
foo.setName('Jay')
foo.sayHello()
```
```python
Hello, world! I'm Jay.
```

###  

#### True

True表示真值。


## 其他

###  

#### 命令行帮助

进入帮助

```python
>>> help()
```

查询模块信息(modules)

```python
help> modules
```
```python
help> __builtin__
```

查询关键字信息(keywords)

```python
help> keywords
```
```python
help> print
```

查询主题信息(topics)

```python
help> topics
```
```python
help> SLICINGS
```

