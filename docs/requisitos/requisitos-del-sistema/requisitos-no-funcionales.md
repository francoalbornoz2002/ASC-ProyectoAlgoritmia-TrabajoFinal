# Requisitos No Funcionales del sistema

**Versión:** 1.0
**Fecha:** 09/06/2025
**Autor(es):** Franco Andrés Albornoz

---

## RNF-01 Narrativa y estética pixel art
**Objetivos relacionados**
- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado

**Requisitos asociados**
- RI-08 a RI-17
- RF-02 Resolver misiones
- RF-03 Ejecutar y visualizar misiones
- RF-04 Generar feedback formativo

**Descripción**
El videojuego deberá incluir una narrativa, historia y ambientación que mantenga la motivación y enganche del alumno asi como también tener una estética retro basada en pixel art, coherente en toda su interfaz.

## RNF-02 Portabilidad y rendimiento del videojuego
**Objetivos relacionados**
- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado

**Requisitos asociados**
- RI-08 a RI-17
- RF-02 Resolver misiones
- RF-03 Ejecutar y visualizar misiones
- RF-04 Generar feedback formativo

**Descripción**
El videojuego deberá estar disponible para ejecutarse en sistemas Windows y Linux y deberá ejecutarse a un mínimo de 30 FPS en equipos con hardware modesto (4 GB RAM, Intel Celeron y GPU integrada).

## RNF-03 Progreso offline y sincronización
**Objetivos relacionados**
- OBJ-10 Persistir el progreso de manera local y sincronizarlo luego

**Requisitos asociados**
- RI-05 Información de alumnos
- RI-06 Información de estadísticas de progreso de los alumnos
- RI-08 Información de capítulos
- RI-09 Información de misiones
- RI-17 Información del feedback generado
- RF-02 Resolver misiones
- RF-03 Ejecutar, visualizar y evaluar misiones
- RF-04 Generar feedback formativo

**Descripción**
El sistema deberá permitir que los alumnos puedan avanzar en la resolución de misiones dentro del videojuego sin necesidad de conexión a internet permanente. El progreso alcanzado (misiones completadas, intentos, desbloqueables, estrellas obtenidas, experiencia y feedback generado) deberá almacenarse de forma local y sincronizarse automáticamente con la base de datos central cuando se detecte conexión a internet, garantizando así continuidad en el seguimiento académico por parte del docente y manteniendo la trazabilidad de la experiencia de aprendizaje.

## RNF-04 Auditoría
**Objetivos relacionados**
- OBJ-09 Gestión de auditoría

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-02 Información de instituciones
- RI-03 Información de cursos
- RI-04 Información de docentes
- RI-05 Información de alumnos
- RI-18 Información de auditoría

**Descripción**
El sistema deberá registrar en una bitácora de auditoría todas las acciones críticas realizadas sobre los módulos de usuarios, instituciones, cursos, sesiones de refuerzo, docentes y alumnos. Estas acciones incluirán altas, bajas, modificaciones y asignaciones, indicando el usuario que realizó la acción, la fecha y hora exacta, y los datos afectados.
El módulo de auditoría solo estará disponible para el administrador del sistema, éste debe permitir consultar, filtrar y exportar los registros según diferentes criterios (tipo de acción, entidad afectada, responsable y rango de fechas).

## RNF-05 Seguridad de la información
**Objetivos relacionados**
- OBJ-07 Gestión Académica
- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**
- RI-01 Información de usuarios
- RI-04 Información de docentes
- RI-05 Información de alumnos
- RI-18 Información de auditoría
- RF-01 Gestionar usuarios
- RF-11 Registro y autenticación con Google

**Descripción**
El sistema deberá garantizar la seguridad en el manejo de credenciales mediante transmisión cifrada (HTTPS), almacenamiento de contraseñas con hashing seguro (bcrypt) y validación de accesos según rol. La autenticación con Google deberá seguir el estándar OAuth 2.0, validando tokens en cada sesión. Se deberán aplicar restricciones ante intentos fallidos, control de sesiones activas y validaciones contra ataques comunes como inyecciones SQL o XSS. El videojuego validará el inicio de sesión vía API segura sin exponer credenciales localmente.