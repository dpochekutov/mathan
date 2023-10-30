+++
title = "БФ23-05Б: Практика N13-14"
template = "page.html"
date = 2023-10-30
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Раскрытие неопределенностей (иррациональные  и тригонометрические функции)."
mathjax = "tex-mml"
+++

<!-- more -->

## Вычисление пределов

### Разбор домашней работы

**Д428** Найдите предел (ниже $n,m\in\mathbb{N}$)
$$\lim\limits_{x\to 1}\left(\frac{m}{1-x^m}-\frac{n}{1-x^n}\right).$$

Рассмотрим
$$
    \frac{m}{1-x^m}-\frac{n}{1-x^n}=\frac{m(1+x+\ldots+x^{n-1})-n(1+x+\ldots+x^{m-1})}{(1-x)(1+x+\ldots+x^{m-1})(1+x+\ldots+x^{n-1})}=
$$
$$
    =\frac{m(n+(x-1)+\ldots+(x^{n-1}-1))-n(m+(x-1)+\ldots+(x^{m-1}-1))}{(1-x)(1+x+\ldots+x^{m-1})(1+x+\ldots+x^{n-1})}=
$$
$$
    =\frac{m((x-1)+\ldots+(x^{n-1}-1))-n((x-1)+\ldots+(x^{m-1}-1))}{(1-x)(1+x+\ldots+x^{m-1})(1+x+\ldots+x^{n-1})}.
$$
Поскольку для $l\in\mathbb{N}$ справедлива формула 
$$
    \frac{x^l-1}{x-1}=1+x+\ldots+x^{l-1}
$$
суммы геометрической прогрессии, получаем
$$
    \lim\limits_{x\to 1}\left(\frac{m}{1-x^m}-\frac{n}{1-x^n}\right)=\frac{m(1+\ldots+(n-1))-n(1+\ldots+(m-1))}{-mn}=
$$
$$
    =\frac{m(n-1)n-n(m-1)m}{-2mn}=\frac{m-n}{2}.
$$

### Домашняя работа

1. Д436, Д438, Д440б Д442, Д451,Д452.
2. Д476, Д477, Д482.

### Подготовка к контрольной работе

[Нулевой вариант](/MA1_Test1_v0.pdf)