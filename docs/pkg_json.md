# json

## json.dumps

### 示例：将对象转成字符串，使用中文编码

```
json = json.dumps(obj, ensure_ascii=False)
```


## json.loads

### 示例：将字符串转成对象，制定字符串的编码方式

```
obj = json.loads(request, encoding='utf8')
```
