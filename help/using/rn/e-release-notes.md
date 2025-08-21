---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: ht
source-wordcount: '1033'
ht-degree: 100%

---

# Notas de versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).


## Notas de la versión preliminar de agosto de 2025 {#25-8-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: miércoles, 19 de agosto de 2025


### Nuevas funciones {#Aug-25-8-features}

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
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
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
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche los datos de Adobe Experience Platform en el editor de personalización para personalizar su contenido. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de la API. Cuando haya terminado, puede usar sus datos para personalizar su contenido en [!DNL Journey Optimizer].</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad con canales de entrada,</li>
<li>La función de ayuda “datasetLookup” ahora se puede utilizar dentro de la expresión y los fragmentos visuales para personalizar el contenido mediante datos de conjuntos de datos de Adobe Experience Platform,</li>
<li>Una opción del conjunto de datos ahora le permite habilitar conjuntos de datos para la personalización de la búsqueda, sin tener que realizar una llamada API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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
<th><strong>Optimización de la ruta del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le ofrece las herramientas necesarias para optimizar sus recorridos mediante el uso de la IA y los marcos de experimentación, a la vez que garantiza una facilidad de uso y una diferenciación perfectas entre las funcionalidades de optimización y condición.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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
<li>Capacidad para crear nodos entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>Capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularios personalizados de página de aterrizaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite crear formularios personalizados y aprovecharlos en páginas de aterrizaje para capturar los atributos de perfil en el conjunto de datos definido para cada formulario.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Administración**

   * **Alertas de monitorización de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que se produzca un error de configuración de canal o si falta un registro DNS.

* **Campañas**

   * **Control de velocidad en las campañas de salida**: ahora puede habilitar el control de la velocidad del acelerador para las campañas de salida (correo electrónico, SMS, notificaciones push), lo que le permite evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de servicio de atención al cliente.

   * **Programación de campañas de acción**: los programadores de campañas diarias, semanales y mensuales se han actualizado para mejorar la granularidad. Por ejemplo, ahora puede establecer el número de semanas/meses entre las programaciones, definir en qué día se van a ejecutar y decidir si se detienen después de un número específico de ocurrencias o en una fecha específica.

   * **Campañas de acción transaccional programadas**: ya están disponibles las campañas de acción transaccional programadas para enviar comunicaciones transaccionales por lotes y basadas en público por correo electrónico, SMS y canales push.

* **Canal: Push**

   * **Fecha de caducidad de la notificación push**: ahora puede especificar una fecha de caducidad para cada notificación push, lo que evita que los mensajes con limitación de tiempo (como las ofertas de Black Friday) se envíen después de una fecha determinada y, por lo tanto, evita ofrecer una mala experiencia a sus clientes.

* **Canal: correo electrónico**

   * **Archivos PDF adjuntos a correos electrónicos**: ahora puede adjuntar archivos PDF estáticos a los mensajes de correo electrónico enviados con Journey Optimizer.

* **Canal: SMS**

   * **Exclusión aproximada**: cuando está habilitada, la opción **Exclusión aproximada** detecta mensajes entrantes que se parecen mucho a las palabras clave de exclusión definidas (por ejemplo, “CANCILAR”) y envía automáticamente una respuesta de confirmación para comprobar la intención del usuario de cancelar su suscripción. Si el usuario confirma esta decisión a través de la indicación definida, se cancela su suscripción.

     Tenga en cuenta que **exclusión aproximada** solo está disponible con Sinch e Infobip.

   * **Verificar conexión de SMS**: ahora puede probar y comprobar fácilmente sus credenciales de API de SMS en Adobe Journey Optimizer enviando un mensaje de ejemplo a un dispositivo designado.

* **Configuración**

   * **Compatibilidad con dominios dinámicos**: Journey Optimizer ahora admite la personalización en las direcciones URL de seguimiento para los dominios predefinidos enumerados en el nivel de configuración de canal.

   * **Compatibilidad con atributos personalizados con la URL de cancelación de suscripción de un solo clic**: con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un punto final personalizado externo definiendo su propio vínculo para cancelar la suscripción con un solo clic en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

     Para personalizar aún más el vínculo de cancelación de suscripción de un solo clic, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento.

* **Toma de decisiones**

   * **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar fragmentos a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante políticas de decisión.

* **Recorridos**

   * **Operaciones masivas de recorridos**: en su lista de recorridos, ahora puede seleccionar varios elementos. Una vez seleccionados, puede pausar o reanudar hasta 10 recorridos a la vez.
