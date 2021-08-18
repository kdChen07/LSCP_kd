matplotlib

#1 import 

```
import matplotlib
import matplotlib.pyplot as plt
import numpy as np
```

#2 data

```
X = np.arange(0,12.1,0.1)
Y = np.sin(X)
```

#3 plot

```python
plt.plot(X,Y,color = 'lime',linestyle = '-',linewidth = 2, \
         marker = '*',markerfacecolor = 'black',markedgecolor = 'red', \
         markersize = 4,markeredgewidth = 1)
#plt.scatter(x,y)
```

color定义线条颜色  linestyle定义线条类型 空值为空白线条  linewidth定义线条粗细

marker定义点类型  markfacecolor定义点内部颜色  markeredgecolor定义点边界颜色

markersize定义点大小  markeredgewidth定义点边界粗细

plt.scatter(x,y) 散点图

```python
ax1 = plt.gca()
ax1.set_title('Big Title',fontname = 'Arial',fontname = 20,weight='bold',\
             style='italic')  #设置标题、字体、字号、加粗、斜体
ax1.set_xlabel('time(UTC)')  #设置x轴内容
ax1.set_ylabel('T(C)')  #设置y轴内容

axi.set_xticks([0.2.5,7,11])  #设置刻度
axi.set_xtickslabels([J.A,N,E])  #为设置的刻度命名

ax1.tick_params(axis='both',direction='in',color='blue',\
               length=10,width=2)  #设置刻度类型 axis选择x、y轴 direction方向
                                   #color设置颜色 length设置长度 width设置粗细

plt.plot(X+2,Y，label='strange')  #平移
plt.legend(loc='best')  #图例 loc位置 best lower left左下角 uper right右上角

zorder  #图层顺序 数值越大 越在上层
```

保存

```python
plt.tight_layout()  #紧致布局
plt.savefig('./Big Title.png',dpi=400)  #dpi分辨率
```

