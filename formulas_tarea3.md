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

## Rapidez de propagación

La rapidez en una onda periódica se encuentra dada por

$$
v = \lambda f
$$

Es importante mencionar que la rapidez de propagación es una magnitud constante, por lo que, si la frecuencia $f$ aumenta, la longitud de onda $\lambda$ disminuye para que se mantenga la rapidez constante. En concreto, la rapidez de propagación en una cuerda que se mueve con un movimiento senoidal es

$$
v = \sqrt{\frac{F}{\mu}}
$$

Donde $F$ es la tensión que se le aplica a la fuerza y $\mu$ es la densidad lineal de masa de la cuerda.

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
