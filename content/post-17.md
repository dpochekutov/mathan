+++
title = "БФ23-05Б: Практика N5-6"
template = "page.html"
date = 2023-09-18
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Предел числовой последовательности"
mathjax = "tex-mml"
+++

<!-- more -->

## Разбор домашней работы

[Pdf-файл](/MA1_Homework_2_bf.pdf)

## Точная верхняя и нижняя грани

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

## Определение предела числовой последовательности

$$
   \lim_{n\to\infty} a_n=a \Leftrightarrow \forall \varepsilon>0\ \exists N=N(\varepsilon)\ \forall n> N\ (|a_n-a|<\varepsilon).
$$

$$
   \lim_{n\to\infty} a_n=\infty \Leftrightarrow \forall \varepsilon>0\ \exists N=N(\varepsilon)\ \forall n> N\ \left(|a_n|>\frac{1}{\varepsilon}\right).
$$

### Домашняя работа

1. Д18б, Д19б, Д20а.
2. Д41, Д42а, Д43аб.