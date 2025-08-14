### UC-XX Nombre del caso de uso

#### Objetivos asociados

- **OBJ-10** Persistir el progreso de manera local y sincronizarlo luego

#### Requisitos funcionales y no funcionales asociados

- **RF-07** Sincronizar y mantener actualizado las dificultades de los alumnos
- **RNF-01** Progreso offline y sincronización

#### Requisitos de información utilizados

- **RI-03** Información de cursos
- **RI-05** Información de alumnos
- **RI-07** Información de dificultades de los alumnos

#### Actor principal

- Videojuego (externo), Sistema (interno)

#### Descripción

El videojuego sincroniza todas las dificultades del alumno determinadas en el videojuego, el sistema las registra y actualiza el riesgo académico del alumno en cuestión.

#### Precondición

- El videojuego debe contar con conexión a internet al momento de intentar sincronizar

#### Postcondición

- Las dificultades del alumno quedan actualizadas en la plataforma web.
- El riesgo académico del alumno queda actualizado.

#### Flujo principal

1. Este caso de uso comienza cuando el videojuego (sistema externo) intenta sincronizar las dificultades del alumno a la plataforma web al terminar una misión o al cerrar la sesión en el videojuego.
2. El sistema recibe las dificultades del alumno determinadas en el videojuego. Si se quiere registrar una nueva dificultad, el sistema recibe:
   - Id del alumno al que se quiere asociar la nueva dificultad
   - Id de tipo de dificultad
   - Id de dificultad
   - Grado de la dificultad a registrar
3. Si se quiere actualizar la dificultad, el sistema recibe:
   - Id del alumno
   - Id de tipo de dificultad
   - Id de dificultad
   - Grado de la dificultad a actualizar
4. El sistema actualiza las dificultades del alumno en la plataforma web.
5. El sistema actualiza el riesgo académico del alumno en base a las dificultades actualizadas. Ver caso de uso *Actualizar riesgo académico*.

#### Excepciones

**Paso 1**: La sincronización falla por algun factor externo (como internet). Se cancela la sincronización y las dificultades se mantienen localmente en el videojuego hasta el próximo intento de sincronización.

#### Rendimiento

**Paso 4 y 5**: 3 segundos

#### Frecuencia

Varias veces por día (depende de la cantidad de alumnos en el curso y su actividad en el videojuego)

#### Estabilidad: Alta

#### Comentarios
- 