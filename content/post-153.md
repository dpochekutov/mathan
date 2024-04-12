+++
title = "РФ23-01Б: Практика N19"
template = "page.html"
date = 2024-04-12
[taxonomies]
tags = ["rf23-01b", "MA2"]
[extra]
summary = "Замена переменных"
mathjax = "tex-mml"
+++

<!-- more -->

## Замена переменных

**Демидович 3481** Преобразовать к полярным координатам $r$ и $\varphi$ выражение
$$
    w = x \frac{\partial u}{\partial y} - y \frac{\partial u}{\partial x}.
$$

Матрица Якоби полярной замены координат $x= r \cos{\varphi}$, $y = r\sin{\varphi}$ имеет вид
$$
    \Pi(r,\varphi) = \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right),
    \\ \det \Pi(r, \varphi) = r.
$$
Тогда дифференциал этого отображения переводит касательный вектор $(dr, d\varphi)$ в вектор
$$
    \left( \begin{array}{c} dx \\\\ dy\end{array}\right) =
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right)
    \left( \begin{array}{c} dr \\\\ d\varphi\end{array}\right) =
    \left( \begin{array}{c} \cos{\varphi} dr - r \sin{\varphi} d\varphi \\\\ 
                            \sin{\varphi} dr + r  \cos{\varphi} d\varphi
            \end{array}\right).
$$
Записав дифференциал функции $u$:
$$
    du(r,\varphi) =
    \left( \begin{array}{cc} u'_x & u'_y\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right)
    \left( \begin{array}{c} dr \\\\ d\varphi\end{array}\right) =
    \left( \begin{array}{cc} u'_r & u'_{\varphi}\end{array}\right)
    \left( \begin{array}{c} dr \\\\ d\varphi\end{array}\right),
$$
мы приходим к соотношению
$$
    \left( \begin{array}{cc} u'_x & u'_y\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right) =
    \left( \begin{array}{cc} u'_r & u'_{\varphi} \end{array}\right).
$$
Из него находим, что 
$$
    \left( \begin{array}{cc} u'_x & u'_y\end{array}\right) = 
    \left( \begin{array}{cc} u'_r & u'_{\varphi}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right)^{-1} =
    \left( \begin{array}{cc} u'_r & u'_{\varphi}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} &    \sin{\varphi} \\\\
        -\frac{\sin{\varphi}}{r} &  \frac{\cos{\varphi}}{r} \\\\
    \end{array}    
    \right).
$$
Тогда
### Аудиторные задачи

1. Д3256-62 (чётные).
2. Д3284-3300 (чётные).

### Домашняя работа

1. Д3289-3301 (нечётные).
2. Д3305-3309.