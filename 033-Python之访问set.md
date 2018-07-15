## Python之访问set ##

由于**set存储的是无序集合**，所以我们没法通过索引来访问。

访问 set中的某个元素实际上就是判断一个元素是否在set中。

例如，存储了班里同学名字的set：

```python
>>> s = set(['Adam', 'Lisa', 'Bart', 'Paul'])
```

我们可以用 in 操作符判断：

Bart是该班的同学吗？

```python
>>> 'Bart' in s
True
```

Bill是该班的同学吗？

```python
>>> 'Bill' in s
False
```

bart是该班的同学吗？

```python
>>> 'bart' in s
False
```

看来大小写很重要，'Bart' 和 'bart'被认为是两个不同的元素。