## Python中替换元素 ##

假设现在班里仍然是3名同学：

```python
>>> L = ['Adam', 'Lisa', 'Bart']
```

现在，Bart同学要转学走了，碰巧来了一个Paul同学，要更新班级成员名单，我们可以先把Bart删掉，再把Paul添加进来。

另一个办法是直接用Paul把Bart给替换掉：

```python
>>> L[2] = 'Paul'
>>> print L
L = ['Adam', 'Lisa', 'Paul']
```

对list中的某一个索引赋值，就可以直接用新的元素替换掉原来的元素，list包含的元素个数保持不变。

由于Bart还可以用 -1 做索引，因此，下面的代码也可以完成同样的替换工作：

```python
>>> L[-1] = 'Paul'
```