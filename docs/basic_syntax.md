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


## 序列：列表


## 序列：元组


## 序列：字符串


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


## 关键字


## 其他


