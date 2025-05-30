# Documento de Visión

**Versión:** 1.2
**Fecha:** 29/05/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Introducción

### 1.1 Propósito  
El proposito de este documento es proporcionar la información necesaria del proyecto a desarrollar. En este documento se podrá encontrar el contexto del negocio, los problemas o necesidades a abordar y el impacto que tendrá el desarrollo del software, asi como también la visión del producto explicada en objetivos y alcance del mismo.

---

## 2. Contexto de Negocio

### 2.1 Descripción del negocio

El desarrollo de este proyecto se sitúa en la Facultad de Ciencias Exactas, Químicas y Naturales (Módulo Apóstoles) de la Universidad Nacional de Misiones donde se dictan las carreras de informática: Analista en Sistemas de Computación (Pregrado, 3 años), Profesorado Universitario en Computación (Grado, 4 años) y Licenciatura en Sistemas de Información (Grado, 5 años).

En el plan de estudio de cada una de las carreras se encuentra la materia principal e introductora a los conceptos base para progresar en la carrera, la cual es sumamente importante: "Algoritmos y Estructuras de Datos I". La materia es anual, es decir que se dicta duante el primer cuatrimestre y segundo cuatrimestre del año lectivo.

El contenido de la materia se divide en los siguientes temas:
- Algoritmos y Secuencia
- Lógica proposicional
  - Operador lógico Y (AND)
  - Operador lógico O (OR)
  - Operador lógico NO (NOT)
  - Tablas de verdad
- Estructuras de control
  - Si - Sino (if-else)
  - Repetir
  - Mientras (while)
- Variables (enteros, caracteres, reales, ...)
  - Declaración y asignación
  - Variables globales
  - Variables locales
- Procedimientos
  - Con o sin parámetros de E/S
- Funciones
  - Con o sin parámetros de E/S
- Estructuras de datos
  - Cadena de caracteres (String)
  - Vectores y matrices (Arrays)
  - Registros (Record)
  - Archivos (Files)

Las clases se dividen en teoría y práctica y los días y horarios son los siguientes (al momento de la redacción de este documento):
- La **teoría** se dictan los Lunes de 10:00 AM a 12:00 PM. En la teoría se presenta mediante diapositivas el contenido teórico y fundamental del tema de la semana. Dicho contenido, luego de la clase, queda disponible en el aula virtual para que los alumnos puedan consultarlo en cualquier momento.
- La **práctica** se dictan los días lunes de 17:00 PM a 19:00 PM, miércoles de 10:30 AM a 12:30 PM. En las clases de práctica se llevan a cabo la presentación y resolución de los ejercicios y trabajos prácticos sobre los contenidos teóricos dados el día lunes.
- Adicionalmente, se tiene una clase de **consulta** los días jueves de 19:00 PM a 20:00 PM. La clase de consulta sirve para que los alumnos puedan, si asi lo requieren, llevar sus dudas inconclusas acerca de los temas o ejercicios y pedir una revisión de los ejercicios ya resueltos para obtener retroalimentación de los docentes.

Esta materia es la más importante al momento de ingresar a las carreras de informática, ya que su contenido es fundamental e indispensable para el avance de la carrera por su contenido y correlatividad. Por lo tanto, la cátedra busca garantizar que todos los alumnos puedan aprender de manera adecuada y poseer conocimientos sólidos y afianzados de los contenidos tanto teóricos como prácticos.

### 2.2 Problema o necesidad
Actualmente en la cátedra, las prácticas de los temas que van desde algoritmos hasta prodecimientos y funciones se llevan a cabo y se enfocan en el programa llamado "Visual DaVinci", el cual tiene como escenario a un robot que recorre una ciudad juntando flores y papeles en las esquinas de la misma. La ciudad está representada como una matriz de 100x100 y la misma tiene calles (filas), avenidas (columnas) y esquinas (intersección de una calle y una avenida).

Este programa ya se viene implementando hace muchos años en la cátedra, aproximadamente desde 1998, siendo que el programa salió en 1997. Permite realizar edición de codigo con una serie de instrucciones disponibles. El alumno puede diseñar un algoritmo para resolver distintos problemas y al momento de ejecutar se tiene un visor simulado la ciudad con cuadros azules, el robot con un punto rojo y negro, flores con un circulo rojo con centro amarillo y papeles con circulos blancos. Algunas de las instrucciones disponibles son:
- mover: el robot avanza a la siguiente esquina
- derecha: el robot gira a la derecha
- tomarFlor: el robot toma una flor en la esquina
- tomarPapel: el robot toma un papel en la esquina
- HayFlorEnLaEsquina: el robot se pregunta si existe una flor en la esquina en la que está posicionado actualmente.
- HayPapelEnLaEsquina: el robot se pregunta si existe un papel en la esquina en la que está posicionado actualmente.
- Pos(x, y): el robot salta se posiciona en la calle "x" y en la avenida "y".
- Entre otras...

![Ejemplo del area de trabajo de Visual DaVinci](imagenes/ejemploDaVinci.png "Ejemplo del area de trabajo de Visual DaVinci")
Ejemplo del area de trabajo de Visual DaVinci.
Video Youtube: Visual DaVinci - Capítulo 2: Estructura si - ChamanDEV

Los principales problemas que se encuentran en esta plataforma es que el programa no brinda ningún tipo de sugerencia o dinámica de aprendizaje según el código que ejecutemos, sino que se limita solamente a la prueba del mismo. No evalúa indentación, repetición de primitivas o secuencia ineficiente, no ofrece ningún tipo de feedback para mejorar la solución propuesta. Además, debido a la antigüedad del sistema, su interfaz con componentes en su mayoría grises y pocos colores se quedó muy atrás y no resulta atractiva.

Aparte del programa, otro problema relacionado a la cátedra es que tienen problemas para llevar a cabo el **seguimiento** de los alumnos en cuanto a su nivel de aprendizaje y la toma de decisiones al respecto. Los docentes indican que “El seguimiento está en su cabeza”, es decir, no tienen una forma de llevar el seguimiento o progreso del alumno en su aprendizaje y conocimientos. Esto es otra cosa que el programa actual no permite, no se evidencia el progreso del alumno en el uso ni conocimientos aprendidos a lo largo del tiempo, no tiene dificultad progresiva ni presenta grandes desafios de mejora para el alumno.

Al ser la primera materia de la carrera, cada año se tiene una gran cantidad de alumnos cursando y llegado un punto del año se torna imposible para los docentes llevar un seguimiento y brindar apoyo adicional a aquellos alumnos que quedaron atrasados en los contenidos y que no lograron afianzar conocimientos.
Por otro lado, cada alumno que ingresa a la carrera tiene una personalidad diferente. Aquellos que son más introvertidos o con poca confianza, si se llegan a atrasar, les cuesta mucho tomar la iniciativa para solicitar apoyo de los docentes.

En resumen, los problemas específicos identificados son:

1. Baja motivación
   - Interfaz anticuada (tonos grises, componentes básicos) que no despierta interés.
   - Ausencia de alguna narrativa que enganche al estudiante.

2. Repetitividad
   - Flujos y primitivas siempre iguales, sin novedades que mantengan vivo el desafío.
   - Falta de progresión de dificultad estructurada.

3. Falta de feedback formativo.
   - Solo valida si el código funciona o no; no sugiere optimizaciones, mejoras de indentación o patrones eficientes.
   - No muestra métricas de calidad de código (reutilización de primitivas, complejidad cíclica).

4. Carencia de seguimiento académico.  
   - Los docentes “llevan el seguimiento en la cabeza”: no existe registro centralizado de avances ni estadísticas de desempeño por alumno.
   - Imposible detectar a tiempo qué alumnos quedan rezagados o necesitan apoyo adicional.

5. Barreras de colaboración.
   - Estudiantes introvertidos o con baja confianza quedan aislados, al no existir mecanismos de colaboración.

### 2.3 Oportunidad e impacto

Teniendo en cuenta la situación actual y la problemática, se realizará una propuesta de solución: el desarrollo de una plataforma de aprendizaje denominada "Plataforma Gamificada 'Algoritmia' (PGA)", que permitirá a los alumnos aprender algoritmos, lógica y estructuras de control y para los docentes permitirá el seguimiento académico exhaustivo de cada uno de los alumnos.
La plataforma incorporará y se enfocará el concepto de “Gamificación” y lucirá una estética visual de “Pixel Art”.

#### La gamificación
El concepto de "gamificación" se refiere a la aplicación de narrativa, mecánicas y elementos propios de los videojuegos (como niveles, experiencia, puntos, logros, desafíos, tablas de clasificación y recompensas) en contextos no lúdicos, como la educación y el trabajo.
Aumenta la motivación, participación y mejora la experiencia de aprendizaje haciendo que las personas sientan que están jugando. Esta técnica se utiliza para hacer que las actividades sean más interesantes, atractivas y divertidas aumentando el compromiso de los participantes. Algunos de los beneficios más importantes de la gamificación, según especialistas, son:
- **Incrementa la motivación**: potencia la predisposición del alumno a aprender y genera menor rechazo comparándolo con el estudio tradicional.
- **Brinda diferentes niveles de dificultad**: a medida que se avanza y completa los desafíos, éstos se vuelven cada vez más complejos.
- **Mejora la lógica y las estrategias para la resolución de problemas**: los estudiantes deberán utilizar el pensamiento lógico para resolver el problema que tienen delante con las herramientas disponibles.
- **Aumenta la atención y la concentración**: para los alumnos será como estar jugando un videojuego, y por ello se esforzarán, aumentará su motivación y comprenderán bien los contenidos.
- **Incrementa el rendimiento académico**: al entender los conceptos correctamente y estar motivado, hay altas probabilidades de que el alumno pueda aprobar sus exámenes con éxito.

#### Pixel Art
El pixel art es un estilo artístico digital utilizado para crear imágenes con píxeles individuales para formar un mosaico visual. Este estilo es reconocido por su estética retro y la conexión que tiene con los videojuegos clásicos, en donde la resolución y recursos eran limitados. Algunas de sus características son:
- **Creación pixel a pixe**l: se centra en crear imágenes colocando un color en cada píxel individual. Es un estilo muy artesanal con el cual se pueden lograr resultados muy detallados pero con componentes simples.
- **Estilo retro**: el pixel art nos recuerda a los primeros videojuegos y computadoras, con paleta de colores limitada y gráficos de baja resolución.
- **Influencia en los videojuegos**: es un estilo popular en el diseño de videojuegos, donde se utiliza para crear sprites, personajes, entornos y gráficos de interfaz de usuario.


El desarrollo de este sistema ofrece varias oportunidades tanto a alumnos como a docentes.

**Para alumnos**:
- Podrán aprender y practicar acerca de los contenidos dados en la materia mediante la resolución de ejercicios y ejecución del mismo mediante un escenario de videojuego con estética visual Pixel Art, estusiasmando y enganchando al alumno durante sus prácticas.
- Mediante gamificación, los alumnos podrán ganar experiencia, subir de nivel y desbloquear más misiones o habilidades manteniendo la participación y motivación en utilizar el sistema.
- El sistema detectará los errores cometidos, evaluará métricas de código y propondrá mejoras a la solución, todo a modo de feedback formativo para que el alumno pueda mejorar constantemente sus soluciones futuras.

**Para docentes**:
- Podrán contar con un seguimiento académico exhaustivo de todos sus alumnos.
- Ver las estadisticas, rendimiento semanal, porcentaje de avance en los temas de cada alumno.
- Detectar a aquellos alumnos rezagados o con bajo rendimiento en los contenidos para la toma de decisiones.

Con el desarrollo del sistema se esperan los siguientes beneficios a corto plazo:
1. **Alumnos motivados**: se espera que los alumnos se sientan enganchados y atraídos con el entorno de videojuego con gamificación y estética pixel art.
2. **Seguimiento global e individual del grupo de alumnos**: el docente cada semana podrá revisar el estado de avance global e individual y la evolución de cada uno de los alumnos. Podrá detectar aquellos alumnos que quedaron atrasados y reforzar los contenidos en la siguiente clase si asi lo requiriese.
3. **Proceso de aprendizaje dinámico**: con las mejoras y feedback formativo que brindará el sistema, se espera que los alumnos puedan comprender y aprender los contenidos de manera rápida.

Los beneficios a largo plazo:
1. **Menos alumnos atrasados**: con el seguimiento academico y mejora constante, Se espera que se tome menos tiempo de cursada "oficial" para el refuerzo de los contenidos y que haya una menor cantidad de alumnos atrasados al momento de, por ejemplo, la toma de exámenes o al final de la cursada.
2. **Alumnos con conocimientos solidificado**s: mediante la resolución de ejercicios y feedback formativo constante, se espera que los alumnos cuenten con una base sólida en cada contenido dado en la plataforma y sean capaces de diseñar mejores soluciones a futuro.
3. **Plataforma oficial para el dictado en la cátedra**: se espera que a largo plazo el sistema quede consolidado como herramienta principal en el dictado de la cátedra reemplazando al Visual DaVinci, integrando la resolución de ejercicios y seguimiento académico de los alumnos en un solo lugar.

---

## 3. Visión general del producto

### 3.1 Perspectiva del producto

El desarrollo e implementación de este sistema encaja perfecamente en la situación y escenario actual debido a los siguientes puntos:
- **Facil adaptación**: el sistema seguirá con la dinámica de aprendizaje de edición de código y ejecución de la "prueba de escritorio" mediante un visor, con la principal diferencia que tendrá un contexto gamificado con visuales y componentes propios de los videojuegos.
- **Seguimiento docente**: los docentes carecen de un seguimiendo académico exhaustivo de cada uno de los alumnos. La incorporación del seguimiento académico mediante el sistema hará que los docentes tengan una mejor visión del estado de avance tanto del grupo de alumnos como cada uno individualmente.
- **Producto propio de la FCEQyN**: el Visual Da Vinci es un proyecto de Tesis de la Universidad Nacional de La Plata (UNLP). Entonces, al desarrollar e implementar un proyecto propio y desarrollado en la misma FCEQyN, engrandecerá el sentido de pertenencia e identidad de los docentes y alumnos.

### 3.2 Objetivos

#### 3.2.1 Objetivo General
Desarrollar la Plataforma Gamificada "Algoritmia" (PGA) para el aprendizaje de Lógica, Algoritmos y Estructuras de Control (PGA) con enfoque en la gamificación y estética visual en Pixel Art, que incremente la motivación, facilite la resolución de ejercicios y permita un seguimiento académico exhaustivo de los alumnos.

#### 3.2.2 Objetivos Específicos
1. Generar motivación en el estudiante con mecánicas y narrativa de videojuegos
   1. Diseñar e implementar una interfaz Pixel Art atractiva y con una narrativa interesante, de modo que el entorno se perciba como un videojuego.
   2. Integrar mecánicas de misiones, niveles, puntos de experiencia (EXP) y puntuación (en estrellas) para premiar el progreso y mantener el interés del usuario.

2. Ofrecer ejercicios de dificultad progresiva y desbloqueables.
   1. Crear un repertorio de ejercicios (misiones) que cubran los temas de: algoritmos, lógica, estructuras de control (condicionales y bucles), variables, procedimientos y funciones.
   2. Implementar un sistema de desbloqueo de nuevos retos conforme el alumno avance, garantizando una curva de aprendizaje controlada.

3. Proveer feedback formativo inmediato
   1. Analizar automáticamente la solución del alumno y generar sugerencias de optimización, tales como correcciones de indentación, reducción de primitivas redundantes y simplificación de estructuras.
   2. Mostrar métricas de calidad de la solución tras cada envío para reforzar la reflexión sobre buenas prácticas.
  
4. Ofrecer seguimiento académico exhaustivo con tableros de progreso y alertas.
   1. Desarrollar un tablero de progreso y reportes para docentes que muestre el avance y rendimiento individual y grupal de los alumnos (nivel actual, cantidad de ejercicios completados, estrellas obtenidas, promedio de intentos por ejercicio, porcentaje de avance en temas específicos y avance global, ultima conexión) pudiendo así identificar a los alumnos atrasados y con poca actividad en la plataforma.
   2. Configurar alertas automáticas periódicas para el docente cuando un alumno o grupo de alumnos supere un umbral de atraso en contenidos o se detecte inactividad prolongada.
   3. Configuración de reportes automáticos semanales para que el docente pueda visualizar el tablero de progreso y rendimiento semanal de los alumnos de forma individual y grupal.

5. Programar sesiones de refuerzo de contenido automáticas
   1. Implementar un sistema que detecte a los alumnos con menor progreso y, de forma automática, sugiera al docente conformar un grupo de refuerzo; el docente podrá confirmar la sesión adicional en la siguiente clase presencial y los alumnos indicarán su disponibilidad.

### 3.3 Modulos del sistema
#### 3.3.1 Funcionales
- Gestión de usuarios
- Banco de ejercicios
- Gamificación
- Programación, ejecución y feedback
- Gestión Docente
#### 3.3.2 No Funcionales
- Seguridad y autenticación
- Auditoría

### 3.4 Alcance y Limitaciones

#### 3.4.1 Gestión de usuarios
#### 3.4.2 Banco de ejercicios
Para el desarrollo del sistema, en una primera versión, NO se tomarán todos los temas de la materia, debido al tiempo de desarrollo disponible para el mismo. Por recomendación y solicitud de los profesores, los conceptos más importantes que si o si se deben afianzar y solidificar:
- Algoritmos y secuencia de pasos
- Lógica proposicional (Operadores lógicos: OR, AND, NOT)
- Estructuras de control (Si-Sino, Mientras y Repetir)

Adicionalmente, también se abordará los conceptos de:
- Variables (globales y locales)
- Procedimientos con y sin parámetros de E/S
- Funciones con y sin parámetros de E/S

#### 3.4.3 Programación, ejecución y feedback
#### 3.4.4 Gamificación
Para crear el entorno basado en gamificación, se tendrán en cuenta los siguientes apartados
##### Componentes
Se incorporarán varios componentes de videojuegos, explicando primero su significado propio de los videojuegos y luego lo que representarán, análogamente, del dominio del problema.

Los componentes de gamificación a incorporar en el sistema son los siguientes:
- Misiones (ejercicios): una misión es una tarea la cual tiene que ser resuelta por un personaje jugador, o un grupo de estos, para conseguir una determinada recompensa. Estas misiones representarán los ejercicios a resolver de los contenidos dados, las cuales tendrán un nivel de dificultad determinado entre: Fácil, Medio o Difícil.
  
- Acciones, habilidades y objetos: una acción es algo que el jugador puede hacer, como moverse o girar, una habilidad es una capacidad especial que tiene el jugador y un objeto es un elemento que puede ser recolectado, utilizado, equipado o interactuado por el jugador. Las acciones representarán las primitivas que puede realizar el jugador, como moverse, las habilidades especiales representarán a las estructuras de control, procedimientos y funciones y los objetos representarán las variables.
Primero se comenzará con un abanico limitado de acciones básicas para resolver los primeros ejercicios, luego al avanzar más en la historia se irán desbloqueando habilidades y objetos.

- Niveles (progreso): en los videojuegos, los niveles sirven para representar el progreso y la experiencia de un personaje, así como para desbloquear nuevas habilidades y mejoras. Subir de nivel significa que el personaje se vuelve más poderoso y capaz de enfrentar desafíos más grandes. Para el desarrollo del sistema, se utilizarán los niveles para desbloquear nuevas misiones, acciones, habilidades y objetos.
  
- Puntos de experiencia (XP): los puntos de experiencia (XP o EXP) son una medida de progreso y nivel de habilidad. Los puntos de experiencia se obtendrán y se acumulan al realizar ejercicios y permitirán al jugador subir de nivel.
  
- Puntuación en estrellas (evaluación): la puntuación en estrellas es un sistema de evaluación que utiliza estrellas para indicar el nivel de desempeño de un jugador al resolver una tarea o desafío, en este caso, una misión (ejercicio), siendo 3 estrellas la puntuación más alta, 2 estrellas puntuación media y 1 estrella la puntuación más baja.

#### 3.4.5 Feedback formativo
El sistema ofrecerá tres tipos de feedback formativo durante la resolución de un ejercicio: previo a la ejecución, al momento de ejecutar y posterior a la ejecución. A continuación, detallaremos los aspectos que el sistema analizará y ofrecerá retroalimentación al alumno.

- Previo a la ejecución: el sistema estará analizando en tiempo real la estructura y forma de escribir de la solución del alumno para poder indicar errores y sugerencias.
- Al momento de ejecutar: si la solución posee errores (de sintaxis u otro tipo) el sistema no permitirá la ejecución de la misma e indicará donde se encuentra el error para que el alumno pueda corregirla. Si la solución tiene sugerencias (como variables declaradas pero no utilizadas) el sistema permitirá la ejecución de la misma igualmente.
- Posterior a la ejecución: el sistema analizará la solución del alumno y ofrecerá retroalimentación a modo de sugerencias y optimizaciones de la solución.

Detallaremos las sugerencias y optimizaciones específicas que el sistema ofrecerá en cada tipo de feeback

##### Previo a la ejecución
Mientras el alumno diseña su solución para un ejercicio, el sistema estará analizando y controlando en tiempo real la estructura y sintaxis de la misma para poder indicar errores y sugerencias antes de ejecutar la solución. La siguiente tabla muestra los "problemas" a analizar previo a la ejecución de la solución y el feedback correspondiente.

| Problema                                           | Descripción                                                                                  | Feedback                                                                                    |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Errores de sintaxis                                | Instrucciones o estructuras mal escritas                                                     | Resaltado en rojo en la instrucción o estructura mal escrita.                               |
| Variable no declarada                              | Cuando se quiere utilizar una variable (globales o locales) que no fue declarada previamente | Resaltado en rojo en donde se quiere utilizar la variable con un mensaje de "no declarada"  |
| Variable declarada pero no utilizada               | Cuando se declara una variable pero nunca se utiliza                                         | Resaltado en amarillo en la variable declarada pero no utilizada                            |
| Procedimiento o función definida pero no utilizada | Cuando se define un procedimiento o función pero nunca se utiliza                            | Resaltado en amarillo en la cabecera del procedimiento o funcion definida pero no utilizada |

##### Al momento de ejecutar
Cuando el alumno terminó de diseñar su solución y decida ejecutar, el sistema verificará que la estructura y sintaxis esté correctamente escrita para ejecutar. La siguiente tabla muestra los "problemas" a analizar al momento de ejecutar la solución y el feedback correspondiente.

| Problema                                           | Descripción                                                                                              | Feedback                                                                                                                        | ¿Es posible ejecutar la solución? |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| Error de sintaxis                                  | Instrucciones o estructuras mal escritas                                                                 | Mensaje de error en la ejecución y resaltado en rojo en la instrucción o estructura mal escrita.                                | No                                |
| Variable no declarada                              | Cuando se quiere ejecutar la solución pero se quiere utilizar una variable (global o local) no declarada | Mensaje de error en la ejecución y resaltado en rojo en la variable no declarada                                                | No                                |
| Variable decladara pero no utilizada               | Cuando se declara una variable (global o local) pero nunca se utiliza                                    | Mensaje de advertencia de variables declaradas pero no utilizadas con opción de ejecutar la solución igualmente                 | Si                                |
| Procedimiento o función definida pero no utilizada | Cuando se define un procedimiento o función pero nunca se utiliza                                        | Mensaje de advertencia de procedimientos o funciones definidas pero no utilizadas con opción de ejecutar la solución igualmente | Si                                |

##### Posterior a la ejecución
Luego de la ejecución de la solución del alumno, completado el ejercicio y dada la puntuación obtenida, el sistema analizará la solución proponiendo mejoras y optimizaciones para la solución. El sistema mostrará el antes y después de la solución del alumno y una breve explicación de los cambios realizados y el por qué.
El alumno decidirá si implementar o no las sugerencias y optimizaciones brindadas por el sistema o dejar la solución como está. Si decide implementar las optimizaciones, esto no aumentará la puntuación ni experiencia obtenida, debido a que esta funcionalidad del sistema es a modo formativo y para evitar aprovechamientos.
La siguiente tabla muestra los "problemas" a analizar posterior a la ejecución de la solución y el feedback correspondiente.

| Problema                                      | Descripción                                                                                                                                                                   | Feedback                                                                                                                                         |
| --------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Secuencia de múltiples instrucciones iguales  | Cuando se utiliza una misma instrucción multiples veces una debajo de otra de manera innecesaria (con un como mínimo de 3 instrucciones)                                      | Reemplazar el conjunto de multiples instrucciones por una estructura repetitiva (mientras o repetir) para reducir el uso del procesador          |
| Secuencia de múltiples estructuras de control | Cuando se utiliza una misma estructura de control multiples veces una dentro de otra o una debajo de la otra de manera innecesaria (con un mínimo de 3 estructuras de contro) | Identificar aquellas estructuras de control innecesarias, refactorizar y reordenar la estructuras de control para reducir la complejidad cíclica |
| Variables declaradas y no utilizadas          | Cuando se declara una variable (global o local) pero nunca se utiliza                                                                                                         | Eliminar la variable no utilizada para ahorrar espacio en memoria                                                                                |
| 


#### 3.4.6 Gestion Docente
En este módulo del sistema, los docentes tendrán diferentes funcionalidades para realizar el seguimiento a sus alumnos.

**Creación de cursos**
El docente podrá crear un curso para agrupar los dinstintos grupos de alumnos de las distintas instituciones de las cuales da clases. Podrá especificar el nombre del curso, institución, materia y definir una contraseña para permitirle a sus alumnos ingresar al curso.

**Definición de días y horarios de cursada**
Los docentes podrán configurar los días y horarios de cursada de la materia. Esto le servirá al sistema para luego realizar las sesiones de refuerzo automáticas.

**Visualización del estado de avance de los alumnos**
Los docentes podrán consultar el estado de avance de los diferentes cursos que tenga a cargo. Podrá visualizar el estado de avance del curso en general y de forma individual por alumno. Los datos que podrá visualizar son los siguientes:
- Porcentaje de avance del curso en la historia (programa total)
- Porcentaje de avance del curso en cada tema
- Estadisticas del alumno
  - Nombre completo
  - Nivel actual
  - Misión actual
  - Cantidad de misiones completadas hasta el momento
  - Cantidad de estrellas obtenidas hasta el momento
  - Promedio de intentos por misión
  - Porcentaje de avance individual en la historia
  - Porcentaje de avance individual en un tema
  - Ultimo ingreso a la plataforma.

Todos estos datos se podrán ordenar de manera ascendente o descendente en la vista. Tambien se podrán aplicar los siguientes filtros de búsqueda:
- Por fechas (desde - hasta)
- Por tema
- 

**Creación de sesiones de refuerzo**: los docentes podrán crear sesiones de refuerzo eligiendo a los alumnos que ellos consideren atrasados en los contenidos o con inactividad prolongada, elegir el día y horario de la sesión de refuerzo.

#### 3.4.7 Seguridad y autenticación
#### 3.4.8 Auditoría


### 3.5 Excluye
- Personalización de ejercicios por usuario.  
- Soporte multi‑idioma.
- Foros o chat interno.
- Estructuras de datos avanzadas (strings, matrices, archivos).

---

## 4. Stakeholders

| Stakeholder                   | Papel o interés                                 |
| ----------------------------- | ----------------------------------------------- |
| Profesores Tutores            | Consultores, validación académica y supervisión |
| Alumnos y Docentes / Usuarios | Uso y evaluación de la plataforma               |

---

## 5. Supuestos y Restricciones
- Debe validarse con 20 usuarios antes del 15/11/2025.  
- Versión local solo para demostración; despliegue en nube queda fuera  
  de la versión inicial.