# Documento de Visión

**Versión:** 2.0
**Fecha:** 29/07/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Introducción

### 1.1 Propósito

El proposito de este documento es proporcionar la información necesaria del proyecto a desarrollar. En este documento se podrá encontrar el contexto del negocio, los problemas o necesidades a abordar y el impacto que tendrá el desarrollo del software, asi como también la visión del producto explicada en objetivos y alcance del mismo.

### 1.2 Presentación general

El presente proyecto se trata del desarrollo de una plataforma de aprendizaje denominada "Plataforma Gamificada 'Algoritmia' (PGA)", que permitirá a los alumnos aprender algoritmos, lógica y estructuras de control incorporando “Gamificación” con mecánicas y componentes propios de los videojuegos para el aprendizaje y luciendo una estética visual de “Pixel Art”. Además, para los docentes permitirá el seguimiento académico exhaustivo de cada uno de los alumnos y el sistema podrá ser adaptado e incluido a cualquier institución educativa.

### 1.3 Participantes del proyecto

El equipo de desarrollo esta compuesto por el integrante Franco Andrés Albornoz, que cumple las funciones de gestor de proyecto, diseñador y desarrollador.
Participan también en el proyecto alumnos y docentes de la materia Algoritmos y Estructuras de Datos I.

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
  - Con o sin parámetros de entrada, salida y entrada/salida
- Funciones
  - Con o sin parámetros de entrada, salida y entrada/salida
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

Actualmente en la cátedra, las prácticas de los temas que van desde algoritmos hasta prodecimientos se llevan a cabo y se enfocan en el programa llamado "Visual DaVinci", el cual tiene como escenario a un robot que recorre una ciudad juntando flores y papeles en las esquinas de la misma. La ciudad está representada como una matriz de 100x100 y la misma tiene calles (filas), avenidas (columnas) y esquinas (intersección de una calle y una avenida).

Este programa ya se viene implementando hace muchos años en la cátedra, aproximadamente desde 2007. Permite realizar edición de codigo con una serie de instrucciones disponibles. El alumno puede diseñar un algoritmo para resolver distintos problemas y al momento de ejecutar se tiene un visor simulado la ciudad con cuadros azules, el robot con un punto rojo y negro, flores con un circulo rojo con centro amarillo y papeles con circulos blancos. Algunas de las instrucciones disponibles son:

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

### 2.3 Propuesta de solución

Teniendo en cuenta la situación actual y la problemática, se realizará una propuesta de solución: el desarrollo de una plataforma de aprendizaje denominada "Plataforma Gamificada 'Algoritmia' (PGA)", enfocada en el concepto de “Gamificación” y luciendo una estética visual de “Pixel Art”. La plataforma permitirá a los alumnos aprender algoritmos, lógica y estructuras de control y para los docentes permitirá el seguimiento académico exhaustivo de cada uno de los alumnos.

La solución estará compuesta por dos aplicaciones separadas pero integradas:

- Un **videojuego independiente**, desarrollado con Godot y GDScript, orientado exclusivamente a los alumnos. Este videojuego estará diseñado con una historia y narrativa dividida en capítulos temáticos y permitirá la resolución de misiones prediseñadas en un entorno con narrativa y mecánicas lúdicas, funcionando de forma offline y sincronizando el progreso académico a posteriori.
- Una **plataforma web**, destinada a docentes, administradores y en parte a los alumnos también. Esta le permitirá a los docentes hacer seguimiento del progreso de los alumnos, generar reportes y crear sesiones de refuerzo de contenidos. Para el administrador, le permitirá gestionar instituciones, cursos, asignación de docentes a los cursos y auditoría. Para los alumnos, permitirá el registro e inicio de sesión mediante Google, consulta de estadísticas y descarga del videojuego.

Ambas aplicaciones estarán conectadas a la misma base de datos, permitiendo que los datos de avance y resultados obtenidos por los estudiantes en el videojuego se reflejen luego en la plataforma web. El videojuego tambien funcionará de manera offline, permitiendo a los alumnos resolver misiones aun sin conexión. Una vez que se disponga de acceso a Internet, la aplicación sincronizará automáticamente el progreso acumulado con el backend, permitiendo que los datos estén disponibles en la parte web.

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

- **Creación pixel a pixel**: se centra en crear imágenes colocando un color en cada píxel individual. Es un estilo muy artesanal con el cual se pueden lograr resultados muy detallados pero con componentes simples.
- **Estilo retro**: el pixel art nos recuerda a los primeros videojuegos y computadoras, con paleta de colores limitada y gráficos de baja resolución.
- **Influencia en los videojuegos**: es un estilo popular en el diseño de videojuegos, donde se utiliza para crear sprites, personajes, entornos y gráficos de interfaz de usuario.

#### Oportunidades

El desarrollo de este sistema ofrece varias oportunidades tanto a alumnos como a docentes.
**Para alumnos**:

- Podrán aprender y practicar acerca de los contenidos dados en la materia mediante la resolución de misiones y ejecución en tiempo real de sus algoritmos con un escenario de videojuego con estética visual Pixel Art, estusiasmando y enganchando al alumno durante sus prácticas.
- Mediante gamificación, los alumnos podrán ganar experiencia, subir de nivel y desbloquear nuevas misiones y habilidades manteniendo la participación y motivación en utilizar el sistema.
- El sistema detectará los errores cometidos y propondrá mejoras al algoritmo para que el alumno pueda mejorar constantemente, además de recopilar estos mismos datos para informar a los docentes acerca de las dificultades de los alumnos.

**Para docentes**:

- Podrán contar con un seguimiento académico exhaustivo de todos sus alumnos.
- Ver las estadisticas, rendimiento de la semana y porcentaje de avance en los temas de cada alumno.
- Detectar a aquellos alumnos atrasados o con dificultades en los contenidos para la toma de decisiones.

#### Beneficios

Con el desarrollo del sistema se esperan los siguientes beneficios a corto plazo:

1. **Alumnos motivados**: se espera que los alumnos se sientan enganchados y atraídos con el entorno de videojuego con gamificación y estética pixel art.
2. **Seguimiento global e individual del grupo de alumnos**: el docente cada semana podrá revisar el estado de avance global e individual y la evolución de cada uno de los alumnos y podrá detectar aquellos alumnos que quedaron atrasados y reforzar los contenidos.
3. **Proceso de aprendizaje dinámico**: con las mejoras, la detección de errores y la asignación de ejercicios para resolver las dificultades, se espera que los alumnos puedan aprender de manera eficiente los contenidos y corregir o mitigar sus errores rápidamente para poder diseñar mejores algoritmos para otros problemas a futuro.

Los beneficios a largo plazo:

1. **Menos alumnos atrasados**: con el seguimiento academico y mejora constante, Se espera que se tome menos tiempo de cursada "oficial" para el refuerzo de los contenidos y que haya una menor cantidad de alumnos atrasados al momento de, por ejemplo, la toma de exámenes o al final de la cursada.
2. **Alumnos con conocimientos solidificados**: mediante la resolución de ejercicios y ejercicios especiales para mitigar errores, se espera que los alumnos cuenten con una base sólida en cada contenido dado en la plataforma y sean capaces de diseñar mejores algoritmos a futuro.
3. **Plataforma oficial para el dictado en la cátedra**: se espera que a largo plazo el sistema quede consolidado como herramienta principal en el dictado de la cátedra reemplazando al Visual DaVinci, integrando la resolución de ejercicios y seguimiento académico de los alumnos en un solo lugar.

---

## 3. Visión del producto

### 3.1 Perspectiva del producto

El desarrollo e implementación de este sistema encaja perfecamente en la situación y escenario actual debido a los siguientes puntos:

- **Facil adaptación**: el sistema seguirá con la dinámica de aprendizaje de edición de código y ejecución de la "prueba de escritorio" mediante un visor, con la principal diferencia que tendrá un contexto gamificado con visuales y componentes propios de los videojuegos.
- **Seguimiento docente**: los docentes carecen de un seguimiendo académico exhaustivo de cada uno de los alumnos. La incorporación del seguimiento académico mediante el sistema hará que los docentes tengan una mejor visión del estado de avance tanto del grupo de alumnos como el progreso y dificultades de cada uno.
- **Producto propio de la FCEQyN**: el Visual Da Vinci es un proyecto de Tesis de la Universidad Nacional de La Plata (UNLP). Entonces, al desarrollar e implementar un proyecto propio y desarrollado en la misma FCEQyN, engrandecerá el sentido de pertenencia e identidad de los docentes y alumnos.

### 3.2 Objetivos del sistema

#### 3.2.1 Objetivo General

Desarrollar la Plataforma Gamificada "Algoritmia" (PGA) para el aprendizaje de Lógica, Algoritmos, Estructuras de Control y manejo de Variables y Procedimientos con enfoque en la gamificación y estética visual en Pixel Art, que incremente la motivación, facilite la resolución de ejercicios y permita un seguimiento académico exhaustivo de los alumnos.

#### 3.2.2 Objetivos Específicos

| OBJ-01      | Crear y diseñar un videojuego para el aprendizaje gamificado                                                                                                                                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Crear y diseñar un videojuego con mecánicas de capítulos, misiones, acciones, habilidades, objetos, niveles, puntos de experiencia y puntuaciones acompañado de una interfaz Pixel Art y narrativa e historia interesante para motivar e incentivar la participación del alumno |
| Estabilidad | Alta                                                                                                                                                                                                                                                                            |
| Comentarios | -                                                                                                                                                                                                                                                                               |

| OBJ-02      | Ofrecer misiones con dificultad progresiva y curva de aprendizaje controlada                                                                                                                                                                                                                                                                                                                                     |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Diseñar un repertorio de misiones (ejercicios) divididas en capítulos temáticos que exploren las bases de la programación: secuencia, lógica, estructuras de control (condicionales y bucles), variables y procedimientos e implementar que las misiones se desbloqueen progresivamente a medida que el alumno avance y que el docente gestione los capítulos para garantizar la curva de aprendizaje controlada |
| Estabilidad | Alta                                                                                                                                                                                                                                                                                                                                                                                                             |
| Comentarios | -                                                                                                                                                                                                                                                                                                                                                                                                                |

| OBJ-03      | Ofrecer ejecución y visualización del algoritmo en tiempo real                                                                                                                                  |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Diseñar e implementar un sistema de ejecución que lea y ejecute en tiempo real cada instrucción del algoritmo del alumno y la visualice un escenario acorde a la narrativa y estética Pixel Art |
| Estabilidad | Alta                                                                                                                                                                                            |
| Comentarios | -                                                                                                                                                                                               |

| OBJ-04      | Identificar dificultades en los alumnos y ofrecer ayudas para mejorar los algoritmos                                                                                                                                                                                                                                                                                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Analizar automáticamente el algoritmo del alumno para indicar errores de sintaxis, proveer ayudas al diseñar el algoritmo y posteriormente generar sugerencias de optimización, tales como eliminación de instrucciones redundantes y simplificación de estructuras, asi como también determinar las dificultades de los alumnos mediante la recopilación de errores para que el docente pueda estar al tanto de las dificultades individuales de cada alumno |
| Estabilidad | Alta                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Comentarios | -                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

| OBJ-05      | Proveer seguimiento académico exhaustivo                                                                                                                                                                                                                                            |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Desarrollar un tablero de progreso con filtros para docentes que muestre el progreso individual y grupal de los alumnos pudiendo así identificar a los alumnos atrasados y con poca actividad en la plataforma, asi como tambien las dificultades y el riesgo académico de cada uno |
| Estabilidad | Alta                                                                                                                                                                                                                                                                                |
| Comentarios |                                                                                                                                                                                                                                                                                     |

| OBJ-06      | Gestionar reportes y sesiones de refuerzo                                                                                                                                                                                                                                                                      |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Permitir a los docentes generar reportes de progreso, dificultades y estadísticas, asi como también la creación de sesiones de refuerzo para aquellos alumnos con riesgo académico alto para poder tratar a tiempo las dificultades, dudas y consultas de los alumnos para evitar que se atrasen en el cursado |
| Estabilidad | Media                                                                                                                                                                                                                                                                                                          |
| Comentarios | Adicionalmente, el sistema tendrá como proceso automatizado la generación de un reporte semanal de progreso y dificultades de los alumnos con la coordinación de una sesión de refuerzo para aquellos que posean un riesgo académico alto                                                                      |

| OBJ-07      | Gestionar cursos y datos de la institución                                                                                                                                                                                                                                |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Permitir el despliegue del sistema a cualquier institución educativa que quiera incorporar el sistema a su metodología de enseñanza, ofreciendo la gestión de sus cursos y personal docentes correspondientes                                                             |
| Estabilidad | Alta                                                                                                                                                                                                                                                                      |
| Comentarios | El rol de administrador se encargará de la configuración de los datos de la institución, la gestión de cursos, docentes y la asignación de docentes a los cursos. El docente puede cambiar la contraseña del curso la cual informará a sus alumnos para que puedan unirse |

| OBJ-08      | Gestionar usuarios y roles del sistema                                                                                                                                                                         |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Permitir la gestión, registro e inicio de sesión de usuarios asi como también la asignación de roles en el sistema (alumno, docente y administrador)                                                           |
| Estabilidad | Alta                                                                                                                                                                                                           |
| Comentarios | Los alumnos podrán registrarse e iniciar sesión en la web mediante autenticación con Google y en el videojuego solo por el usuario y contraseña. Docentes y administradores solamente con usuario y contraseña |

| OBJ-09      | Gestionar la auditoría del sistema                                                                                      |
| ----------- | ----------------------------------------------------------------------------------------------------------------------- |
| Descripción | Proporcionar a los administradores un módulo de auditoría que les permita visualizar los diferentes eventos del sistema |
| Estabilidad | Media                                                                                                                   |
| Comentarios | -                                                                                                                       |

| OBJ-10      | Persistir el progreso de manera local y sincronizarlo luego                                                                                                                                                                                               |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Permitir que los alumnos resolver las misiones del videojuego sin necesidad de conexión a internet permanente, almacenando el progreso de forma local para posteriormente sincronizarlo a la base de datos principal cuando se tenga conexión a internet. |
| Estabilidad | Media                                                                                                                                                                                                                                                     |
| Comentarios | -                                                                                                                                                                                                                                                         |

| OBJ-11      | Diseñar un pseudo-lenguaje gamificado para la resolución de misiones                                                                                                                                                                                         |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Descripción | Diseñar un pseudocódigo gamificado que permita manejar: primitivas, estructuras de control (condicionales y bucles), variables y procedimientos con parámetros que permitan al alumno diseñar algoritmos efectivos para resolver las misiones del videojuego |
| Estabilidad | Alta                                                                                                                                                                                                                                                         |
| Comentarios | -                                                                                                                                                                                                                                                            |

### 3.3 Modulos del sistema

#### 3.3.1 Plataforma web

**Funcionales**

- Usuarios
- Institución y cursos
- Progreso
- Dificultades
- Estadísticas
- Reportes
- Sesiones de refuerzo

**No funcionales**

- Seguridad y autenticación
- Auditoría

#### 3.3.2 Videojuego

No se divide en módulos como un sistema tradicional. No se desarrollará ni diseñará como un sistema software tradicional y no se utilizarán metodologías de desarrollo de software tradicionales.
Consulte el Game Design Document ubicado en `docs/game-design/gdd.md` para obtener la información necesaria de todas las funcionalidades, diseño y componentes del videojuego.

### 3.4 Alcance y Limitaciones por módulo

#### 3.4.1 Usuarios

En la gestión de usuarios, se tendrán tres roles diferentes que servirán para definir los niveles de acceso al sistema:

- **Administrador**: Acceso a los módulos de gestión de instituciones, gestión de cursos y tareas de gestión de docentes, como la alta, baja, modificación y también el asignar o remover docentes a cursos correspondientes. Es el unico usuario que poseerá acceso al módulo de auditoría para consulta y exportación.
- **Alumno**: Acceso en la web para registrarse sea con Google o mediante formulario, inciar sesión, unirse a un curso, revisión de sus estadísticas de juego, dificultades y modificación del perfil. Tendrá acceso a la descarga exclusiva del videojuego.
- **Docente**: Acceso principal y completo al módulo de Progreso y estadísticas donde podrá visualizar y realizar reportes de progreso de los alumnos y visualizar sus dificultades. En el módulo de Gestion de sesiones de refuerzo podrá coordinar sesiones de refuerzo para los alumnos. También tendrá acceso parcial a la gestión de cursos, para visualizarlos, cambiar contraseña de acceso y permitir el acceso de sus alumnos.

#### 3.4.2 Institución y cursos

Este modulo del sistema estará controlado en su mayor medida por el administrador del sistema y algunas funcionalidades para los docentes.

El administrador del sistema tendrá las siguientes funcionalidades:

**Dar de alta los datos de la institución**
El administrador, al instalar el sistema en la institución educativa, deberá configurar y dar de alta los datos específicos de la misma, los cuales estarán disponibles en el sistema a partir del Padron Oficial de Establecimientos Educativos.

**Gestión de Cursos**
El administrador podrá realizar tareas de alta, baja y modificación de los cursos dentro del sistema.

**Asignación de docentes a los cursos**
El administrador tambien se encargará de asignar a los docentes a sus cursos correspondientes asi como también remover a un docente de un curso cuando corresponda.

El docente también tendra las siguientes funcionalidades:

**Definición de días y horarios de cursada**
Los docentes podrán configurar los días, horarios y modalidad (presencial, virtual o mixta) de cursada de la materia por cada curso a su cargo. Esto le servirá al sistema para luego realizar las sesiones de refuerzo automáticas.

**Habilitación de capítulos**
Los docentes podrán habilitar los capítulos de la historia a medida que se vayan dando los contenidos en la materia para garantizar una curva de aprendizaje controlada y seguimiento académico ordenado de los alumnos.

#### 3.4.3 Progreso

En este módulo del sistema, los docentes tendrán funcionalidades para realizar el seguimiento de progreso a sus alumnos. Podrán consultar el progreso en el videojuego en tiempo real y las dificultades que tenga cada alumno al intentar resolver las misiones.

**Visualización y reportes del progreso y dificultades de alumnos**

Los docentes podrán consultar y realizar reportes del progreso de los alumnos del curso, tanto el progreso total como el progreso en cada capítulo. Por cada curso, se podrán visualizar los siguientes datos:

**Progreso del curso**

- Porcentaje total de misiones completadas
- Porcentaje de misiones completadas en el capítulo actual

**Progreso individuales del alumno**

- Nombre/s y Apellido/s del alumno
- Capítulo y Misión en la que se encuentra
- Cantidad de misiones completadas
- Porcentaje total de misiones completadas
- Porcentaje de misiones completadas en el capítulo actual
- Promedio de intentos por misión
- Cantidad de estrellas obtenidas
- Total de puntos de experiencia (EXP) acumulados
- Fecha y hora del ultimo inicio de sesión en el videojuego.
- Ultima actividad (Activo hace N minuto(s) / hora(s) / día(s))

También, se podrán aplicar los siguientes filtros de búsqueda:

- Busqueda por nombre(s) y/o apellido(s)
- Filtro por fechas desde - hasta
- Filtro por capítulo(s)
- Filtro por porcentaje de misiones completadas
  - más del 25%
  - más del 50%
  - más del 75%
  - más del 90%
- Filtro por promedio de intentos por misión
  - 1 a 3 intentos
  - 3 a 6 intentos
  - 6 a 9 intentos
  - Más de 10 intentos
- Filtro por días de inactividad
  - hasta 3 días
  - hasta 5 días
  - hasta 7 días
  - más de 7 días

**Progreso del curso en el capítulo**
Si filtra la búsqueda por un capítulo específico, se mostrarán algunos datos adicionales:

- Porcentaje de avance del curso en el capítulo
  - Si está "En curso", se muestra el porcentaje de misiones completadas hasta el momento.
  - Si está "Finalizado", se muestra el porcentaje de misiones completadas cuando finalizó y el porcentaje de misiones completadas hasta el momento, ya que los alumnos podrán seguir jugando misiones que no hayan completado de capitulos con estado "Finalizado".
- Estado del capítulo: "En curso" o "Finalizado"

**Progreso individual del alumno**

Todas los datos de progreso de cada alumno serán las mismas pero correspondientes al capítulo seleccionado.

Todos los datos se podrán ordenar de manera ascendente o descendente.

#### 3.4.4 Dificultades

En este módulo del sistema, los docentes podrán consultar las dificultades de todos los alumnos del curso.
Se tendrán distintas dificultades agrupadas por tipo, los cuales son: Secuencia, Lógica proposicional, Estructuras de control, Variables y Procedimientos. La lista de las dificultades posibles son las siguientes:
**Secuencia**

- Errores de sintaxis
- Instrucciones redundantes

**Lógica proposicional**

- Condiciones mal formuladas
- Uso incorrecto de operadores lógicos

**Estructuras de control**

- Bucle infinito

**Variables**

- **Procedimientos**

- Mal pasaje de parámetros

El sistema permitirá aplicar los siguientes filtros de búsqueda:

- Búsqueda por nombre(s) y/o apellido(s)
- Filtro por tipo(s) de dificultad
- Filtro por dificultad(es)
- Filtro por grado(s) de dificultad (determinada por la cantidad de errores acumulados de ese tipo de dificultad)

(COMPLETAR CUANDO SE VEAN LOS CASOS DE EVALUACIÓN DE DIFICULTAD)

#### 3.4.7 Sesiones de refuerzo

Las de sesiones de refuerzo son la forma por la cual el sistema ofrece, a docentes y alumnos, la coordinación de un espacio de resolución de dudas, consultas y dificultades.

Este módulo le permitirá a los docentes visualizar e identificar el estado de cada alumno en cuando a progreso, dificultades y/o inactividad en la plataforma. Mediante un algoritmo, el sistema clasificará a los alumnos en diferentes niveles de riesgo académico. Con riesgo académico nos referimos a la probabilidad de que el alumno no alcance el nivel de dominio o avance esperado en el videojuego y en el curso. La clasificación es la siguiente:

**Riesgo bajo (resaltados en color amarillo suave)**: Son aquellos alumnos que posean:

- De 1 a 3 dificultades al resolver misiones.
- Inactividad de hasta 2 días.

**Riesgo medio (resaltados en color naranja suave)**: Son aquellos alumnos que posean:

- De 3 a 5 dificultades al resolver misiones.
- Inactividad de hasta 4 días.

**Riesgo alto (resaltados en color rojo suave)**: Son aquellos alumnos que posean:

- Más de 5 dificultades al resolver misiones.
- Inactividad de más de 5 días

##### Creación de una sesión de refuerzo

Para cada sesión de refuerzo se deberá completar:

**Alumnos involucrados**: se deberá seleccionar a los alumnos a involucrar en la sesión. Se mostrarán a los alumnos dentro de la clasificación mencionada anteriormente.

**Dificultades de los alumnos**: de cada alumno seleccionado, se mostrarán las dificultades con su respectivo grado y los días de inactividad.

**Descripción de la sesión**: en base a las dificultades de cada alumno, el sistema propondrá como tratar y mitigar las dificultades. El docente podrá modificar la descripción de la sesión a su gusto agregando o eliminando información.

**Modalidad de la sesión**: se deberá especificar como se realizará la sesión de refuerzo: presencial o virtual.

**Duración**: se debe colocar la duración de la sesión en minutos, el sistema recomendará 20 minutos.

**Fecha**: El sistema, como recomendación, propondrá la fecha de la siguiente clase del curso, por disponibilidad de los alumnos. De todas maneras, el docente puede elegir la fecha que desee en un rango de 7 días hacia adelante.

**Hora**: aquí dependerá si el docente eligió una fecha correspondiente a un día de clases o una fecha libre.

- **Fecha de clases**: si se eligió una fecha de clases, el docente podrá elegir cuándo realizar la sesión de refuerzo: antes o después de la clase. Dependiendo de la elección, el sistema autocompletará la hora de la sesión:
  - Si se eligió _antes_ de la clase: a la hora de incio de clase se restan los minutos de duración de la sesión
  - Si se eligió _después_ de la clase: a la hora de fin de clase se suman los minutos de duración de la sesión
- **Fecha libre**: si se eligió una fecha libre, el docente elige la hora libremente con las siguientes reglas:
  - Se pueden coordinar sesiones de refuerzo a partir de las 07:00.
  - Se pueden coordinar sesiones hasta cierto horario dependiendo de la duración de la sesión, terminando como máximo a las 23:00. Es decir, Si la duración de la sesión de refuerzo es de 30 minutos, como máximo se podrá coordinar a las 22:30. A partir de las 22:31 ya no se pueden coordinar sesiones para ese día.

**Sesión virtual**: si la sesión será virtual, se deberán completar datos adicionales:

- **URL de la reunión**: puede ser la misma URL recurrente de reunión del curso o de alguna URL programada en alguna plataforma de reuniones virtuales, como Zoom, Google Meet, etc.
- **ID o código de reunión**: Opcional, debido a que en algunas plataformas basta con la URL y permiso del anfitrión para ingresar a la reunión.
- **Contraseña de acceso a la reunión**: Opcional, por el mismo motivo del ID o codigo de reunión.

Una vez creada la sesión, los alumnos involucrados serán notificados vía correo eletrónico y deberan confirmar su asistencia a la misma con un tiempo disponible de hasta 2 horas antes del inicio de la sesión, se enviarán recordatorios cada 6 horas. Para que la sesión sea válida, minimamente un alumno debe confirmar su asistencia y el docente mantener la sesión encaminada.

Cuando un alumno indica que asistirá a la sesion de refuerzo, éste podrá escribir sus dudas o consultas específicas al docente. Esto servirá para que el docente pueda saber de antemano, además de las dificultas del alumno, sus dudas o consultas específicas para preparar mejor la sesión.

Si un docente crea una sesión de refuerzo pero luego indica que no puede asistir y aún no llegan las dos horas previas al inicio de la sesión, otro docente del curso puede decidir tomar la sesión de refuerzo e indicar su asistencia a la misma.

##### Estado de una sesión de refuerzo
Luego de crear una sesión de refuerzo, esta puede pasar por diferentes estados:
- **En espera**: estado predeterminado de la sesión cuando:
  - Se crea una sesión de refuerzo automática y queda a la espera de la confirmación de un docente y/o un alumno.
  - Se crea una sesión de refuerzo manualmente por un docente y queda a la espera de la confirmación de un alumno.
  - Un docente crea una sesión y posteriormente desmarca su asistencia. La sesión queda a la espera de la confirmación de otro docente.
- **Programada**: estado de la sesión cuando un docente y mínimo un alumno confirmaron su asistencia. Se mantendrá en este estado así mientras un docente y mínimamente un alumno mantengan su asistencia hasta llegar a las 2 horas previas al inicio de la sesión.
- **A realizarse**: estado en el que queda la sesión de refuerzo cuando se llega a las dos horas previas a la sesión. Cuando la sesión está en este estado, ya no se podrán modificar asistencias ni del docente ni de los alumnos.
- **En curso**: estado cuando "transcurre" la sesión de refuerzo.
- **Cancelada**: estado cuando la sesión de refuerzo es cancelada manualmente por un docente o cuando se llega a las dos horas previas al inicio de la sesión y ningun docente del curso indica que asistirá.
- **Realizada**: estado que queda cuando el docente confirma que se realizó la sesión de refuerzo. Para que pueda colocarse este estado, es necesario que la sesión haya pasado por el estado de "A realizarse" y "En curso".
- **No realizada**: estado en el que que queda la sesión cuando el docente indica que no se realizó la sesión de refuerzo aunque haya pasado por el estado de "A realizarse" y "En curso".

##### Progreso semanal y sesión de refuerzo automatizada

El sistema tendrá como uno de los procesos automatizados la generación de un reporte resumido de progreso y dificultades de los alumnos del curso junto con la creación de una sesión de refuerzo. Este proceso automatizado se realizará semanalmente los días sábado a las 18:00 y para su realización trabajarán en conjunto el módulo de Progreso y el módulo de Sesiones de refuerzo.

El objetivo de este proceso automatizado es que el docente pueda tener una vista rápida y resumida del progreso de los alumnos durante la semana asi como también las dificultades determinadas automáticamente por el videojuego. Con ello, tener programada automáticamente una sesión de refuerzo con aquellos alumnos con más dificultades e inactividad para poder atender sus dudas y consultas en la siguiente clase del curso.

En el reporte se incluirán el progreso y las dificultades de los alumnos del curso. El progreso estará agrupado por capítulos (solo los capítulos "Finalizados" y los que estén "En curso") y las dificultades agrupadas por tipo y dificultad. El reporte será enviado a todos los docentes del curso a su correo electrónico.

A partir de los datos procesados durante la semana, el sistema creará una sesión de refuerzo automáticamente con la siguiente configuración:

- **Alumnos involucrados**: todos los alumnos resaltados en rojo en el reporte.
- **Dificultades de los alumnos**: todas las de los alumnos involucrados.
- **Descripción de la sesión**: propuesta automática del sistema en base a las dificultades de los alumnos involucrados.
- **Modalidad**: la definida en el curso.
- **Duración**: 20 minutos.
- **Fecha**: siguiente clase del curso.
- **Hora**: antes de la clase.

Para que la sesión sea confirmada, deben confirmar su asistencia:

- Uno de los docentes a cargo del curso (el cual será el responsable de dirigirla) y
- Un alumno (mínimamente).

Tanto los docentes como los alumnos tendrán un tiempo límite para confirmar o modificar su respuesta hasta 2 horas antes de la hora de inicio de la sesión.

**Flujo de decisión**

1. **Si un docente confirma su asistencia antes que un alumno**: se notifica a todos los alumnos involucrados vía mail avisando que el docente está dispuesto a dar la sesión y para recordar que confirmen su asistencia. Se enviarán recordatorios cada 6 horas. Dado este caso:

   1. **Un alumno confirma la asistencia**: si mínimamente un alumno confirma su asistencia y mantiene su decisión hasta las 2 horas antes del inicio de la sesión, el sistema asumirá que la sesión de refuerzo se llevará a cabo.

   2. **Ningún alumno confirma la asistencia**: si ningun alumno confirma la asistencia en el tiempo determinado (hasta las 2 horas antes del inicio de la sesión), el sistema asume que la sesión no se llevará a cabo. El sistema buscará en los proximos 5 días el siguiente día de clases y re-agendará la sesión para esa fecha y se le notificará a los involucrados (docentes y alumnos). Se mantendrá la asistencia del docente para la sesión re-agendada.

2. **Si un alumno confirma su asistencia antes del docente**: se notifica por correo electrócnio a todos los docentes del curso solicitando que uno confirme su asistencia a la sesión. Se enviarán recordatorios cada 2 horas. Dado este caso:

   1. **Un docente confirma la asistencia**: si un docente confirma su asistencia a la sesión y mantiene su decisión hasta las 2 horas antes del inicio de la sesión y si el alumno que confirmó mantiene su decisión hasta las 2 horas antes del incio de la sesión, el sistema asumirá que la sesión de refuerzo se llevará a cabo.

   2. **Ningún docente confirma su asistencia** si ningun docente confirma la asistencia en el tiempo determinado (hasta las 2 horas antes del inicio de la sesión), el sistema asume que la sesión no se llevará a cabo. El sistema buscará en los proximos 5 días el siguiente día de clases, re-agendará la sesión para esa fecha y se le notificará a los involucrados (docentes y alumnos). Se mantendrá la asistencia del alumno para la sesión re-agendada.

3. **Ninguno de los involucrados confirma su asistencia**: si ningun docente ni alumno confirma la asistencia en el tiempo determinado (hasta las 2 horas antes del inicio de la sesión), el sistema asume que la sesión no se llevará a cabo. El sistema buscará en los proximos 5 días el siguiente día de clases, re-agendará la sesión para esa fecha y se le notificará a los involucrados (docentes y alumnos).

4. **Cambios en una sesión de refuerzo encaminada**

   1. **El docente a cargo indica que no asistirá**: si el docente había confirmado su asistencia y si antes de llegar a las 2 horas previas al inicio de la sesión indica que no podrá asistir y mantiene su decisión hasta las 2 horas antes del inicio de la sesión, el sistema asume que la sesión no se llevará a cabo. El sistema buscará en los proximos 5 días el siguiente día de clases, re-agendará la sesión para esa fecha y se le notificará a los involucrados (docentes y alumnos). Se mantendrán las asistencias de los alumnos que así la mantuvieron.

   2. **Todos los alumnos que iban a asistir indican que no asistirán**: si _todos_ los alumnos que confirmaron su asistencia cambian su respuesta e indican que no asistirán, y esto se mantiene así hasta las 2 horas previas al incio de la sesión sin que, mínimamente, un alumno confirme su asistencia, el sistema asume que la sesión no se llevará a cabo. El sistema buscará en los proximos 5 días el siguiente día de clases, re-agendará la sesión para esa fecha y se le notificará a los involucrados (docentes y alumnos). Se mantendrán la asistencia del docente para la sesión re-agendada.

Cuando llega el horario de fin la sesión de refuerzo, el docente y alumnos involucrados tendrán 12 horas para confirmar si efectivamente asistieron a la sesión.

#### 3.4.5 Estadísticas

En el módulo de estadísticas, los docentes podrán consultar estadísticas de interés a partir de los datos acumulados del progreso y las dificultades de los alumnos del curso.

**Estadísticas del progreso de los alumnos**

- Recuento de misiones completadas en el día: tambien disponible como resumen en el dashboard docente en la página de inicio.
- Recuento de misiones completadas en la semana: tambien disponible como resumen en el dashboard docente en la página de inicio.
- Recuento de misiones completadas en un intervalo de fechas (desde-hasta)
- Recuento de intentos por misión en un capítulo

**Estadísticas de las dificultades de los alumnos**

- Recuento de alumnos
  - por tipo de dificultad
  - por dificultad
- Recuento de dificultades por grado
- Grado estimado de dificultad por tipo: también disponible como resumen en el dashboard docente
- Evolución de las dificultades de un alumno (cambios del grado de dificultad)

**Estadísticas de las sesiones de refuerzo**
Este parte del módulo solo será accesible por el administrador del sistema. Se tendrá:

- Recuento de sesiones de refuerzo realizadas y no realizadas
- Recuento de sesiones de refuerzo creadas por docente
- Recuento de sesiones de refuerzo automáticas aceptadas por docente
- Recuento de docentes que cambiaron su asistencia positivamente (rechazó y luego aceptó) y negativamente (aceptó pero luego rechazó)

#### 3.4.6 Reportes

#### 3.4.8 Seguridad y autenticación

El manejo de la seguridad y autenticación en los alumnos y docentes es un tanto diferente, asi que se definirán algunas reglas de autenticación para cada rol en el sistema.

##### Reglas de registro e inicio de sesión según el tipo de usuario

**Alumnos**
El registro de alumnos estará habilitado desde el sistema (se pueden registrar solos)

- **Opción 1**: Registro en la web mediante formulario tradicional.
- **Opción 2**: Registro en la web con Google (autenticación con Google y luego completar datos adicionales el formulario).
- Almacenamiento en la base de datos con posibilidad de iniciar sesión en la plataforma web por cualquiera de los dos medios (usuario/contraseña o Google).

El **incio de sesión** en el videojuego se realizará unicamente con usuario y contraseña definidos en el registro en la parte web. Al inciar sesión, el videojuego validará y sincronizará los datos del alumno en el videojuego para guardar el progreso localmente y, cuando comience a progresar en el videojuego, el progreso local se sincronizará a la web.

**Docentes**
El registro de docentes NO ESTARÁ habilitado desde el sistema (NO se pueden registrar solos) y el inicio de sesión solo será mediante usuario y contraseña (sin autenticación con Google).

- Los docentes deberán proporcionar sus datos al administrador del sistema mediante un formulario.
- El administrador se encargará de verificar los datos del docente y deberá darlo de alta manualmente en el sistema.
- El administrador crea el usuario del docente con los datos declarados.
- Luego, el sistema envía automáticamente el usuario y contraseña inciales del docente al correo declarado.
- Luego del primer inicio de sesión del docente, el sistema exigirá que cambie la contraseña de su usuario por seguridad.

#### 3.4.9 Auditoría

Este módulo estará principalmente disponible para el rol **administrador**, que es quien supervisa el uso y funcionamiento general de la plataforma.

##### Tareas de Auditoría que podrá realizar el Administrador

1. **Revisar inicios de sesión**: Ver quién, cuándo y desde dónde se accede a la plataforma (docentes, alumnos, admin).
2. **Auditar la gestión de usuarios**: Revisar la alta, baja y modificación de usuarios del sistema por quién y cuándo.
3. **Auditar cambios en los datos de la institución**: Ver cuándo se configuran y modifican los datos de la institución dentro del sistema y quien realiza las acciones.
4. **Auditar cambios en cursos**: Ver cuándo se crean, modifican o eliminan cursos, asi como también la asignación y desasignación de docentes a los cursos y quién lo hizo.
5. **Auditar configuraciones de sesiones de refuerzo**: Ver cuándo se programaron, aprobaron o marcaron como realizadas las sesiones de refuerzo.
6. **Auditar acciones críticas del sistema**: Cambios de contraseña de administrador.
7. **Auditar registros fallidos de inicio de sesión**: Intentos fallidos que pueden revelar problemas o accesos no autorizados.

Entonces, dentro del módulo de auditoría, el administrador podrá:

1. Seleccionar el módulo a auditar
2. Según lo seleccionado, ver un historial de los eventos ordenados cronológicamente.
3. Filtrar por tipo de evento, usuario, fecha o rol.
4. Buscar eventos específicos (por palabra clave).
5. Exportar el historial como PDF (opcional).
6. Ver detalles expandibles de cada entrada (antes y después del cambio).

##### Qué se registra en la auditoría

Cada entrada de auditoría contendrá los siguientes campos:

| Campo              | Descripción                                                       |
| ------------------ | ----------------------------------------------------------------- |
| `timestamp`        | Fecha y hora del evento                                           |
| `usuario`          | ID o nombre del usuario que realizó la acción                     |
| `rol`              | Rol del usuario (admin, docente, alumno)                          |
| `acción`           | Tipo de evento (inicio de sesión, creación de curso, etc.)        |
| `recurso_afectado` | A qué recurso afectó (curso, usuario, sesión de refuerzo, etc.)   |
| `datos_antes`      | Estado anterior del recurso (si aplica, por ejemplo en ediciones) |
| `datos_despues`    | Estado posterior del recurso (si aplica)                          |

##### Seguridad y privacidad

- Solo el administrador del sistema tendría acceso completo al módulo de auditoría.
- Los registros no deben poder editarse ni eliminarse por ningún usuario.
- Los logs se almacenarán en una tabla especial en la base de datos con acceso restringido.

### 3.5 Exclusiones de la plataforma web

Con el alcance del proyecto definido, se listarán tambien algunas funcionalidades que el sistema NO INCLUIRÁ en la versión final del producto a entregar el 15/11/2025. Que las siguientes funcionalidades listadas aquí no se incluyan en el proyecto no significa que no estén consideradas para implementarse en un futuro.

#### 3.5.1 Gestión de usuarios

- Administrador
  - No existirá una interfaz avanzada para análisis estadístico de gestión global del sistema.
- Alumno
  - No podrá cambiar de curso. El alumno puede estar inscripto a un solo curso.
  - No podrá modificar su nombre de usuario o correo tras el registro (solo cambio de contraseña).
- Docente
  - No podrá crear ejercicios personalizados ni modificar el banco de ejercicios.

#### 3.5.2 Gestión de instituciones

- No se permitirá la importación/exportación masiva de alumnos o docentes por archivo.

#### 3.5.3 Gestión de cursos

- No se permitirá crear misiones específicos por curso.
- No se podrán crear distintas configuraciones de misiones por curso.
- No se podrán configurar parámetros como el porcentaje de XP o cantidad de estrellas de puntuación por curso.

#### 3.5.4 Seguimiento académico

- No se incluirá funcionalidad para mensajes o anuncios escritos por docentes y alumnos dentro de la plataforma.

#### 3.5.6 Seguridad y autenticación

- No se incorporará autenticación mediante redes sociales externas como Facebook, X, GitHub, etc.
- No se incorporará verificación en dos pasos (2FA).
- No se integrará autenticación OAuth para docentes ni administradores (registro solo manual).
- No se permitirán inicios de sesión simultáneos en múltiples dispositivos (se mantendrá simple).

#### 3.5.7 Auditoría

- No habrá visualización avanzada con gráficos o dashboards de auditoría.
- No se incluirán alertas automatizadas por eventos sospechosos o fallos de seguridad.

#### 3.6 Exclusiones del videojuego

##### Misiones

- No se incluirán **temas de estructuras de datos avanzadas**: strings, arrays, matrices, registros, arrays de registros y archivos.
- No se implementará un **editor visual de creación de ejercicios** (por ejemplo, arrastrar y soltar condiciones).
- No se permitirán **ejercicios grupales colaborativos**.
- No se podrán **personalizar los ejercicios** ni por docentes ni por administradores.
- No se incluirá la funcionalidad de evaluaciones o exámenes.

#### Componentes

- No se incluirán tiendas de ítems o recompensas.
- No habrá modificación o personalización de avatar (ropa, color de cabello, accesorios).
- No se implementarán eventos temporales o dinámicas gamificadas adicionales (ej: misiones diarias, recompensas por login).
- No se incluirá un ranking público de alumnos ni competencia directa entre ellos.

#### Diseño de algoritmos y ejecución

- No se incluirán múltiples lenguajes de programación (se trabaja con un único lenguaje gamificado).
- No se podrá configurar la velocidad de ejecución normal.
- No se permitirá guardar múltiples soluciones para un mismo ejercicio.
- No se mostrarán estadísticas detalladas por algoritmo (tiempo de ejecución, memoria, etc.).
- El feedback se centrará en sugerencias básicas de optimización y errores de sintaxis, no en explicación semántica o pedagógica demaciado profunda.
- No se implementarán tests automatizados personalizados (test cases hechos por docentes o alumnos).

---

## 4. Stakeholders

| Stakeholder                   | Papel o interés                                 |
| ----------------------------- | ----------------------------------------------- |
| Profesores Tutores            | Consultores, validación académica y supervisión |
| Alumnos y Docentes / Usuarios | Uso y evaluación de la plataforma               |

---

## 5. Supuestos y Restricciones

- Debe validarse con 20 usuarios antes del 15/11/2025.
- El proyecto se desarrollará en un entorno local para la demostración. El despliegue de la aplicación quedará para más adelante.
