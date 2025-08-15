### UC-25 Desmarcar asistencia a sesión

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

Este caso de uso es aplicable para que un docente o alumno desmarque su asistencia a una sesión de refuerzo. El actor busca la sesión de refuerzo, marca su asistencia y el sistema la registra.

#### Precondición

- Debe existir al menos una sesión de refuerzo con la asistencia del actor marcada

#### Postcondición

- La asistencia del actor queda desmarcada en el sistema

#### Flujo principal

1. Este caso de uso comienza cuando un docente o alumno quiere desmarcar su asistencia a una sesión de refuerzo
2. El sistema ejecuta el *UC-22 Buscar sesión de refuerzo* mostrando las sesiones con estado "Programada" y donde el actor marcó su asistencia.
3. El actor desmarca su asistencia de la sesión de refuerzo.
   1. Si el actor tiene rol *Docente*, se coloca la sesión en estado "En espera".
   2. Si el actor tiene rol *Alumno* y es el único alumno que tenía marcada su asistencia, se coloca la sesión en estado "En espera".
4. El sistema registra el desmarque de asistencia y notifica a los demás docentes y alumnos del curso.

#### Excepciones

1. Paso de la excepción

#### Rendimiento

**Paso 4**: 1 segundo

#### Frecuencia

1 vez por semana

#### Estabilidad: Media

#### Comentarios
- 