# Game Design Document

**Versión:** 2.2
**Fecha:** 29/07/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Título

El título del juego será "Algoritmia".

## 2. Resumen del juego

Algoritmia es un videojuego que forma parte de la Plataforma Gamificada Algoritmia (PGA). Es un videojuego en donde aprenderás algoritmos, lógica y estructuras de control resolviendo problemas diseñando y visualizando la ejecución tu propio algoritmo. Deberás enfrentarte a desafíos, recolectar y usar objetos, luchar contra enemigos y evitar obstáculos con tu propio algoritmo diseñado a tu manera para completar la misión y aprendiendo en el proceso.

## 3. Concepto y pilares de diseño

La escencia del videojuego y lo que quiero transmitir se basan en estos 3 pilares:

### 3.1 Pixel Art

El pixel art es un estilo artístico de videojuegos. Es reconocido por su estética retro y la conexión que tiene con los videojuegos clásicos, en donde la resolución y recursos eran limitados. Se caracteriza por ser un estilo muy artesanal, donde cada diseño se realiza pixel por pixel logrando un estilo muy simple pero a la vez detallado, el cual resulta agradable a la vista.

Lo que Algoritmia quiere transmitir con su estilo visual es simpleza pero belleza a su vez mediante el pixel art en sus escenarios isométricos / top down estilo RPG, interfaces, objetos y personajes utilizando colores llamativos, una paleta de colores adecuada a la estética y trama del videojuego y diseños minimalistas. Se busca transmitir esa sensación de estar jugando un videojuego pero aprendiendo a la vez.

### 3.2 Pseudocodigo gamificado y ejecución en tiempo real

Algoritmia tendrá un pseudocodigo gamificado llamado _PGAScript_ compuesto con primitivas, estructuras de control y manejo de variables y de procedimientos que permitirán al jugador diseñar sus soluciones para las misiones del juego, visualizando en tiempo real la ejecución del algoritmo en el escenario de juego.

### 3.3 Aprendizaje continuo con feedback inmediato

Algoritma busca brindar aprendizaje continuo mediante feedback inmediato durante y post diseño del algoritmo para resolver la misión. Algoritmia analizará automáticamente el código del jugador y ofrecerá sugerencias y optimizaciones para mejorar el algoritmo propuesto, asi como tambien la recopilación de datos de los errores frecuentes para la toma de decisiones o refuerzo de contenidos a posteriori por parte de los docentes.

## 4. Descripción del juego

Algoritmia es un videojuego de aventura con estética RPG con vista isométrica en donde el jugador tendrá que completar misiones divididas en capítulos temáticos diseñados y enfocados los conceptos base de la programación. El alcanse del videojuego abarcará los conceptos de:

- Algoritmos y secuencia de pasos
- Lógica proposicional
  - Proposiciones simples y compuestas
  - Operadores lógicos: OR, AND, NOT
  - Operadores matemáticos: suma (+), resta (-), multiplicación (*), división (/) y módulo (mod).
  - Comparadores relacionales: <, >, ==, <=, >=, !=
- Estructuras de control (Si-Sino, Mientras y Repetir)
- Declaración y asignación de variables (globales y locales)
- Procedimientos sin parámetros o con parámetros de: entrada, salida y entrada/salida.

En cada misión, el jugador deberá resolver un problema con reglas y condiciones específicas utilizando pseudocodigo gamificado _PGAScript_ compuesto con primitivas, estructuras de control, manejo de variables y procedimientos pero tomando un enfoque estilo RPG con acciones, habilidades especiales y objetos que permitirán al jugador diseñar sus propios algoritmos para poder completar las misiones, visualizando en tiempo real la ejecución del algoritmo en el escenario de la misión.

El objetivo de Algoritmia es que el jugador pueda lograr el aprendizaje continuo de las bases de la programación. Para ello, el videojuego ofrecerá la documentación de _PGAScript_ en todo momento, ayudas al jugador para detectar y corregir errores de manera sencilla y lo más importante: feedback inmediato en forma de sugerencias y optimizaciones formativas y explicativas para mejorar el algoritmo propuesto.

### 4.1 Pseudocodigo gamificado

Como mencioanmos, el pseudocodigo gamificado _PGAScript_ estará compuesto por primitivas, estructuras de control y manejo de variables y procedimientos. Pero, para darle un tono de videojuegos, cada uno de estos elementos de la programación tradicional se representarán con componentes de videojuegos estilo RPG:

- **Primitivas -> "Acciones"**: las acciones representarán a las primitivas básicas (atómicas) que el jugador podrá realizar.
- **Estructuras de control -> Estrategias**: las estrategias representan las estructuras de control básicas: Si-Sino, Mientras y Repetir donde se podrán manejar proposiciones simples o compuestas utilizando operadores matemáticos básicos y operadores relacionales.
- **Variables -> Objetos**: los objetos representarán a las variables del juego. Se tendrán dos tipos de variables:
  - Variables de juego relacionadas al escenario y a los objetos de inventario del jugador.
  - Variables globales y locales de tipo entero y tipo booleano que el jugador podrá declarar y asignar valores.
- **Procedimientos -> Habilidades especiales**: las habilidades especiales representarán a los procedimientos. Se tendrán dos tipos de procedimientos:
  - **Procedimientos pre-diseñados** desbloqueables que el jugador podrá utilizar como "Habilidad especial"
  - Procedimientos que el jugador podrá definir e invocar incluyendo o no parámetros de entrada, salida y entrada/salida en el diseño del algoritmo.

Se especificará a mas detalle el diseño de _PGAScript_ en la sección _6.1 PGAScript_

### 4.2 Feedback formativo y ayudas

Las ayudas que se ofrecerán son las siguientes:

1. **Manual del heroe**: El "_Manual del Heroe_" es un manual que representará la documentación de PGAScript y estará disponible para consulta del jugador en todo momento durante el diseño del algoritmo. Especificará la sintaxis y semántica de cada primitiva, estructura de control, variable de juego, el manejo de variables y procedimientos que el jugador puede utilizar para resolver la misión.
2. **Ayuda visual con colores e íconos**: cada primitiva, estructura, variable o procedimiento estará resaltado con un color e ícono representativo para denotar que está bien definida la instrucción para así tambien detectar errores de sintaxis. Un texto plano sin ícono o color indicará que la instrucción está mal escrita o no existe.
3. **Resaltado de sintaxis**: se resaltarán los errores de sintaxis y advertencias en color rojo y amarillo respectivamente.

En cuando al feedback formativo, se dará en tres etapas:
**1. Durante el diseño de la algoritmo**:
Mientras el alumno diseña su algoritmo para la misión, se estará analizando y controlando en tiempo real la estructura y sintaxis de la misma para poder indicar errores y sugerencias antes de pasar a la ejecución.

**Errores**
Los errores son aquellos que impiden que la ejecución del algoritmo se lleve a cabo. Los posibles errores a indicar son los siguientes:

| Error                  | Descripción                                                                               | Feedback                                                                                                                                                                                                     |
| ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Error de sintaxis      | Se da cuando hay instrucciones o estructuras mal escritas                                 | Indicador rojo en el número de la linea del error y subrayado en rojo en la instrucción o estructura mal escrita. Si se apoya el cursor por encima del error se mostrará "Error de sintaxis".                |
| Variable no declarada  | Cuando se intenta utilizar una variable (global o local) que no fue declarada previamente | Indicador rojo en el número de la linea del error y subrayado en rojo en donde se quiere utilizar la variable. Si se apoya el cursor por encima del error se mostrará el mensaje de "Variable no declarada". |
| Parámetros indefinidos | Cuando se llama a un procedimiento y no se colocan los parámetros de manera correcta      | Indicador rojo en la linea del error y subrayado en rojo en el procedimiendo llamado. Si se apoya el cursor por encima del error se mostrará "Parámetros erróneos o indefinidos".                            |

**Advertencias**
Las advertencias son aquellas que no impiden que el algoritmo se ejecute pero son recomendable de atender. Las posibles advertencias son las siguientes:

| Advertencia                              | Descripción                                             | Feedback                                                                                                                                                                                                                                                             |
| ---------------------------------------- | ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Variable declarada pero no utilizada     | Cuando se declara una variable pero nunca se utiliza    | Mientras el jugador no la utilice, indicador en amarillo en la línea de la advertencia y subrayado en amarillo en la variable declarada pero no utilizada. Si se apoya el cursor por encima de este aviso se mostrará "Variable no utilizada".                       |
| Procedimiento definido pero no utilizado | Cuando se define un procedimiento pero nunca se utiliza | Mientras el jugador no lo utilice, indicador en amarillo en la línea de la advertencia y subrayado en amarillo en la cabecera del procedimiento definido pero no utilizado. Si se apoya el cursor por encima de este aviso se mostrará "Procedimiento no utilizado". |

**2. Al intentar ejecutar**
Cuando el alumno terminó de diseñar el algoritmo y decida ejecutar, el sistema verificará que la estructura y sintaxis esté correctamente escrita para ejecutar.
Si se ignoran todos los **errores** durante el diseño del algoritmo, este no se podrá ejecutar y se mostrará un mensaje indicando en rojo la linea donde se encuentra el error, el motivo y la sugerencia para corregirlo.

**3. Después de la ejecución del algoritmo indicando:**
Luego de la ejecución del algoritmo del alumno, completado el ejercicio y dada la puntuación obtenida, el sistema analizará el algoritmo proponiendo mejoras y optimizaciones. El sistema mostrará el antes y después de aplicar los cambios al algoritmo del jugador, una breve explicación de los cambios realizados, el por qué y la posibilidad de aplicarlos si asi lo desea.

- **Redundancia de instrucciones**: si hay al menos 2 lineas de código llamando a la misma instrucción se sugerirá reemplazarlas por una estructura repetitiva como un mientras o un repetir.
- **Redundancia de condicionales**: si hay al menos 2 estructuras de control "Si" una debajo de la otra se sugerírá reemplazarlas por una estructura condicional con una proposición compuesta por las dos proposiciones originales utilizando un conectivo lógico apropiado.
- **Redundancia de bucles**: si hay al menos 2 estructuras de control "Mientras" o "Repetir" una debajo de la otra se sugerirá reemplazarlas por una estructura repetitiva con una proposición compuesta por las dos proposiciones originales utilizando un conectivo lógico apropiado.
- **Variables no utilizadas**: si hay variables declaradas pero no utilizadas se sugerirán eliminarlas del código.

### 4.3 Core Loop

El Core Loop principal del videojuego es:

1. Ingresar al mapa principal del juego
2. Seleccionar un capitulo
3. Seleccionar la misión deseada
4. Diseñar un algoritmo para resolver la misión
5. Ejecutar el algoritmo visualizando el efecto de cada instrucción en el escenario
6. Si se completa la misión exitosamente, recibir una puntuación de hasta 3 estrellas y EXP.
7. Recibir feedback formativo por parte del sistema para refactorizar y optimizar el algoritmo si se quiere.

## 5. Historia

### 5.1 Narrativa

"Cuenta la leyenda que en el reino de **"Algoritmia"**, en lo más profundo del _Santuario Algorismi_ se encuentra escondido un tesoro muy especial: un algoritmo que tiene el poder de resolverlo todo, llamado _Algorismus Resolutor_.
No importa el problema, el contexto ni los involucrados: se dice que este algoritmo es capaz de adaptarse a cualquier situación y resolverla de manera eficiente y eficaz.

Muchos guerreros algorítmicos han intentado alcanzar este anhelado tesoro, pero ninguno ha logrado superar todas las pruebas del Santuario Algorismi. Algunos dicen que fallan porque no razonan ni analizan el problema frente a ellos, que se lanzan sin planificación o toman decisiones apresuradas sin considerar las condiciones del entorno.

La leyenda indica que solo aquel guerrero que desarrolle ciertas habilidades muy especiales será digno de hallar el _Algorismus Resolutor_:

I. Gran capacidad de razonamiento lógico.
II. Planificación ordenada de sus acciones".
III. Toma de decisiones precisas, evaluando los posibles caminos..
IV. Tenacidad para repetir acciones las veces que sea necesario, conociendo o no su fin.
V. Administración y uso de los suministros y objetos del viaje.
VI. Definición de planes de acción para distintas situaciones.

Y lo más importante, el guerrero deberá tener presente las tres sagradas reglas de la Algoritmia:

I. **Finitud** de acciones a realizar
II. **Precisión** en cada acción sin ambiguedad y con exactitud.
III. **Definición** de comportamiento para producir los mismos resultados en diferentes situaciones.

Movido por esta leyenda, un/una joven guerrero/a algorítmico/a novato/a —pero con una gran determinación- decide emprender su viaje hacia el _Santuario Algorismi_, con la esperanza de alcanzar el _Algorismus Resolutor_.
A lo largo del camino, deberá superar pruebas difíciles, adquirir conocimientos y habilidades en el arte de la algoritmia, enfrentar obstáculos, combatir enemigos, recolectar objetos clave y perfeccionar estrategias que lo acerquen, paso a paso, a su objetivo."

### 5.2 Mundo

El mundo ficticio de Algoritmia se dividirá en 8 capítulos temáticos que el jugador deberá atravesar para llegar al _Santuario Algorismi_. Cada capítulo tendrá una serie de misiones tutorial, donde se presentarán las primitivas básicas o desbloqueadas y misiones normales que el jugador deberá completar. En las misiones tutorial no se aplicará feedback formativo, ya que son misiones de tutorial, en las misiones normales si se aplicará feedback.

#### Capítulo 1: El llamado de Algorismus Resolutor

**Descripción**
En este capítulo se desarrolla el inicio de la historia. Se presentarán de manera introductoria las primeras primitivas junto con la lógica proposicional y estructuras de control (condicionales y bucles).

**Temas referenciados**

- Secuencia de pasos
- Lógica proposicional
- Estructuras de control:
  - Decisiva: Si-Sino
  - Repetitiva: Repetir
  - Iterativa: Mientras

**Desbloqueables**
**Primitivas**

- mover: disponible desde el inicio, es el movimiento básico del jugador.
- recogerMoneda: le permite al jugador recoger monedas en la posición actual.
- saltar: le permite al jugador realizar un salto que "omite" una celda.

**Estructuras de control**

- **Emblema del Juicio**: le da el poder al jugador de tomar decisiones evaluando sus objetos y elementos del entorno.
- **Ritual de la Perseverancia**: le da el poder al jugador de repertir una serie de acciones un número (definido por el jugador) finito de veces.
- **Orbe del Ciclo Infinito**: le da el poder al jugador de ejecutar una serie de acciones basadas en una condición. Es una herramienta poderosa pero tambien se debe tener cuidado en la elección de la condición para evitar una secuencia infinita!

**Lista de misiones**

- M1: Introducción a la primitiva `mover`
- M2: Introducción a la primitiva `recogerMoneda`
- M3: Introducción a los `obstáculos`
  - Se desbloquea la primitiva `saltar`.
  - Al finalizar se desbloquea el `Emblema del Juicio`
- M4: Introducción a las proposiciones y toma de decisiones
  - Se desbloquean las proposiciones `hayFosa` y `hayMoneda`
  - Se desbloquea la estructura de control `Si` y se presenta su uso con proposiciones simples.
- M5: Introducción a la estructura de control `Si-Sino`
- M6: Introducción a los conectivos lógicos y proposiciones compuestas
  - Se desbloquean los conectivos lógicos: `AND` `OR` y `NOT`
  - Se presenta el uso de estructura de control `Si-Sino` con proposiciones compuestas.
- M7 a M9: Misiones normales solo con lo desbloqueado hasta el momento.
  - En la M9 desbloqueo del `Ritual de la Perseverancia`.
- M10: Introducción a la estructura `Repetir N`.
- M11 a M13: Misiones normales solo con lo desbloqueado hasta el momento.
  - En la M13 desbloqueo del `Orbe del Ciclo Infinito`.
- M14: Introducción a la estructura `Mientras` con proposiciones simples.
- M15: Se presenta el uso del `Mientras` con proposiciones compuestas.
- M16: Tip y estructura para evaluar por cual condición se "corta" el `Mientras`.
- M17 a la M20: Misiones normales con todo lo aprendido hasta ahora.

#### Capítulo 2: El Valle de las Decisiones

**Descripción**
En este capítulo se pondran a prueba todo lo aprendido hasta el momento, con nuevas misiones con más dificultad y nuevas primitivas y objetos desbloqueables.

**Temas referenciados**
Todos los del capítulo 1.

**Lista de misiones**

- M21 a la M25: misiones normales
- M26: Introducción a los `enemigos`.
  - Se desbloquea la proposición `hayEnemigo`.
  - Se desbloquea la primitiva `atacar`.
- M27 a M32: misiones normales
- M33 a M35: misiones de mayor dificultad

#### Capítulo 3: Laberinto del Flujo

**Descripción**
En este capítulo tambien se tendrán nuevas misiones con más dificultad. No se desbloqueará ninguna primitiva u objeto.

**Temas referenciados**
Los mismos del capitulo 1.

**Lista de misiones**

- M36 a M49 misiones normales alternando dificultad.

#### Capítulo 4: El Origen del Almacenamiento

**Descripción**
**Temas referenciados**

**Lista de misiones**

#### Capítulo 5: Las Ruinas del Recuerdo

**Descripción**
**Temas referenciados**

**Lista de misiones**

#### Capítulo 6: El Legado de Modularius

**Descripción**
**Temas referenciados**

**Lista de misiones**

#### Capítulo 7: La Prueba del Guardián de Algorismi

**Descripción**
**Temas referenciados**

**Lista de misiones**

#### Capítulo Final - El Santuario Algorismi

**Nombre**
**Descripción**

**Cantidad de misiones**

- Misiones tutorial:
- Misiones normales:

### 5.2 Personajes

#### 5.2.1 Protagonista

#### 5.2.2 Enemigos

## 6. Gameplay y elementos del juego

### 6.2 Misiones o niveles

### 6.3 Objetos a encontrar/recolectar/etc.

### 6.4 Enemigos y obstáculos

### 6.5 Mecánicas del personaje

Definir las mecánicas y habilidades del personaje, comportamiento durante el gameplay, como y cuando se desbloquean, su uso, etc. Primitivas, etc.

### 6.X PGAScript

El pseudocódigo gamificado _PGAScript_ está diseñado para enseñar pensamiento algorítmico de manera progresiva y accesible. Su sintaxis simple y visual con colores e íconos representativos permite al jugador resolver misiones mediante primitivas, estructuras de control básicas, manejo de variables y procedimientos que se irán desbloqueando a medida que se avanza en la historia.

#### 6.X.1 Propósito educativo

PGAScript está pensado para:

- Introducir a los alumnos en la lógica algorítmica y estructuras de control básicas.
- Fomentar el diseño de soluciones generales (no específicas).
- Reforzar conceptos como secuenciación, repetición, condicionales, procedimientos, parámetros y reutilización.

#### 6.X.2 Sintaxis general

- Se escribe en formato pseudocódigo adaptado.
- Cada línea representa una instrucción o bloque lógico.
- El pseudocodigo es sensible a la estructura (usa indentación).
- La primer linea del código es "Inicio" y la última línea "Fin" para indicar el inicio y el fin del código.

#### 6.X.3 Primitivas

Estas son las instrucciones básicas (primitivas) del jugador disponibles en el lenguaje:

| Primitiva       | Descripción                                                                                       |
| --------------- | ------------------------------------------------------------------------------------------------- |
| `avanzar`       | El jugador avanza a la siguiente celda en la dirección actual                                     |
| `saltar`        | El jugador salta hacia adelante (en la dirección actual) omitiendo una celda                      |
| `atacar`        | El jugador ataca al enemigo en la celda frente a la posición actual                               |
| `derecha`       | El jugador hace un giro de 90° a la derecha                                                       |
| `recogerMoneda` | El jugador recoge, si existe, la moneda en la celda actual y suma +1 a las monedas de inventario. |

|

#### 6.X.4 Variables de juego y objetos de inventario

Las variables de juego son las variables relacionadas a los distintos elementos presentes en el escenario de juego que podrán ser evaluados solamente. Los objetos de inventario, de igual manera, podrán estar en el escenario y ser evaluados, utilizadas son los objetos que se pueden acumular en el inventario del jugador.

| Variable     | Descripción                                                                                                               |
| ------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `hayMoneda`  | Evalúa si existe una moneda en la celda actual, retorna verdadero o falso                                                 |
| `hayLlave`   | Evalúa si existe una llave en la celda actual, retorna verdadero o falso                                                  |
| `hayEnemigo` | Evalúa si hay un enemigo en la siguiente celda desde la posición y dirección actual, retorna verdadero o falso            |
| `hayFosa`    | Evalúa si hay una fosa (pozo, hoyo) en la siguiente celda desde la posición y dirección actual, retorna verdadero o falso |
| `dimX`       | Devuelve el valor de la posición actual en el eje X del escenario                                                         |
| `dimY`       | Devuelve el valor de la posición actual en el eje Y del escenario                                                         |

## 7. Estilo visual y arte

### 7.1 Interfaz de usuario

#### 7.1.1 Diseño de menús

Menú principal, pausa, ajustes, selector de misiones, Pre-misión, In-misión, Post-misión, estadisticas personales,

#### 7.1.2 Diagrama de flujo

Flujo principal desde que se inicia el juego hasta obtener el feedback de una misión.

### 7.2 Assets (recursos artísticos)

Describir los assets necesarios (avatares, personajes, etc.) junto a una breve descripción de cada uno.

#### 7.2.1 Personajes

#### 7.2.2 Entorno

#### 7.2.3 Objetos

## 8. Diseño de misiones

### 8.2 Misiones

#### Capítulo 1 - **nombre**

##### Mision X

Datos de la misión: enunciado, descripción, objetivo, etc.

## 9. Música y audio

REVISAR: https://www.youtube.com/@Gretian -> Para crear música para videojuegos

- (+) Suma
- (-) Resta
- (\*) Multiplicación
- (/) División
- (mod) Módulo (resto de una división)
- (<) Menor qué
- (>) Mayor qué
- (<=) Menos o igual qué
- (>=) Mayor o igual qué
- (==) Igual qué
- (!=) Distinto qué
