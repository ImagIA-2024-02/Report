# Capítulo IV: Strategic-Level Software Design
## 4.1. Strategic-Level Attribute-Driven Design.
### 4.1.1. Design Purpose.
El propósito del diseño es facilitar a los usuarios el acceso a la restauración de arte o documentos históricos a través de una aplicación móvil con secuencia intuitiva y sencilla que sea y se vea confiable además de entretenida. Además, el uso de inteligencia artificial debe ser sobreentendido haciendo uso de elementos de diseño.
### 4.1.2. Attribute-Driven Design Inputs.
Esta sección aborda los tres tipos de inputs fundamentales para el proceso de diseño utilizando ADD: la Funcionalidad Principal, los Escenarios de Atributos de Calidad y las Restricciones. Cada uno de estos elementos se describe en detalle, proporcionando la base sobre la cual se construye la arquitectura de la solución.
#### 4.1.2.1. Primary Functionality (Primary User Stories).
En esta sección se especifica los Epics o User stories que tienen mayor relevancia en términos de requisitos funcionales y que tienen impacto sobre la arquitectura de la solución (landing page y aplicación móvil).  
| Epic / UserStory ID | Título                                                           | Descripción                                                                                                                                                                                           | Criterios de Aceptación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Relacionado con (Epic ID) |
|---------------------|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| US01                | Redirección de la Landing Page a tiendas de apps                 | Como visitante de cualquier segmento, deseo dirigirme a la aplicación móvil correspondiente para descargarla en mi dispositivo móvil                                                                  | Scenario 1: Aplicación publicada en Google Play Dado que el visitante de cualquier segmento se encuentra en la vista principal de la landing page Cuando el visitante selecciona descargar la aplicación para Android Entonces el visitante es redirigido a la página de descarga de la aplicación en Google Play   Scenario 2: Aplicación publicada en App Store Dado que el visitante de cualquier segmento se encuentra en la vista principal de la landing page Cuando el visitante selecciona descargar la aplicación para iOS Entonces el visitante es redirigido a la página de descarga de la aplicación en la App Store de iOS   Scenario 3: Aplicación no publicada en las tiendas digitales Dado que el visitante se encuentra en la vista principal de la landing page Y la aplicación no se encuentra publicada  Cuando el visitante selecciona descargar la aplicación  Entonces es redirigido a la página principal de la respectiva tienda                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                           |
| US03                | Envío de mensaje a través de un formulario de contacto           | El sistema debe ofrecer un formulario de contacto que permita a los visitantes de cualquier segmento enviar mensajes a los desarrolladores para sugerencias, quejas, o cualquier otro propósito.      | Scenario 1: Enviar el formulario con los campos correctamentes llenados Dado que el visitante ha completado los campos de nombre,apellido,correo electrónico y mensaje correctamente Cuando los campos son validados Y el visitante ordena enviar el formulario Entonces el formulario es enviado correctamente al correo electrónico   Scenario 2: Enviar el formulario con un correo electrónico no válido Dado El visitante se encuentra en el formulario de contacto Y ingresa un formato de coreo electrónico no válido Cuando el correo electrónico es revisado Y el visitante ordena enviar el formulario Entonces el formulario no es enviado Y se le muestra un mensaje de error indicando que el correo electrónico no es válido   Scenario 3: Envío fallido por campos incompletos en el formulario Dado que el visitante se encuentra en la sección de contacto de la landing page Cuando el visitante completa parcialmente los campos requeridos en el formulario de contacto Y ordena enviar el formulario Entonces se muestra un mensaje de error indicando los campos que aún necesitan ser completados   Scenario 4: Envío del formulario con información vacía Dado que el visitante se encuentra en la sección de contacto de la landing page Cuando el visitante deja en blanco uno o más campos del formulario de contacto Y ordena enviar el formulario Entonces se muestra un mensaje de error indicando que debe rellenar los campos vacíos |                           |
| US04                | Sección de Preguntas Frecuentes                                  | Como visitante, deseo acceder a la sección de Preguntas Frecuentes para resolver mis inquietudes sobre el servicio ofrecido.                                                                          | Scenario 1: Navegación a la sección de Preguntas Frecuentes Dado que el visitante se encuentra en la página principal de la Landing Page Cuando el visitante se desplaza hasta la sección de Preguntas Frecuentes Entonces el visitante encuentra la sección de Preguntas Frecuentes.   Scenario 2: Acceso a preguntas y respuestas específicas Dado que el visitante se encuentra en la sección de Preguntas Frecuentes Cuando el visitante selecciona una pregunta de la lista Entonces se despliega la respuesta correspondiente de manera clara y concisa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |                           |
| US05                | Navegación y Contenido Informativo en el Footer                  | Como visitante, deseo tener acceso fácil y claro a información relevante y enlaces útiles en el footer para acceder rápidamente a secciones importantes de la Landing Page.                           | Scenario 1: Acceso a información relevante en el footer Dado que el visitante se encuentra en cualquier página del sitio web Cuando el visitante desplaza hacia abajo hasta el footer Entonces el visitante encuentra información relevante y enlaces útiles claramente organizados y visibles.   Scenario 2: Enlaces a secciones importantes en el footer Dado que el visitante está en el footer Cuando el visitante busca enlaces a secciones importantes como "Inicio", "Nosotros" y "Contacto" Entonces el visitante encuentra estos enlaces de forma clara y directa.   Scenario 3: Acceso rápido a redes sociales Dado que el visitante está en el footer del sitio web Cuando el visitante selecciona algún ícono de las redes sociales disponibles Entonces el visitante es redirigido a la red social elegida                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                           |
| US10                | Detección automática de entrada al museo                         | Como visitante, quiero que la aplicación detecte automáticamente cuando entro a un museo participante para activar las funciones relevantes.                                                          | Scenario 1: Detección exitosa Dado que tengo la aplicación instalada y el GPS activado Cuando entro en un museo participante Entonces la aplicación me notifica y activa el modo museo   Scenario 2: Activación manual Dado que estoy en un museo pero la detección automática falla Cuando selecciono manualmente el museo en la aplicación Entonces se activan las funciones del modo museo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                           |
| US11                | Escaneo y reconocimiento de obras de arte                        | Como visitante del museo, quiero poder escanear obras de arte con mi dispositivo para obtener información adicional y ver restauraciones digitales.                                                   | Scenario 1: Escaneo exitoso Dado que estoy frente a una obra de arte en el museo Cuando enfoco la cámara de mi dispositivo hacia la obra Entonces la aplicación reconoce la obra y muestra opciones de interacción   Scenario 2: Obra no reconocida Dado que estoy escaneando una obra Cuando la aplicación no puede reconocerla Entonces se me ofrece la opción de buscar manualmente o reportar el problema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                           |
| US12                | Visualización de restauración digital                            | Como visitante, quiero ver una versión restaurada digitalmente de la obra de arte que estoy observando para apreciar cómo se veía originalmente.                                                      | Scenario 1: Visualización de restauración Dado que he escaneado una obra de arte Cuando selecciono la opción "Ver restauración" Entonces se muestra en mi pantalla una versión restaurada digitalmente de la obra   Scenario 2: Comparación antes/después Dado que estoy viendo una restauración digital Cuando uso el control deslizante en la pantalla Entonces puedo comparar dinámicamente la versión actual con la restaurada                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                           |
| US13                | Gamificación de la experiencia museística                        | Como visitante, quiero ganar puntos y logros por explorar el museo y completar desafíos para hacer mi visita más entretenida.                                                                         | Scenario 1: Obtención de puntos Dado que he escaneado una obra de arte Cuando completo la visualización de su información y restauración Entonces recibo puntos que se añaden a mi perfil   Scenario 2: Desbloqueo de logro Dado que he completado un conjunto específico de acciones en el museo Cuando alcanzo el objetivo de un logro Entonces recibo una notificación y se desbloquea una insignia en mi perfil                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |                           |
| US14                | Compartir experiencia en redes sociales                          | Como visitante, quiero compartir mi experiencia y las obras restauradas que he visto en mis redes sociales.                                                                                           | Scenario 1: Compartir obra restaurada Dado que estoy viendo una restauración digital Cuando selecciono la opción "Compartir" Entonces puedo elegir la red social y publicar la imagen con un mensaje predeterminado   Scenario 2: Compartir resumen de visita Dado que he completado mi visita al museo Cuando selecciono "Compartir resumen de visita" Entonces la aplicación genera una tarjeta virtual con estadísticas y obras destacadas de mi visita para compartir                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                           |
| US15                | Restauración automática de imágenes dañadas                      | Como usuario, deseo restaurar automáticamente imágenes dañadas utilizando algoritmos avanzados de machine learning, para mejorar la calidad de imágenes históricas sin necesidad de ajustes manuales. | Scenario 1: Restauración Exitosa  Dado que el usuario ha cargado una imagen dañada,  Cuando selecciona la opción de restauración automática,  Entonces la imagen es restaurada y se muestra el resultado final con una comparación visual.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                           |
| US16                | Ajuste automático de tonalidad para imágenes en B/N              | Como usuario, deseo ajustar automáticamente la tonalidad de imágenes en blanco y negro, para mejorar su aspecto visual de manera rápida y eficiente.                                                  | Scenario 1: Ajuste Tonal Exitoso  Dado que el usuario ha cargado una imagen en blanco y negro,  Cuando selecciona la opción de ajuste automático de tonalidad,  Entonces la tonalidad de la imagen es ajustada automáticamente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |                           |
| US17                | Interfaz de usuario intuitiva y fácil de navegar                 | Como usuario, deseo una interfaz intuitiva y fácil de navegar, para poder utilizar las funcionalidades de la aplicación de manera fluida y sin complicaciones técnicas.                               | Scenario 1: Navegación Exitosa  Dado que el usuario inicia sesión en la aplicación,  Cuando navega por las diferentes secciones,  Entonces encuentra todas las funcionalidades claramente organizadas y de fácil acceso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                           |
| US18                | Comparación lado a lado de imagen original y restaurada          | Como usuario, deseo comparar el estado original de una imagen con la versión restaurada, para evaluar la efectividad de la restauración antes de guardar los cambios                                  | Scenario 1: Comparación Exitosa  Dado que el usuario ha restaurado una imagen,  Cuando selecciona la opción de comparación lado a lado,  Entonces se muestra una vista comparativa clara entre la imagen original y la restaurada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                           |
| US19                | Optimización para imágenes extremadamente dañadas                | Como usuario, deseo optimizar la restauración de imágenes extremadamente dañadas, para obtener resultados de alta calidad incluso en fotografías severamente deterioradas                             | Scenario 1: Restauración Optimizada Exitosa  Dado que el usuario ha cargado una imagen severamente dañada,  Cuando selecciona la opción de optimización,  Entonces la imagen es restaurada con mayor detalle y precisión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                           |
| US20                | Historial de cambios con opciones de deshacer y rehacer acciones | Como usuario, deseo acceder a un historial de cambios con opciones de deshacer y rehacer, para gestionar mejor mi flujo de trabajo y corregir errores de manera eficiente.                            | Scenario 1: Deshacer/Rehacer Exitoso  Dado que el usuario ha realizado varios cambios en una imagen,  Cuando utiliza las opciones de deshacer o rehacer,  Entonces el sistema aplica los cambios solicitados sin afectar la calidad de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                           |
#### 4.1.2.2. Quality attribute Scenarios.
#### 4.1.2.3. Constraints.
### 4.1.3. Architectural Drivers Backlog.
### 4.1.4. Architectural Design Decisions.
### 4.1.5. Quality Attribute Scenario Refinements.
En este apartado se presentan refinamientos de los escenarios relacionados con los atributos de calidad más relevantes para el sistema de restauración de imágenes históricas. Estos escenarios ayudan a garantizar que el sistema cumpla con los requisitos clave de rendimiento, seguridad, usabilidad, disponibilidad y escalabilidad, proporcionando una experiencia de usuario robusta y eficiente, incluso bajo condiciones de uso intensivo. A continuación, se describen los escenarios refinados para cada atributo de calidad, con sus correspondientes estímulos, entornos, respuestas esperadas y medidas de desempeño.  
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky" colspan="3">Scenario Refinement for Scenario1</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" colspan="2">Scenario(s)</td>
    <td class="tg-0pky">Un usuario aplica la restauración automática a una imagen dañada de alta resolución (Performance)</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Business Goals</td>
    <td class="tg-0pky">Minimizar el tiempo de procesamiento para ofrecer una experiencia de usuario ágil y evitar la frustración por demoras en dispositivos móviles.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Relevant Quality Attributes</td>
    <td class="tg-0pky">Rendimiento en la restauración de imágenes de alta resolución en dispositivos móviles con recursos limitados.</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">Scenario Components</td>
    <td class="tg-0pky">Stimulus</td>
    <td class="tg-0pky">Un usuario selecciona una imagen de alta resolución y aplica la restauración automática.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Stimulus Source</td>
    <td class="tg-0pky">Usuario utilizando un dispositivo móvil con capacidades limitadas.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Environment</td>
    <td class="tg-0pky">Dispositivo móvil con CPU y memoria limitados.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Artifact (if Known)</td>
    <td class="tg-0pky">Algoritmo de restauración de imágenes.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response</td>
    <td class="tg-0pky">La imagen se restaura en menos de 5 segundos, proporcionando resultados inmediatos.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response Measure</td>
    <td class="tg-0pky">El tiempo de procesamiento medido en segundos no debe exceder los 5 segundos en el 95% de los casos.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Questions</td>
    <td class="tg-0pky">¿Cómo optimiza el sistema el uso de CPU y memoria en dispositivos móviles de gama baja?</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Issues</td>
    <td class="tg-0pky">Necesidad de ajustar el algoritmo de restauración para que funcione eficientemente en hardware con recursos limitados sin sacrificar la calidad de la restauración.</td>
  </tr>
</tbody></table>  

<table class="tg"><thead>
  <tr>
    <th class="tg-0pky" colspan="3">Scenario Refinement for Scenario 2</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" colspan="2">Scenario(s)</td>
    <td class="tg-0pky">Un usuario almacena imágenes restauradas en la nube desde la aplicación (Security)</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Business Goals</td>
    <td class="tg-0pky">Proteger la privacidad y seguridad de las imágenes restauradas durante su almacenamiento en la nube.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Relevant Quality Attributes</td>
    <td class="tg-0pky">Seguridad en la transmisión y almacenamiento de datos en la nube.</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">Scenario Components</td>
    <td class="tg-0pky">Stimulus</td>
    <td class="tg-0pky">El usuario selecciona la opción de guardar imágenes restauradas en la nube.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Stimulus Source</td>
    <td class="tg-0pky">Usuario utilizando una red pública Wi-Fi.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Environment</td>
    <td class="tg-0pky">Red pública de Internet (Wi-Fi) sin cifrado.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Artifact (if Known)</td>
    <td class="tg-0pky">Servicio de almacenamiento en la nube.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response</td>
    <td class="tg-0pky">Los datos deben ser cifrados localmente antes de ser transmitidos a la nube.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response Measure</td>
    <td class="tg-0pky">Protocolo de cifrado (e.g., AES-256) utilizado y longitud de clave verificada antes de la transmisión.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Questions</td>
    <td class="tg-0pky">¿Qué medidas de seguridad adicionales se implementan para proteger los datos almacenados en la nube?</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Issues</td>
    <td class="tg-0pky">Garantizar que el cifrado no degrade el rendimiento de la aplicación ni sobrecargue los recursos del dispositivo.</td>
  </tr>
</tbody></table>  
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky" colspan="3">Scenario Refinement for Scenario 3</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" colspan="2">Scenario(s)</td>
    <td class="tg-0pky">Un usuario nuevo accede por primera vez a la funcionalidad de restauración de imágenes (Usability)</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Business Goals</td>
    <td class="tg-0pky">Maximizar la facilidad de uso para que nuevos usuarios puedan realizar restauraciones sin complicaciones.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Relevant Quality Attributes</td>
    <td class="tg-0pky">Usabilidad e intuitividad de la interfaz de usuario.</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">Scenario Components</td>
    <td class="tg-0pky">Stimulus</td>
    <td class="tg-0pky">Un usuario sin experiencia previa intenta usar la funcionalidad de restauración.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Stimulus Source</td>
    <td class="tg-0pky">Usuario nuevo que accede a la aplicación por primera vez.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Environment</td>
    <td class="tg-0pky">Usuario final interactuando con la interfaz de restauración en un dispositivo móvil.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Artifact (if Known)</td>
    <td class="tg-0pky">Interfaz de usuario.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response</td>
    <td class="tg-0pky">El usuario debe poder completar una restauración básica sin ayuda externa en menos de 3 minutos.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response Measure</td>
    <td class="tg-0pky">Tiempo promedio requerido para completar una restauración básica sin consultar documentación externa.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Questions</td>
    <td class="tg-0pky">¿Qué pasos de onboarding y tutoriales se ofrecen para guiar a los nuevos usuarios?</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Issues</td>
    <td class="tg-0pky">Necesidad de diseñar una interfaz suficientemente intuitiva para minimizar la curva de aprendizaje.</td>
  </tr>
</tbody></table>  
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky" colspan="3">Scenario Refinement for Scenario 4</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" colspan="2">Scenario(s)</td>
    <td class="tg-0pky">Un usuario intenta acceder a la aplicación en cualquier momento del día (Availability)</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Business Goals</td>
    <td class="tg-0pky">Asegurar que la aplicación esté disponible en todo momento para maximizar la satisfacción del usuario.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Relevant Quality Attributes</td>
    <td class="tg-0pky">Disponibilidad del sistema durante todo el ciclo de uso.</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">Scenario Components</td>
    <td class="tg-0pky">Stimulus</td>
    <td class="tg-0pky">Usuario accede a la aplicación desde su dispositivo móvil.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Stimulus Source</td>
    <td class="tg-0pky">Usuario conectado a Internet a través de un dispositivo móvil.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Environment</td>
    <td class="tg-0pky">Dispositivo móvil con conexión a Internet.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Artifact (if Known)</td>
    <td class="tg-0pky">Sistema de aplicación móvil y backend.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response</td>
    <td class="tg-0pky">La aplicación debe estar disponible el 99.9% del tiempo durante un período de 12 meses.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response Measure</td>
    <td class="tg-0pky">Tiempo de inactividad anual debe ser inferior a 8.76 horas.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Questions</td>
    <td class="tg-0pky">¿Qué estrategias de redundancia se han implementado para reducir el tiempo de inactividad?</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Issues</td>
    <td class="tg-0pky">Asegurar que las actualizaciones y el mantenimiento no afecten la disponibilidad.</td>
  </tr>
</tbody></table>  
<table class="tg"><thead>
  <tr>
    <th class="tg-0pky" colspan="3">Scenario Refinement for Scenario 5</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-0pky" colspan="2">Scenario(s)</td>
    <td class="tg-0pky">Aumento en el número de usuarios concurrentes que aplican restauraciones de imágenes durante un evento promocional (Scalability)</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Business Goals</td>
    <td class="tg-0pky">Garantizar que la aplicación pueda manejar un aumento súbito de tráfico sin degradar la experiencia del usuario.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Relevant Quality Attributes</td>
    <td class="tg-0pky">Escalabilidad del sistema para soportar picos de tráfico.</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">Scenario Components</td>
    <td class="tg-0pky">Stimulus</td>
    <td class="tg-0pky">Aumento en usuarios concurrentes durante un evento promocional.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Stimulus Source</td>
    <td class="tg-0pky">Usuario accediendo a la plataforma durante un evento de alta demanda.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Environment</td>
    <td class="tg-0pky">Sistema backend sometido a una carga elevada de usuarios.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Artifact (if Known)</td>
    <td class="tg-0pky">Servidor backend y base de datos.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response</td>
    <td class="tg-0pky">La aplicación debe soportar un aumento del 200% en la carga de usuarios sin una degradación significativa en el rendimiento.</td>
  </tr>
  <tr>
    <td class="tg-0pky">Response Measure</td>
    <td class="tg-0pky">La tasa de respuesta y éxito de las operaciones debe mantenerse por encima del 95% bajo carga máxima.</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Questions</td>
    <td class="tg-0pky">¿Cómo se maneja la distribución de carga en los servidores durante picos de tráfico?</td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="2">Issues</td>
    <td class="tg-0pky">Implementación de soluciones de escalado automático para manejar picos de tráfico sin afectar el rendimiento.</td>
  </tr>
</tbody></table>
## 4.2. Strategic-Level Domain-Driven Design.
### 4.2.1. EventStorming.
### 4.2.2. Candidate Context Discovery.
### 4.2.3. Domain Message Flows Modeling.
### 4.2.4. Bounded Context Canvases.
### 4.2.5. Context Mapping.
## 4.3. Software Architecture.
### 4.3.1. Software Architecture System Landscape Diagram.
### 4.3.1. Software Architecture Context Level Diagrams.
### 4.3.2. Software Architecture Container Level Diagrams.
### 4.3.3. Software Architecture Deployment Diagrams.
