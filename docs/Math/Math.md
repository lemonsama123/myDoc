##  希腊字母

| 效果（大写/小写）  | Tex                | MathJax                                 | 变体          | 变体语法      |
| ------------------ | ------------------ | --------------------------------------- | ------------- | ------------- |
| $\text{A}\alpha$   | `\alpha\alpha`     | `\text{A}\alpha` 或  `{\rm A} \alpha`   |               |               |
| $\text{B}\beta$    | `\Beta\beta`       | `\text{B}\beta` 或 `{\rm B}\beta`       |               |               |
| $\Gamma\gamma$     | `\Gamma\gamma`     | `\Gamma\gamma`                          |               |               |
| $\Delta\delta$     | `\Delta\delta`     | `\Delta\delta`                          |               |               |
| $\text{E}\epsilon$ | `\Epsilon\epsilon` | `\text{E}\epsilon` 或 `{\rm E}\epsilon` | $\varepsilon$ | `\varepsilon` |
| $\text{Z}\zeta$    | `\Zeta\zeta`       | `\text{Z}\zeta` 或 `{\rm E}\epsilon`    |               |               |
| $\text{E}\eta$     | `\Eta\eta`         | `\text{E}\eta` 或 `{\rm E}\eta`         |               |               |
| $\Theta\theta$     | `\Theta\theta`     | `\Theta\theta`                          | $\vartheta$   | `\vartheta`   |
| $\text{I}\iota$    | `\Iota\iota`       | `\text{I}\iota` 或 `{\rm I}\iota`       |               |               |
| $\text{K}\kappa$   | `\Kappa\kappa`     | `\text{K}\kappa` 或 `{\rm K}\kappa`     |               |               |
| $\Lambda\lambda$   | `\Lambda\lambda`   | `\Lambda\lambda`                        |               |               |
| $\text{M}\mu$      | `\Mu\mu`           | `\text{M}\mu` 或 `{\rm M}\mu`           |               |               |
| $\text{N}\nu$      | `\Nu\nu`           | `\text{N}\nu` 或 `{\rm N}\nu`           |               |               |
| $\Xi\xi$           | `\Xi\xi`           | `\Xi\xi`                                |               |               |
| $\text{O}\omicron$ | `\Omicron\omicron` | `\text{O}\omicro` 或 `{\rm O}\omicro`   |               |               |
| $\Pi\pi$           | `\Pi\pi`           | `\Pi\pi`                                | $\varpi$      | `\varpi`      |
| $\text{P}\rho$     | `\Rho\rho`         | `\text{P}\rho` 或 `{\rm P}\rho`         | $\varrho$     | `\varrho`     |
| $\Sigma\sigma$     | `\Sigma\sigma`     | `\Sigma\sigma`                          | $\varsigma$   | `\varsigma`   |
| $\text{T}\tau$     | `\Tau\tau`         | `\text{T}\tau` 或 `{\rm T}\tau`         |               |               |
| $\Upsilon\upsilon$ | `\Upsilon\upsilon` | `\Upsilon\upsilon`                      |               |               |
| $\Phi\phi$         | `\Phi\phi`         | `\Phi\phi`                              | $\varphi$     | `\varphi`     |
| $\text{X}\chi$     | `\Chi\chi`         | `\text{X}\chi` 或 `{\rm X}\chi`         |               |               |
| $\Psi\psi$         | `\Psi\psi`         | `\Psi\psi`                              |               |               |
| $\Omega\omega$     | `\Omega\omega`     | `\Omega\omega`                          |               |               |

> 注：字母 $\text{ABEIKMNOPTX}$ 在 `MathJax` 中只能通 `\text{字母}` 或 `{\rm 字母}` 的形式来表示，但在 `Tex` 中依然可以用类似于 `\Alpha` 的形式来表示。希腊字母的变体在数学和物理中也经常被使用。

![希腊字母](https://pic1.zhimg.com/v2-da3e717cf670582fbfbdddee33073524_b.jpg)

## 上下标

```tex
$$a^2,a_1$$
```

$$
a^2,a_1
$$

```tex
$$x^{y + z},p_{ij}$$
```

$$
x^{y + z},p_{ij}
$$

> 如果上下标是由一个表达式或多个字母，则应当将它们放在 `{}` 中，类似于 `a^{b+c}`.

## 分式与根式

```tex
$$\frac{1}{2},\frac 1 2$$
```

$$
\frac{1}{2},\frac 1 2
$$


```tex
$$\frac 1 {x+y}$$
```


$$
\frac 1 {x+y}
$$

```tex
$$\frac {\frac 1 x + 1}{y + 1}, \frac {\dfrac 1 x + 1}{y + 1},\frac {\cfrac 1 x + 1}{y + 1}$$
```
$$
\frac {\frac 1 x + 1}{y + 1}, \frac {\dfrac 1 x + 1}{y + 1},\frac {\cfrac 1 x + 1}{y + 1}
$$

> 同样的，分子或分母是由一个表达式或多个字母时，应当将它们放在 `{}` 中，`frac、dfrav、cfrac` 的区别是，`dfrac` 的上下间距较大，`cfrac` 离地更高。当然，不同的编辑器的渲染效果会有所不同，视具体情况选择。


```tex
\sqrt 2,\sqrt{x+y},\sqrt[3]x
```



$$
\sqrt 2,\sqrt{x+y},\sqrt[3]x
$$

## 一些运算符

```tex
$$+-=$$
```

$$
+-=
$$

```tex
$$\times,\cdot,\div$$
```

$$
\times,\cdot,\div
$$

```tex
$$\pm,\mp$$
```

$$
\pm,\mp
$$

```tex
$$\gt,\lt,\ge,\le,\gg,\ll,\ne,\not=,\approx,\equiv$$
```

$$
\gt,\lt,\ge,\le,\gg,\ll,\ne,\not=,\approx,\equiv
$$

```tex'
$$\cap,\cup,\in,\notin,\subseteq,\subseteqq,\subsetneq,\subsetneqq,\varnothing$$
```

$$
\cap,\cup,\in,\notin,\subseteq,\subseteqq,\subsetneq,\subsetneqq,\varnothing
$$

```tex
$$\forall,\exists,\nexists$$
```

$$
\forall,\exists,\nexists
$$

```tex
$$\because,\therefore$$
```

$$
\because,\therefore
$$



## 大型运算符

```tex
$$\sum,\prod$$
```

$$
\sum,\prod
$$

```tex
$$\sum_{i=1}^n a_i,\prod_i^n b_i$$
```

$$
\sum_{i=1}^n a_i,\prod_{i=1}^n b_i
$$

```tex
$$\frac{\sum_{i=1}^n a_i}{\prod_{i=1}^n b_i}$$
```

$$
\frac{\sum_{i=1}^n a_i}{\prod_{i=1}^n b_i}
$$

```tex
$$\frac{\sum\limits_{i=1}^n a_i}{\prod\limits_{i=1}^n b_i}$$
```


$$
\frac{\sum\limits_{i=1}^n a_i}{\prod\limits_{i=1}^n b_i}
$$
> 用 `_` 和 `^` 来分别表示运算的上下限，`\limits` 是强制让上下限严格在运算符的上面和下面

## 积分符号

```tex
$$\int,\iint,\iiint,\oint \oiint \oiiint$$
```


$$
\int,\iint,\iiint,\oint \oiint \oiiint
$$

```tex
$$\int_{a}^{b} f(x) \mathrm{d} x,\iint \limits_D f(x,y) \mathrm{d} xy, \iiint \limits _{\Omega} f(x,y,z) \mathrm{d}xyz$$
```

$$
\int_{a}^{b} f(x) \mathrm{d} x,\iint \limits_D f(x,y) \mathrm{d} xy, \iiint \limits _{\Omega} f(x,y,z) \mathrm{d}xyz
$$


>也是使用  `_` 和 `^` 来分别表示运算的上下限，`\limits` 强制让上下限严格在运算符的上面和下面。在 `MathJax` 中好像不支持 `\oiint` 和 `\oiiint`，但在 `Tex` 中是支持的。在 `Tex` 中，只有一个符号表示变量时我们才使用斜体，其他的我们都要修正为正体，对于 $\sin、\cos、\log、\ln$ 这些，直接通过 `\sin` 这种形式来表示，对于没有内置的符号，则可以通过 `\mathrm{符号}` 或来修饰。微分符号 ${\rm d}$ 也应该为正体。

## 一些符号

```tex
$$\mathbb R,\mathbb Q,\mathbb N,\mathbb Z_+$$
```
$$
\mathbb R,\mathbb Q,\mathbb N,\mathbb Z_+
$$
>在 `Tex` 可直接用 `\R` 来达到上面的效果，而在 `MathJax` 中貌似只能通过 `\mathbb R` 来达到上面的效果。当需要表示集合时，请使用上面的符号
```tex
\cdots,\vdots,\ddots
```

$$
\cdots,\vdots,\ddots
$$

```tex
\infty,\partial,∂,\nabla,\propto，^{\circ}
```

$$
\infty,\partial,∂,\nabla,\propto, ^{\circ}
$$

>`Tex` 中支持 `\degree` 来表示度，在 `MathJax` 中好像不支持，这里使用的是 `^{\circ}` 来代替

```tex
\sin x ,\sec x, \cosh x,\log_2 x, \ln x, \lg x,\max x
```

$$
\sin x ,\sec x, \cosh x,\log_2 x, \ln x, \lg x,\max x
$$

## 标志符号

```tex
\vec x,\overrightarrow {AB},\bar x,\overline{AB}
```


$$
\vec x,\overrightarrow {AB}
,\bar x,\overline{AB}
$$

## 箭头

```tex
\leftarrow,\rightarrow,\leftrightarrow,\Leftarrow,\Rightarrow,\Leftrightarrow,\longleftarrow,\longrightarrow,\longleftrightarrow,\Longleftarrow,\Longrightarrow,\Longleftrightarrow
```


$$
\leftarrow,\rightarrow,\leftrightarrow,\Leftarrow,\Rightarrow,\Leftrightarrow,\longleftarrow,\longrightarrow,\longleftrightarrow,\Longleftarrow,\Longrightarrow,\Longleftrightarrow
$$

## 括号与定界符

```tex
()[]\{ \} \lbrace
```

$$
()[]\{ \}\lbrace\rbrace
$$

```tex
\lceil,\rceil,\lfloor,\rfloor,||
```

$$
\lceil,\rceil,\lfloor,\rfloor,||
$$

```tex
\left(0,\frac 1 a\right]
```

$$
\left(0,\frac 1 a\right]
$$
> 使用 `\left` 和 `\right` 来修饰括号会使其具有自适应大小的特性
```tex
\left.\frac {∂f}{∂x}\right|_{x=0}
```


$$
\left.\frac {∂f}{∂x}\right|_{x=0}
$$
> 通过 `\left.` 和 `\right|` 使 `|` 具有自适应大小的特性

## 多行公式

```tex
\begin{aligned}
a & =b+c+d \\
 & =e+f
\end{aligned}
```

$$
\begin{aligned}
a & =b+c+d \\
 & =e+f
\end{aligned}
$$
```tex
$$
\begin{align}
a&=b+c+d \\
&=e+f
\end{align}
$$
```
$$
\begin{align}
a&=b+c+d \\
&=e+f
\end{align}
$$

> 上面的两种方式是一样的。注意：在 `MathJax` 中，换行请用 `\\`，在 `Tex` 中是支持 `\\` 换行的.



## 大括号

```tex
f(x)=
\begin{cases}
\sin x, & -π\le x \le π\\
0,& \text{其他}
\end{cases}
```

$$
f(x)=
\begin{cases}
\sin x, & -π\le x \le π\\
0,& \text{其他}
\end{cases}
$$



```tex
$$
f(x)= \left\lbrace\begin{array}{ll}
\sin x, & -\pi\le x \le \pi\\
0,& \text{其他}
\end{array}\right.
$$
```

$$
f(x)= \left\lbrace\begin{array}{ll}
\sin x, & -\pi\le x \le \pi\\
0,& \text{其他}
\end{array}\right.
$$

> 在 `MathJax` 中，大括号 请使用 `\lbrace` 表示。

```tex
\begin{matrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{matrix}
```

$$
\begin{matrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{matrix}
$$

```tex
\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}
```
$$
\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}
$$

```tex
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{bmatrix}
```


$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{bmatrix}
$$

```tex
$$
\left[\begin{array}{llll}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right]
$$
```
$$
\left[\begin{array}{llll}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right]
$$


```tex
\begin{pmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{pmatrix}
```



$$
\begin{pmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{pmatrix}
$$
```tex
\left(\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right)
```
$$
\left(\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right)
$$
```tex
\begin{vmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{vmatrix}
```


$$
\begin{vmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{vmatrix}
$$

```tex
\left|\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right|
```

$$
\left|\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \cdots & a_{2n} \\
a_{31} & a_{32} & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots  \\
a_{n1} & a_{n2} & a_{n3} & \cdots & a_{(n-1)n}
\end{array}\right|
$$

> 另外，用 `\bf A` 来表示矩阵，`\bf B^{\rm T}` 表示矩阵的转置

$$
\bf A,\bf B^{\rm T}
$$

## 几个例子



### 正态分布

```tex
$$f(x) = \frac{1} {\sqrt {2\pi} \sigma}{\mathrm e}^{-\frac{(x-\mu)^2}{2\sigma ^ 2}}$$
```


$$
f(x) = \frac{1} {\sqrt {2\pi} \sigma}{\mathrm e}^{-\frac{(x-\mu)^2}{2\sigma ^ 2}}
$$
```tex
$$f(x) = \frac{1}{\sqrt{2\pi}\sigma}\exp\left[-\frac{(x-\mu)^2}{2\sigma ^ 2}\right]$$
```
$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma}\exp\left[-\frac{(x-\mu)^2}{2\sigma ^ 2}\right]
$$



### 麦克斯韦方程组

```tex
$$
\begin{aligned}
\oint _l \boldsymbol{H} \cdot \mathrm{d} \boldsymbol{l} & = \iint_S \boldsymbol{J} \cdot \mathrm{d} \boldsymbol{S} + \iint_S \frac{\partial \boldsymbol{D}}{\partial t} \cdot {\mathrm d}\boldsymbol{S} \\
\oint_l \boldsymbol{E} \cdot \mathrm{d} \boldsymbol{l} & = -\iint_s \frac{\partial \boldsymbol{B}}{\partial t} \cdot \mathrm{d} \boldsymbol{S}\\
\oint_S \boldsymbol{B} \cdot \mathrm{d} \boldsymbol{S}& = 0 \\
\oint_S \boldsymbol{D} \cdot \mathrm{d} \boldsymbol{S} & = \iiint_V \rho \mathrm{d} V
\end{aligned}
$$
```

$$
\begin{aligned}
\oint _l \boldsymbol{H} \cdot \mathrm{d} \boldsymbol{l} & = \iint_S \boldsymbol{J} \cdot \mathrm{d} \boldsymbol{S} + \iint_S \frac{\partial \boldsymbol{D}}{\partial t} \cdot {\mathrm d}\boldsymbol{S} \\
\oint_l \boldsymbol{E} \cdot \mathrm{d} \boldsymbol{l} & = -\iint_s \frac{\partial \boldsymbol{B}}{\partial t} \cdot \mathrm{d} \boldsymbol{S}\\
\oint_S \boldsymbol{B} \cdot \mathrm{d} \boldsymbol{S}& = 0 \\
\oint_S \boldsymbol{D} \cdot \mathrm{d} \boldsymbol{S} & = \iiint_V \rho \mathrm{d} V
\end{aligned}
$$

```tex
\begin{aligned}
\nabla \times \boldsymbol{H} & = \boldsymbol{J} + \frac{\partial \boldsymbol{D}}{\partial t} \\
\nabla \times \boldsymbol{E} & = - \frac{\partial \boldsymbol{B}}{\partial t} \\
\nabla \cdot \boldsymbol{B} & = 0 \\
\nabla \cdot \boldsymbol{D} & = \rho
\end{aligned}
```

$$
\begin{aligned}
\nabla \times \boldsymbol{H} & = \boldsymbol{J} + \frac{\partial \boldsymbol{D}}{\partial t} \\
\nabla \times \boldsymbol{E} & = - \frac{\partial \boldsymbol{B}}{\partial t} \\
\nabla \cdot \boldsymbol{B} & = 0 \\
\nabla \cdot \boldsymbol{D} & = \rho
\end{aligned}
$$

### 范德蒙德行列式

```tex
$$
\begin{vmatrix}
1 & 1 & 1 & \cdots & 1 \\
x_{1} & x_{2} & x_{3} & \cdots & x_{n} \\
x_{1}^2 & x_{2}^2 & x_{3}^2 & \cdots & x_{n}^2 \\ 
x_{1}^3 & x_{2}^3 & x_{3}^3 & \cdots & x_{n}^3 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
x_{1}^{n-1} & x_2^{n-1} & x_{3}^{n-1} & \cdots & x_n^{n-1} 
\end{vmatrix} = \prod_{1 \le j \le i \le n}(x_i - x_j)
$$
```

$$
\begin{vmatrix}
1 & 1 & 1 & \cdots & 1 \\
x_{1} & x_{2} & x_{3} & \cdots & x_{n} \\
x_{1}^2 & x_{2}^2 & x_{3}^2 & \cdots & x_{n}^2 \\ 
x_{1}^3 & x_{2}^3 & x_{3}^3 & \cdots & x_{n}^3 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
x_{1}^{n-1} & x_2^{n-1} & x_{3}^{n-1} & \cdots & x_n^{n-1} 
\end{vmatrix} = \prod_{1 \le j \le i \le n}(x_i - x_j)
$$

### 欧拉恒等式

```tex
\mathrm{e}^{\mathrm{i} x} = \cos x + \mathrm{i} \sin x
```

$$
\text{e}^{\text{i} x} = \cos x + \text{i} \sin x
$$

### 巴塞尔问题

```tex
1 + \frac{1}{2^2} + \frac{1}{3^2} + \cdots = \sum_{i=1}^{\infty} \frac{1}{i^2} =\frac{\pi^{2}}{6}
```

$$
1 + \frac{1}{2^2} + \frac{1}{3^2} + \cdots = \sum_{i=1}^{\infty} \frac{1}{i^2} =\frac{\pi^{2}}{6}
$$

### 斐波那契数列

```tex
$$
F(n)= \left\lbrace\begin{array}{ll}
1, &n \le 2\\
F(n-1) + F(n-2),& n \ge 3 
\end{array}\right.
$$
```

$$
F(n)= \left\lbrace\begin{array}{ll}
1, &n \le 2\\
F(n-1) + F(n-2),& n \ge 3 
\end{array}\right.
$$

### 牛顿莱布尼茨公式

```tex
$\int _a^b f(x)\mathrm{d}x = F(b) - F(a)$$
```

$$
\int _a^b f(x)\mathrm{d}x = F(b) - F(a)
$$