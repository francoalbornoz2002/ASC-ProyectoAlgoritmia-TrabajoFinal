# Requisitos de Información del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
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
- Método de registro
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
- Estado del curso (activo/finalizado)

## RI-04 Información de docentes
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

## RI-05 Información de alumnos
**Objetivos asociados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- UC-XX Registrarse
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

## RI-06 Información de estadísticas de progreso de los alumnos
**Objetivos asociados**
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
- UC-XX Consultar mis estadísticas
- UC-XX Consultar progreso de alumnos
- UC-XX Ver progreso individual de alumno
- UC-XX Generar reporte de progreso de alumnos

**Descripción**
El sistema deberá almacenar la información correspondiente a las estadísticas (progreso) de juego de cada alumno dentro del sistema. En concreto:

**Datos específicos**
- Total de puntos de experiencia (EXP) obtenidos
- Nivel actual
- Capítulo y Misión actual
- Cantidad de misiones completadas
- Cantidad de estrellas obtenidas
- Promedio de intentos por misión
- Porcentaje de avance en un capítulo
- Porcentaje de avance en la historia
- Fecha y hora del ultimo ingreso al sistema.

## RI-07 Información de sesiones de refuerzo
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
- Docente a cargo de la sesión de refuerzo
- Alumnos involucrados
- Temas a reforzar
- Fecha y hora de la sesión
- Duración de la sesión en minutos
- Modalidad de la sesión (presencial o virtual)
  - Si es virtual: URL adjunta de la reunión/meet/zoom

## RI-08 Información de capítulos
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
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
- Habilitación del docente (habilitado o no habilitado)

## RI-09 Información de misiones
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
- UC-XX Resolver misión
- UC-XX Buscar misión

**Descripción**
El sistema deberá almacenar la información correspondiente a las misiones (ejercicios) de cada capítulo de la historia dentro del sistema. En concreto:

**Datos específicos**
- Id de misión
- Nombre de la misión
- Capítulo al que pertenece la misión
- Dificultad de la misión (Fácil, Normal o Difícil)
- Descripción (Enunciado) de la misión
- Nivel requerido para desbloqueo

## RI-10 Información del escenario
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
- UC-XX Resolver misión

**Descripción**
El sistema deberá almacenar la información correspondiente a la configuración del escenario de cada misión dentro del sistema. En concreto:

**Datos específicos**
- Id de escenario
- Mision a la que pertenece el escenario
- Cantidad de filas
- Cantidad de columnas
- Cantidad de casilleros (filas * columnas)
- Enemigos del escenario
- Obstáculos del escenario
- Objetos en el escenario

## RI-11 Información de Enemigos, obstáculos y objetos del escenario
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Resolver misión

**Descripción**
El sistema deberá almacenar la información y posición correspondiente a los enemigos, obstáculos y objetos dentro del escenario de cada misión del sistema. En concreto:

**Datos específicos**
- Id de enemigo/obstáculo/objeto
- Nombre del enemigo/obstáculo/objeto
- Descripción del enemigo/obstáculo/objeto
- Proposición del enemigo/obstáculo/objeto (para evaluar)
- Sprite (imagen) del enemigo/obstáculo/objeto
- Posición dentro del escenario (casillero)

## RI-12 Información de acciones
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a las acciones ("primitivas" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de la acción
- Nombre de la acción
- Descripción de la acción
- Sintaxis de la acción
- Nivel requerido para desbloqueo

## RI-13 Información de tácticas
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a las tácticas ("estructuras de control" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de táctica
- Nombre de la táctica
- Descripción de la táctica
- Sintaxis de la táctica
- Nivel requerido para desbloqueo

## RI-14 Información de objeto de inventario
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar manual del héroe
- UC-XX Consultar inventario

**Descripción**
El sistema deberá almacenar la información correspondiente a los objetos que tendrá el jugador en su inventario. En concreto:

**Datos específicos**
- Id del objeto de inventario
- Nombre del objeto de inventario
- Descripción del objeto de inventario
- Sprite (ícono/imagen) del objeto de inventario
- Valor acumulable del objeto (numero entero positivo)

## RI-15 Información de habilidades especiales
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a las habilidades especiales ("procedimientos y funciones" en lenguaje gamificado) dentro del sistema. En concreto:

**Datos específicos**
- Id de habilidad especial
- Nombre de la habilidad especial
- Descripción de la habilidad especial
- Sintaxis de la habilidad especial
- Parámetros de la habilidad especial
- Estructura de la habilidad especial (acciones, tácticas y objetos)
- Nivel requerido para desbloqueo

## RI-16 Información de operadores lógicos y matemáticos
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
- UC-XX Consultar manual del héroe

**Descripción**
El sistema deberá almacenar la información correspondiente a los operadores lógicos (AND, OR y NOT) y matemáticos (+, -, *, /, <, >, ==, <=, >=, !=) dentro del sistema. En concreto:

**Datos específicos**
- Id del operador
- Nombre del operador
- Descripción del operador
- Sintaxis del operador
- Nivel requerido para desbloqueo

## RI-17 Información de auditoría
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