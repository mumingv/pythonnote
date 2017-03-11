# 第1章 快速改造：基础知识

## 安装Python

略。


## 交互式解释器

略。


## 算法是什么

略。


## 数字和表达式

######      

<font color="red">
说明：Python默认的除法就是整除。
</font>

### 整除的两种方法

方法一：

```
>>> 1 / 2
0
```

方法二：

```
>>> 1 // 2
0
>>> 1.0 // 2.0
0.0
```


### 普通除法的三种方法

方法一：使用浮点数

```
>>> 1.0 / 2
0.5
>>> 1 / 2.0
0.5
>>> 1.0 / 2.0
0.5
```
```
>>> 1. / 2
0.5
>>> 1 / 2.
0.5
>>> 1. / 2.
0.5
```

方法二：使用特殊语句

```
>>> from __future__ import division
>>> 1 / 2
0.5
```

方法三：使用命令行参数

```
$ python -Qnew
>>> 1 / 2
0.5
```


### 幂运算符

示例：

```
>>> 2 ** 3
8
>>> -3 ** 2
-9
>>> -(3 ** 2)
-9
>>> (-3) ** 2
9
```

## 变量

略。


## 语句

略。


## 获取用户输入

### input VS raw_input

input要求用户输入的内容必须是一个有效的表达式。如：下面输入的内容必须是一个**带双引号的**字符串。

```
>>> name = input("What's your name? ")
What's your name? "Jay"
>>> print "Hello, " + name + "!"
Hello, Jay!
```

raw_input则无此要求，显得"更人性化"。如：

```
>>> name = raw_input("What's your name? ")
What's your name? Jay
>>> print "Hello, " + name + "!"          
Hello, Jay!
```


### 其他

######     

<font color="red">
说明：在交互式解释器中使用if语句，需要按两次回车才能执行语句。
</font>

```
>>> if 2 != 3: print 'two is not equal three'
... 
two is not equal three
```


## 函数

略。


## 模块

### 导入模块函数的两种方法

方法一：import <module>

```
>>> import math
>>> math.floor(32.9)
32.0
```

方法二：from <module> import <function>

```
>>> from math import floor
>>> floor(32.9)
32.0
```


### math VS cmath

cmath = complex math，复数

math库示例：

```
>>> import math
>>> math.sqrt(9)
3.0
>>> math.sqrt(-9)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  ValueError: math domain error
```

cmath库示例：

```
>>> import cmath  
>>> cmath.sqrt(-9)
3j
```


## 保存并执行程序

略。


## 字符串

### 字符串的三种表示

方法一：单引号

```
>>> print 'Hello, world!'
Hello, world!
```

方法二：双引号

```
>>> print "Hello, world!" 
Hello, world!
```

方法三：三个双引号表示多行长字符串

```
>>> print """This is a very long string.
... "Hello world!"
... That's all.
... """
This is a very long string.
"Hello world!"
That's all.

>>> 
```


### 原始字符串

######     

<font color="red">
说明：原始字符串不会对反斜线做转义处理。
</font>

原始字符串以字母'r'开头。示例：

```
>>> print "C:\nowhere"
C:
owhere
>>> print r"C:\nowhere"
C:\nowhere
```


### Unicode字符串

Unicode字符串存储为16位Unicode字符。

示例：

```
>>> print u"我是中国人"
我是中国人
```


### 值转换为字符串的三种方法

方法一：str函数，转换结果是给用户看的

```
>>> print str("Hello world!")
Hello world!
>>> print str(10000L)        
10000
```

方法二：repr函数，转换结果是Python表达式

```
>>> print repr("Hello world!")   
'Hello world!'
>>> print repr(10000L)        
10000L
```

方法三：反引号，和repr函数作用相同，不建议使用

```
>>> print `"Hello world!"`
'Hello world!'
>>> print `10000L`    
10000L
```


## 小结

略。

