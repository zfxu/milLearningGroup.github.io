---
title: Anaconda 与 Jupyter Notebook
layout: single
permalink: /docs/anaconda-and-jupyter-notebook/
author: Accepted Doge
sidebar:
  nav: "docs"
---

## Anaconda安装

Anaconda 是一个包含数据科学常用包的发行版本。它基于 conda —— 一个包和环境管理器 ——衍生而来。**你将使用 conda 创建环境，以便分隔使用不同 Python 版本和/或不同包的项目。**你还将使用它在环境中安装、卸载和更新包。通过使用 Anaconda，使处理数据的过程更加愉快。这是官网的[下载地址](https://www.continuum.io/downloads)，不过推荐大家使用国内的[清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/)，速度非常的快。在网站右边侧栏可以找到**常用发行版 iso 和应用工具安装包直接下载** ，里面的 Conda 列表可以找到对应的 Anaconda 版本。

安装时推荐安装在系统的默认路径。不过在安装好 Anaconda 之后，为了加快以后各种包的下载速度，推荐添加清华的 Anaconda 仓库镜像以及维护的第三方镜像，[网站上也有明确的教程](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)。

为了避免报错，推荐在默认环境下更新所有的包。打开 Anaconda Prompt （或者 Mac 下的终端），键入：

```python
conda upgrade --all
```

并在提示是否更新的时候输入 y（Yes）以便让更新继续。初次安装下的软件包版本一般都比较老旧，因此提前更新可以避免未来不必要的问题。可以在终端或命令提示符中键入 `conda list`，以查看你安装的内容。

## Anaconda基础指令

### 管理包

安装了 Anaconda 之后，管理包是相当简单的。要安装包，请在终端中键入 `conda install package_name`。例如，要安装 numpy，请键入 `conda install numpy`。

你还可以同时安装多个包。类似 `conda install numpy scipy pandas` 的命令会同时安装所有这些包。还可以通过添加版本号（例如 `conda install numpy=1.10`）来指定所需的包版本。

Conda 还会自动为你安装依赖项。例如，`scipy` 依赖于 `numpy`，因为它使用并需要 `numpy`。如果你只安装 `scipy` (`conda install scipy`)，则 conda 还会安装 `numpy`（如果尚未安装的话）。

大多数命令都是很直观的。要卸载包，请使用 `conda remove package_name`。要更新包，请使用 `conda update package_name`。如果想更新环境中的所有包（这样做常常很有用），请使用 `conda update --all`。最后，要列出已安装的包，请使用前面提过的 `conda list`。

如果不知道要找的包的确切名称，可以尝试使用 `conda search search_term` 进行搜索。例如，我知道我想安装 [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)，但我不清楚确切的包名称。因此，我尝试执行 `conda search beautifulsoup`。它返回可用的 Beautiful Soup 包的列表，并列出了相应的包名称 `beautifulsoup4`。

### 管理环境

#### 创建环境

可以使用 conda 创建环境以隔离项目。要创建环境，请在终端中使用 `conda create -n env_name list of packages`。在这里，`-n env_name` 设置环境的名称（`-n` 是指名称），而 `list of packages` 是要安装在环境中的包的列表。例如，要创建名为 `my_env` 的环境并在其中安装 numpy，请键入 `conda create -n my_env numpy`。

创建环境时，可以指定要安装在环境中的 Python 版本。这在你同时使用 Python 2.x 和 Python 3.x 中的代码时很有用。要创建具有特定 Python 版本的环境，请键入类似于 `conda create -n py3 python=3` 或 `conda create -n py2 python=2` 的命令。实际上，我在我的个人计算机上创建了这两个环境。我将它们用作与任何特定项目均无关的通用环境，以处理普通的工作（可轻松使用每个 Python 版本）。这些命令将分别安装 Python 3 和 2 的最新版本。要安装特定版本（例如 Python 3.5），请使用 `conda create -n py python=3.5`。

#### 进入环境

创建了环境后，在 OSX/Linux 上使用 `source activate my_env` 进入环境。在 Windows 上，请使用 `activate my_env`。

进入环境后，你会在终端提示符中看到环境名称，它类似于 `(my_env) ~ $`。环境中只安装了几个默认的包，以及你在创建它时安装的包。可以使用 `conda list` 检查这一点。在环境中安装包的命令与前面一样：`conda install package_name`。不过，这次你安装的特定包仅在你进入环境后才可用。要离开环境，请键入 `source deactivate`（在 OSX/Linux 上）。在 Windows 上，请使用 `deactivate`。


#### 保存和加载环境

共享环境这项功能确实很有用，它能让其他人安装你的代码中使用的所有包，并确保这些包的版本正确。可以使用 `conda env export > environment.yaml` 将包保存为 [YAML](http://www.yaml.org/)。第一部分 `conda env export` 输出环境中的所有包的名称（包括 Python 版本）。导出命令的第二部分 `> environment.yaml` 将导出的文本写入到 YAML 文件 `environment.yaml` 中。现在可以共享此文件，而且其他人能够创建和你用于项目相同的环境。

要通过环境文件创建环境，请使用 `conda env create -f environment.yaml`。这会创建一个新环境，而且它具有在 `environment.yaml` 中列出的同样的库。

#### 列出环境

如果忘记了环境的名称（我有时会这样），可以使用 `conda env list` 列出你创建的所有环境。你会看到环境的列表，而且你当前所在环境的旁边会有一个星号。默认的环境（即当你不在环境中时使用的环境）名为 `root`。

#### 删除环境

如果你不再使用某些环境，可以使用 `conda env remove -n env_name` 删除指定的环境（在这里名为 `env_name`）。

#### 使用建议

不同的 Python 版本和不同的科学实验环境最好是独立的。

## Jupyter Notebooks 使用说明

- 点击此处查看 [官网文档](http://jupyter.org/documentation.html) （英文）
- [nbviewer](https://nbviewer.jupyter.org/)  是一个在线分享 Jupyter Notebooks 代码的好工具

新版本的 Anaconda 是自带 Jupyter Notebooks 的，Anaconda 终端中输入`jupyter notebook `便可以在当前路径下运行（想要切换路径可以修改配置文件，也可以在终端手动切换等等）。Jupyter Notebook 有两种键盘输入模式。编辑模式，允许你往单元中键入代码或文本，这时的单元框线是绿色的。命令模式，键盘输入运行程序命令，这时的单元框线是灰色。在 nbviewer 上面有 [notebook 说明文档](https://nbviewer.jupyter.org/github/ipython/ipython/blob/4.0.x/examples/Notebook/Index.ipynb) ，你可以预览一下效果。使用的一些快捷键在网络上可以很方便的找到。

如果现在你还没有学习 **Python** ，不用担心，我们将会很快开始 Python 语言的学习。

## 参考资料

- cama_summer_school_2017 Week01 [README文档](https://github.com/milLearningGroup/cama_summer_school_2017/blob/master/Week_1/README.md)
- Accepted Doge 博客 Udacity课程 部分笔记
- Jupyter Notebooks 快捷键部分参考自网络