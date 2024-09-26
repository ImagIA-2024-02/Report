# Capítulo V: Tactical-Level Software Design

## 5.1. Bounded Context: Bounded User Account

El dominio de **User Account** se enfoca en la gestión y administración de cuentas de usuario dentro de la plataforma. Este dominio es responsable de manejar el ciclo de vida de las cuentas de usuario, la gestión de suscripciones y notificaciones, y asegurar que las reglas de negocio relacionadas con los usuarios y sus interacciones con la plataforma se apliquen correctamente.
**Diccionario de Clases:**

El **Diccionario de Clases** es una herramienta fundamental en el diseño del contexto "User Account". Proporciona una descripción detallada de las clases clave que forman la base del modelo de dominio del sistema, facilitando la comunicación entre los miembros del equipo y asegurando una base sólida para la solución propuesta. En esta sección, documentamos las entidades principales, sus atributos, métodos y relaciones con otros objetos.

El **Diccionario de Clases** en este contexto juega un papel clave en el diseño y desarrollo de nuestra solución, ya que proporciona una descripción detallada de las entidades fundamentales relacionadas con la administración de usuarios, suscripciones y notificaciones. Estas clases definen los atributos y comportamientos que permiten gestionar el ciclo de vida de una cuenta de usuario, incluyendo la creación de cuentas, validación de credenciales, manejo de suscripciones, y la gestión de notificaciones personalizadas.

En el Diccionario de Clases del User Account, se han identificado cuatro clases principales: User, Notification, Subscription, y UserRole. Estas clases forman el núcleo de este bounded context y permiten gestionar usuarios, suscripciones y notificaciones de manera eficaz.

<table><tr><th valign="top"><b>Nombre</b></th><th colspan="3" valign="top"><b>User</b></th></tr>
<tr><td valign="top"><b>Relaciones</b></td><td colspan="3" valign="top">Clase Subscription, Notification, UserRole</td></tr>
<tr><td valign="top"><b>Descripción</b></td><td colspan="3" valign="top">Esta clase representa a los usuarios dentro del sistema, gestionando su información de registro, estado de cuenta y suscripción.</td></tr>
<tr><td colspan="3"><b>Atributos</b></td><td rowspan="1"><b>Métodos</b></td></tr>
<tr><td valign="top"><b>Nombre</b></td><td><b>Tipo de dato</b></td><td><b>Visibilidad</b></td></tr>
<tr><td valign="top">Id</td><td valign="top">string</td><td valign="top">private</td><td rowspan="6" valign="top"><p>createAccount()</p><p>validateCredentials()</p><p>updateStatus()</p><p>updateStatus()</p><p>changeSubscription()</p></td></tr>
<tr><td valign="top">Username</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">email</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">password</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">subscriptionType</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">status</td><td valign="top">string</td><td valign="top">private</td></tr>
</table>

<table><tr><th valign="top"><b>Nombre</b></th><th colspan="3" valign="top"><b>Notification</b></th></tr>
<tr><td valign="top"><b>Relaciones</b></td><td colspan="3" valign="top">Clase User</td></tr>
<tr><td valign="top"><b>Descripción</b></td><td colspan="3" valign="top">Gestiona las notificaciones que el sistema envía a los usuarios sobre eventos importantes (cambio de suscripción, notificaciones de sistema, etc.).</td></tr>
<tr><td colspan="3"><b>Atributos</b></td><td rowspan="1"><b>Métodos</b></td></tr>
<tr><td valign="top"><b>Nombre</b></td><td><b>Tipo de dato</b></td><td><b>Visibilidad</b></td></tr>
<tr><td valign="top">id</td><td valign="top">string</td><td valign="top">private</td><td rowspan="4" valign="top">sendNotification()<br>scheduleNotification()</td></tr>
<tr><td valign="top">message</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">timestamp</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">userId</td><td valign="top">string</td><td valign="top">private</td></tr>
</table>

<table><tr><th valign="top"><b>Nombre</b></th><th colspan="3" valign="top"><b>Subscription</b></th></tr>
<tr><td valign="top"><b>Relaciones</b></td><td colspan="3" valign="top">Clase User</td></tr>
<tr><td valign="top"><b>Descripción</b></td><td colspan="3" valign="top">Gestiona las suscripciones que los usuarios pueden adquirir en la plataforma, permitiendo el cambio, activación y cancelación de las mismas.</td></tr>
<tr><td colspan="3"><b>Atributos</b></td><td rowspan="1"><b>Métodos</b></td></tr>
<tr><td valign="top"><b>Nombre</b></td><td><b>Tipo de dato</b></td><td><b>Visibilidad</b></td></tr>
<tr><td valign="top">id</td><td valign="top">string</td><td valign="top">private</td><td rowspan="5" valign="top"><p>activateSubscription()</p><p>renewSubscription()</p><p>cancelSubscription()</p></td></tr>
<tr><td valign="top">type</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">startDate</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">endDate</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">userId</td><td valign="top">string</td><td valign="top">private</td></tr>
</table>

<table><tr><th valign="top"><b>Nombre</b></th><th colspan="3" valign="top"><b>UserRole</b></th></tr>
<tr><td valign="top"><b>Relaciones</b></td><td colspan="3" valign="top">Clase User</td></tr>
<tr><td valign="top"><b>Descripción</b></td><td colspan="3" valign="top">Define los diferentes roles que los usuarios pueden tener en el sistema (por ejemplo, administrador, usuario regular) y gestiona los permisos asociados a cada rol.</td></tr>
<tr><td colspan="3"><b>Atributos</b></td><td rowspan="1"><b>Métodos</b></td></tr>
<tr><td valign="top"><b>Nombre</b></td><td><b>Tipo de dato</b></td><td><b>Visibilidad</b></td></tr>
<tr><td valign="top">id</td><td valign="top">string</td><td valign="top">private</td><td rowspan="3" valign="top"><p>assignRole()</p><p>changePermissions()</p><p>validatePermission()</p></td></tr>
<tr><td valign="top">roleName</td><td valign="top">string</td><td valign="top">private</td></tr>
<tr><td valign="top">permissions</td><td valign="top">List<string></td><td valign="top">private</td></tr>
</table>

### 5.1.1. Domain Layer

Dentro del dominio de User Account, se encuentran entidades clave como User, Subscription, Notification, y UserRole. Estas entidades desempeñan un papel fundamental en la gestión del ciclo de vida de las cuentas de usuario, suscripciones y roles, permitiendo que los usuarios interactúen de manera efectiva con la plataforma, ya sea a través de la creación de cuentas, la suscripción a servicios, o la gestión de sus permisos y notificaciones. En este dominio, el User es el agregado principal, ya que encapsula la lógica de negocio central relacionada con la administración de cuentas de usuario, controlando la activación de cuentas, validación de credenciales y asignación de roles. A continuación, se describen los objetos y entidades relacionados con este dominio.

![Descripción de la imagen](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/51.png?raw=true)

### 5.1.2. Interface Layer

En esta sección, presentamos la **Capa de Interfaz** de nuestro sistema de gestión de cuentas de usuario, que actúa como punto de entrada para las interacciones con los usuarios. Está compuesta por controladores que gestionan las solicitudes y envían las respuestas adecuadas, permitiendo una comunicación eficiente entre la plataforma y los usuarios.

Los controladores principales son: **UserController**, **SubscriptionController**, **NotificationController**, y **RoleController**. Cada uno maneja operaciones específicas: gestión de usuarios, suscripciones, notificaciones y roles, respectivamente.

**UserController:** Gestiona la creación, activación, desactivación de cuentas, cambio de contraseñas, y asignación de roles.

**SubscriptionController:** Gestiona la activación, renovación y cancelación de suscripciones de usuarios.

**NotificationController:** Envía y programa notificaciones en función de eventos clave del sistema.

**RoleController:** Maneja la asignación, actualización y eliminación de roles de usuario.

![Descripción de la imagen 52](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/52.png?raw=true)

### 5.1.3. Application Layer

En esta sección, presentamos la Capa de Aplicación (Application Layer) dentro del contexto del enfoque de diseño Domain-Driven Design (DDD) para el sistema de gestión de cuentas de usuario. La Capa de Aplicación es responsable de coordinar las acciones y el flujo de datos entre la Capa de Dominio y la Capa de Infraestructura, actuando como intermediario y gestionando las interacciones entre estas capas. Esta capa garantiza que la lógica de negocio representada en la Capa de Dominio se ejecute de manera eficiente y coherente.

La Capa de Aplicación se compone de Application Services, Command Handlers y Event Handlers. Los Command Handlers gestionan las operaciones de escritura, como la creación, actualización o eliminación de usuarios y suscripciones. Los Event Handlers procesan los eventos que ocurren en el sistema, como el envío de notificaciones al usuario o cambios en sus suscripciones.

A continuación se describen los principales Command Handlers del sistema:
![Descripción de la imagen 53](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/53.png?raw=true)

### 5.1.4. Infrastructure Layer

En esta sección, presentamos la Capa de Infraestructura (Infrastructure Layer) dentro del contexto del enfoque de diseño Domain-Driven Design (DDD) para el bounded context User Account Management. La Capa de Infraestructura es responsable de proporcionar los componentes técnicos y de soporte necesarios para que las otras capas del sistema funcionen correctamente. Esta capa incluye la implementación de repositorios, servicios que se conectan con sistemas externos, y otros componentes de infraestructura, como la configuración de bases de datos.

Los repositorios en la Capa de Infraestructura implementan las interfaces definidas en la Capa de Dominio y se encargan de la persistencia y gestión de datos. En este sistema, utilizamos repositorios basados en tecnologías como JPA para manejar la interacción con la base de datos. Entre los repositorios clave se encuentran el UserRepositoryImpl, que gestiona la información de los usuarios; el SubscriptionRepositoryImpl, encargado de las suscripciones de los usuarios; y el NotificationRepositoryImpl, que gestiona las notificaciones enviadas a los usuarios.

Además, la Capa de Infraestructura incluye servicios que interactúan con sistemas externos y proporcionan funcionalidades adicionales para la plataforma. El NotificationServiceImpl es uno de estos servicios clave, ya que maneja el envío y la programación de notificaciones para eventos importantes, como la entrada a un museo o la finalización de una mejora de foto. Otro componente esencial es el EmailServiceImpl, que facilita el envío de correos electrónicos a los usuarios, permitiendo notificaciones y confirmaciones relacionadas con sus cuentas.

Finalmente, se incluye la configuración de la base de datos a través del componente DatabaseConfig, que define los detalles técnicos para la conexión y gestión de la persistencia de datos en la plataforma. Esto asegura que las operaciones relacionadas con usuarios, suscripciones y notificaciones se manejen de forma eficiente y segura

![Descripción de la imagen 54](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/54.png?raw=true)

### 5.1.6. Bounded Context Software Architecture Component Level Diagrams

En esta sección, presentamos los Diagramas de Componentes a nivel de Arquitectura de Software del bounded context User Account Management. Estos diagramas proporcionan una visión general de cómo los diferentes componentes interactúan entre sí en el contexto de la gestión de usuarios, suscripciones y notificaciones, tanto para aplicaciones móviles como para sistemas externos.

Las aplicaciones móviles y los sistemas externos interactúan con la plataforma a través de una serie de controladores que manejan las peticiones entrantes y devuelven las respuestas adecuadas. Los controladores clave incluyen UserController, SubscriptionController, NotificationController y RoleController, cada uno encargado de gestionar operaciones específicas como la creación de usuarios, manejo de suscripciones, envío de notificaciones y asignación de roles.

Cada controlador se comunica con sus correspondientes Application Services, que implementan la lógica de negocio y coordinan las operaciones con los Repositories para la persistencia de datos. Los Repositories, a su vez, gestionan el almacenamiento de información de usuarios, suscripciones y notificaciones, interactuando con la base de datos central.

![Descripción de la imagen 55](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/55.png?raw=true)

### 5.1.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.X.7.1. Bounded Context Domain Layer Class Diagrams

Estos diagramas, específicamente modelan la capa de dominio dentro de un bounded context particular en DDD. Estos diagramas están diseñados para proporcionar una vista estructurada del modelo de dominio y cómo se organiza y se relaciona dentro de los límites del contexto delimitado. Son herramientas valiosas para asegurar que el equipo de desarrollo tenga una comprensión común y precisa de cómo se implementará la lógica de negocio en el código, y cómo cada parte del dominio interactúa dentro del contexto acotado.

![Descripción de la imagen 56](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/56.png?raw=true)

#### 5.1.7.2. Bounded Context Database Design Diagram

Es una representación gráfica que muestra cómo se organiza la base de datos en relación con un "Bounded Context" en el Diseño Guiado por el Dominio (DDD). Este tipo de diagrama se enfoca en los aspectos de almacenamiento de datos de un modelo de dominio particular y cómo los datos son estructurados y manejados dentro de los límites de un contexto específico.

![Descripción de la imagen 57](https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/57.png?raw=true)

## 5.2. Bounded Context: Image Recognition

El dominio de Image recognition se enfoca en la interacción con el servicio de reconocimiento de imágenes creado en Tensorflow y la gestión del ciclo de vida de las restauraciones recibidas.

### 5.2.1. Domain Layer

En la capa de dominio, se identificaron las Entities, Value Objects, Aggregates, Factories y Domain Services necesarios para el funcionamiento del Bounded context.

#### Entities

| Nombre      | RawImage                                                                                                                                                         |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Representa la imagen que el usuario escanea o carga antes de ser reconocida por el sistema. Contiene metadatos como la ubicación, fecha, y calidad de la imagen. |

| Nombre      | RecognizedImage                                                                                                                          |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Clase que representa la imagen que ha sido procesada y reconocida mediante IA, con detalles sobre la obra de arte u objeto identificado. |

| Nombre      | RecognitionProcess                                                                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Controla el ciclo de vida del proceso de reconocimiento, incluyendo los diferentes estados: iniciado, en proceso, completado, errores y notificaciones. |

#### Value Objects

| Nombre      | RecognitionType                                                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Valor que indica si el proceso de reconocimiento es automático o requiere intervención manual para la confirmación de los resultados. |

| Nombre      | RecognitionSettings                                                                                                   |
| ----------- | --------------------------------------------------------------------------------------------------------------------- |
| Descripción | Configuraciones aplicadas al proceso de reconocimiento, como la precisión del algoritmo o el tiempo de procesamiento. |

| Nombre      | ErrorNotification                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------ |
| Descripción | Notificación generada en caso de que haya algún problema técnico durante el proceso de reconocimiento. |

| Nombre      | RecognitionMetadata                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| Descripción | Metadatos asociados con la imagen antes del reconocimiento, como la ubicación, formato de archivo, y tamaño. |

#### Aggregates

| Nombre      | ImageRecognitionAggregate                                                                                                                                            |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Descripción | Responsable de gestionar las acciones relacionadas con el reconocimiento de imágenes, como la selección de parámetros del reconocimiento, notificaciones, y ajustes. |

#### Factories

<table class="tg"><thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky">ImageFactory</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" rowspan="2">Methods</td>
    <td class="tg-0pky">createRawImage(filePath: string, user: User): RawImage  <br></td>
  </tr>
  <tr>
    <td class="tg-0lax">createRecognizedImage(rawImage: RawImage, recognitionProcess: RecognitionProcess): RecognizedImage</td>
  </tr>
</tbody>
</table>

<table class="tg"><thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky">RecognitionProcessFactory</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky">Methods</td>
    <td class="tg-0pky">createRecognitionProcess(rawImage: RawImage, settings: RecognitionSettings): RecognitionProcess</td>
  </tr>
</tbody>
</table>

#### Domain Services

<table class="tg"><thead>
  <tr>
    <th class="tg-0pky">Nombre</th>
    <th class="tg-0pky">ImageRecognitionService</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky">Dependencies</td>
    <td class="tg-0pky">AITensorflowService</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="3">Methods</td>
    <td class="tg-0lax">recognizeImage(rawImage: RawImage, settings: RecognitionSettings): RecognitionProcess: Invoca el AIService para enviar la imagen y procesarla usando TensorFlow, luego utiliza el resultado para completar el proceso de reconocimiento.</td>
  </tr>
  <tr>
    <td class="tg-0lax">optimizeRecognition(rawImage: RawImage): RecognitionSettings</td>
  </tr>
  <tr>
    <td class="tg-0lax">validateRecognitionFeasibility(rawImage: RawImage): boolean</td>
  </tr>
</tbody>
</table>

### 5.2.2. Interface Layer

#### Controllers

<table><thead>
  <tr>
    <th>Nombre</th>
    <th>ImageRecognitionController</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Description</td>
    <td>Controlador que permite al usuario interactuar con el proceso de reconocimiento.</td>
  </tr>
  <tr>
    <td rowspan="5">Methods</td>
    <td>selectRecognitionType(): Selección del tipo de reconocimiento.</td>
  </tr>
  <tr>
    <td>applyManualRecognition(): Iniciar reconocimiento manual.</td>
  </tr>
  <tr>
    <td>applyAutomaticRecognition(): Iniciar reconocimiento automático.</td>
  </tr>
  <tr>
    <td>finalizeRecognition(): Finalizar el proceso de reconocimiento.</td>
  </tr>
  <tr>
    <td>undoRedoAction(): Rehacer o deshacer acciones de reconocimiento.</td>
  </tr>
</tbody>
</table>

##### Endpoints planteados:

- POST /api/images/upload
- GET /api/images/{id}
- POST /api/images/{id}/recognize
- GET /api/recognitions/{id}
- PUT /api/recognitions/{id}/pause
- PUT /api/recognitions/{id}/resume
- PUT /api/recognitions/{id}/cancel
- GET /api/recognized-images/{id}
- GET /api/raw-images/{id}/recognized-versions

### 5.2.3. Application Layer

#### Command Handlers

| Nombre       | ImageRecognitionController        |
| ------------ | --------------------------------- |
| Dependencies | IRawImageRepository, ImageFactory |
| Method       | handle(UploadRawImageCommand)     |

| Nombre       | InitiateRecognitionCommandHandler                                                                                                                                                       |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dependencies | IRecognitionProcessRepository, RecognitionProcessFactory, ImageRecognitionService                                                                                                       |
| Method       | handle(InitiateRecognitionCommand): Este comando invoca el proceso de reconocimiento llamando al ImageRecognitionService, que a su vez invoca el AIService para el procesamiento de IA. |

| Nombre       | PauseRecognitionCommandHandler  |
| ------------ | ------------------------------- |
| Dependencies | IRecognitionProcessRepository   |
| Method       | handle(PauseRecognitionCommand) |

| Nombre       | ResumeRecognitionCommandHandler  |
| ------------ | -------------------------------- |
| Dependencies | IRecognitionProcessRepository    |
| Method       | handle(ResumeRecognitionCommand) |

| Nombre       | CancelRecognitionCommandHandler  |
| ------------ | -------------------------------- |
| Dependencies | IRecognitionProcessRepository    |
| Method       | handle(CancelRecognitionCommand) |

| Nombre       | SaveRecognitionCommandHandler  |
| ------------ | ------------------------------ |
| Dependencies | IRecognitionProcessRepository  |
| Method       | handle(SaveRecognitionCommand) |

#### Event Handlers

| Nombre           | RecognitionProcessStartedEventHandler |
| ---------------- | ------------------------------------- |
| Dependencies     | handle(RecognitionProcessStarted)     |
| Responsibilities | Update UI, send notifications         |

| Nombre           | RecognitionProcessCompletedEventHandler                |
| ---------------- | ------------------------------------------------------ |
| Dependencies     | handle(RecognitionProcessCompleted)                    |
| Responsibilities | Update UI, send notifications, trigger post-processing |

| Nombre           | RecognitionProcessFailedEventHandler      |
| ---------------- | ----------------------------------------- |
| Dependencies     | handle(RecognitionProcessFailed)          |
| Responsibilities | Update UI, send notifications, log errors |

### 5.2.4. Infrastructure Layer

#### Repositories Implementations

<table><thead>
  <tr>
    <th>Nombre</th>
    <th>RawImageRepository</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Implements</td>
    <td>IRawImageRepository</td>
  </tr>
  <tr>
    <td>Dependencies</td>
    <td>Database context or ORM</td>
  </tr>
  <tr>
    <td rowspan="4">Methods</td>
    <td>save(rawImage: RawImage): void</td>
  </tr>
  <tr>
    <td>getById(id: UUID): RawImage</td>
  </tr>
  <tr>
    <td>getByUserId(userId: UUID): RawImage[]</td>
  </tr>
  <tr>
    <td>delete(id: UUID): void</td>
  </tr>
</tbody>
</table>

<table><thead>
  <tr>
    <th>Nombre</th>
    <th>RecognizedImageRepository</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Implements</td>
    <td>IRecognizedImageRepository</td>
  </tr>
  <tr>
    <td>Dependencies</td>
    <td>Database context or ORM</td>
  </tr>
  <tr>
    <td rowspan="4">Methods</td>
    <td>save(recognizedImage: RecognizedImage): void</td>
  </tr>
  <tr>
    <td>getById(id: UUID): RecognizedImage</td>
  </tr>
  <tr>
    <td>getByOriginalImageId(originalImageId: UUID): RecognizedImage[]</td>
  </tr>
  <tr>
    <td>delete(id: UUID): void</td>
  </tr>
</tbody>
</table>

<table><thead>
  <tr>
    <th>Nombre</th>
    <th>RecognitionProcessRepository</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Implements</td>
    <td>IRecognitionProcessRepository</td>
  </tr>
  <tr>
    <td>Dependencies</td>
    <td>Database context or ORM</td>
  </tr>
  <tr>
    <td rowspan="4">Methods</td>
    <td>save(recognitionProcess: RecognitionProcess): void</td>
  </tr>
  <tr>
    <td>getById(id: UUID): RecognitionProcess</td>
  </tr>
  <tr>
    <td>getByStatus(status: RecognitionStatus): RecognitionProcess[]</td>
  </tr>
  <tr>
    <td>updateStatus(id: UUID, status: RecognitionStatus): void</td>
  </tr>
</tbody>
</table>

### 5.2.6. Bounded Context Software Architecture Component Level Diagrams

[![Bounded-Context-Software-Architecture-Component-Level-Diagrams.png](https://i.postimg.cc/Ls0rVZR8/Bounded-Context-Software-Architecture-Component-Level-Diagrams.png)](https://postimg.cc/JyZ6r0Gf)

### 5.2.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.2.7.1. Bounded Context Domain Layer Class Diagrams

[![Arch-code-lvl-diagram.png](https://i.postimg.cc/L8QCdKWy/Arch-code-lvl-diagram.png)](https://postimg.cc/BjDcDy4D)

#### 5.2.7.2. Bounded Context Database Design Diagram

[![databs-diagram.png](https://i.postimg.cc/8P1tjzQK/databs-diagram.png)](https://postimg.cc/c6bQzZJw)

## 5.3. Bounded Context: Image Restauration

Se centra en la interacción con el servicio de restauración de imágenes creado en Tensorflow.

### 5.3.1. Domain Layer

#### Entities

- **RawImage**  
  Clase que representa la imagen tal como fue cargada por el usuario, incluyendo sus metadatos y características sin restaurar.

- **RestoredImage**  
  Clase que representa la imagen que ha sido ajustada mediante los procesos de restauración, ya sea automáticamente o con intervención manual.

- **RestorationProcess**  
  Clase que controla el ciclo de vida del proceso de restauración, representando los diferentes estados del proceso, como la restauración iniciada, errores, notificaciones, ajustes y finalización.

- **User**  
  Clase que representa al usuario que carga imágenes y utiliza las funciones de restauración.

#### Value Objects

- **RestorationType**  
  Valor que indica si el proceso de restauración es completamente automático o incluye intervención manual del usuario.

- **RestorationSettings**  
  Configuraciones aplicadas a la restauración, como potencia, contraste y tonalidad.

- **ErrorNotification**  
  Notificación que se genera en caso de un problema técnico durante la restauración.

- **RestorationHistory**  
  Mantiene un registro de todas las versiones restauradas de una imagen.

- **ImageMetadata**  
  Información relacionada con los metadatos de la imagen.

- **ComparisonResult**  
  Resultado de la comparación entre imágenes.

- **ImageDifference**  
  Diferencias encontradas entre imágenes.

#### Aggregates

- **ImageRestorationAggregate**  
  Responsable de gestionar las acciones del proceso de restauración, como la selección del tipo de restauración (manual o automática), los ajustes y las notificaciones.

##### Raíz:

- **RestorationProcess**

##### Entidades:

- **RawImage**, **RestoredImage**

##### Value Objects:

- **RestorationSettings**, **ComparisonResult**

#### Factories

- **ImageFactory**

  - **Métodos:**
    - `createRawImage(filePath: string, user: User): RawImage`
    - `createRestoredImage(rawImage: RawImage, restorationProcess: RestorationProcess): RestoredImage`

- **RestorationProcessFactory**
  - **Métodos:**
    - `createRestorationProcess(rawImage: RawImage, settings: RestorationSettings): RestorationProcess`

#### Domain Services

- **ImageRestorationService**

  - **Métodos:**
    - `restoreImage(rawImage: RawImage, settings: RestorationSettings): RestorationProcess`
    - `optimizeRestoration(rawImage: RawImage): RestorationSettings`
    - `validateRestorationFeasibility(rawImage: RawImage): boolean`

- **ImageComparisonService**

  - **Métodos:**
    - `compareImages(rawImage: RawImage, restoredImage: RestoredImage): ComparisonResult`
    - `analyzeDifferences(comparisonResult: ComparisonResult): ImageAnalysis`

- **RestorationQualityService**
  - **Métodos:**
    - `assessRestorationQuality(restoredImage: RestoredImage): QualityScore`
    - `suggestImprovements(restoredImage: RestoredImage): RestorationSuggestions`

#### Repository Interfaces

- **IRawImageRepository**

  - **Métodos:**
    - `save(rawImage: RawImage): void`
    - `getById(id: UUID): RawImage`
    - `getByUserId(userId: UUID): RawImage[]`
    - `delete(id: UUID): void`

- **IRestoredImageRepository**

  - **Métodos:**
    - `save(restoredImage: RestoredImage): void`
    - `getById(id: UUID): RestoredImage`
    - `getByOriginalImageId(originalImageId: UUID): RestoredImage[]`
    - `delete(id: UUID): void`

- **IRestorationProcessRepository**
  - **Métodos:**
    - `save(restorationProcess: RestorationProcess): void`
    - `getById(id: UUID): RestorationProcess`
    - `getByStatus(status: RestorationStatus): RestorationProcess[]`
    - `updateStatus(id: UUID, status: RestorationStatus): void`

### 5.3.2. Interface Layer

Controllers a tomar en cuenta

##### ImageRestorationController

Controlador que permite al usuario interactuar con el proceso de restauración.

###### Métodos:

- `selectRestorationType()`: Selección del tipo de restauración.
- `applyManualRestoration()`: Iniciar restauración manual.
- `applyAutomaticRestoration()`: Iniciar restauración automática.
- `finalizeRestoration()`: Finalizar el proceso de restauración.
- `undoRedoAction()`: Rehacer o deshacer acciones de edición.

##### ImageUploadController

###### Endpoints:

- `POST /api/images/upload`
- `GET /api/images/{id}`

#### ImageRestorationController

##### Endpoints:

- `POST /api/images/{id}/restore`
- `GET /api/restorations/{id}`
- `PUT /api/restorations/{id}/pause`
- `PUT /api/restorations/{id}/resume`
- `PUT /api/restorations/{id}/cancel`

##### RestoredImageController

###### Endpoints:

- `GET /api/restored-images/{id}`
- `GET /api/raw-images/{id}/restored-versions`

##### ImageComparisonController

###### Endpoints:

- `GET /api/images/{rawId}/compare/{restoredId}`
- `POST /api/images/side-by-side-comparison`

#### Presenters

##### ImagePresenter

###### Métodos:

- `presentRawImage(RawImage): RawImageViewModel`
- `presentRestorationOptions(RawImage): RestorationOptionsViewModel`

##### RestorationProcessPresenter

###### Métodos:

- `presentRestorationStatus(RestorationProcess): RestorationStatusViewModel`
- `presentRestorationProgress(RestorationProcess): RestorationProgressViewModel`

##### RestoredImagePresenter

###### Métodos:

- `presentRestoredImage(RestoredImage): RestoredImageViewModel`
- `presentComparisonResult(ComparisonResult): ComparisonResultViewModel`

#### View Models

##### RawImageViewModel

###### Properties:

- `id`
- `url`
- `thumbnailUrl`
- `metadata`
- `uploadedAt`

##### RestorationOptionsViewModel

###### Properties:

- `availableAlgorithms`
- `qualityLevels`
- `applicableFilters`

##### RestorationStatusViewModel

###### Properties:

- `id`
- `status`
- `progress`
- `estimatedTimeRemaining`

##### RestoredImageViewModel

###### Properties:

- `id`
- `url`
- `thumbnailUrl`
- `originalImageId`
- `restorationDetails`

##### ComparisonResultViewModel

###### Properties:

- `rawImageUrl`
- `restoredImageUrl`
- `sideBySideUrl`
- `similarityScore`
- `highlightedDifferences`

### 5.3.3. Application Layer

#### Command Handlers

##### UploadRawImageCommandHandler

- **Dependencies:**
  - `IRawImageRepository`
  - `ImageFactory`
- **Method:**
  - `handle(UploadRawImageCommand)`

##### InitiateRestorationCommandHandler

- **Dependencies:**
  - `IRestorationProcessRepository`
  - `RestorationProcessFactory`
  - `ImageRestorationService`
- **Method:**
  - `handle(InitiateRestorationCommand)`

##### PauseRestorationCommandHandler

- **Dependencies:**
  - `IRestorationProcessRepository`
- **Method:**
  - `handle(PauseRestorationCommand)`

##### ResumeRestorationCommandHandler

- **Dependencies:**
  - `IRestorationProcessRepository`
- **Method:**
  - `handle(ResumeRestorationCommand)`

##### CancelRestorationCommandHandler

- **Dependencies:**
  - `IRestorationProcessRepository`
- **Method:**
  - `handle(CancelRestorationCommand)`

##### SaveRestorationCommandHandler

- **Dependencies:**
  - `IRestorationProcessRepository`
- **Method:**
  - `handle(SaveRestorationCommand)`

#### Event Handlers

##### RestorationProcessStartedEventHandler

- **Method:**
  - `handle(RestorationProcessStarted)`
- **Responsibilities:**
  - Update UI
  - Send notifications

##### RestorationProcessCompletedEventHandler

- **Method:**
  - `handle(RestorationProcessCompleted)`
- **Responsibilities:**
  - Update UI
  - Send notifications
  - Trigger post-processing

##### RestorationProcessFailedEventHandler

- **Method:**
  - `handle(RestorationProcessFailed)`
- **Responsibilities:**
  - Update UI
  - Send notifications
  - Log errors

### 5.3.4. Infrastructure Layer

La Infrastructure Layer es responsable de la persistencia de los datos, la integración con servicios externos, y la interacción con bases de datos. Aquí se implementan los repositorios que permiten la recuperación y el almacenamiento de las entidades del dominio.

##### Repository Implementations

###### RawImageRepository (implements IRawImageRepository)

- **Dependencies:**
  - Database context or ORM
- **Methods:**
  - `save(rawImage: RawImage): void`
  - `getById(id: UUID): RawImage`
  - `getByUserId(userId: UUID): RawImage[]`
  - `delete(id: UUID): void`

###### RestoredImageRepository (implements IRestoredImageRepository)

- **Dependencies:**
  - Database context or ORM
- **Methods:**
  - `save(restoredImage: RestoredImage): void`
  - `getById(id: UUID): RestoredImage`
  - `getByOriginalImageId(originalImageId: UUID): RestoredImage[]`
  - `delete(id: UUID): void`

###### RestorationProcessRepository (implements IRestorationProcessRepository)

- **Dependencies:**
  - Database context or ORM
- **Methods:**
  - `save(restorationProcess: RestorationProcess): void`
  - `getById(id: UUID): RestorationProcess`
  - `getByStatus(status: RestorationStatus): RestorationProcess[]`
  - `updateStatus(id: UUID, status: RestorationStatus): void`

##### Database Context

###### ImageRestorationDbContext

- **Entities:**
  - RawImage, RestoredImage, RestorationProcess, User
- **Methods:**
  - `SaveChanges(): void`
  - `BeginTransaction(): IDbContextTransaction`

##### File Storage

###### FileStorageService (implements IFileStorageService)

- **Dependencies:**
  - Cloud storage SDK (e.g., AWS S3, Azure Blob Storage)
- **Methods:**
  - `uploadFile(file: File, path: string): string`
  - `getFileUrl(path: string): string`
  - `deleteFile(path: string): void`

##### Image Processing

###### ImageProcessingService (implements IImageProcessingService)

- **Dependencies:**
  - Image processing library (e.g., OpenCV, Pillow)
- **Methods:**
  - `applyFilter(image: Image, filter: RestorationFilter): Image`
  - `resize(image: Image, dimensions: Dimensions): Image`
  - `convertFormat(image: Image, format: ImageFormat): Image`

###### AIRestorationService (implements IAIRestorationService)

- **Dependencies:**
  - AI/ML framework (e.g., TensorFlow, PyTorch)
- **Methods:**
  - `restoreImage(rawImage: RawImage, settings: RestorationSettings): RestoredImage`
  - `trainModel(dataset: ImageDataset): void`
  - `evaluateModel(testSet: ImageDataset): ModelPerformance`

##### Caching

###### CacheService (implements ICacheService)

- **Dependencies:**
  - Caching system (e.g., Redis, Memcached)
- **Methods:**
  - `set(key: string, value: any, expiration: number): void`
  - `get(key: string): any`
  - `delete(key: string): void`

##### Repositories

###### ImageRestorationRepository

- **Descripción:** Maneja el acceso y la persistencia de las imágenes restauradas, así como el historial de versiones.
- **Métodos principales:**
  - `saveRestoredImage():` Guarda una imagen restaurada en la base de datos.
  - `findOriginalImageById():` Recupera una imagen original antes de su restauración.
  - `findRestorationHistory():` Recupera el historial de restauraciones de una imagen específica.
  - `findUserByCredentials():` Recupera un usuario basado en sus credenciales de acceso.

### 5.3.6. Bounded Context Software Architecture Component Level Diagrams

<div class="container" style="text-align: center">
    <img src="https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/5.3.6.png?raw=true" width="200" alt="Bounded Context Software Architecture Component Level Diagrams">
</div>

### 5.3.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.3.7.1. Bounded Context Domain Layer Class Diagrams

<div class="container" style="text-align: center">
    <img src="https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/5.3.7.1.png?raw=true" width="200" alt="Bounded Context Software Architecture Code Level Diagrams">
</div>

#### 5.3.7.2. Bounded Context Database Design Diagram

<div class="container" style="text-align: center">
    <img src="https://github.com/ImagIA-2024-02/Report/blob/main/Recursos/imagenes/5.3.7.2.png?raw=true" width="200" alt="Bounded Context Software Architecture Code Level Diagrams">
</div>

## 5.X. Bounded Context: \<Bounded Context Name\>

### 5.X.1. Domain Layer

### 5.X.2. Interface Layer

### 5.X.3. Application Layer

### 5.X.4. Infrastructure Layer

### 5.X.6. Bounded Context Software Architecture Component Level Diagrams

### 5.X.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.X.7.1. Bounded Context Domain Layer Class Diagrams

#### 5.X.7.2. Bounded Context Database Design Diagram
