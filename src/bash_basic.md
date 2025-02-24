# bash基础

## 一、须知
bash shell 脚本只能直接运行在macOS、各个发行版的Linux, 如果你的电脑是Windows, 将不能直接运行shell文件, 需要通过wsl、docker、Linux虚拟机来学习.

## 二、认识shell文件
创建bash shell脚本文件时, 文件名不作强行要求, 但文件中的第一行必须指定需要使用的shell, 其格式如下

```bash
#!/bin/bash
```

## 三、修改shell文件为可执行文件
执行shell文件前, 必须将shell文件设置为可执行文件, 例如我们拥有一个shell文件叫做install.sh, 其设置为可执行文件的命令如下

```bash
chmod u+x install.sh
```

## 四、执行shell文件
执行shell文件, 只需要输入如下的命令即可

```bash
./install.sh
```

## 五、完整案例

- 编辑一个shell文件叫做test.sh, 其内容如下

```bash
#!/bin/bash
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to study shell programming."
```

- 将shell文件设置为可执行文件

```bash
chmod u+x test.sh
```

- 执行shell文件

```bash
./test.sh
```

随后按照提示文字, 输入你的名字即完成该案例. 尽管你暂时并未看懂该test.sh文件中的内容也不要紧, 随后介绍完shell的各种语法后, 你便能理解其中的内容.
