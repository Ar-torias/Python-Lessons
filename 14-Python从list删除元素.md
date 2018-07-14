## Python从list删除元素 ##

Paul同学刚来几天又要转走了，那么我们怎么把Paul 从现有的list中删除呢？

如果Paul同学排在最后一个，我们可以用list的`pop()`方法删除：

```python
>>> L = ['Adam', 'Lisa', 'Bart', 'Paul']
>>> L.pop()
'Paul'
>>> print L
['Adam', 'Lisa', 'Bart']
```

**pop()**方法总是删掉list的最后一个元素，并且它还返回这个元素，所以我们执行 L.pop() 后，会打印出 'Paul'。

如果Paul同学不是排在最后一个怎么办？比如Paul同学排在第三：

```python
>>> L = ['Adam', 'Lisa', 'Paul', 'Bart']
```

要把Paul踢出list，我们就必须先定位Paul的位置。由于Paul的索引是2，因此，用` pop(2)`把Paul删掉：

```python
>>> L.pop(2)
'Paul'
>>> print L
['Adam', 'Lisa', 'Bart']
```