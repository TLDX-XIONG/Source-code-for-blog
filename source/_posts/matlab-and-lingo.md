---
title: matlab and lingo
date: 2019-11-28 21:45:10
tags:
    - diff
    - int
    - quad
    - dsolve
    - fsolve
    - roots
    - fzero
    - 最小二乘法
    - 血液流动规律
categories: Matlab
---
### <center>MATLAB AND LINGO</center>
- #### diff 函数
  diff(f): 对 f 求导
  diff(f,t): df/dt 或者 &part;f/&part;t
  diff(f,n): 对 f 求 n 阶导数
  diff(f,n,t): 高阶导数 d<sup>n</sup>f/dt<sup>n</sup>（或者 &part;<sup>n</sup>f/&part;t<sup>n</sup>）
<!-- more -->
- #### int 函数
  int(f,t): &int;&fnof;(t)dt
  int(f,t,a,b): 求 a 到 b 的定积分
- #### quad 函数
  quad(f,a,b): 求定积分的近似值
- #### dsolve 函数
  dsolve('eqn','con','v'): 关于变量 v 在初值条件 con 下求解微分方程
- #### fsolve 函数
  fsolve(funs,x0): 对方程组 funs，以向量 x0 为初值求近似解
- #### solve 函数
  solve(s): 对方程中变量 x 求解
  solve(s,v): 对方程中指定变量 v 求解
  solve(s1,s2,s3,···,sn): 对 n 个方程默认变量求解
  solve(s1,s2,s3,···,sn,v1,v2,···,vn): 对 n 个方程的指定变量求解
- #### roots 函数
  roots(p): 求以 p 为系数的一元多项式方程的解
- #### fzero 函数
  fzero(fun,x0): 对一元方程 fun，以 x0 为初值求近似解
- #### matlab 二维数组
  MATLAB 对于二维数组的完整引用方式为：a(i,j)
  其它方式：
  a(:,j): 表示选择第 j 列
  a(i,:): 表示选择第 i 行
  a(a:b,j): 表示选择第 j 列的第 a 到 b 行
  a(i,a:b): 表示选择第 i 行的第 a 到 b 列
- #### 线性最小二乘法
  最小二乘法是一种数学优化技术。通过最小化误差的平方和寻找数据的最佳函数匹配。也可用于`函数拟合`
  **实例**
  实验得到四个数据 (x,y): (1,6)、(2,5)、(3,7)、(4,10)。希望找到一条和这四个点最匹配的直线：y=a+bx。因此有：
  **<center>a+1b=6**
  **a+2b=5**
  **a+3b=7**
  **a+4b=10</center>**
  最小二乘法采用的手段是尽量使得等号两边的方差最小：  
  **<center>S(a,b)=[6-(a+b)]<sup>2</sup> + [5-(a+2b)]<sup>2</sup> + [7-(a+3b)]<sup>2</sup> + [10-(a+4b)]<sup>2</sup></center>**  
  求解 min(a,b), 通过对 a,b 求偏导。再令两者偏导为零，得到 a 与 b 的值。此时的曲线便是最佳拟合曲线。
---
- #### 血液流动规律
  根据 poiseuille 定律，血液流过半径 r、长为 l 的一段血管 AC 时，流量：
  **<center>q=&pi;r<sup>4</sup>&Delta;p/8&mu;l</center>**
  &Delta;P 是 A，C 两点的压力差，&mu; 是血液的黏性系数。在血液流动过程中，机体克服阻力所消耗的能量为 E<sub>1</sub>=q·&Delta;p,将上式中 &Delta;p带入上式得：
  **<center>E<sub>1</sub>=8&mu;q<sup>2</sup>l/&pi;r<sup>4</sup></center>**