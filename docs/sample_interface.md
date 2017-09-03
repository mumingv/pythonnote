# 模块接口

## 用户输入

```
>>> year = raw_input('Year: ')
Year: 2017
>>> print year
2017
```


## File

### 读取文件并按行处理

方法一：

```python
request_query_file = sys.argv[1]
file = open(request_query_file)
try:
	for line in file:
	    line = line.strip("\r\n")
	    if not line:
	        print "empty"
	    else:
	        print line
finally:
	file.close()
```

方法二：

```
>>> with open(r'abc.txt') as fileobj:
...     for line in fileobj:
...         print line
...
```

