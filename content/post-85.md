+++
title = "БФ23-05Б: Практика N22-23"
template = "page.html"
date = 2023-11-27
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Основные правила дифференцирования. Вычисление производных"
mathjax = "tex-mml"
+++

<!-- more -->

## Основные правила дифференцирования. Вычисление производных

## Разбор домашней работы

**Д831** Найти $f'(1)$, если
$$
    f(x)=x+(x-1)\arcsin\sqrt{\frac{x}{x+1}}.
$$

По определению 
$$
    f'(1)=\lim_{h\to\infty} \frac{f(1+h)-f(1)}{h}=\lim_{h\to\infty} \frac{1+h + h\arcsin\sqrt{\frac{1+h}{2+h}}-1}{h}=
$$
$$
    =\lim_{h\to\infty} \frac{h + h\arcsin\sqrt{\frac{1+h}{2+h}}}{h}=\lim_{h\to\infty} \left(1 + \arcsin\sqrt{\frac{1+h}{2+h}}}\right)
$$

## Домашняя работа

1. Д885-970 (11 штук).
2. Д984, Д985, Д986.


