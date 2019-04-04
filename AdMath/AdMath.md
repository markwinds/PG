[TOC]

# 高等数学

## 第一讲：常用基础知识

### 基本初等函数
基本初等函数：幂函数、指数函数、对数函数、三角函数、反三角函数

1. 幂函数
形式：$y=x^\mu$
定义域：当x的指数$\mu$的分母为**偶数**的时候在x的负半轴没有定义,$\mu$**小于0**时在0出没有定义

```gnuplot {cmd=true output="html" hide}
set term svg
set title "常见的幂函数" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-10:10]  
set yrange [-20:20] 
set xtics 2
set mxtics 2
set ytics 5
set mytics 2
set grid
plot x**2 t "x^2", x**0.5 t "x^{0.5}", x**-1 t "x^{-1}"
```

2. 指数函数
形式：$y=a^x(a>0,a\ne0)$
定义域：$(-\infty,+\infty)$
值域：$(0,+\infty)$
单调性：$a>1$ 单调递增 $a<1$ 单调递减

```gnuplot {cmd=true output="html" hide}
set term svg
set title "常见的指数函数" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-8:8]  
set yrange [0:20] 
set xtics 2
set mxtics 2
set ytics 5
set mytics 2
set grid
plot 2**x t "2^x", 0.5**x t "0.5^x"
```

3. 对数函数