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
# 02b - Métodos de Newton-Raphson y otros (Secante, Regula-Falsi)

:::{dropdown} Para tener a mano (clic para expandir)
Newton-Raphson:
- Si converge, es mucho más rápido que Bisección (cuadrático versus lineal esencialmente).
- **No** siempre converge. En general depende del $x_0$ inicial, aunque podría no converger para cualquier $x_0$ que se elija.
- Existen casos de convergencia para cualquier $x_0$ que se elija, por ejemplo:
```{figure} ../images/conv_global_newtonRaphson.png
:width: 400px
:align: center
:name: fig-conv_global_newtonRaphson
```
- Existen casos de convergencia local, es decir hay convergencia si $x_0$ pertenece a un intervalo determinado. Por ejemplo si
  - Si $f$ tiene dos derivadas continuas en $(a,b)$, 
  - $f(r)=0$, 
  - $f'(r)\neq 0$,
  - $r\in(a,b)$.  
  Entonces existe $[c,d]\subseteq[a,b]$ con $r\in(c,d)$ tal que si $x_0\in[c,d]$ entonces el método de Newton-Raphson converge a $r$.

Para ver más se puede consultar el cap. 4 de {cite}`duran_lassalle_rossi`.
:::

:::{note} NB Python para rellenar
- [Para descargar](/code/02_ecs_no_lin/02b_newtonRaphson_otros_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02b_newtonRaphson_otros_incompleta.ipynb)
:::




---
# 02c - Métodos de Punto Fijo

:::{dropdown} Para tener a mano (clic para expandir)
Sea $g:[a,b]\to\mathbb{R}$ continua tal que:
1. $g([a,b])\subseteq[a,b]$.
1. $g$ es contractiva en $[a,b]$ con constante $0\leq L<1$.

Entonces el método de punto fijo $x_{n+1}=g(x_n)$ converge al **único punto fijo** $r\in[a,b]$ de $g$.

Para garantizar que $g$ sea contractiva en $[a,b]$, alcanza con encontrar $0\leq L<1$ tal que
$$
\max_{\theta\in[a,b]}|g'(\theta)|\leq L.
$$

Cotas del error en el método de punto fijo:
- $|x_n-r|\leq L^n|x_0-r|$
- $ |x_n-r|\leq\frac{L^n}{1-L}|x_1-x_0|$
- $|x_n-r|\leq\frac{L}{1-L}|x_n-x_{n-1}|$

:::

:::{note} NB Python para rellenar
- [Para descargar](/code/02_ecs_no_lin/02c_punto_fijo_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02c_punto_fijo_incompleta.ipynb)
:::


---
# 02d - Métodos para Sistemas de Ecuaciones: Punto Fijo y Newton-Raphson

<!-- **FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/02_ecs_no_lin/02d_punto_fijo_y_newtonRaphson_para_sistemas_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02d_punto_fijo_y_newtonRaphson_para_sistemas_completa.ipynb)
:::


---
# 02e - Métodos de Punto Fijo para Sistemas de Ecuaciones **Lineales**: Jacobi y Gauss-Seidel

<!-- **FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/02_ecs_no_lin/02e_Jacobi_GaussSeidel_para_sistemas_lineales_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/02_ecs_no_lin/02e_Jacobi_GaussSeidel_para_sistemas_lineales_completa.ipynb)
:::