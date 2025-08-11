### UC-XX Nombre del caso de uso

#### Objetivos asociados

- **OBJ-05** Proveer seguimiento académico exhaustivo

#### Requisitos funcionales y no funcionales asociados

- **RF-04** Gestionar sesiones de refuerzo
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-03** Información de cursos
- **RI-05** Información de alumnos
- **RI-06** Información del progreso de los alumnos
- **RI-07** Información de dificultades de los alumnos
- **RI-08** Información de sesiones de refuerzo

#### Actor principal

- Docente

#### Descripción

El docente crea una sesión de refuerzo eligiendo a los alumnos que considere que la necesiten. Selecciona a los alumnos, el sistema muestra las dificultades de cada uno y propone los pasos para tratar las mismas. Elige la modalidad de la sesión (presencial o virtual), fecha, duración y hora. El sistema crea la sesión de refuerzo y notifica a los alumnos involucrados.

#### Precondición

- El curso debe tener al menos un alumno asociado
- Al menos un alumno del curso debe tener mínimamente una misión completada.

#### Postcondición

- La sesión queda registrada en el sistema
- Se envía una notificación a los alumnos involucrados

#### Flujo principal

1. Este caso de uso comienza cuando un docente quiere crear una sesión de refuerzo.
2. El sistema solicita al docente que seleccione a los alumnos a involucrar, mostrando de manera prioritaria a los alumnos con dificultades e inactividad en diferentes niveles de riesgo académico:
   - Bajo: de 1 a 3 dificultades y hasta 2 días de inactividad
   - Medio: de 3 a 5 dificultades y hasta 4 días de inactividad.
   - Alto: más de 5 dificultades y más de 5 días de inactividad.
3. El docente selecciona a los alumnos deseados. El sistema sugiere agregar, de manera prioritaria, a todos los que tengan riesgo alto.
4. El sistema muestra las dificultades de cada alumno seleccionado.
5. El sistema autocompleta la descripción de la sesión proponiendo un plan resumido para tratar y mitigar las dificultades de cada uno.
6. El sistema informa que el docente puede modificar la descripción si lo desea
7. El docente agrega, quita o modifica la descripción de la sesión
8. El sistema solicita que el docente seleccione la modalidad de la sesión entre presencial o virtual

#### Excepciones

1. Paso de la excepción

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

N veces por día/mes

#### Estabilidad: Alta/Media/Baja

#### Comentarios

Comentarios o reglas de negocio específicas que condicionan este caso de uso.
