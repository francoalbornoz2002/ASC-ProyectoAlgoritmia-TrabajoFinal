### UC-43 Seleccionar misión

#### Objetivos asociados

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable

#### Requisitos funcionales y no funcionales asociados

- RF-02 Resolver misiones

#### Requisitos de información utilizados

- RI-06 Información de estadísticas de progreso de los alumnos
- RI-08 Información de capítulos
- RI-09 Información de misiones

#### Actor principal

- Actor/es

#### Descripción

El alumno selecciona una misión de las misiones disponibles del capítulo en donde se encuentra en la historia para posteriormente intentar resolverla.

#### Precondición

El alumno debe haber iniciado sesión correctamente en el videojuego y tener al menos una misión disponible.

#### Postcondición
_

#### Flujo principal

1. Este caso de uso comienza cuando el alumno quiere seleccionar una misión para intentar resolverla
2. El sistema solicita que el alumno seleccione el capítulo del cual desea seleccionar la misión.
3. El alumno selecciona el capítulo del cual desea seleccionar una misión.
4. El sistema muestra las misiones disponibles del capítulo seleccionado.
5. El sistema le pide al alumno que seleccione la misión que desea resolver.
6. El alumno selecciona la misión que desea resolver.
7. El sistema muestra la información de la misión: número, nombre, enunciado y dificultad
8. El alumno confirma la selección de la misión y termina el caso de uso.

#### Excepciones

- **Paso 3**: El alumno selecciona un capítulo que no está habilitado por el docente aún. Entonces, el sistema, en el **Paso 4**, muestra todas las misiones como "bloqueadas" sin posibilidad de acceder a las mismas con un mensaje de "Este capítulo aún no está habilitado" y **se vuelve al paso 2**.
- **Paso 6** El alumno selecciona una misión que ya completó anteriormente. Entonces, en el **Paso 7**, además de la información mostrada en el flujo principal, se muestra la puntuación otorgada y los puntos de experiencia adquiridos.

#### Rendimiento

**Paso 3**: 1 segundo
**Paso 6**: 1 segundo

#### Frecuencia

Al menos 1 vez/día

#### Estabilidad: Alta

#### Comentarios

- Luego de seleccionar el capítulo, el sistema debe posicionar o sugerir al alumno la última misión que tenga disponible para completar.
- Se deben poder diferenciar las misiones completadas de las no completadas.
- Se deben poder diferenciar los capítulos y misiones bloquedados.
