# Game Design Document

**Versión:** 1.0
**Fecha:** 18/06/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Título

El título del juego será "Algoritmia".

## 2. Resumen del juego

Algoritmia es un juego en donde aprenderás algoritmos, lógica y estructuras de control resolviendo problemas codificando y visualizando tu propia solución. Deberás enfrentarte a desafíos, recolectar y usar objetos, luchar contra enemigos y evitar obstáculos mediante el diseño de tu propio algoritmo para completar la misión a tu manera y aprendiendo en el proceso.

## 3. Concepto y pilares de diseño

La escencia del videojuego y lo que quiero transmitir se basan en estos 3 pilares:

### 3.1 Pixel Art

El pixel art es un estilo artístico de videojuegos. Es reconocido por su estética retro y la conexión que tiene con los videojuegos clásicos, en donde la resolución y recursos eran limitados. Se caracteriza por ser un estilo muy artesanal, donde cada diseño se realiza pixel por pixel logrando un estilo muy simple pero a la vez detallado, el cual resulta agradable a la vista.

Lo que Algoritmia quiere transmitir con su estilo visual es simpleza pero belleza a su vez mediante el pixel art en sus escenarios, interfaces, objetos y personajes utilizando colores llamativos, una paleta de colores adecuada a la estética y trama del videojuego y diseños minimalistas. Se busca transmitir esa sensación de estar jugando un videojuego pero aprendiendo a la vez.

### 3.2 Lenguaje gamificado y ejecución en tiempo real

Algoritmia tendrá un lenguaje de programación gamificado con acciones, tácticas, objetos y habilidades especiales que permitirán al jugador diseñar sus propias soluciones. Además, el jugador podrá visualizar en tiempo real la ejecución de su solución en el escenario de juego.

### 3.3 Aprendizaje continuo con feedback inmediato

Algoritma busca brindar aprendizaje continuo mediante feedback inmediato cuando el jugador esté diseñando su solución para un problema. La idea es que Algoritmia pueda analizar y ofrecer sugerencias y optimizaciones de la solución del jugador durante y después de su ejecución fomentando el aprendizaje continuo.

en base a lo siguiente:

- Errores de sintaxis.
- Redundancia de instrucciones.
- Redundancia de estructuras de control.
- Cantidad excesiva e innecesaria de lineas de código.
- Variables no utilizadas

Para ello, se ofrecerá:

- Indicador de error de sintaxis
- Sintaxis y semántica detallada del lenguaje gamificado.
- Autocompletado de estructuras de control.
- Reemplazar multiples instrucciones de un mismo tipo con una estructura repetitiva.
- Reemplazar multiples estructuras condicionales con una estructura condicional con proposición compuesta.
- Eliminar variables no utilizadas
- Entre otras.

## 4. Descripción del juego

Algoritmia es un videojuego de aventura estilo RPG que está enfocado en el aprendizaje de las bases de la programación: algoritmos, lógica, estructuras de control (condicionales y bucles) y procedimientos mediante la resolución de ejercicios, codificando y visualizando su solución en tiempo real.
El jugador tendrá que completar misiones divididas en capítulos temáticos donde en cada capitulo se enfocará en un concepto de las bases de la programación: algoritmos, lógica, estructuras de control, variables y procedimientos. En cada misión, el jugador deberá resolver un problema con reglas y condiciones específicas utilizando un lenguaje de programación gamificado diseñado con acciones, tácticas, objetos y habilidades especiales que permitirán al jugador diseñar sus propias soluciones para poder completar las misiones, visualizando en tiempo real la ejecución de la solución en el escenario diseñado como un tablero de N filas por N columnas.
Una característica importante de Algoritmia es que ofrece feedback formativo inmediato y ayudas al jugador para detectar y corregir errores de manera sencilla y optimizar la solución mediante sugerencias visualizando el antes y después.

### 4.1 Lenguaje gamificado

El lenguaje de programación gamificado tiene los siguientes elementos de la programación tradicional:

- **Acciones -> Primitivas o instrucciones**: las acciones representarán a las instrucciones o primitivas básicas que el jugador podrá realizar.
- **Tácticas -> Estructuras de control**: las tácticas representan las estructuras de control básicas: Si-Sino, Mientras y Repetir donde se podrán manejar proposiciones simples o compuestas utilizando operadores matemáticos básicos y operadores relacionales.
- **Objetos -> Variables**: los objetos representarán a las variables del juego. Se tendrán variables de juego (inventario y entorno) y variables globales y locales de tipo entero que el jugador podrá declarar y asignar valores en el diseño de la solución.
- **Habilidades especiales -> Procedimientos**: las habilidades especiales representarán a los procedimientos. Habrán procedimientos pre-diseñados desbloqueables y el jugador podrá crear los propios incluyendo o no parámetros de entrada, salida y entrada/salida.

### 4.2 Feedback formativo y ayudas

Las ayudas que se ofrecerán son las siguientes:

1. **Manual del heroe**: este manual contendrá todas las acciones, tácticas, objetos y habilidades especiales que el jugador puede utilizar para resolver la misión. El manual del heroe especificará la sintaxis, semántica y un ejemplo de la estructura básica de cada instrucción del lenguaje gamificado separada por Acciones, Tácticas, Objetos y habilidades especiales.
2. **Autocompletado**: Aparecerán como sugerencia las instrucciones y estructuras dependiendo de lo que escriba el jugador, dando la posibilidad de autocompletado seleccionando la opción deseada de las sugerencias. Esto aplicará para: primitivas, estructuras de control y procedimientos.
3. **Resaltado de sintaxis**: se resaltarán los errores de sintaxis y advertencias en color rojo y amarillo respectivamente.

En cuando al feedback formativo, se dará en tres etapas:
**1. Durante el diseño de la solución**:
Mientras el alumno diseña su solución para la misión, se estará analizando y controlando en tiempo real la estructura y sintaxis de la misma para poder indicar errores y sugerencias antes de pasar a la ejecución.

**Errores**
Los errores son aquellos que impiden que la ejecución de la solución se lleve a cabo. Los posibles errores a indicar son los siguientes:

| Error                  | Descripción                                                                               | Feedback                                                                                                                                                                                                     |
| ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Errores de sintaxis    | Se dan cuando hay instrucciones o estructuras mal escritas                                | Indicador rojo en el número de la linea del error y subrayado en rojo en la instrucción o estructura mal escrita. Si se apoya el cursor por encima del error se mostrará "Error de sintaxis".                |
| Variable no declarada  | Cuando se intenta utilizar una variable (global o local) que no fue declarada previamente | Indicador rojo en el número de la linea del error y subrayado en rojo en donde se quiere utilizar la variable. Si se apoya el cursor por encima del error se mostrará el mensaje de "Variable no declarada". |
| Parámetros indefinidos | Cuando se llama a un procedimiento y no se colocan los parámetros de manera correcta      | Indicador rojo en la linea del error y subrayado en rojo en el procedimiendo llamado. Si se apoya el cursor por encima del error se mostrará "Parámetros erróneos o indefinidos".                            |

**Advertencias**
Las advertencias son aquellas que no impiden que la solución se ejecute pero son recomendable de atender. Las posibles advertencias son las siguientes:

| Advertencia                              | Descripción                                             | Feedback                                                                                                                                                                                                                                                             |
| ---------------------------------------- | ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Variable declarada pero no utilizada     | Cuando se declara una variable pero nunca se utiliza    | Mientras el jugador no la utilice, indicador en amarillo en la línea de la advertencia y subrayado en amarillo en la variable declarada pero no utilizada. Si se apoya el cursor por encima de este aviso se mostrará "Variable no utilizada".                       |
| Procedimiento definido pero no utilizado | Cuando se define un procedimiento pero nunca se utiliza | Mientras el jugador no lo utilice, indicador en amarillo en la línea de la advertencia y subrayado en amarillo en la cabecera del procedimiento definido pero no utilizado. Si se apoya el cursor por encima de este aviso se mostrará "Procedimiento no utilizado". |

**2. Al intentar ejecutar**
Cuando el alumno terminó de diseñar su solución y decida ejecutar, el sistema verificará que la estructura y sintaxis esté correctamente escrita para ejecutar.
Si se ignoran todos los **errores** durante el diseño de la solución, no se podrá ejecutar la solución y se mostrará un mensaje indicando en rojo la linea donde se encuentra el error, el motivo y la sugerencia para corregirlo.

**3. Después de la ejecución de la solución indicando:**
Luego de la ejecución de la solución del alumno, completado el ejercicio y dada la puntuación obtenida, el sistema analizará la solución proponiendo mejoras y optimizaciones para la solución. El sistema mostrará el antes y después de la solución del alumno y una breve explicación de los cambios realizados y el por qué.

- **Redundancia de instrucciones**: si hay al menos 2 lineas de código llamando a la misma instrucción se sugerirá reemplazarlas por una estructura repetitiva como un mientras o un repetir.
- **Redundancia de condicionales**: si hay al menos 2 estructuras de control "Si" una debajo de la otra se sugerírá reemplazarlas por una estructura condicional con una proposición compuesta por las dos proposiciones originales utilizando un conectivo lógico apropiado.
- **Redundancia de bucles**: si hay al menos 2 estructuras de control "Mientras" o "Repetir" una debajo de la otra se sugerirá reemplazarlas por una estructura repetitiva con una proposición compuesta por las dos proposiciones originales utilizando un conectivo lógico apropiado.
- **Variables no utilizadas**: si hay variables declaradas pero no utilizadas se sugerirán eliminarlas de la solución.

### 4.3 Core Loop

El Core Loop principal del videojuego es:

1. Ingresar al mapa principal del juego
2. Seleccionar el capitulo actual
3. Seleccionar la siguiente misión
4. Diseñar un algoritmo para resolver la misión
5. Ejecutar la solución para visualizar la misma en el escenario
6. Recibir una puntuación y EXP correspondiente si se completa correctamente.
7. Recibir feedback formativo por parte del sistema para refactorizar si se quiere la solución.

## 5. Historia

### 5.1 Narrativa / Trama

### 5.2 Personajes

#### 5.2.1 Protagonista

#### 5.2.2 Enemigos

## 6. Gameplay y elementos del juego

### 6.1 Objetivos

### 6.2 Misiones o niveles

### 6.3 Objetos a encontrar/recolectar/etc.

### 6.4 Enemigos y obstáculos

### 6.5 Mecánicas del personaje

Definir las mecánicas y habilidades del personaje, comportamiento durante el gameplay, como y cuando se desbloquean, su uso, etc. Primitivas, etc.

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

### 8.1 Capítulos

Describir los capitulos de la historia. Tema referenciado. Incluir: nombre, breve descripción del capitulo, objetivo, cantidad de misiones, desbloqueo de habilidades/objetos/etc.

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
