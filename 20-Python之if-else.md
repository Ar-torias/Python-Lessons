## Python之if-else ##

当 if 语句判断表达式的结果为 True 时，就会执行 if 包含的代码块：

```python
if age >= 18:
    print 'adult'
```

如果我们想判断年龄在18岁以下时，打印出 'teenager'，怎么办？

方法是再写一个 if:

```python
if age < 18:
    print 'teenager'
```

或者用 not 运算：

```python
if not age >= 18:
    print 'teenager'
```

细心的同学可以发现，这两种条件判断是“非此即彼”的，要么符合条件1，要么符合条件2，因此，完全可以用一个 if ... else ... 语句把它们统一起来：

```python
if age >= 18:
    print 'adult'
else:
    print 'teenager'
```

利用 if ... else ... 语句，我们可以根据条件表达式的值为 True 或者 False ，分别执行 if 代码块或者 else 代码块。

**注意:** else 后面有个“:”。