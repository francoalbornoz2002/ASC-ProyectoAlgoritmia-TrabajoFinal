## UC-08 Alta curso

#### Objetivos asociados

- **OBJ-07** Gestionar de instituciones y cursos

#### Requisitos funcionales y no funcionales asociados

- **RF-03** Gestionar de cursos
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-03** Información de cursos

#### Actor principal

- Administrador

#### Descripción

El administrador realiza la alta de un curso en el sistema indicando los datos correspondientes: nombre del curso, descripción, docentes a cargo, días, horarios, modalidad de clases (presencial, virtual o mixta) y una contraseña de acceso al curso. El sistema verifica los datos y lo da de alta en el sistema.

#### Precondición

- Los datos de la institución deben estar dados de alta para la creación del curso
- Debe haber al menos un usuario con el rol de docente dado de alta en el sistema.

#### Postcondición

- El curso es dado de alta en el sistema.

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta un curso en el sistema.
2. El sistema solicita al administrador ingrese el nombre y descripción del curso
3. El administrador ingresa el nombre y descripción del curso.
4. El sistema lista a los docentes dados de alta en el sistema y solicita al administrador que seleccione a los docentes que estarán a cargo del curso.
5. El administrador selecciona al/a los docente/s a cargo del curso.
6. El sistema solicita que indique la modalidad de cursada.
7. El administrador selecciona la modalidad de cursada eligiendo entre: presencial, virtual o mixta.
   1. Si elige presencial, ver sección _Modalidad presencial_.
   2. Si elige virtual, ver sección _Modalidad virtual_.
   3. Si elige mixta, ver sección _Modalidad mixta_.
8. Luego de definir los días, horarios y modalidad de las clases, el sistema solicita que el administrador ingrese una contraseña para acceso al curso.
9. El administrador ingresa una contraseña de acceso al curso y solicita dar de alta al curso en el sistema.
10. El sistema verifica todos los datos del curso y da de alta el curso en el sistema. Se registra la fecha de creación, se coloca su estado en "Activo" y termina el caso de uso.

#### Excepciones

- **Paso 3**: El nombre del curso ingresado es igual al nombre de un curso existente. El sistema indica el error y le solicita al administrador que coloque otro nombre de curso volviendo al paso 2.

#### Sección Modalidad presencial

**Flujo principal**

1. Esta sección comienza cuando el administrador elige la modalidad presencial.
2. El sistema solicita que el administrador indique los días y horarios de la cursada.
3. El administrador selecciona los días de clase y, por cada día seleccionado, ingresa un horario de inicio y fin de la clase.
4. El sistema registra los días y horarios de las clases del curso.

#### Sección Modalidad virtual

**Flujo principal**

1. Esta sección comienza cuando el administrador elige la modalidad virtual.
2. El sistema solicita que el administrador indique los días y horarios de la cursada.
3. El administrador selecciona los días de clase y, por cada día seleccionado, ingresa un horario de inicio y fin de la clase.
4. El sistema solicita que el administrador ingrese los datos de la reunión virtual: Código o nombre de la reunión, contraseña y la URL recurrente de ingreso. Este paso es _opcional_ y el administrador puede no completar la información.
5. El sistema registra los días, horarios y datos de la reunión de las clases virtuales del curso.

#### Sección Modalidad mixta

**Flujo principal**

1. Esta sección comienza cuando el administrador elige la modalidad mixta.
2. El sistema solicita que el administrador indique los días y horarios de la cursada.
3. El administrador selecciona los días de clase y, por cada día seleccionado, ingresa un horario de inicio y fin de la clase y la modalidad: presencial o virtual.
4. Como hay al menos un día de clase virtual, el sistema solicita que el administrador ingrese los datos de la reunión virtual: Código o nombre de la reunión, contraseña y la URL recurrente de ingreso. Este paso es _opcional_ y el administrador puede no completar la información.
5. El sistema registra los días, horarios y datos de la reunión de las clases virtuales del curso.

#### Rendimiento

- **Paso 4**: 0,5 segundos
- **Paso 10**: 1 segundo

#### Frecuencia

1 vez cada 4 meses (cuatrimestre)

#### Estabilidad: Alta

#### Comentarios

-
