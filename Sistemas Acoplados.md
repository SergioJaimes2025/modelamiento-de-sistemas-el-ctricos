# Sistemas Acoplados
# Ejemplos de Modelado Dinámico de Sistemas Físicos

##  Ejemplo 1: Control de temperatura de un horno

Modelar el comportamiento térmico de un horno eléctrico regulado por un termostato.

### Supuestos:
- La temperatura interna del horno es `T(t)`.
- La entrada de calor está dada por la señal de control `u(t)`.
- Existe pérdida de calor hacia el ambiente a temperatura `T_amb`.

### Modelo:

Por balance de energía:

```
C * dT(t)/dt = -k * (T(t) - T_amb) + u(t)
```

### Variables:
- `C`: Capacidad térmica del horno.
- `k`: Coeficiente de pérdida térmica.
- `u(t)`: Potencia de calefacción suministrada.
- `T(t)`: Temperatura interna del horno.
- `T_amb`: Temperatura ambiente (constante).

### Interpretación:
- El modelo describe cómo varía la temperatura interna en función del calor suministrado y las pérdidas.
- Se puede usar para diseñar un controlador (ej. PID) que mantenga la temperatura deseada.

---

## Ejemplo 2: Sistema masa-resorte-amortiguador vertical

Modelar el movimiento vertical de una masa suspendida por un resorte y un amortiguador.

### Descripción:
- Una masa `m` cuelga de un resorte con constante `k` y amortiguador de constante `b`.
- La posición vertical de la masa es `y(t)` (medida hacia abajo desde el equilibrio).
- Se considera el efecto de la gravedad.

### Modelo dinámico (segunda ley de Newton):

```
m * y''(t) + b * y'(t) + k * y(t) = 0
```

Donde:
- `y''(t)`: Aceleración de la masa.
- `y'(t)`: Velocidad de la masa.
- `y(t)`: Desplazamiento desde el equilibrio.

Este sistema se puede resolver numéricamente para simular su comportamiento o diseñar un sistema de control.

---

## Sistemas Acoplados
## Para la masa 1:
u - FR1 - FR2 - FF = m1 * a_m1
- La distancia de elongación del resorte 2 depende del movimiento de ambas masas.
- La velocidad del émbolo del amortiguador del resorte 2 depende del movimiento de ambas masas
u(t) - k1 * x1(t) - k2 * (x1(t) - x2(t)) - b * d/dt[x1(t) - x2(t)] = m1 * d²x1(t)/dt²

### Para la masa 2:
- La distancia de elongación del resorte 2 depende del movimiento de ambas masas.
- La velocidad del émbolo del amortiguador del resorte 2 depende del movimiento de ambas masas

k2 * (x1(t) - x2(t)) + b * d/dt[x1(t) - x2(t)] - k3 * x2(t) = m2 * d²x2(t)/dt²


## Modelo resultante (sistema acoplado completo)

u(t) - k1 * x1(t) - k2 * (x1(t) - x2(t)) - b * d/dt[x1(t) - x2(t)] = m1 * d²x1(t)/dt²

k2 * (x1(t) - x2(t)) + b * d/dt[x1(t) - x2(t)] - k3 * x2(t) = m2 * d²x2(t)/dt²

## Ejemplo

### Para la masa `m1`:
m1 * d²x1(t)/dt² = -k1 * x1(t) - b * dx1(t)/dt + k2 * (x2(t) - x1(t))
### Para la masa `m2`:
m2 * d²x2(t)/dt² = -k2 * (x2(t) - x1(t))
## Variables:
- `m1`, `m2`: masas.
- `k1`, `k2`: constantes de los resortes.
- `b`: constante del amortiguador.
- `x1(t)`, `x2(t)`: posiciones respecto al equilibrio.
- `dx1(t)/dt`, `dx2(t)/dt`: velocidades.
- `d²x1(t)/dt²`, `d²x2(t)/dt²`: aceleraciones.
# Ejemplo 1: Sistema de tanque con entrada y salida de fluido
- Un tanque tiene una entrada de flujo de agua `q_in(t)` y una salida proporcional a la altura del fluido.
- La altura del agua en el tanque es `h(t)`.
- La salida se modela como `q_out(t) = k * h(t)` donde `k` es una constante relacionada con el orificio de salida
A * dh(t)/dt = q_in(t) - k * h(t)
## Variables

- `A`: Área de la sección transversal del tanque.
- `h(t)`: Altura del agua en el tanque.
- `q_in(t)`: Flujo de entrada (puede ser constante o variable).
- `k`: Constante de flujo de salida.
- `q_out(t) = k * h(t)`: Flujo de salida

# Ejemplo 2: Péndulo simple
- Una masa `m` está colgada de un hilo de longitud `L`.
- La posición angular respecto a la vertical es `θ(t)`.
- Solo actúa la gravedad (no hay fricción ni resistencia del aire).
**Ecuación del movimiento (no lineal):**
m * L * d²θ(t)/dt² + m * g * sin(θ(t)) = 0
**Aproximación lineal (para pequeños ángulos):**
d²θ(t)/dt² + (g / L) * θ(t) = 0
## Variables

- `m`: Masa del cuerpo.
- `L`: Longitud del hilo.
- `g`: Aceleración de la gravedad.
- `θ(t)`: Ángulo con respecto a la vertical.
## Ejemplo 3: Sistema Rotacional con Torsión

Modelar un sistema rotacional que involucra un resorte de torsión y un amortiguador.

- `φ`: Ángulo de torsión (análogo al desplazamiento lineal).
- `dφ/dt`: Velocidad angular.
- `d²φ/dt²`: Aceleración angular.
- `J`: Momento de inercia (análogo a la masa).
- `T(t)`: Torque aplicado (análogo a la fuerza).
- `k`: Constante de torsión (análogo al resorte lineal).
- `b`: Coeficiente de fricción rotacional (análogo al amortiguador)

- Torque del resorte:  
  `F_R = k * φ`

- Torque del amortiguador:  
  `F_F = b * dφ/dt`

- Torque total aplicado:  
  `T = J * d²φ/dt²`

## Ejemplo: 
Desarrollar un modelo para describir la posición angular `θ(t)` de un sistema rotacional con eje rígido.

- `θ(t)`: Posición angular del eje (variable dependiente).
- `T(t)`: Torque aplicado (entrada).
- `J`: Momento de inercia del eje.
- `b`: Coeficiente de fricción rotacional.
  
T(t) - b * dθ(t)/dt = J * d²θ(t)/dt²
J * θ''(t) + b * θ'(t) = T(t)

## Ejemplo 1: Péndulo simple
Modelar el comportamiento dinámico de un péndulo simple oscilando sin fricción
- La masa se concentra en una esfera de masa `m`.
- La varilla es rígida, de longitud `L` y sin masa.
- No hay fricción (movimiento conservativo).
- El movimiento es angular, en un plano

### Variables:
- `θ(t)`: Ángulo medido desde la vertical (rad).
- `g`: Aceleración gravitacional.
- `L`: Longitud de la varilla.
- `m`: Masa puntual al final de la varilla.

### Modelo dinámico:

Aplicando las leyes del movimiento rotacional:
J * d²θ(t)/dt² + m * g * L * sin(θ(t)) = 0
Donde el momento de inercia del péndulo respecto al punto de suspensión es:
J = m * L²
Sustituyendo:
m * L² * d²θ(t)/dt² + m * g * L * sin(θ(t)) = 0
Dividiendo todo entre `m * L`:
L * d²θ(t)/dt² + g * sin(θ(t)) = 0
Cuando `θ(t)` es pequeño, `sin(θ) ≈ θ`:
d²θ(t)/dt² + (g / L) * θ(t) = 0

## Ejemplo 2: Sistema masa-resorte horizontal sin fricción

Modelar el movimiento de una masa unida a un resorte horizontal sobre una superficie sin fricción.
### Variables:
- `x(t)`: Desplazamiento de la masa desde su posición de equilibrio.
- `k`: Constante del resorte.
- `m`: Masa del objeto.

### Modelo dinámico:

Por la segunda ley de Newton:
F_resorte = -k * x(t) m * d²x(t)/dt² = -k * x(t)
O escrito como:
d²x(t)/dt² + (k / m) * x(t) = 0
La solución es una función seno/coseno:
x(t) = A * cos(ωt) + B * sin(ωt)
Donde `ω = sqrt(k/m)` es la frecuencia angular del sistema

## Definiciones

### Trabajo:
Es una medida de la realización del esfuerzo (fuerza).

\[ W = F \cdot x \quad \text{[N·m]} \]

Trabajo total realizado:
\[ \int_{0}^{x} kx \, dx = \frac{1}{2} kx^2 \]

• Energía: Capacidad para realizar trabajo.
Tipos de energía:
- Energía potencial
- Energía cinética
