## Python之多重循环 ##

在循环内部，还可以嵌套循环，我们来看一个例子：

```python
for x in ['A', 'B', 'C']:
    for y in ['1', '2', '3']:
        print x + y
```

x 每循环一次，y 就会循环 3 次，这样，我们可以打印出一个全排列：

A1
A2
A3
B1
B2
B3
C1
C2
C3