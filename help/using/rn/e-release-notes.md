---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 3f38c4a48bc1ae55e285209ce33a0ebc9ecc4dcb
workflow-type: tm+mt
source-wordcount: 1658
ht-degree: 10%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece continuamente nuevas funciones, mejoras en las funciones existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de junio de 2026 {#june-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios están activos en la producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante. Consulte la Fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 16 y 17 de junio de 2026


### Recorridos {#june-26-journeys}

Las siguientes funcionalidades y mejoras están llegando a los recorridos en esta versión.

* **Aumento del límite de recorridos activos y nuevas protecciones**: ahora puede tener hasta **200 recorridos activos**, más que el límite anterior de 100.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">Vincular a tarea DOCAC JIRA</a>

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido activo, ahora aparecen en el **encabezado del recorrido** junto al distintivo del estado activo. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">Vincular a tarea DOCAC JIRA</a>

* **Detener o cerrar un recorrido pausado directamente** - Ahora puede **detener un recorrido o cerrarlo a nuevas entradas** directamente desde el estado **Pausado**. Anteriormente, un recorrido pausado tenía que reanudarse a Activo antes de que se pudiera detener o cerrar.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">Vincular a tarea DOCAC JIRA</a>

<!--
* **Supplemental identifier support for external audiences** - Supplemental identifiers in journeys are now supported for external audiences, including audiences imported from a CSV file and audiences created with Federated Audience Composition. You can designate any non-identity attribute or non-person identity attribute from the audience as the supplemental ID, no schema labeling is required.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14541">Link to DOCAC JIRA task</a>
-->

### Campañas orquestadas {#june-26-oc}

Las siguientes funcionalidades y mejoras están llegando a las campañas orquestadas en esta versión.

<table>
<thead>
<tr>
<th><strong>Actividad de carga de archivos en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten la carga de un <strong>archivo CSV o TXT</strong> directamente en el lienzo de campaña como audiencia de segmentación, sin ingerir primero el archivo en Adobe Experience Platform. Los datos del archivo se consumen en el momento de la ejecución y no persisten como un conjunto de datos de Adobe Experience Platform. Durante la configuración del archivo, puede definir asignaciones de columnas, tipos de datos, control de valores NULL y directivas de error por columna. Esto admite campañas de envíos específicos o de listas de socios en las que no es práctico crear una canalización de ingesta completa.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Personalización basada en bucles para datos relacionales en campañas orquestadas**: el editor de personalización ahora admite un **bloque de bucles** que se repite en colecciones relacionales, como pedidos, cuentas o reservas, y procesa un bloque de contenido por registro en un solo correo electrónico o SMS. Las colecciones se configuran mediante el selector de datos utilizando tokens de personalización, sin necesidad de escribir expresiones.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">Vincular a tarea DOCAC JIRA</a>

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña**: las campañas organizadas ahora admiten la personalización de **campos de encabezado de correo electrónico**, incluidos el nombre del remitente, la dirección del remitente y la respuesta a, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer en el nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">Vincular a tarea DOCAC JIRA</a>

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">Link to DOCAC JIRA task</a>
-->

### Toma de decisiones {#june-26-decisioning}

La siguiente funcionalidad llega a Decisioning en esta versión.

<table>
<thead>
<tr>
<th><strong>Aprovechamiento del fragmento de contenido de Adobe Experience Manager en Decisioning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede asignar <strong>fragmentos de contenido de Adobe Experience Manager</strong> a <strong>elementos de decisión</strong> en la toma de decisiones y aprovecharlos dentro de las directivas de decisión para entregar el fragmento adecuado al cliente correcto en el momento adecuado.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Canales {#june-26-channels}

En esta versión se introduce la siguiente funcionalidad.

<table>
<thead>
<tr>
<th><strong>Canales salientes personalizados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora presenta <strong>Canales personalizados</strong>, una nueva funcionalidad que permite a los administradores traer cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente a Journey Optimizer a través de un generador de canales sin código.</p>
<p>Una vez configurados, los canales personalizados están disponibles en todas las campañas, recorridos y campañas orquestadas, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza. Esto llena el vacío que antes subsanaban las acciones personalizadas, que se limitaban a los recorridos y carecían de creación de contenido dedicada.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Correo electrónico {#june-26-email}

Las siguientes funcionalidades y mejoras están llegando al canal de correo electrónico en esta versión.

<!--
<table>
<thead>
<tr>
<th><strong>Advanced Components</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Email Designer now includes a library of ready-to-use layout components — such as Headers, Product Cards (1, 2, or 3 columns), Information blocks, and Footers — that you can drag and drop directly into your email canvas. Each component comes pre-configured with editable properties (image, title, text, button, links) and can be fully customized through the WYSIWYG interface, speeding up email creation without requiring you to build structures from scratch.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Comprobación de contenido en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora permite a los usuarios validar su <strong>calidad del contenido del correo electrónico</strong>, incluida la legibilidad, la eficacia y la coherencia del contenido, directamente en la interfaz de Designer de correo electrónico.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activar reducción de tamaño de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta nueva opción permite <strong>reducir el tamaño del HTML</strong> en un mensaje de correo electrónico eliminando espacio en blanco, comentarios y código redundante innecesarios, sin cambiar el aspecto del correo electrónico. Esto ayuda a mejorar la capacidad de entrega (algunos proveedores de correo electrónico rechazan o marcan correos electrónicos de gran tamaño) y puede acelerar el tiempo de carga de los destinatarios.</p>
<p>Fecha de disponibilidad: 10 de junio de 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Texto enriquecido en campos editables para fragmentos**: Ahora puede agregar texto enriquecido a los fragmentos personalizables que se utilizan en el contenido de los correos electrónicos. Por ejemplo, al utilizar el componente Texto como campo editable en el Designer de correo electrónico, puede dar formato directamente al contenido (por ejemplo, negrita y cursiva) e insertar hipervínculos.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14715">Vincular a tarea DOCAC JIRA</a>

<!--
* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment. When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered — both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">Link to DOCAC JIRA task</a>
-->

### Mensajería móvil (SMS, MMS, RCS y LINE) {#june-26-mobile}

Las siguientes mejoras se incluyen en la mensajería móvil en esta versión.

* **Clics únicos para informes de SMS**: Se ha introducido un nuevo módulo de **Clics únicos** en los informes de SMS, que trae el mismo nivel de seguimiento granular de rendimiento a los SMS disponibles actualmente para los informes de correo electrónico.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">Vincular a tarea DOCAC JIRA</a>

* **Canal LINE - Creación de cambios** - La interfaz de usuario del canal LINE se ha actualizado con funciones avanzadas de creación de mensajes. Esta versión incorpora compatibilidad con **varios formatos de mensaje**, incluidos Texto, Imagen, Mapa de imágenes, Carrusel y Flex (Editor JSON), además de vistas previas de dispositivos en tiempo real. Los usuarios ahora pueden administrar mensajes agrupados de hasta cinco mensajes ordenados (con controles de adición, eliminación y reordenación) y aprovechar el editor de personalización integrado para mensajes validados y dinámicos.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">Vincular a tarea DOCAC JIRA</a>

* **SMS - Mostrar métricas de uso** - Para los clientes que compran SMS directamente a través de Adobe Journey Optimizer, se ha introducido un nuevo **panel de uso de SMS**. Ahora puede ver y rastrear las métricas de envío de mensajes de los últimos 90 días, clasificadas por mensajes móviles originados (MO) y móviles terminados (MT). Estos datos también están disponibles para su descarga a través de CSV, lo que proporciona una mayor visibilidad y control sobre la inversión en SMS.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">Vincular a tarea DOCAC JIRA</a>

### Contenido e integraciones {#june-26-content}

En esta versión se incluyen las siguientes funcionalidades y mejoras para la administración de contenido y las integraciones.

<table>
<thead>
<tr>
<th><strong>Mejoras en los fragmentos de contenido de Adobe Experience Manager en Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versión incorpora varias mejoras para que <strong>Fragmentos de contenido de Adobe Experience Manager</strong> sean más utilizables, controlables y estén más listos para la producción dentro de los flujos de trabajo de creación de Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ahora admite la captura de fragmentos de contenido desde varias configuraciones de Adobe Experience Manager, incluidos los niveles de creación, publicación y publicación autenticada.</li>
<li>Una vez seleccionado un fragmento, su contexto se conserva en todo el mensaje, lo que permite a los autores reutilizar los campos de fragmento en bloques de contenido sin volver a seleccionar.</li>
<li>Se ha introducido una nueva página de lista de fragmentos de contenido en Journey Optimizer para mejorar la administración del ciclo vital; los usuarios pueden identificar fragmentos no sincronizados y sincronizar manualmente el déclencheur para mantenerse al día.</li>
<li>La compatibilidad con la configuración regional y las variaciones ahora permite a los especialistas en marketing trabajar con versiones alternativas del mismo fragmento de contenido de forma más deliberada.</li>
<li>Ahora tiene flexibilidad en la forma en que Adobe Journey Optimizer accede al contenido de Adobe Experience Manager. Esta versión incluye la capacidad de <strong>cambiar el repositorio de origen</strong> para los fragmentos de contenido utilizados en sus recorridos y campañas.</li>
<li>Ahora compatible con <b>Managed Services</b>, puede ver, acceder y usar fragmentos de contenido de Adobe Experience Manager directamente en Journey Optimizer para personalización. Simplemente agregue la URL del repositorio de Adobe Experience Manager Managed Services en los ajustes de configuración como una configuración única.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">Vincular a tarea DOCAC JIRA</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14821">Vincular a tarea DOCAC JIRA</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración del asistente de IA con Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El asistente de IA ahora recupera automáticamente <b>imágenes aprobadas por la marca</b> directamente de su Adobe Experience Manager Assets al generar correos electrónicos, páginas web y notificaciones push. Esto elimina la necesidad de buscar manualmente en Assets o confiar en las retrospectivas de IA genéricas, lo que garantiza que cada imagen sea perfectamente precisa y compatible con la marca.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14761">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Campañas {#june-26-campaigns}

Las siguientes mejoras se implementan en las campañas de esta versión.

* **Anular el campo de ejecución predeterminado en las campañas**: disponible anteriormente en el nivel de recorrido, ahora puede anular el **campo de ejecución predeterminado** establecido globalmente para sus envíos de correo electrónico, SMS y WhatsApp en los parámetros de campaña.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">Vincular a tarea DOCAC JIRA</a>

### Creación de informes {#june-26-reporting}

En esta versión se incluyen las siguientes mejoras en los informes.

* **Nuevas métricas estimadas de clics para los informes de correo electrónico y SMS**: para proporcionar una vista más precisa de la participación real de los clientes, ahora hay nuevas métricas estimadas disponibles en los informes Recorridos, Campañas y Canales. Estas métricas ayudan a filtrar las interacciones no humanas (NHI) y los clics de bots a partir de los datos de los informes:
   * Clics estimados: el total de clics se cuenta después de eliminar el tráfico de bots y no humanos identificados.
   * Estimated CTR: clics estimados en relación con las entregas totales.
   * Estimated CTOR for email only: Clics estimados en relación con las aperturas estimadas.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">Vincular a tarea DOCAC JIRA</a>

### Configuración {#june-26-configuration}

Las siguientes mejoras se incluyen en la configuración y administración de esta versión.

* **Listas blancas de IP de Firewall de aplicaciones web (WAF)**: Adobe Journey Optimizer ahora admite la lista blanca de IP de WAF para páginas de aterrizaje, lo que permite a las organizaciones exigir que todas las solicitudes entrantes se enruten exclusivamente a través de su infraestructura de WAF configurada. Con esta mejora, los clientes pueden configurar Journey Optimizer para que rechace cualquier solicitud directa que omita el nivel de WAF, lo que garantiza que las políticas de seguridad definidas en herramientas como Imperva se apliquen de forma coherente. Esta capacidad refuerza la postura de seguridad de las empresas con requisitos estrictos de acceso a la red, lo que les permite un control total del flujo de tráfico a sus páginas de aterrizaje alojadas en Journey Optimizer.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">Vincular a tarea DOCAC JIRA</a>

* **Proceso OTP del bucle de comentarios para subdominios personalizados**: el proceso de configuración del subdominio personalizado del bucle de comentarios (FBL) se ha mejorado al mostrar el centro de remitentes de Yahoo **Contraseña única (OTP)** directamente en la interfaz de usuario del producto. Los usuarios ahora pueden recuperar y mostrar automáticamente el OTP generado durante la verificación de propiedad del dominio del centro de remitentes de Yahoo.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">Vincular a tarea DOCAC JIRA</a>

* **Se han actualizado los análisis de rendimiento de entrega por lotes con escenarios orientados al cliente**. Los análisis de rendimiento de entrega por lotes de Adobe Journey Optimizer se han actualizado para reflejar el rendimiento de nivel de producción en varios escenarios de personalización, desde envíos básicos hasta contenido dinámico complejo con lógica condicional. Las métricas actualizadas ahora están disponibles en la descripción del producto para ayudar a los clientes a planificar con precisión sus volúmenes de mensajería.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">Vincular a tarea DOCAC JIRA</a>

* **Conjunto de datos que se mueve de flujo a modo por lotes** - El conjunto de datos de evento de comentarios de mensajes de AJO está pasando de flujo a **modo de ingesta por lotes**. Este cambio garantiza que la ingesta de datos no supere los límites de ingesta de transmisión. Si utiliza este conjunto de datos en informes de Customer Journey Analytics o ejecuta consultas en él, espere un aumento de la latencia de datos de hasta dos horas en adelante.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">Vincular a tarea DOCAC JIRA</a>

### Mejoras de uso {#june-26-usability}

La siguiente mejora de uso se publicará en esta versión.

* **Carpetas para Recorridos y campañas**: ahora puede organizar sus recorridos y campañas en **carpetas** para mejorar la navegación y la administración en la interfaz.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Vincular a tarea DOCAC JIRA</a>

