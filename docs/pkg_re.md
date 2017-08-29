# re

## 示例

### 获取方括号中的字符串

```
>>> import re
>>> obj = re.compile("\[(.*?)\]")  
>>> result = obj.match("[singer]")
>>> print result.group(1)
singer
```

