## Python中返回函数

Python的函数不但可以返回int、str、list、dict等数据类型，还可以返回函数！

例如，定义一个函数 f()，我们让它返回一个函数 g，可以这样写：

```python
def f():
    print 'call f()...'
    # 定义函数g:
    def g():
        print 'call g()...'
    # 返回函数g:
    return g
```

仔细观察上面的函数定义，我们在函数 f 内部又定义了一个函数 g。由于函数 g 也是一个对象，函数名 g 就是指向函数 g 的变量，所以，最外层函数 f 可以返回变量 g，也就是函数 g 本身。

调用函数 f，我们会得到 f 返回的一个函数：

```python
>>> x = f()   # 调用f()
call f()...
>>> x   # 变量x是f()返回的函数：
<function g at 0x1037bf320>
>>> x()   # x指向函数，因此可以调用
call g()...   # 调用x()就是执行g()函数定义的代码
```

请注意区分返回函数和返回值：

```python
def myabs():
    return abs   # 返回函数
def myabs2(x):
    return abs(x)   # 返回函数调用的结果，返回值是一个数值
```

返回函数可以把一些计算延迟执行。例如，如果定义一个普通的求和函数：

```python
def calc_sum(lst):
    return sum(lst)
```

调用calc_sum()函数时，将立刻计算并得到结果：

```python
>>> calc_sum([1, 2, 3, 4])
10
```

但是，如果返回一个函数，就可以“延迟计算”：

```python
def calc_sum(lst):
    def lazy_sum():
        return sum(lst)
    return lazy_sum
```

\# 调用calc_sum()并没有计算出结果，而是返回函数:

```python
>>> f = calc_sum([1, 2, 3, 4])
>>> fp
<function lazy_sum at 0x1037bfaa0>
```

\# 对返回的函数进行调用时，才计算出结果:

```python
>>> f()
10
```

由于可以返回函数，我们在后续代码里就可以决定到底要不要调用该函数。

### 任务

请编写一个函数calc_prod(lst)，它接收一个list，返回一个函数，返回函数可以计算参数的乘积。

```python
def calc_prod(lst):
    def prod():
        return reduce(lambda x, y : x * y, lst)
    return prod

f = calc_prod([1, 2, 3, 4])
print f()
```

或者：

```python
def calc_prod(lst):
    def prod(x1, x2):
        return x1 * x2
    def c_prod():
        return reduce(prod, lst)
    return c_prod

f = calc_prod([1, 2, 3, 4])
print f()
```

