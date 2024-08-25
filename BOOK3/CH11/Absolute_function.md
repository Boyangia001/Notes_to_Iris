# 绘制绝对值函数
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
