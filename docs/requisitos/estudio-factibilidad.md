# Estudio de Factibilidad
A continuación se presenta el análisis completo de factibilidad (técnica, económica y operativa) para el desarrollo de la Plataforma Gamificada “Algoritmia” (PGA). Este documento sintetiza las respuestas aportadas por el equipo (Franco Andrés Albornoz) y completa las secciones faltantes con propuestas concretas.

## 1. Factibilidad Técnica
### 1.1 Hardware disponible
#### 1.1.1 PC principal de desarrollo
- **Marca y model**o: HP Laptop 14
- **Sistema Operativo**: Windows 11 Home (activado de fábrica) / Linux Mint 22
- **Procesador**: Intel® Core™ i5-1135G7 @ 2.40 GHz (4 núcleos / 8 hilos)
- **Memoria RAM**: 8 GB DDR4 @ 3200 MHz
- **Almacenamiento**: SSD M.2 NVMe PCIe de 240 GB (libre suficiente para proyectos)
- **Tarjeta Gráfica**: Intel Iris Xe (integrada)
- **Periféricos relevantes**:
  - Tableta gráfica Xp-Pen Deco Mini 7 (para diseño de assets en Pixel Art)

#### 1.1.2 Equipamiento de respaldo
- Actualmente no se posee otra PC de desarrollo propia.
- En caso de falla, existe copia de seguridad de todo el código y documentación en Google Drive y GitHub. Se estima conseguir una PC de reemplazo en aproximadamente 1 semana si fuera necesario.

#### 1.1.3 Licencias de Sistemas Operativos
- **Windows 11 Home**: activado.
- **Linux Mint 22**: distribución libre y actualizada.

La PC cumple con los requisitos básicos para ejecutar IDEs (VS Code), entornos locales (Node.js, SQLite) y herramientas de diseño (Aseprite). El respaldo está resuelto a través de backups en la nube.

### 1.2 Sistema Operativo y Software de Desarrollo
#### 1.2.1 Sistemas Operativos de trabajo
- **Desarrollo principal**: Se utilizará como sistema operativo principal Linux Mint 22 para el entorno de desarrollo del sistema.
- Alternativamente, se usará **Windows 11**para uso de Aseprite, Frame0, u otras herramientas que tengan compatibilidad unicamente con Windows.

#### 1.2.2 Software instalado y versiones
**Git**
- Versión: git 2.43.0 (disponible en ambos SO).
- Configuración: usuario y correo set en ~/.gitconfig.

**Aseprite**
- Versión: 1.3.3 (instalado en Windows).
- Uso: diseño y edición de sprites Pixel Art.

**Frame0**
- Versión: 1.0 (instalada en Windows y Linux).
- Uso: prototipado rápido de interfaces

**Visual Studio Code**
- Versión: 1.79.0 (instalado en ambos sistemas).
- Extensiones definidas en el apartado 1.4.2.


**Node.js / npm / Yarn**
- **Node.js**: se instalará la versión v22.16.0 LTS recomendada para compatibilidad con NestJS y dependencias.
- **npm**: v10.x (incluido con Node.js).

**Herramientas de testing**
- Jest (para back-end en Node.js/NestJS).
- Vitest (para pruebas de unidades en SvelteKit).

**Entorno de desarrollo (IDE/Editor)**
- VS Code con extensiones en Windows y Linux.
- Configuración de sincronización de settings entre ambos SO usando la función de “Settings Sync” de VS Code.

### 1.3 Stack de Desarrollo y Curva de Aprendizaje
#### 1.3.1 Front-end
**Frameworks y librerías**
- SvelteKit 2
- Tailwind CSS (v4.0) para estilos utilitarios.
- Phaser v3.90.0 "Tsugumi" para la parte de motor de juego y animaciones Pixel Art.

**Nivel de experiencia actual**
- Sin experiencia previa directa en SvelteKit, Tailwind o Phaser. Conocimiento general de JavaScript y conceptos de front-end.

**Recursos de capacitación**

**HTML, CSS y JavaScript básico**
- Cursos gratuitos de MiduDev en YouTube.
- Documentación oficial de MDN (Mozilla).

**SvelteKit y Tailwind CSS**
- Tutoriales oficiales de SvelteKit y Tailwind, ejemplos y cursos de MiduDev.
- Documentación en línea:
  - https://kit.svelte.dev/docs
  - https://tailwindcss.com/docs

Phaser v3.90.0
- Cursos y listas de reproducción en YouTube.
- Documentación oficial: https://phaser.io/docs
- Ejemplos de proyectos en GitHub para referencia.

#### 1.3.2 Back End
**Framework y entorno de ejecución**
- Node.js (v22.16.0 LTS) con NestJS (v11.x) en TypeScript.

**Nivel de experiencia actual**
- Sin experiencia previa directa en NestJS; conocimientos básicos de Node.js y TypeScript.

**Recursos de capacitación**
- Curso de Nestjs - Framework Backend de Nodejs en YouTube (Fazt Code).
- Documentación oficial: https://docs.nestjs.com
- Ejemplos de proyectos CRUD con NestJS en GitHub.

**Lenguaje de servidor**
- TypeScript (v5.8.3) para mejorar control de tipos y escalabilidad.

#### 1.3.3 Base de Datos
Elección inicial:
- SQLite como base de datos local para desarrollo rápido y pruebas sin requerir servidor adicional.

Migración futura:
- PostgreSQL para entornos de demostración y despliegue (DB MS completo).

Nivel de conocimiento actual:
- Conocimiento en modelos relacionales con normalización (3ra forma).

Recursos de capacitación:
- Tutorial “SQLite tutorial” (Página oficial sqlite.org).
- Curso “PostgreSQL básico” en YouTube (Academia de DB).
- Documentación oficial: https://www.postgresql.org/docs

El objetivo es modelar inicialmente con SQLite y, en fase de demostración del sistema, migrar a PostgreSQL para integrar consultas avanzadas (vistas, triggers, funciones).

#### 1.3.4 Curva de Aprendizaje y Recursos

**Tiempo estimado para dominar tecnologías elegidas**
- HTML/CSS/JS: 3 semanas
- SvelteKit + Tailwind + Phaser: 3 semanas adicionales
- Node.js + NestJS + SQLite + TypeScript: 4 semanas
- Total estimado: 10 semanas de dedicación (2–3 horas diarias).

**Recursos gratuitos o pagos**
- YouTube (MiduDev) para la mayoría de tutoriales.
- Documentación oficial de cada framework/librería.
- Foros (Stack Overflow) y comunidad de Discord/GitHub.

**Cronograma de aprendizaje**
| Semana          | Tecnología                             |
| --------------- | -------------------------------------- |
| 09 Jun - 15 Jun | HTML - CSS - JavaScript                |
| 16 Jun - 22 Jun | HTML - CSS - JavaScript                |
| 23 Jun - 29 Jun | HTML - CSS - JavaScript                |
| 30 Jun - 06 Jul | Svelte - Tailwind - Phaser             |
| 07 Jul - 13 Jul | Svelte - Tailwind - Phaser             |
| 14 Jul - 20 Jul | Svelte - Tailwind - Phaser             |
| 21 Jul - 27 Jul | Node.js - NestJs / SQLite / TypeScript |
| 28 Jul - 03 Ago | Node.js - NestJs / SQLite / TypeScript |
| 04 Ago - 10 Ago | Node.js - NestJs / SQLite / TypeScript |
| 11 Ago - 17 Ago | Node.js - NestJs / SQLite / TypeScript |
| 18 Ago - 24 Ago | Node.js - NestJs / SQLite / TypeScript |

Con un cronograma de 10 semanas y recursos gratuitos (canal MiduDev, documentación), la curva de aprendizaje es asumible. En caso de mayor dificultad, se tomarán horas extra y se consultará con docentes o compañeros familiarizados con el stack.