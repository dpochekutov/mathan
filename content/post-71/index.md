+++
title = "БФ23-05Б: Практика N18-19"
template = "page.html"
date = 2023-11-13
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Исследование функций на непрерывность. Равномерная непрерывность"
mathjax = "tex-mml"
+++

<!-- more -->

## Исследование функций на непрерывность

### Разбор домашней работы

**Д674з** Докажем, что функция $f(x)=\arctg{x}$ является непрерывной на $\mathbb{R}$.

Пусть $x_0\in \mathbb{R}$. Рассмотрим величину
$$
    |\mathop{arctg}x-\mathop{arctg}{x_0}|=|\mathop{arctg}\frac{x-x_0}{1+xx_0}|.
$$



## Равномерная непрерывность

### Определение равномерной непрерывности

Функция $f(x)$ называеся *равномерно* *непрерывной* *на множестве* $M$ тогда и только тогда, когда выполняется 
условие
$$
 \forall \varepsilon >0 \exists \delta>0 \forall x', x''\in M: |x'-x''|<\delta \Rightarrow |f(x')-f(x'')|<\varepsilon.
$$

Запишем отрицание условия равномерной непрерывности функции $f(x)$ на множестве $M$:
$$
 \exists \varepsilon >0 \forall \delta>0 \exists x', x''\in M: |x'-x''|<\delta \Rightarrow |f(x')-f(x'')|\geq \varepsilon.
$$


### Примеры

**Д793** Является ли равномерно непрерывной функция $f(x)=x^2$ на а) интервале $(-l;l)$, где $l$ есть
любое положительное число; б) на множестве $\mathbb{R}$.

а) Пусть $x',x'' \in (-l;l)$, тогда величина 
$$
    |(x')^2-(x'')^2|=|(x'-x'')(x'+x'')|\leq |x'-x''|(|x'|+|x''|)< 2l |x'-x''|< \varepsilon,
$$
если $|x'-x''|<\delta := \frac{\varepsilon}{2}.$ Условие равномерной непрерывности выполняется.

б) Рассмотрим две бесконечно большие последовательности $x'_n=\sqrt{n+1}, x''_n=\sqrt{n}\in \mathbb{R}$, при любом $n\in \mathbb{N}$
$$
    |(x'_n)^2-(x''_n)^2|=|(n+1)-n|=1.
$$
В силу того, что $x'_n - x''_n \to 0$ при $n\to +\infty$, выполняется отрицание условия равномерной сходимости.


## Домашняя работа

1. Д678, Д679, Д680, Д682, Д690, Д702.
2. Д786, Д788, Д789, Д790, Д794.
