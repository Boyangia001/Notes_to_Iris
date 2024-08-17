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
总结: format() 方法提供了一种灵活的方式来格式化字符串，使得我们可以将变量的值嵌入到字符串中，使代码更易读和易于维护。
