# Fórmulas para oscilaciones amortiguadas

La ecuación diferencial de las oscilaciones amortiguadas está dada por

$$
m\frac{d^2 x}{dt^2} + b\frac{dx}{dt} + kx = 0 \hspace{3pt} \Rightarrow \hspace{3pt} \frac{d^2 x}{dt^2} + \frac{b}{m}\frac{dx}{dt} + \frac{k}{m}x = 0
$$

Así entonces, se pueden definir las siguientes variables

$$
\alpha = \frac{b}{2m},\, \omega_0 = \sqrt{\frac{k}{m}},\, \lambda = -\alpha \pm \sqrt{\alpha^2 - \omega_0^2} = -\frac{b}{2m} \pm \sqrt{\frac{b^2}{4m^2}-\frac{k}{m}}
$$

Para la solución de la ecuación diferencial existen 3 casos generales que den solución a la ecuación diferencial.

## Caso 1: Sobre-amortiguamiento

La condición para que un sistema sea sobre-amortiguado es

$$
\alpha^2 - \omega_0^2 > 0 \hspace{3pt} \Rightarrow \hspace{3pt} b > 2\sqrt{km}
$$

La solución de la ecuación diferencial está dada por

$$
x(t) = C_1e^{\lambda_1 t} + C_2e^{\lambda_2 t} \hspace{3pt} \Rightarrow \hspace{3pt} x(t) = e^{-\alpha t} \left[ C_1 e^{t\sqrt{\alpha^2 - \omega_0^2}} + C_2 e^{-t\sqrt{\alpha^2 - \omega_0^2}} \right]
$$

A partir de las condiciones iniciales, $x(0) = x_0$ y $v(0) = v_0$, se pueden calcular el valor de las constantes $C_1$ y $C_2$.

Retomando la función de posición ($x(t)$), es posible calcular la velocidad ($v(t) = dx/dt$)

$$
v(t) = \lambda_1 C_1 e^{\lambda_1 t} + \lambda_2 C_2 e^{\lambda_2 t}
$$

Entonces

$$
x(0) = C_1 + C_2 = x_0
$$

$$
v(0) = C_1 \lambda_1 + C_2 \lambda_2 = v_0
$$

Al resolver el sistema de ecuaciones, entonces

$$
C_1 = x_0 - \frac{v_0 - x_0\lambda_1}{\lambda_2 - \lambda_1};\: C_2 = \frac{v_0 - x_0\lambda_1}{\lambda_2 - \lambda_1}
$$

Además,la aceleración está dada por

$$
a(t) = \lambda_1^2 C_1 e^{\lambda_1 t} + \lambda_2^2 C_1 e^{\lambda_2 t}
$$

## Caso 2: Críticamente-amortiguado

La condición para que un sistema sea críticamente amortiguado es

$$
\alpha^2 - \omega_0^2 = 0 \hspace{3pt} \Rightarrow \hspace{3pt} b = 2\sqrt{km}
$$

Entonces, al ser iguales $\alpha$ y $\omega_0$, $\lambda = -\alpha \pm \sqrt{\alpha^2 - \omega_0^2} = -\alpha$, entonces la solución a la ecuación diferencial está dada por

$$
x(t) = (C_1 + C_2 t)e^{\lambda t} \hspace{3pt} \Rightarrow \hspace{3pt} x(t) = (C_1 + C_2 t) e^{-\alpha t}
$$

Para buscar las constantes se utilizarán las condiciones iniciales como en los sobre-amortiguados, pero antes, se necesita calcular la velocidad

$$
v(t) = -\alpha C_1 e^{-\alpha t} + C_2e^{-\alpha t} - C_2\, \alpha t \,e^{-\alpha t}
$$

Ahora sí, entonces

$$
x(0) = C_1 = x_0
$$

$$
v(0) = -C_1\alpha + C_2 = v_0
$$

Los valores de las constantes están dadas por

$$
C_1 = x_0;\: C_2 = v_0 + \alpha x_0
$$

La aceleración está dada por

$$
a(t) = \alpha e^{-\alpha t} (C_1 \alpha - 2C_2 + C_2\alpha t)
$$

## Caso 3: Sub-amortiguado

La condición que se debe cumplir para que sea sub-amortiguado es que

$$
\alpha^2 - \omega_0^2 < 0 \hspace{3pt} \Rightarrow \hspace{3pt} b < 2\sqrt{km}
$$

La solución a la ecuación diferencial está dada por

$$
x(t) = C_1 e^{-(b/2m)t} \cos{(\omega t + C_2)}
$$

Donde $\omega = \sqrt{\omega_0^2 - \alpha^2} = \sqrt{\frac{k}{m} - \left( \frac{b}{2m} \right)^2}$. La velocidad dada por

$$
v(t) = -\frac{C_1 b}{2m} e^{-(b/2m)t} \cos{(\omega t + C_2)} - C_1 \omega e^{-(b/2m)t} \sin{(\omega t + C_2)}
$$

Entonces, el sistema de ecuaciones que se obtienen a partir de las condiciones iniciales es el siguiente

$$
x(0) = C_1 \cos{C_2} = x_0
$$

$$
v(0) = -\frac{C_1 b}{2m} \cos{C_2} - C_1 \omega \sin{C_2} = v_0
$$

La solución entonces está dada por

$$
C_2 = \arctan{\left[ -\left( \frac{v_0}{x_0 \omega} + \alpha \right)\right]} =\arctan{\left[ -\left( \frac{v_0}{x_0 \omega} + \frac{b}{2m} \right)\right]}
$$

$$
C_1 = \sqrt{\frac{x_0^2 + (\frac{v_0}{\omega})^2}{ \left( \frac{\alpha}{\omega} \cos{C_2} \right)^2 + \frac{\alpha}{\omega} \sin{(2 C_2)} + 1}} = \sqrt{\frac{x_0^2 + (\frac{v_0}{\omega})^2}{ \left( \frac{b}{2m\omega} \cos{C_2} \right)^2 + \frac{b}{2m\omega} \sin{(2 C_2)} + 1}}
$$

Note que para la constante $C_2$, cuando $x_0 = 0$, entonces $C_2 = n\frac{\pi}{2}$, donde $n \in \mathbb{Z} \backslash \{0\}$, y si se hubiera querido, con reemplazar $C_1$ en la segunda ecuación, no obstante, se presentaba un gran problema cuando $x_0 = 0$, por lo que se buscó la manera en la que se exprese el valor de la constante $C_1$ para así evitar el problema antes mencionado, se aprecia de que con la expresión obtenida, se soluciona precisamente ese problema. A pesar de que en la ecuación de $C_1$ aparezca $C_2$, se vió más cómodo expresarlo así, pero si se desea, también se puede reemplazar.

La aceleración está dada por

$$
a(t) = 2C_2 \alpha \omega e^{-\alpha t} \sin{(\omega t + C_2)} + (\alpha^2 - \omega^2)e^{-\alpha t} \cos{(\omega t + C_2)}
$$
