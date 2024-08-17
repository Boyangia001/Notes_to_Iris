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

