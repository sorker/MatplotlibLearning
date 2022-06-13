- figure 是 窗口
- axes 是 子区域
- 则 窗口 中可以包含多个 子区域

#### matlab 层级 
- Figure：顶层级，用来容纳所有绘图元素

- Axes：matplotlib宇宙的核心，容纳了大量元素用来构造一幅幅子图，一个figure可以由一个或多个子图组成

- Axis：axes的下属层级，用于处理所有和坐标轴，网格有关的元素

- Tick：axis的下属层级，用来处理所有和刻度有关的元素

### 一些设置
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

#### 思考题
- 1、请思考两种绘图模式的优缺点和各自适合的使用场景
 - 第一种适合多子区域的情况，设置灵活，第二种适合单图显示，简单方便。
- 2、在第五节绘图模板中我们是以OO模式作为例子展示的，请思考并写一个pyplot绘图模式的简单模板

```
# step1 准备数据
x = np.linspace(0, 2, 100)
y1 = x**2
y2 = x**3

# step2 设置绘图样式，这一模块的扩展参考第五章进一步学习，这一步不是必须的，样式也可以在绘制图像是进行设置
mpl.rc('lines', linewidth=4, linestyle='-.')

# step3 定义布局， 这一模块的扩展参考第三章进一步学习
fig, (ax1, ax2) = plt.subplots(1,2)

# step4 绘制图像， 这一模块的扩展参考第二章进一步学习
ax1.plot(x, y1, label='linear')
ax2.plot(x, y2, label='linear')

# step5 添加标签，文字和图例，这一模块的扩展参考第四章进一步学习
ax1.set_xlabel('x label')
ax1.set_ylabel('y label')
ax1.set_title("Simple Plot")
ax1.legend()
ax2.set_xlabel('x label')
ax2.set_ylabel('y label')
ax2.set_title("Simple Plot")
ax2.legend()
plt.show()
```