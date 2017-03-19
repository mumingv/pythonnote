# 基本语法

## 注释

单行注释，使用Shell风格的注释。

```
# ...
```

多行注释：使用一对'''(三个单引号)，或者使用一对"""(三个双引号)包含注释信息

```
'''
comment...
'''
```

```
"""
comment...
"""
```


## 类型


## 变量


## 函数

###  

#### 函数定义与调用

```
def hello(name):
    return 'Hello, ' + name + '!';
print hello('Jay');
```
```
Hello, Jay!
```


#### 位置参数收集

```
def printPositionParams(*params):
    print params

printPositionParams(1, 2, 3)
```
```
(1, 2, 3)
```


#### 关键字参数收集

```
def printKeywordParams(**params):
    print params

printKeywordParams(foo = 1, bar = 2, test = 3)
```
```
{'test': 3, 'foo': 1, 'bar': 2}
```


#### 混合参数收集

```
def printCompoundParams(title, *posParams, **keyParams):
    print title
    print posParams
    print keyParams

printCompoundParams('Params test:', 1, 2, 3, foo = 4, bar = 5, test = 6)
```
```
Params test:
(1, 2, 3)
{'test': 6, 'foo': 4, 'bar': 5}
```


#### 调用函数时使用元组作为实参

```
def add(x, y): 
    return x + y 

params = (1, 2)
print add(*params)
```
```
3
```


#### 调用函数时使用字典作为实参

```
def hello2(name='Guy', greeting='Welcome'):
    print greeting + ' ' + name + '!';
    
params = {'name': 'Jay', 'greeting': 'Hello'}
hello2(**params)
```
```
Hello Jay!
```


## 序列

通用序列操作主要包括：索引(indexing)、分片(slicing)、加(adding)、乘(multiplying)、成员资格(in)。


## 序列：列表


## 序列：元组


## 序列：字符串

###  

#### 索引

```
>>> foo = 'Hello World!'
>>> foo[1]
'e'
```


#### 分片

<font color="red">
说明：分片索引遵循“包头不包尾”原则。
</font>

示例：获取字符串中的单词

```
>>> foo = 'Hello World!'
>>> foo[6:-1]
'World'
```

示例：未指定开始索引，则默认从字符串头部开始

```
>>> foo = 'Hello World!'
>>> foo[:5]             
'Hello'
```

示例：未指定结束索引，则默认到字符串尾部结束

```
>>> foo = 'Hello World!'
>>> foo[6:]
'World!'
```


#### 加

<font color="red">
说明：加在这里表示连接字符串。
</font>

```
>>> 'Hello' + 'World' + '!'
'HelloWorld!'
```


#### 乘

<font color="red">
说明：乘在这里表示重复字符串。
</font>

```
>>> 'Hello' * 3
'HelloHelloHello'
```


#### 成员资格

```
>>> 'o' in 'Hello World!'
True
>>> 'a' in 'Hello World!' 
False
```


## 映射：字典


## 集合：集合


## 分支语句 `if`

### if语句的三种基本结构

#### if...

```
number = 3
if number > 0:
    print 'positive'
```


#### if...else...

```
number = -3
if number > 0:
    print 'positive'
else:
    print 'negative'
```


#### if...elif...else...

```
number = 3
if number < 0:
    print 'negative'
elif number < 10:
    print 'positive little'
else:
    print 'positive big'
```


## 循环语句 `for` `while`

### 循环语句 for...in...

#### 遍历字符串列表

```
words = ['this', 'is', 'python', 'note']
for word in words:
    print word
```


#### 遍历数字列表

```
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
for number in numbers:
    print number
```

```
for number in range(0, 10):
    print number
```


### 循环语句 while

```
x = 1
while x < 10:
    print x
    x += 1
```


## 操作符

###  

#### 除 /

如果除数和被除数都是整数，则除法操作默认为整除操作。

```
>>> 1 / 2
0
```

如果除数和被除数有一个是浮点数，则除法操作默认为普通除法操作。

```
>>> 1.0 / 2
0.5
>>> 1.0 / 2.0
0.5
```
```
>>> 1. / 2
0.5
>>> 1. / 2.
0.5
```

补充：对于除数和被除数都是整数，如果也想执行普通除法操作的话，可以使用下面两个方法。

1.使用特殊语句

```
>>> from __future__ import division
>>> 1 / 2
0.5
```

2.使用命令行参数

```
$ python -Qnew
>>> 1 / 2
0.5
```

#### 整除 //

不管除数和被除数是整数还是浮点数，//均执行整除操作。

```
>>> 1 // 2
0
>>> 1.0 // 2
0.0
>>> 1.0 // 2.0
0.0
```


## 关键字

###  

#### print

示例：输出空行

```
>>> print

>>> 
```

示例：输出字符串

```
>>> print 'Hello world!'
Hello world!
```
```
>>> print 'Bli ' * 2 + 'Xiaomoxian!'
Bli Bli Xiaomoxian!
```


## 其他

###  

#### 命令行帮助

进入帮助

```
>>> help()
```

查询模块信息(modules)

```
help> modules
```
```
help> __builtin__
```

查询关键字信息(keywords)

```
help> keywords
```
```
help> print
```

查询主题信息(topics)

```
help> topics
```
```
help> SLICINGS
```

