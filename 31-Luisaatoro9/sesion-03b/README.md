# sesion-03b Viernes 27 marzo

Tema: Introducción a Circuitos y Análisis de Esquemas

En esta sesión profundizamos en la lectura de esquemáticos electrónicos y el comportamiento de la energía en diferentes configuraciones de circuitos.

## 1. Modos de Operación de Circuitos

Aprendimos a identificar tres estados fundamentales en los circuitos electrónicos:

    Astable: El circuito no tiene un estado estable y oscila continuamente (ideal para luces parpadeantes).
    Monostable: Tiene un estado estable y solo cambia temporalmente cuando recibe un estímulo externo.
    Bistable: Tiene dos estados estables y permanece en cualquiera de ellos hasta que se le indica cambiar.

## 2. Análisis de Circuitos y Resistencias

Revisamos cómo se comporta la energía dependiendo de cómo conectamos los componentes:
Configuraciones de Circuitos

    Circuito en Serie: Los componentes van uno tras otro.
    Circuito en Paralelo: La energía tiene múltiples caminos, lo que hace que la carga sea más "llevadera" entre los componentes. Si un camino falla, el resto debe asumir más carga.
    Circuito Diamante (Puente): Una configuración específica para equilibrar o medir voltajes.

Cálculos de Resistencia Equivalente (ReqReq​)

Para calcular la resistencia total en un circuito en paralelo, usamos la fórmula:

1Req=1R1+1R2Req​1​=R1​1​+R2​1

**💡Tip**

Cuando tenemos solo dos resistencias en paralelo, aplicamos la regla de: "Arriba se multiplica y abajo se suma". Req=R1⋅R2R1+R2Req​=R1​+R2​R1​⋅R2​​
🧮Resistencia Equivalente (Paralelo)

Para dos resistencias en paralelo, la fórmula simplificada que mencionaste (multiplicación arriba, suma abajo) es:

* **Req=R1⋅R2R1+R2Req​=R1​+R2​R1​⋅R2**
​

**Apuntes**

* **El 555 en configuración astable funciona como un oscilador que genera una señal periódica de onda cuadrada, alternando continuamente entre niveles alto y bajo.**
* **Resitencia equivalente:** Es una resistencia imaginaria que tiene el mismo efecto que todas las resistencias de un circuito juntas. Es como si cambiaras un grupo de piezas por una sola que hace exactamente el mismo trabajo.
* **o´eilly - willey - libros**
* **Link libros:** https://docs.google.com/document/d/1gTPNpDtJLYWSLITBKJXJEM3XxiRnhSkOY_hltDzEYis/edit?usp=sharing
* **Link conversión:** https://www.digikey.com/es/resources/conversion-calculators/conversion-calculator-resistor-color-code
<img width="340" height="898" alt="Captura de pantalla 2026-03-27 110857" src="https://github.com/user-attachments/assets/b1f4ec71-2f1e-45fd-ab79-70cfeff5ae25" />
<img width="330" height="934" alt="Captura de pantalla 2026-03-27 111123" src="https://github.com/user-attachments/assets/db52f551-42f6-4eda-a30f-ddb77377c0e2" />
<img width="330" height="958" alt="Captura de pantalla 2026-03-27 112136" src="https://github.com/user-attachments/assets/fd6c567c-9a92-4e4e-851a-d7175e6af731" />

# Datos
* **Para comprar cosas en barrio San Diego, donde todo se compra presencial. Busquen las direcciones en Google MAPS.**
* **Electronica Ibarra es la más barata si pagan en efectivo.**
* **Electronica Hobby es la más grande, pero a veces tiene filas largas.**
* **Electronica ORFALI tiene la señora más amable, pero a veces es un poco cara.**
* **Electronica MINY tiene componentes más extraños.**
* **Dentro de Galería SUR se encuentran desarmadurías donde encuentran componentes más exóticos aún.**

# **Ejercicios:**

https://github.com/user-attachments/assets/a6650c78-b97b-4c8c-8c9e-d1963e3b5500

https://github.com/user-attachments/assets/4d6c63b8-cb2f-49a7-9113-e06dd1082fd2

<img width="330" height="541" alt="atari-punk" src="https://github.com/user-attachments/assets/a92d62ad-26d6-4bc3-be46-87a8b47235ac" />
<img width="330" height="541" alt="atari-punk" src="https://github.com/user-attachments/assets/579ff073-117f-46df-ba7e-711d3ed91fa9" />
<img width="330" height="541" alt="atari-punk" src="https://github.com/user-attachments/assets/32bf51d0-9083-4fb0-bb80-ca2ac5bf1fa5" />



R1 va a ser un pote
R4 va a ser un LDR
C1 va ser de 100n
<img width="1000" height="541" alt="atari-punk" src="https://github.com/user-attachments/assets/40ef318c-a4b2-4f98-8b45-ac2595e7eef9" />


## 4. Reflexiones de Clase

Vimos que en los circuitos en paralelo, la distribución de la energía es más eficiente. Sin embargo, hay que tener cuidado: si un componente deja de aportar o se desconecta, el resto del circuito recibe una carga mayor, lo que podría afectar el funcionamiento general.​​
