### UC-15 Consultar dificultades de alumno

#### Objetivos asociados

- **OBJ-05** Proveer seguimiento académico exhaustivo

#### Requisitos funcionales y no funcionales asociados

- **RF-08** Visualizar y generar reportes de las dificultades de los alumnos

#### Requisitos de información utilizados

- **RI-05** Información de alumnos
- **RI-07** Información de dificultades de los alumnos

#### Actor principal

- Docente

#### Descripción

El docente consulta las dificultades de los alumnos del curso. El sistema muestra, por cada alumno, la lista de sus dificultades por tipo de dificultad y grado de dificultad.

#### Precondición

- El curso debe tener al menos un alumno asociado
- Al menos un alumno del curso debe tener mínimamente una misión completada.

#### Postcondición

- 

#### Flujo principal

1. Este caso de uso comienza cuando el docente quiere consultar las dificultades de los alumnos del curso.
2. El sistema muestra, por cada alumno del curso, los siguientes datos:
   - Nombre(s) y Apellido(s) del alumno
   - Tipo(s) de dificultad
   - Dificultad(es) de cada tipo(s)
   - Cantidad de errores cometidos en cada dificultad
   - Grado(s) de cada dificultad(es)
3. El sistema permite aplicar los siguientes filtros de búsqueda:
   - Busqueda por nombre(s) y/o apellido(s)
   - Filtro por Tipo(s) de dificultad
     - Secuencia
     - Lógica
     - Estructuras de control
     - Variables
     - Procedimientos
   - Filtro por dificultad(es)
     - (determinar)
   - Filtro por grado(s) de dificultad
     - Alto
     - Medio
     - Bajo
     - Ninguno

#### Excepciones

- 

#### Rendimiento

**Paso 2**: 1 segundo

#### Frecuencia

1 vez por día

#### Estabilidad: Media

#### Comentarios
- 
