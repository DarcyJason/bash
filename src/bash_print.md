# 输出

## 一、序言
任何伟大的程序员都从会编写一个Hello World!程序开始, 让我们开始学习如何编写Shell脚本文件, 实现输出Hello World!

## 二、创建shell脚本文件实现输出功能
用你喜欢的编辑器如Vim、neoVim或VScode等编写test.sh文件, 其内容如下, 当你完成设置文件为可执行文件, 并执行后, 如果看到Hello World! 恭喜你成功完成了你的第一个shell脚本程序

```bash
#!/bin/bash
echo "Hello World!"
```

如果你学习过其它编程语言(C、Java、Python等), 你便能很快掌握echo, echo就类似于其它语言的printf()、System.out.print()、print()语句, 将你想要输出的内容输出到终端中显示. 但echo默认是输出并换行, 想要不换行输出, 需要在前方添加 -n 选项. 如下:

```bash
#!/bin/bash
echo -n "Hello World! "
echo -n "Welcome to study shell programming"
```

此时, 当你设置文件为可执行文件, 并执行时, 便能发现这两句出现在了同一行.

## 三、输出变量
除了以上两个功能, echo还有更强大的其它功能, 例如输出变量的值, 如果你看不太懂不要紧, 因为我们会在下一章节讲解变量, 这里只是为了讲解echo的功能.

```bash
#!/bin/bash
one=1
echo "one is equal to $one"
```

运行后, 如果看到one is equal to 1 说明运行成功了, 接下来学习更多的bash shell语法来了解强大的echo.
