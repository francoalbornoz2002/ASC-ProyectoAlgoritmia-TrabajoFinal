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

El docente crea una sesión de refuerzo eligiendo a los alumnos que considere que la necesiten. El docente selecciona a los alumnos, el sistema sugiere elegir a aquellos con riesgo académico alto o medio prioritariamente. El sistema muestra las dificultades de cada uno y propone los pasos para tratar cada dificultad. El docente completa los datos de la sesión: modalidad (presencial o virtual), duración (en minutos) fecha y hora. El sistema crea la sesión de refuerzo y notifica a los alumnos involucrados.

#### Precondición

- El curso debe tener al menos un alumno asociado
- Al menos un alumno del curso debe tener mínimamente una misión completada.

#### Postcondición

- La sesión queda registrada en el sistema
- Se envía una notificación a los alumnos involucrados

#### Flujo principal

1. Este caso de uso comienza cuando un docente quiere crear una sesión de refuerzo.
2. El sistema solicita al docente que seleccione a los alumnos a involucrar, mostrando de manera prioritaria a los alumnos con riesgo académico en diferentes niveles:
   - Bajo: de 1 a 3 dificultades y hasta 2 días de inactividad
   - Medio: de 3 a 5 dificultades y hasta 4 días de inactividad.
   - Alto: más de 5 dificultades y más de 5 días de inactividad.
3. El docente selecciona a los alumnos. El sistema sugiere agregar, de manera prioritaria, a todos los que tengan riesgo alto.
4. El sistema muestra las dificultades y su grado de cada alumno seleccionado.
5. El sistema autocompleta la descripción de la sesión proponiendo un plan resumido para tratar y mitigar las dificultades de cada alumno. El sistema informa que el docente puede modificar la descripción si lo desea.
6. El docente agrega, quita o modifica la descripción de la sesión.
7. El sistema solicita que el docente seleccione la modalidad (presencial o virtual) y duración (en minutos) de la sesión.
8. El docente seleccione la modalidad y duración de la sesión.
9. El sistema solicita al docente que ingrese la fecha de la sesión. Por defecto, se propondrá la fecha de la siguiente clase del curso para facilitar la disponibilidad de los alumnos. Igualmente, el docente podrá seleccionar cualquier fecha desde el día actual hasta un máximo de 7 días posteriores.
10. El sistema solicita al docente que ingrese la hora de la sesión, considerando las siguientes reglas dependiendo del tipo de fecha elegida:
    1. **Si la fecha corresponde a un día de clases**: el docente elige si la sesión se realizará antes o después de la clase. Según la opción, el sistema calcula automáticamente la hora restando o sumando la duración de la sesión respecto al horario de inicio o fin de la clase. La hora de fin se calcula automáticamente.
    2. **Si la fecha es libre**: el docente selecciona la hora manualmente, pudiendo programar la sesión a partir de las 07:00 y hasta un horario que permita finalizarla antes de las 23:00. Elegida la hora de inicio, la hora de fin se calcula automáticamente.
11. El docente solicita crear la sesión de refuerzo.
12. El sistema verifica que todos los datos estén correctos y registra la sesión de refuerzo.
13. El sistema notifica a los alumnos involucrados acerca de la sesión de refuerzo por correo electrónico.

#### Excepciones

**Paso 2**: Ningun alumno posee riesgo académico en nivel bajo, medio o alto. El sistema le informa al docente y termina el caso de uso.
**Paso 10.1**: El docente selecciona que la sesión se realice después de la clase, pero la hora de fin de la misma, sumada a la duración establecida, haría que la sesión termine después de las 23:00. El sistema informa que esta opción no es posible y habilita únicamente la alternativa de realizarla antes de la clase.

#### Rendimiento

**Paso 2**: 1 segundo
**Paso 4**: 0,5 segundo
**Paso 5**: 1 segundo
**Paso 10.1**: 0,1 segundo

#### Frecuencia

1 o 2 veces por semana

#### Estabilidad: Media

#### Comentarios

- La fecha de la sesión no debe ser anterior a la fecha actual y posterior a la fecha actual mas 7 días.
- En caso de que la sesión sea virtual, el docente deberá indicar la URL de la reunión (obligatoria) y, de forma opcional, el ID/código y la contraseña de acceso, según lo requiera la plataforma utilizada.
