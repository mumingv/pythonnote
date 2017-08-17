# pymongo

## 安装

### Mac

```
$ sudo pip install pymongo
```


## 参考资料

- http://api.mongodb.com/python/current/tutorial.html#a-note-on-unicode-strings
- http://wiki.jikexueyuan.com/project/start-learning-python/232.html
- http://xitongjiagoushi.blog.51cto.com/9975742/1657096


## 示例

### 连接数据库并插入数据

```python
import pymongo
client = pymongo.MongoClient("localhost", 27017)
db = client.case
session = db.session
print db.collection_names()
c2 = {"name" : "菜鸟教程", "site" : "www.runoob.com"}
session.insert(c2)
```

