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

:::{dropdown} Para tener a mano (clic para expandir)
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

Tenemos datos de un experimento cuyo modelo teórico $f$ no conocemos o resulta muy complicado de utilizar. Buscamos un modelo teórico polinomial $P_n$ que aproxime al modelo $f$, pues los polinomios son fáciles de manejar. Realizamos esta aproximación obligando a $P_n$ a pasar por los datos que tenemos (es decir a interpolar los datos).

:::{dropdown} Para tener a mano (clic para expandir)
Modelo teórico $f$ desconocido o complicado.  
Sabemos algunos datos: $f(x_0)=y_0, f(x_1)=y_1,\dots,f(x_n)=y_n$.  

Polinomio interpolador $P_n$ para los $n+1$ datos $(x_0, y_0), (x_1, y_1),\dots,(x_n, y_n)$:
- Grado de $P_n$ menor o igual a $n$.
- En los datos le pega justo: $P_n(x_0)=y_0, P_n(x_1)=y_1,\dots, P_n(x_n)=y_n$.
- Para un $x$ "cualquiera", esperamos que $P(x)$ aproxime "bien" a $f(x)$.
  - $x$ "cualquiera" es porque $x$ debe estar en el rango $[a,b]$ de los $x_0, x_1,\dots, x_n$. Justamente por eso le decimos `inter`polar (si estuviese fuera de rango sería `extra`polar).

Por supuesto, no hay aproximación sin estimación del error.  
Si $f:[a,b]\to\mathbb{R}$, y tanto $x$ como los $x_i$ están en $[a,b]$, entonces:

$$
\left|f(x)-P_n(x)\right|
\leq
\frac{\displaystyle\max_{\theta\in[a,b]}
\left|f^{(n+1)}(\theta)\right|}
{(n+1)!}
(b-a)^{n+1}
\qquad\text{($x_i$ cualesquiera)}
$$

$$
\left|f(x)-P_n(x)\right|
\leq
\frac{\displaystyle\max_{\theta\in[a,b]}
\left|f^{(n+1)}(\theta)\right|}
{(n+1)!}
\left(\frac{b-a}{2}\right)^{n+1}
\qquad\text{($x_i$ equiespaciados)}
$$

$$
\left|f(x)-P_n(x)\right|
\leq
\frac{\displaystyle\max_{\theta\in[a,b]}
\left|f^{(n+1)}(\theta)\right|}
{(n+1)!}
\left(\frac{b-a}{2}\right)^{n+1}
\frac{1}{2^n}
\qquad\text{($x_i$ ceros de \(T_{n+1}\) de Tchebyshev)}
$$
:::

:::{note} NB Python para rellenar: interpolación polinomial
- [Para descargar](/code/01_aprox_funcs/01b_interpolacion_polinomial_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/01_aprox_funcs/01b_interpolacion_polinomial_incompleta.ipynb)
:::




---
# 01c - Interpolación de Hermite y Splines

- **Hermite:** misma idea que interpolación polinomial, con la diferencia que ahora interpolamos datos de la función y de sus derivadas.  
(Ver ejemplo en la NB).
- **Splines:** misma idea que interpolación polinomial, con la diferencia que "pegamos" muchas interpolaciones polinomiales, cada una realizada en un intervalo "pequeño" y con un polinomio de grado bajo (típicamente grado 1, 2 o 3).
<!-- 

:::{dropdown} Para tener a mano (clic para expandir)
**EN CONSTRUCCIÓN**.
::: -->

:::{note} NB Python para rellenar: interpolación Hermite y Splines
- [Para descargar](/code/01_aprox_funcs/01c_interpolacion_hermite_y_splines_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/01_aprox_funcs/01c_interpolacion_hermite_y_splines_incompleta.ipynb)

:::
