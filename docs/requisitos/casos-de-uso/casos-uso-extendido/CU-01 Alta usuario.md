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

El administrador realiza la alta de un usuario en el sistema indicando los datos correspondientes: nombre de usuario, contraseña, correo eletrónico, nombre/s, apellido/s, género y rol (administrador, docente o alumno). El sistema verifica los datos y lo da de alta en el sistema.

#### Precondición

- 

#### Postcondición

El usuario está dado de alta en el sistema.

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta un usuario en el sistema.
2. El sistema solicita que el administrador ingrese los datos correspondientes a un usuario.
3. El administrador indica el nombre de usuario, contraseña, correo eletrónico, nombre/s, apellido/s, género y rol dentro del sistema eligiendo entre: administrador, docente o alumno.
4. El administrador solicita realizar la alta del usuario en el sistema.
5. El sistema asigna un id de usuario, registra la fecha de creación, coloca su estado en "Activo", realiza la alta en el sistema y termina el caso de uso.

#### Excepciones

- Paso 4: El nombre de usuario y/o correo electrónico del usuario que se desea dar de alta ya existe en el sistema. El sistema indica el error y solicita que se ingrese un nuevo nombre de usuario y/o correo electrónico.

#### Rendimiento

- Paso 5: 1 segundo

#### Frecuencia

- 5 veces/mes

#### Estabilidad: Alta

#### Comentarios
Si el administrador da de alta a un usuario con el rol de alumno, el método de registro del usuario será registrado como "Manual".
