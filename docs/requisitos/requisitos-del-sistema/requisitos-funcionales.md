# Requisitos Funcionales del sistema

**Versión:** 2.0
**Fecha:** 02/08/2025
**Autor(es):** Franco Andrés Albornoz

En este documento contiene la lista de los requisitos funcionales del sistema expresado en forma tradicional.

---

## RF-01 Gestionar usuarios

**Objetivos relacionados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- RI-01 Información de usuarios
- RI-04 Información de docentes
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir la alta, baja y modificación de usuarios, la asignación de los roles de administrador, docente y alumno y el inicio de sesión en el sistema mediante usuario y contraseña y autenticación con Google en caso de alumnos.

## RF-02 Configurar datos de la institución

**Objetivos relacionados**

- OBJ-07 Gestionar cursos y datos de la institución

**Requisitos asociados**

- RI-02 Información de la institución

**Descripción**
El sistema debe permitir, para el rol de administrador, configuración de los datos de la institución que utilice el sistema.

## RF-03 Gestionar de cursos

**Objetivos relacionados**

- OBJ-07 Gestionar cursos y datos de la institución

**Requisitos asociados**

- RI-03 Información de cursos
- RI-04 Información de docentes
- RI-05 Información de alumnos
- RI-09 Información de capítulos

**Descripción**
El sistema debe permitir, para el rol de administrador, la alta, baja y modificación de cursos del sistema. Para el rol de docente, le debe permitir la modificación de los datos del curso (de manera restringida) y la habilitación de capítulos para controlar la curva de aprendizaje. Para el rol de alumno, le debe permitir ingresar a cursos con la contraseña de acceso proporcionada por el docente.

## RF-04 Gestionar sesiones de refuerzo

**Objetivos relacionados**

- OBJ-06 Generar reportes semanales y sesiones de refuerzo automáticos

**Requisitos asociados**

- RI-03 Información de cursos
- RI-05 Información de docentes
- RI-05 Información de alumnos
- RI-06 Información del progreso de los alumnos
- RI-08 Información de sesiones de refuerzo

**Descripción**
El sistema debe permitir al docente la creación, modificación y cancelación de sesiones de refuerzo y la generación automática de la sesión de refuerzo semanal todos los sábados a las 18:00 hs notificando por correo electrónico al docente y alumnos involucrados.

## RF-05 Sincronizar y mantener actualizado el progreso de los alumnos

**Objetivos relacionados**

- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-10 Persistir el progreso de manera local y sincronizarlo luego

**Requisitos asociados**

- RI-03 Información de cursos
- RI-05 Información de alumnos
- RI-06 Información del progreso de los alumnos
- RI-09 Información de capítulos
- RI-10 Información de misiones
- RNF-01 Progreso offline y sincronización

**Descripción**
El sistema debe permitir la sincronización y actualización del progreso de cada alumno del curso proveniente del videojuego (externo). Cada sincronización será iniciada por el videojuego al completar una misión exitosamente o al cerrar sesión en el mismo y el sistema debe ser capaz de recibir los datos de una misión o de varias misiones en caso de que se haya acumulado localmente.

## RF-06 Visualizar y generar reportes del progreso de alumnos

**Objetivos relacionados**

- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-03 Información de cursos
- RI-05 Información de alumnos
- RI-06 Información del progreso de los alumnos
- RI-09 Información de capítulos
- RI-10 Información de misiones

**Descripción**
El sistema debe permitir al docente visualizar y generar reportes de las estadísticas de progreso de todos los alumnos, tanto en la historia general como en cada capítulo, de cada curso que esté a cargo, pudiendo aplicar los siguientes filtros:

- Selección de capítulo
- Búsqueda por nombre y/o apellido del alumno
- Porcentaje de misiones completadas
- Promedio de intentos por misión
- Estado de un capítulo (En curso o Finalizado)
- Días de inactividad
- Fechas desde - hasta

Si se filtra por capítulo, todas las estadísticas individuales de cada alumno serán de ese capítulo en específico. Además, se añadirán los siguientes datos adicionales:

- Estado del capítulo: "En curso" o "Finalizado"
- Porcentaje de avance del curso en el capítulo
  - Si está en curso, se muestra el porcentaje de avance
  - Si está finalizado, se muestra el porcentaje de avance cuando finalizó y el porcentaje de avance actualizable post-finalización, ya que los alumnos podrán seguir jugando misiones que no hayan completado de capitulos finalizados.

**Comentarios**
El sistema tambien deberá realizar la generación automática de un reporte de progreso semanal de los alumnos, ordenado por capítulos (solo los capítulos finalizados y los que estén curso) todos los sábados a las 18:00 hs enviandola por correo electrónico a todos los docentes del curso.

## RF-07 Sincronizar y mantener actualizado las dificultades de los alumnos

**Objetivos relacionados**

- OBJ-04 Identificar dificultades en los alumnos y ofrecer ayudas para mejorar los algoritmos
- OBJ-05 Proveer seguimiento académico exhaustivo
- OBJ-10 Persistir el progreso de manera local y sincronizarlo luego

**Requisitos asociados**

- RI-03 Información de cursos
- RI-05 Información de alumnos
- RI-07 Información de dificultades de los alumnos

**Descripción**
El sistema debe permitir la sincronización y actualización de las dificultades de cada alumno del curso proveniente del videojuego (externo). Cada sincronización será iniciada por el videojuego al completar una misión exitosamente o al cerrar sesión en el mismo.

## RF-08 Visualizar y generar reportes de las dificultades de los alumnos

**Objetivos relacionados**

- OBJ-04 Identificar dificultades en los alumnos y ofrecer ayudas para mejorar los algoritmos
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-03 Información de cursos
- RI-05 Información de alumnos
- RI-07 Información de dificultades de los alumnos

**Descripción**
El sistema debe permitir visualizar y generar reportes de las dificultades que posean los alumnos a partir en resolución de misiones en el videojuego. Las dificultades deben poder ser visualizadas tanto por los docentes como por los alumnos individualmente pudiendo filtrar por dificultad, tipo de dificultad y/o grado de dificultad. El sistema permitirá aplicar los siguientes filtros de búsqueda:

- Búsqueda por nombre(s) y/o apellido(s)
- Filtro por tipo(s) de dificultad
- Filtro por dificultad(es)
- Filtro por grado(s) de dificultad (determinada por la cantidad de errores acumulados de ese tipo de dificultad)

## RF-09 Determinar el riesgo académico de los alumnos

**Objetivos relacionados**

- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-05 Información de alumnos 
- RI-06 Información del progreso de los alumnos
- RI-07 Información de dificultades de los alumnos

**Descripción**
El sistema debe determinar el riesgo académico del alumno mediante un algoritmo que utilizará los datos de progreso y las dificultades y grado del alumno. En el contexto del sistema, *riesgo* académico se referiere a la probabilidad de que el alumno no alcance el nivel de dominio o avance esperado en el videojuego y en el curso

## RF-10 Controlar la curva de aprendizaje mediante habilitación de capitulos

**Objetivos relacionados**

- OBJ-02 Ofrecer misiones con dificultad progresiva y curva de aprendizaje controlada
- OBJ-05 Proveer seguimiento académico exhaustivo

**Requisitos asociados**

- RI-03 Información de cursos
- RI-09 Información de capítulos

**Descripción**
El sistema debe permitir al docente habilitar y finalizar los capítulos a medida que se vayan dando los contenidos en la materia para garantizar una curva de aprendizaje controlada y seguimiento académico ordenado de los alumnos.

**Comentarios**
Un capítulo estará "En curso" mientras el capitulo siguiente no sea habilitado por el docente. Si el docente habilita un capítulo, el anterior se considerará con estado "Finalizado". El docente solo podrá habilitar los capítulos de manera secuencial y NO desordenada. Los alumnos podrán jugar misiones que no hayan completado de capitulos finalizados igualmente.

## RF-11 Registro y autenticación con Google

**Objetivos relacionados**

- OBJ-08 Gestionar usuarios y roles del sistema

**Requisitos asociados**

- RI-01 Información de usuarios
- RI-05 Información de alumnos

**Descripción**
El sistema debe permitir a los alumnos registrarse y autenticarse utilizando su cuenta de Google mediante el protocolo OAuth 2.0. Durante el registro, se solicitará acceso a los datos básicos del perfil (nombre, correo electrónico) y, en caso de ser un nuevo usuario, se completarán los datos restantes requeridos por la plataforma. Una vez registrado, el alumno podrá iniciar sesión y autenticarse posteriormente utilizando el mismo método.

<!-- Plantilla

## RF-XX DDD

**Objetivos relacionados**

- s

**Requisitos asociados**

- s

**Descripción**
s

-->