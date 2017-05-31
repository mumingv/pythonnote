# 网络编程

## 少数几个网络设计模块

### socket模块

略。


### urllib和urllib2模块

示例：打开远程文件，使用正则表达式过滤字符串

```
>>> from urllib import urlopen
>>> webpage = urlopen('http://www.python.org/')
>>> import re
>>> text = webpage.read()  # 即：text = '<a href="/about/" title="" class="">About</a>'
>>> m = re.search('<a href="([^"]+)" .*?>about</a>', text, re.IGNORECASE)
>>> m.group(1)
'/about/'
```


### 其他模块

略。


##  SocketServer和它的朋友们


## 多个连接


## Twisted


## 小结


