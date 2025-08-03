# Requisitos Funcionales del sistema

**Versión:** 2.0
**Fecha:** 02/08/2025
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
El sistema debe permitir la alta, baja y modificación de usuarios, la asignación de los roles de administrador, docente y alumno y el inicio de sesión en el sistema mediante usuario y contraseña y autenticación con Google en caso de alumnos.

## RF-02 Gestionar instituciones

**Objetivos relacionados**

- OBJ-07 Gestión Académica

**Requisitos asociados**

- RI-02 Información de instituciones

**Descripción**
El sistema debe permitir, para el rol de administrador, la alta, baja y modificación de las instituciones educativas.

## RF-03 Gestión de cursos

**Objetivos relacionados**

- OBJ-07 Gestión Académica

**Requisitos asociados**

- RI-03 Información de cursos
- RI-04 Información de docentes
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir, para el rol de administrador, la alta, baja y modificación de cursos asi como también las acciones de asignar docentes a cursos y removerlos cuando sea necesario.
El sistema debe permitir, para el rol de docente, cambiar la contraseña de acceso al curso y aceptar las solicitudes de ingreso al curso de cada alumno verificando su identidad.
El sistema debe permitir, para el rol de alumno, ingresar a cursos con el nombre del curso y contraseña proporcionados por el docente.

## RF-04 Gestionar sesiones de refuerzo

**Objetivos relacionados**

- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- RI-05 Información de docentes
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-08 Información de sesiones de refuerzo

**Descripción**
El sistema debe permitir al docente la creación, modificación y cancelación de sesiones de refuerzo y la generación automática de la sesión de refuerzo semanal todos los sábados a las 18:00 hs notificando por correo electrónico al docente y alumnos involucrados.

## RF-05 Visualizar el progreso de alumnos

**Objetivos relacionados**

- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-09 Información de capítulos

**Descripción**
El sistema debe permitir al docente visualizar y generar reportes de las estadísticas de progreso de todos los alumnos, tanto en la historia general como en cada capítulo, de cada curso que esté a cargo, pudiendo aplicar los siguientes filtros:

- Búsqueda por nombre y/o apellido del alumno
- Capítulo específico
- Porcentaje de avance
- Promedio de intentos por misión
- Días de inactividad

**Comentarios**
El sistema tambien deberá realizar la generación automática de un reporte de progreso semanal de los alumnos todos los sábados a las 18:00 hs enviandola por correo electrónico a todos los docentes del curso.

## RF-06 Determinar las dificultades específicas de los alumnos

**Objetivos relacionados**

- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-05 Información de alumnos
- RI-07 Información de dificultades de los alumnos

**Descripción**
El sistema debe analizar y determinar las dificultades que posean los alumnos a partir de los recopilación de errores en resolución de misiones realizada por el videojuego. Además, estas deben poder ser visualizadas por los docentes tanto en el perfil del alumno como en las sesiones de refuerzo, pudiendo filtrar por tipo de dificultad y estado de gravedad.

## RF-07 Controlar la curva de aprendizaje mediante habilitación de capitulos

**Objetivos relacionados**

- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-09 Información de capítulos

**Descripción**
El sistema debe permitir al docente habilitar y finalizar los capítulos a medida que se vayan dando los contenidos en la materia para garantizar una curva de aprendizaje controlada y seguimiento académico ordenado de los alumnos.

**Comentarios**
Un capítulo estará "En curso" mientras el capitulo siguiente no sea habilitado por el docente. Si el docente habilita un capítulo, el anterior se considerará con estado "Finalizado". El docente solo podrá habilitar los capítulos de manera secuencial y NO desordenada. Los alumnos podrán jugar misiones que no hayan completado de capitulos finalizados igualmente.

## RF-08 Registro y autenticación con Google

**Objetivos relacionados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- RI-01 Información de usuarios
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir a los alumnos registrarse y autenticarse utilizando su cuenta de Google mediante el protocolo OAuth 2.0. Durante el registro, se solicitará acceso a los datos básicos del perfil (nombre, correo electrónico) y, en caso de ser un nuevo usuario, se completarán los datos restantes requeridos por la plataforma. Una vez registrado, el alumno podrá iniciar sesión y autenticarse posteriormente utilizando el mismo método.