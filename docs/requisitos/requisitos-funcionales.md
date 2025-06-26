# Requisitos Funcionales del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
**Autor(es):** Franco Andrés Albornoz

En este documento contiene la lista de los requisitos funcionales, expresado en forma tradicional.

---

## RF-01 Registro de alumnos
**Objetivos relacionados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir el registro de los alumnos via web mediante formulario tradicional o con autenticación con Google (OAuth 2.0).

## RF-02 Ingresar a cursos
**Objetivos relacionados**
- OBJ-08 Gestión Académica

**Requisitos asociados**
- RI-03 Información de cursos 

**Descripción**
El sistema debe permitir a los alumnos ingresar a cursos colocando el nombre del curso y la contraseña proporcionada por el docente.

## RF-03 Aceptar ingreso de alumnos al curso
**Objetivos relacionados**
- OBJ-08 Gestión Académica

**Requisitos asociados**
- RI-03 Información de cursos
- RI-05 Información de alumnos 

**Descripción**
El sistema debe permitir a los docentes, a modo de seguridad, aceptar a cada alumno que haya solicitado ingresar al curso verificando su identidad.

## RF-04 Resolver, ejecutar y visualizar misiones
**Objetivos relacionados**
- OBJ-01 Crear un entorno de videojuegos con gamificación
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-03 Ofrecer ejecución y visualización de la solución en tiempo real

**Requisitos asociados**
- RI-08 Información de capítulos
- RI-09 Información de misiones
- RI-12 Información de acciones
- RI-13 Información de tácticas
- RI-14 Información de objeto de inventario
- RI-15 Información de habilidades especiales
- RI-16 Información de operadores lógicos y matemáticos

**Descripción**
El sistema debe permitir a los alumnos resolver las misiones mediante el lenguaje de programación gamificado y ejecutar y visualizar en tiempo real de la solución en el escenario de videojuego.

## RF-05 Generar feedback formativo
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
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-07 Información de sesiones de refuerzo

**Descripción**
El sistema debe permitir al docente la creación, modificación y eliminación de sesiones de refuerzo, adicionalmente debe soportar la generación automática de las mismas todos los domingos a las 20:00 PM.

## RF-07 Visualizar progreso de alumnos
**Objetivos relacionados**
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos

**Descripción**
El sistema debe permitir al docente visualizar las estadísticas de progreso de todos los alumnos de cada curso que esté a cargo pudiendo filtrar por: nombre y/o apellido del alumno, capítulo, porcentaje de avance en la historia, promedio de intentos por misión y ultima actividad (Activo hace x día(s)).


## RF-XX ---
**Objetivos relacionados**
- 

**Requisitos asociados**
- 

**Descripción**


Gestión de cursos
Gestión de instituciones

Generación de feedback formativo
