# Capítulo VII: Product Implementation, Validation & Deployment

## 7.1. Software Configuration Management.

<!-- Descripcion general del punto:
En esta sección el equipo establece las decisiones y convenciones que permitirán mantener la consistencia durante el ciclo de vida. Se incluyen secciones internas para:
Source Code Management, Development Environment Configuration y Deployment Configuration
-->

### 7.1.1. Software Development Environment Configuration.

- **Project Management**:  
  Para la gestión del proyecto se utilizará [Nombre de la herramienta] ya que [breve justificación de 1-2 razones principales]. Esta herramienta nos permite [principal beneficio para el equipo].  
  **Enlace:** [URL de la herramienta]

- **Requirements Management**  
  Para la gestión de requerimientos hemos seleccionado [Nombre de la herramienta] debido a [breve justificación]. Esta herramienta es fundamental para nuestro equipo ya que [principal beneficio].  
  **Enlace:** [URL de la herramienta]

- **Product UX/UI Design**  
  Para el diseño UX/UI de nuestro producto utilizaremos [Nombre de la herramienta] porque [breve justificación]. Esta herramienta nos proporciona [principales beneficios].  
  **Enlace:** [URL de la herramienta]

- **Software Development**  
  Para el desarrollo de software, utilizaremos las siguientes herramientas:  
  Para [componente específico] utilizaremos **[Nombre del IDE/herramienta]** ya que [breve justificación]. [Principal beneficio].  
  **Enlace**: [URL de la herramienta]

Para [otro componente] usaremos **[Nombre del IDE/herramienta]** debido a [breve justificación]. [Principal beneficio].  
**Enlace**: [URL de la herramienta]

- **Software Testing**  
  Para testing, implementaremos las siguientes herramientas:  
  Para [componente específico], utilizaremos **[Nombre de la herramienta]**, ya que [breve justificación].  
  **Enlace**: [URL de la herramienta]

Para [otro componente] emplearemos **[Nombre de la herramienta]** porque [breve justificación].  
**Enlace**: [URL de la herramienta]

- **Software Deployment**  
  Para el despliegue de nuestras soluciones utilizaremos:  
  **[Nombre de la herramienta]** para [componente específico] porque [breve justificación].  
  **Enlace**: [URL de la herramienta]

**[Nombre de la herramienta]** para [otro componente] ya que [breve justificación].  
**Enlace**: [URL de la herramienta]

- **Software Documentation**  
  La documentación del software será realizada en **[Nombre de la herramienta]** mediante [método específico], elegimos esta herramienta porque [breve justificación].  
  **Enlace:** [URL de la herramienta]

### 7.1.2. Source Code Management.

<!--
En esta sección el equipo establece los medios y esquema de organización que aplicará para el seguimiento de modificaciones. Para ello utilizará GitHub como
plataforma y sistema de control de versiones. Debe incluirse el URL del repositorio de GitHub para cada producto digital que forma parte del alcance. Tomar en cuenta
que en el caso de Web Services, se incluye en el repositorio el proyecto y los archivos de pruebas (en este caso los archivos .feature).
En esta sección debe también explicarse de qué forma implementará GitFlow (Ver artículo “A successful Git branching model” de Vincent Driessen en la sección de
Referencias) como Workflow de control de versiones, es decir qué branches (ramas) creará además de main branch (rama principal), por ejemplo, develop branch. Para
GitFlow cada Feature requiere su propio branch, por ello debe especificar qué convenciones se aplicará para nombrar los feature branches. Igualmente debe incluir
las convenciones para Release branches y Hotfix branches. Aplique semantic versioning para nombrar sus Releases (Vea “Semantic Versioning 2.0.0” en la sección
de Referencias).
-->

**Repositorios**
Se creó una organización llamada ImagIA-2024-02 en Github, en la cual el equipo cuenta con los repositorios donde se trabajarán las soluciones propuestas.
Enlace de la organización: [https://github.com/ImagIA-2024-02/](https://github.com/ImagIA-2024-02/)

| **Solución**           | **Nombre del repositorio** | **Enlace**                              |
| ---------------------- | -------------------------- | --------------------------------------- |
| Landing Page           | art-vision-landing         | https://github.com/ImagIA-2024-02/<TDB> |
| Web Services (Backend) | art-vision-backend         | https://github.com/ImagIA-2024-02/<TDB> |
| Mobile Application     | art-vision-mobile          | https://github.com/ImagIA-2024-02/<TDB> |
| AI Models              | art-vision-ml-models       | https://github.com/ImagIA-2024-02/<TDB> |

**Gitflow**

Para la implementación del flujo de trabajo Gitflow, usando la herramienta de control de versiones Git, se usó de referencia la entrada de blog "A successful Git branching model" de Vincent Driessen, que nos ayudó a detallar las siguientes convenciones que se usarán en el proyecto:

**Main branch**  
La Main branch es la principal rama de desarrollo del proyecto. En esta rama se encontrará el código que se encuentra actualmente en producción.  
Notación: main

**Develop branch**  
La Develop branch será la rama que contendrá las últimas actualizaciones y cambios agregados que se entregarán en la siguiente versión del proyecto.  
Notación: develop  
Creación: git checkout -b develop main

**Feature branches**  
Las Feature branches se usarán para desarrollar nuevas características del producto que se agregarán en versiones futuras. Estas funcionalidades se deberán reunir o juntar eventualmente a la rama Develop.

Debe derivarse de la rama Develop.  
Debe fusionarse de vuelta a la rama Develop.  
Notación: feature/[name of feature]  
Creación: git checkout -b feature/[name of feature] develop

**Conventional Commits**  
Para la redacción de las siguientes convenciones de commits se utilizó de referencia el artículo Conventional Commits 1.0.0.

Types:

- add: se usará para indicar que se añadieron archivos o carpetas.
- fix: este tipo de commit se utilizará para la confirmación de una corrección de un error en el código.
- feat: este tipo de commit se utilizará para la confirmación de que se ha añadido una nueva funcionalidad.
- test: se usará para indicar que se añadieron archivos de test.
- docs: se usará para indicar que se añadieron actualizaciones a la documentación.
- BREAKING CHANGE: este tipo de commit se utilizará para confirmar la introducción de un cambio importante en el código.

### 7.1.3. Source Code Style Guide & Conventions.

<!-- RESUMEN DEL PUNTO:
Aquí el equipo resume e indica las referencias que adoptará para nombrar elementos y programar en los lenguajes que se utilizan en la solución (como por
ejemplo C#, Java, TypeScript, Kotlin, Swift, u otros según los constraints del proyecto; así como Gherkin para los archivos .feature). Para todos los lenguajes debe aplicar la
nomenclatura en inglés. Adicionalmente, adopte convenciones estándares para coding (Vea por ejemplo “Gherkin Conventions for Readable Specifications”, “Google
TypeScript Style Guide” en la sección de Referencias).
-->

<!--
__ATENCION___
__TEMPLATE COPIADO DE OTRO PROYECTO, CAMBIAR/AJUSTAR/MEJORAR__
-->

**Guía de Estilo y convenciones de codificación HTML**  
Para las convenciones de codificación HTML, adoptaremos las pautas delineadas en las referencias "Guía de Estilo y Convenciones de Codificación HTML" y "Guía de Estilo HTML/CSS de Google". Aquí algunos puntos clave:

**Convenciones de Nomenclatura:**

- Aplicar nomenclatura en inglés
- Utilizar letras minúsculas para todos los nombres de elementos HTML
- Separar palabras en nombres de ID y clases con guiones (-)
- Utilizar nombres significativos y descriptivos para IDs y clases

**Formato:**

- Sangrar elementos anidados para mejorar la legibilidad
- Utilizar comillas dobles para los valores de atributos
- Emplear etiquetas auto-cerradas para elementos

**Comentarios:**

- Agregar comentarios para explicar secciones complejas o proporcionar contexto a futuros desarrolladores
- Utilizar la sintaxis de comentarios HTML

**Guía de Estilo y convenciones de codificación CSS**  
Para las convenciones de codificación CSS, seguiremos las pautas proporcionadas en la referencia "Google HTML/CSS Style Guide". Aquí tienes algunos puntos clave:

**Convenciones de nomenclatura:**

- Aplicar nomenclatura en inglés
- Usar letras minúsculas para todos los selectores CSS y nombres de propiedades
- Separar palabras en nombres de clases con guiones (-)
- Utilizar nombres significativos y descriptivos para las clases

**Formato:**

- Indentar estilos anidados para mejorar la legibilidad
- Utilizar un estilo de indentación consistente, como dos espacios
- Usar propiedades abreviadas cuando sea posible para mantener el código conciso

**Comentarios:**

- Agregar comentarios para explicar estilos complejos o proporcionar contexto para futuros desarrolladores
- Utilizar la sintaxis de comentarios CSS /\* \*/

**Guía de Estilo y convenciones de codificación JavaScript/TypeScript**  
Para las convenciones de codificación JavaScript/TypeScript, adoptaremos las pautas proporcionadas en las referencias "Google JavaScript Style Guide" y "Google TypeScript Style Guide". Aquí tienes algunos puntos clave:

**Convenciones de nomenclatura:**

- Aplicar nomenclatura en inglés
- Utilizar camelCase para nombres de variables y funciones
- Utilizar PascalCase para nombres de clases
- Utilizar letras mayúsculas para constantes

**Formato:**

- Utilizar un estilo de indentación consistente, como dos o cuatro espacios
- Utilizar punto y coma al final de las sentencias
- Evitar el uso de variables globales siempre que sea posible

**Comentarios:**

- Agregar comentarios para explicar lógica compleja o proporcionar contexto para futuros desarrolladores
- Utilizar la sintaxis de comentarios JavaScript/TypeScript // para comentarios de una sola línea y /\* \*/ para comentarios de varias líneas

**Guía de Estilo y convenciones de codificación Java**  
Para las convenciones de codificación Java, nos adheriremos a las pautas descritas en la referencia "Google Java Style Guide". Aquí tienes algunos puntos clave:

**Convenciones de nomenclatura:**

- Aplicar nomenclatura en inglés
- Utilizar camelCase para nombres de variables y métodos
- Utilizar PascalCase para nombres de clases
- Utilizar letras mayúsculas para constantes

**Formato:**

- Utilizar un estilo de indentación consistente, como cuatro espacios
- Colocar las llaves de apertura en la misma línea que la declaración
- Utilizar nombres significativos para variables y métodos para mayor claridad

**Comentarios:**

- Agregar comentarios para explicar algoritmos complejos o proporcionar contexto para futuros desarrolladores
- Utilizar la sintaxis de comentarios Java // para comentarios de una sola línea y /\* \*/ para comentarios de varias líneas

### 7.1.4. Software Deployment Configuration.

<!--
En esta sección el equipo especifica la configuración del despliegue de la solución, incluyendo los pasos necesarios para que, a partir de los repositorios de código
fuente, se pueda lograr el despliegue o publicación satisfactorio de cada uno de los productos digitales en la solución. Adicionalmente a la explicación,
el equipo incluye aquí el Deployment Diagram de C4 Model.
-->

**Despliegue de la landing page en GitHub Pages**

<!--
Imagen despues de cada paso y añadir el enlace
-->

Ir a la configuración del repositorio
Seleccionar la opción "Pages"
Elegir la rama que se desea desplegar y dar click en "Save"
Se mostrará el enlace de la página en la parte superior

## 7.2. Solution Implementation.

### 7.2.1. Sprint 1

#### 7.2.1.1. Sprint Planning 1.

<table border="2">
    <tr>
        <td>
           <p style = "font-weight: bold"><b>Sprint #</b></p>
        </td>
        <td>
          <p style = "font-weight: bold">Sprint 1</p>
        </td>
    </tr>
    <tr>
        <td colspan="2">
           <p><b>Sprint Planning Background</b></p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Date</p>
        </td>
        <td>
          <p>[DD-MM-YYYY]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Time</p>
        </td>
        <td>
          <p>[HH:MM]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Location</p>
        </td>
        <td>
          <p>[Virtual/Physical location]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Prepared By</p>
        </td>
        <td>
          <p>[Team Member Name]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Attendees</p>
        </td>
        <td>
          <p>[List of team member names]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 0 Review Summary</p>
        </td>
        <td>
          <p>[Summary of previous sprint review]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 0 Retrospective Summary</p>
        </td>
        <td>
          <p>[Summary of previous sprint retrospective]</p>
        </td>
    </tr>
    <tr>
        <td colspan="2">
           <p><b>Sprint Goal & User Stories</b></p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 1 Goal</p>
        </td>
        <td>
          <p>[Define sprint goal]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 1 Velocity</p>
        </td>
        <td>
          <p>[Number]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sum of Story Points</p>
        </td>
        <td>
          <p>[Number]</p>
        </td>
    </tr>
</table>

#### 7.2.1.2. Sprint Backlog 1.

[Descripción del objetivo principal del Sprint 1]

A continuación, se presenta un screenshot del sprint 1 en desarrollo realizado en Jira por
el equipo:

<div align="center">
  <img src="[ruta-imagen-jira]" alt="Jira Sprint 1 Screenshot">
</div>

Asimismo, se presenta la tabla de nuestro primer sprint con las respectivas user stories a trabajar:

| Sprint #   | Sprint 1           |     |              |                    |                    |               |          |
| ---------- | ------------------ | --- | ------------ | ------------------ | ------------------ | ------------- | -------- |
| User Story | Work-Item/Task     |     |              |                    |                    |               |          |
| Id         | Title              | Id  | Title        | Description        | Estimation (Hours) | Assigned To   | Status   |
| US[XX]     | [User Story Title] | 1   | [Task Title] | [Task Description] | [X]                | [Team Member] | [Status] |
| US[XX]     | [User Story Title] | 2   | [Task Title] | [Task Description] | [X]                | [Team Member] | [Status] |

[...continuar según necesidades del proyecto]

#### 7.2.1.3. Development Evidence for Sprint Review.

[Descripción general del desarrollo realizado en el Sprint]

| Repository  | Branch        | Commit ID | Commit Message | Commit Message Body | Commited on (Date) |
| ----------- | ------------- | --------- | -------------- | ------------------- | ------------------ |
| [Repo Name] | [Branch Name] | [ID]      | [Message]      | [Body]              | [DD-MM-YYYY]       |
| [Repo Name] | [Branch Name] | [ID]      | [Message]      | [Body]              | [DD-MM-YYYY]       |

[...continuar según necesidad]

**Network**

<div align="center">
  <img src="[ruta-imagen-network-1]" width=500 alt="Network">   
</div>

<div align="center">
  <img src="[ruta-imagen-network-2]" width=500 alt="Network">   
</div>

#### 7.2.1.4. Testing Suite Evidence for Sprint Review.

| Repository  | Branch   | Commit ID | Commit Message | Commit Message Body | Commited on (Date) |
| ----------- | -------- | --------- | -------------- | ------------------- | ------------------ |
| [Test Repo] | [Branch] | [ID]      | [Message]      | [Body]              | [DD-MM-YYYY]       |

[Descripción de la estrategia de testing utilizada y justificación]

<div align="center">
 <img src="[ruta-imagen-testing-1]" width=500 alt="Testing">   
 <img src="[ruta-imagen-testing-2]" width=500 alt="Testing">
</div>

**Enlace del repositorio:** [URL del repositorio de testing]

#### 7.2.1.5. Execution Evidence for Sprint Review.

- **Landing Page**

Para el Sprint 1, se completó exitosamente el desarrollo de la landing page, cumpliendo con todos los objetivos establecidos. Se implementó una hero section impactante, una sección clara de características del producto y un footer informativo. La página es completamente responsive y se integró correctamente la redirección a las tiendas de aplicaciones. Se realizaron pruebas exhaustivas en diferentes dispositivos y navegadores para garantizar una experiencia consistente.

<div align="center">
 <img src="[ruta-imagen-landing]" width=500 alt="Execution">   
</div>

- **Modelos de IA**

El desarrollo de los modelos de IA representó uno de los mayores desafíos del sprint, requiriendo un proceso iterativo de investigación y pruebas.  
Se exploraron dos aproximaciones en paralelo para encontrar la solución óptima. La primera aproximación involucró el uso de Azure Cognitive Services, realizando pruebas iniciales con sus servicios cognitivos para el reconocimiento de imágenes y evaluando su precisión con un conjunto selecto de obras de arte famosas. Paralelamente, se trabajó en el desarrollo y entrenamiento de modelos personalizados utilizando TensorFlow, enfocándose tanto en el reconocimiento de obras de arte como en la restauración digital básica.  
Durante el proceso de desarrollo, se evaluó cuidadosamente el balance entre precisión y tamaño de los modelos, considerando dos alternativas de implementación: la integración directa en la aplicación móvil o el despliegue en un servicio separado con llamadas API. Las pruebas de rendimiento y precisión se realizaron sistemáticamente para determinar la mejor aproximación final para el proyecto.

<div align="center">
 <img src="[ruta-imagen-modelo-IA]" width=500 alt="Execution">   
</div>

- **Aplicación móvil**

Se alcanzó un progreso sustancial en el desarrollo de la aplicación móvil utilizando Flutter, estableciendo las funcionalidades fundamentales del sistema. El desarrollo se centró en la implementación del sistema de autenticación de usuarios robusto y seguro. Se logró desarrollar una interfaz de usuario principal con una navegación fluida e intuitiva, junto con la integración exitosa del módulo de cámara para el escaneo de obras. También se implementó la visualización básica de los resultados de reconocimiento y restauración. La arquitectura de la aplicación se diseñó considerando la potencial integración de los modelos de IA, manteniendo la flexibilidad necesaria para adaptarse tanto a una implementación on-device como a llamadas API.

<div align="center">
 <img src="[ruta-imagen-movil]" width=500 alt="Execution">   
</div>

- **Web Service (Backend)**

Se estableció exitosamente la infraestructura básica del backend del sistema, implementando los componentes esenciales para el funcionamiento de la aplicación. El desarrollo incluyó la implementación de un sistema de autenticación robusto utilizando JWT para garantizar la seguridad de las sesiones de usuario. Se crearon los endpoints básicos necesarios para la gestión completa de usuarios, incluyendo registro, autenticación y administración de perfiles. Adicionalmente, se estableció la estructura inicial necesaria para la futura integración con los modelos de IA, preparando el terreno para la incorporación de las capacidades de procesamiento de imágenes. El servicio se desplegó exitosamente en un ambiente de desarrollo, permitiendo realizar las primeras pruebas de integración con la aplicación móvil y validar el funcionamiento del sistema completo.

<div align="center">
 <img src="[ruta-imagen-Backend]" width=500 alt="Execution">   
</div>

#### 7.2.1.6. Services Documentation Evidence for Sprint Review.

Durante el Sprint 1, se establecieron dos componentes principales de servicios que soportan la funcionalidad core de la aplicación:

**Servicios de IA para Reconocimiento y Restauración**

Se implementaron dos aproximaciones paralelas para los servicios de procesamiento de imágenes:

Los modelos de IA se desarrollaron utilizando TensorFlow, creando servicios especializados para:

- Reconocimiento de obras de arte famosas
- Restauración digital de imágenes

Para optimizar el rendimiento y reducir el tamaño de la aplicación móvil, se implementó una arquitectura que utiliza Cloud Functions para el procesamiento de los modelos de IA. Esta decisión permitió mantener los modelos en la nube, reduciendo significativamente el tamaño de la aplicación mientras se mantiene la capacidad de procesamiento necesaria.

**API de Gestión de Usuarios**

Se desplegó exitosamente en Microsoft Azure una API RESTful que gestiona toda la funcionalidad relacionada con usuarios. Esta API incluye:

- Endpoints para registro y autenticación de usuarios
- Sistema de autenticación implementado con JWT
- Gestión de perfiles de usuario
- Control de acceso y autorización

La integración entre los servicios de IA en la nube y la API de usuarios permite un flujo de trabajo eficiente mientras se mantiene la aplicación móvil ligera y performante.

<div align="center">
 <img src="[ruta-imagen-servicios-1]" width=500 alt="Services"> 
</div>

#### 7.2.1.7. Software Deployment Evidence for Sprint Review.

Para el Sprint 1, se han conseguido desplegar exitosamente los siguientes componentes del sistema:

**Landing Page**

La landing page del proyecto se encuentra desplegada y accesible públicamente a través de GitHub Pages. La página web está alojada en el repositorio principal del proyecto y se actualiza automáticamente con cada push a la rama main.

URL de acceso: [Incluir URL de la landing page]

El despliegue incluye todos los elementos planificados para el primer sprint:

- Hero section con presentación del producto
- Sección de características principales de la aplicación
- Información sobre la tecnología de restauración de obras
- Footer con enlaces de contacto y navegación
- Diseño completamente responsive
- Enlaces de redirección a futura publicación en tiendas de aplicaciones

El sitio ha sido verificado y probado en múltiples navegadores (Chrome, Firefox, Safari) y dispositivos para garantizar su correcta visualización y funcionamiento.

<div align="center">
 <img src="[ruta-imagen-deployment-1]" width=500 alt="Deployment">
</div>

**Aplicación Móvil**

La aplicación móvil desarrollada en Flutter se encuentra actualmente en fase de desarrollo y pruebas. Para este primer sprint, se ha configurado un ambiente de pruebas utilizando Firebase

La aplicación aún no está disponible online, se terminara desplegando en firebase mas no en tiendas como google play.

<div align="center">
 <img src="[ruta-imagen-deployment-2]" width=500 alt="Deployment">
</div>

#### 7.2.1.8. Team Collaboration Insights during Sprint.

- **SE NECESITA DE LANDING, API, COLAB, MOVIL: HACERLOS PUBLICOS**

_Pulse_

 <div align="center">
 <img src="[ruta-imagen-pulse-1]" width=500 alt="Pulse Sprint 1">
 </div>

_Contributors_

 <div align="center">
   <img src="[ruta-imagen-contributors-1]" width=500 alt="Contributors Sprint 1">
 </div>

## 7.3. Validation Interviews.

### 7.3.1. Diseño de Entrevistas.

### 7.3.2. Registro de Entrevistas.

### 7.3.3. Evaluaciones según heurísticas.

## 7.4. Video About-the-Product.
