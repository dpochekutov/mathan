+++
title = "БФ23-05Б: Практика N21-22"
template = "page.html"
date = 2024-04-17
[taxonomies]
tags = ["bf23-05b", "MA2"]
[extra]
summary = "Старшие частные производные. Замена переменных"
mathjax = "tex-mml"
+++

<!-- more -->

## Старшие частные производные

### Аудиторные задачи
1. Д3256, Д3257, Д3258.
2. Д3283, Д3284, Д3285.
3. Д3288, Д3294.

## Замена переменных

[Видеозапись практики](https://www.youtube.com/watch?v=n-jWKEl-lGU)

### Аудиторные задачи

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
    \left( \begin{array}{cc} \frac{\partial u}{\partial x} & \frac{\partial u}{\partial y}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right)
    \left( \begin{array}{c} dr \\\\ d\varphi\end{array}\right) =
    \left( \begin{array}{cc} \frac{\partial u}{\partial r} & \frac{\partial u}{\partial \varphi} \end{array}\right)
    \left( \begin{array}{c} dr \\\\ d\varphi\end{array}\right),
$$
мы приходим к соотношению
$$
    \left( \begin{array}{cc} \frac{\partial u}{\partial x} & \frac{\partial u}{\partial y}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right) =
    \left( \begin{array}{cc} \frac{\partial u}{\partial r} & \frac{\partial u}{\partial \varphi} \end{array}\right).
$$
Из него находим, что 
$$
    \left( \begin{array}{cc} \frac{\partial u}{\partial x}& \frac{\partial u}{\partial y}\end{array}\right) = 
    \left( \begin{array}{cc} \frac{\partial u}{\partial r} & \frac{\partial u}{\partial \varphi}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} & -r \sin{\varphi} \\\\
        \sin{\varphi} &  r \cos{\varphi} \\\\
    \end{array}    
    \right)^{-1} =
    \left( \begin{array}{cc} \frac{\partial u}{\partial r} & \frac{\partial u}{\partial \varphi}\end{array}\right)
    \left(
    \begin{array}{cr}
        \cos{\varphi} &    \sin{\varphi} \\\\
        -\frac{\sin{\varphi}}{r} &  \frac{\cos{\varphi}}{r} \\\\
    \end{array}    
    \right).
$$
Тогда искомое выражение принимает вид
$$
    w = r \cos{\varphi}\left(\sin{\varphi} \frac{\partial u}{\partial r} + \frac{\cos{\varphi}}{r} \frac{\partial u}{\partial \varphi} \right)
      - r \sin{\varphi}  \left(\cos{\varphi} \frac{\partial u}{\partial r} - \frac{\sin{\varphi}}{r} \frac{\partial u}{\partial \varphi} \right) = \frac{\partial u}{\partial \varphi}.
$$

### Домашняя работа
1. Д3259-3265.
2. Д3292, Д3295-97.
3. Д3468, Д3469.
4. Д3481-85.
5. Д3488, Д3501.