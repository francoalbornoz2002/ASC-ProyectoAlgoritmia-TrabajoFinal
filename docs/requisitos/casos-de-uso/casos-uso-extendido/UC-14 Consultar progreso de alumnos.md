### UC-21 Consultar progreso de alumnos

#### Objetivos asociados

- **OBJ-05** Proveer seguimiento académico exhaustivo

#### Requisitos funcionales y no funcionales asociados

- **RF-05** Visualizar y generar reportes del progreso de alumnos

#### Requisitos de información utilizados

- **RI-06** Información del progreso de los alumnos
- **RI-09** Información de capítulos

#### Actor principal

- Docente

#### Descripción

El docente realiza la consulta del progreso de los alumnos del curso. El sistema muestra los datos de progreso de cada alumno y estadísticas del curso en general.

#### Precondición

- El curso debe tener al menos un alumno asociado

#### Postcondición

-

#### Flujo principal

1. Este caso de uso comienza cuando el docente quiere visualizar el progreso de los alumnos del curso.
2. El sistema puede mostrar el progreso total del curso o el progreso en un capítulo en específico.
   1. Si el docente elige ver el progreso total ver sección _Progreso total_
   2. Si el docente elige ver el progreso en un capítulo en específico ver sección _Progreso en capítulo_

#### Excepciones

1. Paso de la excepción

#### Sección Progreso general

**Flujo principal**

1. Esta sección comienza cuando el docente elige ver el progreso total del curso
2. El sistema muestra las estadísticas de progreso del curso:
   - Porcentaje total de misiones completadas
   - Porcentaje de misiones completadas en el capítulo actual
3. El sistema muestra, por cada alumno del curso, las estadísticas de progreso individuales:
   - Nombre/s y Apellido/s del alumno
   - Capítulo y Misión en la que se encuentra
   - Cantidad de misiones completadas
   - Porcentaje total de misiones completadas
   - Porcentaje de misiones completadas en el capítulo actual
   - Promedio de intentos por misión
   - Cantidad de estrellas obtenidas
   - Total de puntos de experiencia (EXP) acumulados
   - Ultima actividad (Activo hace N minuto(s) / hora(s) / día(s))

#### Sección Progreso en capítulo

**Flujo principal**

1. Esta sección comienza cuando el docente quiere visualizar el progreso por capítulo.
2. El sistema solicita al docente que seleccione el capítulo del cual quiere ver el progreso.
3. El docente selecciona el capítulo.
4. El sistema muestra las estadísticas de progreso del curso en el capítulo seleccionado:
   - Porcentaje total de misiones completadas
   - Porcentaje de misiones completadas en el capítulo actual
   - Estado del capítulo: "En curso" o "Finalizado"
5. El sistema muestra, por cada alumno del curso, las estadísticas de progreso individuales en el capítulo seleccionado:
   - Nombre/s y Apellido/s del alumno
   - Misión en la que se encuentra
   - Cantidad de misiones completadas
   - Porcentaje total de misiones completadas
   - Promedio de intentos por misión
   - Cantidad de estrellas obtenidas
   - Total de puntos de experiencia (EXP) acumulados
   - Ultima actividad (Activo hace N minuto(s) / hora(s) / día(s))

#### Rendimiento

**Paso 2 y 3 de la sección Progreso general**: 1 segundo
**Paso 4 y 5 de la sección Progreso en capítulo**: 1 segundo

#### Frecuencia

2 veces por día

#### Estabilidad: Alta

#### Comentarios
En la sección Progreso en capítulo, si el capitulo seleccionado está "Finalizado" se mostrará el porcentaje de misiones completadas cuando finalizó y el porcentaje de misiones completadas en ese momento, ya que los alumnos podrán completar misiones de capítulos finalizados igualmente.

