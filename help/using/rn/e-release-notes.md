---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 29%

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
<th><strong>Canal de correo postal en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a Campañas, el canal de correo postal ahora está disponible en el lienzo de recorrido, lo que le permite incorporar el correo postal en sus recorridos. Ahora, el correo postal se puede utilizar en escenarios de recorrido por lotes y 1:1, con compatibilidad con la configuración de extracción de archivos y los ajustes de frecuencia basados en el tiempo.</p>
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
<th><strong>Nueva función de ayuda de metadatos de ejecución</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay una nueva función de ayuda executionMetadata disponible en el editor de personalización. Permite anexar información contextual a cualquier acción nativa y capturarla en un conjunto de datos para exportarla a sistemas externos.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Fecha de disponibilidad: 13 de octubre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agente de experimento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experimentation Agent es una herramienta con tecnología de IA que moderniza la forma de ejecutar y administrar experimentos digitales en sitios web, correos electrónicos, mensajes push y aplicaciones. Creado en la plataforma de IA de Adobe Experience Platform y en las herramientas de experimentación, el agente de experimentación le ayuda a ejecutar experimentos de forma más eficiente, organizar los objetivos comerciales y generar perspectivas procesables, resaltando lo que funcionó, lo que no y dónde experimentar a continuación.</p>
<p>Como parte de la nueva función de Experimentation Accelerator, el agente ofrece:</p>
<ul>
<li><strong>Rendimiento:</strong> una visión clara de lo que ocurrió en el experimento</li>
<li><strong>Información:</strong> una explicación de por qué se produjeron los resultados</li>
<li><strong>Oportunidades:</strong> orientación sobre las siguientes acciones a realizar</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Fecha de disponibilidad: 9 de octubre de 2025</p>
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
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Fecha de disponibilidad: 25 de septiembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

- **Campañas, Experience Decisioning, Recorridos**
   - **Seleccionar reglas reutilizables en segmentación**: ahora puede aprovechar el generador de reglas al usar reglas de segmentación con la característica de optimización de mensajes en recorridos y campañas. <!-- [Read more](../FILE.md) -->

- **Canal - WhatsApp**
   - **Campo de ejecución para el canal de WhatsApp**: además del correo electrónico y los SMS, ahora es posible actualizar el campo de ejecución predeterminado de WhatsApp. También es posible anular el campo de ejecución definido globalmente en los parámetros avanzados de la actividad de recorrido de WhatsApp o en la configuración del canal de WhatsApp. <!-- [Read more](../FILE.md) -->

- **Permisos**
   - **El creador de Recorrido/campaña no debería poder aprobar**. Se agregó una opción al crear o establecer la directiva de aprobación para evitar que los creadores de Recorrido/campaña aprueben sus propios objetos. <!-- [Read more](../FILE.md) -->

- **Canal: Push**
   - **Actividades en vivo móviles - Beta privada** - Las actividades en vivo proporcionan actualizaciones en tiempo real y experiencias interactivas dentro de las aplicaciones móviles, lo que permite a los usuarios mantenerse informados sobre eventos o tareas en curso directamente en la pantalla de su dispositivo. Esta función mejora la participación al ofrecer información en directo, como el seguimiento del progreso, las actualizaciones de eventos o el contenido interactivo, sin que sea necesario que los usuarios abran la aplicación. <!-- [Read more](../FILE.md) -->

- **Recorridos**
   - **Nuevas alertas de Recorrido** - Fecha de disponibilidad: 14 de octubre de 2025
Hay nuevas alertas preconfiguradas disponibles para los recorridos: Tasa de descarte de perfil excedida (proporción de descartes de perfil para perfiles introducidos en el umbral excedido de los últimos 5 minutos), Tasa de error de acción personalizada excedida (proporción de errores de acción personalizados para llamadas HTTP correctas en el umbral excedido de los últimos 5 minutos), Tasa de error de perfil excedida (proporción de perfiles en error para perfiles introducidos en el umbral excedido de los últimos 5 minutos). <!-- [Read more](../FILE.md) -->

- **Configuración**
   - **Compatibilidad con atributos personalizados con URL para cancelar la suscripción con un clic**. Fecha de disponibilidad: 6 de octubre de 2025
Con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un punto final personalizado externo definiendo su propio vínculo de cancelación de suscripción de un solo clic en la configuración de correo electrónico. Cuando los destinatarios hacen clic en el vínculo unsubscribe, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento. Para personalizar aún más el vínculo de cancelación de suscripción, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento. Esta funcionalidad ya está disponible para la URL de cancelación de suscripción con un solo clic desde agosto de 2025 y ahora se libera para la opción Mailto (cancelación de suscripción) en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso. <!-- [Read more](../FILE.md) -->

- **Canal: correo electrónico**
   - **Archivos adjuntos de PDF a correos electrónicos**. Fecha de disponibilidad: 30 de septiembre de 2025
Ahora puede adjuntar un archivo PDF estático a un mensaje de correo electrónico enviado con Journey Optimizer. Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año. El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB. Para cualquier tamaño o volumen adicional, puede adquirir el complemento de datos adjuntos de PDF. Para obtener más información, póngase en contacto con su representante de Adobe.

  >[!AVAILABILITY]
  >
  >Esta mejora, lanzada anteriormente en disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).

  <!-- [Read more](../FILE.md) -->

