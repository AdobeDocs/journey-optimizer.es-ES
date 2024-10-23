---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 0e8c9927f7516abf1927606fd8236b8506b54c96
workflow-type: tm+mt
source-wordcount: '1775'
ht-degree: 43%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión preliminar de octubre de 2024 {#e-2024}

**Fecha de la versión**: 29 y 30 de octubre de 2024

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<table>
<thead>
<tr>
<th><strong>Bloqueo de contenido de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora permite bloquear contenido en plantillas de correo electrónico, ya sea bloqueando la plantilla completa o estructuras y componentes específicos. Esto le permite evitar ediciones o eliminaciones no intencionadas, lo que le proporciona un mayor control sobre la personalización de las plantillas y mejora la eficacia y fiabilidad de sus campañas de correo electrónico.</p>
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Aprobaciones en recorridos y campañas (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con las políticas de aprobación, ahora puede configurar un proceso de aprobación dentro de Journey Optimizer que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de que se activen.</p>
<p>Antes disponibles para un conjunto de organizaciones (LA), las políticas de aprobación ya están disponibles para todos los usuarios (GA).</p>
<p>Para obtener más información, consulte la <a href="../test-approve/gs-approval.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalización de la configuración de correo electrónico (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir subdominios dinámicos y parámetros de encabezado personalizados al crear configuraciones de canal de correo electrónico para disponer de mayor flexibilidad y control sobre la configuración del correo electrónico.</p>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), la personalización de la configuración de correo electrónico ya está disponible para todos los usuarios (GA).</p>
<p>Para obtener más información, consulte la <a href="../email/surface-personalization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo de edición no visual para el diseñador web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como alternativa al diseñador web de Journey Optimizer, ahora puede agregar modificaciones al sitio web mediante un editor no visual. Permite introducir los cambios manualmente sin abrir las páginas en el editor visual.
Este modo de edición no visual resulta útil si no puede instalar extensiones de explorador como el Asistente visual de Adobe Experience Cloud, necesario para cargar las páginas en el diseñador web.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentación en recorridos (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer, que ya estaba disponible en las campañas, ahora admite experimentos en los recorridos. Los experimentos son ensayos aleatorios, lo que en el contexto de las pruebas en línea significa que expone a algunos usuarios seleccionados aleatoriamente a una variación determinada de un mensaje y a otro conjunto de usuarios seleccionados aleatoriamente a otra variación o tratamiento. Después de la exposición, puede medir las métricas de resultado que le interesan, como aperturas de correos electrónicos, suscripciones o compras.</p>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), los experimentos en recorridos ya están disponibles para todos los usuarios (GA).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Conjuntos de reglas (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas de límite de frecuencia granulares y aplicarlas a sus mensajes o recorridos a través de conjuntos de reglas. Esta nueva funcionalidad le permite controlar la frecuencia con la que las audiencias reciben un mensaje configurando reglas en canales múltiples que excluyen automáticamente los perfiles saturados de los mensajes y las acciones.</p><p>También le permite limitar el número de recorridos por día, semana o mes, así como controlar el número de recorridos simultáneos que se ejecutan simultáneamente.</p>
<p> Los conjuntos de reglas están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de esta función.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mensajes multilingües en recorridos y campañas (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido sin esfuerzo en varios idiomas dentro de una sola campaña o recorrido. Con esta función, puede cambiar entre idiomas al editar su campaña o su recorrido, lo que optimiza todo el proceso de edición y mejora su capacidad para administrar de forma eficaz el contenido multilingüe.</p>
<p>Anteriormente disponibles para un conjunto de organizaciones (LA), los mensajes multilingües ya están disponibles para todos los usuarios (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Journey Optimizer y tinta móvil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede integrar Movable Ink Da Vinci y Adobe Journey Optimizer. Con esta nueva integración puede: </p>
<p><ul><li>Aproveche las potentes capacidades del producto Da Vinci de Movable Ink para ensamblar y personalizar las variaciones de correo electrónico para las campañas por lotes</li>
<li>Acelere los flujos de trabajo de los profesionales para los clientes de Journey Optimizer que utilizan Da Vinci para la creación y AJO para la optimización y el envío</li>
<li>Optimizar los modelos Da Vinci con datos de Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencia actualizada de creación de informes (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 16 de octubre de 2024</p>
<p>La creación de informes de Journey Optimizer ya está disponible de forma general (GA) y ofrece una interoperabilidad mejorada con funciones de Customer Journey Analytics, estandarización de los informes en ambas plataformas y mejora de la coherencia y fiabilidad de los datos. Esta integración perfecta entre Journey Optimizer y Customer Journey Analytics proporciona una visión más clara de las métricas de rendimiento, lo que permite a los usuarios tomar decisiones más informadas.</p>
<p>Con la disponibilidad general, se introducen cuatro nuevas funciones: la capacidad de crear métricas sencillas, crear y publicar audiencias, hacer preguntas específicas mediante Insight Builder y programar informes para que se envíen automáticamente por correo electrónico a los destinatarios clave.</p>
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: La experiencia actual de creación de informes se eliminará a partir de enero de 2025. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Recomendamos que se familiarice con las nuevas funciones y características para garantizar una transición sin problemas. <a href="../reports/report-gs-cja.md">Aprenda a empezar con la nueva interfaz de creación de informes de Journey Optimizer</a></p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias basadas en código en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 1 de octubre de 2024</p>
<p>Con el canal de experiencia basado en código, Adobe Journey Optimizer le permite realizar personalizaciones y pruebas avanzadas para cualquiera de sus propiedades de entrada, lo que permite ofrecer experiencias adaptadas en diversos puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, consolas de vídeo, servicios conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, dispositivos IoT y mucho más. El canal de experiencia basado en código ya está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../code-based/create-code-based.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias web en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponible desde el 1 de octubre de 2024</p>
<p>Con el canal web, Adobe Journey Optimizer permite personalizar la experiencia web que ofrece a sus clientes a través de recorridos web entrantes. El canal web ahora está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../web/create-web.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Canal de SMS**

Se han introducido mejoras en los SMS para mejorar sus funciones de mensajería:

* Puede definir y administrar palabras clave únicas para sus campañas y recorridos de SMS, lo que permite una comunicación más personalizada y eficaz.
* Puede crear y enviar un mensaje SMS predeterminado cuando no se reconozca una palabra clave.

**Administración de conflictos y prioridades**

* **Límite de frecuencia por recorrido**: ahora puede crear conjuntos de reglas para aplicarlos a sus recorridos, lo que le permite limitar el número de recorridos por día, semana o mes, así como controlar el número de recorridos simultáneos que se ejecutan simultáneamente.

* **Puntuación de prioridad**: ahora puede asignar una puntuación de prioridad a una campaña o un recorrido, de 0 a 100. Un número mayor indica una prioridad mayor. Cuando dos campañas o recorridos utilizan la misma configuración de canal, Journey Optimizer selecciona el que tenga la puntuación de prioridad más alta. Si las campañas tienen la misma puntuación, se elige la campaña modificada más recientemente. La puntuación de prioridad está disponible para todos los canales entrantes en las campañas y para el canal en la aplicación en los recorridos.

* **Ver conflictos**: un nuevo botón **Ver conflictos** en recorridos y campañas ahora le permite comprobar si hay una posibilidad de superposición con otros recorridos o campañas, como la fecha de inicio, la audiencia de destino o la configuración de canal seleccionada.

>[!AVAILABILITY]
>
>Las funciones de administración de conflictos y prioridades están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de esta función.

**Gestión de decisiones**

* **Auditorías**: la pestaña **Registro de cambios** que le permite ver todos los cambios realizados en una oferta o que se ha eliminado una decisión. Los cambios relacionados con ofertas y decisiones ahora se pueden ver en el menú **Auditorías**.


Configuración de ****

* **Personalización de la configuración del canal**: al usar una configuración personalizada en una campaña o un recorrido, ahora puede obtener una vista previa del contenido del correo electrónico para comprobar posibles errores con la configuración dinámica que definió.

**Recorridos**

* **Experimento de rutas en recorridos**: con el experimento de rutas de recorridos, ahora puede definir y rastrear métricas clave para sus rutas de recorridos, lo que le permite medir el impacto de sus actividades y proporcionar una perspectiva más clara de su rendimiento.

* **Número máximo de recorridos activos**: Journey Optimizer ahora tiene un mecanismo de protección de 500 recorridos activos en zonas protegidas de producción, en lugar de 100. El número de recorridos activos es visible en el lienzo de recorrido. <!-- DOCAC-10977-->

* **Protección de tiempo de vida**: a partir del 1 de noviembre de 2024, se aplicará una protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer de la siguiente manera:

   * 90 días para datos en el almacén de perfiles
   * 13 meses para los datos del lago de datos

  Además, en ese momento, la segmentación de streaming ya no admitirá el uso de eventos de envío y comentarios de conjuntos de datos de seguimiento y comentarios. Hemos recomendado no utilizar esos eventos para la segmentación de streaming durante un tiempo y ahora los deshabilitaremos por completo.

   * Este cambio solo restringe el uso de eventos de envío/apertura en la segmentación de flujo continuo; los eventos de clic se pueden seguir utilizando en un segmento de flujo continuo. Además, los eventos de envío/apertura se pueden seguir utilizando en un segmento por lotes.
   * Los datos de seguimiento se seguirán recopilando. Este cambio no afecta al seguimiento. Todavía puede rastrear a quién se envió un correo electrónico y quién hizo clic en un correo electrónico.
   * Los eventos de reacción en Recorridos no se ven afectados por este cambio.

* **Parámetros en acciones personalizadas** (Fecha de disponibilidad: 3 de octubre de 2024): ahora se admiten parámetros nulos y opcionales en las acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Gobernanza de datos y políticas de consentimiento**: fecha de disponibilidad: 7 de octubre de 2024

* La aplicación de las **políticas de control de datos** ahora se aplica en todos los canales de Journey Optimizer. Para los clientes que han creado políticas en Adobe Experience Platform, estas se aplican a las acciones de marketing como parte de la configuración de canales. Al crear contenido con una configuración, el sistema comprueba todos los campos de personalización para detectar cualquier infracción de la gobernanza de datos. Si se encuentra una infracción, no será posible publicar un recorrido o una campaña. [Más información](../action/action-privacy.md)

* Las **políticas de consentimiento personalizado** ahora se aplican a todos los canales de Journey Optimizer. Al aplicar la ley antes de enviar un mensaje o de entregar una experiencia entrante, el sistema comprueba que el usuario haya dado su consentimiento para utilizar campos de personalización en el contenido que va a recibir. Si no se da ningún consentimiento, la experiencia no se muestra. [Más información](../action/consent.md)

  >[!NOTE]
  >
  >Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas sobre el programa **Healthcare Shield** y el programa **Privacy and Security Shield**.

**Públicos**: fecha de disponibilidad: 8 de octubre de 2024

* Al segmentar el público de un archivo CSV, ahora puede utilizar atributos del archivo en el editor de personalización y en el generador de reglas de recorridos y campañas. [Más información](../audience/about-audiences.md)

* El uso de públicos y atributos de cargas personalizadas (archivos CSV) no está disponible en la actualidad para su uso con el programa Healthcare Shield ni Privacy and Security Shield.



