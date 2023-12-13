+++
title = "РФ23-01Б: Практика N29"
template = "page.html"
date = 2023-12-12
[taxonomies]
tags = ["rf23-01b", "MA1"]
[extra]
summary = "Формула Тейлора (продолжение)"
mathjax = "tex-mml"
+++

<!-- more -->
## Формула Тейлора

### Приближенные вычисления с помощью формулы Тейлора

**Д1397г** Вычислить $\sqrt{5}$ с точностью до $10^{-4}$.

Рассмотрим функцию $f(x)=\sqrt{4+x}$ такую, что $f(1)=\sqrt{5}$.

Запишем остаточный член формулы Тейлора для $f(x)$ с центром в точке $x_0=0$  в форме Лагранжа. Для начала найдем 
$$
    f^{(n)}(x)=\left(\sqrt{4+x}\right)^{(n)}
    = \left( \frac{1}{2}(4+x)^{-\tfrac{1}{2}}\right)^{(n-1)}=
$$
$$    
    =\frac{1}{2}\left(-\frac{1}{2}\right)\left(-\frac{3}{2}\right)\cdot\ldots\cdot \left(-\frac{2n-3}{2}\right)\left(4+x\right)^{-n+\frac{1}{2}}=
    \frac{(-1)^{(n-1)} (2n-3)!!}{2^n (4+x)^{n-\frac{1}{2}}}.
$$
Тогда при $x\in[0;1]$ остаток  имеет вид
$$
    r_{n-1}(x)=\frac{f^{(n)}(\xi)}{n!}x^{n}=
    \frac{(-1)^{(n-1)} (2n-3)!!}{2^n (4+\xi)^{n-\frac{1}{2}}\cdot n! }x^n,
$$
где $0<\xi<1$. Мы можем оценить величину его модуля следующим образом
$$
    |r_{n-1}(x)|\leq \frac{(2n-3)!!}{2^n (4+\xi)^{n-\frac{1}{2}}\cdot n!}<\frac{(2n-3)!!}{2^n \cdot 4^{n-\frac{1}{2}}\cdot n!}=\frac{(2n-3)!!}{(2n)!!}\cdot \frac{1}{2^{2n+1}}.
$$
Поскольку
$$
    \frac{(2n-3)!!}{(2n)!!}=\frac{1}{2}\frac{3}{4}\cdot \ldots \frac{2n-3}{2n-2}\cdot \frac{1}{2n}<\frac{1}{4n},
$$  
мы можем утверждать, что
$$
    |r_{n-1}(x)|<\frac{1}{n}\cdot \frac{1}{2^{2n+3}}<10^{-4},
$$
если $n=5$. Таким образом, нужную нам точность при вычислении $f(1)=\sqrt{5}$ даст разложение Тейлора для $f(x)$ до $x^4$:
$$
    f(x)\approx 2 \left(1+\frac{x}{4}\right)^{\frac{1}{2}}=
$$
$$  =
    2\left(
    1+\frac{1}{2}\cdot \frac{x}{4} 
    + \frac{\frac{1}{2}\cdot(\frac{1}{2}-1)}{2} \cdot  \frac{x^2}{16}
    +  \frac{\frac{1}{2}(\frac{1}{2}-1)(\frac{1}{2}-2)}{6} \cdot  \frac{x^3}{64}+\right.
$$
$$  \left.
    + \frac{\frac{1}{2}(\frac{1}{2}-1)(\frac{1}{2}-2)(\frac{1}{2}-3)}{24} \cdot  \frac{x^4}{256}
    \right)=2+\frac{x}{4}-\frac{x^2}{64}+\frac{x^3}{512}-\frac{5x^4}{16384}.
$$
Тогда 
$$
    \sqrt{5}\approx 2 + \frac{1}{4}-\frac{1}{64}+\frac{1}{512}-\frac{5}{16384}=2.2360.
$$

### Раскрытие неопределенностей с помощью формулы Тейлора

**Д1400** Используя локальное разложение в окрестности нуля
$$
    (1+x)^{\alpha}=1+\alpha x + \frac{\alpha(\alpha-1)}{2!}x^2+\ldots+\frac{\alpha(\alpha-1)\ldots(\alpha-n+1)}{n!}x^n+o(x^n),
$$
вычислить предел
$$
    L=\lim_{x\to +\infty} x^{\frac{3}{2}}\left(
        \sqrt{x+1}+\sqrt{x-1}-2\sqrt{x}
    \right).
$$
Запишем
$$
    L=\lim_{x\to +\infty} x^{2}\left(
        \sqrt{1+\frac{1}{x}}+\sqrt{1-\frac{1}{x}}-2
    \right)=
$$
$$
    =\lim_{x\to +\infty} x^{2}\left[
        1+\frac{1}{2x}-\frac{1}{8x^2}+o\left(\frac{1}{x^2}\right)+
        1-\frac{1}{2x}-\frac{1}{8x^2}+o\left(\frac{1}{x^2}\right)-2
    \right]=
$$
$$
    =\lim_{x\to +\infty} \frac{
        -\frac{1}{4x^2}+o\left(\frac{1}{x^2}\right)
    }{\frac{1}{x^2}}
   =\lim_{x\to +\infty} \left[
    -\frac{1}{4}+\frac{o\left(\frac{1}{x^2}\right)
    }{\frac{1}{x^2}}
    \right]    
    =-\frac{1}{4}.
$$

### Домашняя работа

1. Д1394вг, 1395, 1397бв.
2. Д1399, Д1401-05.


