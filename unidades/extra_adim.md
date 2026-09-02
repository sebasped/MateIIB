---
title: Extra - adimensionalización
---

# Ejemplo de adimensionalización de un modelo

Un ejemplo clásico es el del péndulo simple. El modelo es:
$$
mL\frac{d^2\theta}{dt^2}=-mg\sin\theta.
$$
donde:
- $m$ es la masa del péndulo.
- $L$ es su longitud.
- $g$ es la aceleración de la gravedad.
- $\theta(t)$ es el ángulo que forma el péndulo con la vertical.
- $t$ es el tiempo.

Tanto $m$, $L$, $g$ y $t$ tienen unidades. El ángulo $\theta(t)$ es adimensional, asi que por ese no nos tenemos que preocupar.  
La idea entonces es convertir el modelo original en uno equivalente sin unidades (adimensionalizado).  
**¿Por qué está bueno adimensionalizar?** Porque hace que nuestros análisis sean independientes de las unidades de medición.

Veamos. De regalo podemos hacer desaparecer $m$ cancelando. Perfecto una cosa menos con unidades.  Simplificando la masa $m$, obtenemos:
$$
\frac{d^2\theta}{dt^2}+\frac{g}{L}\sin\theta=0.
$$

## Elección de una escala característica de tiempo
Una técnica típica para adimensionalizar es reescalar el tiempo. Lo que en Física se conoce como encontrar el tiempo característico del sistema.
Como el único término que nos quedó con unidades es $g/L$, que tiene unidades de $1/t^2$, parece natural probar la siguiente escala de tiempo:
$$
t_c=\sqrt{\frac{L}{g}}.
$$
Definimos entonces el tiempo adimensional:
$$
\tau=\frac{t}{t_c} =t\sqrt{\frac{g}{L}}.
$$
Y veamos si nos sirve.

## Transformación al modelo adimensionalizado
Como $\tau = t\sqrt{\frac{g}{L}}$, ahora $\theta$ puede considerarse como una función de $\tau$: $\theta=\theta(\tau)$ (esto es simplemente porque $\tau \sqrt{\frac{L}{g}}= t$).

Como $\theta$ depende de $\tau$, y $\tau$ depende de $t$, por regla de la cadena tenemos que:
$$
\frac{d\theta}{dt} = \frac{d\theta}{d\tau} \frac{d\tau}{dt} = \frac{d\theta}{d\tau} \sqrt{\frac{g}{L}}
$$
Derivando nuevamente respecto de $t$ obtenemos:
$$
\frac{d^2\theta}{dt^2} =  \frac{d^2\theta}{d\tau^2} \frac{g}{L}
$$

Sustituyendo ahora en el modelo original, obtenemos:

$$
\frac{g}{L} \frac{d^2\theta}{d\tau^2} + \frac{g}{L}\sin\theta=0.
$$

Y finalmente cancelando $g/L$:

$$
\boxed{
\frac{d^2\theta}{d\tau^2} + \sin\theta=0
}
$$

Obtenemos el modelo equivalente adimensionalizado. Las unidades quedaron escondidas en la nueva escala de tiempo $\tau$ (que tampoco tiene unidades).  
**¿Por qué se le dice tiempo característico a $t_c=\sqrt{L/g}$?** Porque cuando $t=t_c$ equivale $\tau=1$. Es decir avanzar 1 unidad de tiempo en la nueva escala, es equivalente a avanzar $t_c$ en la escala de tiempo original.

## Para leer más sobre esto
- [Cap. 7 de este sitio: análisis dimensional](https://sites.google.com/unal.edu.co/hacia-la-mecanica-de-fluidos/cap%C3%ADtulos/cap%C3%ADtulo-7).
- [Cap. 10 de este libro: análisis dimensional y similitud](https://ingenieria.uner.edu.ar/referencia/bibliografia/jdipaolo/mecanica_de_los_fluidos-2edicion.pdf).
- [Clase 10 de esta materia](https://materias.df.uba.ar/edlm1a2024cv/files/2024/02/E1_clase_10.pdf).

