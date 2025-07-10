# Requisitos Funcionales del sistema

**Versión:** 1.3
**Fecha:** 28/06/2025
**Autor(es):** Franco Andrés Albornoz

En este documento contiene la lista de los requisitos funcionales del sistema expresado en forma tradicional.

---

## RF-01 Gestionar usuarios
**Objetivos relacionados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-04 Información de docentes
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir la alta, baja y modificación de usuarios, la asignación de los roles de administrador, docente y alumno y el inicio de sesión en el sistema mediante usuario y contraseña.

## RF-02 Resolver misiones
**Objetivos relacionados**
- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

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

## RF-03 Ejecutar, visualizar y evaluar misiones
**Objetivos relacionados**
- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-03 Ofrecer ejecución y visualización de la solución en tiempo real
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

**Requisitos asociados**
- RI-10 Información del escenario
- RI-11 Información de enemigos, obstáculos y objetos del escenario

**Descripción**
El sistema debe permitir la ejecución de la solución del alumno diseñada con el lenguaje de programación gamificado ejecutando y visualizando cada instrucción en tiempo real en el escenario de la misión. Si se completa exitosamente, el sistema debe otorgar una puntuación de hasta 3 estrellas y asignar los puntos de experiencia correspondientes a la puntuación obtenida y actualizar el progreso de avance y nivel del alumno.

## RF-04 Generar feedback formativo
**Objetivos relacionados**
- OBJ-04 Proveer feedback formativo inmediato

**Requisitos asociados**
- RI-17 Información del feedback generado

**Descripción**
El sistema deberá analizar y realizar automáticamente mejoras y optimizaciones a la solución de un alumno cuando éste resuelva una misión de manera exitosa, presentando el código antes y despues a la mejora con un texto explicativo a modo formativo para que el alumno pueda comprender el por qué de la mejora propuesta.

**Comentarios**
El sistema deberá guardar el feedback generado en el historial de la misión para consulta posterior. El alumno podrá aceptar o no la mejora para aplicarla a su solución.

## RF-05 Gestionar sesiones de refuerzo
**Objetivos relacionados**
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
- RI-05 Información de docentes
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-07 Información de sesiones de refuerzo

**Descripción**
El sistema debe permitir al docente la creación, modificación y eliminación de sesiones de refuerzo y debe realizar la generación automática de la sesión de refuerzo semanal todos los domingos a las 20:00 PM notificando por correo electrónico al docente y alumnos involucrados.

## RF-06 Reportes de progreso de alumnos en la historia
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

El sistema tambien deberá realizar la generación automática de un reporte semanal del progreso de los alumnos todos los domingos a las 20:00 PM enviandola por correo electrónico a los docentes.

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

## RF-08 Habilitar capítulos de la historia
**Objetivos relacionados**
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**
- RI-08 Información de capítulos

**Descripción**
El sistema debe permitir al docente habilitar los capítulos de la historia a medida que se vayan dando los contenidos en la materia para garantizar una curva de aprendizaje controlada y seguimiento académico ordenado de los alumnos.

**Comentarios**
Un capítulo estará "En curso" mientras el capitulo siguiente no sea habilitado por el docente. Si el docente habilita un capítulo, el anterior se considerará con estado "Finalizado". El docente solo podrá habilitar los capítulos de manera secuencial y NO desordenada. Los alumnos podrán jugar misiones que no hayan completado de capitulos finalizados igualmente.

## RF-09 Gestión de cursos
**Objetivos relacionados**
- OBJ-07 Gestión Académica

**Requisitos asociados**
- RI-03 Información de cursos
- RI-04 Información de docentes
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir, para el rol de administrador, la alta, baja y modificación de cursos asi como también la asignación de docentes a cursos.
El sistema debe permitir, para el rol de docente, cambiar la contraseña de acceso al curso si asi lo quisiera y, a modo de seguridad, aceptar a cada alumno que haya solicitado ingresar al curso verificando su identidad.
El sistema debe permitir, para el rol de alumno, ingresar a cursos colocando el nombre del curso y contraseña específicos y proporcionados por el docente.

## RF-10 Gestionar instituciones
**Objetivos relacionados**
- OBJ-07 Gestión Académica

**Requisitos asociados**
- RI-02 Información de instituciones

**Descripción**
El sistema debe permitir, para el rol de administrador, la alta, baja y modificación de las instituciones educativas.

## RF-11 Registro y autenticación con Google
**Objetivos relacionados**
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir a los alumnos registrarse y autenticarse utilizando su cuenta de Google mediante el protocolo OAuth 2.0. Durante el registro, se solicitará acceso a los datos básicos del perfil (nombre, correo electrónico) y, en caso de ser un nuevo usuario, se completarán los datos restantes requeridos por la plataforma. Una vez registrado, el alumno podrá iniciar sesión y autenticarse posteriormente utilizando el mismo método.