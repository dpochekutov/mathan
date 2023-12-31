+++
title = "РФ22-01Б: Практика N11"
template = "page.html"
date = 2023-11-10
[taxonomies]
tags = ["rf22-01b", "MA3"]
[extra]
summary = "Замена переменных в тройном интеграле"
mathjax = "tex-mml"
+++

<!-- more -->

## Замена переменных в тройном интеграле

**Д4087** Переходя к сферическим координатам, вычислить интеграл
$$
    I = \iiint_V \sqrt{x^2+y^2+z^2} dxdydz,
$$
где область $V$ ограничена поверхностью $x^2+y^2+z^2=z$.

Рассмотрим <a href="https://ru.wikipedia.org/wiki/%D0%A1%D1%84%D0%B5%D1%80%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0_%D0%BA%D0%BE%D0%BE%D1%80%D0%B4%D0%B8%D0%BD%D0%B0%D1%82">сферическую замену</a>
$$
    x=\rho \cos{\varphi} \sin{\psi}, y= \rho \sin{\varphi} \sin{\psi}, z=\rho \cos{\psi},
$$
где $\psi$ является наименьшим углом (угол $\theta$ по ссылке) между положительным направлением оси $z$ и радиус-вектором точки
$(x,y,z)$, а $\varphi$ есть наименьший угол между положительным направлением оси $x$ и 
радиус-вектором точки $(x,y,0)$. Определитель её матрицы Якоби равен
$$
    J=\rho^2 \sin{\psi}.
$$

Область $V$ представляет собой шар с центром в точке $(0,0,\frac{1}{2})$ радиуса $\frac{1}{2}$. В сферических
координатах она задаётся условиями $0\leq \rho \leq \cos{\psi}$, $0\leq \psi \leq \frac{\pi}{2}$ и $0\leq \varphi \leq 2\pi$. 

После замены по теореме Фубини получаем
$$
    I = \left(\int_0^{2\pi} d\varphi\right)\left(\int_0^{\frac{\pi}{2}} \sin{\psi} \ d\psi \int_0^{\cos{\psi}} \rho^3 d\rho\right)
    = 2\pi \int_0^{\frac{\pi}{2}} \frac{\cos^4{\psi}\sin{\psi}}{4}d\psi = \frac{\pi}{10}.
$$