---
title: 01 - Aproximación de Funciones
---

# 01a - Polinomio de Taylor

A pesar de que el polinomio de Taylor pueda ser un tema más bien teórico, hay varias cosas que podemos hacer en la compu que son útiles, a saber:
- Graficar la función y sus polinomios de Taylor, todo junto, y observar que:
    - Cerca del $x_0$ la aproximación es mejor.
    - Al aumentar el orden del polinomio la aproximación es mejor.
- Estimar numéricamente los errores que se comenten al usar el polinomio de Taylor en vez de la función.
- Acotar en papel el resto de Taylor, y utilizarlo para encontrar **a priori** un órden que asegure que el error cometido sea menor a un umbral de interés.

:::{dropdown} Para tener a mano (hacer clic para expandir)
Polinomio de Taylor para $f$ alrededor de $x_0$:
- Orden 1: $$T_1(x) = f(x_0) + f'(x_0)(x-x_0)$$
- Orden 2: $$T_2(x) = T_1(x) + \frac{f''(x_0)}{2!}(x-x_0)^2$$
- Orden 3: $$T_3(x) = T_2(x) + \frac{f'''(x_0)}{3!}(x-x_0)^3$$
Etc.

Resto de orden $n$: $$ R_n(x) = f(x) - T_n(x) = \frac{f^{(n+1)}(\theta)}{(n+1)!}(x-x_0)^{n+1} $$ con $\theta$ entre $x$ y $x_0$.

Error (este es el que se acota para estimarlo): $$|R_n(x)| = |f(x) - T_n(x)| = \left|\frac{f^{(n+1)}(\theta)}{(n+1)!}(x-x_0)^{n+1} \right| $$ con $\theta$ entre $x$ y $x_0$.
:::

:::{note} NB Python para rellenar: polinomio de Taylor
- [Para descargar](/code/01_aprox_funcs/01a_polinomio_Taylor_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/01_aprox_funcs/01a_polinomio_Taylor_incompleta.ipynb)
:::



---
# 01b - Interpolación polinomial

Explicación introductoria

:::{dropdown} Para tener a mano (hacer clic para expandir)
BLA
:::

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar](/code/01_aprox_funcs/01b_interpolacion_polinomial_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/01_aprox_funcs/01b_interpolacion_polinomial_incompleta.ipynb)
:::





# 01c - Interpolación de Hermite y Splines