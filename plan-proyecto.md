# Plan del Proyecto

**Versión:** 1.1
**Fecha de inicio:** 10/05/2025
**Autor(es):** Franco Andrés Albornoz

---

## 1. Cronograma General

| Fase         | Fecha Inicio | Fecha Fin  | Responsable            |
| ------------ | ------------ | ---------- | ---------------------- |
| Incepción    | 10-05-2025   | 30-05-2025 | Franco Andrés Albornoz |
| Elaboración  | 31-05-2025   | 11-07-2025 | Franco Andrés Albornoz |
| Construcción | 12-07-2025   | 31-10-2025 | Franco Andrés Albornoz |
| Transición   | 01-11-2025   | 15-11-2025 | Franco Andrés Albornoz |

---

## 2. Iteraciones

| Iteración | Fechas          | Fase UP      | Objetivo principal                                                                                                                                                                                                        | Entregables clave                                                                                                                                                                                                                                                         |
| :-------: | :-------------- | :----------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|     0     | 10 May – 16 May | Incepción    | Plan global <br> Repositorio y estructura <br> Visión y alcance preliminares                                                                                                                                              | `vision.md`<br>`plan-proyecto.md`<br>`docs/iteraciones/iteracion-0/iteracion-0.md`<br>`docs/iteraciones/iteracion-0/retrospectiva-0.md`                                                                                                                                   |
|     1     | 17 May – 30 May | Incepción    | Doc. de Visión completo <br> Riesgos y mitigación del proyecto <br> Glosario <br> Requisitos Funcionales <br> Requisitos No Funcionales <br> Factibilidad (Técnica, Económica y Operativa) <br> Diagrama CU Ligero (~20%) | Actualizaciones en `vision.md`<br>`docs/glosario.md`<br>`docs/analisis/requisitos-funcionales.md`<br>`docs/analisis/requisitos-no-funcionales.md`<br>`docs/analisis/estudio-factibilidad.md`<br>`docs/modelo-casos-uso.md`<br>`diagramas/vista-casos-de-uso.puml`(ligero) |
|     2     | 31 May – 13 Jun | Elaboración  | Diagrama CU completo <br> 80% CU Especificados <br> 50% Clases de análisis (Conceptos) <br> Modelo de dominio ligero (~50%)                                                                                               | Actualizaciones en `diagramas/vista-casos-de-uso.puml`<br>`docs/analisis/casos-de-uso/CU-XX-####-especificacion.md`(~80% completo)<br> `docs/analisis/modelo-de-dominio/concepto-####.md`                                                                                 |
|     3     | 14 Jun – 27 Jun | Elaboración  | 100% CU Especififacos <br> 100% Clases de Análisis (Conceptos) <br> Modelo de dominio completo <br> Diagramas de Secuencia de Sistema y Contratos de Operaciones (~50%)                                                   | `docs/analisis/casos-de-uso/*`(carpeta 100% completa) <br> `docs/analisis/modelo-de-dominio/*`(carpeta 100% completa) <br> `docs/analisis/secuencia/secuencia-CU-XX.md`(carpeta ~50% completa)                                                                            |
|     4     | 28 Jun – 11 Jul | Elaboración  | 100% DSS y Contratos <br> Diagramas de Secuencia de Diseño <br> Diagrama de Clases (~75%)                                                                                                                                 | `docs/analisis/secuencia/*`(100% completo) <br> `docs/diseño/secuencia-diseño/secuencia-diseño-CU-XX-#####.puml`(carpeta 100% completa)                                                                                                                                   |
|     5     | 12 Jul – 25 Jul | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|     6     | 26 Jul – 08 Ago | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|     7     | 09 Ago – 22 Ago | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|     8     | 23 Ago – 05 Sep | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|     9     | 06 Sep – 19 Sep | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|    10     | 20 Sep – 03 Oct | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|    12     | 04 Oct – 17 Oct | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|    13     | 18 Oct – 31 Oct | Construcción | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |
|    14     | 01 Nov – 15 Nov | Transition   | ...                                                                                                                                                                                                                       | ...                                                                                                                                                                                                                                                                       |

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
| R2  | Desde el inicio del proyecto realizar investigaciones de tecnologías, organizar material de aprendizaje (documentación, cursos, videos) y realizar la capacitación                                                                          |
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
- **Motor de Base de Datos:**
- **Tecnologías front-end:**
- **Tecnologías back-end:**
- **Herramientas de modelado:**
  - Digramas UML: PlantUML
  - Interfaz de usuario: Frame 0, Aseprite (Pixel Art)
  - Modelado de Base de Datos: dbdiagram.io
- **CI/CD:** GitHub Actions