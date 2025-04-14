## Principio general de modelamiento

El **principio general de modelamiento** es una regla fundamental utilizada para describir sistemas físicos. Aplica tanto para **masa** como para **energía** (o cualquier otra cantidad conservativa como carga, cantidad de movimiento, etc.)
- **Tasa de acumulación**: Cambio en el tiempo de la cantidad dentro del sistema (puede ser masa, energía, etc.)
- **Flujo de entrada**: Lo que entra al sistema
- **Flujo de salida**: Lo que sale del sistema

Este principio se usa para modelar:

- Sistemas térmicos (balance de energía)
- Dinámica de fluidos (balance de masa)
- Circuitos eléctricos (balance de carga o energía)
- Sistemas mecánicos (balance de momento o cantidad de movimiento)
## Sistemas Mecanicos
# Resorte

El resorte es un elemento mecánico fundamental en sistemas físicos. Se utiliza para modelar fuerzas restauradoras que dependen del desplazamiento.

# Modelo de resorte lineal (Ley de Hooke)

\[
F = k \cdot x = k(x_1 - x_2)
\]

Donde:
- `F` es la fuerza ejercida por el resorte,
- `k` es la constante del resorte (rigidez),
- `x` es el desplazamiento desde la posición de equilibrio,
- `x₁`, `x₂` son las posiciones de los extremos del resorte
Se asumen **resortes lineales**, es decir, la **fuerza externa aplicada y el desplazamiento están relacionados por una constante de proporcionalidad** (`k`)

La gráfica muestra la relación fuerza vs. desplazamiento para diferentes tipos de resortes:

- **Resorte lineal**: relación lineal (recta)
- **Resorte duro**: la rigidez aumenta con el desplazamiento
- **Resorte suave**: la rigidez disminuye con el desplazamiento
# Amortiguador

Un **amortiguador** es un elemento mecánico que modela una fuerza proporcional a la **velocidad relativa** entre dos cuerpos. Este comportamiento es típico en sistemas donde se presenta fricción viscosa
# Modelo de fricción viscosa (Amortiguador lineal)

\[
F = b \cdot \dot{x} = b(\dot{x}_1 - \dot{x}_2)
\]

Donde:
- `F` es la fuerza generada por el amortiguador.
- `b` es la **constante de fricción viscosa**.
- \(\dot{x}_1\) y \(\dot{x}_2\) son las velocidades de los extremos del amortiguador
# Comportamiento del amortiguador

- Es un **comportamiento lineal**.
- La fuerza disipa energía cinética.
- Se utiliza comúnmente para representar la **fricción entre una masa y una superficie**, o en sistemas de suspensión
## Tipos de fricción
## Fricción en seco

### Diagrama de fuerzas

En la imagen se muestra un bloque sobre una superficie plana, donde se ilustran las fuerzas involucradas en la fricción en seco:
- **mg**: peso del objeto (fuerza gravitacional)
- **N**: fuerza normal (perpendicular a la superficie)
- **F**: fuerza de fricción (se opone al movimiento)
- **Fuerza de tracción**: fuerza que intenta mover el objeto

También se muestra una gráfica que relaciona la fuerza de fricción con la velocidad:

- En reposo, la fricción es **estática**, que aumenta hasta un valor máximo.
- Una vez iniciado el movimiento, la fricción se convierte en **deslizante** (o cinética), que es menor y casi constante

Esto refleja que:
- La **fricción estática** impide que el cuerpo se mueva hasta que se supera su límite
- Al comenzar el movimiento, la **fricción deslizante** toma el control
### Fricción en seco
- Es aquella que se presenta cuando un cuerpo con una superficie no lubricada se desliza sobre otra superficie no lubricada.
  - **Fricción estática**
  - **Fricción por deslizamiento**
  - **Fricción por rodamiento**
  - 
## Fricción por rodamiento

La **fricción por rodamiento** ocurre cuando un cuerpo (como una rueda o cilindro) rueda sobre una superficie en lugar de deslizarse. Este tipo de fricción es mucho menor que la fricción por deslizamiento

- **mg**: peso del cuerpo (fuerza hacia abajo debido a la gravedad).
- **N**: fuerza normal ejercida por la superficie.
- **P**: fuerza aplicada para mover el cuerpo.
- **T₁ y T₂**: fuerzas de contacto en los extremos del área de contacto.
- **r**: radio del cuerpo que rueda.
- **h**: altura a la que se aplica la fuerza **P**.
