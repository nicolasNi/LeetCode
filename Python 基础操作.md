# Python 字符串

## Python join() 方法用于将序列中的元素以指定的字符连接生成一个新的字符串。

join()方法语法： 
>str.join(sequence)

```python
s1 = "-"
s2 = ""
seq = ("r", "u", "n", "o", "o", "b") # 字符串序列
print (s1.join( seq ))
print (s2.join( seq ))

r-u-n-o-o-b
runoob
```

## Python format 格式化函数
```python
>>>"{} {}".format("hello", "world")    # 不设置指定位置，按默认顺序
'hello world'
 
>>> "{0} {1}".format("hello", "world")  # 设置指定位置
'hello world'
 
>>> "{1} {0} {1}".format("hello", "world")  # 设置指定位置
'world hello world'
```

## Python isdigit() 方法检测字符串是否只由数字组成。
```python
str = "123456";  # Only digit in this string
print str.isdigit();

str = "this is string example....wow!!!";
print str.isdigit();

True
False
```
