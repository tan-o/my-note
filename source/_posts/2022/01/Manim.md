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

- [基本環境](#基本環境)
  - [Conda](#conda)
    - [安裝conda](#安裝conda)
  - [dvisvgm](#dvisvgm)
  - [sox](#sox)
  - [Pycario](#pycario)
    - [安裝pycario](#安裝pycario)
  - [ffmpeg](#ffmpeg)
  - [Miklex](#miklex)
  - [下載Manim](#下載manim)
- [調試](#調試)
- [中文支持](#中文支持)

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
![2022-01-21T161524](2022-01-21T161524.png)

`cp後邊的數字代表你的python的版本`

下載后將文件放在C盤根目錄,右鍵,用`cmd(wt)` ![2022-01-21T161350](2022-01-21T161350.png)
舊版就在文件的地址欄輸入`cmd`
```bash
cd c:\
pip install pycairo-1.20.1-cp39-cp39-win_amd64.whl
```

## ffmpeg
[下載鏈接](https://www.ffmpeg.org/download.html#build-windows)

![2022-01-21T161555](2022-01-21T161555.png)

選擇Windows下載(隨便一個啦) !!埋果你的系統係Windows!!

## Miklex
[下載鏈接](https://miktex.org/)
亦有人推薦下載`texlive`,!!我用的時候總是報錯,所以最終都係放棄了.!!
安裝的時候也有一個坑,默認普通用戶安裝就得啦,裝完之後以管理員的模式打開`cmd`,輸入:
```bash
regsvr32 MiKTeX211210-packagemanager.dll
regsvr32 MiKTeX211210-packagemanager-PS.dll
regsvr32 MiKTeX211210-core.dll
regsvr32 MiKTeX211210-core-PS.dll
```
其中,那個`211210`係你miktex的版本號!!巨坑啊(╯‵□′)╯︵┻━┻!!

## 下載Manim
[下载链接](https://github.com/3b1b/manim)
下載之後建議解壓到冇中文的路徑

進入到manim,運行:
```bash
pip install manimgl
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
```
由於網絡問題,有報錯就運行多幾次,並安裝缺失的

# 調試
儅一切都安裝完后,就可以運行喇,進入到manim的目錄,打開cmd,運行:
```bash
manimgl .\example_scenes.py
```
就會得到
![2022-01-21T162024](2022-01-21T162024.png)
將呢10個全部運行一次,埋過冇報錯的話,恭喜🎉🎉🎉,你安裝成功

+++info 演示

{% media video %}
- name: "AnimatingMethods"
  url: AnimatingMethods.mp4
- name: "CoordinateSystemExample"
  url: CoordinateSystemExample.mp4
- name: "GraphExample"
  url: GraphExample.mp4
- name: "OpeningManimExample"
  url: OpeningManimExample.mp4
- name: "TexTransformExample"
  url: TexTransformExample.mp4
- name: "TextExample"
  url: TextExample.mp4
- name: "UpdatersExample"
  url: UpdatersExample.mp4
{% endmedia %}

+++

# 中文支持
找到這個文件
![2022-01-21T161836](2022-01-21T161836.png)
![2022-01-21T161902](2022-01-21T161902.png)
按照注釋中的進行修改
仲要修改字體,使得支持中文字體
![2022-01-21T164947](2022-01-21T164947.png)


