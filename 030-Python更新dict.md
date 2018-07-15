## Python更新dict ##

dict是可变的，也就是说，我们可以随时往dict中添加新的 key-value。比如已有dict：

```python
d = {
    'Adam': 95,
    'Lisa': 85,
    'Bart': 59
}
```

要把新同学'Paul'的成绩 72 加进去，用赋值语句：

```python
>>> d['Paul'] = 72
```

再看看dict的内容：

```python
>>> print d
{'Lisa': 85, 'Paul': 72, 'Adam': 95, 'Bart': 59}
```

如果 key 已经存在，则赋值会用新的 value 替换掉原来的 value：

```python
>>> d['Bart'] = 60
>>> print d
{'Lisa': 85, 'Paul': 72, 'Adam': 95, 'Bart': 60}
```