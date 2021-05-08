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


