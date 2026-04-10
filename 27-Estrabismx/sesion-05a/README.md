# sesion-05a

## Apuntes Clase 07 de Abril ##

### Compuertas lógicas ###

[Hablar sobre sus partes, tales como las entradas inversoras]

#### Algebra de Bool ####

### Chips 4093 - 386 ###

### Sonido y sus alteraciones ###

#### Filtro ####

#### Variaciones / Oscilaciones ####

#### Apartado siglas ####

- VCC

- VC

- VCA

- VCO

- DAC

- ???

### VCV RACK###

#### Eurorack ####

### Moritz Klein ###

[https://moritzkleininstruments.com/]

#### Manuales ####

[https://moritzkleininstruments.com/] [Incluir el manual]

#### Videos ####

[Hablar de su canal de Youtube]

## Ejercicios Aplicados ##

### Oscilador ###

## Encargo / _Schmitt Trigger_ ##

*** Complementar con el funcionamiento de las compuertas lógicas ***

Es un circuito comparador (compara 2 voltajes para definir cual es el encendido y cual es el apagado) que se conecta a la entrada no inversora (quien recibe voltaje + y lo amplifica, no así la entrada opuesta, la que al recibir voltaje + lo disminuye) [***Actualizar esta parte para que quede definida en el punto de compuertas lógicas***] de la compuerta lógica 

> Revisar todo lo anterior, está algo curioso xd

### Definición más propia y más simple: ###

Este sistema establece un umbral para definir cuando algo está encendido y cuanto está apagado, este umbral se genera tomando como referencia 2 voltajes diferentes, por lo que elimina el _ruido_ que podría alterar a un comparador normal. 

Por ejemplo: Si estamos jugando Minecraft tenemos 3 posibilidades 

a. Estar quieto (0)

b. Caminar (0.5)

c. Correr (1)

Y estas se definen según cuanta presión apliquemos al botón _W_, siendo 0 no presionar y 1 tener la tecla hasta el fondo, un comparador normal entendería que:

a. Estar quieto (0 - 0.4)

b. Caminar (0.5)

c. Correr (0.6 - 1)

Por lo que si jugamos normalmente y tenemos ligeras variaciones como 0.4 a 0.6 tendriamos a _Steve_ pasando de caminar a correr a estar quieto de manera intermitente e irregular. Lo más normal es querer variar estos umbrales tan sensibles, ahí entra en juego el Shmitt Trigger, quien establecería límites _más reales_, es decir que entendería que:

a. Estar quieto (0 - 0.2)

b. Caminar (0.3 - 0.7)

c. Correr (0.8 - 1)

Estableciendo un rango más amplio y reduciendo la sensibilidad.

> Entiendo que puedan existir ciertos puntos que no asemejen la realidad del funcionamiento del sistema en cuestión, pero en tintes generales esta fue mi manera de entender como funciona
>
> > Se que para correr en Minecraft se debe presionar la _W_ dos veces con un determinado tiempo, no soy fake fan xd
