### UC-16 Sincronizar progreso de alumno

#### Objetivos asociados

- **OBJ-10** Persistir el progreso de manera local y sincronizarlo luego

#### Requisitos funcionales y no funcionales asociados

- **RF-05** Sincronizar y mantener actualizado el progreso de los alumnos
- **RNF-01** Progreso offline y sincronización

#### Requisitos de información utilizados

- **RI-09** Información de capítulos
- **RI-10** Información de misiones

#### Actor principal

- Videojuego (externo), Sistema (interno)

#### Descripción

El videojuego sincroniza todos los datos de progreso del alumno, el sistema los registra y actualiza el progreso y riesgo académico del alumno en cuestión. También se actualiza el progreso total del curso al que pertenece el alumno.

#### Precondición

- El videojuego debe contar con conexión a internet al momento de intentar sincronizar

#### Postcondición

- El progreso del alumno queda actualizado en la plataforma web.
- El riesgo académico del alumno queda actualizado.
- El progreso del curso al que pertenece el alumno queda actualizado.

#### Flujo principal

1. Este caso de uso comienza cuando el videojuego (sistema externo) intenta sincronizar los datos de progreso del alumno a la plataforma web al terminar una misión o al cerrar la sesión en el videojuego.
2. El sistema recibe los datos de progreso del alumno, por cada misión completada se recibe:
   - Misión completada
   - Capítulo al que pertenece la misión completada
   - Puntuación obtenida (estrellas)
   - Puntos de experiencia obtenidos (EXP)
   - Cantidad de intentos registrados
3. El sistema actualiza el progreso individual del alumno en la plataforma web.
4. El sistema actualiza el riesgo académico del alumno en base al progreso actualizado. Ver caso de uso *Actualizar riesgo académico*.
5. El sistema actualiza el progreso del curso al que pertenece el alumno en cuestión en base al progreso actualizado.

#### Excepciones

1. Paso de la excepción

#### Sección

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

N veces por día/mes

#### Estabilidad: Alta/Media/Baja

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
