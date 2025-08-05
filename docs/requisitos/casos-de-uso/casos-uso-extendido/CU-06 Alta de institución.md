### UC-06 Alta de institución

#### Objetivos asociados

- OBJ-07 Gestionar instituciones y cursos

#### Requisitos funcionales y no funcionales asociados

- RF-02 Gestionar instituciones
- RNF-02 Auditoría

#### Requisitos de información utilizados

- RI-02 Información de instituciones

#### Actor principal

- Administrador

#### Descripción

El administrador realiza la alta de una institución indicando 

#### Precondición

- 

#### Postcondición

El usuario fué dado de alta en el sistema

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta a una institución en el sistema
2. El sistema solicita que el administrador coloque los datos correspondientes de la institución.
3. El administrador indica el nombre de la institución, contraseña, correo eletrónico, nombre/s, apellido/s, género y rol dentro del sistema eligiendo entre: administrador, docente o alumno.
4. El administrador solicita realizar la alta del usuario en el sistema.
5. El sistema asigna un id de usuario, registra la fecha de creación, coloca el estado en "Activo", realiza la alta en el sistema y termina el caso de uso.

#### Excepciones

- Paso 6: El nombre de usuario y/o correo electrónico del usuario que se desea dar de alta ya existe en el sistema. El sistema indica el error y solicita que se ingrese un nuevo nombre de usuario y/o correo electrónico.

#### Rendimiento

- Paso 7: 1 segundo

#### Frecuencia

- 5 veces/mes

#### Estabilidad: Alta

#### Comentarios
Si el administrador da de alta a un usuario con el rol de alumno, el método de registro será registrado como "Manual".
