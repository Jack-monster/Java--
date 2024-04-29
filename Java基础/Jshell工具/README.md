# Jshell
## 启动Jshell
终端中输入jshell
即可进入jshell环境
```shell
(base) PS C:\Users\86182\Desktop\Myworkspace\Java学习> jshell               
|  欢迎使用 JShell -- 版本 22
|  要大致了解该版本, 请键入: /help intro

jshell>
```
## 执行命令

```
jshell> "hello".length()
$1 ==> 5
```
得到的$1可作为运算结果变量继续参与运算

```
jshell> $1 * 100
$2 ==> 500
```

## 结束

```
jshell> /exit
|  再见
```