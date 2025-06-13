# Requisitos de Información del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
**Autor(es):** Franco Andrés Albornoz

---

En este documento se detalla la lista de requisitos de almacenamientos y de restricciones de información que se haya identificado.

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
- Ciudad donde se encuentra la institución
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

**Descripción**
El sistema deberá almacenar la información correspondiente a los cursos del sistema. En concreto:

**Datos específicos**
- Id de curso
- Nombre del curso
- Institución a la que pertenece el curso
- Docente/s a cargo del curso
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
- Institución a la que pertenece el docente
- Cursos a cargo del docente

## IRQ-05 Información de alumnos
**Objetivos asociados**
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- UC-XX Registrar alumno
- UC-XX Modificar alumno
- UC-XX Baja alumno
- UC-XX Buscar alumno

**Descripción**
El sistema deberá almacenar la información correspondiente a los alumnos y sus estadísticas de progreso dentro del sistema. En concreto:

**Datos específicos**
- Id de alumno
- Nombre/s y Apellido/s del alumno

## IRQ-06 Información de sesiones de refuerzo
**Objetivos asociados**
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**
-

**Descripción**
xxx

**Datos específicos**
-

## IRQ-07 Información de episodios
**Objetivos asociados**
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
-

**Descripción**
xxx

**Datos específicos**
-

## IRQ-08 Información de misiones
**Objetivos asociados**
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

**Requisitos asociados**
-

**Descripción**
xxx

**Datos específicos**
- 

## IRQ-09 Información de primitivas
**Objetivos asociados**
- OBJ-01 Crear un entorno de videojuegos con gamificación

**Requisitos asociados**
-

**Descripción**
xxx

**Datos específicos**
- 