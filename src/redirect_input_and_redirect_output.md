# 重定向输入和输出

相信许多人在第一次看到重定向输入与输出时一脸懵, 不知道重定向是什么, 其实你不必了解重定向是什么, 只需要指定重定向输入与输出是对文件进行读写操作即可.

## 一、覆盖源文件的输出重定向

```bash
command > outputfile
```

该命令会将command命令的输出结果写入outputfile中并覆盖掉源文件的所有内容, 你也可以理解为先清空outputfile中的所有内容后, 再将command的运行结果写入outputfile中.

或许你并不太懂, 那我们通过例子来掌握吧.

首先, 创建test.txt, 内容如下

```
Hello test!
```

随后, 创建test.txt脚本文件, 内容如下

```bash
#!/bin/bash
date > test.txt
```

当你执行完该脚本后, 使用cat test.txt命令, 即可查看到test.txt中的内容已经变成了date的运行结果而没有Hello test!了, 这便是覆盖源文件的输出重定向的用法. 

## 二、追加至源文件最后的输出重定向

```bash
command >> outputfile
```

该命令就是为了解决不想清空源文件内容, 只想追加内容至文件最后的方法, 我们还是通过例子来掌握.

首先, 删除之前的test.txt然后重新创建test.txt, 内容如下

```
What is the time now?
```

随后, 创建test.txt脚本文件, 内容如下

```bash
#!/bin/bash
date >> test.txt
```

当你执行完该脚本后, 使用cat test.txt命令, 即可查看到test.txt中的内容保留了, 并在最后有date的运行结果, 这便是追加至源文件最后的输出重定向的用法.

## 三、输入重定向

```bash
command < inputfile
```

其实输入重定向, 就是将文件内容作为命令参数传入, 我们依然通过案例来学习, 在此简单介绍一下wc命令, 该命令用于统计文本中的数据进行统计, 并输出三个值, 分别是文本的行数、文本的词数和文本的字节数.

例如我们准备好text.txt文件, 内容如下

```
Hello
my
friend
let's study shell programming
```

创建test.sh脚本文件, 内容如下

```bash
#!/bin/bash
wc < test.txt
```

执行完该脚本, 如果你看到 4  7 46, 说明大功告成了.

## 四、内联输入重定向

```bash
commmand << marker
data
marker
```

这种写法, 可以让我们无需文件, 便可传入大量文本内容为命令参数, 我们依旧通过案例来学习.

编写我们的test.sh文件, 内容如下

```bash
#!/bin/bash
wc << EOF
test string 1
test string 2
test string 3
EOF
```

当我们执行该脚本文件后, 输出 3 9 42, 说明你已经成功完成了内联输入重定向, 虽然marker可以由我们任意指定, 但请记住两个marker必须相同, 通常我们用EOF代替marker.
