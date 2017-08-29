# os

## os.system

在subshell中执行命令，返回值是执行命令的返回码（成功返回0）。

```
>>> os.system('find $PWD')
/Users/muming/Sites/shell/demo/datetime
/Users/muming/Sites/shell/demo/datetime/date_loop.sh
0
>>> ret = os.system('find $PWD')
/Users/muming/Sites/shell/demo/datetime
/Users/muming/Sites/shell/demo/datetime/date_loop.sh
>>> print ret
0
```


## os.popen

执行命令，返回文件描述符，命令返回的内容通过文件描述符获取。

#### 示例

```
>>> import os
>>> os.popen('find $PWD')
<open file 'find $PWD', mode 'r' at 0x1061d9930>
>>> p = os.popen('find $PWD')
>>> for line in p:
...     print line.strip()
...
/Users/muming/Sites/shell/demo/datetime
/Users/muming/Sites/shell/demo/datetime/date_loop.sh
>>>
```

