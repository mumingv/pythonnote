# 包函数

## String Services 字符串

### re（部分）正则表达式

参考：[官方](https://docs.python.org/2/library/re.html) & [木名](#docs/pkg_re)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|re.compile() 		|根据模式生成一个正则表达式对象		|
|re.match() 		|尝试从字符串的起始位置匹配一个模式	|


## Data Types 数据类型

### collections（部分）高性能容器数据类型

参考：[官方](https://docs.python.org/2/library/collections.html) & [木名](#docs/pkg_collections)

|数据结构          	|功能                           |
|-------------------|-------------------------------|
|namedtuple()		||
|deque  			|双端队列|
|Counter 			||
|OrderedDict 		||
|defaultdict		|''|


### copy（部分）浅拷贝和深拷贝操作

###### 

|函数/方法          	|功能                           |
|-------------------|-------------------------------|


## Numeric and Mathematical Modules 数字和数学模块

### random（部分）随机数

参考：[官方](https://docs.python.org/2/library/random.html) & [木名](#docs/pkg_random)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|random.randint()	|随机生成指定范围内的整数			|
|random.random()	|随机生成[0.0, 1.0)范围内的浮点数	|


## File and Directory Access 文件和目录操作

### os.path（部分）文件和目录的路径处理

参考：[官方](https://docs.python.org/2/library/os.path.html) & [木名](#docs/pkg_os_path)

要使用这里的方法，`import os` 和 `import os.path` 都可以。

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|os.path.exists() 	|判断文件/目录的路径是否存在			|


## File Formats 文件格式

### ConfigParser（部分）配置文件解析

参考：[官方](https://docs.python.org/2/library/configparser.html) & [木名](#docs/pkg_configparser)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|objConfigParser.get()|获取配置文件某个选项的值			|


## Generic Operating System Services 一般操作系统服务

### os（部分）操作系统接口

参考：[官方](https://docs.python.org/2/library/os.html) & [木名](#docs/pkg_os)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|os.getpid()		|获取当前进程id					|
|os.getppid() 		|获取父进程id						|
|os.system()		|在subshell中执行命令				|
|os.popen()			|执行命令，返回文件描述符，命令返回的内容通过文件描述符获取|


### time（部分）时间存取和转化

参考：[官方](https://docs.python.org/2/library/time.html) & [木名](#docs/pkg_time)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|time.time()		|返回一个浮点数表示的时间值，单位：s	|


## Interprocess Communication and Networking 进程间通信和网络访问

### socket (部分) 底层网络接口

参考：[官方](https://docs.python.org/2/library/socket.html) & [木名](#docs/pkg_socket)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|socket.socket()      |创建套接字                     |
|socket.gethostname() |获取主机名称                   |
|obj.accept()         |接受连接                       |
|obj.bind()           |将主机名(IP)和地址绑定到套接字 		|
|obj.close()          |关闭套接字                     |
|obj.connect()        |连接                           |
|obj.listen()         |侦听                           |
|obj.recv()           |接收数据                       |
|obj.send()           |发送数据                       |

## Internet Data Handling 互联网数据处理

### json JSON编解码

参考：[官方](https://docs.python.org/2/library/json.html) & [木名](#docs/pkg_json)

|函数/方法          	|功能                           |
|-------------------|-------------------------------|
|json.loads() 		|字符串转对象|
|json.dumps() 		|对象转字符串|


## Python Runtime Services 运行时服务

### sys (部分) 系统参数和函数

参考：[官方](https://docs.python.org/2/library/sys.html) & [木名](#docs/pkg_sys)

|属性/函数/方法       |功能                           |
|-------------------|-------------------------------|
|sys.argv           |数组，存放命令行参数           |
|sys.stdin 			|文件对象，与标准输入对应 		|
|sys.stdout 		|文件对象，与标准输出对应		|
|sys.stderr 		|文件对象，与标准错误对应		|


## Python Language Services 语言服务

### keyword 关键字

参考：[官方](https://docs.python.org/2/library/keyword.html) & [木名](#docs/pkg_keyword)

|属性/函数/方法       |功能                           |
|-------------------|-------------------------------|
|keyword.iskeyword()|检查字符串是否是python的关键字		|
|keyword.kwlist 	|python所有关键字的列表			|


