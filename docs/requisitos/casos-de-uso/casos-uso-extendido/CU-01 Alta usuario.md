### UC-01 Alta usuario

#### Objetivos asociados

- OBJ-08 Gestionar usuarios y roles del sistema

#### Requisitos funcionales y no funcionales asociados

- RF-01 Gestionar usuarios
- RNF-02 Auditoría
- RNF-03 Seguridad de la información

#### Requisitos de información utilizados

- RI-01 Información de usuarios

#### Actor principal

- Administrador

#### Descripción

El administrador realiza la alta de un usuario. Completa los datos correspondientes, elige el rol correspondiente y lo da de alta en el sistema.

#### Precondición

- 

#### Postcondición

El usuario fué dado de alta en el sistema

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta a un usuario del sistema
2. El sistema solicita que el administrador coloque los datos correspondientes de un usuario.
3. El administrador indica el nombre de usuario, contraseña, correo eletrónico, nombre/s, apellido/s, género y rol dentro del sistema eligiendo entre: administrador, docente o alumno.
4. Si el administrador elige el rol de docente, el sistema solicita al administrador que seleccione la o las instituciones a las que pertenece el docente. Si se elige cualquier otro rol, ignorar el paso 5 y saltar al paso 6.
5. El administrador selecciona la o las instituciones a las que pertenece el docente.
6. El administrador solicita realizar la alta del usuario en el sistema.
7. El sistema asigna un id de usuario, registra la fecha de creación, coloca el estado en "Activo", realiza la alta en el sistema y termina el caso de uso.

#### Excepciones

- Paso 6: El nombre de usuario y/o correo electrónico del usuario que se desea dar de alta ya existe en el sistema. El sistema indica el error y solicita que se ingrese un nuevo nombre de usuario y/o correo electrónico.

#### Rendimiento

- Paso 7: 1 segundo

#### Frecuencia

- 5 veces/mes

#### Estabilidad: Alta

#### Comentarios
Si el administrador da de alta a un usuario con el rol de alumno, el método de registro será registrado como "Manual".
