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


## 运行出现错误：UnicodeDecodeError: 'utf8' codec can't decode byte 0xc8 in position 0: invalid continuation byte

line为gbk编码的json字符串，使用json.loads报错。

```
single_session = json.loads(line)
```

原因是python默认会使用utf8对字符串进行解码，如果不是就需要进行显示指定字符编码。

```
line = line.decode("gbk")
single_session = json.loads(line)
```

这样的话就会把gbk编码转成python内部处理的unicode编码。

最后输出的时候需要使用encode函数将unicode编码的字符串转换成目标编码。如下所示：

```
fpout.write(json.dumps(mcpack_request_data, ensure_ascii=False).encode("gbk"))
```

当然，如果不想每个输出都显示指定编码的话，也可以在文件头部设置默认的编码。如下所示：

```
reload(sys)
sys.setdefaultencoding('utf-8')
```
```
fpout.write(json.dumps(mcpack_request_data, ensure_ascii=False))
```

如果输出的时候以上两种方式都不使用，则会报编码错误。如下所示：

```
fpout.write(json.dumps(mcpack_request_data, ensure_ascii=False))
```
```
UnicodeEncodeError: 'ascii' codec can't encode characters in position 158-159: ordinal not in range(128)
```

注意：这里json.dumps函数使用了ensure_ascii=False参数，否则导出的文件就是unidoce编码格式而不是中文格式。














