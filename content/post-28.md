+++
title = "РФ22-01Б: Практика N5"
template = "page.html"
date = 2023-09-29
[taxonomies]
tags = ["rf22-01b", "MA3"]
[extra]
summary = "Эйлеровы интегралы (продолжение)"
mathjax = "tex-mml"
+++

<!-- more -->

## Бета-функция

### Разбор домашней работы

**Задача.** (Демидович, 3868) Вычислить интеграл
$$
    \int_0^1 \ln{\Gamma(x)}dx.
$$
**Решение.** Сделаем в интеграле замену $x\mapsto 1-x:$
$$
    \int_0^1 \ln{\Gamma(x)}dx=\int_1^0 \ln{\Gamma(1-x)} (-dx)=\int_0^1 \ln{\Gamma(1-x)}dx.
$$
Тогда от интеграла 
$$
    2\int_0^1 \ln{\Gamma(x)}dx=    \int_0^1 \ln{\Gamma(x)}dx+\int_0^1 \ln{\Gamma(1-x)}dx=\int_0^1 \ln{\Gamma(x)\Gamma(1-x)}dx,
$$
используя формулу дополнения, приходим к интегралу
$$
    2\int_0^1 \ln{\Gamma(x)}dx=\int_0^1 \ln{\frac{\pi}{\sin{\pi x}}} dx
                              =\int_0^1 \ln{\pi} dx - \int_0^1 \ln{\sin{\pi x}} dx. 
$$
Следовательно,
$$
    \int_0^1 \ln{\Gamma(x)}dx=\frac{1}{2}\ln{\pi} - \frac{1}{2}\int_0^1 \ln{\sin{\pi x}} dx. 
$$
Сделаем замену $\pi x \mapsto x$ в интеграле
$$
    \int_0^1 \ln{\sin{\pi x}} dx=\frac{1}{\pi}\int_0^{\pi} \ln{\sin{x}}dx.
$$
Далее, используя интегралы из Д2353,
$$
    \int_0^{\pi} \ln{\sin{x}}dx=\int_0^{\frac{\pi}{2}} \ln{\sin{x}}dx + \int_{\frac{\pi}{2}}^{\pi} \ln{\sin{x}}dx=
$$
$$
    =-\frac{\pi}{2}\ln{2}+\int_0^{\frac{\pi}{2}}\ln\sin(x+\frac{\pi}{2}) d(x+\frac{\pi}{2})=
$$
$$
    =-\frac{\pi}{2}\ln{2}+\int_0^{\frac{\pi}{2}}\ln\cos{x} dx=-\frac{\pi}{2}\ln{2}-\frac{\pi}{2}\ln{2}=-\pi\ln{2}.
$$
В конечном итоге
$$
    \int_0^1 \ln{\Gamma(x)}dx=\frac{1}{2}\ln{\pi}+\frac{1}{2}\ln{2}=\ln{\sqrt{2\pi}}.
$$

### Домашняя работа

1. Д3851, Д3852, Д3853.