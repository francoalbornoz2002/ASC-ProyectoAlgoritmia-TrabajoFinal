# Requisitos Funcionales del sistema

**Versión:** 1.3
**Fecha:** 28/06/2025
**Autor(es):** Franco Andrés Albornoz

En este documento contiene la lista de los requisitos funcionales, expresado en forma tradicional.

---

## RF-01 Gestión de usuarios
**Objetivos relacionados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-04 Información de docentes
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir la alta, baja y modificación de usuarios asi como también la asignación de los roles de administrador, docente y alumno.

## RF-02 Ingresar a cursos
**Objetivos relacionados**
- OBJ-08 Gestión Académica

**Requisitos asociados**
- RI-03 Información de cursos 

**Descripción**
El sistema debe permitir a los alumnos ingresar a cursos colocando el nombre del curso y contraseña específicos y proporcionados por el docente.

## RF-03 Aceptar ingreso de alumnos al curso
**Objetivos relacionados**
- OBJ-08 Gestión Académica

**Requisitos asociados**
- RI-03 Información de cursos
- RI-05 Información de alumnos 

**Descripción**
El sistema debe permitir a los docentes, a modo de seguridad, aceptar a cada alumno que haya solicitado ingresar al curso verificando su identidad.

## RF-04 Resolver misiones
**Objetivos relacionados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
- RI-08 Información de capítulos
- RI-09 Información de misiones
- RI-12 Información de acciones
- RI-13 Información de tácticas
- RI-14 Información de objeto de inventario
- RI-15 Información de habilidades especiales
- RI-16 Información de operadores lógicos y matemáticos

**Descripción**
El sistema debe permitir a los alumnos resolver las misiones utilizando todas las acciones, tácticas, objetos y habilidades especiales disponibles en el lenguaje de programación gamificado, pudiendo el alumno consultar en todo momento el manual del heroe que contiene la sintaxis y semántica de cada instrucción.

## RF-05 Ejecutar y visualizar misiones
**Objetivos relacionados**
- OBJ-03 Ofrecer ejecución y visualización de la solución en tiempo real

**Requisitos asociados**
- RI-10 Información del escenario
- RI-11 Información de enemigos, obstáculos y objetos del escenario

**Descripción**
El sistema debe permitir la ejecución de la solución del alumno diseñada con el lenguaje de programación gamificado ejecutando y visualizando cada instrucción en tiempo real en el escenario de la misión.

## RF-06 Generar feedback formativo
**Objetivos relacionados**
- OBJ-04 Proveer feedback formativo inmediato

**Requisitos asociados**
- RI-17 Información del feedback generado

**Descripción**
El sistema deberá analizar y realizar automáticamente mejoras y optimizaciones a la solución de un alumno cuando éste resuelva una misión de manera exitosa, presentando el código antes y despues a la mejora con un texto explicativo a modo formativo para que el alumno pueda comprender el por qué de la mejora propuesta. El sistema deberá guardar el feedback generado en el historial de la misión para consulta posterior. El alumno podrá aceptar o no la mejora para aplicarla a su solución.

## RF-06 Gestionar sesiones de refuerzo
**Objetivos relacionados**
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
- RI-05 Información de docentes
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-07 Información de sesiones de refuerzo

**Descripción**
El sistema debe permitir al docente la creación, modificación y eliminación de sesiones de refuerzo y debe realizar la generación automática de la sesión de refuerzo semanal todos los domingos a las 20:00 PM notificando al docente y alumnos involucrados.

## RF-07 Reportes de progreso de alumnos en la historia
**Objetivos relacionados**
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos

**Descripción**
El sistema debe permitir al docente visualizar y generar reportes de las estadísticas de progreso de todos los alumnos en la historia general de cada curso que esté a cargo, pudiendo aplicar los siguientes filtros:
- Búsqueda por nombre y/o apellido del alumno
- Porcentaje de avance en la historia
- Promedio de intentos por misión
- Días de inactividad

## RF-07 Reportes de progreso de alumnos en un capítulo
**Objetivos relacionados**
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-08 Información de capítulos

**Descripción**
El sistema debe permitir al docente visualizar y generar reportes de las estadísticas de progreso de todos los alumnos en cada capítulo de la historia de cada curso que esté a cargo, aplicar los siguientes filtros:
- Capítulo
- Búsqueda por nombre y/o apellido del alumno
- Porcentaje de avance en el capítulo
- Promedio de intentos por misión en el capítulo
- Días de inactividad


## RF-XX ---
**Objetivos relacionados**
- 

**Requisitos asociados**
- 

**Descripción**


Gestión de cursos
Gestión de instituciones

Generación de feedback formativo
