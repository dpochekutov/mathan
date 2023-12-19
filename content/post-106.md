+++
title = "БФ23-05Б: Практика N27-28"
template = "page.html"
date = 2023-12-18
[taxonomies]
tags = ["bf23-05b", "MA1"]
[extra]
summary = "Раскрытие неопределенностей"
mathjax = "tex-mml"
+++

<!-- more -->

## Раскрытие неопределенностей

### Правило Лопиталя

**Д1342** Определить значение выражения
$$
    \lim_{x\to +0} x^x.
$$

Заметим, что
$$
      \lim_{x\to +0} x^x =  \lim_{x\to +0} e^{x\ln{x}}. 
$$
В силу непрерывности функции $e^x$ достаточно найти предел
$$
    \lim_{x\to +0} x\ln{x}. 
$$
Для того, чтобы воспользоваться правилом Лопиталя, перепишем его в виде
$$
    \lim_{x\to +0} x\ln{x}=\lim_{x\to +0} \frac{\ln{x}}{\frac{1}{x}}.
$$
Тогда 
$$
  \lim_{x\to +0} \frac{\ln{x}}{\frac{1}{x}}=\lim_{x\to +0} \frac{\frac{1}{x}}{-\frac{1}{x^2}}
  =-\lim_{x\to +0} x=0.
$$
Следовательно,
Заметим, что
$$
      \lim_{x\to +0} x^x =  e^0=1. 
$$

### Раскрытие неопределенностей с помощью формулы Тейлора

**Д1400** Используя локальное разложение в окрестности нуля
$$
    (1+x)^{\alpha}=1+\alpha x + \frac{\alpha(\alpha-1)}{2!}x^2+\ldots+\frac{\alpha(\alpha-1)\ldots(\alpha-n+1)}{n!}x^n+o(x^n),
$$
вычислить предел
$$
    L=\lim_{x\to +\infty} x^{\frac{3}{2}}\left(
        \sqrt{x+1}+\sqrt{x-1}-2\sqrt{x}
    \right).
$$
Запишем
$$
    L=\lim_{x\to +\infty} x^{2}\left(
        \sqrt{1+\frac{1}{x}}+\sqrt{1-\frac{1}{x}}-2
    \right)=
$$
$$
    =\lim_{x\to +\infty} x^{2}\left[
        1+\frac{1}{2x}-\frac{1}{8x^2}+o\left(\frac{1}{x^2}\right)+
        1-\frac{1}{2x}-\frac{1}{8x^2}+o\left(\frac{1}{x^2}\right)-2
    \right]=
$$
$$
    =\lim_{x\to +\infty} \frac{
        -\frac{1}{4x^2}+o\left(\frac{1}{x^2}\right)
    }{\frac{1}{x^2}}
   =\lim_{x\to +\infty} \left[
    -\frac{1}{4}+\frac{o\left(\frac{1}{x^2}\right)
    }{\frac{1}{x^2}}
    \right]    
    =-\frac{1}{4}.
$$

### Домашняя работа

1. Д1327-30, Д1332-33, Д1338-39, Д1348, Д1350.
2. Д1401-1406а.

