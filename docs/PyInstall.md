# Python 安装教程

## 环境安装

### Windows

通过python官网下载，具体可参照[安装教程](https://blog.csdn.net/maiya_yayaya/article/details/131450517)  
可以和本教程一致，安装`Python 3.10`，或者其他版本。

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

![python弹出版本号](../res/python_version.png)

## 本教程环境

本教程使用`Ubuntu 22.04 LTS`系统，python版本为`Python 3.10.12`  
不使用`anaconda`，使用`python pip`自带的`virtualenv`创建虚拟环境。

## 创建虚拟环境

在一个工作文件夹下打开`终端`或`cmd`，输入

```shell
python -m venv .venv
# .venv是虚拟环境名，你可以自定义一个其他的
```

就可以在当前文件夹下创建一个虚拟环境了

## 使用虚拟环境

### 准备

会用`Anaconda`的朋友可以继续用，我们这里给一个`Anaconda`的[安装教程](https://blog.csdn.net/lulukanshijie/article/details/150028587)备用，本教程使用`virtualenv`。  

如果没有安装的朋友先装一下。

```shell
pip install virtualenv
```

### 启动虚拟环境

#### Linux / MacOS

依然以`Ubuntu 22.04`举例，其他Linux发行版的朋友我相信你们能自己解决！

切换到你的工作文件夹下，然后输入

```shell
source ./.venv/bin/activate
```

#### Windows

切换到你的工作文件夹下，然后输入

```shell
.venv\Scripts\activate 
```

#### 启动结果

这样之后我们就成功启动了虚拟环境，在终端前会带有`(虚拟环境名)`，像这个样子。

![python启动了虚拟环境](../res/python_venv_activate.png)

#### 退出虚拟环境

在启动了虚拟环境的终端里输入

```shell
deactivate
```

就可以退出虚拟环境。

## 安装开发工具

一般我们不用`python`自带的`IDLE`，而是用更好的开发工具，这里推荐`VS Code`和`PyCharm`

### VSCode

登录[VSCode官网](https://code.visualstudio.com/download)，下载安装包安装VSCode。  

进入VSCode后，我们还要安装一些插件来优化我们的编程体验。  
进入插件窗口，输入python，下载以下插件

![python插件下载](../res/py_extensions.png)

然后就可以在VSCode里面愉快写Python了！

### Pycharm

Pycharm是Jetbrains公司研发的针对python的IDE(Integrated Development Environment)，好用但是要花钱。  

但是学生可以免费享用完整版。  

前往[Pycharm下载官网](https://www.jetbrains.com/pycharm/download/)下载对应安装包下载即可，同时我们去[Jetbrains用户界面](https://account.jetbrains.com/licenses/assets)，使用学生邮箱注册账户，申请Pycharm的完整版许可证。
