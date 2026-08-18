---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
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
source-git-commit: fbbab8c264a03f2170f4ab37fa89f1b4e77d6e50
workflow-type: tm+mt
source-wordcount: 1040
ht-degree: 18%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de agosto de 2026 {#august-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 18 y 19 de agosto de 2026

<!--
### Onboarding {#august-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Recorridos {#august-26-journeys}

Las siguientes capacidades y mejoras estarán disponibles en los recorridos en esta versión.

<table>
<thead>
<tr>
<th><strong>Recorrido de nivel de resistencia (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un grupo de exclusión para los recorridos directamente desde las propiedades de recorrido. Una exclusión es un porcentaje configurable de la audiencia de destino que se excluye de la entrada al recorrido y que no recibe ninguna comunicación. Al comparar los perfiles de exclusión con los perfiles activos en los informes de Customer Journey Analytics, puede medir el alza incremental, el verdadero impacto, que ofrece su recorrido.</p>
<p> Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Agregar nueva función dateDiff en el editor de expresiones de recorrido** - El editor de expresiones de recorrido ahora incluye la función `dateDiff`, que calcula la diferencia entre dos fechas en número de días. Esta función es útil para lógica basada en tiempo, como la creación de plazos, el cálculo de las duraciones del ciclo vital de los clientes o la creación de temporizadores de cuenta atrás en condiciones de recorrido. <!-- Documentation link: TBD -->

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido, ahora aparecen en el encabezado del recorrido junto al distintivo de estado. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado. <!-- Documentation link: TBD -->

### Canales {#august-26-channels}

En esta versión de Campaign se incluye la siguiente mejora:

* **Metadatos de ejecución de actividades activas (executionMetadata)**: las campañas de actividades activas activadas por API (transaccionales y de marketing) ahora admiten un campo executionMetadata opcional en cada destinatario. Esto permite adjuntar datos de clave/valor personalizados, como un ID de pedido, un nivel de fidelidad o un código de región, a una ejecución.

### Campañas {#august-26-camp}

En esta versión de Campaign se incluyen las siguientes funcionalidades y mejoras.

<table>
<thead>
<tr>
<th><strong>Simulación de experiencia entrante en campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular acciones de canal entrante en campañas de acción antes de lanzarlas. Utilice el modo de simulación para probar la configuración con usuarios simulados y previsualizar la experiencia procesada, incluida una URL y un código QR generados, para poder validar reglas, decisiones y el procesamiento de contenido de principio a fin.</p>
<p>Actualmente, esta funcionalidad está en versión beta privada y está disponible para un conjunto limitado de organizaciones. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Rediseño del flujo de creación de campañas de acción**: el flujo de creación de campañas de acción de Adobe Journey Optimizer se ha rediseñado para ofrecer una experiencia de usuario significativamente más intuitiva, eficiente y fluida.

* **Carpetas para campañas de acción**: ahora puede organizar sus campañas de acción en carpetas para mejorar la navegación y la administración en la interfaz. <!-- Documentation link: TBD -->

<!--* **Brand alignment score in Action Campaign dashboard** - You can now assess your brand alignment score directly within your Action Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.  Documentation link: TBD -->

* **Anular los campos de ejecución predeterminados en las campañas de acción**. Anteriormente disponible en el nivel de recorrido, ahora puede anular los campos de ejecución predeterminados configurados globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de la campaña de acción. <!-- Documentation link: TBD -->

### Campañas orquestadas {#august-26-oc}

Las siguientes funcionalidades y mejoras están llegando a Orchestrated Campaigns en esta versión.

<table>
<thead>
<tr>
<th><strong>Asistencia de Horas tranquilas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar Horas de silencio. Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para evitar que los mensajes se envíen durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento en los casos de uso de la orquestación de la campaña.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío mediante olas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede programar que los mensajes salientes se entreguen en lotes controlados a lo largo del tiempo. Ideal para campañas de gran volumen o en las que el tiempo es un factor importante, la entrega de olas también ofrece una mejor capacidad de entrega y ayuda a mantener una sólida reputación de remitente, ya que reduce el riesgo de ser marcado como correo no deseado. </p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Capacidad para administrar dimensiones de destino de perfil**. Ahora puede eliminar un Dimension de destino de perfil o editar e intercambiar su área de nombres de identidad configurada, lo que proporciona mayor control y flexibilidad sobre las configuraciones de datos. <!-- Documentation link: TBD -->

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña (disponibilidad limitada)**: las campañas orquestadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos el nombre del remitente, el prefijo del correo electrónico remitente, el nombre del remitente y el correo electrónico de respuesta, así como la dirección de ejecución, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer a nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso.
Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada).
  <!-- Documentation link: TBD -->

* **Simplificación de la dimensión de destino**: la dimensión de segmentación activa ahora se muestra en el lienzo del flujo de trabajo, para que pueda ver qué dimensión utiliza una actividad de canal. El flujo de segmentación de varias entidades es más sencillo, ya que ya no necesita una actividad &quot;Change dimension&quot; independiente. Además, ahora puede elegir explícitamente si los mensajes se envían en el nivel de perfil o en un nivel de dimensión secundario. <!-- Documentation link: TBD -->



### Toma de decisiones {#august-26-decisioning}

En esta versión de, se incluyen las siguientes funcionalidades y mejoras en Decisioning.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Decisioning en el canal web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning ya está disponible para el canal Web. Puede utilizar las políticas de decisión directamente en el editor visual web para entregar las ofertas más relevantes a cada visitante.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Límite de frecuencia de nivel de ubicación en Decisioning**: las reglas de límite de frecuencia en Decisioning ahora se pueden vincular a ubicaciones individuales, lo que le proporciona un control más preciso sobre la frecuencia con la que se muestra una oferta en una superficie determinada. Hay dos modos disponibles: límite específico de la ubicación, que define un límite que se aplica solo cuando la oferta se muestra en una ubicación seleccionada, y límite por ubicación, que aplica un límite de forma independiente en cada ubicación en la que aparece la oferta, de modo que cada ubicación mantiene su propio contador de límite. Tenga en cuenta que el límite relacionado con la ubicación no se aplica a las ofertas restringidas mediante reglas basadas en datos de Adobe Experience Platform. <!-- Documentation link: TBD -->

### Administración {#august-26-administration}

La siguiente mejora se presenta para la administración en esta versión.

* **Proceso OTP del bucle de comentarios para subdominios personalizados**: el proceso de configuración del subdominio personalizado del Bucle de comentarios (FBL) se ha mejorado al mostrar la contraseña única (OTP) de Yahoo sender hub directamente dentro de la interfaz de usuario del producto. Los usuarios ahora pueden recuperar y mostrar automáticamente el OTP generado durante la verificación de propiedad del dominio del centro de remitentes de Yahoo. <!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


