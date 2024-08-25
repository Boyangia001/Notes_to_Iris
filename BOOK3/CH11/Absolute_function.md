# 绘制绝对值函数
提供了一种解法，配色方案、坐标轴标注方式、网格线大小与示例图并不完全一致。
```python
import matplotlib.pyplot as plt
import numpy as np

# 定义 x 轴的范围
x = np.linspace(-2, 2, 400)

# 绘制不同斜率 k 的绝对值函数 y = k * |x|
k_values = [0.5, 1, 1.5, 2, 2.5]

plt.figure(figsize=(6, 6))
for k in k_values:
    y = k * np.abs(x)
    plt.plot(x, y, label=f'k = {k}')

plt.axhline(0, color='black',linewidth=0.5) # 添加 x 轴
plt.axvline(0, color='black',linewidth=0.5) # 添加 y 轴
plt.xlim([-2, 2])
plt.ylim([-2, 2])
plt.grid(True)

# 设置标签
plt.xlabel('x')
plt.ylabel('y')

# 显示图例
#plt.legend()

# 显示图形
plt.show()
```
另一种
```python
import matplotlib.pyplot as plt
import numpy as np

# 定义 x 轴的范围
x = np.linspace(-2, 2, 400)

# 绘制不同斜率 k 的绝对值函数 y = k * |x|
k_values = [0.5, 1, 1.5, 2, 2.5]
colors = ['blue', 'cyan', 'orange', 'red', 'yellow']  # 配色方案

plt.figure(figsize=(6, 6))
for k, color in zip(k_values, colors):
    y = k * np.abs(x)
    plt.plot(x, y, color=color, label=f'k = {k}', linewidth=2)

plt.axhline(0, color='black', linewidth=0.5)  # 添加 x 轴
plt.axvline(0, color='black', linewidth=0.5)  # 添加 y 轴
plt.xlim([-2, 2])
plt.ylim([-2, 2])
plt.grid(True)

# 设置标签
plt.xlabel('x')
plt.ylabel('y')

# 设置坐标轴刻度
plt.xticks(np.arange(-2, 3, 1))
plt.yticks(np.arange(-2, 3, 1))

# 隐藏顶部和右侧的边框线
plt.gca().spines['top'].set_color('none')
plt.gca().spines['right'].set_color('none')

# 显示图例
plt.legend()

# 显示图形
plt.show()
```
