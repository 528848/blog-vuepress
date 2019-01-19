# tensorflow学习之基础语法
### 模块的引入
```python
import tensorflow as tf
```

### 常量的定义
```python
data1 = tf.constant(2.5)
```

### 变量的定义
```python
data2 = tf.Variable(10,name="var")
```

### session的定义和执行
tensorflow中所有的操作都在session中进行

```python
sess = tf.Session()
print(sess.run(data1))
//变量需要初始化，不然会报异常
init = tf.global_variables_initializer()
sess.run(init)
print(sess.run(data2))
//关闭session
sess.close()
```

### tensorflow实质
1. 张量tensor和计算图grahps，张量表示的是数据，op代表操作，grahps代表运算图。
![](https://ws2.sinaimg.cn/large/006tNbRwgy1fugc3q63uyj30vm0gq0vi.jpg)

### 常量、变量的四则运算
```python
import tensorflow as tf
data1 = tf.constant(12)
data2 = tf.constant(24)
dataadd = tf.add(data1,data2)
datamul = tf.multiply(data1,data2)
datasub= tf.subtract(data1,data2)
datadiv = tf.div(data1,data2)
with tf.Session() as sess:
    print(sess.run(dataadd))
    print(sess.run(datamul))
    print(sess.run(datasub))
    print(sess.run(datadiv))
```

### numpy模块

### matplotlib模块
#### 折线图
```python
import numpy as np
import matplotlib.pyplot as plt
x = np.array([1,2,3,4,5,6,7,8])
y = np.array([3,5,7,6,2,6,10,15])
plt.plot(x,y,'r')
```

![](https://ws2.sinaimg.cn/large/006tNbRwgy1fujmyco7wfj30z80mktbq.jpg)

#### 柱状图
```python
import numpy as np
import matplotlib.pyplot as plt
# x = np.array([1,2,3,4,5,6,7,8])
# y = np.array([3,5,7,6,2,6,10,15])
# plt.plot(x,y,'r')
x = np.array([1,2,3,4,5,6,7,8])
y = np.array([3,5,7,6,2,6,10,15])
plt.bar(x,y,0.5,alpha=1,color="b")
plt.show()
```
![](https://ws2.sinaimg.cn/large/006tNbRwgy1fujnihwyfrj30ty0lognv.jpg)


