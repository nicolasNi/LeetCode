## Python3 ord() 函数
ord() 函数是 chr() 函数（对于 8 位的 ASCII 字符串）的配对函数，它以一个字符串（Unicode 字符）作为参数，返回对应的 ASCII 数值，或者 Unicode 数值。
```python
>>>ord('a')
97
>>> ord('€')
8364
```


## Python sum() 函数
sum() 方法对系列进行求和计算。
```python
>>>sum([0,1,2])  
3  
>>> sum((2, 3, 4), 1)        # 元组计算总和后再加 1
10
>>> sum([0,1,2,3,4], 2)      # 列表计算总和后再加 2
12
```

## Python3 map() 函数
map() 会根据提供的函数对指定序列做映射。
第一个参数 function 以参数序列中的每一个元素调用 function 函数，返回包含每次 function 函数返回值的新列表。
```python
>>>def square(x) :            # 计算平方数
...     return x ** 2
>>> map(square, [1,2,3,4,5])   # 计算列表各个元素的平方
[1, 4, 9, 16, 25]


nums = list(map(str, nums))  # 把int数组转换成字符串数组
```
