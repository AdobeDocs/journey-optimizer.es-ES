---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c998adc41e5696cc24bb7c640ec330ccfefa139a
workflow-type: tm+mt
source-wordcount: 3073
ht-degree: 17%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos. Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

>[!NOTE]
>
>Las funcionalidades enumeradas en estas notas de la versión incluyen una **fecha de disponibilidad** que indica cuándo se puede acceder a cada cambio en su entorno. Se esperan entradas en los acordeones de **Próximamente** en los próximos días o semanas. La información de estas secciones está sujeta a cambios.

## Notas de la versión de mayo de 2026 {#may-26-rn}

### Recorridos {#may-26-journeys}

En esta versión se han añadido las siguientes funciones y mejoras a los recorridos de. También se esperan cambios adicionales en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Fragmentos de recorrido (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear <strong>fragmentos de Recorrido</strong> en Adobe Journey Optimizer. Los fragmentos de recorrido son conjuntos reutilizables de nodos de recorrido que puede generar una vez y soltarlos en cualquier recorrido de la zona protegida. Ya sea una comprobación de elegibilidad, una lógica de enrutamiento de canal preferida o una secuencia de bienvenida, los fragmentos ayudan a los equipos a moverse más rápido y a mantenerse consistentes, sin reconstruir la misma lógica desde cero cada vez.</p>
<p>Una vez creados, los fragmentos se almacenan en un <strong>inventario de fragmentos</strong> específico y se pueden insertar en cualquier recorrido mediante la actividad <strong>fragmentos de Recorrido</strong>.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-fragments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 13 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de recorrido (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer su recorrido en <strong>Simulación</strong>. Este modo le permite validar su lógica usando <strong>usuarios simulados</strong>. Son perfiles temporales creados específicamente para la simulación, lo que le permite realizar pruebas libremente sin necesidad de administrar perfiles de prueba persistentes en Adobe Experience Platform.</p>
<p>Esta capacidad está disponible para todos los clientes como disponibilidad limitada con funciones esenciales.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/simulate-journey.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 5 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Próximamente — **La información siguiente está sujeta a cambios.**

Se esperan las siguientes capacidades de recorrido en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Optimización de ruta de recorrido: segmentación (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use el nuevo nodo <strong>Optimizar</strong> para segmentar audiencias específicas y determinar la mejor ruta para cumplir con los KPI centrados en la empresa.</p>
<p>Esta herramienta le permite desarrollar campañas de marketing más efectivas que tengan más probabilidades de interesar en el nivel 1:1, mejorar los esfuerzos de personalización de marketing para los clientes y mejorar los KPI de participación del cliente esencial, como las conversiones y los ingresos.</p>
<p>Esta capacidad, que antes estaba disponible en disponibilidad limitada, ya está disponible en todos los entornos.</p>
<p>Fecha de disponibilidad: 1 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recorrido Arbitration - fórmulas de clasificación (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar fórmulas para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de atributos de perfil del cliente y factores contextuales, lo que garantiza que los clientes ingresen los recorridos más relevantes.</p>
<p>Esta capacidad, que antes estaba disponible en disponibilidad limitada, ya está disponible en todos los entornos.</p>
<p>Fecha de disponibilidad: 1 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Asistente de IA para expresiones de Recorrido (Beta público)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El asistente de IA ahora funciona en el editor de expresiones avanzadas de recorrido para convertir las peticiones de datos en lenguaje natural en expresiones válidas y lógica condicional. Describa la expresión que desea crear y el Asistente para IA genera un código listo para usar que puede aplicar inmediatamente o perfeccionar mediante mensajes de seguimiento.</p>
<p>Esta capacidad está disponible para todos los clientes como un Beta público.</p>
<!--<p><img src="assets/do-not-localize/expression-assistant.gif"></p>-->
<p>Fecha de disponibilidad: 2 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de recorrido (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lanzada anteriormente en disponibilidad limitada, la simulación de Recorrido ya está disponible para todos los entornos. Con esta versión de General Availability, ahora puede utilizar Journey Agent para generar usuarios y eventos simulados directamente en el menú Simulation.</p>
<p>Fecha de disponibilidad: principios de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Finalización automática para recorridos de audiencia de lectura no recurrentes** - Los recorridos de **audiencia de lectura** no recurrentes ahora pasan automáticamente al estado **Detenido** una vez que se cierra el último perfil activo. Anteriormente, estas recorridos permanecían **Activas** hasta que expiró el tiempo de espera global de 91 días, incluso cuando ya no circulaba ningún perfil por ellas. Con esta mejora, el estado de recorrido refleja el estado de ejecución real en cuanto se completa, lo que mantiene el inventario de recorrido preciso sin intervención manual.

  Tenga en cuenta que este comportamiento no se aplica a los recorridos que incluyen nodos que causan períodos de espera, como nodos de espera, nodos de reacción o transiciones activadas por eventos. Estos recorridos siguen estando sujetos al tiempo de espera global estándar de 91 días.

  Fecha de disponibilidad: 2 de junio de 2026

* **Autenticación personalizada basada en certificados en acciones personalizadas**: las acciones personalizadas ahora admiten la autenticación personalizada basada en certificados. Al agregar `subType: "certificateCredential"` a una configuración de autorización personalizada, Journey Optimizer utiliza el certificado administrado de Adobe para firmar una aserción de cliente JWT e intercambiarla por un token de acceso (no se requiere secreto de cliente). Diseñado para API empresariales que aplican la verificación de identidad basada en certificados, como Azure Entra ID.

  Fecha de disponibilidad: 2 de junio de 2026

* **Compatibilidad con identificadores adicionales para audiencias externas**. Ahora se admiten identificadores adicionales en recorridos para audiencias externas, incluidas audiencias importadas de un archivo CSV y audiencias creadas con Federated Audience Composition. Puede designar cualquier atributo que no sea de identidad o de identidad que no sea de persona de la audiencia como ID suplementario; no se requiere un etiquetado de esquema.

  Fecha de disponibilidad: 1 de junio de 2026

+++

### Campañas orquestadas {#may-26-oc}

En esta versión se han agregado las siguientes funcionalidades y mejoras a las campañas orquestadas. También se esperan cambios adicionales en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Campañas orquestadas encadenadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, las campañas orquestadas se pueden vincular activando una campaña orquestada directamente desde la <strong>actividad final</strong> de otra campaña orquestada.</p>
<p>Esto permite dividir la lógica de orquestación compleja en flujos más pequeños y reutilizables a los que se puede llamar desde varias campañas principales en lugar de reconstruirlos cada vez. La carga útil pasada en tiempo de ejecución está disponible para la segmentación y personalización en la campaña de flujo descendente, por lo que cada campaña vinculada se puede comportar según el contexto que reciba.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Agregar vínculos en la actividad de enriquecimiento**: la funcionalidad Agregar vínculo ya está disponible en la actividad de enriquecimiento para campañas orquestadas. Esto permite crear una relación directa entre los datos de la tabla de trabajo y las tablas de base de datos existentes.

  Fecha de disponibilidad: 20 de mayo de 2026

+++ Próximamente — **La información siguiente está sujeta a cambios.**

Se espera la siguiente capacidad de campaña orquestada en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Direccionamiento basado en archivos para campañas orquestadas (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten la carga de un archivo CSV o TXT directamente en el lienzo de campaña como audiencia de destino, sin ingerir primero el archivo en Adobe Experience Platform. Los datos del archivo se consumen en el momento de la ejecución y no persisten como un conjunto de datos de Adobe Experience Platform. Durante la configuración del archivo, puede definir asignaciones de columnas, tipos de datos, control de valores NULL y directivas de error por columna. Esto admite campañas de envíos específicos o de listas de socios en las que no es práctico crear una canalización de ingesta completa.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 1 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Personalización basada en bucles para datos relacionales**: el editor de personalización ahora admite un bloque de Bucle que se repite en colecciones relacionales, como pedidos, cuentas o reservas, y procesa un bloque de contenido por registro en un solo correo electrónico o SMS. Las colecciones se configuran mediante el selector de datos utilizando tokens de personalización, sin necesidad de escribir expresiones.

  Fecha de disponibilidad: principios de junio de 2026

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña**: las campañas organizadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos el nombre del remitente, la dirección del remitente y la respuesta a, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa.

  Los valores del encabezado se pueden establecer en el nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso.

  Fecha de disponibilidad: principios de junio de 2026

+++

### Campañas {#may-26-campaigns}

+++ Próximamente — **La información siguiente está sujeta a cambios.**

* **Alertas de cliente para eventos de ciclo vital de campañas**: las nuevas alertas del sistema ahora le notifican de eventos de ciclo vital clave para campañas activadas por acciones y API. Suscribirse en el nivel de zona protegida.

  Fecha de disponibilidad: 1 de junio de 2026

* **Anular el campo de ejecución predeterminado en las campañas**: antes disponible en el nivel de recorrido, ahora se puede anular el campo de ejecución predeterminado establecido globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de campaña.

  Fecha de disponibilidad: 1 de junio de 2026

+++

### Toma de decisiones {#may-26-decisioning}

En esta versión se han añadido las siguientes funcionalidades y mejoras a Decisioning. También se esperan cambios adicionales en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Optimización de IA de fórmula de decisiones y reglas de clasificación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] ahora utiliza IA para detectar reglas de Decisioning y fórmulas de clasificación que se pueden simplificar. En el inventario, aparece un indicador rojo en cualquier regla para la que la IA haya identificado una oportunidad de optimización. Al hacer clic en el indicador, se muestra la expresión original junto con la versión sugerida por IA. Desde allí, puede descargar un archivo para revisar cómo se evalúan los perfiles simulados en cada versión y confirmar que se comportan de forma idéntica. A continuación, reemplace la expresión por la optimizada.</p>
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Para obtener más información, consulte la <a href="../start/ai-features.md#decisioning-optimization">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 5 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Fragmentos de contenido de Adobe Experience Manager en Decisioning**: ahora puede asignar fragmentos de contenido de Adobe Experience Manager a elementos de decisión en Decisioning y aprovecharlos dentro de las directivas de decisión para entregar el fragmento adecuado al cliente correcto en el momento adecuado. [Más información](../integrations/aem-fragments.md#aem-decisioning)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

  Fecha de disponibilidad: 20 de mayo de 2026

* **Detalles de la directiva de decisión del resumen de campaña**: desde la página de resumen de la campaña, ahora puede revisar la estructura completa de cada directiva de decisión (incluidas las estrategias de selección, los elementos de decisión y las ofertas de reserva) sin duplicar ni editar la campaña. También puede copiar un resumen de JSON en el portapapeles para la resolución de problemas con el Soporte de Adobe o su equipo de ingeniería. [Más información](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

  Fecha de disponibilidad: 20 de mayo de 2026

* **API de flujo de trabajo de migración de decisiones**: se ha actualizado el contrato de API para crear análisis de dependencia y flujos de trabajo de migración: pase **`request-level`** como **parámetro de consulta** en la dirección URL de solicitud (`sandbox`, `offer` o `decision`). El nivel de solicitud ya no debe enviarse en el cuerpo de JSON. [Más información](../experience-decisioning/decisioning-migration-api.md)

  Fecha de disponibilidad: 6 de mayo de 2026

+++ Próximamente — **La información siguiente está sujeta a cambios.**

Se espera la siguiente capacidad de toma de decisiones en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Decisioning en el canal de correo directo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede agregar directivas de decisión a recorridos y campañas de correo directo. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de decisión para devolver dinámicamente el mejor contenido para cada miembro de la audiencia. La toma de decisiones por correo postal también admite casos de uso de toma de decisiones por lotes, lo que permite exportar los elementos de oferta correspondientes para cada perfil en una audiencia de Adobe Experience Platform determinada.</p>
<!--<p><img src="assets/do-not-localize/exd-dm.gif"></p>-->
<p>Fecha de disponibilidad: 1 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Canal de correo electrónico {#may-26-email}

En esta versión se han añadido las siguientes funcionalidades y mejoras al canal de correo electrónico. También se esperan cambios adicionales en los próximos días o semanas.

<table>
<thead>
<tr>
<th><strong>Vínculos profundos en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora es posible añadir vínculos profundos al contenido del correo electrónico mediante una opción específica en el Designer de correo electrónico. Esto garantiza que los usuarios sean llevados directamente al contenido correcto en la aplicación, en lugar de ser redirigidos a navegadores o tiendas de aplicaciones, preservando el contexto y la participación.</p>
<p>Tenga en cuenta que, aunque la opción Vínculo profundo está disponible para todos los clientes, los vínculos profundos solo funcionan si ha completado los pasos de configuración necesarios y de implementación de la aplicación móvil.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Para obtener más información, consulte la <a href="../email/deeplinks.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Restringir el salto de herencia en fragmentos**: al crear o editar un fragmento, ahora puede elegir si se puede modificar cuando se utiliza en correos electrónicos. Bloquear un fragmento garantiza que permanezca sincronizado en cualquier lugar donde aparezca, lo que evita ediciones locales que podrían romper los estándares de marca o los requisitos de cumplimiento. Esta configuración se puede actualizar más adelante y se aplicará a usos futuros. [Más información](../content-management/create-fragments.md#lock-visual-fragment)

  Fecha de disponibilidad: 21 de mayo de 2026

### Mensajería móvil (SMS, MMS y RCS) {#may-26-mobile}

En esta versión se han añadido las siguientes funciones y mejoras a la mensajería móvil.

<table>
<thead>
<tr>
<th><strong>Nuevo canal de mensajes móviles y mensajería RCS mejorada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los SMS, MMS y RCS ahora están unificados en una sola acción de <strong>Mensaje móvil</strong> en Adobe Journey Optimizer, lo que facilita la administración de todos los tipos de mensajes móviles desde un solo lugar. Como parte de esta actualización, ahora puede crear mensajes RCS de medios enriquecidos, incluidas imágenes, carruseles y acciones sugeridas, directamente en Journey Optimizer a través de una nueva experiencia de creación nativa.</p>
<p>Para obtener más información, consulte la <a href="../mobile/get-started-mobile.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Recuento de caracteres**: en Adobe Journey Optimizer, ahora puede usar el Recuento de caracteres para monitorizar la longitud de sus mensajes SMS en tiempo real. Le ayuda a ver cuándo se dividirá un mensaje en varios segmentos para administrar mejor el formato y evitar aumentos inesperados en los costes de envío. [Más información](../mobile/create-mobile-message.md)

* **Enlaces SMS a un conjunto de datos personalizado**: en **credenciales de la API de SMS**, enrute **SMS entrantes** a un **conjunto de datos de evento de experiencia personalizado con perfil habilitado** que seleccione en lugar de solo el conjunto de datos de seguimiento predeterminado. [Más información](../mobile/mobile-webhook.md)

* **Mejora de la interfaz de webhook**: al configurar los webhooks de SMS, la interfaz de usuario ahora incluye una guía de configuración integrada con ejemplos prácticos, lo que facilita la alineación de las cargas del proveedor y la resolución de problemas sin abandonar el flujo de configuración. [Más información](../mobile/mobile-webhook.md)

* **Vínculos profundos en el contenido de SMS**: Ahora es posible agregar vínculos profundos al contenido de SMS mediante la función de ayuda de URL. Esto garantiza que los destinatarios se dirijan directamente al contenido en la aplicación deseado, sin enrutarlos a través de un explorador web o una tienda de aplicaciones, siempre y cuando haya completado los pasos de configuración necesarios y la implementación de la aplicación móvil. [Más información](../email/deeplinks.md)

### Canal de WhatsApp {#may-26-whatsapp}

En esta versión se han añadido las siguientes mejoras al canal de WhatsApp.

* **Compatibilidad y seguimiento con botones WhatsApp**: Las plantillas de WhatsApp ahora admiten **respuesta rápida**, **Call to action - URL** y **Call to action - teléfono**, **No se admite copiar el código**. Journey Optimizer envía los botones admitidos y rastrea las interacciones junto con los demás informes de canal.

* **Datos de contexto del canal WhatsApp**: Journey Optimizer ahora captura datos de interacción adicionales devueltos por el canal WhatsApp y los almacena en el **conjunto de datos AJO EmailTrackingExperienceEvent** en el grupo de campos `whatsAppChannelContext`.

  +++ Los siguientes campos se capturan y se pueden usar para crear audiencias y analizar la participación de WhatsApp

   * **`messageType`** - tipo de mensaje de WhatsApp (por ejemplo: `templateBased`, `response`)
   * **`inboundMessage`** - Contenido de respuesta entrante (por ejemplo: `stop`, `start`, `subscribe`)
   * **`inboundNumber`** - Identificador de remitente donde se recibió el mensaje entrante
   * **`channelType`** - Categoría de canal (`Utility`, `Marketing` o `Promotional`)
   * **`profileNumber`** - Número de teléfono desde el cual se recibió el mensaje entrante
   * **`origTimestamp`**: marca de tiempo original de Meta/WhatsApp
   * **`status`** - Estado del envío que incluye comentarios estandarizados del proveedor (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` o `unknown`) y el mensaje de estado del proveedor sin procesar
   * **`reactionEvent`** - Contenido de la respuesta del usuario: emoji para reacciones o texto del mensaje para respuestas a un mensaje específico
   * **`reactionMessageID`**: ID del mensaje original al que se está respondiendo
   * **`reactionActionName`** - Tipo de acción de respuesta (`react`, `unreact` o `reply`)
   * **`interactiveSelectedTitle`** - Título seleccionado por el usuario de un mensaje interactivo de WhatsApp
   * **`interactiveType`** - Tipo de mensaje interactivo (`list reply`, `button reply` o `button`)
   * **`interactiveSelectedDescription`** - Descripción de la opción interactiva de WhatsApp seleccionada
   * **`interactiveSelectedID`**: ID de la opción seleccionada de WhatsApp

  +++

### Contenido e integraciones {#may-26-content}

En esta versión se han añadido las siguientes funciones y mejoras a la administración de contenido y a las integraciones.

<table>
<thead>
<tr>
<th><strong>Selector de Asesor de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora usa el <strong>selector de Asesor de contenido</strong>, un modal unificado para seleccionar fragmentos de contenido y Experience Manager Assets. El nuevo selector incluye:</p>
<ul>
<li><strong>Examinar, buscar y filtrar </strong>todos los recursos y fragmentos.</li>
<li><strong>Búsqueda semántica de IA</strong>: describa lo que necesita en un lenguaje sencillo, por ejemplo, "café en las montañas", para que aparezcan recursos relevantes para el contexto en función del significado y el contenido, no solo coincidencias de texto. También se admiten consultas multilingües.</li>
<li><strong>Carga breve</strong>: cargue una información de marketing para que aparezcan automáticamente los recursos que se alineen con el contexto de su campaña en función de su contenido y sus requisitos.</li>
<li><strong>representaciones de Dynamic Media</strong>: elija y aplique representaciones de imagen para los recursos dinámicos sin salir del selector.</li>
</ul>
<p>Para obtener más información, consulte la <a href="../integrations/aem-content-advisor.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 19 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integraciones</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La característica <b>Integraciones</b> le permite conectar fuentes de datos de terceros directamente a Adobe Journey Optimizer. Al simplificar la forma de extraer datos externos y <b>contenido maquetable</b>, esta característica facilita la entrega de mensajes dinámicos y personalizados en todos los canales.</p>
<p>Esta capacidad, que se lanzó anteriormente en beta, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../integrations/integrations.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de mayo de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Acceso a repositorios entre organizaciones en el Selector de recursos de Assets**: ahora puede seleccionar recursos sin problemas entre repositorios de varias organizaciones directamente desde el Selector de recursos de Adobe Experience Manager.

### Administración {#may-26-admin}

+++ Próximamente — **La información siguiente está sujeta a cambios.**

* **El conjunto de datos de evento de comentarios de mensajes que se mueve a la ingesta por lotes** - `AJO Message Feedback Event Dataset` está realizando una transición del flujo al modo de ingesta por lotes. Este cambio garantiza que la ingesta de datos no supere los límites de ingesta de transmisión. Si utiliza este conjunto de datos en informes de Customer Journey Analytics o ejecuta consultas en él, espere un aumento de la latencia de datos de hasta dos horas en adelante.

  Fecha de disponibilidad: 1 de junio de 2026

+++

### Creación de informes {#may-26-reporting}

+++ Próximamente — **La información siguiente está sujeta a cambios.**

* **Excluir clics de bots para informes de correo electrónico y SMS**: ahora hay disponibles nuevas métricas estimadas para filtrar las interacciones no humanas (bots) de los informes de correo electrónico y SMS. Estas incluyen las tasas de clics estimadas, las tasas de clics (CTR) y las tasas de clics hasta la apertura (CTOR), lo que proporciona una vista más precisa de la participación real del cliente. Las métricas existentes se mantienen sin cambios y estas nuevas métricas pueden utilizarse junto con los informes actuales para mejorar el análisis.

  Fecha de disponibilidad: 1 de junio de 2026

+++

### Mejoras de uso {#may-26-usability}

En mayo de 2026 también se publicaron las siguientes mejoras de uso.

#### Listas

* **Acciones en lotes**: ahora puede seleccionar varios elementos a la vez en las listas **Campañas**, **Fragmentos** y **Plantillas** y realizar operaciones en lotes desde una sola barra de acciones, lo que incluye agregar elementos a un paquete, moverlos a una carpeta, editar etiquetas, administrar el acceso y archivarlos o eliminarlos. [Más información](../start/search-filter-categorize.md#bulk-actions)

  ![](../start/assets/bulk-actions-campaigns.png)

* Ahora, las listas **Ordenar y cambiar el tamaño de las columnas** - **Campañas**, **Fragmentos** y **Plantillas** admiten la ordenación al hacer clic en cualquier encabezado de columna. En la vista de carpetas de Campañas, también está disponible la ordenación y el filtrado por **[!UICONTROL Prioridad]** y **[!UICONTROL Configuración del canal]**. También se puede cambiar el tamaño de los anchos de columna en las listas **Fragmentos** y **Plantillas**; arrastre el borde de la columna para que se ajuste a los datos que más le interesan. [Más información](../start/search-filter-categorize.md#filter-lists)

#### Creación de contenido

* **Edición de atributos de perfil en línea**: la edición de atributos de perfil en línea en el Designer de correo electrónico se publicó inicialmente en abril. Como parte de la versión de mayo, esta capacidad se ha desunido del asistente de IA y se ha ampliado al editor de canales push. [Más información](../personalization/personalize.md#inline-personalization)

  ![](../personalization/assets/inline-profile-attributes.png)

* **Información sobre la URL del vínculo en el editor de canales push**: cuando una URL de un vínculo o campo multimedia es demasiado larga para mostrarla, siempre aparece un icono de información sobre herramientas junto al campo; pase el ratón sobre él para ver la URL completa. [Más información](../push/design-push.md#on-click-behavior)

  ![](../rn/assets/do-not-localize/push-link-tooltip.png)

<!--
#### Simulation & Preview

* **Redesigned preview experience** - The content preview screen has been redesigned with a side-by-side layout that lets you compare how your content renders across multiple profiles at a glance, enabling quicker and more confident reviews before sending. [Learn more](../test-approve/simulate-sample-input.md#preview)

  ![](../test-approve/assets/simulation-preview-redesign.png)
-->

+++ Próximamente — **La información siguiente está sujeta a cambios.**

* **Carpetas para recorridos y campañas**: ahora puede organizar sus recorridos y campañas en carpetas para mejorar la navegación y la administración en la interfaz.

  Fecha de disponibilidad: 2 de junio de 2026

+++
