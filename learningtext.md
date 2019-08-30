# 第三章 Ipython

## Ipython基础

import numpy as np

from numpy.random import randn

data = {i : randn() for i in range(7)}

data

## Tab键注释

an_apple = 27

an_example = 42

an<tab>  # tab不用输入，按键即可

## 内省

def add_numbers(a,b):
    """
    add two numbers together
    
    Returns
    --------
    the_sum: type of arguments
    """
    return a+b

add_numbers?

add_numbers??

np.*load*?

## %run命令

     假设存在car.py脚本文件，只需输入 In[ ]:%run car.py 即可运行脚本文件

## 中断正在执行代码
     在任何代码执行时，只要按“Ctrl-C”，即可停止程序

## 执行剪切板中的代码
     多数情况下可以通过‘Ctrl-shift-v’（Windows中不行，仅显示第一行,只能点击菜单中的复制功能），缩进代码中有空行会引发IndentationError
     应使用 %paste 和 %cpasta

## 高级IPython功能

class Message:
    def __init__(self,msg):
        self.msg = msg
    # 仅定义init，输出为<__main__.Message at 0x232479bb5f8>
    
    def __repr__(self):
        return 'Message: %s'% self.msg

x = Message("I have a secret") #利用__repr__方法得到更有意义的输出形式
x

# 第四章：Numpy基础：数组和矢量计算

## ndarray

import numpy as np
data =np.array([[1,2,3],[4,5,6]]) 
#创建数组

data+data

data.shape

data.dtype

## 索引与切片

arr = np.arange(10)

arr_slice = arr[5:8]

arr_slice[1] =100

arr





