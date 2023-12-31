+++
title = "РФ23-01Б: Практика N20"
template = "page.html"
date = 2023-11-10
[taxonomies]
tags = ["rf23-01b", "MA1"]
[extra]
summary = "Равномерная непрерывность"
mathjax = "tex-mml"
+++

<!-- more -->
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

**Д790** Показать, что функция $f(x)=\sin{x^2}$ непрерывна и ограничена на $\mathbb{R}$, но не является равномерно
непрерывной на этом множестве.

Функция является непрерывной как элементарная функция на своей области определения. Ограниченность очевидна.

Рассмотрим две бесконечно большие числовые последовательности
$$
    x'_n=\sqrt{\pi n}, x''_n=\sqrt{\pi n + \frac{\pi}{2}}.
$$

Заметим, что их разность 
$$
    0<x''_n - x'_n = x'_n=\sqrt{\pi n + \frac{\pi}{2}}-\sqrt{\pi n}=\frac{\frac{\pi}{2}}{\sqrt{\pi n + \frac{\pi}{2}}+\sqrt{\pi n}}\to 0
$$
при $n\to +\infty$. Следовательно, для любого $\delta >0 $ найдутся такие члены этих последовательностей 
$x'_N$, $x''_N$,
$$
    0<x''_N - x'_N<\delta.
$$
При этом величина
$$
    |f(x''_N)-f(x'_N)|=|\sin{\left(\pi n+\frac{\pi}{2}\right)}-\sin{\pi n}|=1=:\varepsilon.
$$
Таким образом, выполняется отрицание условия равномерной непрерывности.

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

### Домашняя работа

1. Д786, Д788, Д789, Д792.
2. Д794.
