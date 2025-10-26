# Python 安装教程

## 环境安装

工欲善其事，必先利其器，先把最基础的python解释器下载下来吧。

### Windows

通过python官网下载，具体可参照[安装教程](https://blog.csdn.net/maiya_yayaya/article/details/131450517)  ，记得勾选`添加到PATH`一项
可以和本教程一致，安装`Python 3.9.24`，或者其他版本。

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

### 验证安装成功

打开`终端`或`cmd`，输入

```shell
python --version
# 或者输入
python3 --version 
```

弹出来的是版本号就对了，就像这样

![python弹出版本号](../res/python_version.png)

## 本教程环境

本教程使用`Ubuntu 22.04 LTS`系统，python版本为`Python 3.9.24`，使用`anaconda`创建的虚拟环境。  
> 关于使用的不是`Windows`或`Mac`系统这点不必太慌张，`python`支持跨平台，同样的源码可以在这几个系统中运行出一样的结果。

## 虚拟环境

虚拟环境是一个用户自己定制的特殊编程环境，和正常使用python的方式一致，但是各个虚拟环境是独立的，和系统默认的环境也是独立的。

虚拟环境的重要性在于，很多python项目的环境差别很大，python版本，安装的包的种类，版本等等都可能不同。  
如果没有虚拟环境，那么所有python项目都要共享同一个环境，这会导致我们在研究不同项目时都要对原有环境做一定适配，包括但不限于

- python版本升级/降级
- 包重新安装
- 包版本升级/降级

非常麻烦，因此我们才引入了`虚拟环境`的概念。  
如果你当前不在虚拟环境中，那么你使用的就是系统默认的环境。

### 使用虚拟环境

#### anaconda

`anaconda`是一个包管理器，在其中你可以自己创建环境，让多个项目使用同一个环境，甚至可以修改`python版本`。

具体安装可以参考[安装教程](https://anaconda.org.cn/anaconda/install/)。

我们大概罗列一下conda的指令，如果感觉指令太多，可以先掌握

- `conda activate`
- `conda deactivate`
- `conda install`
- `conda list`

这四条指令和相关内容，其他的可以深入学习过后再阅读和了解。

我们后续的conda相关操作也会带着大家一起做的，可以在实际使用的过程中了解和学习。

| 功能分类      | 指令示例                                       | 说明                                                                     |
|-----------|--------------------------------------------|------------------------------------------------------------------------|
| **版本与帮助** | `conda --version`                          | 查看 Conda 版本                                                            |
|           | `conda -h` 或 `conda --help`                | 查看 Conda 帮助文档                                                          |
|           | `conda <命令> -h` （如 `conda create -h`）      | 查看具体命令的帮助（如创建环境的参数说明）                                                  |
| **环境管理**  | `conda env list` 或 `conda info --envs`     | 列出所有虚拟环境（`*` 表示当前激活环境）                                                 |
|           | `conda create -n <环境名>`                    | 创建新环境（默认继承 base 环境的 Python 版本）                                         |
|           | `conda create -n <环境名> python=3.9`         | 创建指定 Python 版本的环境（如 Python 3.9）                                        |
|           | `conda activate <环境名>`                     | 激活虚拟环境（Windows 用 cmd/PowerShell，Linux/macOS 通用）                        |
|           | `conda deactivate`                         | 退出当前虚拟环境                                                               |
|           | `conda remove -n <环境名> --all`              | 删除指定虚拟环境（需先退出该环境）                                                      |
|           | `conda rename -n <旧名> -n <新名>`             | 重命名虚拟环境（Conda 4.14+ 支持）                                                |
| **包管理**   | `conda list`                               | 列出当前环境已安装的包                                                            |
|           | `conda list -n <环境名>`                      | 列出指定环境的已安装包                                                            |
|           | `conda install <包名>`                       | 在当前环境安装指定包（如 `conda install numpy`）                                    |
|           | `conda install <包名>=1.2.3`                 | 安装指定版本的包（如 `conda install pandas=1.5.3`）                               |
|           | `conda install -n <环境名> <包名>`              | 给指定环境安装包（无需激活该环境）                                                      |
|           | `conda update <包名>`                        | 更新当前环境的指定包                                                             |
|           | `conda update --all`                       | 更新当前环境的所有包                                                             |
|           | `conda remove <包名>`                        | 卸载当前环境的指定包                                                             |
|           | `conda search <包名>`                        | 搜索 Conda 仓库中可用的包版本                                                     |
| **镜像配置**  | `conda config --show channels`             | 查看当前配置的镜像源                                                             |
|           | `conda config --add channels <镜像地址>`       | 添加镜像源（如清华源：`https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/`） |
|           | `conda config --remove channels <镜像地址>`    | 删除指定镜像源                                                                |
|           | `conda config --set show_channel_urls yes` | 显示包的安装来源（方便确认是否用了镜像）                                                   |
| **其他常用**  | `conda clean -p`                           | 清理未使用的包缓存（节省磁盘空间）                                                      |
|           | `conda clean -y --all`                     | 彻底清理所有缓存（包括索引和未使用包）                                                    |
|           | `conda env export > environment.yml`       | 导出当前环境的依赖清单到文件                                                         |
|           | `conda env create -f environment.yml`      | 根据依赖清单创建新环境                                                            |

##### 环境变量配置

虽然Anaconda官方不推荐配置，但是我们为了使用的方便一般还是会配置一下的，接下来配置一下。

(暂待填充。。。)

#### virtualenv

这是`python`自带的一个虚拟环境工具，我们这里仅仅提及，想深入的朋友可以自行了解。

## 安装开发工具

一般我们不用`python`自带的`IDLE`，而是用更好的开发工具，这里推荐`VS Code`和`PyCharm`

### VSCode

登录[VSCode官网](https://code.visualstudio.com/download)，下载安装包安装VSCode。  

进入VSCode后，我们还要安装一些插件来优化我们的编程体验。  
进入插件窗口，输入python，下载以下插件

![python插件下载](../res/py_extensions.png)

然后就可以在VSCode里面愉快写Python了！

### Pycharm

`Pycharm`是Jetbrains公司研发的针对python的IDE(Integrated Development Environment)，好用但是要花钱。  

但是学生可以免费享用完整版。  

前往[Pycharm下载官网](https://www.jetbrains.com/pycharm/download/)下载对应安装包下载即可，同时我们去[Jetbrains用户界面](https://account.jetbrains.com/licenses/assets)，使用学生邮箱注册账户，申请Pycharm的完整版许可证。
