# Estudio de Factibilidad
A continuación se presenta el análisis completo de factibilidad (técnica, económica y operativa) para el desarrollo de la Plataforma Gamificada “Algoritmia” (PGA). Este documento sintetiza las respuestas aportadas por el equipo (Franco Andrés Albornoz) y completa las secciones faltantes con propuestas concretas.

## 1. Factibilidad Técnica
### 1.1 Hardware disponible
#### 1.1.1 PC principal de desarrollo
- **Marca y modelo**: HP Laptop 14
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

La PC cumple con los requisitos básicos para ejecutar IDEs (VS Code y Phaser Launcher), entornos locales (Node.js, SQLite) y herramientas de diseño (Aseprite). El respaldo está resuelto a través de backups en la nube.

### 1.2 Sistema Operativo y Software de Desarrollo
#### 1.2.1 Sistemas Operativos de trabajo
- **Desarrollo principal**: Se utilizará como sistema operativo principal Windows 11 para el entorno de desarrollo del sistema, debido a la compatibilidad con herramientas clave para el desarrollo del sistema como Phaser Launcher, Aseprite y Frame0.

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

**Entorno de desarrollo (IDE): Visual Studio Code**
- Versión: 1.79.0 (instalado en ambos sistemas).
- Extensiones definidas en el apartado 1.4.2.
- Configuración de sincronización de settings entre ambos SO usando la función de “Settings Sync” de VS Code.

#### 1.2.3 Software a instalar y versiones
**Node.js / npm /**
- **Node.js**: se instalará la versión v22.16.0 LTS recomendada para compatibilidad con NestJS y dependencias.
- **npm**: v10.x (incluido con Node.js).

**Bases de datos: SQLite y PostgreSQL**
- SQLite en su versión 3.50.0
- PostgreSQL en su versión 17.5

**Herramientas de testing**
- Se instalará Jest (para back-end en Node.js/NestJS).
- Se instalará Vitest (para pruebas de unidades en SvelteKit).

**Phaser Launcher**
- Se instalará la versión v3.90.0 en Windows.

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
- Tutoriales oficiales de SvelteKit y Tailwind, ejemplos y cursos en YouTube.
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
**Elección inicial**:
- SQLite como base de datos local para desarrollo rápido y pruebas sin requerir servidor adicional.

**Migración futura**:
- PostgreSQL para consultas avanzadas, demostración y defensa y despliegue (DBMS completo).

**Nivel de conocimiento actual**:
- Conocimiento en modelos relacionales con normalización (3ra forma).
- Conocimientos en base de datos activas (vistas, funciones, triggers)

**Recursos de capacitación**:
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

### 1.4 Infraestructura para Desarrollo Local
#### 1.4.1 Máquina de Desarrollo
No se planea utilizar Docker o Kubernetes inicialmente, debido a falta de experiencia y al desarrollo local con SQLite y entornos Node.js integrados. Si surgiera la necesidad en despliegues futuros, se evaluará agregar Docker para contenerización.

#### 1.4.2 IDE y herramientas
**IDEs**
- Visual Studio Code en Linux Mint 22 y Windows 11.
- Phaser Launcher en Windows 11.

**Extensiones de VS Code**
- Markdown
  - `Markdown All in One` para mejoras en la edición de documentos MD.
  - `Markdown Preview Enhanced` para vista previa.
  - `Markdown PDF` para exportar a PDF.
- Control de Versiones
  - `Git Extension Pack` que integra comandos de Git.
  - `GitLens` para inspección avanzada del repositorio.
- Asistente de IA
  - `GitHub Copilot` para sugerencias de código en general.
  - `IntelliSense` para sugerencias y autocompletado de codigo en general.
- Modelado UML
  - `Plant UML` para renderizado de diagramas a partir de texto
- Liting y formateo
  - `ESLint` para JavaScript y TypeScript
  - `Prettier` para formateo de código
- Lenguajes y Frameworks
  - `Svelte for VS Code` para resaltado de sintaxis y snippets de SvelteKit.
  - `Tailwind CSS IntelliSense` para autocompletado de clases Tailwind.
  - `Node.js Extension Pack` integrado para Node.js
  - `Vscode NestJs Snippets` para autocompletado y atajos de código para controllers, services, modules.
- Depuración y Testing
  - `JavaScript` Debugger para depuración del front-end en navegador.
  - `Jest` para integración de pruebas unitarias en back-end.
  - `Vitest` para pruebas de unidades en SvelteKit

#### 1.4.3 Control de versiones
**Repositorio remoto**
En GitHub (cuenta personal), se creó un repositorio para el proyecto denominado "ASC-ProyectoAlgoritmia-TrabajoFinal". Enlace: https://github.com/francoalbornoz2002/ASC-ProyectoAlgoritmia-TrabajoFinal

**Flujo de ramas**
Se usará GitHub Flow como estrategia simple basada en la rama `main` y ramas de `feature`
1. Crear rama `feature/<nombre>` para cada funcionalidad.
2. Hacer Pull Request (PR) a `main` al terminar la feature.
3. Revisar, aprobar y mergear.
4. `main` siempre contiene código listo para producción o demostración local.
Este enfoque permite despliegues frecuentes, PRs ágiles y evita complejidad de ramas intermedias.

### 1.5 Dependencias Externas
#### 1.5.1 Google OAuth2.0 (Passport.js)
**Librería**
Se utilizará la libería Passport.js en su versión 0.7.0 con la estrategia `passport-google-oauth20` para la autenticación de usuarios (alumnos) mediante cuenta Google, se manejará la integración con NestJs con @nestjs/passport y estrategias de PassportStrategy.

**Proyecto en Google Cloud Console**
Aún no creado. Se generarán credenciales (Client ID & Client Secret) en la sección “APIs & Services → Credentials” de Google Cloud, configurando el URI de redirección a http://localhost:3000/auth/google/callback. La configuración de OAuth2.0 tendrá un alcance de: profile y email.

#### 1.5.2 Librería para animaciones y Pixel Art
**Phaser**
Phaser es un framework de desarrollo de juegos 2D para navegadores web (HTML5). Facilita la creación de juegos en 2D, especialmente en navegadores de escritorio y móviles, con funcionalidades como gráficos, física, sonido y animaciones. Se eligió por:
- Motor de física y animación de sprites integrado.
- Manejador de recursos (tilesets, spritesheets).
- Comunidad activa y ejemplos claros.
- Se integra correctamente con cualquier framework front-end moderno (SvelteKit en este caso) a través de la creación de un “canvas” en la aplicación.
Tambien resulta compatible con SvelteKit
- Phaser se carga como módulo ES (import Phaser from 'phaser').
- Se inicializa dentro de un componente Svelte que incluya `<canvas>` con `bind:this={container}`.
- Documentación de ejemplo: https://github.com/phaserjs/examples

Otra opción de librería para crear el videojuego era PixiJs, pero se descarto debido a:
- PixiJS es más liviano para renderizado 2D, pero no incluye motor de física ni tutoriales específicos para juegos de lógica/rompecabezas.
- Phaser provee sistemas de escena, input management y suport de físicas (Arcade Physics) listo para usar.

#### 1.5.3 Recursos Pixel Art gratuitos
Se planea que para los tilesets y assets del videojuego, se utilicen recursos gratuitos de libre uso. La mayoría de estos packs de assets se encuentran en Itch.io (sección “Assets”, licencias CC0 o CC-BY).
Igualmente, si surge la necesidad como no encontrar un pack de assets integrado o el pack elegido cambie repentinamente la licencia, se evaluarán packs premium de Itch.io (costo variable) o crear assets propios en Aseprite.

### 1.6 Restricciones Técnicas
1. Versión mínima de Node.js: Se empleará Node.js ≥ v18.x, idealmente v22.16.0 LTS. Esto asegura compatibilidad con NestJS v10 y dependencias modernas.
2. Versión mínima de npm: se usará npm 10 que viene incluido con Node.js v22.16.0 LTS.
3. Requerimientos de navegador:
   - Navegadores recomendados: Chrome, Firefox, Edge, Safari (versiones recientes en soporte).
   - Si bien SvelteKit y Phaser generan un canvas HTML5 compatible con la mayoría, se indicará en documentación que se use una versión modern (Chrome ≥ 100, Firefox ≥ 100).
4. Resolución / FPS para animaciones Pixel Art
   - Phaser configurado para 60 FPS, resolución 800×600 (adaptable).
   - Meta de rendimiento: ≥ 30 FPS en hardware modesto (Intel UHD Graphics + 4 GB RAM).
   - Probar en netbooks del estado argentino garantiza fluidez con ajustes de calidad mínima (sin postprocesamiento extra).
5. Compatibilidad mínima garantizada
   - Windows 10+
   - Distribuciones Linux con kernel ≥ 5.4.

### 1.7 Conclusión de Factibilidad Técnica
**Infraestructura actual suficiente**
La PC (Intel i5, 8 GB, SSD) es suficiente para IDEs, compilación de Node.js, compilación de SvelteKit + Phaser y diseño Pixel Art en Aseprite. Por el momento no se requiere nuevo equipamiento; en caso de fallo, la copia de seguridad en la nube permite retomar el desarrollo rápidamente.

**Herramientas y lenguajes**
Falta por instalar Node.js v20, NestJS, SvelteKit, Phaser, Jest y Vitest. Por lo demás, Git, VS Code, Aseprite y Frame0 ya funcionan correctamente en los dos sistemas operativos.

**Riesgos técnicos**
- El riesgo técnico más crítico es la curva de aprendizaje de SvelteKit, Phaser y NestJS, donde cada uno requiere 3–4 semanas de estudio.
- Posible incompatibilidad de Phaser con SvelteKit si se integra incorrectamente. Si llegase a pasar, se buscarán alternativas viendo ejemplos de la comunidad o la documentación oficial de Phaser en el apartado de plantillas para Svelte.
- Falta de experiencia en testing unitario. Pero resulta un riesgo mitigable con 1–2 semanas de práctica.

**Medidas mitigadoras**
- Cursos y tutoriales de YouTube (MiduDev) y documentación oficial antes de la fase de construcción.
- "Pair programming" con compañeros familiarizados con alguna de las tecnologías.
- Consultoría puntual con docentes o la comunidad en Discord/GitHub Issues si surge un bloqueo.

Técnicamente, el proyecto es factible con la infraestructura actual. Se prevén riesgos principalmente asociados a la curva de aprendizaje, pero existen planes de mitigación como el cronograma de estudio y recursos en línea.

## 2. Factibilidad Económica
### 2.1 Personal y Recursos Humanos

**Equipo de desarrollo**
Franco Andrés Albornoz (único desarrollador), asumiendo roles de:
- Analista de Sistemas
- Diseñador Pixel Art (uso de Aseprite)
- Desarrollador Front-end (SvelteKit, Phaser)
- Desarrollador Back-end (NestJS, SQLite/PostgreSQL)
- Tester (pruebas unitarias y funcionales con Jest/Vitest)
- Gestor de Proyecto (planificación, seguimiento, documentación)

**Ayuda académica**
- **Tutores**: Docentes de la cátedra “Trabajo Final (ASC)” y “Proyecto Software (LSI)” (Mgter. Sergio D. Caballero, ASC. Juan José Bolano) serán consultados para validación académica.
- **Compañeros de materia**: En caso de dudas técnicas, se recurrirá al grupo de compañeros.
- **Docentes de la cátedra AyED I**: En caso de dudas acerca de contenido académico o formas de trabajo, se consultarán a los distintos docentes de la cátedra.

**Subcontratación futura**
- No se prevé contratar artistas o gestores externos en el corto plazo.
- Si PGA crece en alcance, se podría considerar incorporar un artista Pixel Art freelance para packs avanzados o un administrador de sistemas.

### 2.2 Costo de Hardware y Licencias de Software
En el proyecto en general, no se requieren gastos adicionales significativos en hardware o licencias. Se pasa a detallar los costos y licencias:

**Licencias de IDE / herramientas**
- Aseprite: ya adquirido (aprox. 20 USD).
- Frame0: gratuito.
- VS Code: gratuito (open source).
- Phaser, SvelteKit, Tailwind, NestJS, SQLite: todos frameworks/licencias MIT gratuitos.

**Recursos adicionales planeados**
- Tableta gráfica (Xp-Pen Deco Mini 7): ya disponible.
- No se requiere comprar monitores o microservicios en nube por ahora.

**Recursos Pixel Art**
- Itch.io / OpenGameArt: se usarán assets CC0 o CC-BY gratuitos.
- No se planean compras de packs premium de inmediato.

### 2.3 Costo de Infraestructura (Servidores, Hosting, Cloud)

**Despliegue inicial**
- Se realizará solo en local para la demostración final (proyección en aula).
- No se contratará servidor en la nube en esta fase de Trabajo Final.

**Hosting futuro (opcional)**
- Cuando se considere el despliegue real, se evaluarán planes gratuitos / educativos:
  - GitHub Student Developer Pack (posibles créditos en DigitalOcean, AWS Educate).
  - Heroku (Free Tier), Fly.io, Render.com (Free Tier) para back-end y SQLite.
  - Vercel o Netlify para despliegue front-end (gratuitos con limitaciones de CPU/ram).

**Dominios y SSL**
- Para demo local no se requiere dominio ni SSL.
- Futuro: usar Let’s Encrypt (gratuito) para certificados SSL; dominios gratuitos (por ejemplo, subdominios de Vercel).

### 2.4 Beneficios Esperados
Con el desarrollo e implementación del sistema, se esperan los siguientes beneficios a corto y largo plazo

**Beneficios a corto plazo**
- **Alumnos motivados**: entorno Pixel Art y dinámica de misiones/XP incrementan la retención y compromiso.
- **Seguimiento académico**: tablero de progreso individual y grupal disponible desde la primera semana, facilitando la detección de rezagados.
- **Feedback formativo inmediato**: propone optimizaciones de código, lo cual acelera la curva de aprendizaje.

**Beneficios a largo plazo**
- **Menos alumnos atrasados**: adopción de PGA como herramienta de práctica reduce la cantidad de alumnos que repiten la materia.
- **Base sólida de conocimientos**: resolución constante de misiones con feedback mejora la competencia en algoritmia para materias posteriores.
- **Identidad institucional**: sustitución oficial de Visual DaVinci por PGA (herramienta propia de FCEQyN) fortalece sentido de pertenencia y evita licencias externas.

### 2.5 Riesgos Económicos

**1. Subestima de tiempo y esfuerzo**
  - **Posible escenario**: Curva de aprendizaje de alguna tecnología demora más de lo calculado (15 semanas en vez de 10).
  - **Impacto económico**: No se traduce en gasto monetario adicional inmediato (sin contrataciones externas), pero el tiempo extra implicaría retraso en la entrega y reajuste del cronograma académico.
  - **Mitigación**: Ajustar semanalmente el cronograma en caso de desviaciones, destinar horas extras de estudio, solicitar ayuda puntal a tutores.

**2. Dependencia de recursos externos de pago**
  - **Posible escenario**: Un pack de sprites gratuito cambia a modelo de pago cuando ya se ha avanzado en la interfaz con esos assets.
  - **Impacto económico**: Si se adquiere la licencia, podría costar entre USD 10–20 por pack; en caso de no adquirir, se requeriría rediseñar assets propios o buscar alternativas equivalentes.
  - **Mitigación**:
    - Si el costo no es muy elevado, adquirir la licencia.
    - Usar assets con licencia Creative Commons Zero (CC0) (OpenGameArt) que no cambian a pago.
    - Mantener copia de los assets descargados en caso de pérdida de licencia.

**3. Imprevistos en licencias o hardware**
  - **Posible escenario**: Falla total de la PC principal, obligando a comprar una nueva (~ USD 500 – 700 para un equipo modesto).
  - **Impacto económico**: Gastos directos en reemplazo de hardware.
  - **Mitigación**:
    - Definir un fondo de contingencia mensual pequeño (p. ej. USD 20–30).
    - Posponer compra de hardware nuevo a momento de necesidad real; usar PC de laboratorio de la facultad mientras tanto.

### 2.6 Conclusión de Factibilidad Económica
**1. Costos asumibles**
  - No se requieren gastos adicionales en licencias o equipos: Aseprite ya está pagado, resto de herramientas son gratuitas.
  - El único posible gasto sería la compra de hardware en caso de falla grave (amortizable a mediano plazo).
  - No hay necesidad de contratar personal adicional en esta fase.

**2. Medidas mitigadoras**
  - En caso de sobrecostos, usar exclusivamente recursos open source (Phaser, SvelteKit, SQLite).
  - Posponer despliegue en la nube (usar local para demo).
  - Reasignar tiempo para corregir desviaciones en la curva de aprendizaje.

**3. Posibles fuentes de financiamiento**
  - **Convenio académico de UNaM**: podría solicitarse subsidio para licencia de assets premium si fuera necesario.
  - **GitHub Student Developer Pack**: créditos para DigitalOcean o Heroku.

## 3. Factibilidad Operativa
### 3.1 Adaptación a la Dinámica de la Cátedra
1. Integración de PGA en la rutina de la cátedra

- Uso como herramienta principal
  - La plataforma PGA está pensada y orientada para darle uso como herramienta principal para guiar las prácticas de la materia.
  - PGA reemplazará a Visual DaVinci en prácticas de Algoritmos y Estructuras de Datos I.
  - Se actualizará el programa de la materia (previa aprobación de directivos) para incorporar PGA desde el inicio del cuatrimestre.

- Taller inicial de introducción
  - Donde se realizará una sesión de 1 hora para mostrar y presentar la plataforma PGA a todos los alumnos, mostranto temas como la navegación básica, los primeros pasos y ejercicios y otras funcionalidades.

- Asignación de ejercicios
  - Docentes podrán asignar misiones específicas como tarea para la siguiente clase, reforzando la práctica fuera de horario presencial.

2. Coexistencia con teoría, práctica y consulta
  - Teoría (lunes 10:00–12:00):
    - Se mostrará el concepto teórico en clase mediante presentaciones en diapositivas; PGA se mencionará como complemento para practicar. Dicho tema teórico tendrá que tener la sintaxis y semántica definida por PGA.
  - Práctica (lunes 17:00–19:00, miércoles 10:30–12:30):
    - Los alumnos usarán PGA en clase para resolver ejercicios mientras el docente supervisa y responde consultas, dudas o repasa algunos temas teóricos.
  - Consulta (jueves 19:00–20:00):
    - Los alumnos pueden traer dudas sobre ejercicios de PGA; el docente empleará PGA para replicar y explicar cada caso.

### 3.2 Aceptación por Parte de Alumnos y Docentes
1. Alumnos
  - **Encuesta previa**: Se han encuestado en total a 26 alumnos ingresantes y 7 alumnos avanzados (más de un año en la carrera). 
    - 80.7 % de ingresantes opina que gamificación aumentaría “bastante” o “mucho” su compromiso.
    - 84.6 % valora como “Muy importante” recibir sugerencias automáticas de optimización.
    - Los ingresantes indican que las características que hubieran querido tener son: interfaz intuitiva, agradable a la vista, ayuda y especificación de errores y sintaxis intuitiva.
    - En cuanto a las tres mejoras prioritarias que desearían tener: sintaxis sencilla, indicador de errores de sintaxis, interfaz sencilla, atractiva y agradable, sugerencias automáticas para optimización.
    - **Resumen**: Claramente existe una demanda significativa de los alumnos por una plataforma más atractiva y con feedback formativo.
  - **Grupo mínimo viable para pilotar PGA**:
    - Tomar al menos 20 usuarios (entre ingresantes, avanzados y 1–2 docentes) para una prueba inicial.
    - Se propone: 15 ingresantes del año 2025 + 3 avanzados + 2 docentes para recibir feedback exhaustivo.

2. Docentes
- **Nivel de comodidad con tecnología** 
Todos los docentes manejan muy bien la tecnología web. Se trata de una factulad que dicta solo carreras de informática y donde se utilizan aulas virtuales para el dictado de las materias, por lo tanto los docentes estan muy bien capacitados en la parte de computación y navegación web.

- **Resistencia al cambio**
Ningún docente manifestó rechazo; al contrario, hubo entusiasmo por modernizar Visual DaVinci.
Segun la entrevista realizada al Profesor Adjunto de la cátedra Algoritmos y Estructuras de Datos I, el Licenciado Mario Vialey, la idea le atrae mucho y considera que es una buena posibilidad para incorporar esta plataforma a la cátedra, ya que el Visual Da Vinci ya que viene utilizando desde 2007 en la materia y considera que sería bueno un "nuevo aire" para los alumnos, además de ayudarle a tener un seguimiento del estado de avance de los alumnos.

- **Capacitación a docentes**
Se planea una sesión de capacitación para los docentes al momento de que se incorpore a la cátedra y para las pruebas del sistema. Esto a modo de que los profesores puedan conocer a fondo el sistema, los ejercicios, las instrucciones y todo lo necesario para poder guiar los contenidos en la cátedra en base a la plataforma, además tambien para capacitarlos a futuro cuando se pueda incorporar la personalización de ejercicios.
Los temas específicos serán:
- Navegación en PGA (login, registro, dashboard).
- Uso de tablero de progresos y reportes.
- Creación y gestión de sesiones de refuerzo.
Adicionalmente se contará con material de apoyo: un manual en PDF y video tutorial (ver apartado 3.5).

### 3.3 Proceso de Registro y Acceso
#### 3.3.1 Alumnos
**1. Opciones de registro**
El registro de alumnos estará habilitado desde el sistema (se pueden registrar solos) con dos opciones:
  - **Registro manual**
    - Los alumnos completarán los campos correspondientes y requeridos por el sistema, como nombre completo, avatar, correo electrónico, usuario y contraseña.
    - Al enviar el registro, se genera código de verificación que se envía al correo para validar email.
  - **Autenticación con Google (OAuth 2.0)**
    - Opción “Registrarse con Google”
    - Tras aceptar permisos (profile, email), se completa perfil con datos faltantes (avatar, usuario y contraseña).
**2. Flujo de unirse a un curso (PGA)**
  1. Crear cuenta / login (Google o formulario).
  2. Vista de “Cursos disponibles”:
    - El alumno verá lista de cursos creados por docentes (p. ej., “Algoritmos y Estruct. de Datos I – 2025”).
  3. Unirse a curso
    - Ingresar contraseña del curso proporcionada por el docente.
    - Al validarla, el alumno se asocia al curso y accede a las misiones disponibles.

**3. Validaciones extra**
  - Verificación de correo electrónico (si se registra por formulario).

#### 3.3.2 Docentes
**1. Registro del docente**
El registro de docentes NO ESTARÁ habilitado desde el sistema (NO se pueden registrar solos). El registro del docente se llevará a cabo mediante el administrador del sistema.
- Manual por Administrador
  - El docente completa un formulario con los datos necesarios: nombre completo, correo institucional, constancias y se las envía al Administrador.
  - El Administrador valida credenciales y crea el usuario y contraseña para el docente en el sistema.
  - El Administardor le provee al docente el usuario y una contraseña temporal al correo declarado.
- Primer login
  - Al hacer login con usuario/contraseña temporales, se fuerza cambio de contraseña por seguridad.

2. Acceso a funcionalidades de Gestión Docente
El sistema detecta rol “docente” tras el login y habilita todas las funcionalidades de la gestión docente. Desde allí, el docente podrá acceder a:
  1. Dashboard de progreso (visualiza estado del curso).
  2. Reportes semanales (ver sección 3.4).
  3. Sesiones de refuerzo (crear, ver estado, aprobar).
No se habilita registro de ejercicios ni gestión de banco de ejercicios (solo Administrador).

### 3.4 Flujos de Uso Diarios y Semanales
#### 3.4.1 Alumnos
- **Frecuencia de interacción**
  - **Objetivo mínimo**: 1 ingreso diario para practicar misiones.
  - **Durante días de práctica presencial**: 2 ingresos (una sesión en clase, otra en casa).
- **Plan de ejercicios diarios**
  - Se incentivará completar al menos 1 misión por día (o 3 misiones por semana) para mantener la curva de progreso.
- Notificaciones / Recordatorios
  - **In-app**:
    - Mensaje diario si no se ha completado misión en las últimas 24 horas:
    - “¡No te olvides de completar tus misiones! Completa una misión y gana XP para seguir aprendiendo.”
  - **Correo electrónico**:
    - Enviar recordatorio diario a las 20:00 h si el alumno no entró a PGA ese día.

#### 3.4.2 Docentes
- **Revisión del dashboard**
  - **Frecuencia recomendada**: cada día de clase (lunes y miércoles), 30 min antes de la sesión práctica.
  - **Reporte semanal automático**:
    - Se genera todos los domingos a las 20:00 h (cron job).
    - Envía PDF/CSV al correo del docente con:
      - Porcentaje de avance global del curso
      - Porcentaje de avance por tema
      - Estadísticas individuales de cada alumno (nivel, misiones completadas, estrellas, promedio intentos, última conexión).
- **Confirmación de sesiones de refuerzo**
  - **Automatizado**: el sistema sugiere sesión de refuerzo cada domingo a las 22:00 h.
  - El docente debe confirmar mínimamente; de lo contrario, se reagendará de forma automática para siguiente clase.
  - **Plazos**:
    - Como máximo hasta 2 horas antes del inicio de la sesión, alumnos y docentes deben confirmar asistencia.
    - Si no hay confirmación, se reprograma automáticamente.

### 3.5 Capacitación y Documentación Interna