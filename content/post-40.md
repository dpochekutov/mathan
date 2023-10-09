+++
title = "РФ23-01Б: Практика N11"
template = "page.html"
date = 2023-10-10
[taxonomies]
tags = ["rf23-01b", "MA1"]
[extra]
summary = "Предел функции"
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

### Домашняя работа

1. Д390, Д391, Д392, Д394, Д400.
2. Д405, Д406.
