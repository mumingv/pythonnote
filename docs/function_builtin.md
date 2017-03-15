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
|set([iterable])            |返回从iterable生成的元素集合           |
|-                          |-                                      |
|abs(number)                |返回一个数的绝对值                     |
|hex(number)                |将数字转换为16进制表示的字符串         |


