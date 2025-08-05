# Modelo de Casos de Uso

**Versión:** 2.1
**Fecha:** 01/08/2025
**Autor(es):** Franco Andrés Albornoz

---

## Actores del sistema

### ACT-01 Alumno

Representa a los estudiantes que utilizarán el videojuego desarrollado en Godot como herramienta principal para practicar y afianzar los contenidos de la materia. En este caso, se realizará la descripcion de Alumno respecto a sus funcionalidades en la plataforma web.

Los alumnos podrán registrarse en la plataforma web mediante un formulario tradicional o autenticarse con Google. Una vez registrados, inciarán sesión y se uniran a un curso ingresando un nombre de curso y contraseña provistos por el docente. Una vez unido a un curso, podrán descargar el videojuego e iniciar sesión con su usuario y contraseña para establecer sus datos y sincronizar el progreso que realicen posteriormente asi como también sus dificultades.

Dentro de la plataforma web, podrán realizar las siguientes acciones:

- Registrarse e iniciar sesión con Google.
- Unirse a un curso.
- Cambiar la contraseña de usuario.
- Ver su progreso detallado y sus dificultades.
- Descargar el videojuego para ejecutarlo en su PC.
- Confirmar asistencia a sesiones de refuerzo, ya sea desde la web o a través del enlace recibido por correo electrónico.

### ACT-02 Docente

Representa al personal docente encargado de dictar la materia y brindar seguimiento académico a los alumnos. Los docentes utilizarán exclusivamente la plataforma web, donde tendrán acceso a diversas funcionalidades de seguimiento.

Sus principales responsabilidades incluyen:

- Gestionar los cursos a su cargo (asignados previamente por el administrador) de manera limitada.
  - Modificar la contraseña de acceso del curso para nuevos alumnos.
  - Validar y aceptar solicitudes de ingreso de alumnos a sus cursos.
- Visualizar en tiempo real el progreso y las dificultades de sus alumnos.
- Generar reportes de progreso con filtros.
- Programar sesiones de refuerzo para alumnos con bajo progreso, dificultades o inactividad prolongada.

### ACT-03 Administrador

Representa al administrador general del sistema. Es responsable de mantener la infraestructura organizativa y funcional del entorno académico.

Entre sus funciones se destacan:

- Registrar los datos de la institución educativa
- Gestionar los cursos y asignar docentes a los mismos.
- Gestionar usuarios del sistema (docentes, alumnos y otros administradores en el futuro).
- Auditar cambios realizados en las distintas entidades del sistema: altas, bajas, modificaciones de usuarios, cursos, institución y sesiones de refuerzo.

### ACT-04 Google OAuth 2.0

Representa al servicio externo de autenticación de Google utilizado por la plataforma web para permitir el inicio de sesión o registro de alumnos mediante sus cuentas de Google. Es un actor externo que colabora en los procesos de autenticación sin intervención directa del usuario sobre sus mecanismos internos.

### ACT-05 Videojuego

Representa al videojuego desarrollado en Godot que enviará los datos de progreso de cada alumno a la plataforma web para que sea visualizado por los docentes. Recibirá los datos de la web en caso de que el alumno inicie sesión la primera vez y se tenga que sincronizar el progreso en el videojuego. Tambien será el encargado de, dentro de la lógica del videojuego, registrar los errores cometidos en la resolución de misiones de los alumnos y determinar las dificultades específicas de cada uno para posteriormente enviarlas a la plataforma web para la visualización del docente.

---

## Casos de uso del sistema

#### Gestión de usuarios

- **UC-01** Alta usuario
- **UC-02** Modificar usuario
  - INCLUDE: **UC-03** Buscar usuario
- **UC-04** Baja usuario
  - INCLUDE: **UC-03** Buscar usuario
- **UC-05** Modificar datos personales

#### Gestión de institución y cursos

- **UC-06** Alta institución
- **UC-07** Modificar institución
- **UC-08** Alta curso
- **UC-09** Modificar curso
  - INCLUDE: **UC-10** Buscar curso
- **UC-11** Baja curso
  - INCLUDE: **UC-10** Buscar curso
- **UC-12** Asignar docente a curso
  - INCLUDE: **UC-13** Buscar docente
- **UC-14** Desasignar docente de curso
  - INCLUDE: **UC-13** Buscar docente
- **UC-15** Definir días y horarios del curso
- **UC-16** Cambiar contraseña de acceso a curso
- **UC-17** Unirse a un curso
  - INCLUDE: **UC-10** Buscar curso
- **UC-18** Habilitar capítulo
  - INCLUDE: **UC-19** Buscar capítulo
- **UC-20** Finalizar curso
  - INCLUDE: **UC-10** Buscar curso

#### Progreso y estadísticas

- **UC-21** Consultar progreso de alumnos
  - EXTEND: **UC-22** Ver progreso general
  - EXTEND: **UC-23** Ver progreso en capítulo
- **UC-24** Generar reporte de progreso
- **UC-25** Consultar dificultades de alumnos
- **UC-26** Sincronizar progreso de alumno
- **UC-27** Actualizar dificultades de alumno
- **UC-28** Consultar mi progreso
- **UC-29** Consultar mis dificultades

#### Gestión de sesiones de refuerzo

- **UC-30** Crear sesión de refuerzo
- **UC-31** Modificar sesión de refuerzo
  - INCLUDE: **UC-32** Buscar sesión de refuerzo
- **UC-33** Cancelar sesión de refuerzo
  - INCLUDE: **UC-32** Buscar sesión de refuerzo
- **UC-34** Indicar asistencia a sesión
  - INCLUDE: **UC-32** Buscar sesión de refuerzo

#### Auditoría

- **UC-35** Consultar registros de auditoría
  - EXTEND: **UC-36** Exportar registros de auditoría

#### Seguridad y autenticación

- **UC-37** Iniciar sesión
  - EXTEND: **UC-38** Iniciar sesión normal
  - EXTEND: **UC-39** Inicar sesión con Google
- **UC-40** Registrarse
  - EXTEND: **UC-41** Registro normal
  - EXTEND: **UC-42** Registro con Google

## Diagrama de Casos de Uso

### DCU de alto nivel / Diagrama de Subsistemas

![DCU de alto nivel o Diagrama de Subsistemas](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/DCU_AltoNivel.png)

### Subsistema Gestión de Usuarios

![Subsistema Gestión de Usuarios](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_GestionUsuarios.png)

### Subsistema Gestión de Instituciones

![Subsistema Gestión de Instituciones](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_GestionInstituciones.png)

### Subsistema Gestión de Cursos

![Subsistema Gestión de Cursos](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_GestionCursos.png)

### Subsistema Progreso y Estadísticas

![Subsistema Progreso y Estadísticas](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_ProgresoEstadisticas.png)

### Subsistema Gestión de Sesiones de refuerzo

![Subsistema Gestión de Sesiones de refuerzo](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_GestionSesionesRefuerzo.png)

### Subsistema Gestión de Auditoría

![Subsistema Gestión de Auditoría](/docs/requisitos/casos-de-uso/diagrama-casos-de-uso/SUBSISTEMA_GestionAuditoria.png)
