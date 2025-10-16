---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: c2b990a413762dccc71e4152cbb145a51a5d073e
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 42%

---

# Notas de versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).


## Notas previas al lanzamiento de octubre de 2025 {#25-10-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: 21-22 de octubre de 2025

### Nuevas funciones {#oct-25-10-features}



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

<table>
<thead>
<tr>
<th><strong>Mensajería básica de RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la nueva oferta de complementos básicos de RCS, ahora puede ofrecer mensajería básica de servicios de comunicaciones enriquecidos (RCS) en Journey Optimizer, lo que permite las siguientes funciones de mensajería mejoradas sujetas a la asistencia geográfica y del proveedor:</p>
<ul>
<li><strong>Compatibilidad con remitente verificado y con marca:</strong> Envíe mensajes utilizando perfiles comerciales verificados con elementos de marca (logotipo, nombre del remitente, etc.).</li>
<li><strong>Información sobre la entrega de mensajes:</strong> Reciba informes de entrega detallados que incluyan actualizaciones del estado del mensaje (por ejemplo, enviado, entregado, leído).</li>
<li><strong>Seguimiento de vínculos:</strong> Incruste y rastrea direcciones URL en mensajes RCS para el análisis de participación.</li>
<li><strong>Reserva a SMS:</strong> Reserva automática a SMS cuando el dispositivo del destinatario no admite RCS o no se puede acceder temporalmente a través de RCS.</li>
<li><strong>Composición básica de mensajes:</strong> Envíe mensajes RCS básicos basados en texto.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El canal de correo postal ya está disponible en campañas orquestadas. La actividad de correo directo facilita el envío de correo directo dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación del archivo de extracción requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de la campaña orquestada para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

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
<p> Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
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
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentación detallada</a>.</p>
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


### Mejoras

**Seleccionar reglas reutilizables en Segmentación**

Ahora puede aprovechar el generador de reglas al utilizar reglas de segmentación con la función Optimización de mensajes en recorridos y campañas. <!-- [Read more](../FILE.md) -->

**Campo de ejecución para el canal de WhatsApp**

Además de Correo electrónico y SMS, ahora es posible actualizar el campo de ejecución predeterminado de WhatsApp. También es posible anular el campo de ejecución definido globalmente en los parámetros avanzados de la actividad de recorrido de WhatsApp o en la configuración del canal de WhatsApp. <!-- [Read more](../FILE.md) -->

**Permisos**

**Nuevas alertas de recorrido**

Hay nuevas alertas preconfiguradas disponibles para los recorridos: [Tasa de descartes de perfiles superada](../reports/alerts.md#alert-discard-rate) (proporción de descartes de perfiles para perfiles introducidos en el umbral excedido de los últimos 5 minutos), [Tasa de errores de acción personalizada superada](../reports/alerts.md#alert-custom-action-error-rate) (proporción de errores de acción personalizados para llamadas HTTP correctas en el umbral excedido de los últimos 5 minutos) y [Tasa de errores de perfil superada](../reports/alerts.md#alert-profile-error-rate) (proporción de perfiles en error para perfiles ingresados en el umbral excedido de los últimos 5 minutos). Puede modificar los valores de umbral y suscribirse a alertas de nivel de recorrido individual o global.

Fecha de disponibilidad: 14 de octubre de 2025

**Compatibilidad con atributos personalizados para la dirección Mailto (cancelar la suscripción)**

Con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer puntos de conexión personalizados externos definiendo su propio vínculo de cancelación de suscripción de un clic y una dirección de correo electrónico de cancelación de suscripción personalizada en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo Cancelar LA suscripción, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

Para personalizar aún más los extremos personalizados, ahora puede definir atributos personalizados que también se adjuntarán al evento de consentimiento. [Más información](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esta funcionalidad ya está disponible para la URL **[!UICONTROL Cancelar la suscripción con un solo clic]** desde agosto de 2025 y ahora está disponible para la opción **[!UICONTROL Mailto (cancelar la suscripción)]** en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Fecha de disponibilidad: 6 de octubre de 2025