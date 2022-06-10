---
title: Notas de la versión 2022
description: Notas de la versión de Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: f5e3b7cee816be420a09abd8aa9404faaccfec87
workflow-type: ht
source-wordcount: '1069'
ht-degree: 100%

---

# Notas de la versión 2022 {#release-notes-2022}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzado en 2022.

Las notas de la última versión están disponibles [en esta página](release-notes.md).

## Versión de abril de 2022 {#april-2022-release}

### Mejoras

**Páginas de destino**

* **Nueva opción para casillas de verificación de inclusión/exclusión.** Ahora puede insertar una sola casilla de verificación para la inclusión/exclusión en las páginas de destino de suscripción. Los usuarios deben marcar la casilla de verificación para el consentimiento (inclusión) y desmarcar para eliminar su consentimiento (exclusión). [Más información](../landing-pages/design-lp.md#define-lp-specific-content)

* **Rellenar previamente campos de páginas de destino.** Ahora es posible proporcionar a los usuarios la capacidad de rellenar previamente los campos de la página de aterrizaje con información del perfil. [Más información](../landing-pages/create-lp.md#configure-primary-page)

**Administración de decisiones**

* **API de decisiones en Edge.** La API de Edge Decisioning puede entregar y procesar ofertas personalizadas que se administran en Offer decisioning. Puede crear sus ofertas y otros objetos relacionados mediante la interfaz de usuario (IU) o las API de Offer decisioning. [Más información](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administración**

* **Duración de envío de PTR.** La duración de la edición de PTR para que sea efectiva es ahora de unas pocas horas. [Más información](../configuration/ptr-records.md#processing)

**Diseño de correo electrónico**

* **Veinte nuevas plantillas de correo electrónico** ya están disponibles para diseñar el contenido de su correo electrónico en Journey Optimizer.

**Interfaz de usuario**

* **Ayuda contextual en la interfaz de usuario de Journey Optimizer.** Se han agregado vínculos de ayuda contextual a varias páginas en Journey Optimizer. Cuando esté disponible, haga clic en el icono “i” para ver una descripción rápida de la funcionalidad actual y acceder a los artículos relacionados.

**Integración con Adobe Campaign Standard**

Como cliente de Adobe Campaign Standard, ahora puede enviar correos electrónicos, notificaciones push y SMS mediante Journey Optimizer. Utilice las nuevas acciones integradas para aprovechar las capacidades de mensajería transaccional de Campaign Standard en Journey Optimizer.  [Más información](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Lanzamiento de marzo de 2022 {#march-2022-release}

### Mejoras

**Recorridos**

* Para evitar tener campos innecesarios en el esquema de perfil unificado, el esquema de Evento de paso de recorrido ya no está habilitado para perfiles de forma predeterminada. Si es necesario, puede activarlo. [Más información](../reports/sharing-overview.md)
* Journey Optimizer ahora envía a Adobe Experience Platform nuevos eventos relacionados con los trabajos de exportación. Se han añadido ejemplos de consultas a la documentación. [Más información](../reports/query-examples.md)

**Administración de decisiones**

* Ahora puede especificar si la restricción de oferta se aplica a todos los usuarios o a un perfil específico, así como a todas las ubicaciones o a una. [Más información](../offers/offer-library/add-constraints.md#capping)
* La API de decisiones por lotes permite a las organizaciones utilizar la funcionalidad de Offer Decisioning para todos los perfiles de un segmento determinado en una llamada. El contenido de la oferta para cada perfil del segmento se coloca en un conjunto de datos de AEP, donde está disponible para flujos de trabajo por lotes personalizados. [Más información](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administración**

* Ahora puede habilitar/deshabilitar el vínculo de cancelación de suscripción en/desde el encabezado de correo electrónico en el nivel de ajuste preestablecido de mensaje y establecer una URL de cancelación de suscripción personalizada en el nivel de mensaje. [Más información](../configuration/message-presets.md#list-unsubscribe)
* Ahora, la lista de permitidos se puede habilitar y deshabilitar a través de la interfaz [!DNL Journey Optimizer] en entornos limitados de producción y sin producción. [Más información](../reports/allow-list.md#enable-allow-list)

**Personalización**

* Ahora puede guardar más de 40 expresiones de personalización en la biblioteca. [Más información](../personalization/personalization-library.md)

## Lanzamiento de febrero de 2022 {#feb-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Páginas de aterrizaje de suscripción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y diseñar páginas de aterrizaje en Journey Optimizer y dirigir a los usuarios a formularios en línea en los que pueden optar por su inclusión o exclusión en la recepción de comunicaciones, o suscribirse a un servicio específico, como una newsletter.</p>
<p>Para obtener más información, consulte la <a href="../landing-pages/create-lp.md">documentación detallada</a> y el <a href="../landing-pages/lp-use-cases.md">caso de uso de muestra</a> relacionado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nueva biblioteca de expresiones de personalización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora proporciona una biblioteca en la que puede acceder a expresiones de personalización predefinidas. Estas expresiones las configuran los usuarios administradores.</p>
<p>Para obtener más información, consulte la <a href="../personalization/personalization-library.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Pasar información para realizar un seguimiento de los mensajes con parámetros de seguimiento de UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En el contenido del mensaje de Journey Optimizer, ahora puede añadir parámetros UTM a sus vínculos: pueden proporcionar datos adicionales sobre ese vínculo y ayudarle a identificar dónde y por qué hizo clic una persona en él.</p>
<p>Para obtener más información, consulte la <a href="../configuration/message-presets.md#configure-email-settings">documentación detallada</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Para optimizar el rendimiento, todos los recorridos en modo de prueba que no se hayan activado durante una semana volverán al estado Borrador. [Más información](../building-journeys/testing-the-journey.md#important_notes)
* La integración entre Journey Optimizer y Adobe Campaign Classic se ha optimizado para mejorar el rendimiento. La configuración predeterminada de límite se ha cambiado a 4000 llamadas/cinco minutos.	[Más información](../action/acc-action.md#important-notes)

**Creación de informes**

* Ahora se pueden filtrar los envíos en función de su estado:
   * Desde la lista Ejecución de mensajes, ahora puede excluir pruebas de la lista de envíos.
   * Desde los informes activos/globales, puede elegir excluir los eventos de prueba.

* Ahora puede acceder a los informes sobre los datos de optimización del tiempo de envío: el número de personas que recibieron mensajes inmediatamente y el número de personas que recibieron mensajes con optimización de una hora, dos horas, etc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Administración de decisiones**

* Las clasificaciones y la clasificación de IA ahora se agrupan en una sola pestaña.

## Lanzamiento de enero de 2022 {#january-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Recorridos: optimice la ampliación de su IP con las condiciones del límite del perfil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al configurar una actividad de <strong>Condición</strong> en un recorrido, ahora puede definir un límite de perfil. Este nuevo tipo de condición le permite establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa. Esto le permite aumentar el volumen de los envíos (aumento de IP). Por ejemplo, puede que desee ampliar las entregas en un dominio dividiendo la ejecución: enviar 1000 mensajes el día 1, 2000 el día 2, etc.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/condition-activity.md#profile_cap">documentación detallada</a> y el <a href="../building-journeys/ramp-up-deliveries-uc.md">ejemplo de uso</a> relacionado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recorridos: Leer la mejora de segmentos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La opción <strong>Lectura incremental</strong> se ha añadido a las actividades <strong>Leer segmento</strong> recurrentes. Esta opción le permite dirigirse únicamente a las personas que ingresaron al segmento desde la última ejecución del recorrido. La primera ejecución siempre se dirige a todos los miembros del segmento.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Los eventos de paso de Journey Optimizer ahora se pueden vincular a otros conjuntos de datos en [Customer Journey Analytics de Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=es). El campo **profileID**, en el esquema integrado de Evento de paso de recorrido, ahora se define como un campo de identidad. [Más información](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Al actualizar una oferta, una oferta de reserva, una colección de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en un mensaje publicado, las actualizaciones ahora se reflejan automáticamente en el mensaje correspondiente, sin necesidad de volver a publicarlas. [Más información](../offers/offers-e2e.md#insert-decision-in-email)

* Al simular qué ofertas se enviarán para un perfil de prueba determinado, ahora puede modificar los ajustes de simulación predeterminados y ver el código correspondiente a las simulaciones que se pueden utilizar para solucionar problemas. [Más información](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administración**

* Los administradores ahora pueden editar registros PTR con un subdominio CNAME configurado. [Más información](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalización**

* **Agregar a favoritos**: para ayudar a mejorar la eficacia al trabajar con la personalización, hemos introducido el concepto de guardado de favoritos. Añadir atributos diferentes al menú de favoritos permite acceder rápidamente a los elementos más utilizados. [Más información](../personalization/personalize.md#fav)
