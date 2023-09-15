+++
title = "РФ23-01Б: Практика N4"
template = "page.html"
date = 2023-09-15
[taxonomies]
tags = ["РФ23-01Б", "МА1"]
[extra]
summary = "Предел последовательности"
mathjax = "tex-mml"
+++

<!-- more -->

## Предел последовательности

### Разбор домашней работы

**Д10в.** Докажем неравенство
$$
   \left| \sin \sum_{k=1}^n x_k \right| \leq \sum_{k=1}^n \sin{x_k},
$$
где $x_k\in [0;\pi]$, $k=1,\ldots, n,$ методом математической индукции.

При $n=1$ неравенство тривиально выполняется. Докажем неравенство при $n=2$, для
этого заметим, что по неравенству треугольника
$$
   |\sin{(x_1+x_2)}|=|\sin{x_1}\cos{x_2}+\sin{x_2}\cos{x_1}|\leq |\sin{x_1}\cos{x_2}|+|\sin{x_2}\cos{x_1}|.
$$
Так как $|\cos{x_i}|\leq 1$ при $x_i\in \mathbb{R}$ и $\sin{x_i}\geq 0$ при $x_i\in [0;\pi]$,
$$
   |\sin{(x_1+x_2)}|\leq |\sin{x_1}||\cos{x_2}|+|\sin{x_2}||\cos{x_1}|\leq \sin{x_1}+\sin{x_2}.
$$

Теперь предположим, что при некотором $p\in \mathbb{N}$
$$
   \left| \sin \sum_{k=1}^p x_k \right| \leq \sum_{k=1}^p \sin{x_k},
$$
где $x_k\in [0;\pi]$, $k=1,\ldots, p.$ Тогда выполняется цепочка неравенств
$$
   \left| \sin \sum_{k=1}^{p+1} x_k \right|=
   \left| \sin \left(\sum_{k=1}^{p} x_k \right) \cos{x_{p+1}} + \sin{x_{p+1}} \cos \left(\sum_{k=1}^{p} x_k \right)\right|\leq
$$
$$
   \leq \left| \sin \left(\sum_{k=1}^{p} x_k \right)\right| \left| \cos{x_{p+1}} \right| + \left|\sin{x_{p+1}}\right| \left| \cos \left(\sum_{k=1}^{p} x_k \right)\right|
   \leq \left| \sin \left(\sum_{k=1}^{p} x_k \right) \right| + \left|\sin{x_{p+1}} \right| \leq
$$
$$
   \left / \text{по гипотезе индукции} \right/ \leq \sum_{k=1}^{p} \sin  x_k   + \sin{x_{p+1}} = \sum_{k=1}^{p+1} \sin  x_k.
$$ 
Тем самым согласно принципу математической индукции неравенство справедливо для всех $n\in\mathbb{N}$.

### Точная верхняя и нижняя грани

**Д19а.** Докажем, что $\inf{(X+Y)}  = \inf X+\inf Y$, где множество $X+Y$ состоит из всевозможных сумм вида $x+y$,
где $x\in X$ и $y\in Y$.

Предположим, что $i_X = \inf X$, $i_Y=\inf Y$. По определению точной нижней грани, во-первых, для всех $x\in X$ справедливо
$i_X\leq x$ и для всех $y\in Y$ справедливо $i_Y\leq y.$ Складывая эти два неравенства, получим, что
для всех $x\in X$ и $y\in Y$ выполняется неравенство
$$
   i_X+i_Y \leq x+y.
$$
Иными словами, всякий элемент из $X+Y$ не меньше чем сумма $i_X+i_Y.$

Во-вторых, для всякого $\varepsilon >0$ найдутся $x_\varepsilon\in X$ и $y_\varepsilon \in Y$ такие, что
$$
   x_\varepsilon < i_X + \frac{\varepsilon}{2},\ y_\varepsilon < i_Y + \frac{\varepsilon}{2}.
$$
Откуда $x_\varepsilon + y_\varepsilon < i_X+i_Y + \varepsilon.$ Таким образом, если мы увеличим число $i_X+i_Y$ на сколь угодно малую положительную константу, то во множестве $X+Y$ найдется элемент, который будет строго меньше чем это увеличенное значение.
Следовательно, $i_X+i_Y=\inf{(X+Y)}.$

### Предел числовой последовательности

$$
   \lim_{n\to\infty} a_n=a \Leftrightarrow \forall \varepsilon>0\ \exists N=N(\varepsilon)\ \forall n> N\ (|a_n-a|<\varepsilon).
$$

### Домашняя работа

1. Д18, Д20.
2. Д21, Д22-27.
3. Д41.