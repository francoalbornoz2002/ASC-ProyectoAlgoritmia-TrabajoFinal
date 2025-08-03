# Modelo de Casos de Uso

**Versión:** 2.1
**Fecha:** 01/08/2025
**Autor(es):** Franco Andrés Albornoz

---

## Actores del sistema

### ACT-01 Alumno

Representa a los estudiantes que utilizarán el videojuego desarrollado en Godot como herramienta principal para practicar y afianzar los contenidos de la materia "Algoritmos y Estructuras de Datos I". En este caso, se realizará la descripcion de Alumno respecto a sus funcionalidades en la plataforma web.

Los alumnos podrán registrarse en la plataforma web mediante un formulario tradicional o autenticarse con Google. Una vez registrados, inciarán sesión y se uniran a un curso ingresando un nombre de curso y contraseña provistos por el docente. Una vez unido a un curso, podrán descargar el videojuego e iniciar sesión con su usuario y contraseña para establecer sus datos y sincronizar el progreso que realicen.

Dentro de la plataforma web, podrán realizar las siguientes acciones:

- Registrarse e iniciar sesión con Google
- Unirse a un curso
- Cambiar la contraseña de usuario.
- Consultar recursos de apoyo.
- Ver estadísticas más detalladas de su rendimiento.
- Descargar el videojuego para ejecutarlo en su PC.
- Confirmar asistencia a sesiones de refuerzo, ya sea desde la web o a través del enlace recibido por correo electrónico.

---

### ACT-02 Docente

Representa al personal docente encargado de dictar la materia y brindar seguimiento académico a los alumnos. Los docentes utilizarán exclusivamente la plataforma web, donde tendrán acceso a diversas funcionalidades de seguimiento.

Sus principales responsabilidades incluyen:

- Gestionar los cursos a su cargo (asignados previamente por el administrador) de manera limitada.
  - Modificar la contraseña de acceso del curso para nuevos alumnos.
  - Validar y aceptar solicitudes de ingreso de alumnos a sus cursos.
- Visualizar en tiempo real el avance y desempeño de sus alumnos (misiones resueltas, dificultades específicas, actividad reciente, entre otros).
- Generar reportes de progreso con diferentes filtros.
- Programar sesiones de refuerzo para alumnos con bajo rendimiento, dificultades o inactividad prolongada.

---

### ACT-03 Administrador

Representa al administrador general del sistema. Es responsable de mantener la infraestructura organizativa y funcional del entorno académico.

Entre sus funciones se destacan:

- Registrar y gestionar instituciones educativas.
- Crear cursos y asignar docentes a los mismos.
- Gestionar usuarios del sistema (docentes, alumnos y otros administradores en el futuro).
- Auditar cambios realizados en las distintas entidades del sistema: altas, bajas, modificaciones de usuarios, cursos e instituciones.

En esta versión inicial, se prevé que exista un único administrador central. En versiones futuras, podría habilitarse un esquema con administradores por institución.

---

### ACT-04 Google OAuth 2.0
Representa al servicio externo de autenticación de Google utilizado por la plataforma web para permitir el inicio de sesión o registro de alumnos mediante sus cuentas de Google. Es un actor externo que colabora en los procesos de autenticación sin intervención directa del usuario sobre sus mecanismos internos.

---

### ACT-05 Videojuego
Representa al videojuego desarrollado en Godot que enviará los datos de progreso de cada alumno a la plataforma web para que sea visualizado por los docentes. Recibirá los datos de la web en caso de que se tenga que sincronizar el progreso de un alumno en el videojuego.


<!--
## Casos de uso del sistema

### Administrador

#### Gestión de usuarios

- **UC-01** Alta usuario  
- **UC-02** Modificar usuario  
  - INCLUDE: **UC-03** Buscar usuario  
- **UC-04** Baja usuario  
  - INCLUDE: **UC-03** Buscar usuario  
- **UC-05** Iniciar sesión

#### Gestión de instituciones

- **UC-06** Alta de institución  
- **UC-07** Modificar institución  
  - INCLUDE: **UC-08** Buscar institución  
- **UC-09** Baja de institución  
  - INCLUDE: **UC-08** Buscar institución  

#### Gestión de cursos

- **UC-10** Alta de curso  
- **UC-11** Modificar curso  
  - INCLUDE: **UC-12** Buscar curso  
- **UC-13** Baja de curso  
  - INCLUDE: **UC-12** Buscar curso  
- **UC-14** Asignar docente a curso  
  - INCLUDE: **UC-15** Buscar docente
- **UC-16** Remover docente de curso
  - INCLUDE: **UC-15** Buscar docente

#### Auditoría

- **UC-17** Consultar registros de auditoría
  - EXTEND: **UC-18** Exportar registros de auditoría

---

### Docentes

#### Seguimiento académico

- **UC-19** Consultar progreso de alumnos
  - EXTEND: **UC-20** Ver progreso general (historia)
  - EXTEND: **UC-21** Ver progreso por capítulo
- **UC-22** Generar reporte de progreso de alumnos

#### Gestionar sesiones de refuerzo
- **UC-23** Crear sesión de refuerzo
- **UC-24** Modificar sesión de refuerzo
  - INCLUDE: **UC-25** Buscar sesión de refuerzo
- **UC-26** Cancelar sesión de refuerzo
  - INCLUDE: **UC-25** Buscar sesión de refuerzo 
- **UC-27** Aceptar sesión de refuerzo automática

#### Gestionar cursos (docente)
- **UC-28** Definir días y horarios del curso
- **UC-29** Cambiar contraseña de acceso a curso
- **UC-30** Aprobar solicitud de ingreso al curso
- **UC-31** Habilitar capítulo
  - INCLUDE: **UC-32** Buscar capítulo
- **UC-33** Consultar dificultades de alumno
  - INCLUDE: **UC-34** Buscar alumno

#### Gestión de cuenta
- **UC-05** Iniciar sesión
- **UC-35** Modificar datos personales

### Alumnos

#### Gestión de cuenta
- **UC-36** Registrarse
  - EXTEND: **UC-37** Registro normal
  - EXTEND: **UC-38** Registro con Google
- **UC-39** Iniciar sesión
  - EXTEND: **UC-40** Iniciar sesión normal
  - EXTEND: **UC-41** Inicar sesión con Google
- **UC-35** Modificar datos personales
- **UC-42** Consultar mi progreso

#### Cursos
- **UC-43** Solicitar ingreso a curso
- **UC-44** Confirmar asistencia a sesión de refuerzo
-->


## Diagrama de Casos de Uso

### DCU de alto nivel / Diagrama de subsistemas


## Diagrama de Casos de Uso – Plataforma Web
### DCU de alto nivel / Diagrama de subsistemas








