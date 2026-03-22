# sesion-2b

## Ley de Ohm

La relación fundamental entre voltaje, resistencia y corriente es:

```
V = R × I
```

Donde:

| Símbolo | Nombre | Unidad |
|---------|--------|--------|
| `V` | Voltaje (tensión) | Volt (V) |
| `R` | Resistencia | Ohm (Ω) |
| `I` | Corriente (intensidad) | Ampere (A) |

---

### Las tres formas de la misma ecuación

De `V = R × I` se pueden despejar las tres variables:

```
        V
       ───
V = R × I     →    I = V / R     →    R = V / I
```

| Quiero calcular... | Fórmula | Ejemplo con 9V y 1kΩ |
|--------------------|---------|----------------------|
| Corriente `I` | `I = V / R` | `I = 9V / 1000Ω = 0.009 A = 9 mA` |
| Voltaje `V` | `V = R × I` | `V = 1000Ω × 0.009A = 9 V` |
| Resistencia `R` | `R = V / I` | `R = 9V / 0.009A = 1000 Ω` |

---

### Cómo calcular la resistencia para un LED

Un LED rojo típico necesita:
- Voltaje de operación: **~2V**
- Corriente recomendada: **~20 mA = 0.02 A**

Con una batería de **9V**, el voltaje que "cae" sobre la resistencia es:

```
V_R = V_batería − V_LED = 9V − 2V = 7V
```

Entonces la resistencia necesaria es:

```
R = V_R / I = 7V / 0.02A = 350 Ω
```

Se elige la resistencia comercial más cercana hacia arriba: **390 Ω** o **470 Ω**.

> Usar una resistencia más grande reduce la corriente y hace el LED un poco menos brillante, pero es más seguro. Usar una más chica puede quemar el LED.

---

### El triángulo mágico

Una forma visual de recordar las fórmulas: tapa la variable que querés calcular y leés la operación que queda.

```
        ┌───┐
        │ V │
        ├───┼───┐
        │ R │ I │
        └───┴───┘

  tapa V  →  V = R × I
  tapa R  →  R = V / I
  tapa I  →  I = V / R
```

---

## Capacitor

Un capacitor es un componente que **almacena energía en forma de campo eléctrico** entre dos placas conductoras separadas por un material aislante (dieléctrico). No deja pasar corriente continua (DC) de forma permanente, pero sí reacciona ante cambios de voltaje.

Se puede pensar como un **pequeño tanque de carga**: se llena rápido cuando sube el voltaje y se vacía (descarga) cuando el voltaje baja.

### Unidad de medida

La capacitancia se mide en **Faradios (F)**, pero en electrónica práctica los valores son muy pequeños:

| Símbolo | Nombre | Equivalencia |
|---------|--------|--------------|
| `1 F` | Faradio | 1 F |
| `1 mF` | Milifaradio | 0.001 F |
| `1 µF` | Microfaradio | 0.000001 F |
| `1 nF` | Nanofaradio | 0.000000001 F |
| `1 pF` | Picofaradio | 0.000000000001 F |

### Para qué sirve un capacitor

| Uso | Qué hace |
|-----|----------|
| **Filtrado** | Suaviza el voltaje eliminando ruido o picos (muy común en fuentes de alimentación) |
| **Desacople** | Bloquea DC pero deja pasar señales AC (audio, comunicación) |
| **Temporización** | Junto a una resistencia define tiempos de carga/descarga (circuito RC) |
| **Almacenamiento** | Guarda energía para soltarla rápido (flash de cámara, motores) |

### Tipos comunes

```
  Electrolítico          Cerámico           Film (poliéster)
  ┌──────────┐           ┌──┐                  ┌──┐
  │ +  100µF │           │  │ 100nF            │  │ 100nF
  │  ─── ─── │           └──┘                  └──┘
  └──────────┘
  polarizado             no polarizado          no polarizado
  (tiene + y -)          cualquier orientación  alta precisión
  valores grandes        valores pequeños       audio / filtros
```

> **Ojo con los electrolíticos:** tienen polaridad. Si se conectan al revés pueden calentarse, hincharse o explotar. Siempre fijate cuál pata es el `+`.

### Ejemplo: circuito RC (temporización)

Con una resistencia y un capacitor se puede calcular el tiempo que tarda en cargarse el capacitor al 63% de su voltaje máximo:

```
τ (tau) = R × C

Ejemplo: R = 10kΩ, C = 100µF
τ = 10.000 Ω × 0.0001 F = 1 segundo
```

El capacitor se considera "completamente cargado" luego de **5τ** (5 veces tau) → en este caso, ~5 segundos.

---

## Circuito integrado 555

El **NE555** (o simplemente "555") es uno de los circuitos integrados más usados de la historia. Fue diseñado en 1972 y todavía hoy se usa en miles de proyectos. Sirve para generar pulsos, temporizadores, osciladores y señales cuadradas.

Internamente combina resistencias, comparadores y un flip-flop para controlar cuándo su salida está en HIGH o LOW.

### Pinout (vista desde arriba)

```
              ┌────────┐
   GND    1 ──┤        ├── 8   VCC  (+5V a +15V)
   TRIG   2 ──┤  555   ├── 7   DISCH
   OUT    3 ──┤        ├── 6   THRES
   RESET  4 ──┤        ├── 5   CTRL
              └────────┘
```

| Pin | Nombre | Función |
|-----|--------|---------|
| 1 | GND | Tierra, negativo de la alimentación |
| 2 | TRIG | Disparo: si baja de 1/3 VCC → activa la salida |
| 3 | OUT | Salida: HIGH o LOW según el estado interno |
| 4 | RESET | Si se pone en LOW fuerza la salida a LOW (normalmente a VCC) |
| 5 | CTRL | Control de voltaje interno (normalmente va un capacitor de 10nF a GND) |
| 6 | THRES | Umbral: si sube a 2/3 VCC → desactiva la salida |
| 7 | DISCH | Descarga: conectado internamente para vaciar el capacitor |
| 8 | VCC | Alimentación positiva (+5V a +15V) |

### Modos de operación

#### Modo monoestable (un solo pulso)

Genera **un pulso de duración fija** cada vez que se activa el TRIG. Útil para retardos o rebotes de botón.

```
TRIG ──>                     (disparo)
OUT  ──┐      ┌──            (pulso de duración t)
       └──────┘

t = 1.1 × R × C

Ejemplo: R = 10kΩ, C = 10µF → t = 1.1 × 10.000 × 0.00001 = 0.11 s
```

#### Modo astable (oscilador libre)

Genera una **señal cuadrada continua** sin necesidad de disparo externo. El capacitor se carga y descarga entre dos resistencias, haciendo que la salida suba y baje indefinidamente.

```
OUT  ─┐  ┌──┐  ┌──┐  ┌──    (oscila solo)
      └──┘  └──┘  └──┘

Frecuencia:  f = 1.44 / ((R1 + 2×R2) × C)
Duty cycle:  D = (R1 + R2) / (R1 + 2×R2) × 100%

Ejemplo: R1 = 1kΩ, R2 = 10kΩ, C = 10µF
f = 1.44 / (21.000 × 0.00001) ≈ 6.86 Hz
```

> El modo astable es ideal para hacer parpadear un LED, generar tonos o hacer un metrónomo simple.

