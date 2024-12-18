# Chapter VII: Product Implementation, Validation & Deployment

## 7.1 Software Configuration Management

### 7.1.1 Software Development Environment Configuration

#### Project Management

Usamos **GitHub** como el repositorio principal para organizar las tareas. **Trello** facilita la gestión de hitos y pendientes, permitiendo establecer límites claros en los plazos. Las reuniones grupales se realizan en **Discord** cuando hay dudas o consultas.

#### Requirements Management

Cada entrega es revisada y discutida por el equipo para reducir errores en la fase de presentación. **Figma** es nuestra referencia para visualización de requisitos.

#### Product UX/UI Design

El diseño de UX/UI se realiza en **Figma**, desde wireframes hasta prototipos de alta fidelidad para Mobile Apps. Referencia: [Figma](https://www.figma.com/).

#### Software Development

Para la app móvil, utilizamos **Flutter** y **Dart** con **Android Studio** como entorno de desarrollo, ajustado para garantizar una experiencia óptima en dispositivos móviles.

#### Software Deployment

La landing page y otras partes del frontend están alojadas en **GitHub**, proporcionando una integración ágil. El backend está implementado en **Azure**, mientras que la app móvil utiliza **Firebase**.

#### Software Documentation

Usamos **GitHub** para documentar y gestionar la colaboración del equipo, permitiendo un control efectivo de versiones y una estructura modular.

### 7.1.2 Source Code Management

Cada componente tiene su propio repositorio en GitHub:

- **Report**: [https://github.com/ImagIA-2024-02/Report](https://github.com/ImagIA-2024-02/Report)
- **Backend**: [https://github.com/ImagIA-2024-02/backend-Imagia](https://github.com/ImagIA-2024-02/backend-Imagia)
- **App Móvil**: [https://github.com/ImagIA-2024-02/frontend-app](https://github.com/ImagIA-2024-02/frontend-app)
- **Landing Page**: [https://github.com/ImagIA-2024-02/LandingPage](https://github.com/ImagIA-2024-02/LandingPage)
- **AI-models**: [https://github.com/ImagIA-2024-02/AI-models](https://github.com/ImagIA-2024-02/AI-models)

### 7.1.3 Source Code Style Guide & Conventions

### HTML Conventions

- Usa nombres en minúsculas para elementos y atributos.
- Asegúrate de cerrar todos los elementos y especificar `alt`, `width`, y `height` en imágenes.

### CSS Conventions

- Nombres significativos y concisos en IDs y clases.
- Orden alfabético en declaraciones, y propiedades shorthand donde sea posible.

Referencias:

- [HTML Style Guide](https://www.w3schools.com/html/html5_syntax.asp)
- [CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html#CSS)

### 7.1.4 Software Deployment Configuration

**GitHub** es nuestra herramienta para el control de versiones y gestión de ciclo de vida, permitiendo una colaboración estructurada en el backend y frontend del proyecto.

- **Report**: [https://github.com/ImagIA-2024-02/Report](https://github.com/ImagIA-2024-02/Report)
- **Backend**: [https://github.com/ImagIA-2024-02/backend-Imagia](https://github.com/ImagIA-2024-02/backend-Imagia)
- **App Móvil**: [https://github.com/ImagIA-2024-02/frontend-app](https://github.com/ImagIA-2024-02/frontend-app)
- **Landing Page**: [https://github.com/ImagIA-2024-02/LandingPage](https://github.com/ImagIA-2024-02/LandingPage)
- **AI-models**: [https://github.com/ImagIA-2024-02/AI-models](https://github.com/ImagIA-2024-02/AI-models)

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
          <p>80</p>
        </td>
    </tr>
    <tr>
        <td>
           <p>Sum of Story Points</p>
        </td>
        <td>
          <p>21</p>
        </td>
    </tr>
</table>

#### 7.2.1.2. Sprint Backlog 1.

El Sprint 1 tiene como objetivo establecer los cimientos fundamentales del proyecto de restauración digital de obras de arte famosas, enfocándose en cuatro pilares principales:

**Landing Page**<br>
Desarrollo de una landing page responsive y funcional que sirva como punto de entrada al proyecto. Esta incluirá una hero section impactante, información clara sobre las características del producto, y enlaces de redirección a las tiendas de aplicaciones, proporcionando así una presencia web profesional y efectiva.<br><br>

**Infraestructura Backend**<br>
Implementación del sistema base de autenticación y gestión de usuarios, estableciendo la infraestructura necesaria para el manejo seguro de cuentas de usuario mediante JWT, sentando las bases para futuras funcionalidades.<br><br>

**Aplicación Móvil Base**<br>
Desarrollo de la primera versión de la aplicación móvil con una interfaz de usuario intuitiva, incluyendo las funcionalidades esenciales de navegación, registro/login de usuarios, y la capacidad de escanear obras de arte mediante la cámara del dispositivo.<br><br>

**Modelos de IA Fundamentales**<br>
Implementación de las primeras versiones de los modelos de inteligencia artificial necesarios para:<br>

- Reconocimiento de obras de arte famosas
- Restauración digital básica de imágenes
- Visualización comparativa del antes y después de la restauración<br><br>

Este sprint sienta las bases tecnológicas y funcionales del proyecto, permitiendo validar el concepto principal y obtener feedback temprano de usuarios sobre las funcionalidades core del producto.<br><br>

**Métricas de Éxito**<br>

- Landing page funcional y responsive
- Sistema de autenticación operativo
- Capacidad de escanear y reconocer al menos 5 obras famosas predefinidas
- Generar una versión restaurada básica de las obras escaneadas<br><br>

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

| Repository     | Branch  | Commit ID                                | Commit Message                                                           | Commit Message Body | Commited on (Date) |
| -------------- | ------- | ---------------------------------------- | ------------------------------------------------------------------------ | ------------------- | ------------------ |
| frontend-app   | main    | 0288fdbe14851461b6f22a70ee0eb82116fb5120 | Merge pull request                                                       | ...                 | 02-11-2024         |
| frontend-app   | develop | 5ed08b9ea6234ef610f3fb48116b9da2336f5d6b | added little details                                                     | ...                 | 02-11-2024         |
| frontend-app   | develop | a2829ac15f58c6f6c6e163fbf4e887b07a61ee2b | added icons personalized and optimized models                            | ...                 | 01-11-2024         |
| frontend-app   | develop | 3edcb3a0b3810e2423ef6871763c6fa54c613272 | added save gallery and improve UI                                        | ...                 | 01-11-2024         |
| frontend-app   | develop | 6225f7df6625c098a25425b77d88606f8aa8d06a | updated comments unnecessary                                             | ...                 | 30-10-2024         |
| frontend-app   | develop | d5cc592668753952afbb539149ed367d2236f0c2 | added configuration android and ios                                      | ...                 | 30-10-2024         |
| frontend-app   | develop | c374afd9b3ac2ad0b4e08a9a470e633803a8414c | added models from firebase and basic ui                                  | ...                 | 30-10-2024         |
| backend-Imagia | main    | 33a2161b3e72a949ec8cc39c138fc5eb7bd92775 | Merge branch 'develop'                                                   | ...                 | 29-10-2024         |
| backend-Imagia | develop | ef4b82ecb407de40101fa9c137bd0d88d0c1c412 | Add conection to remote database                                         | ...                 | 29-10-2024         |
| backend-Imagia | main    | d6d760642e903426e61b176fdefa4900ac316f80 | Add or update the Azure App Service build and deployment workflow config | ...                 | 28-10-2024         |
| backend-Imagia | develop | 17cab8b883054f41ba580528b953e43556760ad6 | add registro de obras de arte                                            | ...                 | 27-10-2024         |
| backend-Imagia | develop | efa7f6db11de6c2c9994477fd89075c80fadf808 | first commit                                                             | ...                 | 22-10-2024         |
| LandingPage    | main    | d1f4cb4f5d29b42bf03d31ba38de5f819378b1bf | Primer commit - Landing page de PictorIA                                 | ...                 | 02-11-2024         |
| AI-models      | main    | 60f9200eba13f0eda947cfd83ab2871e5aea169e | add description for restoration model                                    | ...                 | 02-11-2024         |
| AI-models      | main    | 462a4fd6cf847e6b998971b84d77284b52d5fbb0 | add description for recognition model and notebooks                      | ...                 | 02-11-2024         |

**Network**  
Frontend:

<div align="center">
  <img src="../Recursos/imagenes/network_frontend-app.png" width=500 alt="Network">   
</div>  
Backend:  
<div align="center">
  <img src="../Recursos/imagenes/network_backend-imagia.png" width=500 alt="Network">   
</div>  
AI-models:
<div align="center">
  <img src="../Recursos/imagenes/network_AI-models.png" width=500 alt="Network">   
</div> 

#### 7.2.1.4. Testing Suite Evidence for Sprint Review.

| Repository | Branch | Commit ID                                | Commit Message      | Commit Message Body | Commited on (Date) |
| ---------- | ------ | ---------------------------------------- | ------------------- | ------------------- | ------------------ |
| Gherkin    | main   | e355caf03b659878a50591af018235adea7ca34e | add core US Guerkin | ...                 | 02-11-2024         |

##### Estrategia de Testing

La estrategia de testing utilizada para estas historias de usuario se basa en pruebas funcionales utilizando el formato BDD (Behavior-Driven Development), empleando el lenguaje Gherkin para definir escenarios de prueba en un lenguaje claro y comprensible tanto para el equipo técnico como para los stakeholders. Esta estrategia se centra en validar que cada funcionalidad cumpla con los requisitos especificados en las historias de usuario, asegurando así una alta calidad en la experiencia de usuario final.

###### Justificación

- Claridad y Comunicación: El uso de Gherkin facilita la comprensión de los requisitos y pruebas, ya que permite que todos los involucrados (desarrolladores, testers y stakeholders) puedan leer y entender los casos de prueba sin necesidad de conocimientos técnicos avanzados.

- Orientación a la Funcionalidad: Al estar basada en pruebas funcionales, esta estrategia se enfoca en validar que cada funcionalidad cumpla con las expectativas del usuario final, alineándose con los objetivos de cada historia de usuario.

- Cobertura de Casos Positivos y Negativos: Los escenarios incluyen tanto casos exitosos como el manejo de errores, asegurando que la aplicación responde adecuadamente tanto en condiciones óptimas como en situaciones adversas.

- Mejora Continua y Automatización: Al emplear Gherkin, los casos de prueba son fácilmente automatizables con herramientas como Cucumber, lo que permite ejecutar pruebas de manera continua e integrarlas en un flujo de CI/CD, reduciendo el tiempo de feedback y mejorando la eficiencia del proceso de desarrollo.

- Esta estrategia garantiza que las funcionalidades clave del sistema se prueben exhaustivamente y que el usuario reciba una experiencia coherente y confiable.

<div align="center">
 <img src="../Recursos/imagenes/testing_US12.png" width=500 alt="Testing">   
</div>

**Enlace del repositorio:** [[https://github.com/ImagIA-2024-02/Gherkin](https://github.com/ImagIA-2024-02/Gherkin)]

#### 7.2.1.5. Execution Evidence for Sprint Review.

- **Landing Page**

Para el Sprint 1, se completó exitosamente el desarrollo de la landing page, cumpliendo con todos los objetivos establecidos. Se implementó una hero section impactante, una sección clara de características del producto y un footer informativo. La página es completamente responsive y se integró correctamente la redirección a las tiendas de aplicaciones. Se realizaron pruebas exhaustivas en diferentes dispositivos y navegadores para garantizar una experiencia consistente.

<div align="center">
 <img src="../Recursos/imagenes/landing-img.png" width=500 alt="Execution">   
</div>

- **Modelos de IA**

El desarrollo de los modelos de IA representó uno de los mayores desafíos del sprint, requiriendo un proceso iterativo de investigación y pruebas.  
Se exploraron dos aproximaciones en paralelo para encontrar la solución óptima. La primera aproximación involucró el uso de Azure Cognitive Services, realizando pruebas iniciales con sus servicios cognitivos para el reconocimiento de imágenes y evaluando su precisión con un conjunto selecto de obras de arte famosas. Paralelamente, se trabajó en el desarrollo y entrenamiento de modelos personalizados utilizando TensorFlow, enfocándose tanto en el reconocimiento de obras de arte como en la restauración digital básica.  
Durante el proceso de desarrollo, se evaluó cuidadosamente el balance entre precisión y tamaño de los modelos, considerando dos alternativas de implementación: la integración directa en la aplicación móvil o el despliegue en un servicio separado con llamadas API. Las pruebas de rendimiento y precisión se realizaron sistemáticamente para determinar la mejor aproximación final para el proyecto.

<div align="center">
 <img src="../Recursos/imagenes/modelo-ia-recognition.png" width=500 alt="Execution">  
 <img src="../Recursos/imagenes/modelo-ia-restoration.png" width=500 alt="Execution">   
</div>

- **Aplicación móvil**

Se alcanzó un progreso sustancial en el desarrollo de la aplicación móvil utilizando Flutter, estableciendo las funcionalidades fundamentales del sistema. El desarrollo se centró en la implementación del sistema de autenticación de usuarios robusto y seguro. Se logró desarrollar una interfaz de usuario principal con una navegación fluida e intuitiva, junto con la integración exitosa del módulo de cámara para el escaneo de obras. También se implementó la visualización básica de los resultados de reconocimiento y restauración. La arquitectura de la aplicación se diseñó considerando la potencial integración de los modelos de IA, manteniendo la flexibilidad necesaria para adaptarse tanto a una implementación on-device como a llamadas API.

<div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/excecution-movil.png" width=500 alt="Execution">   
</div>

- **Web Service (Backend)**

Se estableció exitosamente la infraestructura básica del backend del sistema, implementando los componentes esenciales para el funcionamiento de la aplicación. El desarrollo incluyó la implementación de un sistema de autenticación robusto utilizando JWT para garantizar la seguridad de las sesiones de usuario. Se crearon los endpoints básicos necesarios para la gestión completa de usuarios, incluyendo registro, autenticación y administración de perfiles. Adicionalmente, se estableció la estructura inicial necesaria para la futura integración con los modelos de IA, preparando el terreno para la incorporación de las capacidades de procesamiento de imágenes. El servicio se desplegó exitosamente en un ambiente de desarrollo, permitiendo realizar las primeras pruebas de integración con la aplicación móvil y validar el funcionamiento del sistema completo.

<div align="center">
 <img src="../Recursos/imagenes/backend-swagger.png" width=500 alt="Execution">   
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

#### 7.2.1.7. Software Deployment Evidence for Sprint Review.

Para el Sprint 1, se han conseguido desplegar exitosamente los siguientes componentes del sistema:

**Landing Page**

La landing page del proyecto se encuentra desplegada y accesible públicamente a través de GitHub Pages. La página web está alojada en el repositorio principal del proyecto y se actualiza automáticamente con cada push a la rama main.

URL de acceso: [[https://imagia-2024-02.github.io/LandingPage/](https://imagia-2024-02.github.io/LandingPage/)]

El despliegue incluye todos los elementos planificados para el primer sprint:

- Hero section con presentación del producto
- Sección de características principales de la aplicación
- Información sobre la tecnología de restauración de obras
- Footer con enlaces de contacto y navegación
- Diseño completamente responsive
- Enlaces de redirección a futura publicación en tiendas de aplicaciones

El sitio ha sido verificado y probado en múltiples navegadores (Chrome, Firefox, Safari) y dispositivos para garantizar su correcta visualización y funcionamiento.

<div align="center">
 <img src="../Recursos/imagenes/deployment-landing.png" width=500 alt="Deployment">
</div>

**Aplicación Móvil**

La aplicación móvil desarrollada en Flutter se encuentra actualmente en fase de desarrollo y pruebas. Para este primer sprint, se ha configurado un ambiente de pruebas utilizando Firebase

La aplicación aún no está disponible online, se terminara desplegando en firebase mas no en tiendas como google play.

#### 7.2.1.8. Team Collaboration Insights during Sprint.

**_Pulse_**

App movil:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_movil_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

Backend:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse-backend-1.png" width=500 alt="Pulse Sprint 1">
 </div>

Modelos de IA:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_ai_model_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

Landing page:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_landing_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

**_Contributors_**

App movil:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_movil_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

Backend:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/contributors-backend-1.png" width=500 alt="Pulse Sprint 1">
 </div>

Modelos de IA:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_ai_model_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

Landing page:

 <div align="center">
 <img src="../Recursos/imagenes/7.2.1.sprint-1/pulse_landing_tb2.png" width=500 alt="Pulse Sprint 1">
 </div>

### 7.2.2. Sprint 2

#### 7.2.2.1. Sprint Planning 2.

<table><thead>
  <tr>
    <th>Sprint #</th>
    <th>2</th>
  </tr></thead>
<tbody>
  <tr>
    <td colspan="2">Sprint Planning Background</td>
  </tr>
  <tr>
    <td>Date</td>
    <td>06 - 11 - 2024</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>21:00</td>
  </tr>
  <tr>
    <td>Location</td>
    <td>Reunión virtual vía Discord</td>
  </tr>
  <tr>
    <td>Prepared by</td>
    <td>Antonela Gonzales</td>
  </tr>
  <tr>
    <td>Attendees</td>
    <td>Todos los integrantes</td>
  </tr>
  <tr>
    <td>Sprint 1 Review Summary</td>
    <td>Parcialmente completado</td>
  </tr>
  <tr>
    <td>Sprint 1 Retrospective summary</td>
    <td>Los integrantes deben avisas de sus avances en el chat grupal.</td>
  </tr>
  <tr>
    <td colspan="2">Sprint Goal &amp; User Stories</td>
  </tr>
  <tr>
    <td>Sprint 2 Goal</td>
    <td>Completar el flujo core y garantizar la confiabilidad de los modelos en un 75%.</td>
  </tr>
</tbody>
</table>

#### 7.2.2.2. Sprint Backlog 2.

El sprint 2 tiene como objetivo completar el flujo core de la aplicación Pictoria, lo cual incluye:

<table><thead>
  <tr>
    <th>Sprint #</th>
    <th colspan="7">2</th>
  </tr></thead>
<tbody>
  <tr>
    <td colspan="2">User Story</td>
    <td colspan="6">Work Item/Task</td>
  </tr>
  <tr>
    <td>Id</td>
    <td>Title</td>
    <td>Id</td>
    <td>Title</td>
    <td>Description</td>
    <td>Estimation (Hours)</td>
    <td>Asigned to</td>
    <td>Status</td>
  </tr>
  <tr>
    <td rowspan="3">US10</td>
    <td rowspan="3">Escaneo y reconocimiento de obras de arte.</td>
    <td>1</td>
    <td>Refinar el flujo de reconocimiento</td>
    <td>Asegurarse de que el flujo de reconocimiento funcione correctamente.</td>
    <td>4</td>
    <td>Rafael Primo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Implementar flujo de segmentación.</td>
    <td>Asegurarse de que el flujo de segmentación funcione correctamente.</td>
    <td>4</td>
    <td>Rafael Primo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Refinar flujo de restauración.</td>
    <td>Asegurarse de que el flujo de restauración funcione correctamente.</td>
    <td>4</td>
    <td>Rafael Primo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td rowspan="4">TS02</td>
    <td rowspan="4">Escaneo y reconocimiento de obras de Arte.</td>
    <td>4</td>
    <td>Conectar los modelos de IA</td>
    <td>Subir los modelos mejorados a Firebase y asegurarse de que se integren en la aplicación móvil.</td>
    <td>2</td>
    <td>Rafael Primo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Refinar modelo de reconocimiento</td>
    <td>Mejorar la precisión del modelo</td>
    <td>4</td>
    <td>Jesica Jaramillo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Crear modelo segmentador</td>
    <td>Crear modelo que delimite la obra de arte de una foto</td>
    <td>4</td>
    <td>Jesica Jaramillo</td>
    <td>Done</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Corregir modelo de restauración</td>
    <td>Corregir las manchas negras generadas por el modelo de restauración V1.</td>
    <td>4</td>
    <td>Jesica Jaramillo</td>
    <td>Done</td>
  </tr>
</tbody></table>

#### 7.2.2.3. Development Evidence for Sprint Review.

| Repository     | Branch                    | Commit ID                                | Commit Message                                        | Commit Message Body | Commited on (Date) |
| -------------- | ------------------------- | ---------------------------------------- | ----------------------------------------------------- | ------------------- | ------------------ |
| frontend-app   | main                      | af24b0cb0b06263d8237d1f484369b7131f3e2c9 | Merge pull request #3 from ImagIA-2024-02/develop     | ...                 | 17-11-2024         |
| frontend-app   | develop                   | a66f637de7cce8d01a30049912084f944af40a74 | updated the models, designs and interface of the app  | ...                 | 17-11-2024         |
| AI-models      | main                      | 43cdefa8bb885dc79013bdc0038b825b5b1604e9 | Add fixed models and update Readme                    | ...                 | 18-11-2024         |
| backend-imagia | refactor/name-conventions | 6e06237ea7cf4d7a70a40a8128e13e933ca99d47 | feat: Secutity and handler exceptions, not tested yet | ...                 | 16-11-2024         |
| backend-imagia | refactor/name-conventions | fde2f9b5b22e90828dbc9674bfaff8900951ef76 | feat: database connect                                | ...                 | 15-11-2024         |
| backend-imagia | refactor/name-conventions | 89da765f85a932995323ce88d841837570c23f6d | feat: mantain table names                             | ...                 | 15-11-2024         |
| backend-imagia | refactor/name-conventions | 6d02855c451562cb2717ba333be5be73a9805a51 | feat: names with correct standars                     | ...                 | 15-11-2024         |

##### Network:

- Frontent:  
  [![Captura-de-pantalla-2024-11-21-151609.png](https://i.postimg.cc/JhtZXthG/Captura-de-pantalla-2024-11-21-151609.png)](https://postimg.cc/p9bmbWzH)
- Backend:  
  [![Captura-de-pantalla-2024-11-21-151507.png](https://i.postimg.cc/vHdrKQ0N/Captura-de-pantalla-2024-11-21-151507.png)](https://postimg.cc/RqXJ6z57)
- AI-models:  
  [![Captura-de-pantalla-2024-11-21-151740.png](https://i.postimg.cc/mr0zFwq5/Captura-de-pantalla-2024-11-21-151740.png)](https://postimg.cc/HJ9sqQTw)

#### 7.2.2.4. Testing Suite Evidence for Sprint Review.

##### Sobre el Modelo de restauración:

Se hicieron pruebas con una sección del dataset destinada a la validación:  
[![Imagen-de-Whats-App-2024-11-21-a-las-15-51-35-bfb93a70.jpg](https://i.postimg.cc/QdK0L6p6/Imagen-de-Whats-App-2024-11-21-a-las-15-51-35-bfb93a70.jpg)](https://postimg.cc/QFsp1JY5)  
Conjunto de validación (20% del dataset original):  
[![Imagen-de-Whats-App-2024-11-21-a-las-15-51-35-62ab98dd.jpg](https://i.postimg.cc/VLdFM7HY/Imagen-de-Whats-App-2024-11-21-a-las-15-51-35-62ab98dd.jpg)](https://postimg.cc/fJQXQvNF)  
Resultado de la evaluación:  
[![Imagen-de-Whats-App-2024-11-21-a-las-15-52-13-b586d287.jpg](https://i.postimg.cc/vTD5rBhP/Imagen-de-Whats-App-2024-11-21-a-las-15-52-13-b586d287.jpg)](https://postimg.cc/Zvt9ZJ13)  
Verificación de objetivo (Eliminar manchas negras generadas por fondos blancos y reflejos de luz):  
[![Imagen-de-Whats-App-2024-11-21-a-las-15-53-23-51d619d9.jpg](https://i.postimg.cc/jqkHsHqB/Imagen-de-Whats-App-2024-11-21-a-las-15-53-23-51d619d9.jpg)](https://postimg.cc/c6wgh8nc)

##### Sobre el modelo de reconocmiento:

Se realizaron pruebas unitarias con diversas imágenes de autores diferentes:  
[![images.jpg](https://i.postimg.cc/tCxxp8MV/images.jpg)](https://postimg.cc/mtTDSpRb)  
Resultado:  
[![Captura-de-pantalla-2024-11-21-160550.png](https://i.postimg.cc/wjYsvFC4/Captura-de-pantalla-2024-11-21-160550.png)](https://postimg.cc/Yh8SDNqQ)  
Se observa el nuevo umbral agregado. De modo que si la confianza del modelo para la predicción es menor a 75%, se mostrará el resultado "Desconocido".

#### Sobre el modelo de visión artificial (reconocimiento de artwork con yolo).

Se realizaron pruebas unitarias con diversas imágenes de internet:  
[![Captura-de-pantalla-2024-11-21-160933.png](https://i.postimg.cc/QtCFPz7C/Captura-de-pantalla-2024-11-21-160933.png)](https://postimg.cc/hzF4QppR)  
De modo que utilizando el cuadro delimitador, se recortará el "Artwork" del fondo:  
[![Captura-de-pantalla-2024-11-21-161120.png](https://i.postimg.cc/kMVcR1H7/Captura-de-pantalla-2024-11-21-161120.png)](https://postimg.cc/7bk7pVDR)

#### 7.2.2.5. Execution Evidence for Sprint Review.
Evidencia de ejecución de la aplicación móvil: [https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a](https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a)  
Enlace de invitación para aplicación Android desplegada en Firebase App Distribution: [https://appdistribution.firebase.dev/i/1568548a852a7713](https://appdistribution.firebase.dev/i/1568548a852a7713)

#### 7.2.2.6. Services Documentation Evidence for Sprint Review.

##### Descripción del Modelo para el Reconocimiento de Autores

Este modelo fue desarrollado en Google Colab utilizando TensorFlow. Su objetivo es clasificar obras de arte según el autor, utilizando una arquitectura de MobileNetV2 como base para optimización y velocidad, ideal para dispositivos móviles. La construcción del modelo incluyó varios pasos, desde la carga y preprocesamiento de datos hasta la creación y el entrenamiento de la red neuronal.

###### Proceso de Entrenamiento

- Aumentación de Datos: Se utilizó ImageDataGenerator para simular condiciones reales de captura de imágenes, como rotaciones, desplazamientos y ajustes de brillo.
- Entrenamiento de Capas Superiores: Inicialmente, solo se entrenaron las capas superiores, con las capas base congeladas para evitar el sobreajuste temprano.
- Fine-Tuning: Posteriormente, se descongelaron capas adicionales de MobileNetV2 para mejorar la precisión en las últimas etapas del entrenamiento.

###### Problemas Encontrados

Conversión a TensorFlow Lite: Durante la conversión a TFLite, el modelo experimentó errores de compatibilidad con el delegado XNNPack. Este problema se resolvió deshabilitando el delegado en la configuración del intérprete.
Errores de Dimensión: Durante las pruebas, hubo varios problemas con la dimensión del tensor de entrada. Esto se resolvió ajustando la redimensión y la normalización de las imágenes.

###### Link al Notebook de Google Colab

[[Enlace al notebook en Colab](https://colab.research.google.com/drive/1zNUN2m8Yqs4IebR2McDBQSlPpxp4yyfw?usp=sharing)]
[[Cuanderno descargado en el Repositorio](https://github.com/ImagIA-2024-02/AI-models/blob/main/ReconocimientoAutorSimpifPlayground.ipynb)]

##### Descripción del Modelo de Restauración de Imágenes

Este proyecto implementa un modelo de restauración de imágenes desarrollado en VSCode usando TensorFlow. El modelo sigue una arquitectura de tipo U-Net, diseñada para transformar imágenes degradadas en versiones restauradas, corrigiendo efectos como ruido, desenfoque, desvanecimiento de colores y grietas.

###### Proceso de Entrenamiento

_Dataset_

- Se generó un conjunto de datos con imágenes degradadas artificialmente. Las degradaciones incluyen adición de ruido, desvanecimiento de colores aleatorio, desenfoque, y superposición de texturas de grietas.
- Las imágenes originales fueron preprocesadas para evitar sobresaturación y se aplicaron métodos probabilísticos para garantizar una mayor variabilidad en las degradaciones.  
  _Entrenamiento_
- El modelo fue entrenado para aprender a restaurar estas imágenes degradadas, utilizando la función de pérdida de error cuadrático medio (MSE) para medir la diferencia entre las imágenes restauradas y las originales.
- Los datos se manejaron en lotes pequeños para optimizar el uso de memoria.

###### Problemas Enfrentados y Soluciones Implementadas

_1. Saturación de Colores:_
Al inicio, el modelo sobresaturaba los colores de las imágenes restauradas. Para solucionar esto:

- Se ajustó el proceso de degradación, implementando desvanecimiento de colores aleatorio con probabilidades controladas.
- Esto aumentó la diversidad del dataset, mejorando la capacidad del modelo para generalizar.
  _2. Uso de Memoria:_
  Durante el entrenamiento en Google Colab y sistemas locales con GPU, surgieron limitaciones de memoria:
- Se redujo el tamaño de lote (batch_size) y se configuró el uso dinámico de memoria en la GPU.
- Se implementaron pipelines con tf.data.Dataset para cargar los datos por lotes, optimizando el rendimiento.
  _3. Manchas Negras en Imágenes Restauradas:_
  Inicialmente, las imágenes restauradas presentaban manchas negras debido a una falta de diversidad en el dataset.
- Se ampliaron las variaciones en las texturas de grietas y degradaciones.
- Además, se incluyó protección para áreas blancas, evitando que el ruido degradara regiones clave de las imágenes originales.
  _4. Formato y Portabilidad:_
  El modelo se guardó en formato TensorFlow (SavedModel) para permitir vsu carga y uso eficiente, reduciendo el impacto en la memoria RAM durante las evaluaciones.

###### Link al Notebook

[[Cuanderno descargado en este Repositorio](https://github.com/ImagIA-2024-02/AI-models/blob/main/restorationv2/PlaygroundRegeneration.ipynb)]

###### Conclusión

Esta versión del modelo ha demostrado ser más robusta y eficiente para restaurar imágenes degradadas, ofreciendo resultados significativamente mejores gracias a las optimizaciones realizadas en el dataset, el entrenamiento y el manejo de recursos.

##### Descripción del Modelo Delimitador con YOLOv5

Este modelo fue desarrollado en Google Colab utilizando PyTorch y exportado a TensorFlow Lite para su implementación en dispositivos móviles. Su objetivo principal es detectar cuadros u obras de arte dentro de imágenes, generando coordenadas precisas de las áreas delimitadas (bounding boxes). El modelo es ideal para aplicaciones que requieren alta precisión y velocidad, como aplicaciones móviles o sistemas embebidos.

###### Proceso de Entrenamiento

- Modelo Base: Se utilizó la arquitectura YOLOv5, conocida por su balance entre precisión y velocidad, como base para la detección de objetos.
- Dataset Personalizado: Las imágenes fueron etiquetadas en formato YOLO para entrenar el modelo en la detección de cuadros dentro de diversos contextos.
- Aumentación de Datos: Incluyó rotaciones, cambios de escala y ajustes de brillo/contraste para simular escenarios reales.
- Entrenamiento: Se entrenó el modelo en múltiples épocas, utilizando GPUs de Google Colab para acelerar el proceso. Se configuró un umbral de confianza para filtrar detecciones menos precisas.

###### Conversión a TensorFlow Lite

- Exportación: El modelo entrenado en PyTorch fue exportado directamente a TensorFlow Lite usando el script export.py de Ultralytics.
- Optimización: Se aplicó la optimización de cuantización para reducir el tamaño del modelo y mejorar su rendimiento en dispositivos con recursos limitados.

###### Problemas Encontrados

1. Errores de Compatibilidad: Durante la conversión a TensorFlow Lite, surgieron problemas con ciertas capas del modelo. Esto se resolvió ajustando el script de exportación.
2. Configuración de Entrada: Se detectaron problemas con las dimensiones de entrada durante las pruebas. Esto se solucionó redimensionando las imágenes a 640x640 y normalizándolas a valores entre 0 y 1.
3. Interpretación de Resultados: Al principio, los valores de salida del modelo no coincidían con las expectativas. Esto requirió una reconfiguración de la estructura de salida del modelo.

###### Link al Notebook de Google Colab

[[Enlace al notebook en Colab](https://colab.research.google.com/drive/1AiyJ4cQnDVnyxSng1UCqZ4kaluPIcAe6?usp=sharing)]
[[Cuanderno descargado en este Repositorio](https://github.com/ImagIA-2024-02/AI-models/blob/main/PlaygroundArtworkReco.ipynb)]

Este modelo está listo para ser implementado en aplicaciones móviles, donde se pueden utilizar bounding boxes generados para procesar imágenes y brindar una experiencia de usuario óptima.

#### 7.2.2.7. Software Deployment Evidence for Sprint Review.
##### Aplicación móvil
Aplicación Móvil desplegada en Firebase App Distribution:  
[![Captura-de-pantalla-2024-11-21-204440.png](https://i.postimg.cc/0Qx2Z9vL/Captura-de-pantalla-2024-11-21-204440.png)](https://postimg.cc/mcXsgftw)  
Enlace de invitación para aplicación Android desplegada en Firebase App Distribution: [https://appdistribution.firebase.dev/i/1568548a852a7713](https://appdistribution.firebase.dev/i/1568548a852a7713)  

##### Modelos de IA:
Modelos de ia desplegados en Firebase Machine Learning:  
[![Imagen-de-Whats-App-2024-11-21-a-las-20-45-32-2b764d91.jpg](https://i.postimg.cc/Gpj1LG05/Imagen-de-Whats-App-2024-11-21-a-las-20-45-32-2b764d91.jpg)](https://postimg.cc/rdzHgdw1)  
##### Web Serivide Backend:
###### Backend desplegado en azure:
[![Captura-de-pantalla-2024-11-21-205941.png](https://i.postimg.cc/T3JRwZg0/Captura-de-pantalla-2024-11-21-205941.png)](https://postimg.cc/MnXk33sf)  
Dominio predeterminado: [imagia-back-ggesdta7c3c7duc4.canadacentral-01.azurewebsites.net](imagia-back-ggesdta7c3c7duc4.canadacentral-01.azurewebsites.net)
###### Swagger:  
<div align="center">
 <img src="/Recursos/imagenes/backend-swagger.png" width=500 alt="Execution">   
</div>

##### Base de datos:
Base de datos desplegada en azure:  
[![Captura-de-pantalla-2024-11-21-205801.png](https://i.postimg.cc/7hFRMZ8z/Captura-de-pantalla-2024-11-21-205801.png)](https://postimg.cc/N2xbQY0G)


#### 7.2.2.8. Team Collaboration Insights during Sprint.

##### AI Models:

- Pulse:  
  [![Captura-de-pantalla-2024-11-21-152330.png](https://i.postimg.cc/JhwMN2rZ/Captura-de-pantalla-2024-11-21-152330.png)](https://postimg.cc/LJVcRvZ8)
- Contributors:  
  [![Captura-de-pantalla-2024-11-21-152534.png](https://i.postimg.cc/ZRbkjk1B/Captura-de-pantalla-2024-11-21-152534.png)](https://postimg.cc/McFrKLZq)

##### Frontent-app (mobile):

- Pulse:  
  [![Captura-de-pantalla-2024-11-21-152730.png](https://i.postimg.cc/wvGWNSHd/Captura-de-pantalla-2024-11-21-152730.png)](https://postimg.cc/Pp1zsVP6)
- Contributors:  
  [![Captura-de-pantalla-2024-11-21-152838.png](https://i.postimg.cc/SRbgVcXZ/Captura-de-pantalla-2024-11-21-152838.png)](https://postimg.cc/ygnh8gy9)

##### Backend-imagia:

- Pulse:  
  [![Captura-de-pantalla-2024-11-21-153207.png](https://i.postimg.cc/tCC3brH3/Captura-de-pantalla-2024-11-21-153207.png)](https://postimg.cc/t7wZtNJJ)
- Contributors:  
  [![Captura-de-pantalla-2024-11-21-153310.png](https://i.postimg.cc/Z5Xpr4vH/Captura-de-pantalla-2024-11-21-153310.png)](https://postimg.cc/k2F2CrcR)

## 7.3. Validation Interviews.

### 7.3.1. Diseño de Entrevistas.

A continuación, se presenta el diseño de las entrevistas de validación para los diferentes segmentos de usuarios de la aplicación móvil de restauración de obras de arte famosas.<br><br>

**Preguntas Generales (para todos los segmentos)**<br>

- ¿Qué opinas de la interfaz principal de la aplicación?
- ¿Qué tan intuitivo te resultó el proceso de registro y login?
- ¿Cómo evalúas la funcionalidad de escaneo de obras de arte?
- ¿Qué te parece la calidad de las restauraciones generadas?
- ¿Te resultó fácil comparar la obra original con la versión restaurada?
- ¿Encontraste algún aspecto confuso o difícil de usar en la aplicación?
- ¿Qué características adicionales te gustaría ver en la aplicación?<br><br>

**Preguntas para Turistas**<br>

- ¿Con qué frecuencia visitas museos durante tus viajes?
- ¿Qué te pareció el proceso de reconocimiento de obras famosas?
- ¿Te resultó útil la información proporcionada sobre las obras reconocidas?
- ¿Utilizarías esta aplicación en futuros viajes a museos?
- ¿Compartirías las obras restauradas en tus redes sociales?
- ¿Qué información adicional sobre las obras te gustaría ver?<br><br>

**Preguntas para Estudiantes**<br>

- ¿Cómo utilizarías esta aplicación en tus estudios de arte?
- ¿Qué te parece la precisión del reconocimiento de obras famosas?
- ¿Te resulta útil la funcionalidad de restauración para estudiar detalles de las obras?
- ¿Considerarías usar la aplicación para proyectos académicos?
- ¿Qué herramientas adicionales necesitarías para tus estudios?
- ¿Te gustaría poder exportar o compartir las restauraciones de alguna manera específica?<br><br>

**Preguntas para Aficionados al Arte**<br>

- ¿Qué aspectos de la restauración digital te parecen más interesantes?
- ¿Cómo evalúas la calidad del proceso de restauración?
- ¿Te gustaría tener más control sobre los parámetros de restauración?
- ¿Qué opinas de la biblioteca de obras famosas reconocibles?
- ¿Utilizarías esta aplicación para explorar obras en diferentes museos?
- ¿Qué funcionalidades adicionales te ayudarían a apreciar mejor las obras?<br><br>

**Pregunta de Cierre (para todos los segmentos)**<br>

- Después de probar la aplicación, ¿la recomendarías a otras personas? ¿Por qué sí o por qué no?
- ¿Hay algún comentario adicional o sugerencia que quieras compartir sobre tu experiencia con la aplicación?

### 7.3.2. Registro de Entrevistas.

**Segmento: Ciudadanos Aficionados al arte:**

**Entrevistador:** Diego Merino
**Entrevistada:** Cristiana Poma
**Edad:**: 18 años
**Distrito:**: Los Olivos
**Ocupación:**: Estudiante de Comunicaciones Audiovisuales
**Dispositivo:** Android

<div class="container" style="text-align: center">
    <img src="https://media.discordapp.net/attachments/779964091531788330/1309319167798808607/image.png?ex=674125ff&is=673fd47f&hm=545ea14e055bd816916ce06fb788959fc502518e74fa206b906201ccd074e1eb&=&format=webp&quality=lossless" width="200" alt="Imagen de entrevista">
</div>

- Perfil:
  Cristiana Poma, una joven estudiante de Comunicaciones Audiovisuales de 18 años, representa un segmento juvenil interesado en el arte visual desde una perspectiva más general y no necesariamente tradicional. Reside en Los Olivos, un distrito urbano que favorece la conexión tecnológica, y utiliza un dispositivo Android como su principal herramienta de interacción. Aunque no es particularmente afín a visitar museos, Cristiana muestra interés por las pinturas y cuadros, especialmente aquellos que evocan emociones o tienen historias detrás.

- Interacción con la aplicación:
  Cristiana expresó que tuvo ciertas dificultades iniciales para comprender el funcionamiento de la aplicación, perdiéndose un poco entre las opciones disponibles. A pesar de esto, valoró el concepto de la plataforma y destacó que le resulta interesante la posibilidad de explorar más sobre las pinturas de manera interactiva.

Sugerencias:

Narrador: Cristiana sugirió incluir una función de narrador dentro de la aplicación, que proporcione más detalles sobre las pinturas y sus contextos. Esta característica, según ella, permitiría profundizar en la historia de cada obra y hacer la experiencia más inmersiva.
Galería Online: Le gustaría contar con una galería virtual organizada en “salas” temáticas o cronológicas. En estas salas, los usuarios podrían recorrer virtualmente las obras de arte, conocer más sobre ellas, y tener una experiencia similar a la de caminar por un museo físico, pero desde la comodidad de su dispositivo.
Interacción social: Cristiana mencionó que sería interesante integrar un espacio para dejar comentarios o reflexiones sobre las pinturas, como una forma de interactuar con otros usuarios y compartir opiniones.
Preferencias en la experiencia:

Prefiere experiencias visuales enriquecidas con narrativas que expliquen detalles únicos de las obras, pero sin sobrecargar de texto.
Encuentra atractivo el concepto de conectar con el arte a través de representaciones digitales dinámicas.
Considera que la posibilidad de agregar un elemento social o colaborativo dentro de la aplicación la haría más atractiva para las personas jóvenes, especialmente aquellas que no son habituales en museos.

**Entrevistador:** Diego Merino
**Entrevistada:** Maryorie Contreras
**Edad:**: 20 años
**Distrito:**: San Miguel
**Ocupación:**: Estudiante de Administración de Negocios Internacionales
**Dispositivo:** Android

<div class="container" style="text-align: center">
    <img src="https://media.discordapp.net/attachments/779964091531788330/1309319145430581310/image.png?ex=674125fa&is=673fd47a&hm=3b16d2e1af9b08be4dcb563d4550cbf27032eb2d687290755db26ea8faeadcbd&=&format=webp&quality=lossless&width=299&height=350" width="200" alt="Imagen de entrevista">
</div>

- Perfil:
  Maryorie Contreras, estudiante de 20 años de Administración de Negocios Internacionales, representa un segmento joven con un interés general por el arte, especialmente las pinturas, aunque no es de visitar museos frecuentemente. Al igual que otros jóvenes de su generación, utiliza un dispositivo Android como su principal herramienta tecnológica y tiene una conexión constante con aplicaciones digitales, lo que la convierte en una potencial usuaria de la aplicación PictorIA.

- Interacción con la aplicación:
  Maryorie resaltó varios puntos relacionados con su experiencia al utilizar la plataforma:

Confusión en los nombres de las opciones:

La opción "Galería" generó expectativas de una galería virtual donde se pudieran explorar obras de arte categorizadas o exhibidas en un formato interactivo. En lugar de eso, la funcionalidad actual no coincidió con lo que ella esperaba, lo que la llevó a expresar su frustración.
Considera que los nombres de las secciones y opciones deben ser más claros y representativos de su función.
Falta de un tutorial:

Maryorie destacó la necesidad de incluir un tutorial inicial o una guía dentro de la aplicación para explicar cómo navegar por las distintas secciones y aprovechar las funciones disponibles.
Señaló que la plataforma no le resultó intuitiva, lo que generó una curva de aprendizaje que, en su opinión, podría desmotivar a algunos usuarios.
Sugerencias:

Revisar y optimizar la nomenclatura: Cambiar nombres de opciones y secciones para que sean más descriptivos y fáciles de entender, como reemplazar "Galería" por algo como "Explorar Obras" o "Museo Virtual".
Implementar un tutorial interactivo: Agregar un tutorial introductorio que guíe al usuario en su primera interacción con la aplicación, mostrando las funcionalidades principales y cómo utilizarlas.
Mejorar la usabilidad: Simplificar la estructura de la aplicación para que sea más amigable para usuarios con poca experiencia en herramientas digitales avanzadas.
Preferencias en la experiencia:

Maryorie se siente atraída por la idea de explorar pinturas y obras de arte desde su dispositivo, pero enfatiza la importancia de que la experiencia sea fácil de usar y no requiera mucho tiempo para entenderla.
Cree que una galería virtual bien implementada podría atraer más a personas como ella, que disfrutan del arte pero no son visitantes frecuentes de museos.

**Entrevistador:** Diego Merino
**Entrevistada:** Mónica Prialé de la Peña
**Edad:**: 49
**Distrito:**: San Isidro
**Ocupación:**: Docente universitaria en informática
**Dispositivo:** Android

<div class="container" style="text-align: center">
    <img src="https://media.discordapp.net/attachments/779964091531788330/1309319119224569928/image.png?ex=674125f3&is=673fd473&hm=1fa6f671dd0972a37c4f6f58c9b829885a22cee60448faa3b7732c4fbb6884e9&=&format=webp&quality=lossless" width="200" alt="Imagen de entrevista">
</div>

- Perfil:
  Mónica Prialé de la Peña, docente universitaria en el área de informática, representa un perfil profesional y analítico. Aunque tiene un interés general por el arte, este no forma parte central de su vida, lo que aporta una perspectiva objetiva y práctica sobre la interacción con la aplicación PictorIA. Como usuaria de Android y con una experiencia avanzada en tecnología, Mónica brinda observaciones detalladas sobre la usabilidad y terminología de la plataforma, subrayando áreas clave para mejorar la experiencia del usuario.

- Interacción con la aplicación:

Confusión en la terminología:

Mónica señaló que el término "Galería" fue confuso, ya que lo interpretó como una galería virtual o un espacio museístico en línea, en lugar de una referencia a la galería de imágenes del dispositivo.
Recomendó cambiar o aclarar esta nomenclatura para evitar malentendidos y alinear las expectativas del usuario con las funcionalidades reales.
Sugerencias de mejora en los menús:

El término "Editor" le generó dudas, ya que esperaba herramientas típicas de edición (como añadir texto o modificar fondos). Sugirió un cambio en el nombre que refleje de manera más precisa la funcionalidad, como "Restaurar Imagen" o "Ajustar Detalles".
Resaltó la necesidad de tutoriales o ayudas contextuales, especialmente para explicar los términos y las opciones del menú.
Flujo de trabajo:

Apreció los pasos cortos y simples que forman parte del flujo de trabajo, lo que facilita que el usuario realice las acciones necesarias sin sentirse abrumado.
Sin embargo, señaló que la interfaz podría ser más clara para que los usuarios comprendan rápidamente qué esperar de cada funcionalidad.
Percepción de la restauración:

Destacó las diferencias entre las imágenes originales y restauradas, especialmente en aquellas que muestran daños notorios.
Comentó que en casos donde el daño es menor, las mejoras no siempre son evidentes, lo que podría ser decepcionante para algunos usuarios.
Falta de contexto inicial:

Mónica expresó que al principio tuvo dudas sobre cómo empezar a utilizar la aplicación y qué esperar de cada opción. Esto subraya la importancia de proporcionar un contexto claro desde el inicio, ya sea mediante un tutorial o una pantalla de bienvenida con explicaciones breves.
Sugerencias:

Revisar la terminología: Cambiar los nombres de las opciones "Galería" y "Editor" para reflejar con mayor precisión sus funcionalidades, como "Museo Virtual" o "Explorar Obras" en lugar de "Galería" y "Restaurar Imagen" en lugar de "Editor".
Implementar tutoriales interactivos: Incluir un tutorial inicial que explique paso a paso cómo utilizar la aplicación y qué esperar de cada opción del menú.
Optimizar la interfaz: Mejorar la claridad visual y textual de la interfaz para que sea más intuitiva y fácil de navegar para todos los usuarios, independientemente de su familiaridad con la tecnología.
Ofrecer ejemplos visuales: Incorporar ejemplos comparativos de imágenes dañadas y restauradas para que los usuarios comprendan mejor el valor de la funcionalidad, incluso en casos donde el daño sea mínimo.
Preferencias en la experiencia:

Mónica valora un flujo de trabajo eficiente y bien estructurado, pero cree que la claridad en la interfaz es fundamental para garantizar una experiencia satisfactoria.
Aunque su interés por el arte no es profundo, está dispuesta a utilizar una aplicación como PictorIA si esta logra transmitir sus funcionalidades de manera clara y eficiente.

**Entrevistador:** Diego Merino
**Entrevistado:** Leonardo Aquino
**Edad:**: 24
**Distrito:**: Cercado de Lima
**Ocupación:**: Estudiante de Ingeniería de Software
**Dispositivo:** Android

<div class="container" style="text-align: center">
    <img src="https://media.discordapp.net/attachments/779964091531788330/1309319097103814676/image.png?ex=674125ee&is=673fd46e&hm=8cc2b9c3631927e05769b6391e2f25ac27b4cc9ecb46ac73a5bf232ee686e63b&=&format=webp&quality=lossless&width=431&height=516" width="200" alt="Imagen de entrevista">
</div>

- Perfil:
  Leonardo Aquino, estudiante de Ingeniería de Software, aborda el arte como un hobby. Su interés se centra en la observación de distintos tipos de arte, desde piezas históricas hasta expresiones más liberales. Como usuario técnico y crítico, Leonardo aporta una perspectiva detallada sobre las áreas de mejora en la funcionalidad y el diseño de la aplicación PictorIA, con comentarios que reflejan tanto su conocimiento técnico como su aprecio por una experiencia de usuario optimizada.

- Interacción con la aplicación:

Restauración de imágenes:

Comentó que, en imágenes de alta calidad, las diferencias entre las versiones originales y restauradas no son muy notorias, lo que podría reducir el impacto visual esperado.
Observó que algunas imágenes restauradas parecían "aplastadas", lo que afecta la percepción estética y profesional del resultado.
Sugirió incorporar una descripción del autor y una explicación más detallada de las obras en futuras versiones, con el fin de enriquecer la experiencia educativa de los usuarios.
Interfaz:

Leonardo considera que las opciones no son intuitivas, lo que dificulta la navegación inicial y la comprensión de las funcionalidades.
Criticó el diseño estético de la aplicación, mencionando que podría ser más atractivo y estar alineado con las tendencias modernas de diseño para aplicaciones culturales y educativas.
Rendimiento:

Señaló que el tiempo requerido para restaurar imágenes es algo lento, lo que podría afectar la percepción de eficiencia del prototipo.
Percepción general:

Reconoció el potencial del prototipo, destacando que, si bien la idea es innovadora, hay aspectos clave que necesitan mejoras significativas, como la claridad de la interfaz y la calidad visual de las imágenes restauradas.
Sugerencias:

Mejorar la restauración:

Refinar los algoritmos de restauración para evitar distorsiones visuales como el efecto de "aplastado".
Incorporar herramientas que permitan al usuario ajustar manualmente ciertos parámetros de restauración para personalizar los resultados.
Ampliar la información sobre las obras:

Agregar descripciones detalladas de los autores y explicaciones contextuales sobre las obras, destacando su relevancia histórica o artística. Esto enriquecería la experiencia y cumpliría con las expectativas de usuarios interesados en el aprendizaje.
Optimizar la interfaz:

Rediseñar la estructura del menú para que sea más intuitiva, utilizando iconos descriptivos y textos más claros.
Modernizar el diseño gráfico para hacerlo más atractivo, con colores, tipografía y transiciones acordes a una experiencia digital innovadora.
Mejorar el rendimiento:

Incrementar la velocidad de los procesos de restauración mediante la optimización de los algoritmos y la gestión de recursos.
Ofrecer una barra de progreso para que los usuarios tengan una idea clara del tiempo que tomará la restauración.
Preferencias en la experiencia:

Leonardo aprecia aplicaciones que combinen estética, funcionalidad y velocidad, destacando que un diseño bien pensado puede marcar la diferencia en la adopción de un producto.
Aunque valora la propuesta de PictorIA, considera que los detalles técnicos y de usabilidad deben pulirse para que la aplicación cumpla con las expectativas de un usuario exigente y crítico.

### 7.3.3. Evaluaciones según heurísticas.

#### UX Heuristics & Principles Evaluation

##### Usability – Inclusive Design – Information Architecture

**CARRERA**: Ingeniería de Software  
**CURSO**: Arquitecturas de Software Emergentes  
**SECCIÓN**: WS82
**AUDITOR**: Diego Merino Mas  
**CLIENTE(S)**: Imagia

##### TAREAS A EVALUAR

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Análisis de imágenes sospechosas
2. Restauración de imágenes
3. Visualización de resultados del análisis
4. Gestión del historial de análisis
5. Compartir resultados
6. Configuración de preferencias de análisis

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Integración con servicios de terceros
2. Análisis de múltiples imágenes simultáneamente
3. Gestión de perfiles de usuario
4. Exportación masiva de resultados

##### ESCALA DE SEVERIDAD

| Nivel | Descripción                                                                                                                                                                                     |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1     | Problema superficial: puede ser fácilmente superado por el usuario ó ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.                    |
| 2     | Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente release. |
| 3     | Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les debe asignar una prioridad alta.                                 |
| 4     | Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.                               |

##### TABLA RESUMEN

| #   | Problema                                                                    | Escala de severidad | Heurística/Principio violada(o)               |
| --- | --------------------------------------------------------------------------- | ------------------- | --------------------------------------------- |
| 1   | Falta de indicador visual durante el procesamiento de imágenes              | 2                   | Usability: Visibilidad del estado del sistema |
| 2   | La interfaz no proporciona retroalimentación sobre el progreso del análisis | 3                   | Usability: Retroalimentación del sistema      |
| 3   | No hay opción de cancelar el análisis una vez iniciado                      | 2                   | Usability: Control y libertad del usuario     |

##### DESCRIPCIÓN DE PROBLEMAS

**PROBLEMA #1: Falta de indicador visual durante el procesamiento de imágenes**
**Severidad**: 2  
**Heurística violada**: Usability - Visibilidad del estado del sistema

**Problema**:  
Cuando un usuario sube o restaura una imagen en la aplicación móvil, no existe ningún indicador visual (como una barra de progreso o un ícono de carga) que informe al usuario que la aplicación está procesando la imagen. La interfaz permanece estática durante este proceso, lo cual puede generar incertidumbre en el usuario sobre si la acción se está ejecutando correctamente o si la aplicación se ha detenido.

<div style="border: 1px solid #ccc; padding: 10px; margin: 10px 0; text-align: center;">
    <img src="https://media.discordapp.net/attachments/779964091531788330/1302340723462504509/Screenshot_20241102_133153.jpg?ex=6727c2d0&is=67267150&hm=48029cc22151994034b6a8836462863488c02891ae9431328efedd1a306805fd&=&format=webp&width=238&height=531" alt="Captura de pantalla mostrando la falta de indicador visual durante el procesamiento" style="max-width: 100%; height: auto;">
    <p style="font-style: italic; margin-top: 5px;">Fig 1. Interfaz sin indicador de progreso durante el análisis de imagen</p>
</div>

**Recomendación**:  
Se recomienda implementar:

1. Un indicador de progreso animado (spinner) que aparezca inmediatamente después de iniciar el procesamiento
2. Una barra de progreso que muestre el porcentaje de avance del análisis
3. Un mensaje claro que indique la etapa actual del procesamiento
4. Posibilidad de minimizar la aplicación mientras se procesa la imagen, manteniendo una notificación del estado en la barra de sistema

**PROBLEMA #2: La interfaz no proporciona retroalimentación sobre el progreso del análisis**
**Severidad**: 3  
**Heurística violada**: Usability - Retroalimentación del sistema
**Problema**:  
Durante el proceso de análisis de imágenes, la aplicación no proporciona información sobre las diferentes etapas o pasos que se están ejecutando. El usuario no tiene visibilidad sobre si el análisis está en la fase de preprocesamiento, evaluación o generación de resultados. Esta falta de retroalimentación detallada puede causar frustración y desconfianza en el proceso, especialmente cuando los análisis toman más tiempo del esperado.

<div style="border: 1px solid #ccc; padding: 10px; margin: 10px 0; text-align: center;">
   <img src="https://media.discordapp.net/attachments/779964091531788330/1302340723462504509/Screenshot_20241102_133153.jpg?ex=6727c2d0&is=67267150&hm=48029cc22151994034b6a8836462863488c02891ae9431328efedd1a306805fd&=&format=webp&width=238&height=531" alt="Captura de pantalla mostrando la falta de retroalimentación durante el análisis" style="max-width: 100%; height: auto;">
   <p style="font-style: italic; margin-top: 5px;">Fig 2. Interfaz sin información sobre el progreso del análisis</p>
</div>

**Recomendación**:

1. Implementar un sistema de notificaciones que muestre:

- Fase actual del análisis (preprocesamiento, análisis, generación de reporte)
- Tiempo estimado restante
- Porcentaje de progreso total

2. Añadir mensajes informativos que expliquen brevemente cada fase
3. Incluir un indicador visual que muestre el flujo del proceso
4. Permitir al usuario acceder a un registro detallado del proceso si lo desea

### PROBLEMA #3: No hay opción de cancelar el análisis una vez iniciado

**Severidad**: 2  
**Heurística violada**: Usability - Control y libertad del usuario
**Problema**:  
Una vez que se inicia el proceso de análisis de una imagen, el usuario no tiene la opción de cancelarlo. Esto es especialmente problemático en situaciones donde:

- El usuario seleccionó accidentalmente la imagen incorrecta
- El proceso está tomando más tiempo del esperado
- El usuario necesita liberar recursos del dispositivo para otras tareas
- Se requiere realizar un análisis más urgente de otra imagen

<div style="border: 1px solid #ccc; padding: 10px; margin: 10px 0; text-align: center;">
   <img src="https://media.discordapp.net/attachments/779964091531788330/1302340723462504509/Screenshot_20241102_133153.jpg?ex=6727c2d0&is=67267150&hm=48029cc22151994034b6a8836462863488c02891ae9431328efedd1a306805fd&=&format=webp&width=238&height=531" alt="Captura de pantalla mostrando la falta de botón de cancelación" style="max-width: 100%; height: auto;">
   <p style="font-style: italic; margin-top: 5px;">Fig 3. Interfaz sin opción de cancelar el análisis en progreso</p>
</div>

**Recomendación**:

1. Agregar un botón de "Cancelar" claramente visible durante el proceso de análisis
2. Implementar un diálogo de confirmación cuando se solicite la cancelación
3. Asegurar que el proceso de cancelación libere los recursos del sistema apropiadamente
4. Proporcionar la opción de guardar el progreso parcial del análisis

## 7.4. Video About-the-Product.
### Verión 1:
[![Ver el video](https://img.youtube.com/vi/p9zqYlg8VJ8/0.jpg)](https://www.youtube.com/watch?v=p9zqYlg8VJ8)  
### Version final: 
[https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a](https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a)
