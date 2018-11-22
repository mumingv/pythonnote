# 环境FAQ

## [Mac]安装管理多个Python版本？

参考：https://juejin.im/post/5b42cbb15188251abf413ee6


## [Mac]安装pandas，提示无法卸载numpy？

安装pandas，提示如下错误信息：

```
$ sudo -H pip install pandas
Cannot uninstall 'numpy'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall.
```

解决方法：强制安装新的numpy后重新再安装pandas。

```
$ sudo -H pip install --ignore-installed numpy
$ sudo -H pip install pandas
```

