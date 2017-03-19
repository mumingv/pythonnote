# 列表函数&方法

## 列表函数总结

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|cmp(list1, list2)          |比较两个列表的元素                     |
|len(list)                  |列表元素个数                           |
|max(list)                  |返回列表元素最大值                     |
|min(list)                  |返回列表元素最小值                     |
|list(seq)                  |将元组转换为列表                       |


## 列表方法总结

### 增

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|list.append(obj)           |在列表末尾添加新的对象                 |
|list.extend(seq)           |在列表末尾一次性追加另一个序列中的多个值|
|list.insert(index, obj)    |将对象插入列表                         |

### 删

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|list.remove(obj)           |移除列表中某个值的第一个匹配项         |
|list.pop([index])          |移除列表中的一个元素（默认最后一个元素），并且返回该元素的值|


### 改

######   

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|list.reverse()             |反向列表中的元素                       |


### 查

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|list.count(obj)            |统计某个元素在列表中出现的次数         |
|list.index(obj)            |从列表中找出某个值第一个匹配项的索引位置|


### 其他

######  

|函数                       |含义                                   |
|---------------------------|---------------------------------------|
|list.sort([func])          |对原列表进行排序                       |
