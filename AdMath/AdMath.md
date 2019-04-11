[TOC]

# 高等数学

## 第一讲：常用基础知识

### 基本初等函数
基本初等函数：幂函数、指数函数、对数函数、三角函数、反三角函数

1. 幂函数
形式：$y=x^\mu$
定义域：当x的指数$\mu$的分母为**偶数**的时候在x的负半轴没有定义,$\mu$**小于0**时在0处没有定义

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

$
\lim\limits_{n \to \infty }{x_n} = a \Leftrightarrow \forall\varepsilon>0, \; 
\exists N \in N_+，
当n>N时，恒有|x_n-a|<\varepsilon
$

##### 数列收敛的充要条件

- **定理1：** 若数列{$a_n$}收敛，则其任何子列{$a_{n_k}$}也收敛，且$\lim\limits_{k \to \infty }{a_{n_k}} = \lim\limits_{n \to \infty }{a_n}$

##### 收敛数列的性质

- **定理2：**（唯一性）数列$\{x_n\}$,若$\lim\limits_{n \to \infty }{x_n}=a$,则a是唯一的:

- **定理3：**（有界性）若数列$\{x_n\}$的极限存在，则$\{x_n\}$有界

- **定理4：**（保号性）数列$\{x_n\}$存在极限a,且a>0，则存在正整数N，当n>N时，$x_n>0$

##### 极限的运算规则
设 $\lim\limits_{n \to \infty }{x_n}=a,\, \lim\limits_{n \to \infty }{y_n}=b$,则，数列的和、积、商（分母不为0）为对应的极限的和、积、商。

##### 数列极限存在准则

- **准则1：**(夹逼定理)数列满足以下两个条件
    1. $y_n\leq x_n\leq z_n$
    2. $\lim\limits_{n \to \infty }{y_n}=a,\,\lim\limits_{n \to \infty }{z_n}=a,$

    则 $\lim\limits_{n \to \infty }{x_n}=a$

- **准则2：** 单调有界数列必定有极限
    >一个应用在书上P26,$$\lim\limits_{n \to \infty }{(1+\frac{1}{n})^n}=e$$


#### 函数极限的概念、性质与定理

##### 函数极限的定义
$\lim\limits_{x \to x_0 }{f(x)}=A \Leftrightarrow \forall \varepsilon>0, \exists \delta>0,当0<|x-x_0|<\delta,有|f(x)-A|<\varepsilon$

##### 函数极限存在的充要条件
1. 左右极限存在且相等
2. f(x)在点$x_0$出可以表示为A加上一个等价无穷小

##### 函数极限的性质
- 唯一性
极限存在则唯一
- 局部有界性
$\lim\limits_{x \to x_0 }{f(x)}=A 则存在M和\delta,当0<|x-x_0|<\delta,有|f(x)|\leq M$
- 局部保号性
如果极限A>0则存在一个去心邻域使得f(x)>0

##### 无穷小和无穷大
无穷小的比阶图
@import "./pic/无穷小的比阶.png"

>不是任意的无穷小都可以进行比阶eg $x^2,xsin\frac{1}{x}$
- 无穷小的运算规则
    1. 有限个无穷小的和是无穷小
    2. 有限函数与无穷小的乘积是无穷小
    3. **有限个**无穷小的乘积是无穷小
    4. 加法低阶吸收高阶，乘法累加，非零的常数不会影响阶数
- 常用的等价无穷小
@import "./pic/常用的等价无穷小.png"

##### 洛必达法则
- 洛必达法则的使用有3个条件
    1. 是$\frac{0}{0}$或者是$\frac{\infty}{\infty}$的形式
    2. 两个函数可导
    3. 导数的比值存在或者是无穷大
    >需要注意的是当导数的比值不存在时，洛必达法则失效，但是并不能说明原函数比值不存在、
    eg $x,\,x^2sin\frac{1}{x}$

##### 海涅定理（归结原则）
$设f(x)在x_0的去心领域里面有定义则：\lim\limits_{x \to x_0 }{f(x)}=A 存在 \Leftrightarrow 对任何以x_0为极限的数列 \{x_n\}, 极限 \lim\limits_{n \to \infty }{f(x_n)}=A 存在$
>应该会用在有三角函数的地方，通过控制数列的通项公式让sin里面的值只取1或只取0

#### 函数的连续与间断

##### 连续的定义

1. $\lim\limits_{\Delta x \to 0 }{\Delta y} = \lim\limits_{\Delta x \to 0 }{[f(x_0+\Delta x)-f(x_0)]}=0$ 此定义常用于证明题
2. 函数在$x_0$处的值等于在此处的极限值

##### 间断点的定义
- 第一类间断点
    1. 可去间断点 $\lim\limits_{x \to x_0 }{f(x)}=A \ne f(x_0)$ f(x)甚至可以在$x_0$处没有定义
    2. 跳跃间断点 左右极限都存在但是不相等
- 第二类间断点
    1. 无穷间断点 左右极限都为无穷
    2. 震荡间断点 极限震荡不存在


### 题目讲解
- 还有问题的题目
p36 2.9(3,4,5)
- 错题
p35 2.7

>等价无穷小在要求极限的式子是乘式的时候可以用
要证明无界的话只要给出一个反例。
- 极限的定义与三个性质
    - 两个区间有界的结论（由有界性推出）
        1. f(x)在[a,b]上连续，则f(x)在该区间上有界
        2. f(x)在(a,b)上连续，且 $\lim\limits_{x \to a^+ }{f(x)},\lim\limits_{x \to b^- }{f(x)}$存在，则f(x)在这个开区间上有界
        >需要注意的是，该命题的逆命题不成立，即有界不能推出极限存在，f(x)可以在a点有界的震荡。所以要证明无界的话只要给出一个反例。

- 和式$\sum\limits_{i=1}^{n}{u_i} = u_1+u_2+\cdots +u_n$缩放的两个典型方法
    1. 当n为无穷大时 $n\cdot u_{min} \leqslant \sum\limits_{i=1}^{n}{u_i} \leqslant n\cdot u_{max}$
    2. 当n是有限数，且$u_i \geqslant 0$时,$1\cdot u_{max} \leqslant \sum\limits_{i=1}^{n}{u_i} \leqslant n\cdot u_{max}$

    之所以从这两个角度来划分，是因为在和式中谁有决定性的作用。当n为无穷大时，每一项$u_i$都是趋向无穷小的，所以都有平等的权利。而在有限项中喝式中的最大值起决定性的作用。



## 第三讲：一元函数微分学的概念与计算

### 知识点讲解

#### 导数与微分的概念

- 导数的两种表示形式
    1. $$f'(x_0)=\lim\limits_{\Delta x \to 0 }{\frac{\Delta y}{\Delta x}} = \lim\limits_{\Delta x \to 0 }{\frac{f(x_0+\Delta x) -f(x_0)}{\Delta x}}$$
    2. $$f'(x_0)=\lim\limits_{x \to x_0 }{\frac{f(x)-f(x_0)}{x-x_0}}$$

- 函数可导的要求：左导数和右导数存在且相等

- 可微的概念：$\Delta y$就是微分，可导和可微是充要条件，所以证明可微就是证明可导。但是这种情况是针对于一元函数的。

#### 导数与微分的计算

- 四则运算
    $$[u(x)+v(x)]'=u'(x)+v'(x)$$$$[u(x)\,v(x)]'=u'(x)\,v(x)+u(x)\,v'(x)$$$$\bigg[\frac{u(x)}{v(x)} \bigg]'=\frac{u'(x)\,v(x)-u(x)\,v'(x)}{[v(x)]^2}$$

- 复合函数
    $${f[g(x)]}'=f'[g(x)]g'(x)$$

- 反函数的导数
    $$\varphi'(y)=\frac{1}{f'(x)}$$

- 参数方程
    $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}$$

- 隐函数
两边对x求导，最后解出$y'$

- 对数求导法
对于有多项相乘、相除、开方、乘方的式子，一般两边同取对数，再两边对x求导

- 幂指函数
$u(x)^{v(x)}$通常将其转化为复合函数$e^{v(x)ln\,u(x)}$

- 高阶求导
    1. 直接逐次求导找通项公式$sin(kx)^{(n)}=k^nsin(kx+n\cdot \frac{\pi}{2}), cos(kx)^{(n)}=k^ncos(kx+n\cdot \frac{\pi}{2})$
    2. 对于两个函数乘积的高阶导数，可以用莱布尼茨公式
        $$(uv)^{(n)}=\sum\limits_{k=0}^{n}{C^k_nu^{n-k}v^{(k)}}$$
    3. 写出泰勒公式或者麦克劳林公式，通过比较系数得到$f^{(n)}(x_0)$,任何无穷阶可导的函数都可以写成
        $$f(x)=\sum\limits_{n=0}^{\infty}{\frac{f^{(n)}(x_0)}{n!}}\cdot(x-x_0)^n$$或者
        $$f(x)=\sum\limits_{n=0}^{\infty}{\frac{f^{(n)}(0)}{n!}}\cdot x^n$$

- 变限积分求导公式
    $$F'(x)=\frac{d}{dx}\bigg[ \int_{\varphi _1}^{\varphi _2} f(t)dt\bigg] = f[\varphi _2(x)]\varphi _2'(x) - f[\varphi _1(x)]\varphi _1'(x)$$

- 基本初等函数的导数公式
    原函数 | 导函数
    ----|----
    $x^a$ | $ax^{a-1}$
    $a^x$ | $a^xlna$
    $log_ax$ | $\frac{1}{xlna}$
    $sinx$ | $cosx$
    $cosx$ | $-sinx$
    $arcsinx$ | $\frac{1}{\sqrt{1-x^2}}$
    $arccos$ | $-\frac{1}{\sqrt{1-x^2}}$
    $tanx$ | $sec^2x$
    $cotx$ | $-csc^2x$
    $arctanx$ | $\frac{1}{1+x^2}$
    $arccotx$ | $-\frac{1}{1+x^2}$
    $secx$ | $secx\,tanx$
    $cscx$ | $-cscx\,cotx$
    $ln(x+\sqrt{x^2+1})$ | $\frac{1}{\sqrt{x^2+1}}$
    $ln(x+\sqrt{x^2-1})$ | $\frac{1}{\sqrt{x^2-1}}$




## 第四讲：一元函数微分学的几何应用

### 知识点讲解

#### 极值与最值

- 极值的定义
    在$x_0$的某个领域内，使得在该领域内任意一点x均有$f(x)\leq f(x_0)$则称$x_0$是极大值点，$f(x_0)$称为极大值。
- 最值的定义
    $x_0$为定义域内的一点，定义域内任意一点x均有$f(x)\leq f(x_0)$则称$f(x_0)$为最大值。

>间断点可以是极值点

>凹凸性对应单调性，极值点对应拐点
#### 单调性与极值的判别

- 一阶可导点是极值点的必要条件：$f(x)$在 $x_0$处可导且取得极值，则必有 $f'(x_0)=0$

- 判别极值的几个充分条件
    1. （第一充分条件）$f(x)$在 $x_0$处**连续**，在某去心领域内可导。若左半领域 $f'(x)<0$右半领域 $f'(x)>0$,则在 $x_0$处取得极小值，反之取得最大值。
    2. （第二充分条件）$f(x)$在 $x_0$处**二阶可导**，$f'(x_0)=0,f''(x_0)\ne 0$。若$f''(x_0)<0$取得极大值，$f''(x_0)>0$取得极小值。
    3. （第三充分条件）$f(x)$在 $x_0$处**n阶可导**，$f^{m}(x_0)=0(m=1,2, \cdots ,n-1),f^{n}(x_0)\ne 0$。**当n为偶数时**若$f^{n}(x_0)<0$取得极大值，$f^{n}(x_0)>0$取得极小值。

#### 凹凸性与拐点的概念和判别

- 凹凸性的定义
    函数在区间I上任意两点 $x_1,x_2$满足 $f( \frac{x_1+x_2}{2}) < \frac{f(x_1+f(x_2))}{2}$,则称 $f(x)$在区间I上是凹的，反之是凸的。
- 拐点的定义：曲线的凹弧与凸弧的分界点成为拐点。

- 二阶可导点是拐点的必要条件：$f''(x_0)$存在且 $(x_0,f(x_0))$为曲线上的拐点，则 $f''(x_0)=0$

- 拐点判别的几个充分条件
    1. （第一充分条件）$f(x)$在 $x_0$处**连续**，在某去心领域内二阶可导。 $f''(x)$变号则是拐点。
    2. （第二充分条件）$f(x)$在 $x_0$处**某领域内三阶可导**，$f''(x_0)=0,f'''(x_0)\ne 0$则该点是拐点。
    3. （第三充分条件）$f(x)$在 $x_0$处**n阶可导**，$f^{m}(x_0)=0(m=2,3, \cdots ,n-1),f^{n}(x_0)\ne 0 (n\geq 3)$。**当n为奇数时**是拐点。

#### 渐近线
- 水平渐近线
- 铅直渐近线
- 斜渐近线
    若 $\lim\limits_{x \to +\infty }{\frac{f(x)}{x}}=k_1 , \lim\limits_{x \to +\infty }{[f(x)-k_1x]}=b_1$则$y=k_1x+b_1$是曲线 $y=f(x)$的一条斜渐近线（x趋向于负无穷同理）

#### 最值或取值范围问题
- 求闭区间[a,b]上连续函数的最大值和最小值
    1. 求出驻点和不可导点的函数值
    2. 求出端点的函数值
    3. 比较这些值中的最大最小值
- 求开区间(a,b)上连续函数的最大值和最小值
    这类题的做法和闭区间的差不多，只是在求端点值的改为在端点处求极限值

#### 作函数的图形
1. 确定定义域，观察奇偶性、对称性
2. 求出一二阶导，并利用无定义点、一二阶导不存在或等于0的点将定义域划分为多个子区间，确定每一段上的单调性与凹凸性。
3. 看是否有渐近线
4. 作出函数图形


## 第五讲：中值定理

### 知识点讲解

#### 涉及函数f(x)的中值定理
设f(x)在[a,b]上连续
- 定理1（有界与最值定理）
    $m\leq f(x) \leq M$其中m,M是区间上的最小值和最大值
- 定理2（介值定理）
    当$m\leq \mu \leq M$时，存在$\xi \in [a,b]$ 使得 $f(\xi)=\mu$
- 定理3（平均值定理）
    当 $a<x_1<x_2<\cdots <x_n<b$时，在$[x_1,x_n]$内至少存在一点 $\xi$,使
    $$f(\xi)=\frac{f(x_1)+f(x_2)+\cdots +f(x_n)}{n}$$
- 定理4（零点定理）
    当f(a)f(b)<0时，存在$\xi \in (a,b)$使得 $f(\xi)=0$

#### 涉及导数f'(x)的中值定理
- 定理5（费马定理）
    $设f(x)在x_0处可导且取得极值，则f'(x)=0$
    >证明：
    不妨设在$f(x)$处取得极大值，则在领域内，都有$\Delta f=f(x)-f(x_0)\leq 0$,于是根据导数的定义和极限的保号性有
    $$f'_-(x_0)= \lim\limits_{x \to x_0^-}{ \frac{f(x)-f(x_0)}{x-x_0}}\geq 0$$
    $$f'_+(x_0)= \lim\limits_{x \to x_0^+}{ \frac{f(x)-f(x_0)}{x-x_0}}\leq 0$$
    又f(x)在$x_0$处可导，于是$f'_-(x_0)=f'_+(x_0)$故$f'(x_0)=0$
- 定理6（罗尔定理）
    $f(x)满足[a,b]上连续，(a,b)上可导，f(a)=f(b),则存在\xi \in (a,b)使得f'(\xi)=0$
    >此定理可以推广，a,b可以替换为$\infty ,-\infty$,在a,b上连续可以写成极限相同或都为无穷
- 定理7（拉格朗日中值定理）
    $f(x)满足[a,b]上连续(a,b)上可导，则存在\xi \in (a,b)使得 f(b)-f(a)=f'(\xi)(b-a)$
    $$f'(\xi)=\frac{f(b)-f(a)}{b-a}$$
- 定理8（柯西中值定理）
    $f(x),g(x)满足[a,b]上连续，(a,b)上可导，g'(x)\ne 0，则存在\xi \in (a,b)使得$
    $$\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(\xi)}{g'(\xi)}$$
- 定理9（泰勒公式）
    1. 带拉格朗日余项的n阶泰勒公式
        设f(x)在点$x_0$的某个邻域内n+1阶导数存在，则对该邻域的任意点x，有
        $$f(x)=f(x_0)+f'(x_0)(x-x_0)+\cdots +\frac{1}{n!}f^{(n)}(x_0)(x-x_0)^n+\frac{1}{(n+1)!}f^{(n+1)}(\xi)(x-x_0)^{n+1}$$
        其中$\xi$介于$x,x_0$
    2. 带佩亚诺余项的n阶泰勒公式
        设f(x)在$x_0$出n阶可导，则存在$x_)$的一个邻域，对于该邻域的任意一点有
        $$f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{1}{2!}f''(x_0)(x-x_0)^2+ \cdots +\frac{1}{n!}f^{(n)}(x_0)(x-x_0)^{n}+\omicron((x-x_0)^{n})$$
    >当$x_0=0$时，泰勒公式称为麦克劳林公式
    @import "./pic/几个重要函数的麦克劳林公式.png"


## 第六讲：零点问题、微分不等式

### 知识点讲解

#### 零点问题

1. 零点定理（主要用于证明根的存在性）
    $设f(x)在[a,b]上连续，且f(a)f(b)<0,则f(x)=0在(a,b)内至少有一个根$
    >此定理可以推广，a,b可以替换为$\infty ,-\infty$,在a,b上连续可以写成极限相同或都为无穷
2. 单调性（主要用于证明根的唯一性）
    $f(x)在(a,b)内单调，则f(x)=0在(a,b)内至多有一个根，这里a,b可以是有限数，也可以是无穷数$
3. 罗尔原话（罗尔定理的推论）
    $f^{(n)}至多有k个根，则f(x)=0至多有k+n个根$
4. 实系数奇次方程知道有一个实根
    $x^{2n+1}+a_1x^{2n}+\cdots +a_{2n}x+a_{2n+1}=0$可以用单调性证明

#### 微分不等式

- 经典不等式的总结
    1. 设a,b为实数，则$2|ab|\leq a^2+b^2,\; |a\pm b|\leq |a|+|b|,\; \big||a|-|b|\big|\leq |a-b|$
    2. 设$a_1,a_2,\cdots ,a_n>0$则
        $$\frac{a_1+a_2+\cdots +a_n}{n}\geq \sqrt[n]{a_1a_2\cdots a_n}$$
        $$\Big|\frac{a_1+a_2+\cdots +a_n}{n}\Big| \leq \sqrt{\frac{a_1^2+a_2^2+\cdots +a_n^2}{n}}$$
        当且仅当$a_1=a_2=\cdots =a_n$时，等号成立
    3. 设$x>0,y>0,p>0,q>0,\frac{1}{p}+\frac{1}{q}=1$则$xy\leq \frac{x^p}{p}+\frac{y^q}{q}$
    4. $(a^2+b^2)(c^2+d^2)\geq (ac+bd)^2$
    5. 若f(x),g(x)在[a,b]上可积且平方可积，则
        $$\Big[ \int^b_af(x)g(x)dx \Big]^2 \leq \int _a^bf^2(x)dx \cdot \int _a^bg^2(x)dx$$
    6. 设f(x)在[a,b]上p次方可积，g(x)在[a,b]上q次方可积，
        $$\Big| \int^b_af(x)g(x)dx \Big|\leq \Big[ {\int_a^b|f(x)|^pdx} \Big]^{\frac{1}{p}} \cdot \Big[ {\int_a^b|g(x)|^qdx} \Big]^{\frac{1}{q}}$$
        其中$p>1,\frac{1}{p}+\frac{1}{q}=1$
    7. 其他重要不等式
    

### 题目讲解
书前面知识点的证明要去看


## 第二讲：极限与连续

### 知识点讲解













