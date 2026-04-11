# Sesión 01b: Viernes 13 de marzo

**Temas:** Introducción a protoboards, LEDs y resistencias / Reporte Aaron Swartz.

## 1. Investigación: Componentes Pasivos y de Salida o básicos

En esta sesión introducimos el hardware que será la base de nuestros prototipos. He profundizado en el funcionamiento técnico de cada uno para entender por qué son fundamentales.

**Conceptos Técnicos:**

* **Componentes Pasivos:** Son aquellos que no pueden generar energía por sí mismos, solo la consumen, la limitan o la almacenan.   La **resistencia** es el ejemplo más claro, ya que su función es limitar el paso de la corriente.
* **Componentes de Salida (Actuadores):** Son los que transforman la energía eléctrica en otro tipo de fenómeno físico que podemos percibir. En nuestro caso, el **LED** actúa como un componente de salida al convertir la electricidad en luz visible.

**Protoboard (Placa de pruebas):** Es una placa con orificios conectados eléctricamente entre sí siguiendo patrones de líneas.

* **Funcionamiento interno:** Las filas centrales están conectadas horizontalmente (en nodos de 5 puntos), mientras que las líneas laterales (buses) están conectadas verticalmente para la alimentación ($VCC$ y $GND$).
* **Importancia:** Permite prototipar sin soldar, facilitando el error y la experimentación rápida.

**LED (Diodo Emisor de Luz):** Es un componente semiconductor que emite luz cuando la corriente fluye a través de él.

* **Polaridad:** Es un dispositivo polarizado.
* El **Ánodo** (pata larga, $+$) y el **Cátodo** (pata corta, $-$). Si se conecta al revés, no conduce electricidad.

* **Dato técnico:** Los LEDs tienen un voltaje de caída (forward voltage) que varía según su color (aprox. $1.8V$ para rojo y $3.2V$ para azul/blanco).

**Resistencia (Resistor):** Componente diseñado para introducir una resistencia eléctrica específica en un circuito.

* **Función crítica:** Limitar el flujo de corriente para proteger componentes sensibles como los LEDs. Sin una resistencia adecuada, el LED recibiría demasiada corriente y se quemaría por efecto Joule (calor excesivo).
* **Ley de Ohm:** Es la base para calcular qué resistencia usar: $V = I \cdot R$.
  
## 2. encargo-01b: "The Internet's Own Boy" (Aaron Swartz)

Aaron Swartz no fue solo un programador prodigio; fue un arquitecto de la libertad en la red. Participó en la creación del formato **RSS** a los 14 años, fue co-fundador de **Reddit** y una pieza clave en **Creative Commons**. El conflicto ético y legal Su detención por descargar masivamente artículos académicos de **JSTOR** en el MIT puso en evidencia una tensión que aún persiste: ¿De quién es el conocimiento? Aaron creía que el acceso a la información académica (pagada muchas veces con fondos públicos) debería ser un derecho humano, no un negocio de editoriales privadas.

Reflexión y Conclusión Propia Tras ver el documental y analizar su legado, mi conclusión es que como **Diseñadores Industriales** que interactúan con tecnología y electrónica, no podemos ser "neutrales". La historia de Aaron me hace reflexionar sobre la **ética del código y del hardware**. A menudo diseñamos objetos sin pensar en quién tiene acceso a la tecnología o cómo los algoritmos pueden restringir libertades. Su sacrificio nos recuerda que la innovación debe ir de la mano con la responsabilidad social. Me quedo con la idea de que la tecnología es una herramienta de empoderamiento, y que nuestro rol en este taller es aprender a usarla no solo para que "funcione", sino para que aporte valor real y abierto a la sociedad.

### Referencias y Fuentes

* **Documental:** *The Internet's Own Boy: The Story of Aaron Swartz* (2014).
* **Teoría:** *All About LEDs*, [Adafruit Learning System](https://learn.adafruit.com/all-about-leds).
* **Articulo:** [Adiós a Aaron Swartz, un hacker y activista extraordinario](https://www.eff.org/deeplinks/2013/01/farewell-aaron-swartz) - Electronic Frontier Foundation (EFF).
