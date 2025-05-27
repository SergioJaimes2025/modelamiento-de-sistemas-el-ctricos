## Algebra de bloques
- ¿Qué es un Bloque Funcional en un Diagrama de Bloques?

Los diagramas de bloques son representaciones gráficas que utilizamos para describir sistemas complejos.

Permiten visualizar el flujo de señales o información a través de diferentes componentes o etapas.

Son ampliamente usados en ingeniería, especialmente en control automático y procesamiento de señales.

\[ U = \int_{x_0}^{x} mg \, dx = mgh \]

Donde:
- \( m \): masa
- \( g \): aceleración debida a la gravedad
- \( h \): altura desde una referencia
  
# Energía y Potencia en Sistemas Mecánicos

## Energía Cinética

- La energía cinética es debida a la velocidad.
- Solo los elementos de inercia pueden almacenar energía cinética.

$$
T = \frac{1}{2}mv^2 \quad \text{o} \quad T = \frac{1}{2}J\omega^2
$$

- El cambio en la energía cinética corresponde al trabajo realizado sobre una masa:

$$
\Delta T = \int_{t_1}^{t_2} \vec{F} \cdot \vec{v} \, dt = \frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2
$$

---

## Potencia

- La potencia es la realización de trabajo respecto al tiempo:

$$
P = \frac{dW}{dt}
$$

- Potencia media:

$$
\text{Potencia media} = \frac{\text{Trabajo realizado entre } (t_2 - t_1)}{t_2 - t_1}
$$

---

## Energía Potencial en un Resorte

- Trabajo neto hecho sobre el resorte cuando se comprime o estira:

$$
U = \int F \, dx = \int kx \, dx = \frac{1}{2}kx^2
$$

- Cambio general de energía:

$$
\Delta U = \frac{1}{2}kx_2^2 - \frac{1}{2}kx_1^2
$$

---

## Potencia en un Resorte

- Potencia requerida para estirar o comprimir un resorte:

$$
P = \frac{dW}{dt} = \frac{dF \cdot dx}{dt} = Fx = kx \cdot \dot{x}
$$

- Sabiendo que:

$$
\dot{U} = kx \cdot \dot{x}
$$

Entonces:

$$
P = \dot{U}
$$

---

## Potencia en una Masa

- Potencia para acelerar una masa en línea recta:

$$
P = \frac{dW}{dt} = F \cdot \dot{x} = m\ddot{x} \cdot \dot{x}
$$

- Sabiendo que:

$$
T = \frac{1}{2}m\dot{x}^2
$$

Entonces:

$$
P = \dot{T}
$$

---

## Energía Disipada en un Amortiguador

- Energía disipada corresponde al trabajo realizado por la fuerza de fricción viscosa:

$$
\Delta W = \int F \, dx = \int b\dot{x} \, dx = \int b\dot{x}^2 \, dt
$$

- **No importa el signo de la velocidad**, siempre se disipa energía.

---

## Potencia Disipada en Amortiguador

- Potencia disipada por fricción:

$$
P = F \cdot \dot{x} = b\dot{x} \cdot \dot{x} = b\dot{x}^2
$$
