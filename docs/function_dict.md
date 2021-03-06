# 字典函数&方法

## 字典函数列表

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|cmp(dict1, dict2)          |比较两个字典元素                       |
|len(dict)                  |计算字典元素个数，即键的总数           |
|str(dict)                  |输出字典可打印的字符串表示             |
|type(variable)             |返回输入的变量类型，如果变量是字典就返回字典类型   |


## 字典函数示例


## 字典方法列表

###### 

|方法                       |含义                                   |
|--------------------------|---------------------------------------|
|dict.get() 				|返回指定键的值 	|
|dict.values()              |以列表返回字典中的所有值               |


## 字典方法总结

### 创建

######  

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|dict.fromkeys(seq[, val])) |创建一个新字典，以序列 seq 中元素做字典的键，val 为字典所有键对应的初始值 |


### 增

######  

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|dict.setdefault(key, default=None) |和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default   |
|dict.clear()               |删除字典内所有元素                     |


### 删改

######  

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|dict.update(dict2)         |把字典dict2的键/值对更新到dict里       |


### 查

######  

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|dict.get(key, default=None)|返回指定键的值，如果值不在字典中返回default值  |
|dict.keys()                |以列表返回一个字典所有的键             |
|dict.values()              |以列表返回字典中的所有值               |
|dict.items()               |以列表返回可遍历的(键, 值) 元组数组    |
|dict.has_key(key)          |如果键在字典dict里返回true，否则返回false  |


### 其他

######  

|方法                       |含义                                   |
|---------------------------|---------------------------------------|
|dict.copy()                |返回一个字典的浅复制                   |


## 字典方法示例

###  

#### dict.keys

```python
>>> dict = {")":"(", "]":"[", "}":"{"}
>>> dict.keys()
[')', '}', ']']
```


#### dict.values 

```python
>>> dict = {")":"(", "]":"[", "}":"{"}
>>> dict.values()
['(', '{', '[']
```


## 字典相关操作

###  

#### 增加

##### 增加字典元素

```
>>> dict
{'zhangsan': 18, 'wangwu': 22}
>>> dict['zhaoliu'] = 24
>>> dict
{'zhaoliu': 24, 'zhangsan': 18, 'wangwu': 22}
```


#### 删除

##### 删除字典元素

```
>>> dict = {"zhangsan": 18, "lisi": 20, "wangwu": 22}
>>> dict
{'lisi': 20, 'zhangsan': 18, 'wangwu': 22}
>>> del dict['lisi']
>>> dict
{'zhangsan': 18, 'wangwu': 22}
```


#### 遍历

##### 查询所有的key

```
>>> dict = {"zhangsan": 18, "lisi": 20, "wangwu": 22}
>>> for key in dict:
...     print key
...
lisi
zhangsan
wangwu
```










