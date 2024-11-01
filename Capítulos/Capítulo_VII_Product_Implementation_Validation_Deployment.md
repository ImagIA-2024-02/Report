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
          <p>27-10-2024</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Time</p>
        </td>
        <td>
          <p>08:00</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Location</p>
        </td>
        <td>
          <p>Reunión virtual vía Discord</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Prepared By</p>
        </td>
        <td>
          <p>Antonella Gonzales</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Attendees</p>
        </td>
        <td>
          <p>Antonella Frida Gonzales Gomez, Jesica Rut Jaramillo Almora, Diego Martin Merino Mas, Rafael Wimmer Primo Estrada</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 0 Review Summary</p>
        </td>
        <td>
          <p>[-]</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sprint 0 Retrospective Summary</p>
        </td>
        <td>
          <p>[-]</p>
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
          <p>Desarrollar la landing page, unos primeros modelos funcionales e integrarlos en una primera versión de la aplicación móvil y desplegarlas</p>
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

El Sprint 1 tiene como objetivo establecer los cimientos fundamentales del proyecto de restauración digital de obras de arte famosas, enfocándose en cuatro pilares principales:

Landing Page
Desarrollo de una landing page responsive y funcional que sirva como punto de entrada al proyecto. Esta incluirá una hero section impactante, información clara sobre las características del producto, y enlaces de redirección a las tiendas de aplicaciones, proporcionando así una presencia web profesional y efectiva.
Infraestructura Backend
Implementación del sistema base de autenticación y gestión de usuarios, estableciendo la infraestructura necesaria para el manejo seguro de cuentas de usuario mediante JWT, sentando las bases para futuras funcionalidades.
Aplicación Móvil Base
Desarrollo de la primera versión de la aplicación móvil con una interfaz de usuario intuitiva, incluyendo las funcionalidades esenciales de navegación, registro/login de usuarios, y la capacidad de escanear obras de arte mediante la cámara del dispositivo.
Modelos de IA Fundamentales
Implementación de las primeras versiones de los modelos de inteligencia artificial necesarios para:

Reconocimiento de obras de arte famosas
Restauración digital básica de imágenes
Visualización comparativa del antes y después de la restauración

Este sprint sienta las bases tecnológicas y funcionales del proyecto, permitiendo validar el concepto principal y obtener feedback temprano de usuarios sobre las funcionalidades core del producto.
Métricas de Éxito

Landing page funcional y responsive
Sistema de autenticación operativo
Capacidad de escanear y reconocer al menos 5 obras famosas predefinidas
Generar una versión restaurada básica de las obras escaneadas

A continuación, se presenta un screenshot del sprint 1 en desarrollo realizado en Jira por
el equipo:

[Jira Sprint 1 Screenshot]

<div align="center">
  <img src="[ruta-imagen-jira]" alt="Jira Sprint 1 Screenshot">
</div>

Asimismo, se presenta la tabla de nuestro primer sprint con las respectivas user stories a trabajar:

| Sprint #   | Sprint 1                                                 |     |                                                     |                                                                                                                                                                                                                                                                                  |                    |                                |         |
| ---------- | -------------------------------------------------------- | --- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ | ------------------------------ | ------- |
| User Story | Work-Item/Task                                           |     |                                                     |                                                                                                                                                                                                                                                                                  |                    |                                |         |
| Id         | Title                                                    | Id  | Title                                               | Description                                                                                                                                                                                                                                                                      | Estimation (Hours) | Assigned To                    | Status  |
| US08       | Sección de Inicio de la Landing Page                     | 1   | Diseño inicial de hero section                      | Implementar la estructura HTML y estilos CSS de la hero section con contenido impactante y llamadas a la acción                                                                                                                                                                  | 4                  | Diego Martin Merino Mas        | Pending |
| US07       | Sección de Características del producto                  | 2   | Implementación de sección de características        | Desarrollar la sección que muestra las funcionalidades principales de la app de restauración de obras famosas                                                                                                                                                                    | 4                  | Diego Martin Merino Mas        | Pending |
| US05       | Diseño Responsivo de la Landing Page                     | 3   | Adaptación responsive del diseño                    | Implementar media queries y ajustes necesarios para garantizar la correcta visualización en todos los dispositivos                                                                                                                                                               | 6                  | Jesica Rut Jaramillo Almora    | Pending |
| US01       | Redirección de la landing Page a tiendas de aplicaciones | 4   | Configuración de enlaces a tiendas                  | Implementar la lógica de redirección a App Store o Play Store según el dispositivo del usuario                                                                                                                                                                                   | 3                  | Diego Martin Merino Mas        | Pending |
| US04       | Navegación y Contenido Informativo en el Footer          | 5   | Desarrollo del footer informativo                   | Crear el footer con links relevantes, información de contacto y navegación secundaria                                                                                                                                                                                            | 3                  | Diego Martin Merino Mas        | Pending |
| TS06       | Gestión de Usuarios y Autenticación                      | 6   | Implementación del sistema de autenticación         | Desarrollar el backend para registro y login de usuarios con JWT                                                                                                                                                                                                                 | 8                  | Antonella Frida Gonzales Gomez | Done    |
| US16       | Interfaz de usuario intuitiva                            | 7   | Desarrollo de UI móvil principal                    | Implementar las pantallas principales de la app móvil con navegación básica, incluyendo pantallas de login, registro, galería y visualización de obras                                                                                                                           | 10                 | Rafael Wimmer Primo Estrada    | Done    |
| US10       | Escaneo y reconocimiento de obras de arte                | 8   | Integración de cámara y reconocimiento              | Desarrollar la funcionalidad de escaneo de obras de arte usando la cámara del dispositivo, incluyendo la integración con los modelos de IA y manejo de errores                                                                                                                   | 16                 | Rafael Wimmer Primo Estrada    | Done    |
| TS02       | Escaneo y Reconocimiento de Obras de Arte                | 9   | Implementación del modelo de reconocimiento         | Investigación y pruebas de diferentes arquitecturas de ML para reconocimiento de obras famosas. Incluye recopilación de dataset, entrenamiento del modelo inicial, pruebas de precisión y optimización. Desarrollo de API endpoints para el procesamiento de imágenes            | 12                 | Jesica Rut Jaramillo Almora    | Done    |
| US11       | Visualización de restauración digital                    | 10  | Implementación del sistema de restauración completo | Desarrollo de la interfaz de visualización de restauración y modelo de IA inicial. Incluye investigación de técnicas de restauración digital, pruebas con diferentes algoritmos, implementación del modelo seleccionado y desarrollo de la interfaz de comparación antes/después | 14                 | Jesica Rut Jaramillo Almora    | Done    |

#### 7.2.1.3. Development Evidence for Sprint Review.

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

[Descripción general de los productos/features implementados]

- **Landing Page**

[Descripción de los logros y características implementadas en la Landing Page]

<div align="center">
 <img src="[ruta-imagen-landing]" width=500 alt="Execution">   
</div>

- **[Nombre del otro componente/aplicación]**

[Descripción de los logros y características implementadas]

<div align="center">
 <img src="[ruta-imagen-componente]" width=500 alt="Execution">   
</div>

#### 7.2.1.6. Services Documentation Evidence for Sprint Review.

[Descripción de los servicios implementados o simulados durante el sprint]

<div align="center">
 <img src="[ruta-imagen-servicios-1]" width=500 alt="Services"> 
</div>

[Descripción adicional de la implementación de servicios si es necesario]

<div align="center">
 <img src="[ruta-imagen-servicios-2]" width=500 alt="Services">   
</div>

#### 7.2.1.7. Software Deployment Evidence for Sprint Review.

- **[Componente 1 (ej: Landing Page)]**

[Descripción de la estrategia de despliegue utilizada y justificación]

<div align="center">
 <img src="[ruta-imagen-deployment-1]" width=500 alt="Deployment">
</div>

[Descripción del proceso de despliegue]

<div align="center">
 <img src="[ruta-imagen-deployment-2]" width=500 alt="Deployment">
</div>

[Descripción de resultados del despliegue]

<div align="center">
 <img src="[ruta-imagen-deployment-3]" width=500 alt="Deployment">
</div>

**Enlace del despliegue**: [URL del despliegue]

- **[Componente 2 (ej: Web Application)]**

[Descripción de la estrategia de despliegue utilizada y justificación]

<div align="center">
 <img src="[ruta-imagen-deployment-4]" width=500 alt="Deployment">
 <img src="[ruta-imagen-deployment-5]" width=500 alt="Deployment">
</div>

**Enlace del despliegue**: [URL del despliegue]

#### 7.2.1.8. Team Collaboration Insights during Sprint.

- **[Componente 1]**

_Pulse_

 <div align="center">
 <img src="[ruta-imagen-pulse-1]" width=500 alt="Pulse Sprint 1">
 </div>

_Contributors_

 <div align="center">
   <img src="[ruta-imagen-contributors-1]" width=500 alt="Contributors Sprint 1">
 </div>

- **[Componente 2]**

_Pulse_

 <div align="center">
   <img src="[ruta-imagen-pulse-2]" width=500 alt="Pulse Sprint 1">
 </div>

_Contributors_

 <div align="center">
   <img src="[ruta-imagen-contributors-2]" width=500 alt="Contributors Sprint 1">
 </div>

## 7.3. Validation Interviews.

### 7.3.1. Diseño de Entrevistas.

### 7.3.2. Registro de Entrevistas.

### 7.3.3. Evaluaciones según heurísticas.

## 7.4. Video About-the-Product.
