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

- OBJ-07 Gestionar de instituciones y cursos

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

- OBJ-07 Gestionar de instituciones y cursos

**Requisitos asociados**

- UC-XX Alta de curso
- UC-XX Modificar curso
- UC-XX Baja de curso
- UC-XX Buscar curso
- UC-XX Solicitar ingreso a curso
- UC-XX Asignar docente a curso
- UC-XX Aprobar solicitud de ingreso al curso
- UC-XX Cambiar contraseña de acceso a curso
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

- OBJ-07 Gestionar de instituciones y cursos
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- UC-XX Modificar datos personales
- UC-XX Buscar docente

**Descripción**
El sistema deberá almacenar la información correspondiente a los docentes del sistema. En concreto:

**Datos específicos**

- Id de docente (Id de usuario)
- Nombre/s y Apellido/s del docente
- Género (Masculino, Femenino u Otro)
- Institucion/es a la que pertenece el docente
- Cursos a cargo del docente
- Sesiones de refuerzo creadas y dictadas por el docente

## RI-05 Información de alumnos

**Objetivos asociados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- UC-XX Registrarse
- UC-XX Modificar datos personales
- UC-XX Buscar alumno

**Descripción**
El sistema deberá almacenar la información correspondiente a los alumnos dentro del sistema. En concreto:

**Datos específicos**

- Id de alumno (Id de usuario)
- Nombre/s y Apellido/s del alumno
- Género (Masculino, Femenino u Otro)
- Cursos a los que está asociado
- Dificultades que posee
- Método de registro

**Comentarios**
Las dificultades de un alumno son aquellos temas puntuales en los cuales se le dificulta al diseñar los algoritmos para resolver las misiones. Por ejemplo, una dificultad podría ser "Manejo de variables", "Condicionales", etc.

## RI-06 Información de estadísticas de progreso de los alumnos

**Objetivos asociados**

- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- UC-XX Consultar mi progreso
- UC-XX Consultar progreso de alumnos
- UC-XX Generar reporte de progreso de alumnos

**Descripción**
El sistema deberá almacenar la información correspondiente a las estadísticas de progreso de cada alumno en el videojuego. En concreto:

**Datos específicos**

- Id de alumno (Id de usuario)
- Nombre/s y Apellido/s del alumno
- Nivel actual
- Total de puntos de experiencia (EXP) obtenidos
- Capítulo y misión actual
- Cantidad de misiones completadas
- Cantidad de estrellas obtenidas
- Promedio de intentos por misión
- Porcentaje de avance en un capítulo
- Porcentaje de avance en la historia
- Fecha y hora del ultimo inicio de sesión en el videojuego.
- Cantidad de días de inactividad

## RI-07 Información de dificultades de los alumnos

**Objetivos asociados**

- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- UC-XX Consultar dificultades de alumno

**Descripción**
El sistema deberá almacenar la información de las dificultades específicas de cada alumno dentro del sistema. Estas dificultades se determinarán a partir del registro de errores comunes de un alumno que el videojuego envíe a la plataforma web. En concreto:

**Datos específicos**
- Id de dificultad
- Tipo de dificultad
- Descripción específica de la dificultad
- Cantidad de errores relacionados a esa dificultad
- Gravedad de la dificultad

**Comentarios**
Los tipos de dificultades de los alumnos son: Secuencia, Lógica, Estructuras de Control, Variables y Procedimientos. La descripción implica detallar especificamente en qué tiene dificultad el alumno, por ejemplo: Si tiene dificultades en "Lógica" -> Podría hacer un mal uso de los conectivos lógicos, variables mal evaluadas, condiciones siempre falsas, etc.

## RI-08 Información de sesiones de refuerzo

**Objetivos asociados**

- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- UC-XX Consultar progreso de alumnos
- UC-XX Crear sesión de refuerzo
- UC-24 Modificar sesión de refuerzo
- UC-XX Cancelar sesión de refuerzo
- UC-XX Buscar sesión de refuerzo
- UC-XX Confirmar asistencia a sesión de refuerzo
- UC-XX Aceptar sesión de refuerzo automática

**Descripción**
El sistema deberá almacenar la información correspondiente a las sesiones de refuerzo de contenidos dentro del sistema. En concreto:

**Datos específicos**

- Id sesión de refuerzo
- Docente a cargo de la sesión de refuerzo
- Alumnos involucrados y sus dificultades específicas
- Descripción de la sesión
- Fecha, hora y duración en minutos de la sesión
- Modalidad de la sesión (presencial o virtual)
  - Si es virtual: URL de la reunión en Google Meet o Zoom
  - Si es presencial: Momento de realización (antes o después de la clase)

## RI-09 Información de capítulos

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
- Tema/s clave del capítulo (Secuencia, Lógica, Estructuras de Control, Variables o Procedimientos)
- Cantidad de misiones del capítulo
- Habilitación del docente (habilitado o no)
- Estado del capítulo (En curso o Finalizado)

## RI-10 Información de misiones

**Objetivos asociados**

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**

- UC-XX Buscar misión

**Descripción**
El sistema deberá almacenar la información correspondiente a las misiones (ejercicios) de cada capítulo de la historia dentro del sistema. En concreto:

**Datos específicos**

- Id de misión
- Nombre de la misión
- Capítulo al que pertenece la misión
- Dificultad de la misión (Fácil, Normal o Difícil)
- Descripción (Enunciado) de la misión
- Cantidad y porcentaje de alumnos que completaron la misión
- Promedio de la puntuación obtenida por los alumnos

## RI-11 Información de auditoría

**Objetivos asociados**

- OBJ-09 Gestionar la auditoría del sistema

**Requisitos asociados**

- UC-XX Consultar registros de auditoría
- UC-18 Exportar registros de auditoría

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