序列是Python中最基本的数据结构。序列中的每个元素都分配一个数字 - 它的位置，或索引，第一个索引是0，第二个索引是1，依此类推。
Python有6个序列的内置类型，但最常见的是列表和元组。
序列都可以进行的操作包括索引，切片，加，乘，检查成员。
此外，Python已经内置确定序列的长度以及确定最大和最小的元素的方法。
列表是最常用的Python数据类型，它可以作为一个方括号内的逗号分隔值出现。
列表的数据项不需要具有相同的类型
创建一个列表，只要把逗号分隔的不同的数据项使用方括号括起来即可。如下所示：
```python
list1 = ['Google', 'Runoob', 1997, 2000];
list2 = [1, 2, 3, 4, 5 ];
list3 = ["a", "b", "c", "d"];
```

## List pop()方法用于移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
```python
list1 = ['Google', 'Runoob', 'Taobao']
list1.pop()
print ("列表现在为 : ", list1)
list1.pop(1)
print ("列表现在为 : ", list1)

列表现在为 :  ['Google', 'Runoob']
列表现在为 :  ['Google']
```


## 删除列表元素
### 可以使用 del 语句来删除列表的的元素
```python
list = ['Google', 'Runoob', 1997, 2000]
print ("原始列表 : ", list)
del list[2]
print ("删除第三个元素 : ", list)

原始列表 :  ['Google', 'Runoob', 1997, 2000]
删除第三个元素 :  ['Google', 'Runoob', 2000]
```
### remove() 函数用于移除列表中某个值的第一个匹配项。
```python
list1 = ['Google', 'Runoob', 'Taobao', 'Baidu']
list1.remove('Taobao')
print ("列表现在为 : ", list1)
list1.remove('Baidu')
print ("列表现在为 : ", list1)

列表现在为 :  ['Google', 'Runoob', 'Baidu']
列表现在为 :  ['Google', 'Runoob']
```


## Python列表脚本操作符
Python 表达式|结果|描述
---|:--:|---:
len([1, 2, 3])|3|长度
[1, 2, 3] + [4, 5, 6]|[1, 2, 3, 4, 5, 6]|组合
['Hi!'] * 4|['Hi!', 'Hi!', 'Hi!', 'Hi!']|重复
3 in [1, 2, 3]|True|元素是否存在于列表中
for x in [1, 2, 3]: print(x, end=" ")|1 2 3|迭代

## Python列表截取与拼接
```python
>>>L=['Google', 'Runoob', 'Taobao']
>>> L[2]
'Taobao'
>>> L[-2]
'Runoob'
>>> L[1:]
['Runoob', 'Taobao']
```

## list[::-1]翻转的一些用法
[::-1] #顺序相反操作
[3::-1]就是从第3个位置坐标开始 截取顺序相反
```python
a = [1,3,4,2,'a','d']
print a[::-1]
['d', 'a', 2, 4, 3, 1]

print a[3::-1]
[2, 4, 3, 1]
```

## List sort()方法用于对原列表进行排序，如果指定参数，则使用比较函数指定的比较函数。
+ key -- 主要是用来进行比较的元素，只有一个参数，具体的函数的参数就是取自于可迭代对象中，指定可迭代对象中的一个元素来进行排序。
+ reverse -- 排序规则，reverse = True 降序， reverse = False 升序（默认）。
```python
list.sort( key=None, reverse=False)
```
```python
aList = ['Google', 'Runoob', 'Taobao', 'Facebook']
aList.sort()
print ( "List : ", aList)
List :  ['Facebook', 'Google', 'Runoob', 'Taobao']

降序
vowels = ['e', 'a', 'u', 'o', 'i']
vowels.sort(reverse=True)
print ( '降序输出:', vowels )
降序输出: ['u', 'o', 'i', 'e', 'a']

指定列表中的元素排序来输出列表：
def takeSecond(elem):
    return elem[1]
random = [(2, 2), (3, 4), (4, 1), (1, 3)]
random.sort(key=takeSecond)
print ('排序列表：', random)
排序列表：[(4, 1), (2, 2), (1, 3), (3, 4)]
```
