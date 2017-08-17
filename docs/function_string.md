# 字符串常量&函数&方法

## 字符串常量

######  

|常量                       |含义                                   |
|---------------------------|---------------------------------------|
|string.digits              |'0123456789'                           |
|string.letters             |'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'|
|string.lowercase           |'abcdefghijklmnopqrstuvwxyz'           |
|string.uppercase           |'ABCDEFGHIJKLMNOPQRSTUVWXYZ'           |
|string.printable           |'0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!"#$%&\'()*+,-./:;<=>?@[\\]^_`{}~ \t\n\r\x0b\x0c'|
|string.punctuation         |'!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~'   |


## 字符串方法列表

###### 

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.format() 				|格式化字符串		|
|obj.strip()				|去除收尾空白字符	|


## 字符串方法总结

### 字符串和序列的相互转换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.join(seq)           |以 string 作为分隔符，将 seq 中所有的元素(的字符串表示)合并为一个新的字符串|
|obj.split(str)          |以 str 为分隔符切片 string             |


### 去除首尾空白字符

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.strip()             |删除 string 字符串首尾的空格           |
|obj.lstrip()            |删除 string 字符串首部的空格           |
|obj.rstrip()            |删除 string 字符串尾部的空格           |


### 删

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|


### 大小写转换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.upper()             |转换 string 中的小写字母为大写         |
|obj.lower()             |转换 string 中所有大写字符为小写       |


### 查

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.find(str)           |检测 str 是否包含在 string 中          |


### 字符串替换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.replace(str1, str2) |把 string 中的 str1 替换成 str2        |


### 其他

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|obj.translate(str, del="")  |根据 str 给出的表(包含 256 个字符)转换 string 的字符   |


## 字符串方法示例

### format

#### 示例

```python
>>> "{} {}".format("hello", "world")
'hello world'
```


### split

函数原型：

```python
obj.split(str="", num=string.count(str))
```

#### 示例：使用空格切分字符串

```python
>>> str = 'aaa bbb ccc ddd eee fff ggg'
>>> str.split(" ")
['aaa', 'bbb', 'ccc', 'ddd', 'eee', 'fff', 'ggg']
>>> str.split(" ", 1)
['aaa', 'bbb ccc ddd eee fff ggg']
>>> str.split(" ", 2)
['aaa', 'bbb', 'ccc ddd eee fff ggg']
```

