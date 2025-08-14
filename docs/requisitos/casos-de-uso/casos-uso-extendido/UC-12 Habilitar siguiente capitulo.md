### UC-12 Habilitar siguiente capítulo

#### Objetivos asociados

- **OBJ-02** Ofrecer misiones con dificultad progresiva y curva de aprendizaje controlada

#### Requisitos funcionales y no funcionales asociados

- **RF-10** Controlar la curva de aprendizaje mediante habilitación de capitulos
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-09** Información de capítulos

#### Actor principal

- Docente

#### Descripción

El docente habilita el siguiente capítulo del videojuego para que los alumnos puedan avanzar. El sistema lista todos los capítulos del videojuego indicando el siguiente a habilitar. El docente habilita el capítulo, el sistema envía las peticiones al videojuego para que realice las acciones dentro del mismo. El nuevo capítulo habilitado se coloca en estado "En curso" y el anterior queda en estado "Finalizado", pero jugable aún.

#### Precondición

- El capítulo que se va a colocar en estado "Finalizado" debe tener al menos un 70% de misiones completadas.

#### Postcondición

- El nuevo capítulo queda habilitado y con estado "En curso". El anterior queda en estado "Finalizado". Se habilita el nuevo capítulo en el videojuego y en la plataforma web.

#### Flujo principal

1. Este caso de uso comienza cuando el docente quiere habilitar el siguiente capítulo del videojuego.
2. El sistema lista todos los capítulos del videojuego e indica el siguiente a habilitar.
3. El docente habilita el siguiente capítulo.
4. El sistema verifica que el capítulo actual tenga al menos 80% de misiones completadas para pasar al siguiente.
5. El sistema envía una petición para que se habilite el capítulo dentro del videojuego.
6. El nuevo capítulo queda habilitado en el videojuego y en la web con estado "En curso" y el capítulo anterior queda en estado "Finalizado" pero todavía jugable para los alumnos que no lograron completar todas las misiones.

#### Excepciones

- **Paso 2**: Se está "En curso" en el último capítulo. El sistema indica que ya no quedan capítulos para habilitar y termina el caso de uso.
- **Paso 4**: El capítulo "En curso" tiene menos del 70% de misiones completadas por todos los alumnos. El sistema indica que no se puede habilitar el capítulo y termina el caso de uso.
- **Paso 5**: La comunicación entre la plataforma web y el videojuego falla. El sistema indica el error y termina el caso de uso.

#### Rendimiento

- **Paso 2**: 0,5 segundos
- **Paso 4**: 0,5 segundos
- **Paso 5**: 3 segundos (?)

#### Frecuencia

Como máximo 7 veces durante todo el curso

#### Estabilidad: Media

#### Comentarios
El primer capítuloe es habilitado automáticamente cuando se da de alta el curso.