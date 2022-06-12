- figure 是 窗口
- axes 是 子区域
- 则 窗口 中可以包含多个 子区域

#### matlab 层级 
- Figure：顶层级，用来容纳所有绘图元素

- Axes：matplotlib宇宙的核心，容纳了大量元素用来构造一幅幅子图，一个figure可以由一个或多个子图组成

- Axis：axes的下属层级，用于处理所有和坐标轴，网格有关的元素

- Tick：axis的下属层级，用来处理所有和刻度有关的元素

```
plt.figure

fig.subplot

ax.set_title

ax.yaxis
ax.yaxis.set_minor_locater
ax.yaxis.set_major_formatter
ax.set_ylable
ax.yaxis.set_major_locator
ax.xaxis
ax.xaxis.set_minor_locater
ax.set_xlable

ax.legrnd
ax.grid
ax.scatter
ax.plot
ax.spines

```

![](https://matplotlib.org/_images/anatomy.png)

