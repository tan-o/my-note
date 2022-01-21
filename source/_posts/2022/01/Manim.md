---
title: 安裝Manim的踩坑記錄
date: 2022-01-19 22:35:11
categories:
  - 學習
  - 踩坑
tags:
  - Manim
  - 基本
  - 安裝
---

+++info 注意

:::info
環境:
  - python-3.9
  - manim中3b1b的分支
  - dvisvgm-2.12
  - miktex-21.12.10(呢個版本號好重要!!!)
  - ffmpeg-2021.12.17
  - Pycario-1.20.1-cp39
:::

:::warning
以下内容,新手入門,且可能僅適用於本人,敬請留意!!!
:::

+++

# 基本環境
## Conda
:::info
本人裝的係miniconda
:::

### 安裝conda
這個唔使我講啦,一直點下一步,不過要記得勾選添加變量環境
關於conda的運用,可以看[conda的基本運用](/2022/01/conda的基本運用/index.html)

## dvisvgm
直接去[官網](https://dvisvgm.de/Downloads/)下載,自己下最新版就得啦,我最近睇dvisvgm已經更新到2.13,裝完之後記得要添加變量,最後將文件夾的名字改成dvisvgm,最後將版本號刪咗佢

## sox
可以去SourceForge下載,呢個係[下載鏈接](https://sourceforge.net/projects/sox/files/sox/)

## Pycario
### 安裝pycario
[下載鏈接](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo)
選擇適合自己的版本

