# [sys](https://github.com/mumingv/python/tree/master/func/sys)

## sys.argv 获取命令行参数

函数原型及说明，请参考：[官方文档](https://docs.python.org/2/library/sys.html#sys.argv)。

<font color="red">sys.argv[0]表示脚本名称，sys.argv[1] ... 表示参数。</font>

示例：

```python
import sys
print sys.argv[0]
print sys.argv[1]
```

```python
$ python sys.argv.py param
sys.argv.py
param
```





