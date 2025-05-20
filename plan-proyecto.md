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

| Iteración | Fechas          | Fase UP      | Objetivo principal                                                                                                                                                                 | Entregables clave                                                                                                                                                                                                                                                         |
| :-------: | :-------------- | :----------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|     0     | 10 May – 16 May | Incepción    | Plan global <br> Repositorio y estructura <br> Visión y alcance preliminares                                                                                                       | `vision.md`<br>`plan-proyecto.md`<br>`docs/iteraciones/iteracion-0/iteracion-0.md`<br>`docs/iteraciones/iteracion-0/retrospectiva-0.md`                                                                                                                                   |
|     1     | 17 May – 30 May | Incepción    | Doc. de Visión completo <br> Glosario <br> Requisitos Funcionales <br> Requisitos No Funcionales <br> Factibilidad (Técnica, Económica y Operativa) <br> Diagrama CU Ligero (~20%) | Actualizaciones en `vision.md`<br>`docs/glosario.md`<br>`docs/analisis/requisitos-funcionales.md`<br>`docs/analisis/requisitos-no-funcionales.md`<br>`docs/analisis/estudio-factibilidad.md`<br>`docs/modelo-casos-uso.md`<br>`diagramas/vista-casos-de-uso.puml`(ligero) |
|     2     | 31 May – 13 Jun | Elaboración  | Diagrama CU completo <br> 80% CU Especificados <br>                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     3     | 14 Jun – 27 Jun | Elaboración  | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     4     | 28 Jun – 11 Jul | Elaboración  | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     5     | 12 Jul – 25 Jul | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     6     | 26 Jul – 08 Ago | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     7     | 09 Ago – 22 Ago | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     8     | 23 Ago – 05 Sep | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|     9     | 06 Sep – 19 Sep | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|    10     | 20 Sep – 03 Oct | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|    12     | 04 Oct – 17 Oct | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|    13     | 18 Oct – 31 Oct | Construcción | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |
|    14     | 01 Nov – 15 Nov | Transition   | ...                                                                                                                                                                                | ...                                                                                                                                                                                                                                                                       |

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

## 4. Riesgos y Mitigaciones

| Riesgo                                   | Severidad | Mitigación                                  |
| ---------------------------------------- | --------- | ------------------------------------------- |
| Incompletitud en requisitos              | Alta      | Revisiones semanales con docentes           |
| Retrasos en entregas de prototipos UI    | Media     | Iteraciones de 1 semana, buffer de 1 semana |
| Baja participación en pruebas de usuario | Alta      | Incentivos y recordatorios proactivos       |

---

## 5. Plan de Comunicaciones

| Destinatario | Canal                   | Frecuencia        | Responsable     |
| ------------ | ----------------------- | ----------------- | --------------- |
| Profesor     | Presentación de avances | Semanal (Lunes)   | Franco Albornoz |
| Profesor     | Estado de avance        | Semanal (Viernes) | Franco Albornoz |

---

## 6. Herramientas

- **Control de versiones:** GitHub
- **Documentación:** Markdown
- **Modelado UI:** Frame 0, Aseprite (Pixel Art)
- **Desarrollo futuro:** Godot, Node.js, MySQL
- **CI/CD:** GitHub Actions