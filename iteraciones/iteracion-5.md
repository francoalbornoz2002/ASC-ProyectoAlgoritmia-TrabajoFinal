# Plan de Iteración

**Iteración Nº:** `5`  
**Fase UP:** `Elaboración`
**Fechas:** `05/07/2025 - 18/07/2025`  
**Duración:** `2 semanas`

---

## 1. Objetivos de la Iteración

- Realizar el Modelo de Dominio del sistema
- Realizar los Diagramas de Secuencia del Sistema
- Continuar con el Game Design Document hasta el punto 7.
- Diseñar las primeras pantallas clave de la web.

## 2. Alcance

- **Artefactos** a generar
  - `modelo-dominio.md`
  - `modelo-dominio.puml`
  - `DSS-CU-XX-####.md`
  - `interfaces-web.png`

## 3. Actividades y Tareas

| Actividad                  | Tarea concreta                                        | Artefacto (salida)                                                                         |
| -------------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Modelo de dominio          | Identificar conceptos idóneos                         | Sección "Conceptos idóneos" en `docs/analisis/modelo-dominio/modelo-dominio.md`            |
| Modelo de dominio          | Descripción de los conceptos                          | Sección "Descripción de los conceptos" en `docs/analisis/modelo-dominio/modelo-dominio.md` |
| Modelo de dominio          | Definir las relaciones entre los conceptos            | Sección "Relaciones entre conceptos" en `docs/analisis/modelo-dominio/modelo-dominio.md`   |
| Modelo de dominio          | Describir los atributos de cada concepto              | Sección "Descripción de los atributos" en `docs/analisis/modelo-dominio/modelo-dominio.md` |
| Modelo de dominio          | Realizar el diagrama del modelo de dominio            | Sección "Modelo de dominio" en `docs/analisis/modelo-dominio/modelo-dominio.md`            |
| Comportamiento del sistema | Realizar Diagrama de Secuencia de Sistema y contratos | `DSS-CU-XX-####.md` con diagrama y contratos por cada DSS                                  |

## 4. Entregables

- `docs/analisis/modelo-dominio/modelo-dominio.md`
- `docs/analisis/modelo-dominio/modelo-dominio.png`
- `docs/diagramas/modelo-dominio.puml`
- `docs/analisis/diagrama-secuencia-sistema/*`
- Actualizaciones en `docs/game-design/gdd.md`
- `docs/diseño/interfaces-web/interfaces-clave.png`

## 5. Definition of Done (DoD)

- [ ] Modelo de dominio terminado 
- [ ] DSS y Contratos de los casos de uso críticos terminados
- [ ] Primeras interfaces web diseñadas
- [ ] Primeras interfaces del videojuego diseñadas

## 6. Riesgos y Mitigaciones

| Riesgo                                                                        | Mitigación                                                                                                          |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Especificación incompleta de casos de uso que impacte en el modelo de dominio | Refactorización y verificación constante de los casos de uso al momento de comenzar a realizar le modelo de dominio |
| Incompatibilidad de PlantUML para realizar el modelo de dominio               | Modelarlo como un diagrama de clases (sin métodos) o consideración de otra herramienta                              |

---

## 7. Notas Adicionales

- Dependencias, feedback y recordatorios generales.
