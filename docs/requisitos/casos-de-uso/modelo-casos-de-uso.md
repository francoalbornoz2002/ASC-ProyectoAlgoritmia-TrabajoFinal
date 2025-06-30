# Modelo de Casos de Uso

**Versión:** 1.0
**Fecha:** 21/06/2025
**Autor(es):** Franco Andrés Albornoz

---

## Actores del sistema

### ACT-01 Alumno

Representa a los estudiantes que utilizarán el videojuego desarrollado en Godot como herramienta principal para practicar y afianzar los contenidos de la materia "Algoritmos y Estructuras de Datos I".

Los alumnos podrán registrarse en la plataforma web mediante un formulario tradicional o autenticarse con Google. Una vez registrados, inciarán sesión y se uniran a un curso ingresando un nombre de curso y contraseña provistos por el docente. Una vez unido a un curso, podrán descargar el videojuego e iniciar sesión con su usuario y contraseña para establecer sus datos y sincronizar el progreso que realicen.

Dentro del videojuego, podrán:

- Consultar y resolver misiones gamificadas.
- Recibir feedback formativo automático tras cada intento.
- Obtener puntuaciones, experiencia y subir de nivel.
- Desbloquear nuevas habilidades y capítulos de la historia según el progreso.
- Consultar sus estadísticas personales dentro del juego.

Adicionalmente, podrán acceder a la plataforma web para:

- Unirse a un curso
- Cambiar la contraseña
- Consultar recursos de apoyo (manual del héroe, tutoriales, etc.).
- Ver estadísticas más detalladas de su rendimiento.
- Confirmar asistencia a sesiones de refuerzo, ya sea desde la web o a través del enlace recibido por correo electrónico.

---

### ACT-02 Docente

Representa al personal docente encargado de dictar la materia y brindar seguimiento académico a los alumnos. Los docentes utilizarán exclusivamente la plataforma web, donde tendrán acceso a diversas funcionalidades de gestión académica.

Sus principales responsabilidades incluyen:

- Gestionar los cursos a su cargo (asignados previamente por el administrador) de manera limitada.
  - Modificar la contraseña de acceso del curso para nuevos alumnos.
  - Validar y aceptar solicitudes de ingreso de alumnos a sus cursos.
- Visualizar en tiempo real el avance y desempeño de sus alumnos (misiones resueltas, errores frecuentes, actividad reciente, etc.).
- Generar reportes académicos filtrados por curso, capítulo o estudiante.
- Programar sesiones de refuerzo para alumnos con bajo rendimiento o inactividad prolongada.

---

### ACT-03 Administrador

Representa al administrador general del sistema. Es responsable de mantener la infraestructura organizativa y funcional del entorno académico.

Entre sus funciones se destacan:

- Registrar y gestionar instituciones educativas.
- Crear cursos y asignar docentes a los mismos.
- Gestionar usuarios del sistema (docentes, alumnos y otros administradores en el futuro).
- Auditar cambios realizados en las distintas entidades del sistema: altas, bajas, modificaciones de usuarios, cursos e instituciones.

En esta versión inicial, se prevé que exista un único administrador central. En versiones futuras, podría habilitarse un esquema con administradores por institución.

## Diagrama de Casos de Uso

### Videojuego

### Plataforma web


## Casos de uso del sistema

### Administrador

#### Gestión de usuarios

- UC-XX Alta usuario
- UC-XX Modificar usuario
  - INCLUDE: UC-XX Buscar usuario
- UC-XX Baja usuario
  - INCLUDE: UC-XX Buscar usuario
- UC-XX Iniciar sesión

#### Gestión de instituciones
- UC-XX Alta de institución
- UC-XX Modificar institución
  - INCLUDE: UC-XX Buscar institución
- UC-XX Baja de institución
  - INCLUDE: UC-XX Buscar institución

#### Gestión de cursos

- UC-XX Alta de curso
- UC-XX Modificar curso
  - INLCUDE: UC-XX Buscar curso
- UC-XX Baja de curso
  - INCLUDE: UC-XX Buscar curso
- UC-XX Asignar docente a curso
  - INCLUDE: UC-XX Buscar docente

#### Auditoría
- UC-XX Auditoría

### Docentes

#### Gestionar seguimiento académico
- UC-XX Consultar progreso de alumnos
  - EXTEND: Ver progreso general (historia)
  - EXTEND: Ver progreso por capítulo
- UC-XX Generar reporte de progreso de alumnos

#### Gestionar sesiones de refuerzo
- UC-XX Crear sesión de refuerzo
- UC-XX Modificar sesión de refuerzo
- UC-XX Cancelar sesión de refuerzo
- UC-XX Aceptar sesión de refuerzo automática

#### Gestionar cursos (docente)
- UC-XX Definir días y horarios del curso
- UC-XX Cambiar contraseña de acceso a curso
- UC-XX Aceptar alumno a curso
- UC-XX Habilitar capítulo
  - INCLUDE: UC-XX Buscar capítulo

#### Usuario
- UC-XX Iniciar sesión
- UC-XX Actualizar datos personales

### Alumnos

#### Usuario
- UC-XX Registrarse en la plataforma
  - EXTEND: UC-XX Registro normal
  - EXTEND: UC-XX Registro con Google
- UC-XX Iniciar sesión en la plataforma web
  - EXTEND: UC-XX Iniciar sesión normal
  - EXTEND: UC-XX Inicar sesión con Google
- UC-XX Actualizar datos personales
- UC-XX Ver progreso en la web

#### Cursos
- UC-XX Ingresar a un curso
- UC-XX Confirmar asistencia a sesión de refuerzo

#### Videojuego
- UC-XX Iniciar sesión en el videojuego
- UC-XX Jugar misión
  - INCLUDE: UC-XX Buscar misión
  - INCLUDE: UC-XX Diseñar solución con lenguaje gamificado
    - INCLUDE: UC-XX Agregar acción
    - EXTEND: UC-XX Declarar variable
    - EXTEND: UC-XX Asignar valor a variable
    - EXTEND: UC-XX Agregar estructura condicional
    - EXTEND: UC-XX Agregar estructura repetitiva
    - EXTEND: UC-XX Agregar procedimiento
    - EXTEND: UC-XX Consultar manual del heroe
  - INCLUDE: UC-XX Ejecutar misión
  - INCLUDE: UC-XX Evaluar misión
  - INCLUDE: UC-XX Generar feedback
    - EXTEND: UC-XX Aceptar feedback
- UC-XX Ver progreso en el juego
- UC-XX Consultar inventario



