字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值 key=>value 对用冒号 : 分割，每个键值对之间用逗号 , 分割，整个字典包括在花括号 {} 中 。键一般是唯一的，如果重复最后的一个键值对会替换前面的，值不需要唯一。
```python
>>>dict = {'a': 1, 'b': 2, 'b': '3'}
>>> dict['b']
'3'
>>> dict
{'a': 1, 'b': '3'}
```

## 访问字典里的值
```python
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
print "dict['Name']: ", dict['Name']
print "dict['Age']: ", dict['Age']

dict['Name']:  Zara
dict['Age']:  7
```

## 删除字典元素
```python
dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
del dict['Name']  # 删除键是'Name'的条目
dict.clear()      # 清空字典所有条目
del dict          # 删除字典
```
