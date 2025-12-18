---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión de 2025
description: Notas de la versión de Journey Optimizer 2025
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: b7550b55327cb27e67cb914c340bdd08360d4490
workflow-type: tm+mt
source-wordcount: '7909'
ht-degree: 99%

---

# Notas de la versión de 2025 {#release-notes-2025}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzadas en 2025.


## Notas de la versión de septiembre de 2025 {#25-9-rn}

**Fecha de la versión**: 23-24 de septiembre de 2025

### Nuevas funciones {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator es un producto basado en inteligencia artificial diseñado para llevar sus experimentos al siguiente nivel. Creado para usuarios de Adobe Journey Optimizer y Adobe Target, unifica la administración de experimentos, ofrece perspectivas y oportunidades con tecnología de IA e introduce un nuevo agente de experimentación.</p>
<p>Esto es lo que puede esperar:</p>
<ul>
<li><strong>Inventario de experimentos unificado:</strong> vea, filtre y administre rápidamente todos los experimentos de Adobe Journey Optimizer y Adobe Target en un espacio de trabajo central.</li>
<li><strong>Perspectivas y oportunidades de experimentos de IA:</strong> vaya más allá de las lecturas estadísticas con perspectivas y recomendaciones impulsadas por GenAI. Ahora, cada experimento ofrece oportunidades procesables, junto con argumentos de apoyo, para que los equipos puedan decidir con mayor seguridad qué probar a continuación.</li>
<li>Soporte de <strong>Multi-Armed Bandit (MAB) en Journey Optimizer:</strong> maximice el impacto y reduzca el tráfico desperdiciado con experimentos de Multi-Armed Bandit. En lugar de dividir los públicos de manera uniforme, MAB asigna automáticamente a más visitantes a las variaciones con mejor rendimiento en tiempo real para que pueda ofrecer mejores experiencias a más clientes sin dejar de aprender lo que funciona.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/es/docs/experimentation-accelerator/using/overview">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ya está aquí Journey Agent.</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la tecnología de <a href="https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, Journey Agent está disponible en Journey Optimizer. Permite analizar los recorridos a través de una interfaz de lenguaje natural. El agente detecta conflictos de público o de programación y caídas de perfiles en un recorrido para ayudarle a tomar medidas para resolverlos. Pronto, usted será capaz de crear recorridos con apoyo agéntico.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo oscuro en el Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Diseñador de correo electrónico de Journey Optimizer ahora permite cambiar a la vista en modo oscuro, donde además puede definir configuraciones personalizadas específicas que se mostrarán solo para los destinatarios que lean sus correos electrónicos en modo oscuro.</p>
<p>Tenga en cuenta lo siguiente:</p>
<ul>
<li>El renderizado final del modo oscuro puede variar y depende del cliente de correo electrónico del destinatario.</li>
<li>No todos los clientes de correo electrónico admiten el modo oscuro personalizado. Además, algunos clientes de correo electrónico solo aplican su propio modo oscuro predeterminado a todos los correos electrónicos recibidos. En ambos casos, no se puede procesar la configuración personalizada que definió en el Diseñador de correo electrónico.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/dark-mode.md">documentación detallada</a>.</p>
 <p>Fecha de disponibilidad: 16 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimización de la ruta del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilice el nuevo nodo Optimizar para dirigirse a públicos específicos o ejecutar pruebas A/B para determinar la mejor ruta para satisfacer los KPI empresariales.</p>
<p>Esta herramienta le permite probar y variar, así como personalizar las comunicaciones, la secuencia y el tiempo para llegar mejor a sus clientes.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/optimize.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegación personalizada para subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además de la delegación completa y del método CNAME, ahora hay disponible un nuevo método de configuración de subdominios: el método de delegación personalizada, que le permite controlar y mantener por completo todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>Para obtener más información, consulte la <a href="../configuration/delegate-custom-subdomain.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización y la toma de decisiones</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta función, que se lanzó anteriormente en beta pública, ya está disponible en todos los entornos. Con esta versión, se han introducido las siguientes mejoras:</p>
<ul><li>Compatibilidad con la personalización de la búsqueda de conjuntos de datos en canales entrantes.</li>
<li>Ahora, la función de ayuda "datasetLookup" se puede utilizar dentro de los fragmentos de expresiones. Por ahora, esta capacidad está disponible para un conjunto limitado de clientes. Para obtener acceso, póngase en contacto con su representante de Adobe.</li>
<li>Una opción de la interfaz de gestión del conjunto de datos ahora le permite habilitar conjuntos de datos para la personalización de la búsqueda, sin tener que realizar una llamada API.</li>
<li>Monitorización mejorada para rastrear el estado de ingesta de datos y saber cuándo los conjuntos de datos están listos para la búsqueda.</li>
<li>Se han actualizado las directrices y protecciones de uso para garantizar un rendimiento y una fiabilidad óptimos.</li>
<li>Los conjuntos de datos de Adobe Experience Platform ahora se pueden aprovechar en las reglas de límite de Decisioning.</li></ul></p>
<p>Para obtener más información, consulte la <a href="../data/lookup-aep-data.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>


### Mejoras {#sept-25-9-improvements}

* **Compatibilidad con webhook para campañas activadas por API**\
  Las campañas activadas por API ahora admiten webhooks. Configure una URL de webhook para recibir actualizaciones del estado en tiempo real para cada mensaje, mejorando la observabilidad y permitiendo una monitorización y automatización sin problemas. [Más información](../configuration/feedback-webhooks.md)

  Fecha de disponibilidad: 29 de septiembre de 2025

* **Compatibilidad con mTLS para el canal SMS**
Al configurar un proveedor de SMS personalizado, ahora tiene la opción de habilitar la autenticación TLS mutua (mTLS), lo que requiere que tanto el cliente como el servidor confirmen mutuamente sus identidades antes de establecer una conexión segura. [Más información](../sms/sms-configuration-custom.md) - Fecha de disponibilidad: 23 de septiembre de 2025

* **Esquemas relacionales**\
  Ahora puede utilizar esquemas relacionales para cubrir sus necesidades de modelado relacional en campañas orquestadas. [Más información](../orchestrated/gs-schemas.md) - Fecha de disponibilidad: 23 de septiembre de 2025

* **Compatibilidad con la búsqueda de conjuntos de datos en recorridos**\
  La nueva actividad en recorridos, **Búsqueda de conjuntos de datos**, le permite recuperar dinámicamente datos de conjuntos de datos de registros de Adobe Experience Platform durante el tiempo de ejecución. Al utilizar esta capacidad, puede acceder a datos que podrían no estar en el perfil o en la carga útil del evento, lo que garantiza que sus interacciones con los clientes sean relevantes y oportunas. [Más información](../building-journeys/dataset-lookup.md) - Fecha de disponibilidad: 23 de septiembre de 2025

  Esta actividad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

* **Compatibilidad de redireccionamiento en acciones personalizadas de Recorrido**\
  Ahora se admiten redirecciones (302) en las Acciones personalizadas de recorrido. - Fecha de disponibilidad: 23 de septiembre de 2025

* **Alertas de monitorización de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que se produzca un error de configuración de canal usando la delegación de subdominio personalizada. [Más información](../reports/alerts.md#alert-channel-config-failure) - Fecha de disponibilidad: 23 de septiembre de 2025

* **Solicitudes de cancelación de suscripción de un clic**: hemos introducido mejoras que refuerzan aún más la administración de las solicitudes de cancelación de suscripción de un clic configuradas en Adobe Managed, lo que garantiza un procesamiento confiable y coherente. - Fecha de disponibilidad: 23 de septiembre de 2025

* **Ahora se admiten parámetros de cuerpo JSON anidados en la autenticación personalizada**\
  Al configurar la autenticación personalizada para una acción personalizada, ahora se admiten objetos JSON anidados (por ejemplo, subobjetos dentro de `bodyParams`). [Más información](../datasource/external-data-sources.md#custom-authentication-mode) - Fecha de disponibilidad: 18 de septiembre de 2025

* **Frecuencia de restricción de restablecimiento por hora**: ahora puede aplicar una restricción por hora a los conjuntos de reglas de canal. Esta función, que antes estaba disponible en disponibilidad limitada, ahora está disponible en todos los entornos y le permite elegir 1 hora (antes era 3 horas). [Más información](../conflict-prioritization/channel-capping.md) - Fecha de disponibilidad: 17 de septiembre de 2025

* **Simular variaciones de contenido para todos los canales entrantes**\
  Anteriormente solo disponible para los canales de correo electrónico, SMS y notificaciones push, la simulación de variaciones de contenido ahora también se aplica a todos los canales entrantes. [Más información](../test-approve/simulate-sample-input.md) - Fecha de disponibilidad: 17 de septiembre de 2025

* **Expresión para reglas de límite de Decisioning**: ahora puede crear sus propias expresiones para definir el umbral de una regla de límite para un elemento de decisión. [Más información](../experience-decisioning/items.md#capping) - Fecha de disponibilidad: 16 de septiembre de 2025

* **Compatibilidad con dominios dinámicos**: Journey Optimizer ahora admite la personalización completa o básica de direcciones URL para dominios predefinidos aceptados por Adobe. [Más información](../personalization/personalization-build-expressions.md#where) - Fecha de disponibilidad: 12 de septiembre de 2025

  Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes.

* **Webhooks**: esta versión incorpora las siguientes mejoras para webhooks al configurar un proveedor de SMS personalizado:

   * Ahora puede definir el propósito de su webhook, ya sea de entrada o de comentarios, según el tipo de datos que desee capturar. [Más información](../sms/sms-configuration-custom.md#webhook) - Fecha de disponibilidad: 23 de septiembre de 2025

   * La interfaz para configurar palabras clave se ha mejorado para facilitar la configuración. [Más información](../sms/sms-configuration-custom.md#webhook) - Fecha de disponibilidad: 23 de septiembre de 2025

* **SMS**

   * Al configurar un proveedor de SMS personalizado, ahora puede definir una palabra clave **predeterminada** que se usa cuando un SMS entrante contiene una palabra clave no reconocida. También puede crear palabras clave **personalizadas** para acciones específicas. [Más información](../sms/sms-configuration-custom.md) - Fecha de disponibilidad: 23 de septiembre de 2025

   * Ahora puede acceder a las respuestas de palabras clave de entrada no definidas enviadas mediante un mensaje SMS, incluidos los errores tipográficos, las palabras o las frases que no están definidos explícitamente en la configuración. Se almacenan en el conjunto de datos de **Evento de experiencia de seguimiento de correo electrónico de AJO**, en **InboundMessage** durante 13 meses. Solo está disponible con Sinch, Infobip y el proveedor de SMS personalizado. Fecha de disponibilidad: 23 de septiembre de 2025

## Notas de la versión de agosto de 2025 {#25-8-rn}

**Fecha de lanzamiento**: miércoles, 19 de agosto de 2025

### Nuevas funciones {#Aug-25-8-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede poner en pausa y reanudar los recorridos. Esta funcionalidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando están en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda el recorrido.</p>
<p>Puede poner en pausa y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar criterios de salida basados en atributos de perfil (anteriormente denominados “filtros globales”) a los recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-pause.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista de calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función incluye:</p>
<ul>
<li>Mejoras de diseño para la navegación en fechas,</li>
<li>La capacidad de ver borradores de campañas si ha establecido una fecha de inicio y de finalización,</li>
<li>Una nueva configuración para ocultar y mostrar los elementos de calendario que se ejecutan durante mucho tiempo.</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-ui.md#calendar">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Actividad de acción en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad de acción genérica que permite configurar acciones únicas y grupos de acciones entrantes de acciones múltiples, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>Capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-action.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archivos adjuntos de PDF a correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede adjuntar un archivo PDF estático a un mensaje de correo electrónico enviado con Journey Optimizer.</p>
<ul>
<li>Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año.</li>
<li>El tamaño máximo para cada archivo adjunto es 5 MB.</li>
<li>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Optimización en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, Journey Optimizer le ofrece las herramientas necesarias para ofrecer contenido personalizado y optimizado a su público, lo que le permite ejecutar experimentos de contenido, crear segmentación basada en reglas y utilizar combinaciones avanzadas de ambos para maximizar la eficacia de sus campañas y recorridos.</p>
<p>Con Optimization, puede:</p>
<ul>
<li>Probar múltiples variaciones de contenido para identificar la mensajería más eficaz.</li>
<li>Ofrecer contenido personalizado basado en atributos de usuario y datos contextuales.</li>
<li>Combine segmentación y experimentación para estrategias de campaña avanzadas.</li>
<li>Filtrar los usuarios que no coincidan con los criterios de variante.</li>
<li>Garantizar mecanismos de reserva para mantener la participación del usuario.</li>
</ul>
<P>Una vez que el recorrido o la campaña están activos, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían con la experiencia o el contenido adecuados.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Esta capacidad, que se publicó anteriormente el 8 de agosto solo en campañas, ahora también está disponible en recorridos a partir del 22 de agosto.</p>
<p>Para obtener más información, consulte la <a href="../campaigns/campaigns-message-optimization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Administración**

   * **Alertas de monitorización de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que <!--a channel configuration failure happens or if -->falte un registro DNS. [Más información](../reports/alerts.md#alert-dns-record-missing)

* **Asistente de IA**

   * **Generación de contenido en varios idiomas**. Ahora el contenido se puede generar en francés, español, alemán, italiano, japonés, sueco, holandés y noruego. [Más información](../content-management/generative-uc.md#languages)

     Fecha de disponibilidad: 25 de agosto


* **Campañas**

   * **Control de velocidad en las campañas de salida**: ahora puede habilitar el control de la velocidad de las campañas de salida (correo electrónico, SMS, notificaciones push), lo que le permite evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de servicio de atención al cliente. [Más información](../campaigns/campaign-schedule.md#set-rate-control)

   * **Programación de campañas de acción**. Los programadores diarios, semanales y mensuales de la campaña se han actualizado para proporcionar un control más detallado sobre las programaciones recurrentes:

      * **Periodicidad semanal**: ahora puede elegir repetir la campaña cada semana o cada dos semanas y seleccionar los días de la semana en que debería ejecutarse.

      * **Periodicidad mensual**: ahora puede elegir repetir la campaña todos los meses o cada dos meses y seleccionar el día del mes en que debe ejecutarse.

      * **Programaciones diarias, semanales o mensuales**: Puede especificar si la programación recurrente debe detenerse en una fecha específica o después de un determinado número de incidencias.

   * **Campañas de acción transaccional programadas**: ya están disponibles las campañas de acción transaccional programadas para enviar comunicaciones transaccionales por lotes y basadas en público por correo electrónico, SMS y canales push.

* **Canal - Tarjetas de contenido**

   * **Plantillas de diseño de tarjeta de contenido**: el canal de tarjeta de contenido ahora proporciona diseños de mensajes OOTB que optimizarán su experiencia de creación. Esta versión incluye plantillas de diseño de Imagen pequeña, Imagen grande y Solo imagen. [Más información](../content-card/design-content-card.md)

* **Canal: Push**

   * **Fecha de caducidad de la notificación push**: ahora puede especificar una fecha de caducidad para cada notificación push, lo que evita que los mensajes con limitación de tiempo (como las ofertas de Black Friday) se envíen después de una fecha determinada y, por lo tanto, evita ofrecer una mala experiencia a sus clientes.

* **Canal: SMS**

   * **Exclusión aproximada**: cuando está habilitada, la opción **Exclusión aproximada** detecta mensajes entrantes que se parecen mucho a las palabras clave de exclusión definidas (por ejemplo, “CANCILAR”) y envía automáticamente una respuesta de confirmación para comprobar la intención del usuario de cancelar su suscripción. Si el usuario confirma esta decisión a través de la indicación definida, se cancela su suscripción. [Más información](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >La **Exclusión aproximada** solo está disponible con Sinch e Infobip.

   * **Verificar conexión de SMS**: ahora puede probar y comprobar fácilmente sus credenciales de API de SMS en Adobe Journey Optimizer enviando un mensaje de ejemplo a un dispositivo designado. [Más información](../sms/sms-configuration-sinch.md)

* **Configuración**

   * **Compatibilidad con atributos personalizados con la URL de cancelación de suscripción de un solo clic**: con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un punto final personalizado externo definiendo su propio vínculo para cancelar la suscripción con un solo clic en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar LA suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

     Para personalizar aún más el vínculo de cancelación de suscripción de un solo clic, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento. [Más información](../email/list-unsubscribe.md#custom-attributes)

* **Conjuntos de datos**

   * **Repositorio de objetos de Decisiones sobre experiencias - Elementos de oferta personalizados**: el conjunto de datos de exportación integrado ahora captura todos los atributos de ofertas y el estado del ciclo vital, lo que permite una personalización y un sistema de informes completos. [Más información](../data/export-datasets.md)

   * Se ha introducido la comprobación de versiones a través del campo `etag` para mejorar la coherencia y rastrear los cambios a fin de ofrecer los elementos de forma más fiable.

* **Toma de decisiones**

   * **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar fragmentos a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante políticas de decisión. Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes. [Más información](../experience-decisioning/create-decision.md#fragments)

* **Recorridos**

   * **Operaciones masivas de recorridos**: en su lista de recorridos, ahora puede seleccionar varios elementos. Una vez seleccionados, puede pausar o reanudar hasta 10 recorridos a la vez.

   * **Compatibilidad con redireccionamiento (302) en acciones personalizadas**: ahora las acciones personalizadas pueden administrar redireccionamientos HTTP 302 por cada solicitud. Esto permite a los recorridos integrarse con API que redirigen las solicitudes a direcciones URL localizadas o específicas de la región. Las redirecciones se siguen automáticamente, lo que garantiza que el contenido correcto se envíe sin configuración adicional.

   * **Varias acciones entrantes en recorridos**: para simplificar la orquestación de recorrido, ahora puede definir varias acciones entrantes en un solo recorrido. Esta capacidad, disponible previamente en campañas, le permite enviar varias experiencias basadas en código, mensajes in-app, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, y cada acción con un contenido específico. [Más información](../building-journeys/journey-action.md#multi-action)

## Orquestación de campañas 

**Fecha de disponibilidad**: 4 de agosto de 2025

Journey Optimizer ahora incluye **orquestación de campañas**, una nueva funcionalidad diseñada específicamente para campañas por lotes iniciadas por la marca. Esta versión presenta un lienzo de orquestación de campaña y un modelado de datos mejorado, que funcionan juntos para permitir que los especialistas en marketing planifiquen, dirijan y entreguen campañas personalizadas en canales múltiples.

>[!IMPORTANT]
>
>Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

![GIF de orquestación de campañas](assets/do-not-localize/release.gif)

Incluye [esquemas y conjuntos de datos relacionales](#oc-relational) y [lienzo de campañas](#oc-canvas). Juntas, estas dos innovaciones suponen un nuevo estándar a la hora de orquestar campañas por lotes en Journey Optimizer. A continuación se enumeran las funcionalidades clave.

### Funcionalidades clave {#oc-capabilities}

* **Flujos de trabajo de varios pasos**

  Dirija sofisticadas campañas por lotes multicanal con el nuevo lienzo de orquestación de campañas diseñado específicamente para este fin.

* **Públicos bajo demanda**

  Segmente públicos bajo demanda para su activación inmediata.

* **Segmentación de varias entidades**

  Cree públicos en un contexto empresarial (dimensiones que no sean personas), como productos, tiendas, renovaciones, reservas y mucho más.

* **Visibilidad previa al envío**

  Revise, perfeccione y optimice públicos y campañas antes del lanzamiento y mientras se ejecutan las campañas

### Lienzo de campaña {#oc-canvas}

Una interfaz de orquestación visual completamente nueva diseñada específicamente para campañas por lotes. Este lienzo permite lo siguiente:

* Planificación visual de flujos de campaña de varios pasos y canales

* Compatibilidad con públicos bajo demanda creadas a partir de consultas relacionales

* División de públicos avanzada, esperas y lógica condicional

* Recuentos precisos previos al envío después de aplicar reglas y filtros empresariales

### Esquemas relacionales y conjuntos de datos {#oc-relational}

Adobe Journey Optimizer ahora admite entidades relacionales (por ejemplo, productos, tiendas, reservas, contratos) vinculadas a perfiles basados en personas. Esto permite la segmentación y personalización en estructuras de datos multidimensionales, lo que permite casos de uso como:

* Un mensaje por reserva, suscripción o contrato

* Segmentación basada en atributos de entidad relacionados (por ejemplo, categoría de producto o ubicación de tienda)

* Mejor direccionamiento (por ejemplo, enviar a todos los contactos conocidos vinculados a una entidad)

### Por qué importa

Esta versión proporciona a los especialistas en marketing un control total sobre el marketing por lotes iniciado por la marca y basado en públicos, combinando un modelado de datos flexible con una experiencia de orquestación diseñada específicamente para este fin. Está diseñada específicamente para la orquestación de campañas por lotes desde recorridos en tiempo real, a la vez que ofrece personalización y escalabilidad avanzadas.

### Más información

Obtenga más información en la [Documentación de orquestación de campañas](../orchestrated/gs-orchestrated-campaigns.md).


## Notas de la versión de julio de 2025 {#25-7-rn}

**Fecha de lanzamiento**: miércoles, 29 de julio de 2025

### Nuevas funciones {#features-25-7}

A continuación, se describen las nuevas funciones incluidas en esta versión.

#### Funcionalidades

<table>
<thead>
<tr>
<th><strong>Marcas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y personalizar sus propias marcas para definir claramente su identidad visual y verbal en todas las comunicaciones. Con la puntuación de alineación de marca, puede recibir comentarios en tiempo real sobre cómo el contenido refleja el tono, el estilo y las directrices de su marca, lo que le ayuda a mantenerse siempre coherente con la marca en cada mensaje que envía.</p>
<p>Esta capacidad, que se lanzó anteriormente en beta, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Para obtener más información, consulte la <a href="../content-management/brands.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Use Decisioning en el canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir directivas de Decisión a recorridos de correo electrónico y campañas. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de Decisioning para devolver dinámicamente el mejor contenido para entregar a cada miembro del público.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliado sus funcionalidades en canales múltiples para incluir la compatibilidad con el canal LINE. Esta mejora le permite crear, editar y previsualizar experiencias de LINE, permitiendo interacciones más personalizadas y atractivas. Con LINE, puede conectarse con más clientes, enviar contenido relevante y mejorar su participación.</p>
<p>Anteriormente disponible solo para solicitudes, el canal LINE ahora está disponible para todos los usuarios (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../../rp_landing_pages/line-landing-page.md">documentación detallada</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ensayo del recorrido </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El ensayo del recorrido es un modo especial de publicación de recorrido de Adobe Journey Optimizer que permite a los profesionales de recorridos probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil. Esta función ayuda a los profesionales de recorridos a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en vivo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-dry-run.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID suplementario para recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede activar recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y que cada instancia siga su propia ruta a través del recorrido.</p>
<p>Publicado anteriormente con disponibilidad limitada, el uso de ID suplementarios en recorridos ya está disponible para todos los entornos. En esta versión con disponibilidad general, la función ahora es compatible con los recorridos de Leer público.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/supplemental-identifier.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Alertas en el producto

Ahora puede suscribirse a **alertas por correo electrónico y en el producto** para las versiones de productos de Journey Optimizer.

Para suscribirse:

* Vaya a **Preferencias de Adobe Experience Cloud**.
* En **Notificaciones**, busque **Nuevas versiones de Journey Optimizer**.
* Habilite las notificaciones in-app y por correo electrónico.

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Cambio en las condiciones del recorrido {#ee-change@}

A partir del 8 de julio, en las nuevas organizaciones de clientes, la creación de expresiones mediante eventos de experiencia dejará de ser compatible con el editor de expresiones utilizado en las condiciones del recorrido. Como resultado, no se pueden usar eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md) para crear expresiones. [Aquí](../building-journeys/exp-event-lookup.md) encontrará referencias a enfoques alternativos y prácticas recomendadas para crear expresiones y lógicas con eventos de experiencia.

No hay cambios en la forma de acceder a los datos de evento de contexto de recorrido en los recorridos unitarios. En los editores de expresiones y personalización, los usuarios pueden seguir accediendo a los datos pasados con el evento de recorrido inicial.

Obtenga más información [en estas preguntas frecuentes](../building-journeys/exp-event-lookup.md#faq-ee).

### Mejoras {#25-7-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Campañas**

   * **Varias acciones entrantes en las campañas**: para simplificar la orquestación de la campaña, ahora puede definir varias acciones entrantes en una sola campaña. Esta capacidad le permite enviar varias experiencias basadas en código, mensajes in-app, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, y cada acción con un contenido específico.
     [Más información](../campaigns/campaign-action.md#multi-action)

   * **Reorganización del inventario de campañas**: las campañas programadas y activadas por API ahora se dividen en pestañas independientes en el inventario de campañas para facilitar la navegación y la administración.

[Más información](../campaigns/manage-campaigns.md)

* **Administración de datos**
   * **Actualización del conjuntos de datos del sistema de Gestión de decisiones**: las ofertas personalizadas y de reserva eliminadas ahora se marcan como archivadas en los conjuntos de datos «decision_object_repository_personalized_offers» y «decision_object_repository_fallback_offers». Los registros existentes en el conjunto de datos no cambian.

[Más información](../offers/export-catalog/access-dataset.md)

* **Recorridos**
   * **Mejoras en la herramienta de zona protegida para recorridos**: al copiar recorridos en varias zonas protegidas mediante las funciones de exportación e importación de paquetes, ahora también están disponibles las siguientes funciones:
      * Selección de un evento existente en el destino
      * Copia de un evento independientemente de un recorrido
      * Detectar relaciones entre grupos de campos y fuentes de datos, vincularlas en el destino si existen y crearlas en caso contrario.

[Más información](../configuration/copy-objects-to-sandbox.md)

* **Canal: in-app**
   * **Pares de clave/valor in-app**: con los mensajes in-app, puede definir pares de clave y valor para incluir variables personalizadas en la carga útil del mensaje. Estos pares clave-valor le permiten pasar datos adicionales según su configuración específica y el caso de uso. [Más información](../in-app/design-in-app.md)

* **Canal - Tarjeta de contenido**

   * **Descalificación de campaña basada en reglas**: al editar reglas de entrega adicionales, la opción de reglas de envío anteriores se ha reemplazado con tres tipos de reglas diferentes para controlar mejor el tiempo y la visibilidad del mensaje:
      * Mostrar mensaje si: Condiciones que determinan cuándo se muestra la tarjeta de contenido.
      * Descartar mensaje si: Condiciones que ocultan temporalmente la tarjeta de contenido. Puede volver a aparecer si se vuelven a cumplir las condiciones de visualización.
      * Descalificar mensaje si: Condiciones que impiden permanentemente que se vuelva a mostrar la tarjeta de contenido.

[Más información](../content-card/design-content-card.md)

* **Toma de decisiones**
   * **API de herramientas de migración**: el equipo de Journey Optimizer está trabajando en las API de herramientas de migración para migrar entidades de gestión de decisiones a Decisioning. Esta herramienta permite una migración perfecta entre zonas protegidas con resolución de dependencia y funciones de reversión. Si está interesado, póngase en contacto con su representante de Adobe.

* **Personalización**
   * Se ha añadido una nueva función auxiliar, «SHA256», al editor de personalización. Esta función se utiliza para calcular y devolver el hash sha256 de una cadena.

[Más información](../personalization/functions/string.md#sha256)


## Notas de la versión de junio de 2025 {#25-6-rn}

**Fecha de lanzamiento**: 18 de junio de 2025

### Nuevas funciones {#25-06-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Conjuntos de datos de Adobe Experience Platform en las tomas de decisiones (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los conjuntos de datos de Adobe Experience Platform, que anteriormente estaban disponibles para la personalización, ahora se pueden aprovechar para la toma de decisiones. Esto le permite ampliar la definición de los atributos de decisión a datos adicionales en conjuntos de datos para actualizaciones masivas que cambian periódicamente sin tener que actualizar manualmente los atributos de uno en uno. Por ejemplo, disponibilidad, tiempos de espera, etc.</p>
<p>Esta funcionalidad está actualmente disponible para todos los clientes en beta pública. Póngase en contacto con el representante de su cuenta si desea tener acceso.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/aep-data-exd.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de junio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensajería RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar, personalizar y entregar mensajes de servicios de comunicación enriquecidos (RCS) a través de un proveedor de terceros mediante la integración con la solución de proveedor de SMS personalizado.</p>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campos de formulario en el contenido de la experiencia basada en código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir los campos editables específicos en las plantillas de contenido JSON o HTML que permitan a los usuarios no técnicos editar fácilmente el contenido en una vista de formulario dentro de la creación del canal de la experiencia basada en código, sin necesidad de manipular ningún código.<br />Más que eso, al definir las plantillas de contenido de la experiencia basada en código, ahora puede insertar directivas de decisión en la plantilla, lo que aumenta la reutilización y facilidad de uso.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Para obtener más información, consulte la <a href="../code-based/code-based-form-fields.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Actividad de decisión de contenido en los recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede incluir ofertas personalizadas en los recorridos mediante una actividad de decisión de contenido específica en el lienzo y utilizarlas en actividades de recorrido, incluidas las condiciones y las acciones personalizadas.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ensayo del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El ensayo del recorrido es un modo especial de publicación de recorrido de Adobe Journey Optimizer que permite a los profesionales de recorridos probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil. Esta función ayuda a los profesionales de recorridos a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en vivo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-dry-run.md">documentación detallada</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede poner en pausa y reanudar los recorridos. Esta funcionalidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando están en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda el recorrido.</p>
<p>Puede poner en pausa y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a los recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-pause.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Escalar el ganador de la experimentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Escalar el ganador de la experimentación permite desplegar automática o manualmente la variación ganadora de un experimento para todo el público. Esta función garantiza que, una vez que se identifique al que tenga el mayor rendimiento, pueda maximizar su alcance y eficacia sin una supervisión manual constante.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-experiment.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de junio de 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflicto y priorización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización - antes disponibles solo para organizaciones de acceso limitado (LA) que ahora están disponibles de forma general (GA).</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad ampliada: las herramientas de administración de conflictos ahora admiten tanto los recorridos unitarios como los recorridos de calificación de público, además de los recorridos de público de lectura.</li>
<li>Solución de problemas mejorada: ahora hay dos nuevos campos de evento de paso disponibles en el servicio de consultas, lo que le permite analizar por qué se rechazó un perfil de un recorrido o una campaña.</li>
<li>Informes mejorados: ahora los informes indican qué regla específica excluyó un perfil de un recorrido o campaña, lo que proporciona una mayor transparencia e información útil.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de junio de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#25-06-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Conjuntos de reglas de canal**

   * **Ventana de duración personalizada** para el límite: ahora hay un nuevo campo **Cada** disponible en la pantalla de configuración de conjuntos de reglas de canal, que le permite aplicar reglas de restricción de frecuencia durante varios días, semanas o meses, según la duración especificada.

   * **Frecuencia de restricción de restablecimiento por hora**: ahora puede aplicar una restricción por hora a los conjuntos de reglas de canal. Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Póngase en contacto con el Servicio de atención al cliente para habilitarlo.

   * **Duración diaria**: anteriormente disponible en disponibilidad limitada, la restricción de frecuencia “diaria” en los conjuntos de reglas de canal ya está disponible para todos los clientes.

  Para obtener más información, consulte la [documentación detallada](../conflict-prioritization/channel-capping.md).

* **Experiencias basadas en código**

   * Ahora es posible añadir una política de decisión en las plantillas de contenido de la experiencia basada en código, donde se puede utilizar para aprovechar las ofertas en campos de formulario editables. [Más información](../code-based/code-based-form-fields.md)

   * Desde la pantalla de recorrido de la experiencia basada en código o de edición de campaña, ahora puede añadir directamente una política de decisión, sin abrir el editor de personalización. [Más información](../code-based/create-code-based.md#edit-code)

* **Compatibilidad con CSS personalizado en el diseñador de correo electrónico**

  Journey Optimizer ahora le permite añadir CSS personalizado al contenido del correo electrónico directamente en el diseñador de correo electrónico. [Más información](../email/custom-css.md)

* **Nueva navegación con pestañas para las campañas**

  El nuevo patrón de navegación permite un acceso más rápido a la creación de contenido y admite una mayor ampliación de la configuración en todas las campañas. [Más información](../campaigns/create-campaign.md)

* **Toma de decisiones**

   * **Copia y toma de decisiones de zona protegida** (fecha de disponibilidad: 3 de junio de 2025): ahora se pueden copiar objetos de decisiones entre zonas protegidas, lo que agiliza los flujos de trabajo de prueba e implementación. [Más información](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Compatibilidad con atributos de elementos de decisión para reglas de toma de decisiones** (fecha de disponibilidad: 4 de junio de 2025). Ahora puede aprovechar los atributos de elementos de decisión para crear reglas de toma de decisiones. [Más información](../experience-decisioning/rules.md#create)

* **Actualización de la API de ejecución de mensajes interactivos** - Fecha de disponibilidad: 6 de junio de 2025

  La API de ejecución de mensajes interactivos ahora le permite eliminar la programación de la próxima ejecución de campañas. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}


## Notas de la versión de mayo de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nuevas funciones {#25-05-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Vista de calendario para el inventario de campañas y recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Ahora mismo, esta función solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para solicitar acceso, utilice <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulario</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obtener más información, consulte estas secciones: <a href="../building-journeys/journey-ui.md">Examinar y filtrar sus recorridos</a>, <a href="../campaigns/manage-campaigns.md">Acceso a campañas</a>.</p>
<p>Fecha de disponibilidad: 28 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de fragmentos de contenido de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la integración de Adobe Experience Manager y Adobe Journey Optimizer, ahora puede utilizar sin esfuerzo fragmentos de contenido de Adobe Experience Manager dentro de su contenido de Journey Optimizer. Esta conexión perfecta facilita el acceso y el uso del contenido de AEM directamente en Journey Optimizer.</p>
<p>Anteriormente disponible para un conjunto limitado de organizaciones (LA), esta funcionalidad ahora es de disponibilidad general (GA) con la siguiente mejora: ahora puede definir marcadores de posición y asignar valores de personalización dentro de la firma del fragmento mediante el modo Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obtener más información, consulte la <a href="../integrations/aem-fragments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Dynamic Media de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y son accesibles directamente en Journey Optimizer. Esta actividad le permite lo siguiente:</p>
<ul>
<li>Administrar centralmente los recursos con actualizaciones en tiempo real.</li>
<li>Modificar la configuración de los recursos, como la anchura y la altura, al instante.</li>
<li>Personalizar las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID suplementario para recorridos activados por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede activar recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y que cada instancia siga su propia ruta a través del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/supplemental-identifier.md">documentación detallada</a>.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de variaciones de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con la versión de Disponibilidad general, la función ahora incluye compatibilidad con el contenido multilingüe y experimentos de contenido, lo que permite probar variaciones en diferentes idiomas y tratamientos. Además, ahora admite atributos contextuales (además de los atributos de perfil), lo que permite realizar pruebas de contenido aún más dinámicas y adaptadas a cada situación.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obtener más información, consulte la <a href="../test-approve/simulate-sample-input.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronización de la programación de público de lectura con el trabajo de segmentación por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede activar ejecuciones de recorrido diarias tras la finalización de la segmentación por lotes. Esta opción ahora está disponible en los recorridos programados diariamente para todos los clientes. Le permite definir un período de tiempo de hasta 6 horas de espera de los datos del público procedentes de los trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos. </p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Proveedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora permite configurar proveedores de SMS adicionales más allá de las opciones predeterminadas: Sinch, Infobip y Twilio. Con la configuración personalizada del proveedor de SMS, puede integrar proveedores de terceros directamente, aprovechar la personalización avanzada de la carga útil para la mensajería dinámica y administrar las preferencias de consentimiento (inclusión/exclusión) para garantizar el cumplimiento.</p>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: 20 de mayo de 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas del Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente temas aprobados anteriormente para garantizar la coherencia de marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir de forma independiente correos electrónicos de alta calidad, al tiempo que se reduce la dependencia en los equipos de diseño.</p>
<p>Actualmente, esta función está en versión Beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisiones: nuevo generador de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear fórmulas de clasificación de decisiones específicas definiendo y combinando criterios a partir de una nueva interfaz mejorada. En lugar de depender únicamente de una prioridad de oferta estática, puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obtener más información, consulte la <a href="../experience-decisioning/ranking/ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#25-05-improv}

A continuación, se describen las mejoras incluidas en esta versión.


* **Nueva compatibilidad con objetos de campaña para copias en zonas protegidas**. Fecha de disponibilidad: 15 de mayo de 2025

  Cuando se copian campañas en varias zonas protegidas limitadas mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Carpetas para páginas de aterrizaje**. Fecha de disponibilidad: 9 de mayo de 2025

  Para administrar con facilidad las páginas de aterrizaje, ahora puede utilizar las carpetas para organizarlas de forma más eficaz en una jerarquía estructurada. [Más información](../landing-pages/manage-lp.md)

* **Correo directo: compatibilidad con claves SSH para conexiones SFTP**. Fecha de disponibilidad: 5 de mayo de 2025

  En la configuración de enrutamiento del archivo de correo directo, además del SFTP existente con el tipo de autenticación por contraseña, ahora puede exportar el archivo de correo directo a un servidor SFTP con la autenticación por clave SSH. [Más información](../direct-mail/direct-mail-configuration.md)

* **Activación de cápsulas para la personalización**. Fecha de disponibilidad: 5 de mayo de 2025

  Se ha añadido el nuevo botón “píldoras” al editor de personalización. Cuando se habilita, los atributos contextuales y de perfil se muestran como píldoras, lo que mejora la legibilidad del código. [Más información](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esta capacidad se implementará gradualmente en todos los entornos en los próximos 30 días.

* **Compatibilidad con “Redireccionar a URL” en el canal web** - Fecha de disponibilidad: 20 de mayo de 2025

  El canal web de Journey Optimizer ahora le permite redirigir a los visitantes a otra URL existente, en lugar de crear una nueva variación en el editor visual. Esta funcionalidad se puede utilizar para ejecutar experimentos comparando dos páginas completamente diferentes en lugar de cambiar solo unos pocos elementos dentro de una página. [Más información](../web/create-web.md#web-redirect-to-url)

* **Carpetas para plantillas y fragmentos**: fecha de disponibilidad: 20 de mayo de 2025

  Las carpetas permiten organizar los objetos de forma más fácil y eficaz en una jerarquía estructurada. Las carpetas, que antes solo estaban disponibles para un conjunto de organizaciones (LA), ahora lo están para que todos los usuarios (GA) administren sus plantillas y fragmentos de contenido. Obtenga más información en las secciones [Plantillas de contenido](../content-management/access-content-templates.md#folders) y [Fragmentos](../content-management/manage-fragments.md#folders).

* **Rastreo de clics en plantillas de correo electrónico** - Fecha de disponibilidad: 20 de mayo de 2025

  El rastreo de clics en elementos `<area>` dentro de mapas de imagen en el contenido de correo electrónico ahora se admite de forma nativa en [!DNL Journey Optimizer]. Esto sirve para garantizar que las áreas de mapa de imagen reciban el mismo encapsulado de seguimiento, datos de seguimiento y parámetros añadidos que los hipervínculos estándar. [Obtenga más información sobre el seguimiento de mensajes](../email/message-tracking.md#manage-tracking).

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Carril derecho en la lista de campañas** - Fecha de disponibilidad: 20 de mayo de 2025

  Al seleccionar una campaña de la lista, se abre el panel que muestra sus detalles.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## Notas de la versión de abril de 2025 {#25-4-rn}

**Fecha de lanzamiento**: del 29 al 30 de abril de 2025

### Nuevas funciones {#25-04-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Editor de personalización: Aprenda haciendo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible un área de reproducción de personalización, donde puede experimentar con expresiones de personalización. Le permite explorar plantillas y cargas útiles de ejemplo para ayudarle a empezar y probar sus propias expresiones de personalización.</p>
<p>Para obtener más información, consulte la <a href="../personalization/personalize.md#playground">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de abril de 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliado sus funcionalidades en canales múltiples para incluir la compatibilidad con el canal LINE. Esta mejora le permite crear, editar y previsualizar experiencias de LINE, permitiendo interacciones más personalizadas y atractivas. Con LINE, puede conectarse con más clientes, enviar contenido relevante y mejorar su participación.</p>
<p>El canal LINE está habilitado para los clientes de Adobe Journey Optimizer previa solicitud. Póngase en contacto con el Servicio de atención al cliente de Adobe o con su representante de Adobe para activar la función para su organización.</p>
<p>Para obtener más información, consulte la <a href="../../rp_landing_pages/line-landing-page.md">documentación detallada</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Métricas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las métricas de recorrido ya están disponibles, lo que le permite medir el impacto de sus actividades en las métricas clave de su empresa y proporcionar una perspectiva más clara de su rendimiento.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Para obtener más información, consulte la <a href="../building-journeys/success-metrics.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 9 de abril de 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Express (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora se integra con Adobe Express, lo que le permite conectar sin problemas sus recursos creativos con la orquestación de recorrido. Esta integración simplifica el proceso de diseño e implementación de contenido personalizado en todas las campañas. </p>
<p>Esta integración no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Para obtener más información, consulte la <a href="../integrations/express.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activación de ejecuciones de recorrido diarias tras la finalización de la segmentación por lotes (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En el caso de los recorridos programados diariamente, una nueva opción le permite definir un intervalo de tiempo de hasta 6 horas para esperar los datos de público de los trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos. La opción Activar tras evaluación de público por lotes solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Puntuación de alineación con la marca (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La función de puntuación de alineación de marca proporciona comentarios claros directamente en el Diseñador de correo electrónico, lo que le ayuda a ver si el contenido se ajusta al tono, al estilo y a las directrices de la marca. Esta función está disponible en Beta.</p>
<p>Para obtener más información, consulte la <a href="../content-management/brands-score.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Mejoras {#25-04-improv}

**API de vista previa de campañas**

Hay nuevas API disponibles para previsualizar campañas, además de las capacidades de envío de pruebas existentes. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Herramientas de la zona protegida**

* **Herramientas de zona protegida para acciones personalizadas**

  Las acciones personalizadas ahora se incluyen en la lista de objetos de Adobe Journey Optimizer que se pueden copiar mediante la función de herramientas de zona protegida, lo que optimiza las pruebas y la implementación. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Herramientas de zona protegida para campañas**. Fecha de disponibilidad: 3 de abril de 2025

  Ahora puede copiar campañas en varias zonas protegidas mediante las funciones de exportación e importación de paquetes. Las campañas se copian junto con todos los elementos relacionados con el perfil, el público, el esquema, los mensajes en línea y los objetos dependientes. Algunos elementos no se copian, como los elementos de decisión, las etiquetas de uso de datos y la configuración de idioma. [Más información](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalización**

* **Nuevo atributo contextual**

  Ahora hay disponible un nuevo atributo contextual, **ID de perfil de mensaje**, que se puede seleccionar en el editor de personalización. Es un atributo orientado a mensajes que identifica de forma exclusiva cada mensaje enviado a cada perfil de destino en un envío. Este identificador único se puede utilizar, por ejemplo, como parámetro de seguimiento de URL para distinguir cada vínculo abierto o en el que los destinatarios hacen clic.

* **Atributos rellenados en el panel de atributos**. Fecha de disponibilidad: 2 de abril de 2025

  El panel de atributos del editor de personalización ahora muestra solo los atributos rellenados de forma predeterminada. Para ver todos los atributos, use el botón de configuración para desactivar la opción **[!UICONTROL Mostrar solo atributos rellenados]**. [Más información](../personalization/personalization-build-expressions.md)

**Canal de correo electrónico**

* **Seguimiento personalizado de URL**. Fecha de disponibilidad: 30 de abril de 2025

  Para obtener una mayor flexibilidad y control sobre la configuración del correo electrónico, ahora puede personalizar todos los parámetros de seguimiento de URL a la vez a nivel de configuración de canal de correo electrónico, en lugar de hacerlo en el Diseñador de correo electrónico para cada vínculo del contenido. [Más información](../email/surface-personalization.md#personalize-url-tracking)

* **Diseñador de correo electrónico**. Fecha de disponibilidad: 1 de abril de 2025

  Para mejorar la accesibilidad en Journey Optimizer, ahora hay dos campos nuevos disponibles en Diseñador de correo electrónico: se corresponden con el elemento `<title>` y el atributo `lang` en el elemento `<html>` del contenido del correo electrónico. Puede definir esta configuración, además del campo **[!UICONTROL Preencabezado]**, en la sección **[!UICONTROL Cuerpo]** del correo electrónico. [Más información](../email/email-metadata.md)

**Manuales de tácticas de casos de uso**

* **Creación y uso compartido de manuales de tácticas (Private Beta)**: ahora puede crear, administrar y compartir sus propios manuales de tácticas de casos de uso. Ahora mismo, esta función solo está disponible para un conjunto de organizaciones como Private Beta. Para obtener acceso, póngase en contacto con su representante de Adobe. [Más información](../start/ai-features.md#playbooks)

**Navegación**

* **Administración de contenido**. Fecha de disponibilidad: 2 de abril de 2025

  Para administrar con facilidad los fragmentos y las plantillas de contenido, ahora puede utilizar carpetas para organizarlos de forma más eficaz en una jerarquía estructurada. Obtenga más información en las secciones [Fragmentos](../content-management/manage-fragments.md#folders) y [Plantillas de contenido](../content-management/access-content-templates.md#folders)

  >[!AVAILABILITY]
  >
  >Esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## Notas de la versión de marzo de 2025 {#25-3-rn}

### Nuevas funciones {#25-03-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integración con Dynamic Media (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y son accesibles directamente en Journey Optimizer. Esta actividad le permite lo siguiente:
<ul>
<li>Administrar centralmente los recursos con actualizaciones en tiempo real</li>
<li>Modificar la configuración de los recursos, como la anchura y la altura, al instante</li>
<li>Personalizar las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización</li>
</ul>
<p>
<p>Esta integración solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integración con Adobe GenStudio (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para mejorar la eficacia del marketing y mantener la coherencia de marca, ahora puede integrar sin problemas las experiencias de GenStudio for Performance Marketing con Journey Optimizer. Esto le permite aprovechar la creación de contenido con tecnología de IA de GenStudio junto con las funcionalidades de orquestación avanzadas de Journey Optimizer.<p>
<p>El uso de la integración de GenStudio en Journey Optimizer no está disponible actualmente con Healthcare Shield o Privacy and Security Shield (disponibilidad limitada).</p>
<p>Para obtener más información, consulte la <a href="../integrations/genstudio.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Evaluación de público flexible (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), la evaluación de público flexible ya está disponible para todos los usuarios (GA). Esta función le permite ejecutar un trabajo de segmentación bajo demanda para los públicos seleccionados, lo que garantiza que siempre tenga los datos de público más actualizados antes de segmentarlos en recorridos y campañas de Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obtener más información, consulte la <a href="../audience/creating-a-segment-definition.md#flexible">documentación detallada</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Mejoras {#25-03-improv}

**Editor de personalización** (fecha de disponibilidad: 12 de marzo)

El editor de personalización de Journey Optimizer se ha actualizado con nuevas funciones:

* **Diseño actualizado del editor de código**: una interfaz más clara y moderna para mejorar la facilidad de uso y el enfoque.
* **Buscar y reemplazar**: funcionalidad añadida para buscar y reemplazar contenido rápidamente en el editor.
* **Compatibilidad con Deshacer y Rehacer**: permite revertir o volver a aplicar fácilmente los cambios.
* **Tamaño de fuente personalizable**: habilita el ajuste del tamaño de fuente del editor para mejorar la legibilidad.
* **Validación JSON en línea**: proporciona validación en tiempo real del lado del cliente para el contenido JSON a fin de acelerar la detección de errores.
* **Completar automáticamente atributos de perfil y contexto**: ofrece sugerencias inteligentes para optimizar la creación de contenido.
* **Resaltado de sintaxis mejorado**: mejora la legibilidad al hacer que la estructura del código quede visualmente más diferenciada.

![Vídeo que muestra la nueva función en el editor de personalización](assets/do-not-localize/personalization-editor.gif)

Para obtener más información, consulte la [documentación detallada](../personalization/personalization-build-expressions.md).

**Aprobaciones**

Al definir las condiciones de una directiva de aprobación, ahora tiene la opción de filtrar por etiqueta o categoría de objeto.

Para obtener más información, consulte la [documentación detallada](../test-approve/approval-policies.md).

**Configuración**

* Ahora puede asignar las etiquetas unificadas de Adobe Experience Platform a las configuraciones de canal. Esto le permite clasificarlas con facilidad y mejorar la búsqueda y la navegación en todas las listas. [Más información](../configuration/channel-surfaces.md#channel-config-tags)

* Al configurar o editar un subdominio de correo electrónico en Journey Optimizer, ahora puede elegir administrar el registro DMARC asociado por su cuenta, si está disponible en el dominio principal. [Más información](../configuration/dmarc-record.md#set-up-dmarc)

**Reglas empresariales**

Ahora puede usar la restricción de frecuencia diaria en recorridos y campañas con la segmentación por lotes. Para garantizar la precisión de las reglas de restricción de frecuencia diaria, asegúrese de elegir el espacio de nombres de prioridad más alta durante la creación de una campaña o recorrido. Obtenga más información sobre la prioridad del espacio de nombres en la [Guía del servicio de identidad de Platform](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como recordatorio, la restricción de frecuencia diaria en los conjuntos de reglas solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Para obtener más información sobre las reglas empresariales, consulte la [documentación detallada](../conflict-prioritization/rule-sets.md).

**Plantillas de contenido**

Las plantillas de contenido de tipo HTML ya no se utilizan. Tenga en cuenta que aún puede usar plantillas de contenido de HTML existentes creadas anteriormente en [!DNL Journey Optimizer]. [Más información sobre las plantillas de contenido](../content-management/content-templates.md)

**Políticas de consentimiento**

Ahora puede aprovechar las políticas de consentimiento personalizadas mediante acciones de marketing en configuraciones de canal de correo electrónico transaccional. [Más información](../action/consent.md#surface-marketing-actions)

<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->



## Notas de la versión de febrero de 2025 {#25-02-rn}

**Fecha de lanzamiento**: 18-19 de febrero de 2025


### Nuevas funciones {#25-02-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Crear y administrar reglas empresariales</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas empresariales utilizando conjuntos de reglas. Los conjuntos de reglas son grupos de reglas que ayudan a limitar los mensajes enviados dentro de las campañas y las acciones de recorrido entre canales, así como para controlar las entradas de perfiles en los recorridos.<p>
<p><ul><li>Cree conjuntos de reglas de canal para restringir el número de mensajes enviados a través de uno o varios canales. Aplíquelas a campañas o acciones de recorrido para aplicar las reglas definidas en el conjunto de reglas. El conjunto de reglas de canal le permite aplicar reglas de límite basadas en tipos de comunicación. Por ejemplo, defina una regla para limitar los “mensajes promocionales” y otra para los “boletines”. Aplique el conjunto de reglas adecuado en la campaña o acción de recorrido según el tipo de comunicación que envíe.</li>
<li> Cree conjuntos de reglas de recorrido para controlar las entradas de perfil en los recorridos. Limite la frecuencia con la que un perfil puede entrar en un recorrido dentro de un período determinado o el número de recorridos en los que se puede inscribir un perfil simultáneamente. Aplíquelas en el nivel de recorrido para garantizar una administración de entrada adecuada.</li></ul></p>
<p>Las reglas empresariales, que anteriormente estaban disponibles para un conjunto de organizaciones (LA), ya están disponibles para todos los usuarios (GA). Las reglas empresariales del dominio de recorrido siguen estando disponibles únicamente para un conjunto limitado de organizaciones (LA).</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/rule-sets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de páginas de aterrizaje con el Asistente de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido atractivo para sus páginas de aterrizaje, incluidos diseños de página completa, texto personalizado e imágenes personalizadas, con la ayuda del Asistente de IA.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Para obtener más información, consulte la <a href="../content-management/generative-full-content.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marcas con el asistente de IA (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar sus propias marcas para definir la identidad visual y verbal de su marca. </p>
<p>Esta capacidad se presenta como una versión beta privada para un conjunto limitado de clientes. Estará disponible de forma progresiva para todos los clientes en futuras versiones.</p>
<p>Para obtener más información, consulte la <a href="../content-management/brands.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Resolución de problemas de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede validar una configuración de acción personalizada realizando llamadas de API reales directamente desde Adobe Journey Optimizer. Esta nueva funcionalidad le ayuda a solucionar los problemas de las acciones personalizadas antes o después de utilizarlas en un recorrido.  </p>
<p>Para obtener más información, consulte la <a href="../action/troubleshoot-custom-action.md">documentación detallada</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Evaluación de público flexible (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La evaluación de público flexible le permite ejecutar un trabajo de segmentación bajo demanda para los públicos seleccionados, lo que garantiza que siempre tenga los datos de público más actualizados antes de segmentarlos en recorridos y campañas de Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obtener más información, consulte la <a href="../audience/creating-a-segment-definition.md#flexible">documentación detallada</a>.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 28 de enero de 2025</p>
</tr>
</tbody>
</table>
</table>


### Mejoras {#25-02-improvements}

Las mejoras que se muestran a continuación están incluidas en la actualización de febrero.

* **Tiempo de vida del conjunto de datos (TTL)**: a partir de este mes, se implementará un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las nuevas zona protegidas y organizaciones de la siguiente manera:

   * 90 días para los datos en el almacén de perfiles
   * 13 meses para los datos en el lago de datos

  Este cambio se implementará en las zonas protegidas de clientes existentes en una fase posterior. 

  Obtenga más información sobre esta actualización en [las preguntas más frecuentes](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Correo directo**: ahora se admite un nuevo tipo de servidor, la zona de aterrizaje de datos, para el enrutamiento de archivos en la configuración del canal de correo directo. [Más información](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: ahora puede administrar el envío de mensajes SMS desde puntos finales multiregionales anulando las direcciones URL de envío, comentarios, entrada y devolución de llamada. Para admitir esto, se ha añadido nuevo campo Anular URL a la configuración de Credenciales de API. Este cambio solo está disponible con el proveedor Sinch. [Más información](../sms/sms-configuration-sinch.md)

* **Personalización** (fecha de disponibilidad: 29 de enero de 2025): hay nuevas funciones de ayuda de fecha y hora disponibles para usar en el editor de personalización. [Más información](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuración de correo electrónico**: si administra el consentimiento fuera de Adobe, ahora puede establecer una dirección de correo electrónico de cancelación de suscripción personalizada y una URL de cancelación de suscripción de un solo clic personalizada como parte de los ajustes de la configuración de canal de correo electrónico.[Más información](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Toma de decisiones** (fecha de disponibilidad: 28 de enero de 2025): la toma de decisiones ahora admite tipos de datos de objeto al editar el esquema del catálogo de elementos. [Más información](../experience-decisioning/catalogs.md)
