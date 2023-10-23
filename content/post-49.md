+++
title = "БФ23-05Б: Практика N12-13"
template = "page.html"
date = 2023-10-23
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Предел функции. Раскрытие неопределенностей (рациональные функции)."
mathjax = "tex-mml"
+++

<!-- more -->

## Предел функции

### Точная нижняя и верхняя грань функции

Число $i=\sup_{x\in X} f(x)$ тогда  и только тогда, когда
1. $\forall x\in X$ значение $f(x)\geq i$.
2. $\forall \varepsilon>0$ $\exists x_\varepsilon \in X$ $\left(f(x_\varepsilon)<i+\varepsilon\right)$.


Число $s=\sup_{x\in X} f(x)$ тогда  и только тогда, когда
1. $\forall x\in X$ значение $f(x)\leq s$.
2. $\forall \varepsilon>0$ $\exists x_\varepsilon \in X$ $\left(f(x_\varepsilon)>s-\varepsilon\right)$.

Точная верхняя грань $\sup_{x\in X} f(x)=+\infty$ тогда и только тогда, когда
$$ 
    \forall \varepsilon > 0 \exists x' \in X \left(f(x)>\frac{1}{\varepsilon}\right).
$$
Из этого условия вытекает, что функция $f$ является неограниченной на $X$.

[Демидович 386](/D386.pdf)

## Вычисление пределов

### Аудиторные задачи

1. Д408-410.
2. Д411-415.


### Домашняя работа

1. Д403-Д406.
2. Д416-428.