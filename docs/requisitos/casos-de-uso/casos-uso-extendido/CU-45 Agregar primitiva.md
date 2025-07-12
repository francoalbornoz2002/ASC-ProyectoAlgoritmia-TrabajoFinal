### UC-45 Agregar primitiva

#### Objetivos asociados

- OBJ-11 Diseñar un lenguaje de programación gamificado para la resolución de misiones

#### Requisitos funcionales y no funcionales asociados

- RF-02 Resolver misiones

#### Requisitos de información utilizados

- RI-12 Información de acciones

#### Actor principal

- Alumno

#### Descripción

El alumno agrega una primitiva (representada por "acciones" del videojuego) a la solución que está diseñando para resolver una misión.

#### Precondición

El alumno debe tener al menos una primitiva (acción) disponible para utilizar.

#### Postcondición

Se agrega la primitiva a la solución.

#### Flujo principal

1. Este caso de uso comienza cuando el alumno quiere agregar una acción en una linea de la solución para una misión.
2. El sistema indica al alumno que tiene disponible en todo momento el manual del héroe para consultar las primitivas (acciones) disponibles. Ver sección "UC-51 Consultar manual del héroe"
3. El alumno escribe la primitiva (acción) que desea agregar a la solución siguiendo la sintaxis.
4. El sistema verifica que la primitiva no tenga error de sintaxis
5. El sistema agrega la primitiva a la solución y termina el caso de uso.

#### Excepciones

- **Paso 4** El alumno escribe de manera errónea la primitiva. El sistema indica la linea del error de sintaxis y le solicita al alumno que lo corrija.

#### Secciones

##### UC-51 Consultar manual del héroe
**Flujo principal**
1. El alumno consulta el manual del heroe
2. El sistema muestra el nombre, sintáxis y semántica de cada
   1. Primitiva (acciones)
   2. Estructura de control (tácticas)
   3. Variables del jugador y del entorno (objetos de inventario y objetos en el escenario)
   4. Procedimientos (habilidades especiales) que el alumno tenga desbloqueada actualmente.

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

N veces por día/mes

#### Estabilidad: Alta/Media/Baja

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
