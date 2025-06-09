# Plan del Proyecto

**Versión:** 1.5
**Fecha de inicio:** 10/05/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Cronograma General

| Fase         | Fecha Inicio | Fecha Fin  | Responsable            |
| ------------ | ------------ | ---------- | ---------------------- |
| Inicio       | 10-05-2025   | 06-06-2025 | Franco Andrés Albornoz |
| Elaboración  | 07-06-2025   | 15-08-2025 | Franco Andrés Albornoz |
| Construcción | 16-08-2025   | 31-10-2025 | Franco Andrés Albornoz |
| Transición   | 01-11-2025   | 15-11-2025 | Franco Andrés Albornoz |

---

## 2. Iteraciones

| Iteración | Fechas          | Fase         | Objetivos principales                                                                                                                                               | Entregables clave                                                                                                                                                                                                                                                         |
| :-------: | :-------------- | :----------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|     0     | 10 May – 16 May | Inicio       | Plan global <br> Repositorio y estructura <br> Visión y alcance preliminares                                                                                        | `vision.md`<br>`plan-proyecto.md`<br>`docs/iteraciones/iteracion-0/iteracion-0.md`<br>`docs/iteraciones/iteracion-0/retrospectiva-0.md`                                                                                                                                   |
|     1     | 17 May – 30 May | Inicio       | Doc. de Visión completo <br> Riesgos y mitigación del proyecto <br> Glosario <br> Requisitos Funcionales y No Funcionales preliminares <br> Estudio de factibilidad | Actualizaciones en `vision.md`<br>`docs/glosario.md`<br>`docs/requisitos/requisitos-funcionales.md`<br>`docs/requisitos/requisitos-no-funcionales.md`<br>`docs/requisitos/estudio-factibilidad.md`                                                                        |
|     2     | 31 May – 06 Jun | Inicio       | **Reajuste:** Requisitos Funcionales y No Funcionales <br> Estudio de Factibilidad <br> Diagrama de CU ~20% <br> Game Design Document ~20%                          | `docs/requisitos/casos-de-uso/modelo-casos-uso.md`<br>`docs/diagramas/diagrama-casos-de-uso.puml` `docs/requisitos/requisitos-funcionales.md`<br>`docs/requisitos/requisitos-no-funcionales.md`<br>`docs/requisitos/estudio-factibilidad.md`<br>`docs/game-design/gdd.md` |
|     3     | 07 Jun – 20 Jun | Elaboración  | Game Design Document 100% <br> Diagrama CU completo <br> Casos de Uso Especificados                                                                                 | `docs/game-design/gdd.md`, `docs/requisitos/casos-de-uso/modelo-casos-uso.md`, `docs/diagramas/diagrama-casos-de-uso.puml`<br>`docs/requisitos/casos-de-uso/CU-XX-####-especificacion.md`<br>                                                                             |
|     4     | 21 Jun – 04 Jul | Elaboración  | Clases de análisis (conceptos) con atributos y relaciones <br> Modelo de dominio completo <br> Diagramas de Secuencia de Sistema y Contratos de Operaciones (~50%)  | `docs/analisis/modelo-de-dominio/concepto-####.md`<br>`docs/diagramas/modelo-de-dominio.puml`<br>`docs/analisis/secuencia/secuencia-CU-XX.md`(carpeta ~50% completa)                                                                                                      |
|     5     | 05 Jul – 18 Jul | Elaboración  | 100% DSS y Contratos <br> Diseño de interfaces web <br> Diseño de interfaces y sprites para el videojuego <br>                                                      | `docs/analisis/secuencia/*`(100% completo)<br>`docs/diseño/interfaces-web/*.png`<br>`docs/game-design/interfaces/*.png`<br>`docs/game-design/sprites/*.png`                                                                                                               |
|     6     | 19 Jul – 01 Ago | Elaboración  | Casos de Uso Reales <br> Diagramas de Secuencia de Diseño <br> Diagrama de Clases                                                                                   | `docs/diseño/secuencia-diseño/CU-XX/*nombre-operacion.puml`<br>`docs/diagramas/diagrama-clases.puml`<br>`docs/diseño/casos-uso-reales/CUR-XX-####-especificacion.md`                                                                                                      |
|     7     | 02 Ago – 15 Ago | Elaboración  | Diseño de Base de Datos (Normalizada) <br> Script SQL de la BD <br> Script SQL de: Vistas, Procedimientos Almacenados, Funciones y Triggers                         | `docs/diseño/base-de-datos/diseño-bd.png`<br>`docs/diseño/base-de-datos/script-bd.sql`<br>`docs/diseño/base-de-datos/script-vistas-sp-funciones-triggers.sql`                                                                                                             |
|     8     | 16 Ago – 29 Ago | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|     9     | 23 Ago – 05 Sep | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|    10     | 06 Sep – 19 Sep | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|    11     | 20 Sep – 03 Oct | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|    12     | 04 Oct – 17 Oct | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|    13     | 18 Oct – 31 Oct | Construcción | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |
|    14     | 01 Nov – 15 Nov | Transición   | ...                                                                                                                                                                 | ...                                                                                                                                                                                                                                                                       |

---

## 3. Roles y Responsabilidades

| Rol                     | Responsable     | Responsabilidades                                     |
| ----------------------- | --------------- | ----------------------------------------------------- |
| Analista de Sistemas    | Franco Albornoz | Vision, alcance, captura de requisitos y glosario     |
| Diseñador               | Franco Albornoz | Arquitectura, Diagramas UML y Diseño de Base de Datos |
| Desarrollador Front‑end | Franco Albornoz | Implementación de UI y TDD                            |
| Desarrollador Back‑end  | Franco Albornoz | Lógica de negocio y servicios REST                    |
| Tester                  | Franco Albornoz | Pruebas unitarias e integración                       |
| Gestor de Proyecto      | Franco Albornoz | Seguimiento de iteraciones, hitos y riesgos           |

---

## 4. Análisis de Riesgos
### 4.1 Riesgos identificados

| ID  | Riesgo                                                                      | Severidad | Probabilidad |
| --- | --------------------------------------------------------------------------- | --------- | ------------ |
| R1  | Incompletitud e inexactitud de requisitos                                   | Alta      | 60%          |
| R2  | Inexperiencia en tecnologías de desarrollo                                  | Alto      | 80%          |
| R3  | Subestimación e inclumplimiento de los tiempos del proyecto                 | Alto      | 60%          |
| R4  | Baja participación en las 20 pruebas de usuario necesarias para el proyecto | Alta      | 50%          |
| R5  | Alta rotación de requisitos o alcance ambiguo                               | Alta      | 70%          |
| R6  | Pérdida de los archivos y progreso del proyecto                             | Alta      | 50%          |

### 4.2 Planificación de riesgos
#### 4.2.1 Planes preventivos
| ID  | Plan preventivo                                                                                                                                                                                                                             |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| R1  | Revisiones y validaciones de requisitos semanales con docentes. Evidenciar trazabilidad de requisitos para detectar dependencias en caso de cambio de requisitos                                                                            |
| R2  | Desde el inicio del proyecto realizar investigaciones de tecnologías, organizar material de aprendizaje (documentación, cursos, videos) y realizar la capacitación a lo largo del proyecto                                                  |
| R3  | Realizar retrospectivas en cada iteración para identificar qué NO se cumplió y planificarlo para la siguiente iteración, revisar y reajustar tiempos y cronograma si es necesario                                                           |
| R4  | Ofrecer incentivos y recordatorios periódicos a los usuarios                                                                                                                                                                                |
| R5  | Establecer un MVP (Producto Mínimo Viable) al comienzo, reacomodar ideas y planificarlas a futuro, ante cualqueir cambio reevaluar tiempo y alcance                                                                                         |
| R6  | Utilizar una herramienta de versionado (GitHub) para el código fuente y documentación, asegurarse de realizar commits regularmente durante una sesión. Utilizar un sistema de archivos en la nube como Google Drive y Notion para resguardo |

#### 4.2.2 Planes correctivos
| ID  | Plan preventivo                                                                                          |
| --- | -------------------------------------------------------------------------------------------------------- |
| R6  | Restaurar los datos a partir de la ultima copia del sistema. Clonar y sincronizar el repositorio remoto. |

---

## 5. Plan de Comunicaciones

| Destinatario | Canal                   | Frecuencia        | Responsable     |
| ------------ | ----------------------- | ----------------- | --------------- |
| Profesor     | Presentación de avances | Semanal (Lunes)   | Franco Albornoz |
| Profesor     | Estado de avance        | Semanal (Viernes) | Franco Albornoz |

---

## 6. Herramientas

- **Gestión de proyectos:** Notion
- **Documentación:** Markdown
- **Control de versiones:** GitHub
- **Motor de Base de Datos:** SQLite para desarrollo, PostgreSQL para demostración y futuro despliegue.
- **Tecnologías front-end:** HTML, CSS y JavaScript con SvelteKit + Tailwind CSS. Phaser para el entorno de videojuego.
- **Tecnologías back-end:** Node.js + NestJs + TypeScript
- **IDE:** Visual Studio Code
- **Herramientas de modelado:**
  - Digramas UML: PlantUML
  - Interfaz de usuario: Frame 0, Aseprite (Pixel Art)
  - Modelado de Base de Datos: dbdiagram.io, chartdb.io