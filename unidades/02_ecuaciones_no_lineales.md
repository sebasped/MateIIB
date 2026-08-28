---
title: 02 - Ecuaciones No Lineales
---

<!-- **FALTA** intro -->

# 02a - Método de Bisección

- **Ventajas**: muy simple de aplicar. Sirve para cualquier función continua.
- **Desventajas**: es lento. No se puede generalizar a sistemas de ecuaciones.

:::{dropdown} Para tener a mano (clic para expandir)
Pseudocódigo para Bisección:

1. Tomo $[a,b]$ un intervalo tal que $f(a)f(b)<0$.
1. Calculo $ c = (a+b)/2 $
   - Si $f(c)=0$, entonces **¡listo!**
   - Si $f(a)f(c)>0$, entonces $f(a)$ y $f(c)$ tienen el mismo signo y la raíz está en $[c,b]$.
   - Si $f(a)f(c)<0$, entonces la raíz está en $[a,c]$.
1. Repito el proceso en el nuevo intervalo.

Estimación del error: si el método de bisección converge a una raíz $r$ de $f$, entonces
$$
|x_n-r| \leq \frac{b-a}{2^{n+1}}
$$
Donde
  - $[a,b]=[a_0,b_0]$ y $x_0=(a_0+b_0)/2$,
  - $x_1=(a_1+b_1)/2$,
  - ...
  - $x_n=(a_n+b_n)/2$.

:::

:::{note} NB Python para rellenar
- [Para descargar](/code/02_ecs_no_lin/02a_biseccion_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02a_biseccion_incompleta.ipynb)
:::



---
# 02b -Métodos de Newton-Raphson y otros (Secante, Regula-Falsi)

<!-- **FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar](/code/02_ecs_no_lin/02b_newtonRaphson_otros_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02b_newtonRaphson_otros_incompleta.ipynb)
:::




---
# 02c - Métodos de Punto Fijo
<!-- 
**FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar](/code/02_ecs_no_lin/02c_punto_fijo_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02c_punto_fijo_incompleta.ipynb)
:::


---
# 02d - Métodos para Sistemas de Ecuaciones: Punto Fijo y Newton-Raphson

**FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
:::

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar]().
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/)
:::


---
# 02e - Métodos de Punto Fijo para Sistemas de Ecuaciones **Lineales**: Jacobi y Gauss-Seidel

**FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
:::

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar]().
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/)
:::