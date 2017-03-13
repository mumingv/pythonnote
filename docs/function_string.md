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


## 字符串方法总结

### 字符串和序列的相互转换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.join(seq)           |以 string 作为分隔符，将 seq 中所有的元素(的字符串表示)合并为一个新的字符串|
|string.split(str)          |以 str 为分隔符切片 string             |


### 去除首尾空白字符

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.strip()             |删除 string 字符串首尾的空格           |
|string.lstrip()            |删除 string 字符串首部的空格           |
|string.rstrip()            |删除 string 字符串尾部的空格           |


### 删

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|


### 大小写转换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.upper()             |转换 string 中的小写字母为大写         |
|string.lower()             |转换 string 中所有大写字符为小写       |


### 查

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.find(str)           |检测 str 是否包含在 string 中          |


### 字符串替换

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.replace(str1, str2) |把 string 中的 str1 替换成 str2        |


### 其他

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|string.translate(str, del="")  |根据 str 给出的表(包含 256 个字符)转换 string 的字符   |

