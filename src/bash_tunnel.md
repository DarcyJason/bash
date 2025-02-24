# 管道

有时候我们需要将一个命令的输出作为另一个命令的输入, 此时, 管道符号派上用场了.

例如, 我们拥有test.txt文件, 内容如下

```
3
8
4
1
```

我们先使用重定向输入与输出编写test.sh, 实现对test.txt文本内容排序

```bash
#!/bin/bash
cat test.txt > need_to_be_sorted.txt
sort < need_to_be_sorted.txt
```

运行该脚本文件后, 其结果如下

```
1
3
4
8
```

如果用管道符号, 我们可以避免创建中间文件, 直接完成排序

```bash
#!/bin/bash
cat test.txt | sort
```

运行该脚本后, 我们依然能够得到如下结果

```
1
3
4
8
```
