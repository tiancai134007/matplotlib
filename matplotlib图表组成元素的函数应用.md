# plot()---展现变量的趋势变化
调用代码：plt.plot(x,y,ls=,lw=,label=)
参数说明：
* x: x轴上的数值
* y: y轴上的数值
* ls：图的线条风格
* lw：图的线条宽度
* label：标记图形内容的标签文本
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np

    x = np.linspace(0.05,10,1000)
    y = np.cos(x)
    plt.plot(x,y,ls="-",lw=2,label="plot figure")
    plt.legend()
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/plot.png)

# scatter()---寻找变量之间的关系
调用代码：plt.scatter(x,y,c=,label=)
参数说明：
* x: x轴上的数值
* y: y轴上的数值
* c: 散点图中的标记的颜色
* label：标记图形内容的标签文本
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.random.rand(1000)
    plt.scatter(x,y,c="red",label="plot figure")
    plt.legend()
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/scatter.png)

# xlabel()与ylabel（）---设置x轴与y轴的标签文本
调用代码：plt.xlabel（string）
参数说明：
* string: 标签文本内容
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="g",label="plot figure")
    plt.legend()
    plt.xlabel("x-axis")
    plt.ylabel("y-axis")
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/xlabel.png)

# grid()----绘制刻度线的网格线
调用代码：plt.grid（linestyle="",color=""）
参数说明：
* linestyle: 网格线的线条风格
* color：网格线的线条颜色 
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.xlabel("x-axis")
    plt.ylabel("y-axis")
    plt.grid(linestyle=":",color="r")
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/grid.png)

# axhline()与axvline（）----绘制平行于x轴与y轴的水平参考线
调用代码：plt.axhline（y=, c="",ls="",lw=）
参数说明：
* y: 水平参考线的出发点
* c：参考线的线条颜色
* ls：线条风格
* lw：线条宽度 
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.axhline(y=0.0,c="g",ls="--",lw=2)
    plt.axvline(x=4.0,c="r",ls="--",lw=2)
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/axhline.png)

# axvspan()与axhspan（）----绘制垂直于x轴与y轴的参考区域
调用代码：plt.axvspan（xmin=1.0, xmax=2.0,facecolor="",alpha=）
参数说明：
* xmin: 参考区域的起始位置
* xmax：参考区域的终止位置
* facecolor：区域填充颜色
* alpha：填充颜色的透明度 
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.axvspan(xmin=4.0,xmax=6.0,facecolor="y",alpha=0.5)
    plt.axhspan(ymin=0.0,ymax=0.5,facecolor="y",alpha=0.5)
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/axvspan.png)

# annotate()----添加图形内容细节的指向型注释文本
调用代码：plt.annotate（string，xy=,xytext=,weight=,color=,arrowprops=dict()）
参数说明：
* string: 图形内容的注释文本
* xy：被注释图形内容的位置坐标
* xytext：注释文本的位置坐标
* weight：注释文本的字体粗细风格
* color: 注释文本的字体颜色
* arrowprops: 指示被注释内容的箭头的属性字典 
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.annotate("maximum",xy=(np.pi/2,1.0),xytext=((np.pi/2) + 1.0,.8),weight="bold",color="b",
             arrowprops=dict(arrowstyle="->",connectionstyle="arc3",color="b"))
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/annotate.png)

# text()----添加图形内容细节的无指向型注释文本
调用代码：plt.text（x,y,string,xy=,weight=,color=）
参数说明：
* x: 注释文本内容所在位置的横坐标
* y：注释文本内容所在位置的纵坐标
* string：注释文本内容
* weight：注释文本内容的粗细风格
* color: 注释文本内容的字体颜色

#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.text(3.10,0.09,"y=sin(x)",weight="bold",color="b")
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/text.png)

# title()----添加图形内容的标题
调用代码：plt.title（string）
参数说明：
* string：图形内容的标题文本
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend()
    plt.title("y=sin(x)")
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/title.png)

# legend()----标示不同图形的文本标签图例
调用代码：plt.legend（loc
）
参数说明：
* loc：图例在图中的地理位置
#### 代码实现
    import matplotlib.pyplot as plt
    import numpy as np
    x = np.linspace(0.05 ,10 ,1000)
    y = np.sin(x)
    plt.plot(x,y,ls="-.",lw=2,c="c",label="plot figure")
    plt.legend(loc="lower left")
    plt.show()
#### 结果展示
![image](https://github.com/tiancai134007/matplotlib/blob/main/%E5%9B%BE%E5%83%8F/legend.png)


