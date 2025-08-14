### UC-16 Sincronizar progreso de alumno

#### Objetivos asociados

- **OBJ-10** Persistir el progreso de manera local y sincronizarlo luego

#### Requisitos funcionales y no funcionales asociados

- **RF-05** Sincronizar y mantener actualizado el progreso de los alumnos
- **RNF-01** Progreso offline y sincronización

#### Requisitos de información utilizados

- **RI-03** Información de cursos
- **RI-05** Información de alumnos
- **RI-09** Información de capítulos
- **RI-10** Información de misiones
- **RI-06** Información del progreso de los alumnos

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
   - Id del alumno
   - Id del curso al que pertenece
   - Id de la misión completada
   - Capítulo al que pertenece la misión completada
   - Puntuación obtenida (estrellas)
   - Puntos de experiencia obtenidos (EXP)
   - Cantidad de intentos registrados
3. El sistema actualiza el progreso individual del alumno en la plataforma web.
4. El sistema actualiza el riesgo académico del alumno en base al progreso actualizado. Ver caso de uso *Actualizar riesgo académico*.
5. El sistema actualiza el progreso del curso al que pertenece el alumno en cuestión en base al progreso actualizado.

#### Excepciones

**Paso 1**: La sincronización falla por algun factor externo (como internet). Se cancela la sincronización y el progreso se mantiene localmente en el videojuego hasta el próximo intento de sincronización.

#### Rendimiento

**Paso 3, 4 y 5**: 3 segundos

#### Frecuencia

Varias veces por día (depende de la cantidad de alumnos en el curso y su actividad en el videojuego)

#### Estabilidad: Alta

#### Comentarios
- 
