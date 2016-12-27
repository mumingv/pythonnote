# 运行FAQ

## 运行出现错误：No module named requests

执行main.py，出现如下错误：

```python
$ python main.py input_file 
Traceback (most recent call last):
  File "main.py", line 17, in <module>
    import requests
ImportError: No module named requests
```

该错误表示没有找到名为requests的模块，需要单独安装。

```
$ sudo pip install requests
```

如果系统中没有pip命令，则需要先安装pip。

```bash
$ sudo yum install python2-pip   # python2.x版本
$ sudo yum install python34-pip  # python3.4版本
```

<font color="red">注：pip是python包的安装和管理工具，是easy_install的替代品。</font>











