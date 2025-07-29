# Requisitos de Información del sistema

**Versión:** 1.3
**Fecha:** 28/06/2025
**Autor(es):** Franco Andrés Albornoz

En este documento se detalla la lista de requisitos de almacenamientos y de restricciones de información que se haya identificado.

---

## RI-01 Información de usuarios

**Objetivos asociados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- UC-XX Alta usuario
- UC-XX Modificar usuario
- UC-XX Baja usuario
- UC-XX Buscar usuario
- UC-XX Iniciar sesión
- UC-XX Registrarse

**Descripción**
El sistema deberá almacenar la información correspondiente a los usuarios del sistema. En concreto:

**Datos específicos**

- Id de usuario
- Nombre de usuario
- Contraseña de usuario
- Correo electrónico
- Rol de usuario (alumno, docente o administrador)
- Fecha de creación de la cuenta
- Estado (activo/inactivo)

## RI-02 Información de instituciones

**Objetivos asociados**

- OBJ-07 Gestión Académica

**Requisitos asociados**

- UC-XX Alta de institución
- UC-XX Modificar institución
- UC-XX Baja de institución
- UC-XX Buscar institución

**Descripción**
El sistema deberá almacenar la información correspondiente a las instituciones del sistema. En concreto:

**Datos específicos**

- Id de institución
- Nombre de la institución
- Dirección de la institución
- Teléfono de contacto
- Correo electrónico de contacto

## RI-03 Información de cursos

**Objetivos asociados**

- OBJ-07 Gestión Académica

**Requisitos asociados**

- UC-XX Alta de curso
- UC-XX Modificar curso
- UC-XX Baja de curso
- UC-XX Buscar curso
- UC-XX Solicitar ingreso a curso
- UC-XX Asignar docente a curso
- UC-XX Aprobar solicitud de ingreso al curso
- UC-XX Cambiar contraseña de curso
- UC-XX Definir días y horarios del curso

**Descripción**
El sistema deberá almacenar la información correspondiente a los cursos del sistema. En concreto:

**Datos específicos**

- Id de curso
- Nombre del curso
- Institución a la que pertenece el curso
- Días y horarios de cursada
- Docente/s a cargo del curso
- Alumnos asociados al curso
- Contraseña para el ingreso al curso
- Estado del curso (activo/finalizado)

## RI-04 Información de docentes

**Objetivos asociados**

- OBJ-07 Gestión Académica
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- UC-XX Actualizar datos personales
- UC-XX Buscar docente

**Descripción**
El sistema deberá almacenar la información correspondiente a los docentes del sistema. En concreto:

**Datos específicos**

- Id de docente (Id de usuario)
- Nombre/s y Apellido/s del docente
- Género (Masculino, Femenino u Otro)
- Institucion/es a la que pertenece el docente
- Cursos a cargo del docente
- Sesiones de refuerzo creadas por el docente

## RI-05 Información de alumnos

**Objetivos asociados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- UC-XX Registrarse
- UC-XX Actualizar datos personales
- UC-XX Buscar alumno

**Descripción**
El sistema deberá almacenar la información correspondiente a los alumnos dentro del sistema. En concreto:

**Datos específicos**

- Id de alumno (que sería el Id de usuario)
- Nombre/s y Apellido/s del alumno
- Género (Masculino, Femenino u Otro)
- Cursos a los que está asociado
- Método de registro

## RI-06 Información de estadísticas de progreso de los alumnos

**Objetivos asociados**

- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- UC-XX Ver progreso en la web
- UC-XX Ver progreso en el juego
- UC-XX Consultar progreso de alumnos
- UC-XX Generar reporte de progreso de alumnos

**Descripción**
El sistema deberá almacenar la información correspondiente a las estadísticas (progreso) de juego de cada alumno dentro del sistema. En concreto:

**Datos específicos**

- Id de alumno (que sería el Id de usuario)
- Total de puntos de experiencia (EXP) obtenidos
- Nivel actual
- Capítulo y Misión actual
- Cantidad de misiones completadas
- Cantidad de estrellas obtenidas
- Promedio de intentos por misión
- Porcentaje de avance en un capítulo
- Porcentaje de avance en la historia
- Fecha y hora del ultimo inicio de sesión en el videojuego.
- Ultima actividad (Activo hace x día(s))

## RI-07 Información de sesiones de refuerzo

**Objetivos asociados**

- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- UC-XX Consultar progreso de alumnos
- UC-XX Crear sesión de refuerzo
- UC-XX Confirmar asistencia a sesión de refuerzo
- UC-XX Aceptar sesión de refuerzo automática

**Descripción**
El sistema deberá almacenar la información correspondiente a las sesiones de refuerzo de contenidos dentro del sistema. En concreto:

**Datos específicos**

- Id sesión de refuerzo
- Docente a cargo de la sesión de refuerzo
- Alumnos involucrados
- Temas a reforzar
- Fecha y hora de la sesión
- Duración de la sesión en minutos
- Modalidad de la sesión (presencial o virtual)
  - Si es virtual: URL adjunta de la reunión/meet/zoom

## RI-08 Información de capítulos

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**

- UC-XX Habilitar capítulo
- UC-XX Buscar capítulo

**Descripción**
El sistema deberá almacenar la información correspondiente a los capítulos (temas) de la historia dentro del sistema. En concreto:

**Datos específicos**

- Id de capítulo
- Nombre del capítulo
- Descripción del capítulo
- Tema referenciado del capítulo (Algoritmos, Lógica, Estructuras de Control, Variables o Procedimientos)
- Cantidad de misiones del capítulo
- Nivel requerido para desbloqueo
- Habilitación del docente (habilitado o no)
- Estado del capítulo (En curso o Finalizado)

## RI-09 Información de misiones

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**

- UC-XX Buscar misión
- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Evaluar misión

**Descripción**
El sistema deberá almacenar la información correspondiente a las misiones (ejercicios) de cada capítulo de la historia dentro del sistema. En concreto:

**Datos específicos**

- Id de misión
- Nombre de la misión
- Capítulo al que pertenece la misión
- Dificultad de la misión (Fácil, Normal o Difícil)
- Descripción (Enunciado) de la misión
- Nivel requerido para desbloqueo
- Estado de desbloqueo
- Estado de la misión (Completada, no completada)

## RI-10 Información del escenario

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión

**Descripción**
El sistema deberá almacenar la información correspondiente a la configuración del escenario de cada misión dentro del sistema. En concreto:

**Datos específicos**

- Id de escenario
- Misión a la que pertenece el escenario
- Ancho del escenario
- Largo del escenario
- Cantidad de celdas del escenario (ancho \* largo)
- Elementos esparcidos por el escenario

## RI-11 Información de elemento de escenario

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión

**Descripción**
El sistema deberá almacenar la información y posición correspondiente a los elementos dentro de un escenario de cada misión del sistema (enemigos, obstáculos y objetos). En concreto:

**Datos específicos**

- Id del elemento de escenario
- Nombre del elemento de escenario
- Tipo de elemento de escenario (enemigo, obstáculo u objeto)
- Descripción del elemento de escenario
- Proposición del elemento de escenario (para evaluar)
- Sprite (imagen) del elemento de escenario.

## RI-12 Información de primitivas

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Agregar acción
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a las primitivas dentro del sistema, las cuales son representadas como "Acciones" en lenguaje gamificado. En concreto:

**Datos específicos**

- Id de la primitiva
- Nombre de la primitiva
- Descripción de la primitiva
- Sintaxis de la primitiva
- Nivel requerido para desbloqueo
- Sprite (imagen/ícono) de la primitiva
- Estado de desbloqueo

**Comentarios**
Llamaremos "Primitiva" a toda instrucción atómica que el alumno puede utilizar en las misiones dentro del videojuego (Por ejemplo: mover, saltar, etc.).

## RI-13 Información de estructuras de control

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Agregar estructura condicional
- UC-XX Agregar estructura repetitiva
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a las estructuras de control (condicional y repetitivas) dentro del sistema, las cuales son representadas como "Estrategias" en lenguaje gamificado. En concreto:

**Datos específicos**

- Id de estructura de control
- Nombre de la estructura de control
- Descripción de la estructura de control
- Tipo de estructura de control (condicional o repetitiva)
- Sintaxis de la estructura de control
- Nivel requerido para desbloqueo
- Sprite (imagen/ícono) de la estructura
- Estado de desbloqueo

## RI-14 Información de objeto de inventario

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Consultar manual del héroe
- UC-XX Consultar inventario

**Descripción**
El sistema deberá almacenar la información correspondiente a los objetos que tendrá el alumno (jugador) en su inventario. En concreto:

**Datos específicos**

- Id del objeto de inventario
- Nombre del objeto de inventario
- Descripción del objeto de inventario
- Sprite (imagen/ícono) del objeto de inventario
- Valor acumulable del objeto (numero entero positivo)

## RI-15 Información de procedimientos

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Agregar procedimiento
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a los procedimientos genéricos que el alumno (jugador) tendrá disponible para utilizar dentro del videojuego, representadas como "Habilidades especiales" en lenguaje gamificado. En concreto:

**Datos específicos**

- Id del procedimiento
- Nombre del procedimiento
- Descripción del procedimiento
- Sintaxis del procedimiento
- Cuerpo del procedimiento
- Nivel requerido para desbloqueo

**Comentarios**
El cuerpo del procedimiento sería todas las instrucciones que realizará el procedimiento. Para evitar complejidades en la versión final del videojuego, se limitó a que los procedimientos genéricos no posean parámetros.

## RI-16 Información de operadores lógicos y matemáticos

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**

- UC-XX Agregar estructura condicional
- UC-XX Agregar estructura repetitiva
- UC-XX Declarar variable
- UC-XX Asignar valor a variable
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a los operadores lógicos (AND, OR y NOT) y matemáticos (+, -, \*, /, <, >, ==, <=, >=, !=, :=) dentro del sistema. En concreto:

**Datos específicos**

- Id del operador
- Nombre del operador
- Descripción del operador
- Sintaxis del operador

## RI-17 Información del feedback generado

**Objetivos asociados**

- OBJ-04 Proveer feedback formativo inmediato

**Requisitos asociados**

- UC-XX Resolver misión
- UC-XX Ejecutar misión
- UC-XX Evaluar misión
- UC-XX Generar feedback
- UC-XX Aceptar feedback

**Descripción**
El sistema deberá almacenar la información correspondiente del feedback formativo generado en la resolución exitosa de una misión. En concreto:

**Datos específicos**

- Id del feedback
- Misión en la que se originó el feedback
- Texto explicativo formativo del feedback
- Código "antes" del feedback
- Código "después" con la mejora propuesta
- Aceptado o no (Booleano) que indica si el alumno aceptó o no la mejora.

**Comentarios**

- Pueden generarse múltiples feedbacks por una misma ejecución si hay más de una mejora sugerida.
- El feedback será accesible desde el historial de la misión (para revisión futura del alumno).

## RI-18 Información de auditoría

**Objetivos asociados**

- OBJ-09 Gestión de auditoría

**Requisitos asociados**

- UC-XX Auditoría

**Descripción**
EL sistema deberá almacenar la información a auditar correspondiente a los diferentes eventos dentro del sistema. En concreto:

**Datos específicos**

- Fecha y hora del evento
- ID o nombre del usuario que realizó la acción
- Rol del usuario
- Tipo de evento
- Recurso afectado
- Estado anterior del recurso
- Estado posterior del recurso
