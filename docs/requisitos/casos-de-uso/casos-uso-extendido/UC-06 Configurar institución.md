### UC-06 Configurar institución

#### Objetivos asociados

- **OBJ-07** Gestionar instituciones y cursos

#### Requisitos funcionales y no funcionales asociados

- **RF-02** Configurar datos de la institución
- **RNF-02** Auditoría

#### Requisitos de información utilizados

- **RI-02** Información de la institución

#### Actor principal

- Administrador

#### Descripción

El administrador realiza el alta de los datos de la institución educativa que utiliza el sistema que serán proporcionados por el Padrón Oficial de Establecimientos Educativos. El administrador indica la jurisdicción, localidad, nombre, domicilio, teléfono y correo electrónico y el sistema establece los datos en el sistema.

#### Precondición

- 

#### Postcondición

Los datos de la institución quedan establecidos en el sistema y la plataforma queda habilitada.

#### Flujo principal

1. Este caso de uso comienza cuando el administrador quiere dar de alta los datos de la institución educativa.
2. El sistema consulta los datos del Padrón Oficial de Establecimientos Educativos y solicita que el administrador ingrese los datos correspondientes a la institución: jurisdicción, localidad y nombre.
3. El administrador selecciona la jurisdicción, localidad y nombre de la institución.
4. El sistema autocompleta los datos del domicilio, teléfono y correo electrónico de la institución.
5. El administrador da de alta los datos de la institución en el sistema.
6. El sistema establece los datos de la institución, habilita la plataforma para el uso general y termina el caso de uso.

#### Excepciones

- **Paso 3**: El establecimiento educativo en cuestión no aparece en el Padrón Oficial de Establecimientos Educativos. El administrador del sistema se debe ponerse en contacto con soporte técnico para dar de alta manualmente los datos de la institución y termina el caso de uso.

#### Rendimiento

- **Paso 2**: 1 segundo

#### Frecuencia

- 1 sola vez

#### Estabilidad: Alta

#### Comentarios
-