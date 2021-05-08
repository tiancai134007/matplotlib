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
