# Balabala
一些有创意的编程题
## 无语言输出

编写一个程序，输出自己的源代码，即所谓的Quine程序。但是，你不能使用任何语言内置的函数或方法，如 print，echo 等，来输出源代码。

附加条件：代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

示例代码（：
```python
File "/a.py", line 1
    File "/a.py", line 1
         ^
SyntaxError: invalid syntax
```
你就说输出了没有嘛/恼

## No.Number

编写一个程序获得一个值为9的变量，但是程序的源码中不得出现任何数字。

附加条件：代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

示例代码：
使用len的基本方法
```python
a=len("xxx")**2
```
歪门邪道的高级手段
```python
a=ord('\t')
```
Ruby写起来似乎更短一些
```ruby
a="\t".ord
```
## 魔方矩阵

编写一个程序，生成一个6*6的魔方矩阵（Magic Square）。魔方矩阵是一个由正整数构成的方阵，其中每行、每列和主对角线上的所有数的和都相等。

附加条件：代码中不得出现数字，代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

不允许自己嗯造一个语言出来。

## 3n+1

编写一个程序，实现3n+1猜想。对于任何一个正整数，如果它是奇数，则对它乘3再加1，如果它是偶数，则对它除以2，如此循环，最终都将得到1。

格式要求:使用","分割数字1000完成3n+1猜想的递归过程

即：1000,500,250,125,376,188,94,47,142,71,214,107,322,161,484,242,121,...,1

附加条件：源代码中不允许出现数字。代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

不允许自己嗯造一个语言出来。

## 质数大师

输出100以内的所有质数

源码的每个字符的出现次数必须是1或者质数

附加条件：不允许写注释（但是允许死代码。代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

不允许自己嗯造一个语言出来。

Python实现（只会用死代码了，但是真的不长）

```python
v=range
pp=lambda n:[i for i in v(2,n)if 0 not in[i%p for p in v(2,i)]]
print(pp(100))
r'\'nnnii()'
```

附带检查工具(GPT4友情提供）

```python
from collections import Counter
import math

def is_prime(n):
    """判断一个数是否为质数"""
    if n < 2:
        return False
    for i in range(2, math.isqrt(n) + 1):
        if n % i == 0:
            return False
    return True

def all_chars_prime_count(multi_line_string):
    """判断一个多行字符串中出现的所有字符（不包括空格）的出现次数是否全部为质数"""
    counter = Counter(multi_line_string.replace(" ", ""))
    return all(is_prime(count) for count in counter.values())

# 测试用例
multi_line_string = """
Hello World!
This is a test case.
"""
print(all_chars_prime_count(multi_line_string))
```

## 回文联

编写一个程序，判断用户输入的字符串是否为回文。回文是指从前往后读和从后往前读都是一样的字符串。

附加条件：源代码本身也必须是一个回文。代码长度最短者获胜。

不允许联网，不允许通过环境变量、文件名、编译参数等作弊。

不允许自己嗯造一个语言出来。

实现：

```
我不会
```
