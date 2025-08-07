### UC-11 Unirse a un curso

#### Objetivos asociados

- **OBJ-07** Gestionar de instituciones y cursos

#### Requisitos funcionales y no funcionales asociados

- **RF-03** Gestionar de cursos
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-03** Información de cursos

#### Actor principal

- Alumno

#### Descripción

El alumno ingresa a un curso que esté dado de alta en el sistema. El sistema lista los cursos dados de alta, el alumno selecciona el curso al que quiere unirse, coloca la contraseña de acceso, si es correcta el alumno queda asociado al curso.

#### Precondición

- Debe existir al menos un curso en el sistema

#### Postcondición

- El alumno se une al curso

#### Flujo principal

1. Este caso de uso comienza cuando un alumno quiere unirse a un curso en el sistema.
2. El sistema lista todos los cursos dados de alta y con estado "En curso" del sistema y le solicita al alumno que seleccione el curso al que quiere unirse.
3. El alumno selecciona el curso.
4. El sistema solicita que el alumno ingrese la contraseña de acceso al curso.
5. El alumno ingresa la contraseña de acceso al curso.
6. El sistema verifica la contraseña, le permite el acceso al curso al alumno y termina el caso de uso.

#### Excepciones

- **Paso 6**: La contraseña de acceso ingresada por el alumno es incorrecta. El sistema indica el error y le solicita que intente de nuevo volviendo al **Paso 4**.

#### Rendimiento

- **Paso 6**: 1 segundo

#### Frecuencia

1 vez por alumno

#### Estabilidad: Alta

#### Comentarios

