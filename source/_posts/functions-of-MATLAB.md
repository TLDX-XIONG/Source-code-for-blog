---
title: functions of matlab 
date: 2019-11-26 21:18:57
tags: 
    - hist
    - linprog
categories: 
        - Matlab
comments: true
---
### <center> WHAT I LEARN TODAY</center>
#### 1. `hist` 函数用法

> hist 有直方图的意思，MATLAB 中绘制直方图的函数是 hist用法是 hist(y,x)，表示以向量 x 的各个元素为统计范围，绘制 y 的分布情况。下面是它的具体用法案例。

 1. N=hist(Y)
将向量 Y 的元素平均分配到十个等间隔的容器中，而且返回每个容器的元素个数。如果 Y 是一个矩阵，hist 指令逐列执行(此时省略 x 则默认为 10)
 2. N=hist(Y,X)
将向量 Y 的元素平均分配到 X 个等间隔的容器中，而且返回每个容器的元素个数。如果 Y 是一个矩阵，hist 指令逐列执行

#### 2. `linprog`函数用法
> linprog 是 MATLAB 中用于求解线性规划问题的指令函数。具体用法如下  

Matlab 中线性规划的标准型为：
<center>
min c^T^*x  

A*x<=b
Aeq*x=beq
lb<=x<=ub
</center>
 linprog 函数的基本形式为 lingprog(c,A,b)，返回值为向量 x 的值。它的标准形式如下：
<center>[x,fval]=linprog(c,a,b,aeq,beq,lb,ub,x0,options)</center>  

fval 返回目标函数的值，lb 和 ub 分别是变量 x 的取值上界和下界，x0 是 x 的初始值，options 此处是控制参数。   
