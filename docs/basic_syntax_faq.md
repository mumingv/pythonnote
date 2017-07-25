# 语法FAQ

## exit()、sys.exit()、os._exit() 的区别是什么？

######  

|函数       |使用场景       |备注           |
|-----------|---------------|---------------|
|exit()/quit()|交互式shell中退出|抛出SystemExit异常|
|sys.exit() |主程序退出     |抛出SystemExit异常|
|os._exit() |子进程退出     |直接退出，不抛异常|





