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

```python
request_query_file = sys.argv[1]
file = open(request_query_file)
for line in file:
    print line
```


