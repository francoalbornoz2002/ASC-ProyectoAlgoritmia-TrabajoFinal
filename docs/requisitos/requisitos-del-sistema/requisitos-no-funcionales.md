# Requisitos No Funcionales del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
**Autor(es):** Franco Andrés Albornoz

---

## RNF-01 Progreso offline y sincronización

**Objetivos relacionados**

- OBJ-10 Persistir el progreso de manera local y sincronizarlo luego

**Requisitos asociados**

- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-07 Información de dificultades de los alumnos
- RI-09 Información de capítulos
- RI-10 Información de misiones
- RF-05 Visualizar el progreso de alumnos
- RF-06 Determinar las dificultades específicas de los alumnos

**Descripción**
El sistema deberá permitir que los alumnos puedan avanzar en la resolución de misiones dentro del videojuego sin necesidad de conexión a internet permanente. El progreso alcanzado (misiones completadas, intentos, estrellas obtenidas y experiencia) deberá almacenarse de forma local. Cuando se complete una misión o se cierre sesión en el videojuego, se deberán sincronizar los datos de progreso locales junto con la recopilación de errores de cada alumno a la plataforma web, garantizando así continuidad en el seguimiento académico por parte del docente y manteniendo la trazabilidad de la experiencia de aprendizaje.

## RNF-02 Auditoría

**Objetivos relacionados**

- OBJ-09 Gestionar la auditoría del sistema

**Requisitos asociados**

- RI-01 Información de usuarios
- RI-02 Información de instituciones
- RI-03 Información de cursos
- RI-04 Información de docentes
- RI-05 Información de alumnos
- RI-11 Información de auditoría

**Descripción**
El sistema deberá registrar en una bitácora de auditoría todas las acciones críticas realizadas sobre los módulos de usuarios, instituciones, cursos, sesiones de refuerzo, docentes y alumnos. Estas acciones incluirán altas, bajas, modificaciones y asignaciones, indicando el usuario que realizó la acción, la fecha y hora exacta, y los datos afectados.
El módulo de auditoría solo estará disponible para el administrador del sistema, éste debe permitir consultar, filtrar y exportar los registros según diferentes criterios (tipo de acción, entidad afectada, responsable y rango de fechas).

## RNF-03 Seguridad de la información

**Objetivos relacionados**

- OBJ-07 Gestionar de instituciones y cursos
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- RI-01 Información de usuarios
- RI-04 Información de docentes
- RI-05 Información de alumnos
- RI-11 Información de auditoría
- RF-01 Gestionar usuarios
- RF-08 Registro y autenticación con Google

**Descripción**
El sistema deberá garantizar la seguridad en el manejo de credenciales mediante transmisión cifrada (HTTPS), almacenamiento de contraseñas con hashing seguro (bcrypt) y validación de accesos según rol. La autenticación con Google deberá seguir el estándar OAuth 2.0, validando tokens en cada sesión. Se deberán aplicar restricciones ante intentos fallidos, control de sesiones activas y validaciones contra ataques comunes como inyecciones SQL o XSS. El videojuego validará el inicio de sesión vía API segura sin exponer credenciales localmente.
