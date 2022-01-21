---
title: conda的基本運用
date: 2022-01-20 14:57:11
categories:
  - 學習
  - 運用
tags:
  - conda
  - 基本
---

- [1. conda 换源](#1-conda-换源)
- [2. 升级conda](#2-升级conda)
- [3. conda基本使用](#3-conda基本使用)
- [4. 安装包](#4-安装包)

# 1. conda 换源

:::info
此源為清華源
:::

-   在cmd中输入：

```python
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --set show_channel_urls yes
```

-   或者可以通过修改用户目录下的 .condarc 文件:

```python
channels:
  - defaults
show_channel_urls: true
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```

即可添加 Anaconda Python 免费仓库。`Windows 用户无法直接创建名为 .condarc 的文件，可先执行 conda config --set show_channel_urls yes 生成该文件之后再修改。`

# 2. 升级conda

```python
conda update <包的名字>
```

# 3. conda基本使用

```python
conda create -n <环境名称> python=<版本号> #创建环境
conda activate <环境名称> #启用环境
conda deactivate #退出环境
conda info --envs #查看当前存在的环境
conda remove -n <环境名称> --all #删除环境
conda install python=<版本号> #更新环境
conda list -n <环境名称> #查看指定环境中已安装的包
```

# 4. 安装包

```python
conda install <包的名称>
pip install <包的名称>
```
