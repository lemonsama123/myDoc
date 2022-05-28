---
title: GCD
author: Lemon
top: false
cover: false
toc: true
mathjax: true
tags:
categories:
  - 算法
abbrlink: 2071db18
reprintPolicy: cc_by
date: 2021-12-16 22:48:19
coverImg:
summary:
img:
password:
---



## 简介

GCD，即[最大公约数](https://baike.baidu.com/item/%E6%9C%80%E5%A4%A7%E5%85%AC%E7%BA%A6%E6%95%B0/869308?fr=aladdin)，是指多个整数共有约数中最大的一个，常见的求解方法有[质因数分解法](https://baike.baidu.com/item/质因数分解)、[短除法](https://baike.baidu.com/item/短除法)、[辗转相除法](https://baike.baidu.com/item/辗转相除法)和[更相减损法](https://baike.baidu.com/item/更相减损法)



## 辗转相除法



### 引例

我们尝试使用辗转相除法求 319 和 377 的最大公倍数：

![image-20220102214834011](https://s2.loli.net/2022/01/19/xpFos89vyVhBLmq.png)

通过上述求解过程，我们可以得到递归方程：
$$
\text{GCD}(a, b) = \text{GCD}(b, a \mod b)
$$
结束条件为：$b = 0$



### 递归实现

```java
public static int GCD(int a, int b) {
    if (b == 0) {
        return a;
    } else {
        return GCD(b, a % b);
    }
}
```

### 迭代实现

```java
public static int GCD(int a, int b) {
    while (b != 0) {
        int t = a;
        a = b;
        b = t % b;
    }
    return a;
}
```



## Stein算法

[Stein算法](https://baike.baidu.com/item/Stein%E7%AE%97%E6%B3%95/7874057#4)是一种计算两个数最大公约数的算法，是针对欧几里德算法在对大整数进行运算时，需要试商导致增加运算时间的缺陷而提出的改进算法。



### 算法描述

1. 设置 $a_{n}=|a|$、$b_{n}=|b|$、$c_{n} = 1$ 和 $ n = 1$
2. 如果 $a_{n} = b_{n}$，那么 $a_{n}$（或 $b_{n}$）* $c_{n}$ 是最大公约数，算法结束
3. 如果 $a_{n} = 0$，$b_{n}$ 是最大公约数，算法结束
4. 如果 $b_{n} = 0$，$a_n$ 是最大公约数，算法结束
5. 如果 $a_{n}$ 和 $b_{n}$ 都是偶数，则 $a_{n+1} = \frac{a_n}{2}$，$b_{n+1} = \frac{b_n}{2}$，$c_{n+1} = c_{n}*2$
6. 如果 $a_{n}$ 是偶数，$b_{n}$ 不是偶数，则 $a_{n+1} = \frac{a_{n}}{2}$，$b_{n+1} = b_{n}$，$c_{n+1}= c_{n}$
7. 如果 $b_{n}$ 是偶数，$a_{n}$ 不是偶数，则$b_{n+1}=\frac{b_{n}}{2}$，$a_{n+1} = a_{n}$，$c_{n+1} = c_{n}$
8. 如果 $a_{n}$ 和 $b_{n}$ 都不是偶数，则 $a_{n+1} = \frac{|An-Bn|}{2}$，$b_{n+1} = \min(a_{n},b_{n})$，$c_{n+1} = c_{n}$
9. n=n+1，转2



### Java 实现

。。。。。。

