### UC-22 Buscar sesión de refuerzo

#### Objetivos asociados

- **OBJ-06** Gestionar reportes y sesiones de refuerzo

#### Requisitos funcionales y no funcionales asociados

- **RF-04** Gestionar sesiones de refuerzo
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-08** Información de sesiones de refuerzo

#### Actor principal

- Administrador, Docente, Alumno

#### Descripción

Se realiza la búsqueda de una sesión de refuerzo. El actor busca por número de sesión.

#### Precondición

- Debe existir al menos una sesión de refuerzo en el sistema

#### Postcondición

-

#### Flujo principal

1. Este caso de uso comienza cuando el actor desea realizar la búsqueda de una sesión de refuerzo.
2. Para el rol de *Administrador*, el sistema permite los siguientes filtros:
   - Sesiones por curso
   - Id de sesión
   - Fechas (desde-hasta)
   - Creada por (docente)
   - Dirigida por (docente)
   - Modalidad (presencial o virtual)
   - Estado
3. Para el rol de *Docente*, el sistema permite los siguientes filtros:
   - Id de sesión
   - Fechas (desde-hasta)
   - Estado
4. El sistema devuelve las sesiones de refuerzo del sistema según lo especificado por el actor.

#### Excepciones

**Paso 4**: No existe ninguna sesión de refuerzo en base a los filtros aplicados. El sistema informa al actor y se vuelve al paso 2 para cambiar los filtros o termina el caso de uso.

#### Rendimiento

**Paso 4**: 1 segundo

#### Frecuencia

1 vez por día

#### Estabilidad: Media

#### Comentarios
- 
