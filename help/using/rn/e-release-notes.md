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
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 19%
---

# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de septiembre de 2026 {#sep-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se implementan en la fecha de lanzamiento de la versión, algunos pueden implementarse más adelante. Consulte la fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 22 y 23 de septiembre de 2026


<!--
### Onboarding {#sep-26-onboarding}

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
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### Recorridos {#sep-26-journeys}

Las siguientes capacidades y mejoras estarán disponibles en los recorridos en esta versión.

* **Se han reducido los eventos de paso para las actividades de espera y evento** - Ya no se generan eventos de paso para las actividades **wait** y **event** cuando el perfil no se ha procesado realmente en esa actividad. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

### Canales {#sep-26-channels}

Las siguientes funcionalidades y mejoras están llegando a los canales en esta versión.

<table>
<thead>
<tr>
<th><strong>Canal saliente personalizado (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Canales salientes personalizados</strong> permiten a los administradores llevar cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente a Journey Optimizer a través de un Generador de canales sin código. Una vez configurados, los canales personalizados están disponibles en cualquier campaña, recorrido y campaña orquestada, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza.</p>
<p>Con esta versión, los canales salientes personalizados también obtienen varias funciones nuevas:</p>
<ul>
<li>Utilice Journey Optimizer Decisioning en la carga útil del canal personalizado a través del Editor de Personalization, del mismo modo que en las experiencias basadas en código.</li>
<li>Aplique reglas empresariales a los canales personalizados, del mismo modo que ya lo hace en los canales nativos.</li>
<li>Seleccione canales personalizados en la lista de canales para campañas activadas por API, lo que anteriormente no era posible.</li>
<li>Defina un webhook de informes para un canal personalizado y adjúntelo a una configuración de canal para que pueda enriquecer los informes de Journey Optimizer con eventos de interacción.</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Canal de correo electrónico {#sep-26-email-channel}

Las siguientes funcionalidades y mejoras están llegando al canal de correo electrónico en esta versión.

<table>
<thead>
<tr>
<th><strong>Anular configuración de canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al crear los recorridos y las campañas, ahora puede anular los parámetros de correo electrónico derivados de la configuración de canal seleccionada directamente en el nivel de acción de recorrido o campaña.</p>
<p>Esto le permite personalizar los campos de encabezado del correo electrónico (<strong>De nombre</strong>, <strong>De prefijo de correo electrónico</strong>, <strong>Responder al nombre</strong> y <strong>Responder al correo electrónico</strong>), la dirección de ejecución y los valores de cancelación de suscripción a una lista, mediante atributos de perfil o datos contextuales para un control más preciso. En particular, esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa.</p>
</td>
</tr>
</tbody>
</table>

* **Anulación de la lista de supresión en el nivel de acción de correo electrónico**: Journey Optimizer ahora le permite anular el comportamiento de la lista de supresión directamente en el nivel de acción de correo electrónico en recorridos y campañas. Esto proporciona a los equipos más flexibilidad para las comunicaciones operativas o críticas para el cumplimiento que requieren una configuración de envío dedicada, al tiempo que conserva los controles de lista de supresión global existentes para todos los demás envíos. Esta mejora ayuda a las organizaciones a gestionar escenarios de excepción con precisión sin cambiar su modelo de gobernanza de supresión más amplio.

* **Validación de sintaxis de URL en la creación de correo electrónico**: Journey Optimizer ahora valida las URL anteriores en el flujo de creación de correo electrónico y ofrece una guía más clara cuando se detecta una sintaxis mal formada. Esto ayuda a los autores a detectar problemas antes de la finalización, reducir los errores de publicación y mejorar la confianza de envío.

### Diseñador de correo electrónico {#sep-26-email-designer}

Las siguientes funcionalidades y mejoras están llegando a Email Designer en esta versión.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con el modo oscuro para variantes de temas de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los temas de correo electrónico ahora admiten el modo oscuro, por lo que cada variante de color puede procesarse con una apariencia adaptada a los destinatarios que ven el correo electrónico en un cliente habilitado para el modo oscuro.</p>
<p>Cuando está habilitada, se genera automáticamente una paleta oscura predeterminada para cada variante y puede personalizarla con una paleta diferente o con sus propios colores personalizados, independientemente del diseño del modo claro, de modo que los cambios realizados en un modo no afectan al otro.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Importar plantillas de Dynamic Media directamente desde archivos de PSD en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El componente Dynamic Media de Designer de correo electrónico ahora le permite importar un archivo de Photoshop (PSD) directamente como una plantilla nueva, además de examinar las plantillas de Dynamic Media existentes. Arrastre y suelte un archivo de PSD en el componente y Adobe Journey Optimizer lo convertirá automáticamente en una plantilla de Dynamic Media almacenada en Dynamic Media, sin necesidad de realizar conversiones manuales ni viajes de ida y vuelta a través de Adobe Experience Manager. Una vez importada, puede editarla con el editor integrado de Dynamic Media, la misma experiencia que se utiliza para el contenido de Adobe Express en el Designer de correo electrónico.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevo componente de tabla en Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Designer de correo electrónico ahora incluye un <strong>componente Tabla</strong> integrado, que le permite estructurar el contenido en filas y columnas directamente dentro del correo electrónico. Arrastre y suelte el componente en el lienzo, personalice el número de filas y columnas y aplique estilo a cada celda de forma independiente para crear diseños claros y organizados sin depender del HTML personalizado.</p>
</td>
</tr>
</tbody>
</table>

* **Fuentes de reserva para fuentes personalizadas en temas de correo electrónico**: ahora puede definir una fuente de reserva para cualquier fuente personalizada (web) aplicada a través de temáticas de correo electrónico. Si el cliente de correo electrónico de un suscriptor no admite la fuente personalizada, Adobe Journey Optimizer muestra automáticamente la fuente de reserva especificada en lugar de dejar la opción a la fuente predeterminada del cliente de correo electrónico. Esto mantiene la tipografía del correo electrónico más cerca de las directrices de marca y reduce las incoherencias en el procesamiento de fuentes en los clientes de correo electrónico.
