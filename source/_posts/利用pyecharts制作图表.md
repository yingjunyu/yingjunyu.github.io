---
title: 利用pyecharts制作图表
date: 2018-08-16 10:55:23
tags: PYTHON
---

## 利用Pyecharts制作图表

pyecharts是基于Echart图表的一个类库，主要基于Web浏览器进行显示，绘制的图形比较多，包括折线图、柱状图、饼图、漏斗图、地图、极坐标图等，代码量少，而且很灵活，绘制出来的图形也很美观。

### 1. 安装pyecharts
```
pip install pyecharts
```

### 2. 一般性应用（制作柱状图为例）
```
from pyecharts import Bar

attr = ['JAVA', 'C++', 'C#', 'PYTHONE']
value = ['100', '120', '85', '150']
bar = Bar("柱状图", "应用率")
bar.add("编程语言", attr, value, is_label_show=True)
bar.render()
```
以上代码在执行以后会在代码所在的目录下生成一个render.html文件，在浏览器里打开这个文件就可以看到一个柱状图的效果了。