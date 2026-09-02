---
title: 03 - Ecuaciones Diferenciales
---

<!-- **FALTA** intro -->

# Una sola ecuación

## 03a - Métodos de Euler (explícito), Taylor y Runge-Kutta

:::{dropdown} Para tener a mano (clic para expandir)
$$
x'(t)=f(t,x(t)), \qquad x(t_0)=x_0.
$$

Error global de Euler explícito. Si
$$
\max_{t\in[t_0,t_F]}|\ddot{x}(t)|\leq C_{max}
$$

$$
\max_{\substack{t\in[t_0,t_F]\\x\in[a,b]}} |f_x(t,x)|\leq L.
$$

Entonces una cota para el error de Euler explícito en el tiempo final es:
$$
|E_N|=|x(t_F)-x_N| \leq \frac{e^{L(t_F-t_0)}-1}{L}\,C_{max}h^2.
$$
La idea es encontrar $h$ para que la cota del error sea menor a uno deseado (el resto de las cosas: $t_0, t_F, L, C_{max}$ son conocidas o calculables).
:::

:::{note} NB Python para rellenar
- [Para descargar](/code/03_edos/03a_euler_taylor_rungekutta_incompleta.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/03_edos/03a_euler_taylor_rungekutta_incompleta.ipynb)
:::



---
## 03b - Método de Euler _Implícito_

<!-- **FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/03_edos/03b_euler_implicito_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/03_edos/03b_euler_implicito_completa.ipynb)
:::




---
## 03c - `solve_ivp` para ecuaciones
`solve_ivp` es la librería nativa de `scipy` para resolver numéricamente ecuaciones diferenciales.
<!-- 
**FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/03_edos/03c_solve_ivp_para_ecuaciones_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/03_edos/03c_solve_ivp_para_ecuaciones_completa.ipynb)
:::


# Sistema de ecuaciones

# 03d - Métodos de Euler (explícito) y Runge-Kutta para sistemas

<!-- **FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/03_edos/03d_euler_rungeKutta_para_sistemas_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/03d_euler_rungeKutta_para_sistemas_completa.ipynb)
:::


---
# 03e - `solve_ivp` para sistemas

<!-- **FALTA**

:::{dropdown} Para tener a mano (clic para expandir)
**FALTA**
::: -->

:::{note} NB Python para mirar: **ya completa**
- [Para descargar](/code/03_edos/03e_solve_ivp_para_sistemas_completa.ipynb).
  - **Si se abre un archivo con texto, `Ctrl+s` lo guarda y listo.**
- [Abrir en Colab](https://colab.research.google.com/github/sebasped/MateIIB/blob/main/code/03_edos/03e_solve_ivp_para_sistemas_completa.ipynb)
:::