# Requisitos de Información del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
**Autor(es):** Franco Andrés Albornoz

En este documento se detalla la lista de requisitos de almacenamientos y de restricciones de información que se haya identificado.

---

## IRQ-01 Información de usuarios
**Objetivos asociados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- UC-XX Alta usuario
- UC-XX Modificar usuario
- UC-XX Baja usuario
- UC-XX Buscar usuario
- UC-XX Iniciar sesión

**Descripción**
El sistema deberá almacenar la información correspondiente a los usuarios del sistema. En concreto: 

**Datos específicos**
- Id de usuario
- Nombre de usuario
- Contraseña de usuario
- Correo electrónico
- Rol de usuario (alumno, docente o administrador)

## IRQ-02 Información de instituciones
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

## IRQ-03 Información de cursos
**Objetivos asociados**
- OBJ-07 Gestión Académica

**Requisitos asociados**
- UC-XX Alta de curso
- UC-XX Modificar curso
- UC-XX Baja de curso
- UC-XX Buscar curso
- UC-XX Ingresar a un curso

**Descripción**
El sistema deberá almacenar la información correspondiente a los cursos del sistema. En concreto:

**Datos específicos**
- Id de curso
- Nombre del curso
- Institución a la que pertenece el curso
- Docente/s a cargo del curso
- Alumnos asociados al curso
- Contraseña para el ingreso al curso

## IRQ-04 Información de docentes
**Objetivos asociados**
- OBJ-07 Gestión Académica
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- UC-XX Alta de docente
- UC-XX Modificar docente
- UC-XX Baja de docente
- UC-XX Buscar docente

**Descripción**
El sistema deberá almacenar la información correspondiente a los docentes del sistema. En concreto:

**Datos específicos**
- Id de docente
- Nombre/s y Apellido/s del docente
- Género (Masculino, Femenino u Otro)
- Instituciones a la que pertenece el docente
- Cursos a cargo del docente

## IRQ-05 Información de alumnos
**Objetivos asociados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- UC-XX Registrar alumno
- UC-XX Modificar alumno
- UC-XX Baja alumno
- UC-XX Buscar alumno

**Descripción**
El sistema deberá almacenar la información correspondiente a los alumnos dentro del sistema. En concreto:

**Datos específicos**
- Id de alumno
- Nombre/s y Apellido/s del alumno
- Género (Masculino, Femenino u Otro)
- Cursos a los que está asociado

## IRQ-06 Información de estadísticas de progreso de los alumnos
**Objetivos asociados**
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
- UC-XX Consultar mis estadísticas
- UC-XX Consultar progreso de alumnos
- UC-XX Generar reporte de progreso de alumnos

**Descripción**
El sistema deberá almacenar la información correspondiente a las estadísticas (progreso) de juego de cada alumno dentro del sistema. En concreto:

**Datos específicos**
- Puntos de experiencia (EXP) obtenidos
- Nivel actual
- Misión actual
- Cantidad de misiones completadas
- Cantidad de estrellas obtenidas
- Promedio de intentos por misión
- Porcentaje de avance en un episodio
- Porcentaje de avance en la historia
- Fecha y hora del ultimo ingreso al sistema.

## IRQ-07 Información de sesiones de refuerzo
**Objetivos asociados**
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
- UC-XX Consultar progreso de alumnos
- UC-XX Generar sesión de refuerzo
- UC-XX Confirmar asistencia a sesión de refuerzo
- UC-XX Confirmar realización de sesión de refuerzo

**Descripción**
El sistema deberá almacenar la información correspondiente a las sesiones de refuerzo de contenidos dentro del sistema. En concreto:

**Datos específicos**
- Id sesión de refuerzo
- Temas a reforzar
- Duración de la sesión en minutos
- Modalidad de la sesión (presencial o virtual)
  - Si es virtual: URL adjunta de la reunión/meet/zoom
- Docente a cargo de la sesión de refuerzo
- Alumnos involucrados en la sesión de refuerzo


## IRQ-08 Información de capítulos
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
- UC-XX Habilitar capítulo

**Descripción**
El sistema deberá almacenar la información correspondiente a los capítulos (temas) de la historia dentro del sistema. En concreto:

**Datos específicos**
- Id de capítulo
- Nombre del capítulo
- Cantidad de misiones del capítulo
- Nivel requerido para desbloqueo
- Habilitación del docente (habilitado o no habilitado)

## IRQ-09 Información de misiones
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
- UC-XX Resolver misión

**Descripción**
El sistema deberá almacenar la información correspondiente a las misiones (ejercicios) de cada capítulo de la historia dentro del sistema. En concreto:

**Datos específicos**
- Id de misión
- Nombre de la misión
- Enunciado de la misión
- Dificultad de la misión (Fácil, Normal o Difícil)
- Nivel requerido para desbloqueo

## IRQ-10 Información de acciones
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a las acciones ("primitivas" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de la acción
- Nombre de la acción
- Sintaxis de la acción
- Semántica de la acción
- Nivel requerido para desbloqueo

## IRQ-11 Información de tácticas
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a las tácticas ("estructuras de control" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de táctica
- Nombre de la táctica
- Sintaxis de la táctica
- Semántica de la táctica
- Nivel requerido para desbloqueo

## IRQ-12 Información de objetos
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a los objetos dentro del sistema. En concreto:

**Datos específicos**
- Id de objeto
- Nombre del objeto
- Sintaxis del objeto
- Semántica del objeto
- Tipo de objeto: (del entorno o de inventario)
- Valor numérico del objeto (número entero)
- Nivel requerido para desbloqueo

## IRQ-13 Información de habilidades especiales
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a las habilidades especiales ("procedimientos y funciones" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de habilidad especial
- Nombre de la habilidad especial
- Sintaxis de la habilidad especial
- Semántica de la habilidad especial
- Parámetros de la habilidad especial
- Estructura de la habilidad especial (acciones, tácticas y objetos)
- Nivel requerido para desbloqueo

## IRQ-14 Información de condicionales
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a los condicionales (AND, OR y NOT) dentro del sistema. En concreto:

**Datos específicos**
- Id del condicional
- Nombre del condicional
- Sintaxis del condicional
- Semántica del condicional
- Nivel requerido para desbloqueo

## IRQ-15 Información de proposiciones
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar libro de habilidades

**Descripción**
El sistema deberá almacenar la información correspondiente a las proposiciones disponibles para actuar como condiciones en las estructuras de control (Si-Sino, Mientras y Repetir) dentro del sistema. En concreto:

**Datos específicos**
- Id de la proposición
- Nombre de la proposición
- Sintaxis del condicional
- Semántica del condicional
- Valor predeterminado (verdadeo o falso)
- Nivel requerido para desbloqueo

## IRQ-16 Información de auditoría
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