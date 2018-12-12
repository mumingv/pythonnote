# 数据类型

官方文档：https://docs.python.org/3/library/datatypes.html

## datetime


## calendar


## collections


## collections.abc 容器的抽象基类

#### 示例：判断给定的对象是否可迭代

```python
>>> from collections.abc import Iterable
>>> isinstance('abc', Iterable)
True
>>> isinstance([1, 2, 3], Iterable)
True
>>> isinstance((1, 2, 3), Iterable)
True
>>> isinstance(123, Iterable)
False
```


## heapq


## bisect


## array


## weakref


## types


## copy


## pprint


## reprlib


## enum


## 





