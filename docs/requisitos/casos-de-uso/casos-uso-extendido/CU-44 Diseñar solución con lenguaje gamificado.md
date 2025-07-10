### UC-44 Diseñar solución con lenguaje gamificado

#### Objetivos asociados

- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

#### Requisitos funcionales y no funcionales asociados

- RF-02 Resolver misiones

#### Requisitos de información utilizados

- RI-06 Información de estadísticas de progreso de los alumnos
- RI-12 Información de acciones
- RI-13 Información de tácticas
- RI-14 Información de objeto de inventario
- RI-15 Información de habilidades especiales
- RI-16 Información de operadores lógicos y matemáticos

#### Actor principal

- Alumno

#### Descripción

El alumno utiliza el lenguaje de programación gamificado para diseñar una solución para posteriormente ejecutarla para intentar resolver la misión.

#### Precondición

El alumno debe tener al menos una acción (primitiva) disponible para utilizar.

#### Postcondición

Se registra la solución diseñada y queda lista para ejecutarse

#### Flujo principal

1. Este caso de uso comienza cuando el alumno debe diseñar la solución para resolver una misión
2. El alumno indica el comienzo de la solución con la palabra "Inicio"
3. El alumno comienza el diseño de la solución para la misión. Como mínimo debe agregar una acción, se ejecuta el ***CU-45** Agregar acción*.
4. El alumno indica el final de la solución con la palabra "Fin" y termina el caso de uso.

#### Excepciones

1. Paso de la excepción

#### Secciones

##### UC-51 Consultar manual del héroe
**Flujo principal**
1. El alumno consulta el manual del heroe
2. El sistema devuelve el nombre, sintáxis y semántica de cada acción, táctica, objeto y habilidad especial que el alumno tenga desbloqueada actualmente.

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

Al menos 1 vez por día

#### Estabilidad: Alta

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
