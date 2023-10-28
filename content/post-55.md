+++
title = "РФ23-01Б: Практика N16"
template = "page.html"
date = 2023-10-27
[taxonomies]
tags = ["rf23-01b", "MA1"]
[extra]
summary = "Сравнение функций (продолжение)"
mathjax = "tex-mml"
+++

<!-- more -->
## Сравнение функций (продолжение)

### О разложение функций $\sin{x}$ и $\cos{x}$ в окрестности нуля

Хорошо известное равенство 
$$
    \lim_{x\to 0} \frac{\sin{x}}{x} = 1,
$$
называемое первым замечательным пределом, эквивалентно тому, что
$$
    \sin{x} = x + o(x), x\to 0.
$$
С его помощью легко найти
$$
    \lim_{x\to 0} \frac{1-\cos{x}}{\frac{1}{2}x^2}= \lim_{x\to 0} \frac{\sin^2{\frac{x}{2}}}{\left(\frac{x}{2}\right)^2} = 1.
$$
Тогда, вспомнив, $\cos{x}\to 1$ при $x\to 0$, мы можем заключить, что
$$
    \cos{x}=1-\frac{1}{2}x^2+o(x^2), x\to 0.
$$

Мы хотим получить еще один член разложений для синуса и косинса  в окрестности точки $0,$ 
опираясь только на пройденный материал. Для этого найдем значение предела
$$
    \lim_{x\to 0} \frac{x-\sin{x}}{x^3}=\lim_{x\to 0} \frac{1-\frac{\sin{x}}{x}}{x^2}.
$$
Решение, которое мы приведём, является адаптированным вариантом нахождения этого предела из [<a href="#1">1</a>].

В начале заметим, что формула синуса двойного угла даёт нам равенства
$$
    2\sin{\frac{x}{2}\cos{\frac{x}{2}}}=\sin{x},
$$
$$
    4\sin{\frac{x}{4}}\cos{\frac{x}{4}}\cos{\frac{x}{2}} = \sin{x}.
$$
По индукции можно доказать, что и для любого $n\in\mathbb{N}$ верно
$$
    2^n \sin{\frac{x}{2^n}}\prod_{k=1}^n \cos{\frac{x}{2^k}}=\sin{x}.
$$
Действительно, база индукции ($n=1$ и $n=2$) даётся указанными равенствами. 
Предположим, что для некоторого
$(p-1)\in\mathbb{N}$ выполняется
$$
    2^{p-1} \sin{\frac{x}{2^{p-1}}}\prod_{k=1}^{p-1} \cos{\frac{x}{2^k}}=\sin{x}.
$$
Тогда последовательное применение сначала формулы синуса двойного угла, а затем гипотезы индукции,
приводит к равенству
$$
    2^p \sin{\frac{x}{2^{p}}}\prod_{k=1}^{p} \cos{\frac{x}{2^k}}=
    2^p \sin{\frac{x}{2^{p}}} \cos{\frac{x}{2^{p}}} \prod_{k=1}^{p-1} \cos{\frac{x}{2^k}}=
$$
$$
    =2^{p-1}\sin{\frac{x}{2^{p-1}}} \prod_{k=1}^{p-1} \cos{\frac{x}{2^k}}=\sin{x}.
$$



Теперь напомним, что в ходе доказательства первого замечательного предела нами было показано, что
$$
    \frac{\sin{x}}{x}< 1 < \frac{\textup{tg } x}{x}, x\in \left(0;\frac{\pi}{2}\right).
$$
С одной стороны, при $ x\in \left(0;\frac{\pi}{2}\right)$ мы имеем неравенство
$$
    \frac{\sin{\frac{x}{2^n}}}{\frac{x}{2^n}}=\frac{2^n \sin{\frac{x}{2^n}}}{x}<1,
$$
умножением которого на $\prod_{k=1}^n \cos{\frac{x}{2^k}},$ получаем
$$
    \frac{2^n \sin{\frac{x}{2^n}}\prod_{k=1}^n \cos{\frac{x}{2^k}}}{x}=\frac{\sin{x}}{x}< \prod_{k=1}^n \cos{\frac{x}{2^k}}.
$$
Таким образом, для $x\in \left(0;\frac{\pi}{2}\right)$ выполняется
$$
    A_n(x):= 1-\prod_{k=1}^n \cos{\frac{x}{2^k}}< 1 -\frac{\sin{x}}{x}.
$$

С другой стороны, при $ x\in \left(0;\frac{\pi}{2}\right)$ выполняется неравенство
$$
    1< \frac{\textup{tg } \frac{x}{2^n}}{\frac{x}{2^n}}=\frac{2^n\sin{\frac{x}{2^n}}}{x\cos{\frac{x}{2^n}}},
$$
из которого умножением на $\prod_{k=1}^n \cos{\frac{x}{2^k}},$ получаются
$$
    \prod_{k=1}^n \cos{\frac{x}{2^k}} < \frac{\sin{x}}{x\cos{\frac{x}{2^n}}},
$$
$$
    1-\frac{\sin{x}}{x} < 1 - \cos{\frac{x}{2^n}}\prod_{k=1}^n \cos{\frac{x}{2^k}}=:B_n(x).
$$

В конечном итоге, мы получаем оценку
$$
    \frac{A_n(x)}{x^2}<\frac{1 -\frac{\sin{x}}{x}}{x^2} <\frac{B_n(x)}{x^2}.
$$


Заметим, что величина $A_n(x)$ с помощью формулы телескопического суммирования может быть представленно в виде
$$
    A_n(x)= \left(1-\cos{\frac{x}{2^n}}\right)+\cos{\frac{x}{2^n}}\left(1-\cos{\frac{x}{2^{n-1}}}\right)
    +\cos{\frac{x}{2^n}}\cos{\frac{x}{2^{n-1}}}\left(1-\cos{\frac{x}{2^{n-2}}}\right)+\ldots+
$$
$$
    +\cos{\frac{x}{2^n}}\cdot\ldots\cdot \cos{\frac{x}{2^2}}\left(1-\cos{\frac{x}{2}}\right)
    =\sum_{i=1}^{n}\prod_{j=i+1}^{n} \cos{\frac{x}{2^j}}\left(1-\cos{\frac{x}{2^i}}\right).
$$
Поэтому   предел
$$
    \lim_{x\to +0} \frac{ A_n(x)}{x^2} = \lim_{x\to +0}\sum_{i=1}^{n}\prod_{j=i+1}^{n} \cos{\frac{x}{2^j}}\frac{\left(1-\cos{\frac{x}{2^i}}\right)}{x^2}
    = \sum_{i=1}^{n}\frac{1}{2^{2i+1}}=\frac{1-\frac{1}{4^n}}{6}.
$$

Величина $B_n(x)$ может быть представлена в виде
$$
    B_n(x)= \left(1 - \cos{\frac{x}{2^n}}\right)+\cos{\frac{x}{2^n}} A_n(x),
$$
следовательно, 
$$
    \lim_{x\to +0} \frac{ B_n(x)}{x^2} =\frac{1}{2^{2n+1}}+\frac{1-\frac{1}{4^n}}{6}.
$$
По определению предела для всякого $\varepsilon >0$ найдется $\delta >0$ такое, что для $x\in(0;\delta)$
одновременно будут выполняться неравенства
$$
    \frac{1-\frac{1}{4^n}}{6}-\varepsilon <\frac{ A_n(x)}{x^2},  \frac{B_n(x)}{x^2}< \frac{1}{2^{2n+1}}+\frac{1-\frac{1}{4^n}}{6}+\varepsilon,
$$
но тогда и 
$$
     \frac{1-\frac{1}{4^n}}{6}-\varepsilon < \frac{1 -\frac{\sin{x}}{x}}{x^2} < \frac{1}{2^{2n+1}}+\frac{1-\frac{1}{4^n}}{6}+\varepsilon.
$$
Переходя к пределу по $n\to \infty$, получим, что для всякого $\varepsilon >0$ найдется $\delta >0$ такое, что для $x\in(0;\delta)$
$$
     \frac{1}{6}-\varepsilon \leq \frac{1 -\frac{\sin{x}}{x}}{x^2} \leq \frac{1}{6}+\varepsilon.
$$
Таким образом, мы показали, что
$$
      \lim_{x\to +0} \frac{1 -\frac{\sin{x}}{x}}{x^2} = \frac{1}{6}.
$$
Поскольку функция, стоящая под знаком предела является четной, то
$$
      \lim_{x\to 0} \frac{1 -\frac{\sin{x}}{x}}{x^2} = \frac{1}{6},
$$
и при $x\to 0$ справедливо разложение
$$
    \sin{x}=x-\frac{1}{6}x^3+o(x^3).
$$

Теперь легко найти, что
$$
    \lim_{x\to 0} \frac{\cos{x}-(1-\frac{x^2}{2})}{x^4}=\lim_{x\to 0} \frac{1-2\sin^2{\frac{x}{2}}-(1-\frac{x^2}{2})}{x^4}=
$$
$$
    \lim_{x\to 0} \frac{-2(\frac{x}{2}-\frac{1}{6}\cdot\frac{x^3}{8}+o(x^3))^2+\frac{x^2}{2})}{x^4}=
    \lim_{x\to 0} \frac{\frac{x^4}{24}+o(x^4)}{x^4}=\frac{1}{24}.
$$
Откуда следует, что при $x\to 0$ имеется разложение
$$
    \cos{x}=1-\frac{x^2}{2}+\frac{x^4}{24}+o(x^4).
$$

#### Библиография
 [<a name="1">[1](https://math.stackexchange.com/a/158134)</a>] [Hans Lundmark](https://math.stackexchange.com/users/1242/hans-lundmark), Evaluation of $\lim\limits_{x\rightarrow0} \frac{\tan(x)-x}{x^3}$, URL (version: 2012-06-14): https://math.stackexchange.com/q/158134
### Домашняя работа

Подготовка к контрольной работе

[Нулевой вариант](/MA1_Test1_v0.pdf)
