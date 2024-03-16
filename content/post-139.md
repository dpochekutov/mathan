+++
title = "РФ23-01Б: Практика N10"
template = "page.html"
date = 2024-03-15
[taxonomies]
tags = ["rf23-01b", "MA2"]
[extra]
summary = "Предел функции нескольких переменных"
mathjax = "tex-mml"
+++

<!-- more -->
## Предел функции нескольких переменных

### Определение

Пусть точка $x_0=(x^1_0,\ldots, x^m_0)$ является предельной для области определения $D(f)$
функции $f(x)=f(x_1,\ldots, x_m)$. Тогда для $a\in \mathbb{R}$
$$
    \lim_{x\to x_0} f(x)=a \Leftrightarrow \forall \varepsilon>0 \exists \delta>0 \forall x\in D(f):
    0<\sqrt{\sum_{k=1}^m (x^k-x_0^k)^2}<\delta \Rightarrow |f(x)-a|<\varepsilon;
$$
$$
    \lim_{x\to \infty} f(x)=a \Leftrightarrow \forall \varepsilon>0 \exists \delta>0 \forall x\in D(f):
    \sqrt{\sum_{k=1}^m (x^k-x_0^k)^2}>\frac{1}{\delta} \Rightarrow |f(x)-a|<\varepsilon.
$$



### Аудиторные задачи

**Демидович 3185.** Найти предел 
$$
    \lim_{(x,y)\to(\infty,\infty)} \frac{x+y}{x^2-xy+y^2}.
$$

Напомним, что для всех $x,y\in\mathbb{R}$ справедливо неравенство
$$
    xy\leq \frac{x^2+y^2}{2}\leq x^2+y^2.
$$
Откуда следует неравенство $-(x^2+y^2) \leq -\frac{x^2+y^2}{2}\leq -xy$, влекущее оценку
$$
    0\leq \frac{x^2+y^2}{2} \leq x^2-xy+y^2.
$$
В силу неё и неравенства треугольника при $(x,y)\neq (0,0)$ имеем
$$
    \left| \frac{x+y}{x^2-xy+y^2} \right|\leq 2 \frac{|x+y|}{x^2+y^2} \leq 2 \frac{|x|+|y|}{x^2+y^2}.
$$
Далее, так как $|x|\leq \sqrt{x^2+y^2}$ и $|y| \leq \sqrt{x^2+y^2}$, при $\sqrt{x^2+y^2}>\tfrac{1}{\delta}$ получаем, что
$$
    \left| \frac{x+y}{x^2-xy+y^2} \right|\leq 4\frac{\sqrt{x^2+y^2}}{x^2+y^2}=\frac{4}{\sqrt{x^2+y^2}}<4\delta=\varepsilon,
$$
если к тому же $\delta=\tfrac{\varepsilon}{4}$. Тем самым, мы доказали, что
$$
    \lim_{(x,y)\to(\infty,\infty)} \frac{x+y}{x^2-xy+y^2}=0.
$$

**Демидович 3187** Найти предел
$$
    \lim_{(x,y)\to(0,a)} \frac{\sin{xy}}{x}.
$$

Мы можем переписать искомый предел в виде произведения
$$
    \lim_{(x,y)\to(0,a)} \frac{\sin{xy}}{x}= \left(\lim_{(x,y)\to(0,a)} \frac{\sin{xy}}{xy}\right) \left( \lim_{(x,y)\to(0,a)} y\right), 
$$
если оба предела в правой части равенства существуют.

Заметим, что $\lim_{(x,y)\to(0,a)} y=a$, так как при $(x,y)$, удовлетворяющих $\sqrt{x^2+(y-a)^2}<\varepsilon,$
выполняется
$$
    |y-a|\leq \sqrt{x^2+(y-a)^2}<\varepsilon.
$$

Из первого замечательного предела при любом $\varepsilon >0$ найдется некоторое $\tau(\varepsilon)>0$ такое, что при $0<|t|<\tau(\varepsilon)$
$$
    \left| \frac{\sin t}{t} - 1 \right|<\varepsilon.
$$

Рассмотрим $t=xy$, при любом $\tau>0$, выбрав $\delta=\sqrt{\tau}$, для точки $(x,y)$, удовлетворяющей $\sqrt{x^2+(y-a)^2}<\delta=\sqrt{\tau}$, будем иметь
$$
    |t|=|xy|\leq \sqrt{x^2+(y-a)^2}\cdot \sqrt{x^2+(y-a)^2}<\delta^2=\tau.
$$
Тогда, для любого $\varepsilon>0$ при $0<\sqrt{x^2+(y-a)^2}<\sqrt{\tau(\varepsilon))}$ выполняется
$$
     \left| \frac{\sin xy}{xy} - 1 \right|<\varepsilon.
$$
Мы доказали, что $\lim_{(x,y)\to(0,a)}\frac{\sin xy}{xy}=1$. Поэтому
$$
    \lim_{(x,y)\to(0,a)} \frac{\sin{xy}}{x}= 1\cdot a = a.
$$
### Домашняя работа

1. Д3181, Д3182.
2. Д3189-92.