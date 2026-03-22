# sesion-02b 20.03

## matematologías

Voltaje = corriente x resistencia

`Esto es lo mismo = Que esto`

9V = I x (220 Ohm)

9V / 220 ohm = I --> 0,04 A

0,04A x 1000 = 40mA

No importa si coloco la **resistencia** en el **positivo o el negativo**. La resistencia pide menos voltaje al estar colocada, no importa el orden.

### Nuevo material

**Fotoresistor:** Según gemini, Un fotoresistor, fotorresistencia o LDR (Light Dependent Resistor) es un componente electrónico semiconductor cuya resistencia eléctrica varía según la cantidad de luz que incide sobre él. Funciona como un sensor de luz: a mayor luz, su resistencia disminuye, y a mayor oscuridad, su resistencia aumenta.

![fotoresistor](./imagenes/fotoresistor.webp)

**Capatitor/Condensador:** Electrolítico. Según gemini, Un capacitor o condensador es un componente electrónico pasivo que almacena energía eléctrica temporalmente en un campo eléctrico entre dos placas conductoras separadas por un material aislante (dieléctrico). Su función principal es almacenar carga para liberarla rápidamente, filtrar señales, suavizar voltajes y bloquear corriente continua.

Capacitor polarizado, 50V max:

![capacitor](./imagenes/capacitor.jpeg)

Capacitor cerámico, no polarizado:

![condensador](./imagenes/condensador.webp)

### Topología

* Según gemini: La topología es la rama de las matemáticas que **estudia las propiedades de los objetos geométricos** que permanecen inalteradas al deformarlos, estirarlos o doblarlos, sin romperlos ni unirlos (homeomorfismo). **Se centra en la conectividad y el número de agujeros** (género), considerando iguales figuras con distinta forma pero misma estructura topológica. 

* _**Taza igual a dona (toro):**_ En topología, una taza y una dona son equivalentes porque ambas tienen exactamente un agujero (el asa de la taza y el centro de la dona). Si estuvieran hechas de plastilina, se puede moldear una en la otra sin cortarla, lo que las hace homeomorfas, o sea, la misma figura. 

* _**Pantalón igual a infinito:**_ La equivalencia de un pantalón (o cualquier figura con dos agujeros) con un "ocho" o el símbolo de infinito también se basa en la flexibilidad topológica.

![dona](./imagenes/topoplogia.jpg)

### Chip 555

![chip](./imagenes/chip555.jpg)

![chip](./imagenes/conexion-chip.jpg)

![chip](./imagenes/1.png)

![lenguaje-condensador](./imagenes/lenguaje.jpg)

## Ejeercicio en clase

Capacitor 1UF: La lucecita no parpadea.

![conexion](./imagenes/lucecita2.jpg)

Capacitor 10UF: La lucecita parpadea rápido.

![conexion](./imagenes/lucecita.gif)

Capacitor 100UF: La lucecita parpadea lento.

![conexion](./imagenes/lucecita3.gif)

Capacitor 1UF+10UF: Pestañeaba la luz muy rápido

![conexion](./imagenes/lucecita4.gif)

Capacitor 100UF+10UF: Pestañaba la luz a velocidad media (segun yo entre la velocidad del de 100UF solo y el de 10UF)

![conexion](./imagenes/lucecita5.gif)

Capacitor 1UF+100UF: La luz pestañaba lento

![conexion](./imagenes/lucecita6.gif)

Capacitor 10UF+Potenciometro:

![conexion](./imagenes/potenciometro.gif)
![potenciometro](./imagenes/2.png)

Capacitor 10UF+Fotoresistor:

![conexion](./imagenes/fotoresistor.gif)
![potenciometro](./imagenes/3.png)

### encargo-02b

1. ordenar las bitácoras de cada sesión, incluyendo las imágenes de forma ordenada.
2. practicar cualquiera de las materias que hayamos visto que creas que necesites, dejar ese registro en la bitácora 02b como respuesta a este encargo.
3. escribir en la bitácora de hoy al menos 10 preguntas para la próxima sesión, sobre cualquier tema que hayamos revisado o mencionado. pueden ser preguntas técnicas, conceptuales, de diseño, etc. todas las preguntas son bienvenidas.

#### práctica personal
me enfoqué en entender mejor lo del capacitor porque al principio no me hacía tanto sentido por qué cambiaba la velocidad del led
lo que entendí ahora es que el capacitor funciona como una mini “batería” temporal:

se carga con energía y después se descarga, ese proceso de cargar y descargar es lo que hace que el led prenda y se apague
entonces:
* si el capacitor es chico -> se carga y descarga rápido -> el led parpadea rápido
* si el capacitor es grande -> se demora más en cargarse -> el led parpadea lento

por eso cuando cambiábamos los UF en clase, cambiaba la velocidad

#### Preguntas para la próxima clase

1. cómo se calcula el tiempo exacto de parpadeo con el chip 555?
2. cómo afecta el voltaje al comportamiento del circuito?
3. hay un límite de capacitores que se puedan usar?
4. cómo elegir el capacitor correcto según lo que quiero lograr?
5. el fotoresistor puede reemplazar una resistencia normal?
6. hay más formas de controlar el parpadeo?
7. se puede hacer que el parpadeo no sea constante?
8. qué otros sensores se pueden usar en este tipo de circuitos?
9. cómo hacer que el cambio de luz sea más suave y no tan brusco?
10. cómo hacer que el circuito tenga distintos ritmos y no solo uno?
