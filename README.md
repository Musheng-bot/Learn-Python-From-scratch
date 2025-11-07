# Python Teaching

## Introduction

这是一篇入门的python教程，希望你们能有所收获

## 环境安装

### Windows

通过python官网下载，具体可参照[安装教程](https://blog.csdn.net/maiya_yayaya/article/details/131450517)  
可以和本教程一致，安装`Python 3.10`，或者其他

### Linux

以`Ubuntu`系统举例，我相信用其他Linux版本的朋友肯定有自己安装python的能力

```shell
sudo apt install python3
sudo apt install python-is-python3
```

### Mac

```shell
brew install python
```

## 验证安装成功

打开`终端`或`cmd`，输入

```shell
python --version
# 或者输入
python3 --version 
```

弹出来的是版本号就对了，就像这样

![python弹出版本号](res/python_version.png)

## 本教程环境

本教程使用`Ubuntu 22.04 LTS`系统，python版本为`Python 3.10.12`  
不使用`anaconda`，使用python自带的`virtualvenv`创建虚拟环境。

## 创建虚拟环境

在一个工作文件夹下打开`终端`或`cmd`，输入

```shell
python -m venv .venv
# .venv是虚拟环境名，你可以自定义
```

就可以在当前文件夹下创建一个虚拟环境了

## 使用虚拟环境

### Linux

依然以`Ubuntu 22.04`举例，其他Linux发行版的朋友我相信你们能自己解决！

```shell
cd /path/to/project
source ./.venv/bin/activate
```

这样之后我们就成功启动了虚拟环境，在终端前会带有`(虚拟环境名)`，像这个样子。

![python启动了虚拟环境](res/python_venv_activate.png)

