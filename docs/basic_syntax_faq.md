# 语法FAQ

## exit()、sys.exit()、os._exit() 的区别是什么？

######  

|函数       |使用场景       |备注           |
|-----------|---------------|---------------|
|exit()/quit()|交互式shell中退出|抛出SystemExit异常|
|sys.exit() |主程序退出     |抛出SystemExit异常|
|os._exit() |子进程退出     |直接退出，不抛异常|


## 如何打印中文字符？

示例：打印对象

```
print(repr(app_info_dict).decode('unicode-escape'))
```
```
{u'dm9A55011141058ED3': {u'app_name': u'wf智能助理', u'id': 2, u'app_key': u'BB350AA36F1388B5E485D552F512B515', u'app_id': u'dm9A55011141058ED3'}, u'dm441BC7F55B82F26A': {u'app_name': u'智能座椅', u'id': 1, u'app_key': u'FA4E05FBC2043997C02712AFD4A1150D', u'app_id': u'dm441BC7F55B82F26A'}}
```

示例：打印json字符串（数组转json）

```
print json.dumps(params, ensure_ascii=False)
```

