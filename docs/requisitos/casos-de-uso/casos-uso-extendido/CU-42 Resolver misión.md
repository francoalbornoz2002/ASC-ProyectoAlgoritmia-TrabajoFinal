### UC-42 Resolver misión

#### Objetivos asociados

- OBJ-01 Crear y diseñar un videojuego para el aprendizaje gamificado
- OBJ-02 Ofrecer misiones con dificultad progresiva y contenido desbloqueable
- OBJ-03 Ofrecer ejecución y visualización de la solución en tiempo real
- OBJ-04 Proveer feedback formativo inmediato
- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

#### Requisitos funcionales y no funcionales asociados

- RF-02 Resolver misiones
- RF-03 Ejecutar, visualizar y evaluar misiones
- RF-04 Generar feedback formativo
- RNF-02 Portabilidad y rendimiento del videojuego
- RNF-03 Progreso offline y sincronización

#### Requisitos de información utilizados
- RI-08 Información de capítulos
- RI-09 Información de misiones
- RI-10 Información del escenario
- RI-11 Información de enemigos, obstáculos y objetos del escenario
- RI-12 Información de acciones
- RI-13 Información de tácticas
- RI-14 Información de objeto de inventario
- RI-15 Información de habilidades especiales
- RI-16 Información de operadores lógicos y matemáticos
- RI-17 Información del feedback generado

#### Actor principal

- Alumno

#### Descripción

El alumno selecciona una misión y diseña una solución utilizando el lenguaje de programación gamificado para intentar resolverla. El sistema ejecuta y evalua la misión, otorga una puntuación, asigna los puntos de experiencia correspondientes, actualiza el progreso y genera el feedback para mejorar la solución dándole la posibilidad al alumno de aceptarlo o no.

#### Precondición

El alumno debe haber iniciado sesión correctamente en el videojuego y tener al menos una misión disponible.

#### Postcondición

Se registra el resultado y puntuación de la misión. Se actualiza y se guarda el progreso del alumno (EXP y Nivel). Se genera y se almacena el feedback generado.

#### Flujo principal

1. Este caso de uso comienza cuando el alumno quiere resolver una misión del videojuego.
2. Se ejecuta el caso de uso ***UC-43** Seleccionar Misión*.
3. Luego de seleccionar la misión, el alumno comienza la resolución de la misma.
4. El sistema solicita que el alumno comience a diseñar la solución para la misión.
5. Se ejecuta el caso de uso *UC-44 Diseñar solución con lenguaje gamificado*.

#### Excepciones

1. Paso de la excepción

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

Al menos 1 vez/día

#### Estabilidad: Alta/Media/Baja

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
