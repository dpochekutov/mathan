+++
title = "ИМ23-04М: Лекция N5"
template = "page.html"
date = 2023-10-30
[taxonomies]
tags = ["im23-04m", "OAG"]
[extra]
summary = "Теория исключения (продолжение)"
mathjax = "tex-mml"
+++

## Теория исключения (продолжение)

### Пример вычисления базиса Грёбнера в Singular

```
ring R = 0,(t,u,x,y,z),lp;
poly f1 = x-t-u;
poly f2 = y-t^2-2*t*u;
poly f3 = z-t^3-3*t^2*u;
ideal I = f1,f2,f3;
ideal J = groebner(I);
J;
```

[Конспект пятой лекции (неполный)](/2023_10_23_LectureV.pdf)