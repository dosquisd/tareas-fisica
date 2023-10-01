# Fórmulas para ondas en una cuerda que se mueve senoidalmente

## Función de onda

La función de una onda que se mueve de forma senoidal está dada por

$$
y(x, t) = A \cos{(kx \pm \omega t + \phi_0)}
$$

Donde
$k = \frac{2\pi}{\lambda}$ es el número de onda.
$\omega = \frac{2\pi}{T}$ es la frecuencia angular.
$\lambda$ es la longitud de onda.
$T$ es el periodo.
$\phi_0$ es la fase inicial, pues no necesariamente todas las ondas iniciarán con la misma posición.
Cuando la onda viaja hacia el eje $+x$, la fase toma el valor de $kx - \omega t + \phi_0$. Cuando viaja hacia el eje $-x$, la fase es $kx + \omega t + \phi_0$

A partir de condiciones iniciales es posible calcular la fase inicial $\phi_0$. Suponiendo que una onda que se propaga a lo largo del eje $+x$, en el instante $t = 0$, $x = x_0$ y $v = v_0$, donde $v = \frac{\partial y(x, t)}{\partial t} = \omega A \sin{(kx - \omega t + \phi_0)}$, obteniendo así el siguiente sistema de ecuaciones

$$
y(x_0, t) = A \cos{(kx_0 + \phi_0)} = y_0
$$

$$
v(x_0, t) = A\omega \sin{(kx_0 + \phi_0)} = v_0
$$

Las incognitas del sistema son $y_0$ y $\phi_0$. Resolviendo el sistema, obtenemos que

$$
y_0 = \pm\sqrt{A^2 - \frac{v_0^2}{\omega^2}}
$$

$$
\phi_0 = \arctan{\left( \frac{v_0}{\omega y_0} \right)} - kx_0
$$

Note que para $\phi$, su ecuación es válida para $y_0 \neq 0$. Cuando sea $y = 0$, $\arctan{\left( \frac{v_0}{\omega y_0} \right)} = n\frac{\pi}{2}$, donde $n \in \mathbb{Z} \backslash\{ 0 \}$. A la hora de desarrollar el programa se tomó la parte positiva en $y_0$ y para cuando $y_0 = 0$, $\phi_0 = \frac{\pi}{2} - kx_0$

## Rapidez de propagación

La rapidez en una onda periódica se encuentra dada por

$$
v = \lambda f
$$

Es importante mencionar que la rapidez de propagación es una magnitud constante, por lo que, si la frecuencia $f$ aumenta, la longitud de onda $\lambda$ disminuye para que se mantenga la rapidez constante. En concreto, la rapidez de propagación en una cuerda que se mueve con un movimiento senoidal es

$$
v = \sqrt{\frac{F}{\mu}}
$$

Donde $F$ es la tensión que se le aplica a la cuerda y $\mu$ es la densidad lineal de masa de la misma.

## Potencia

La potencia instantánea de una cuerda que se mueve a lo largo del eje $+x$ con un movimiento senoidal está dada por

$$
P(x, t) = -F \frac{\partial y(x, t)}{\partial x} \frac{\partial y(x, t)}{\partial t} = \sqrt{\mu F} \omega^2 A^2 \sin^2{(kx - \omega t)}
$$

De la potencia instantánea es posible calcular la potencia máxima y la potencia media

$$
P_{máx} = \sqrt{\mu F} \omega^2 A^2
$$

$$
P_{med} = \frac{1}{2}P_{máx} = \frac{1}{2} \sqrt{\mu F} \omega^2 A^2
$$
