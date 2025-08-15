### UC-24 Marcar asistencia a sesión

#### Objetivos asociados

- **OBJ-06** Gestionar reportes y sesiones de refuerzo

#### Requisitos funcionales y no funcionales asociados

- **RF-04** Gestionar sesiones de refuerzo
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-08** Información de sesiones de refuerzo

#### Actor principal

- Docente o Alumno

#### Descripción

Este caso de uso es aplicable para que un docente o alumno marque su asistencia a una sesión de refuerzo. El actor busca la sesión de refuerzo, marca su asistencia y el sistema la registra.

#### Precondición

- Debe existir al menos una sesión de refuerzo con estado "En espera"

#### Postcondición

- La asistencia del actor queda marcada en el sistema

#### Flujo principal

1. Este caso de uso comienza cuando un docente o alumno quiere indicar su asistencia a una sesión de refuerzo
2. El sistema ejecuta el caso de uso *UC-22 Buscar sesión de refuerzo* para buscar las sesiones con estado "En espera".
3. Si el actor tiene rol "Docente" ver sección *Marcar docente*
4. Si el actor tiene rol "Alumno" ver sección *Marcar alumno*


#### Excepciones

1. Paso de la excepción

#### Sección Marcar docente
**Flujo principal**
1. Esta sección comienza cuando el actor que quiere marcar su asistencia tiene el rol de "Docente".
2. El sistema muestra las sesiones de refuerzo con estado "En espera".
3. El docente marca la asistencia a la sesión de refuerzo deseada.
4. El sistema registra la asistencia a la sesión de refuerzo.
6. El sistema notifica a los alumnos involucrados en la sesión de refuerzo.

#### Sección Marcar alumno
**Flujo principal**
1. Esta sección comienza cuando el actor que quiere marcar su asistencia tiene el rol de "Alumno".
2. El sistema muestra la sesión de refuerzo asignada al alumno y solicita que indique su asistencia.
3. El alumno marca la asistencia a la sesión de refuerzo.
4. El sistema registra la asistencia del alumno a la sesión de refuerzo.
5. Si la sesión tiene un docente que haya marcado su asistencia, se coloca el estado de la sesión en "Programada".
6. El sistema notifica al docente de la asistencia del alumno.

#### Rendimiento

**Paso 2**: 1 segundo
**Sección Marcar docente - Paso 4**: 1 segundo
**Sección Marcar docente - Paso 5**: 1 segundo
**Sección Marcar alumno - Paso 4**: 1 segundo
**Sección Marcar alumno - Paso 5**: 1 segundo

#### Frecuencia

1 vez por semana

#### Estabilidad: Media

#### Comentarios
- Un alumno puede estar involucrado en una sola sesión de refuerzo a la svez y, por lo tanto, marcar la asistencia a una sola sesión de refuerzo por vez.
