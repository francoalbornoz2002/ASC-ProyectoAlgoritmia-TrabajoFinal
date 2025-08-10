### UC-22 Generar reporte de curso

#### Objetivos asociados

- **OBJ-05** Proveer seguimiento académico exhaustivo

#### Requisitos funcionales y no funcionales asociados

- **RF-05** Visualizar y generar reportes del progreso de alumnos
- **RF-06** Visualizar y generar reportes de las dificultades de los alumnos

#### Requisitos de información utilizados

- **RI-06** Información del progreso de los alumnos
- **RI-07** Información de dificultades de los alumnos
- **RI-09** Información de capítulos

#### Actor principal

- Docente

#### Descripción

El docente genera un reporte de los alumnos del curso. Puede generar reportes de progreso, dificultades o completo (que incluye progreso y dificultades). El sistema le da al docente opciones de configuración segun el tipo de reporte. El docente configura el reporte segun sus necesidades y el sistema genera y exporta el reporte en formato PDF.

#### Precondición

- El curso debe tener al menos un alumno asociado.
- Al menos un alumno del curso debe tener una misión completada.

#### Postcondición

- El reporte de progreso es generado y exportado en PDF.

#### Flujo principal

1. Este caso de uso comienza cuando el docente quiere generar un reporte de los alumnos del curso.
2. El sistema solicita que el docente que indique el tipo de reporte a generar.
   1. Si el docente elije reporte de progreso, ver sección *Reporte de progreso*.
   2. Si el docente elije reporte de dificultades, ver sección *Reporte de dificultades*.
   3. Si el docente quiere realizar un reporte completo, ver sección *Reporte completo*.
3. El docente detalla la configuración del reporte
   - Cantidad de misiones completadas por día o por semana.
   - Selección de dificultades de alumnos por tipo o dificultad específica
   - Tipo de detalle: detallado o resumido
   - Agrupación por: capítulo, misión o capítulo y misión.

#### Excepciones

1. Paso de la excepción

#### Sección Reporte de progreso
**Flujo principal**
1. Esta sección comienza cuando el docente elije *Reporte de progreso*
2. El docente realiza la configuración del reporte
   - Rango de fechas (desde - hasta)
   - Filtro por capítulo(s)
   - Filtro por mision(es)
   - Filtro por alumno(s)
   - 

#### Sección Reporte de dificultades
**Flujo principal**
1. 

#### Sección Reporte completo
**Flujo principal**
1. 

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

N veces por día/mes

#### Estabilidad: Alta/Media/Baja

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
