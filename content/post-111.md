+++
title = "РФ22-01Б: Практика N17"
template = "page.html"
date = 2023-12-22
[taxonomies]
tags = ["rf22-01b", "MA3"]
[extra]
summary = "Поверхностные интегралы первого рода"
mathjax = "tex-mml"
+++

<!-- more -->

## Поверхностные интегралы первого рода

### Форма объема на сфере

Рассмотрим следующую параметризацию 
$$
    x=a\sin{u}\sin{v}, y=a\cos{u}\sin{v}, z=a\cos{v}
$$
двумерной сферы с центром в начале координат радиуса $a$.

Касательные векторы имеют координаты
$$
    r_u=(a\cos{u}\sin{v}, -a\sin{u}\sin{v}, 0),
$$
$$
    r_v=(a\sin{u}\cos{v}, a\cos{u}\cos{v}, -a\sin{v}).
$$
Найдем коэффициенты
$$
    E=\left<r_u, r_u\right> =  a^2 \sin^2{v}, F=\left<r_u, r_v\right> = 0,
$$
$$
    G=\left<r_v, r_v\right>= a^2.
$$
Следовательно, форма объема имеет вид
$$
    d S = \sqrt{EG-F^2}\ du\wedge dv = a^2|\sin{v}| du\wedge dv.
$$