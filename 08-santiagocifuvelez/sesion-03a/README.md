# sesion-03a

24 de marzo del 2026

¡Hola profes!, les deseo un bonito día en el momento que se encuentren leyendo esto.
El día de hoy, la bitácora estará dividida en # partes:

1.	Explicación sobre la frecuencia y la oscilación.
2.	Esquematización del parlante y de los botones.
3.	Lectura de estos esquemas para su realización.
4.	Circuito ASTABLE
5.	Registro de intentos del Toy Organ.
6.	Apuntes del documental “variaciones espectrales sobre la vida de José Vicente Asuar”.

Veamos que tal.

## 1.	Explicación sobre la frecuencia y la oscilación.

**¿Qué es la frecuencia?**

La frecuencia es básicamente qué tan rápido se repite una señal eléctrica en el tiempo. En otras palabras; es la cantidad de veces que una corriente o voltaje completa un ciclo en un segundo.

![frecuencia](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-03a/imagenes/img1.jpg)

**¿Como funciona esto con el chip 555?**

Pues este funciona con una frecuencia de oscilación:

![frecuencia,oscilación 555](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-03a/imagenes/img2.jpg)

El circuito funciona generando una señal que cambia repetidamente entre 0V y 9V, lo que se conoce como una oscilación. Esta oscilación es producida por el NE555 timer, que utiliza la energía de la pila para cargar y descargar un capacitor de forma continua. Como resultado, la salida del circuito “enciende y apaga” constantemente, creando una señal periódica cuya rapidez está determinada por la frecuencia de oscilación.

## 2. Esquematización del parlante y de los botones.

Cuando se utilizan parlantes en un circuito, es importante poder controlar la frecuencia de la señal, ya que esta determina el tono del sonido que se escucha. Por eso, en lugar de una resistencia fija, se emplean componentes como un potenciómetro o un fotorresistor, que permiten variar la resistencia del circuito. El potenciómetro permite un control manual, ajustando el tono según la posición, mientras que el fotorresistor modifica la frecuencia automáticamente en función de la luz del entorno. Así, el circuito deja de ser estático y se vuelve interactivo, generando sonidos que pueden cambiar en tiempo real.

