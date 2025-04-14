## Sistemas masa-resorte-amortiguador
1. u - FR - FF = m * a
    Segunda Ley de Newton: la suma de fuerzas es igual a masa por aceleración.

2. FR = k2 * y(t)
    Fuerza del resorte (Ley de Hooke): proporcional al desplazamiento.

3. FF = k1 * dy(t)/dt
    Fuerza del amortiguador (fricción viscosa): proporcional a la velocidad.

4. u(t) - k2 * y(t) - FF = m * a
    Sustituyendo FR en la ecuación de Newton.

5. u(t) - k2 * y(t) - k1 * dy(t)/dt = m * a
    Sustituyendo FF también: ecuación dinámica completa.

6. a = d²y(t)/dt²
    Definición de aceleración como segunda derivada del desplazamiento.

7. u(t) - k2 * y(t) - k1 * dy(t)/dt = m * d²y(t)/dt²
    Forma final de la ecuación diferencial del sistema.
   
## Ejemplo:
Encontrar el modelo matemático que describe el sistema masa-resorte-amortiguador representado por la suspensión de un automóvil.

El sistema está compuesto por:
- Una masa `m` (la carrocería del automóvil).
- Un resorte de rigidez `k₂`.
- Un amortiguador de coeficiente `k₁`.
- Una entrada `u(t)` correspondiente al desplazamiento vertical del terreno o rueda.
- Una salida `y(t)` correspondiente al desplazamiento de la carrocería.

### Supuestos:
- Movimiento unidimensional (vertical)
- Comportamiento lineal de resortes y amortiguadores
- El resorte y amortiguador están conectados entre la masa y el terreno

Fuerza total sobre la masa:
m * d²y(t)/dt² = -k₂ * (y(t) - u(t)) - k₁ * (dy(t)/dt - du(t)/dt)
m * y''(t) + k₁ * (y'(t) - u'(t)) + k₂ * (y(t) - u(t)) = 0

 Donde:
 - `y''(t)` es la aceleración de la masa
 - `y'(t)` es la velocidad de la masa
 - `u(t)` es la entrada del sistema (irregularidad del terreno)
 - `k₁`, `k₂` son constantes positivas
 - Este modelo describe una suspensión pasiva
## Ejemplo 1: Control de temperatura de un horno
Modelar el comportamiento térmico de un horno eléctrico regulado por un termostato

## Supuestos:
- La temperatura interna del horno es `T(t)`.
- La entrada de calor está dada por la señal de control `u(t)`.
- Existe pérdida de calor hacia el ambiente a temperatura `T_amb`.

## Modelo:

Por el principio general de modelamiento (balance de energía):
C * dT(t)/dt = -k * (T(t) - T_amb) + u(t)

## Variables:
- `C`: Capacidad térmica del horno.
- `k`: Coeficiente de pérdida térmica.
- `u(t)`: Potencia de calefacción suministrada.
- `T(t)`: Temperatura interna del horno.
- `T_amb`: Temperatura ambiente (constante).

## Interpretación:
- El modelo describe cómo cambia la temperatura del horno en función de la energía suministrada y las pérdidas.
- Se puede usar para diseñar un controlador (ej. PID) que mantenga la temperatura deseada
## Ejemplo 2: Sistema masa-resorte-amortiguador vertical
Modelar el movimiento vertical de una masa suspendida por un resorte y amortiguador.

## Descripción:
- Una masa `m` cuelga de un resorte con constante `k` y amortiguador de constante `b`.
- La posición vertical de la masa es `y(t)` (medida hacia abajo desde la posición de equilibrio).
- Se considera la gravedad.

### Modelo dinámico (con fuerza neta):
m * d²y(t)/dt² = -k * y(t) - b * dy(t)/dt + m * g
m * y''(t) + b * y'(t) + k * y(t) = 0
