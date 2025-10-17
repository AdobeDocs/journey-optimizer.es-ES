---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3eb73751fdb746dd2659e31c1b776fe2d767809f
workflow-type: tm+mt
source-wordcount: '2478'
ht-degree: 64%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales.  En la sección [Últimas actualizaciones](#updates-rn) dedicada se destacan las nuevas funcionalidades y mejoras que se implementan en la producción, por lo que siempre se le informa de todos los cambios en tiempo real. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas previas al lanzamiento de octubre de 2025 {#oct-25-10-rn}

**Las notas anteriores al lanzamiento que se indican a continuación están sujetas a cambios sin previo aviso hasta la fecha de lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: jueves, 22 de octubre de 2025

### Nuevas funciones {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Horas tranquilas/Exclusiones basadas en el tiempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para los canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento.</p>
<p>Puede aplicar horas tranquilas a través de conjuntos de reglas, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso. Simplificando estos procesos.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitorización y creación de informes de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta función proporciona una mejor visibilidad del estado y la ejecución del recorrido, incluido el estado del ciclo vital y las alertas de rendimiento. Ahora puede comprender rápidamente cuándo, dónde y por qué se produce una situación anómala en una acción personalizada.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Nueva API para recuperar campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible una nueva API de Journey Optimizer que le permite recuperar e inspeccionar mediante programación datos relacionados con la campaña, como detalles, versiones y configuraciones.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevos conectores de origen para aplicaciones de fidelidad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los nuevos conectores de origen ya están disponibles en Adobe Experience Platform para las aplicaciones de fidelidad Talon.One, Capillary y Kobie. Estos conectores le permiten transmitir sin problemas datos de lealtad a Adobe Experience Platform y aprovechar estos datos en Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir directivas de Decisión a recorridos de correo electrónico y campañas. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de Decisioning para devolver dinámicamente el mejor contenido para entregar a cada miembro del público.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo de alto rendimiento para campañas de correo electrónico activadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible un nuevo modo de alto rendimiento en las campañas activadas por API. Este modo está diseñado para mensajes a gran escala en tiempo real (hasta 5000 transacciones por segundo) y proporciona una mayor disponibilidad con una latencia más baja.</p>
<p>Esta funcionalidad solo está disponible para el canal de correo electrónico, para organizaciones que han adquirido la oferta de complemento de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reglas de segmentación reutilizables</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite crear reglas a partir de un menú de interfaz de usuario dedicado y aprovecharlas al crear objetivos, ya sea como parte de la optimización de contenido en una campaña o un recorrido, en la actividad Optimizar recorrido.</p>
<p>Actualmente, las reglas de segmentación están disponibles para las organizaciones que han adquirido la oferta de complementos de Decisioning y para las demás organizaciones (disponibilidad limitada).</p>
<p>Esta capacidad se implementará progresivamente para todos los clientes. Mientras tanto, póngase en contacto con su representante de Adobe para obtener acceso.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<p>Esta funcionalidad, que se publicó anteriormente en la versión beta, ya está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevas alertas de Recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay nuevas alertas preconfiguradas disponibles para controlar la ejecución del recorrido:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Tasa de descartes de perfiles superada</a>: la proporción de descartes de perfiles respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral.</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Tasa de errores de acción personalizada superada</a>: la proporción de errores de acción personalizada respecto a las llamadas HTTP correctas durante los últimos 5 minutos ha superado el umbral.</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Tasa de error de perfil superada</a>: la proporción de perfiles en error respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral.</li></ul> <p>Puede modificar los valores de umbral y suscribirse a alertas de nivel de recorrido individual o global.</p>
<p>Para obtener más información, consulte la <a href="../reports/alerts.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 14 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ayudante de metadatos de ejecución</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay una nueva función de ayuda executionMetadata disponible en el editor de personalización. Permite anexar información contextual a cualquier acción nativa y capturarla en un conjunto de datos para exportarla a sistemas externos.</p>
<p>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p>Para obtener más información, consulte la <a href="../personalization/functions/helpers.md#execution-metadata">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 13 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>¡Experimentation Agent está aquí!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la tecnología <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, el agente de experimentación está disponible en Journey Optimizer. </p>
<p>Experimentation Agent es una herramienta con tecnología de IA que moderniza la forma de ejecutar y administrar experimentos digitales en sitios web, correos electrónicos, mensajes push y aplicaciones. Ayuda a ejecutar experimentos de forma más eficaz, organizar los objetivos comerciales y generar perspectivas procesables, resaltando lo que funcionó, lo que no y dónde experimentar a continuación.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=es" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 10 de octubre de 2025</p>
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
<li>Para cualquier tamaño o volumen adicional, puede comprar un complemento de archivos PDF adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.</li>
</ul>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/pdf-attachments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 30 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pública para recuperar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva API de Journey Optimizer para recuperar recorridos y sus objetos asociados, como campañas y superficies.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 25 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>




<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Mejoras {#updates-improvements}

**Campo de ejecución para el canal de WhatsApp**

Además de correo electrónico y SMS, puede saber cómo actualizar el campo de ejecución predeterminado para sus envíos de WhatsApp en el nivel de zona protegida. También es posible anular el campo de ejecución definido globalmente cambiándolo en los parámetros avanzados de la actividad de recorrido de WhatsApp o en la configuración del canal de WhatsApp. <!-- [Read more](../FILE.md) -->

**Compatibilidad con atributos personalizados para la dirección Mailto (cancelar la suscripción)**

Con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer puntos de conexión personalizados externos definiendo su propio vínculo de cancelación de suscripción de un clic y una dirección de correo electrónico de cancelación de suscripción personalizada en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar LA suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

Para personalizar aún más los extremos personalizados, ahora puede definir atributos personalizados que también se adjuntarán al evento de consentimiento. [Más información](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esta funcionalidad ya está disponible para la URL **[!UICONTROL Cancelar la suscripción con un solo clic]** desde agosto de 2025 y ahora está disponible para la opción **[!UICONTROL Mailto (cancelar la suscripción)]** en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Fecha de disponibilidad: 6 de octubre de 2025

## Notas de la versión de septiembre de 2025 {#latest-rn}

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
<p>Para obtener más información, consulte la <a href="../content-management/experiment-accelerator.md">documentación detallada</a>.</p>
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


### Mejoras {#sept-25-9-improvements}

* **Compatibilidad con webhook para campañas activadas por API**\
  Las campañas activadas por API ahora admiten webhooks. Configure una URL de gancho web para recibir actualizaciones de estado en tiempo real para cada mensaje, mejorando la observabilidad y permitiendo una monitorización y automatización sin problemas. [Más información](../configuration/feedback-webhooks.md)

  Fecha de disponibilidad: 29 de septiembre de 2025

* **Compatibilidad con mTLS para el canal SMS**
Al configurar un proveedor de SMS personalizado, ahora tiene la opción de habilitar la autenticación TLS mutua (mTLS), lo que requiere que tanto el cliente como el servidor confirmen mutuamente sus identidades antes de establecer una conexión segura. [Más información](../sms/sms-configuration-custom.md) - Fecha de disponibilidad: 23 de septiembre de 2025

* **Esquemas basados en modelos**\
  Ahora puede utilizar esquemas basados en modelos para satisfacer sus necesidades de modelado relacional en campañas orquestadas. [Más información](../orchestrated/gs-schemas.md) - Fecha de disponibilidad: 23 de septiembre de 2025

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

* **Webhooks**: Esta versión incorpora las siguientes mejoras para Webhooks al configurar un proveedor de SMS personalizado:

   * Ahora puede definir el propósito de su webhook, ya sea Entrante o Comentarios, según el tipo de datos que desee capturar. [Más información](../sms/sms-configuration-custom.md#webhook) - Fecha de disponibilidad: 23 de septiembre de 2025

   * La interfaz para configurar palabras clave se ha mejorado para facilitar la configuración. [Más información](../sms/sms-configuration-custom.md#webhook) - Fecha de disponibilidad: 23 de septiembre de 2025

* **SMS**

   * Al configurar un proveedor de SMS personalizado, ahora puede definir una palabra clave **Default** que se usa cuando un SMS entrante contiene una palabra clave no reconocida. También puede crear palabras clave **Custom** para acciones específicas. [Más información](../sms/sms-configuration-custom.md) - Fecha de disponibilidad: 23 de septiembre de 2025

   * Ahora puede acceder a las respuestas de palabras clave de entrada no definidas enviadas mediante un mensaje SMS, incluidos los errores tipográficos, las palabras o las frases que no están definidos explícitamente en la configuración. Se almacenan en el conjunto de datos **AJO Email Tracking Experience Event**, en **InboundMessage** durante 13 meses. Solo disponible con Sinch, Infobip y el proveedor de SMS personalizado. - Fecha de disponibilidad: 23 de septiembre de 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


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
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
