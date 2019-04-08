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
单调性：$a>1$ 单调递增 $0<a<1$ 单调递减

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
形式：$y=log_ax(a>0,a\ne1)$
定义域：$(0,+\infty)$
值域：$(-\infty,+\infty)$
单调性：$a>1$ 单调递增 $0<a<1$ 单调递减
>换底公式
$$log_ab=\frac{log_cb}{log_ca}$$

```gnuplot {cmd=true output="html" hide}
set term svg
set title "常用的对数函数" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [0:5]
set yrange [-5:5]
set xtics 1
set mxtics 2
set ytics 2
set mytics 2
set grid
logb(x, base) = log(x)/log(base)
plot  logb(x,2) t "log_2x", logb(x,0.5) t "log_{0.5}x"
```

4. 三角函数
- 正弦函数和余弦函数
- 正切函数($y=tanx$)和余切函数($y=cotx$)
定义域：$y=tanx,x\ne k\pi+\frac\pi2(k\in Z) \quad y=cotx,x\ne k\pi(k\in Z) $  
奇偶性：**两个函数都是奇函数**
周期性：周期都为$\pi$
```gnuplot {cmd=true output="html" hide}
set term svg
set title "正切和余切函数图像" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-2*pi:2*pi]
set yrange [-20:20]
set xtics pi/2
set mxtics 1
set ytics 5
set mytics 2
set grid
plot tan(x) t "y=tanx", 1/tan(x) t "y=cotx"
```

- 正割函数$y=secx$余割函数$y=cscx$
定义域：$y=secx,x\ne k\pi+\frac\pi2(k\in Z) \quad y=cscx,x\ne k\pi(k\in Z) $ 
奇偶性：正割函数是偶函数 余割函数是奇函数
周期性：周期均为2$\pi$
```gnuplot {cmd=true output="html" hide}
set term svg
set title "正割函数和余割函数的图像" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-10:10]
set yrange [-20:20]
set xtics pi
set mxtics 2
set ytics 2
set mytics 2
set grid
plot 1/cos(x) t "y=secx", 1/sin(x) t "y=cscx"
```

- 反正弦$y=arcsinx$反余弦$y=arccosx$
定义域：$[-1,1]$
性质：$arcsinx+arccosx=\frac{\pi}{2}$
```gnuplot {cmd=true output="html" hide}
set term svg
set title "反正弦和反余弦函数的图像" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-1:1]
set yrange [-pi:pi]
set xtics 1
set mxtics 2
set ytics pi
set mytics 2
set grid
plot asin(x) t "y=arcsinx", acos(x) t "y=arccosx"
```
- 反正切$y=arctanx$和反余切$y=arccotx$
性质：$arctanx+arccotx=\frac{\pi}{2}$
```gnuplot {cmd=true output="html" hide}
set term svg
set title "反正切和反余切函数的图像" font ",15"
set key right box
set samples 500
set style data points
set xlabel "x"
set ylabel "y"
set xrange [-10:10]
set yrange [-pi:pi]
set xtics 2
set mxtics 2
set ytics pi/2
set mytics 2
set grid
plot atan(x) t "y=arctanx", atan(1/x) t "y=arccotx"
```

### 其他的注意事项
- 7点关于求导积分后函数性质总结
    1. 偶函数求导以后是奇函数
    2. 奇函数求导以后是偶函数
    3. 周期为T的函数求导以后周期不变
    4. 连续的奇函数的一切原函数都是偶函数
    5. 连续的偶函数只有一个原函数是奇函数
    6. 连续的以T为周期的函数所有原函数都是以T为周期的函数
    7. 若函数在有限区间(a,b)内可导且$f'(x)$有界，则f(x)在(a,b)内有界
- 幂指函数$u(x)^{v(x)}$通常将其转化为复合函数$e^{v(x)ln\,u(x)}$

### 常用的基础知识


## 第二讲：极限与连续

### 知识点讲解

#### 数列极限的概念、性质与定理

##### 数列极限的定义
$\lim\limits_{n \to \infty }{x_n} = a \Leftrightarrow \forall \varepsilon$


### 题目讲解














