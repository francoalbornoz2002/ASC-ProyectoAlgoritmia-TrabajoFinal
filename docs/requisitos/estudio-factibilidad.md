# Estudio de Factibilidad

**Versión:** 1.3
**Fecha:** 22/06/2025
**Autor(es):** Franco Andrés Albornoz

A continuación se presenta el análisis completo de factibilidad (técnica, económica y operativa) para el desarrollo de la Plataforma Gamificada “Algoritmia” (PGA).

---

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
  - Tableta gráfica Xp-Pen Deco Mini 7 (para pixel art y diseño)

#### 1.1.2 Equipamiento de respaldo
**No se dispone de PC secundaria**, pero el proyecto se almacena en repositorio GitHub y en Google Drive como respaldo continuo. En caso de falla, se puede conseguir un equipo de reemplazo estimado en aproximadamente 1 semana.

#### 1.1.3 Licencias de Sistemas Operativos
- **Windows 11 Home**: activado de fábrica.
- **Linux Mint 22**: instalación de dual‐boot, distribución libre y actualizada.

La PC cumple con los requisitos básicos para ejecutar IDEs (VS Code y Phaser Launcher), entornos locales (Node.js, SQLite) y herramientas de diseño (Aseprite). El respaldo está resuelto a través de backups en la nube.

### 1.2 Sistema Operativo y Software de Desarrollo

#### 1.2.1 Componentes y tecnologías principales
De manera general, estas serán las tecnologías definidas para cada parte del sistema:

| Parte del sistema  | Tecnologías                                                        | Justificación                                                                                                                                                                                |
| ------------------ | ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Videojuego**     | Godot Engine (GDScript)                                            | Motor open-source, liviano, multiplataforma y especializado en videojuegos 2D. Permite empaquetar el juego completo y trabajar offline. GDScript es fácil de aprender y altamente expresivo. |
| **Plataforma web** | Frontend: SvelteKit + Tailwind                                     | SvelteKit ofrece alta velocidad, reactividad y bajo consumo. Tailwind permite una UI moderna con poco código CSS.                                                                            |
|                    | Backend: Node.js + NestJS + TypeScript                             | NestJS ofrece modularidad, capas limpias, control de dependencias y estructura clara para escalabilidad. TypeScript reduce errores y provee tipado fuerte.                                   |
| **Base de datos**  | SQLite (para desarrollo y videojuego) / PostgreSQL (entrega final) | SQLite permite pruebas rápidas y locales. PostgreSQL se usará para producción por su robustez y soporte de concurrencia.                                                                     |

**Infraestructura y conectividad**
El videojuego utilizará una base de datos local embebida (formato JSON o SQLite) para guardar el progreso del estudiante sin necesidad de conexión inmediata. Cuando haya conectividad, el videojuego se conectará a la API del backend y realizará una sincronización de datos, actualizando el progreso en la base central.

#### 1.2.1 Sistemas Operativos de trabajo
- **Desarrollo principal**: Se podrán utilizar tanto Windows como Linux como sistemas operativos de desarrollo del sistema, debido a que los dos poseen compatibilidad con herramientas clave para el desarrollo del sistema como Godot Engine, Aseprite y Frame0.

#### 1.2.2 Software instalado y versiones
**Git**
- Versión: git 2.43.0 (disponible en ambos SO).
- Configuración: usuario y correo set en ~/.gitconfig.

**Aseprite**
- Versión: 1.3.3 (instalado en Windows).
- Uso: diseño y edición de sprites Pixel Art.

**Frame0**
- Versión: 1.0 (instalada en Windows y Linux).
- Uso: prototipado rápido de interfaces.

**Godot Engine (Motor de Videojuegos)**
- Versión: 4.4.1 (instalado en Windows y Linux)

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
- Se instalará Jest para back-end en Node.js/NestJS.
- Se instalará Vitest para pruebas de unidades en SvelteKit.
- Se instalará GUT (Godot Unit Testing) para pruebas unitarias en Godot 4.

### 1.3 Stack de Desarrollo y Curva de Aprendizaje
#### 1.3.1 Web Front-end
**Frameworks y librerías**
- SvelteKit 2
- Tailwind CSS (v4.0) para estilos utilitarios.

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

#### 1.3.2 Web Back End
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

#### 1.3.3 Godot Engine
**Nivel de experiencia actual**
- Sin experiencia previa en Godot Engine 4.

**Recursos de capacitación**
- Cursos varios en Youtube, existe gran variedad.
- Documentación oficial: https://docs.godotengine.org/en/stable/index.html
- Ejemplos de proyectos varios

#### 1.3.3 Base de Datos
**Elección inicial**:
- SQLite como base de datos local para desarrollo rápido y pruebas sin requerir servidor adicional. También elegida para ser la base de datos local embebida para el videojuego.

**Migración futura**:
- PostgreSQL para consultas avanzadas, demostración y defensa y despliegue (DBMS completo) para la plataforma web. La base de datos del videojuego se mantendrá actualizada constantemente.

**Nivel de conocimiento actual**:
- Conocimiento en modelos relacionales con normalización (3ra forma).
- Conocimientos en base de datos activas (vistas, funciones, triggers)

**Recursos de capacitación**:
- Tutorial SQLite (Página oficial sqlite.org).
- "Curso de Base de Datos PostgreSQL” en YouTube (Vito Dev).
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
| Semana          | Tecnología                                 |
| --------------- | ------------------------------------------ |
| 23 Jun - 29 Jun | HTML - CSS - JavaScript                    |
| 30 Jun - 06 Jul | HTML - CSS - JavaScript                    |
| 07 Jul - 13 Jul | Svelte - Tailwind                          |
| 14 Jul - 20 Jul | Svelte - Tailwind                          |
| 21 Jul - 27 Jul | Godot 4 - GDScript / SQLite                |
| 28 Jul - 03 Ago | Godot 4 - GDScript / SQLite                |
| 04 Ago - 10 Ago | Godot 4 - GDScript / SQLite                |
| 04 Ago - 10 Ago | Godot 4 - GDScript / SQLite                |
| 18 Ago - 24 Ago | Node.js - NestJs / TypeScript              |
| 25 Ago - 31 Ago | Node.js - NestJs / TypeScript / PostgreSQL |
| 01 Sep - 07 Sep | Node.js - NestJs / TypeScript / PostgreSQL |

Con un cronograma de 10 semanas y recursos gratuitos, la curva de aprendizaje es asumible. En caso de mayor dificultad, se tomarán horas extra y se consultará con docentes o compañeros familiarizados con el stack.

### 1.4 Infraestructura para Desarrollo Local
#### 1.4.1 Máquina de Desarrollo
No se planea utilizar Docker o Kubernetes inicialmente, debido a falta de experiencia y al desarrollo local con SQLite y entornos Node.js integrados. Si surgiera la necesidad en despliegues futuros, se evaluará agregar Docker para contenerización.

#### 1.4.2 IDE y herramientas
**IDEs**
- Visual Studio Code en Linux Mint 22 y Windows 11.
- Godot Engine 4 en Linux Mint 22 y Windows 11.

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

#### 1.5.3 Recursos Pixel Art gratuitos
Se planea que para los tilesets y assets del videojuego, se utilicen recursos gratuitos de libre uso. La mayoría de estos packs de assets se encuentran en Itch.io (sección “Assets”, licencias CC0 o CC-BY).
Igualmente, si surge la necesidad como no encontrar un pack de assets integrado o el pack elegido cambie repentinamente la licencia, se evaluarán packs premium de Itch.io (costo variable) o crear assets propios en Aseprite.

### 1.6 Restricciones Técnicas

**1. Versión mínima de Node.js**  
Se empleará Node.js ≥ v18.x, idealmente v22.16.0 LTS. Esta versión asegura compatibilidad con NestJS v11 y dependencias modernas del backend.

**2. Versión mínima de npm**  
Se utilizará npm 10.x, incluido con Node.js v22.16.0 LTS, para gestionar paquetes de manera segura y actualizada.

**3. Requerimientos de navegador (plataforma web)**  
- Navegadores recomendados: Chrome, Firefox, Edge, Safari (últimas versiones).
- Requiere soporte para JavaScript moderno (ES2022), WebAssembly, y CSS moderno para compatibilidad total con SvelteKit + Tailwind.

**4. Requisitos gráficos y de rendimiento para el videojuego (Godot 4)**  
- Godot 4 configurado para 60 FPS, resolución base 800×600 (adaptable a pantalla completa o escalado dinámico).
- El motor utiliza renderizado 2D mediante Vulkan (por defecto) o compatibilidad con OpenGL para hardware más limitado.
- Meta de rendimiento: ≥ 30 FPS en equipos modestos (Intel UHD Graphics + 4 GB RAM).
- En pruebas con netbooks del estado argentino (Intel N4000–N5000), se prevé fluidez aceptable ajustando la calidad (desactivando sombras y efectos no críticos).

**5. Compatibilidad mínima garantizada**
- **Sistemas operativos**:
  - Windows 10 o superior.
  - Distribuciones Linux con kernel ≥ 5.4 (probado en Linux Mint 22).
- **Hardware mínimo para el juego**:
  - Procesador Dual-Core.
  - 4 GB RAM.
  - GPU integrada con soporte para OpenGL 3.3 o superior.

> **Nota:** El juego estará optimizado para funcionar en entornos educativos con recursos limitados, garantizando acceso inclusivo en laboratorios o dispositivos de gama baja.


### 1.7 Conclusión de Factibilidad Técnica

**Infraestructura actual suficiente**  
La PC disponible (Intel i5, 8 GB RAM, SSD) resulta suficiente para ejecutar entornos de desarrollo modernos como Godot 4, SvelteKit, NestJS y herramientas gráficas como Aseprite. No se requiere equipamiento adicional para completar el proyecto, y en caso de fallas, se dispone de respaldo en la nube (GitHub, Google Drive) que permite continuidad operativa.

**Herramientas y lenguajes adecuados al proyecto**  
Se eligieron tecnologías modernas, escalables y con gran comunidad. Godot 4 permite una experiencia de juego fluida y offline, mientras que el stack SvelteKit + NestJS ofrece modularidad y control total en la parte administrativa. La separación entre el videojuego (alumnos) y la web (docentes/administradores) mejora la organización del código, el mantenimiento y la experiencia de usuario.

**Riesgos técnicos actuales**  
- La principal dificultad es la curva de aprendizaje de Godot, NestJS y SvelteKit, estimada en ~10 semanas con práctica regular.
- La sincronización entre el videojuego y la base de datos compartida requiere diseño cuidadoso de API REST y seguridad en la autenticación.
- La autenticación OAuth con Google debe implementarse de forma consistente entre ambas aplicaciones.
- No hay experiencia previa en testing automatizado con GUT (Godot) o Jest/Vitest.

**Medidas mitigadoras**  
- Capacitación intensiva con documentación oficial y tutoriales en YouTube (MiduDev, Fazt Code, documentación de Godot/NestJS/Svelte).
- Implementación temprana de un prototipo de sincronización para validar la arquitectura de comunicación.
- Consultas periódicas con docentes o referentes técnicos para corregir desvíos en tiempo real.
- Uso de extensiones de VS Code y herramientas de testing para adquirir buenas prácticas desde el comienzo.

**Conclusión general**  
El proyecto es técnica y operativamente viable. La separación de responsabilidades entre las dos aplicaciones garantiza escalabilidad, portabilidad y resiliencia. Se identificaron los principales desafíos, pero se cuenta con un plan realista de formación y mitigación. Las herramientas, el hardware disponible y el diseño técnico del sistema permiten avanzar con confianza en el desarrollo del proyecto.

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

### 3.1 Perfil y Volumen de Usuarios inicial
Durante el primer año, se estiman los siguientes volúmenes:

- **Alumnos**: 100–150 ingresantes a Algoritmos y Estructuras de Datos I.
- **Docentes**: 5 integrantes del equipo de cátedra encargados de evaluar avances y revisar el progreso de los alumnos.
- **Administrador**: 1 perfil centralizado que gestionará los roles, instituciones, cursos y la asignación de docentes.

A futuro, la arquitectura de PGA contempla la creación de administradores institucionales adicionales por cada 10–15 nuevas facultades que adopten el sistema, garantizando así un esquema de escalabilidad operativa sin recargar a un único responsable.

### 3.2 Adaptación a la Dinámica de la Cátedra
**1. Integración de PGA en la rutina de la cátedra**

Se propone que PGA sustituya gradualmente a Visual DaVinci, ya que está pensada y orientada para darle uso como herramienta principal para guiar las prácticas de la materia. Esto involucrará que se tenga que actualizar el programa de la materia (con previa aprobación de directivos) para incorporar PGA desde el inicio del cuatrimestre.

**Incorporación de PGA**
- Semana 1 de cursado: Taller introductorio obligatorio (1 hora práctica) donde se explique la plataforma a todos los alumnos ingresantes y avanzados.
- A partir de la Semana 2, cada clase práctica de Algoritmos y Estructuras de Datos I se realice íntegramente dentro de PGA.

**Ejemplos de flujo**:
  - El docente asigna “Misión 1, 2 y 3” para la siguiente clase de práctica.
  - Los alumnos deben resolverla en PGA antes de la clase presencial.
  - Los docentes analizan el avance en el tablero antes de la siguiente clase y adaptan contenidos según conveniencia.

**2. Coexistencia con teoría, práctica y consulta**
  - PGA estará disponible 24/7
  - Teoría (lunes 10:00–12:00):
    - Se mostrará el concepto teórico en clase mediante presentaciones en diapositivas; PGA se mencionará como complemento para practicar. Dicho tema teórico tendrá que tener la sintaxis y semántica definida por PGA.
  - Práctica (lunes 17:00–19:00, miércoles 10:30–12:30):
    - Los alumnos usarán PGA en clase para resolver ejercicios mientras el docente supervisa y responde consultas, dudas o repasa algunos temas teóricos.
  - Consulta (jueves 19:00–20:00):
    - Los alumnos pueden traer dudas sobre ejercicios de PGA; el docente empleará PGA para replicar y explicar cada caso.
  - Tareas fuera de horario:
    - Los docentes podrán asignar ejercicios PGA como tarea para la próxima sesión de práctica o consulta.
    - Se fomentará que los alumnos entren al menos 1 vez al día para avanzar en niveles y desbloquear misiones.

### 3.3 Aceptación por Parte de Alumnos y Docentes
**1. Alumnos**
  - **Encuesta previa**: Se han encuestado en total a 26 alumnos ingresantes y 7 alumnos avanzados (más de un año en la carrera). 
    - 80.7 % de ingresantes opina que gamificación aumentaría “bastante” o “mucho” su compromiso.
    - 84.6 % valora como “Muy importante” recibir sugerencias automáticas de optimización.
    - Los ingresantes indican que las características que hubieran querido tener son: interfaz intuitiva, agradable a la vista, ayuda y especificación de errores y sintaxis intuitiva.
    - En cuanto a las tres mejoras prioritarias que desearían tener: sintaxis sencilla, indicador de errores de sintaxis, interfaz sencilla, atractiva y agradable, sugerencias automáticas para optimización.
    - **Resumen**: Claramente existe una demanda significativa de los alumnos por una plataforma más atractiva y con feedback formativo.
  - **Grupo mínimo viable para pilotar PGA**:
    - Tomar al menos 20 usuarios (entre ingresantes, avanzados y 1–2 docentes) para una prueba inicial.
    - Se propone: 15 ingresantes del año 2025 + 3 avanzados + 2 docentes para recibir feedback exhaustivo.

**2. Docentes**
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

### 3.4 Proceso de Registro y Acceso
#### 3.4.1 Alumnos
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
  2. Vista de “Cursos":
    - El alumno verá inicialmente la lista de cursos vacía y deberá unirse a un curso colocando la contraseña.
  3. Unirse a curso
    - Ingresar contraseña del curso proporcionada por el docente.
    - Al validarla, el alumno se asocia al curso y accede a las misiones disponibles.

**3. Validaciones extra**
  - Verificación de correo electrónico (si se registra por formulario).

#### 3.4.2 Docentes
**1. Registro del docente**
El registro de docentes NO ESTARÁ habilitado desde el sistema (NO se pueden registrar solos). El registro del docente se llevará a cabo mediante el administrador del sistema.
- Manual por Administrador
  - El docente completa un formulario con los datos necesarios: nombre completo, correo institucional, constancias y se las envía al Administrador.
  - El Administrador valida credenciales y crea el usuario y contraseña para el docente en el sistema.
  - El Administardor le provee al docente el usuario y una contraseña temporal al correo declarado.
- Primer login
  - Al hacer login con usuario/contraseña temporales, se fuerza cambio de contraseña por seguridad.

**2. Acceso a funcionalidades de Gestión Docente**
El sistema detecta rol “docente” tras el login y habilita todas las funcionalidades de la gestión docente. Desde allí, el docente podrá acceder a:
  1. Dashboard de progreso (visualiza estado del curso).
  2. Reportes semanales (ver sección 3.4).
  3. Sesiones de refuerzo (crear, ver estado, aprobar).
No se habilita registro de ejercicios ni gestión de banco de ejercicios (solo Administrador).

### 3.5 Flujos de Uso Diarios y Semanales
#### 3.5.1 Alumnos
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

#### 3.5.2 Docentes
- **Revisión del dashboard**
  - **Frecuencia recomendada**: cada día de clase (lunes y miércoles), 30 min antes de la sesión práctica.
  - **Reporte semanal automático**:
    - Se genera todos los domingos a las 20:00 h (cron job).
    - Envía PDF/CSV al correo del docente con:
      - Porcentaje de avance global del curso
      - Porcentaje de avance por capítulo (tema)
      - Estadísticas individuales de cada alumno (nivel, misiones completadas, estrellas, promedio intentos, última conexión).
- **Confirmación de sesiones de refuerzo**
  - **Automatizado**: el sistema sugiere sesión de refuerzo cada domingo a las 22:00 h.
  - El docente debe confirmar mínimamente; de lo contrario, se reagendará de forma automática para siguiente clase.
  - **Plazos**:
    - Como máximo hasta 2 horas antes del inicio de la sesión, alumnos y docentes deben confirmar asistencia.
    - Si no hay confirmación, se reprograma automáticamente.

### 3.6 Capacitación y Documentación Interna
#### 3.6.1 Manuales y tutoriales para alumnos
**Manual en PDF**
**1. Creación de cuenta**: pasos ilustrados (pantallazos) para registro con formulario y con Google.
**2. Unirse a un curso**: pasos de como unirse a un curso colocando la contraseña proporcionada por el docente
**3. Resolución de la primera misión**:
  - Cómo acceder al editor de código en PGA.
  - Explicación del “Libro de Héroe” (sintaxis de primitivas, estructuras, variables).
  - Ejecución en el visor animado.
**4. Interpretación del feedback formativo**
  - Explicación de error de sintaxis, advertencias de variables no usadas, sugerencias de optimización.
  - Sistema de estrellas (1–3) y puntos de experiencia (XP).
**5. Progreso en niveles y desbloqueo de misiones**
  - Mapa de misiones desbloqueables: imágenes de cada etapa temática.
  - Cómo ver historial de misiones completadas y XP acumulado.

**Video tutorial (YouTube – Unlisted)**
1. “Introducción a PGA: primer login y perfil de alumno” (3 min)
2. “Resolviendo tu primera misión: editor, visor y feedback” (5 min)
3. “Cómo interpretar estrellas y EXP” (2 min)

**Acceso**
  - Enlazado desde el PDF de manual.
  - Disponible en repositorio GitHub en carpeta /docs/tutoriales/.

#### 3.6.2 Documentación para docentes
**Manual en PDF**
**1. Cómo revisar el dashboard y estadísticas**
  - El docente podrá revisar los avances de los distintos cursos que tenga asignado, seleccionará el curso deseado y accederá a las métricas de los alumnos de ese curso.

**2. Cómo programar sesiones de refuerzo**
  - Pasos para crear una sesión de refuerzo desde cero.
  - Pasos para confirmar o reagendar sesión sugerida por el sistema.
  - Plazos para confirmaciones (ver sección 3.4.2).

**3. Cómo interpretar el reporte semanal automático**
  - Estructura del PDF/CSV:
    - Tabla con estadística general del curso.
    - Lista de alumnos en estado crítico (rojo) y atrasados (amarillo).
    - Instrucciones para ordenar y filtrar.

**4. Configuración de cursos y contraseñas**
  - Cambiar contraseña de curso existente.

**Video tutorial (YouTube – Unlisted)**
1. “Dashboard de avance: métricas grupales e individuales, reportes y filtros” (6 min)
2. “Cómo programar tu primera sesión de refuerzo” (3 min)
3. “Interpretando correos automáticos y notificaciones” (3 min)

#### 3.6.3 Documentación para el administrador
**Manual en PDF**
**1. Gestión académica**: instituciones, cursos y docentes.
  - Pasos para dar de alta y baja una institución
  - Pasos para creación de curso y asociación con la institución
**2. Configuración de roles y permisos**.
  - Creación de cuenta del docente y asignación a un curso
  - Gestión de usuarios en general
**3. Monitoreo de logs y métricas de uso.**
  - Los diferentes apartados del sistema que se pueden auditar
  - Filtros y ordenamientos


### 3.7 Limitaciones Operativas
**1. Restricciones en salón de clases / laboratorios de la Facultad**
- La red institucional suele funcionar con suficiente ancho de banda; ocasionales bajones (lentitud) no impiden uso básico de PGA.
- Equipos de laboratorio actualizados (navegadores modernos y suficiente RAM).

**2. Dispositivos de alumnos y docentes**
- La mayoría tiene laptops o desktops con navegadores (Chrome/Firefox) actualizados.
- Se disponen de equipos con navegadores modernos (Chrome/Firefox) en el laboratorio.
- Se recomienda Chrome v90+ o Firefox v88+ para mejor rendimiento de Canvas/WebGL (Phaser).
- Para alumnos con hardware muy antiguo (netbooks con 4 GB y CPU modesto), PGA corre a 30 FPS.

**3. Uso de LAN sin internet**
- No implementado. PGA requiere conexión para autenticación OAuth y carga de assets en tiempo real (CDN).
- Posible mejora a futuro: precargar assets en caché y modo offline limitado (service workers), pero no aplica en esta versión.

**4. Políticas de la Facultad**
- La facultad permite ejecutar aplicaciones web en navegadores.
- No hay limitaciones estrictas para acceder a un dominio público o web.
- No se necesita instalar software local (solo un navegador).

**5. Horario de mantenimiento de red**
- No se conoce un plan oficial de mantenimiento que interrumpa internet de manera programada.
- En caso de caídas del servicio, se dispondrá de archivos PDF con ejercicios impresos como plan B (si falla la plataforma).

### 3.8 Factores de Riesgo Operativo
**1. Baja adopción**
**Escenario**: Menos del 50 % de alumnos registrados usa PGA en primer mes.
**Plan de mitigación**:
- Realizar sesiones obligatorias de práctica con PGA en laboratorio (el docente lo incluye como parte de la calificación).
- Ofrecer recompensas de XP adicionales a los cursos (bonificación en nota de prácticas).- Recoger feedback constante y ajustar UX/UI para facilitar la curva de entrada.

**2. Resistencia al cambio**
**Escenario**: Un profesor decide no usar reportes ni sesiones de refuerzo.
**Mitigación**:
- Reuniones breves con el docente para exponer beneficios de PGA (mejora de retención, ahorro de tiempo).
- Mostrar estadísticas tempranas (primeras semanas) que demuestran impacto en dedicación y avances de alumnos.
- Incorporar PGA de forma gradual: obligar uso en prácticas, pero dejar libre uso de reportes; demostrar resultados a mediano plazo.

**3. Falla de notificaciones (SMTP)**
**Escenario**: Correos de alerta semanal o recordatorios diarios no se envían (problemas con servicio SMTP).
**Detección y solución rápida**:
- Logging en servidor: Registrar cada intento de envío de email con estado (éxito/fallo) en una tabla de log de eventos.
- Alerta interna: Si falla el envío de correo 3 veces consecutivas, generar notificación “en-app” visible para el docente: “Error al enviar correo. Revise configuración SMTP.”

**4. Saturación de carga**
**Escenario**: Muchos alumnos (p. ej. 100 usuarios) ejecutan misiones simultáneamente antes de un examen.
**Mitigación**:
- Optimizar endpoints: Limitar concurrencia de llamadas con colas (p. ej. BullMQ) para suavizar picos.
- Cache de resultados frecuentes (casos de prueba estándar) para evitar recomputar lógicas idénticas.
- Escalabilidad horizontal futura: desplegar back-end en plataforma Cloud (Heroku, Render) con escalado automático si se detecta alta demanda.
- Pruebas de carga previa: usar herramientas como k6 o Artillery para simular concurrencia y ajustar límites.


### 3.9 Conclusión de Factibilidad Operativa
Operativamente, PGA se integra con la dinámica de la cátedra sin mayores fricciones. La existencia de un docente promotor, manuales claros y planes de contingencia garantizan su éxito en uso diario y semanal.

**1. Integración sin interferencias**
  - PGA encaja en el calendario de la cátedra sin solaparse; se usará en prácticas y fuera de horario sin perturbar teoría o consulta.
  - No requiere instalaciones en equipo (solo navegador).

**2. Apoyo de docentes promotores**
  - Lic. Mario Vialey (Profesor Adjunto) actúa como promotor, validando la idea y dispuesto a incorporarla.
  - Se cuenta con la predisposición de la cátedra para hacer la prueba de concepto con alumnos y docentes.

**3. Procedimientos para incidencias**
  - Se definirá canal de soporte en Discord (grupo cerrado) y correo de contacto: soporte@pga.fceqyn.edu.ar.
  - En caso de fallas técnicas, los alumnos podrán documentar errores en GitHub Issues (repositorio PGA) con etiquetas /bug o /issue.

**4. Adopción esperada**
  - Con manuales sencillos y talleres iniciales, la adopción se prevé rápida (≥ 80 % en primer mes).
  - Incentivar participación con bonus de XP y prácticas obligatorias en clase.