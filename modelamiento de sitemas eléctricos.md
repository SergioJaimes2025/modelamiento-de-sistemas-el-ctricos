# Modelamiento de sistemas eléctricos

Los componentes fundamentales de los circuitos eléctricos, específicamente los sistemas RLC. Estos sistemas están compuestos por resistores, inductores y capacitores, que interactúan de acuerdo con las leyes de Kirchhoff. Veremos cómo modelar y analizar estos circuitos mediante ecuaciones diferenciales.

## 1. Circuitos RLC
El circuito RLC es un sistema compuesto por resistores, inductores y capacitores que se conectan de diversas maneras, permitiendo modelar fenómenos físicos como los osciladores eléctricos. La ley de Kirchhoff nos ayuda a analizar el comportamiento de estos circuitos.

🔑 Definición: El circuito RLC es un tipo de circuito eléctrico que incluye un resistor (R), un inductor (L) y un capacitor (C) conectados en diversas configuraciones para analizar fenómenos de oscilación y energía en sistemas eléctricos.
## 1.1. Ley de Kirchhoff y la Ley de Ohm
Aplicamos la ley de Kirchhoff para los circuitos RLC, lo que nos permite escribir las ecuaciones diferenciales que modelan el comportamiento de la corriente y el voltaje en el sistema.
$$R=\frac{v(T)}{i(T)}$$
Ley de Ohm

## 2. Ecuaciones:
Corriente a través de un condensador:   $$I(T)= C \frac{DV(T)}{D T}$$

Voltaje a través de un inductor:  $V(T)=L\frac{DI(T)}{DT}$
## 3. Ejemplo de Análisis de un Circuito RLC
Veamos cómo se puede analizar un circuito RLC utilizando las ecuaciones derivadas de la ley de Kirchhoff.

Circuito de ejemplo:

Aplicando la ley de Kirchhoff de voltajes (LKT) al circuito que aparece en la figura, obtenemos una ecuación diferencial que describe la relación entre el voltaje y la corriente en el sistema:

Ecuación de Kirchhoff:  $U (T)+I(T)*R+L\frac{DI(T)}{DT}+C Y (T)=0$

## 4. Circuitos con Resistores Adicionales
En esta sección, analizaremos un circuito con dos resistores y un condensador. A continuación, se presenta el circuito:

🔑 Definición: Un circuito compuesto por más de un resistor (como R1 y R2) y un condensador puede ser modelado usando las leyes de Kirchhoff para obtener la ecuación del sistema.
## 4.1. Aplicando Leyes de Kirchhoff (LKC)
Cuando tenemos resistores adicionales en el circuito, aplicamos la ley de Kirchhoff de corrientes para modelar el comportamiento del circuito:

$U (T)-2 \frac{DY(T)}{DT}-\frac{1}{0.5}Y(T)=0$

## 4. 4. Ejemplo: Aplicando Nodos
En este caso, utilizamos la ley de Kirchhoff de corrientes para aplicar el análisis de nodos en un circuito con diferentes componentes:

$U(T)-6\frac{DY(T)}{DT}-2Y(T)=0$

## 5. Ejercicios
📚 Ejercicio 1: Obtener el modelo para un circuito con resistores adicionales y un condensador.

Solución:
Utiliza las leyes de Kirchhoff para obtener la ecuación diferencial que describa el sistema. Aplica las ecuaciones obtenidas en la clase para resolver el sistema.

📚 Ejercicio 2:
Aplicar la ley de Kirchhoff para un circuito con dos resistores en serie y un condensador.

Solución:
Similar al ejercicio 1, pero con una configuración distinta de resistores.


## 6. Circuito R-C en Paralelo con Fuente de 0 V
En la figura se presenta un circuito R-C en paralelo que cumple con las especificaciones solicitadas:
Resistencia y condensador en paralelo: Se incluye una resistencia (R) y un condensador (C) conectados en paralelo entre dos nodos comunes (comparten el mismo par de nodos, por lo que tienen el mismo voltaje en sus extremos).
Fuente de voltaje de 0 V: Se representa una fuente ideal de voltaje con valor V = 0 volts conectada entre el nodo superior y tierra. En el análisis de circuitos, establecer una fuente de voltaje en 0 V equivale a reemplazar dicha fuente por un cortocircuito (un conductor ideal)​
studocu.com
. Por ello, en el diagrama la fuente de 0 V aparece como una conexión directa marcada con “V=0”.
Etiquetado claro de componentes: Cada componente está identificado con su símbolo y etiqueta correspondiente: “R” para la resistencia, “C” para el condensador, y “V=0” junto a la fuente de voltaje nula. El nodo inferior se considera tierra (0 V) y se indica mediante el símbolo convencional de tierra en la parte inferior.
Dirección de la corriente: Se añade una flecha indicativa para mostrar el sentido de la corriente en el circuito. En este caso, la flecha apunta desde el nodo positivo (nodo superior) hacia tierra a través de la resistencia, ilustrando la dirección típica de la corriente (por ejemplo, la corriente de descarga del capacitor a través de R).


![image](https://github.com/user-attachments/assets/1da26918-3653-42f3-abe3-adc0fe60e3dc)
