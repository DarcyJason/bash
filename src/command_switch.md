# 命令替换

在Shell脚本中, 我们可以将Linux或macOS的命令输出结果存储在变量中, 其中有两种方法, 分别是反引号``和$()格式

## 一、``格式

```bash
#!/bin/bash
time=`date`
echo "Now is $time"
```

## 二、$()格式

```bash
#!/bin/bash
time=$(date)
echo "Now is $time"
```

这两个方法均可以实现相同的功能, 使用这种方法的前提是你对Linux或macOS命令非常了解, 而且第二种方法一定不能忘记$符号, 否则会与子shell执行命令冲突, 因为(命令)就是将命令放入子shell中执行.
