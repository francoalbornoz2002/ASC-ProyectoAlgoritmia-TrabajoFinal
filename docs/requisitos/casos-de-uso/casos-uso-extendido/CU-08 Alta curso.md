## UC-08 Alta curso

#### Objetivos asociados

- OBJ-07 Gestionar de instituciones y cursos

#### Requisitos funcionales y no funcionales asociados

- **RF-03** Gestionar de cursos
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-03** Información de cursos

#### Actor principal

- Administrador

#### Descripción

El administrador realiza la alta de un curso en el sistema indicando los datos correspondientes: nombre del curso, descripción, docentes a cargo, días, horarios y modalidad de cursada (presencial, virtual o mixta) y una contraseña de acceso al curso. El sistema verifica los datos y lo da de alta en el sistema.

#### Precondición

- Los datos de la institución deben estar dados de alta para la creación del curso
- Debe haber al menos un usuario con el rol de docente dado de alta en el sistema.

#### Postcondición

- El curso es dado de alta en el sistema.

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta un curso en el sistema.
2. El sistema solicita al administrador ingrese el nombre y descripción del curso
3. El administrador ingresa el nombre y descripción del curso.
4. El sistema solicita al administrador que seleccione a los docentes que estarán a cargo del curso.
5. El administrador selecciona a los docentes a cargo del curso.
6. El sistema solicita que indique la modalidad de cursada.
7. El administrador indica la modalidad de cursada eligiendo entre: presencial, virtual o mixta.
8. El administrador solicita realizar la alta del usuario en el sistema.
9.  El sistema asigna un id de usuario, registra la fecha de creación, coloca su estado en "Activo", realiza la alta en el sistema y termina el caso de uso.

#### Excepciones

1. Paso de la excepción

#### Rendimiento

1. Paso - tiempo (seg, min, h)

#### Frecuencia

N veces por día/mes

#### Estabilidad: Alta/Media/Baja

#### Comentarios
Comentarios o reglas de negocio específicas que condicionan este caso de uso.
