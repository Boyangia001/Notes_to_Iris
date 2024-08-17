## 一份个人笔记：Book_3_《数学要素》 | 第二章
### Bk3_Ch2_01

```python
num1 = 2
num2 = 3

# add two numbers
prod = num1*num2

# display the computation
print('The product of {0} and {1} is {2}'.format(num1, num2, prod))
```
这段代码的最后一部分使用了 Python 字符串的 format() 方法来格式化输出结果。  
其中，  
'The product of {0} and {1} is {2}': 这是一个字符串字面量，它包含了三个占位符：{0}, {1}, {2}。这些占位符将在稍后被 format() 方法替换为实际的值。  
.format(num1, num2, prod): 调用字符串的 format() 方法，并将 num1, num2, prod 三个变量作为参数传入。  
format() 的作用: format() 方法会将传入的参数依次替换字符串中的占位符。占位符的编号从 0 开始，对应着传入参数的位置。  
{0} 会被替换为 num1 的值，也就是 2。  
{1} 会被替换为 num2 的值，也就是 3。  
{2} 会被替换为 prod 的值，也就是 6。  
最终输出：
```python
The product of 2 and 3 is 6
```
### Bk3_Ch2_02

```python
# define a function to calculate factorial

num = int(input("Enter an integer: "))

factorial = 1

# check if the number is negative, positive or zero
if num < 0:
    print("Factorial does not exist for negative numbers")
elif num == 0:
    print("The factorial of 0 is ", factorial)
else:
#针对这个循环，注意python中的range not include the upper bound
    for i in range(1,num + 1):
       factorial = factorial*i
    print("The factorial of",num," is ",factorial)
```
至于python为什么采用左闭右开的区间取值形式，document中有解释：  
```python
word[:2]    # The first two characters
word[2:]    # Everything except the first two characters
```
这样的slice可以让 s[:i] + s[i:] = s 。  
对于非负indices，slice的长度是indices间的差，前提是这两个indices都在范围内。例如， word[1:3] 的长度是 2 。

### Bk3_Ch2_03
```python
import numpy as np

a_i = np.linspace(1,10,10)
print(a_i)

a_i_cumprod = np.cumprod(a_i)
np.set_printoptions(suppress=True)
print(a_i_cumprod)
```
#### np.linspace(start, stop, num) 
是 NumPy 中的一个函数，用于创建一个包含 num 个等间距数字的数组。  
start：序列的起始值。  
stop：序列的结束值（包含在序列中）。  
num：要生成的数字个数。    
a_i = np.linspace(1, 10, 10) 会创建一个包含 10 个数字的数组 a_i，这些数字均匀分布在 1 到 10 之间（包含 1 和 10）。  
输出：  
```python
[ 1.  2.  3.  4.  5.  6.  7.  8.  9. 10.]
```
#### 2. suppress=True
np.set_printoptions(suppress=True) 用于设置 NumPy 数组的打印选项。  
suppress：一个布尔值，用于控制是否抑制使用科学计数法打印小数。  
当 suppress=True 时，NumPy 会尽可能使用普通的小数表示法打印数组元素，即使它们非常小。  
np.set_printoptions(suppress=True) 会使得 a_i_cumprod 数组的输出结果不使用科学计数法。  

如果没有设置 suppress=True，a_i_cumprod 的输出结果可能如下所示（取决于 NumPy 版本）：
```python
[1.00000000e+00 2.00000000e+00 6.00000000e+00 2.40000000e+01
 1.20000000e+02 7.20000000e+02 5.04000000e+03 4.03200000e+04
 3.62880000e+05 3.62880000e+06]
```
设置了 suppress=True 后，输出结果会更易读：  
```python
[1 2 6 24 120 720 5040 40320 362880 3628800]
```
