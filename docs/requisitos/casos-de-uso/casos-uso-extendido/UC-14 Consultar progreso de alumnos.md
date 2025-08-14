### UC-21 Consultar progreso de alumnos

#### Objetivos asociados

- **OBJ-05** Proveer seguimiento académico exhaustivo

#### Requisitos funcionales y no funcionales asociados

- **RF-06** Visualizar y generar reportes del progreso de alumnos

#### Requisitos de información utilizados

- **RI-05** Información de alumnos
- **RI-06** Información del progreso de los alumnos
- **RI-09** Información de capítulos

#### Actor principal

- Docente

#### Descripción

El docente realiza la consulta del progreso de los alumnos del curso. El sistema muestra los datos de progreso de cada alumno y estadísticas del curso en general.

#### Precondición

- El curso debe tener al menos un alumno asociado
- Al menos un alumno del curso debe tener mínimamente una misión completada.

#### Postcondición

-

#### Flujo principal

1. Este caso de uso comienza cuando el docente quiere visualizar el progreso de los alumnos del curso.
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
4. El sistema permite los siguientes filtros de búsqueda:
   - Busqueda por nombre(s) y/o apellido(s)
   - Filtro por fechas desde - hasta
   - Filtro por capítulo(s)
   - Filtro por porcentaje de misiones completadas
     - más del 25%
     - más del 50%
     - más del 75%
     - más del 90%
   - Filtro por promedio de intentos por misión
     - 1 a 3 intentos
     - 3 a 6 intentos
     - 6 a 9 intentos
     - Más de 10 intentos
   - Filtro por días de inactividad
     - hasta 3 días
     - hasta 5 días
     - hasta 7 días
     - más de 7 días

#### Excepciones

-

#### Rendimiento

**Paso 2 y 3**: 1 segundo

#### Frecuencia

2 veces por día

#### Estabilidad: Alta

#### Comentarios

Si el progreso se filtra por capítulo, se mostrará

- Porcentaje de misiones completadas en el capítulo seleccionado
- Estado del capítulo: "En curso" o "Finalizado"
  Además, si el capitulo filtrado está "Finalizado" se mostrará el porcentaje de misiones completadas cuando finalizó y el porcentaje de misiones completadas en ese momento, ya que los alumnos podrán completar misiones de capítulos finalizados igualmente.
