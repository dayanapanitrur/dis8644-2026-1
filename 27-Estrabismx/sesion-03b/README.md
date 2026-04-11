# sesion-03b

***Actualizar sobre suma de resistencias e investigar las leyes de Kirchhoff***

>En la sesion-04a se profundizará, ahora no hay tiempo y creo que quedó un registro algo extenso

## Apuntes clase viernes 27 de marzo ##

### Simbología ###

Resumen de las abstracciones simbólicas de cada componente visto hasta la fecha:

![Foto simbología bitácora fisica](./imagenes/simbologia.jpg)

<br>

### Chip 555 ###

A pesar de llevar un par de sesiones trabajando este chip, vamos a hacer breve definición de este chip tan versátil

El **555** en palabras simples es un *timer*, es decir, recibe una corriente constante y la transforma a una intermitente, su frecuencia varía de como se configure con cada *pata*

![Chip 555](./imagenes/555-timer-diagram.gif)

Cada punto de conexión quedaría así

| Pin | Nombre | Función |
| - | - | - |
| 1 | GND | Conexión a tierra |
| 2 | Trigger | **Disparo**. Inicia el ciclo de temporización cuando el voltaje cae por debajo de $1/3$ de $V_{CC}$ |
| 3 | Output | **Salida.** Aquí es donde se conecta la carga (LED, parlante, etc.). Da voltaje alto o bajo |
| 4 | Reset | **Reinicia** el chip si se conecta a tierra. Normalmente se conecta al positivo para que no se reinicie solo |
| 5 | Control | Permite variar el umbral de comparación mediante voltajes externos. Se suele usar un pequeño capacitor aquí para evitar ruido |
| 6 | Threshold | **Umbral**. Detiene el ciclo de temporización cuando el voltaje supera los $2/3$ de $V_{CC}$ |
| 7 | Discharge | **Descarga**. Se usa para descargar el capacitor externo que determina el tiempo del ciclo |
| 8 | VCC | **Alimentación**. El polo positivo (normalmente entre 4.5V y 16V) |

<br>

![Foto 555](./imagenes/temporizador.webp)

> Imagen de chip 555, sumado a lectura de sus Pin

<br>

<br>

#### Modo Astable ####

Fue el primer acercamiento visto en clases, donde el modo astable convierte al 555 en un oscilador autónomo. En esta configuración el chip no tiene un estado estable, de ahí su nombre. La salida (Pin 3) conmuta constantemente entre alto y bajo sin necesidad de un disparo externo.

Funciona mediante la carga y descarga cíclica de un capacitor externo a través de resistencias. Se utiliza principalmente para generar ondas cuadradas, señales de reloj, luces intermitentes o ***tonos de audio.*** 

***Resumido y con analogía:*** Cuando la corriente empieza a circular, se activa el pin 2 que le manda una señal al pin 3 que deja la onda de corriente en la *parte alta*, mientras esto ocurre la energía fluye por R1 y RV1 que cargan el capacitor 3, cuando llega a cierto nivel de carga C3, el pin 6 lo detecta y manda una señal al pin 7 para que se conecte a tierra y descargar al capacitor, al ocurrir todo esto el input *2* detecta que no hay corriente y vuelve a activarse, iniciando así un nuevo ciclo

![Esquematico sesion-02b](./imagenes/esquematico.png)

> Esquematico Astable sesion-02b

<br>

#### Modo Monostable ####

Funciona como un temporizador de ***un solo disparo***. A diferencia del astable este circuito tiene un solo estado estable

Cuando recibe un pulso negativo en el pin 2, la salida pasa a estado alto durante un tiempo determinado y luego regresa automáticamente a su estado de reposo.

***Una explicación más tecnica y coloquial a la vez sería:*** Se recibe un input en el *2* (que según el esquemático, varía por el potenciometro pero sigue siendo constante), al cual posteriormente se le regulado su *velocidad* con la resistencia 1, y donde el capacitor 3 genera un *conteo* al cargarse y descargarse. Todo este conjunto de procesos hace que se genere un pulso que se apaga luego de un determinado tiempo, basicamente, es como la subida de defensea y resisitencia mágica de Warwick en LoL al presionar la habilidad *E* 

![Esquematico Monstable sesion-03a](../sesion-03a/imagenes/sesion-03a-ej-01-sch.png)

#### Atari Punk Console ####

La Atari Punk Console (APC) es un sintetizador de audio DIY (***Do it yourself*** [Larga vida al DIY]) muy popular. Tiene como base 2 chips 555, su nombre viene de los sonidos similares a las consolas Atari.

Usa un modo astable para crear pulsos y uno monoestable para controlar su duración. Con dos perillas controlas el tono y el ritmo, creando ruidos electrónicos, chirridos y efectos *lo-fi* como dirían los lolos

En palabras más propias y no tan GPT. Tenemos un 555 que genera un pulso astable (intermitente), controlado por un potenciometro ligado a los pin 2 y 7, el cual termina saliendo por el pin 3 ingresando al 2do chip 555 por el input 2, para que luego inicie el *conteo* para apagar la señal (funcionamiento propio del monostable), este siendo regualdo por el capacitor 3 y así generar un sonido más unico 

<br>

![Esquemático Atari Punk Console](./imagenes/atari-punk.png)

> Se consideró que R1 fuera un potenciometro y R4 un LDR

<br>

<br>

##### Registro Fotográfico #####

![Registro Fotográfico](./imagenes/proto-atari-punk-1.jpg)

![Registro Fotográfico](./imagenes/proto-atari-punk-2.jpg)

![Registro Fotográfico](./imagenes/proto-atari-punk-3.jpg)

![Registro Fotográfico](./imagenes/case-atari-punk.jpg)

<br>

<br>

### Bibliografía ### 

Durante la clase se mencionaron autores, conceptos y webs utilites para tener en cuenta a futuro

<br>


#### Robert Forrest Mims ####

Es un destacado escritor y diseñador de circuitos estadounidense, reconocido por su capacidad para simplificar conceptos complejos de ingeniería. Aunque no posee una formación académica formal en electrónica, su impacto es masivo gracias a sus cuadernos de notas técnicos, caracterizados por diagramas hechos a mano que guiaron a generaciones de aficionados

Su mayor aporte respecto al 555 radica en la democratización de su uso. A través de su célebre libro ***Engineer's Mini-Notebook: 555 Timer IC Circuits***, Mims transformó este chip en la herramienta educativa por excelencia. Al proponer aplicaciones prácticas y accesibles, desde osciladores hasta temporizadores, convirtió al chip en un pilar fundamental para el aprendizaje de la electrónica recreativa y experimental.

<br>

#### Editoriales ####

El siguiente listado son editoriales que tienden a trabajar libros enfocados en electronica (recomendados por Aarón)

1. O´Reilly
2. Wiley
3. Routledge (?) /No escuché bien como se llamaba

<br>

#### Guias ####

Lista de conceptos para complementar busquedas de información sobre chips, circuitos o similares

1. Handbooks: Escrito que contiene las nociones o informaciones fundamentales
2. Cookbooks: No se refiere a un recetario de cocina, sino a una guía paso a paso de como hacer algo
3. Manual reference: Es un manual detallado con la lógica y conceptos detras del funcionamiento de componentes y circuitos
4. Data Sheets: Conjunto de datos técnicos sobre los componentes

<br>

#### 555-timer-circuits ####

Es una web donde podemos encontrar variedad de información, como información técnica del chip 555 (voltajes, lógicas de funcionamiento, etc), historia de este, circuitos a construir, etc 

https://www.555-timer-circuits.com/

<br>

![Sitio web](./imagenes/captura-de-pantalla.png)

![Ejemplo Servo Tester](./imagenes/captura-de-pantalla2.png)

<br>

### Chips quemados ###

Durante la ejecucción del ejercicio me percaté que a pesar de tener todo conectado no funcionaba el modo monostable del ***Atari Punk Console***, luego de 15 minutos intenté cambiar los chips, ahí es donde caí en cuenta que de los 4 que tenía, queme 3. En el momento le tome mucha importanica, luego de revisar el Discord de la clase, vi que compartieron lugares para comprar componentes electrónicos y luego de comprar chips 555 a solo $250 me di cuenta que el error no era tan grave y fue parte importante del proceso, puesto que conocí nuevos componentes que me llamaron la atención y de los cuales investigaré más adelante. Ahora dejaré por escrito los lugares y ubicaciones visitadas para tener registro para posterior.

1. Electrónica Ibarra: San Diego 920, Santiago 
2. Electrónica Hobby: San Diego 962, Santiago 
3. Electrónica Orfali: San Diego 955, Santiago
4. Electrónica Casa York: San Diego 958 Santiago 

![Mapa con Ubicaciones en mapa](./imagenes/3.png)

<br>

#### Fotos compra ####

![Foto compra](./imagenes/foto-compra1.jpg)

![Foto compra](./imagenes/foto-compra2.jpg)

![Foto compra](./imagenes/foto-compra3.jpg)

![Foto compra](./imagenes/foto-compra4.jpg)

![Foto compra](./imagenes/foto-compra5.jpg)

---

## Info Adicional / Transistor 2N2222 A331 ##

En la clase se nos entregó un transistor, a pesar de que aún no lo utilizamos, realicé una breve introducción sobre su funcionamiento, estos son puntos claves

> El Transistor entregado fue el 2N2222 A331

-  El modelo corresponde a la parte 2N222, la parte A331 es un código de registro del fabricante.
-  Es un transistor del tipo NPN, es decir que posee 2 modos. El primero es de tipo interruptor, sirviendo como switch normal. El segundo es un modo ***amplificador*** el cual convierte una señal débil en una más fuerte

<br>

![Transistor](./imagenes/transistor.webp) 

### Partes del transistor ###

1. Emitter (Emisor): Es el contacto a tierra
2. Base: Se encarga de controlar la corriente eléctrica
3. Collector (Colector): Asociado al ingreso de la energía

