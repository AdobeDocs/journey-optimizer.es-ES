---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0fc693054ad7931545e0053249f310aed031c8c4
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 90%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.


## Notas de la primera versión de julio de 2024 {#27-4-2024}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en esta página en la fecha del lanzamiento.

**Fecha de la versión**: 30-31 de julio de 2024

### Nuevas funciones {#27-4-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Canal de SMS con cualquier proveedor (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar proveedores de SMS adicionales en Journey Optimizer, además de los proveedores predeterminados Sinch, Infobip y Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composición de audiencia federada (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composición de audiencias federada ya está disponible en Adobe Journey Optimizer. Permite a las empresas componer datos para una mejor utilización en varios casos de uso. Con este nuevo enfoque, como usuario de Adobe Real-time Customer Data Platform o Adobe Journey Optimizer, puede federar conjuntos de datos directamente desde el almacén de datos existente para crear y enriquecer audiencias y atributos de Adobe Experience Platform, todo en un sistema.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#27-4-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

* (Fecha de disponibilidad: 8 de julio) **Editor de expresiones avanzadas en la configuración de eventos de recorrido**: ahora puede aprovechar el editor de expresiones avanzadas al configurar un evento, lo que le permite definir expresiones más complejas o utilizar funciones en la condición de ID de evento. [Más información](../event/about-creating.md#adv-exp-editor)

**Públicos**

* El uso de públicos de carga personalizada (archivo CSV) ya está disponible para su uso con Privacy and Security Shield.

## Notas de la versión de junio de 2024 {#24-6-2024}

**Fecha de lanzamiento**: 18 y 19 de junio de 2024

### Nuevas funciones {#june-24-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Personalización de fragmentos de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir campos específicos en un fragmento que se pueden editar cuando el fragmento se añade a una campaña o un recorrido. Esto permite ajustar las partes de contenido en el momento de su uso, lo que ofrece flexibilidad para anular los valores predeterminados con detalles específicos del contexto.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Para obtener más información, consulte la <a href="../content-management/customizable-fragments.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Creación de informes con Customer Journey Analytics (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creación de informes en Journey Optimizer cuenta con una interoperabilidad mejorada con las funciones de Customer Journey Analytics, estandariza la creación de informes en ambas plataformas y mejora la coherencia y fiabilidad de los datos. Esta integración perfecta entre Journey Optimizer y Customer Journey Analytics proporciona una visión más clara de las métricas de rendimiento, lo que permite a los usuarios tomar decisiones más informadas.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Para obtener más información, consulte la <a href="../reports/report-gs-cja.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Asistente de IA de Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El asistente de IA es una función de la interfaz de usuario que se puede utilizar para navegar, comprender los conceptos de Adobe y obtener perspectivas operativas de su entorno específico. Está disponible en varios productos de Adobe Experience Cloud, incluido Adobe Journey Optimizer.</p>
<p>Para obtener más información, consulte la <a href="../start/ai-assistant.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mensajes multilingües en recorridos y campañas (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido sin esfuerzo en varios idiomas dentro de una sola campaña o recorrido. Con esta función, puede cambiar entre idiomas al editar su campaña o su recorrido, lo que optimiza todo el proceso de edición y mejora su capacidad para administrar de forma eficaz el contenido multilingüe.</p>
<p>Ahora mismo, el contenido multilingüe solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentación en los recorridos (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer, que ya estaba disponible en las campañas, ahora admite experimentos en los recorridos. Los experimentos son ensayos aleatorios, lo que en el contexto de las pruebas en línea significa que expone a algunos usuarios seleccionados aleatoriamente a una variación determinada de un mensaje y a otro conjunto de usuarios seleccionados aleatoriamente a otra variación o tratamiento. Después de la exposición, puede medir las métricas de resultado que le interesan, como aperturas de correos electrónicos, suscripciones o compras.</p>
<p>La experimentación en los recorridos solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Mejoras {#june24-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

#### Gestión de decisiones

* **Compatibilidad con varias reglas de gestión de decisiones**: ahora puede añadir hasta 10 reglas límite para una oferta determinada de Gestión de decisiones. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas. [Más información](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Fragmentos de contenido

>[!AVAILABILITY]
>
>Tenga en cuenta que estas mejoras se implementarán gradualmente durante varios días después del lanzamiento inicial. Aunque algunos usuarios tendrán acceso inmediato, otros pueden experimentar un retraso antes de que esté disponible en sus cuentas.

* Ahora, los fragmentos se pueden editar y los cambios se pueden propagar a todos los recorridos activos y campañas en las que se utilicen.
* Se han introducido nuevos estados para los fragmentos de contenido: **Borrador**, **Activo**, **Publicación** y **Archivado**.
* Para utilizar un fragmento de un recorrido o una campaña, ahora debe tener el estado **Activo**. Se ha añadido un nuevo paso al proceso de creación de fragmentos, que permite publicar el fragmento y se puede utilizar en recorridos y campañas. Tenga en cuenta que la publicación de fragmentos requiere un nuevo permiso.

  **PRECAUCIÓN**: puesto que los estados **Borrador** y **Activo** se han incorporado con la versión de junio de Journey Optimizer, el estado de todos los fragmentos creados antes de esta versión es **Borrador**, incluso si se utilizan en un recorrido o una campaña. Si realiza algún cambio en estos fragmentos, debe [publicarlos](../content-management/create-fragments.md#publish) para que tengan el estado “Activo” y propagarlos a las campañas y recorridos asociados. También debe crear una nueva versión del recorrido/campaña y publicarla. 

Obtenga más información en la documentación de [fragmento de contenido](../content-management/fragments.md).

#### Recorridos

* El tiempo de espera global de los Recorridos se ha ampliado a 91 días. [Más información](../building-journeys/journey-properties.md#global_timeout)

  Cualquier nuevo recorrido creado tendrá reflejado este nuevo tiempo de espera. Consulte esta sección [Sección de preguntas frecuentes](../building-journeys/journey-properties.md#timeout-faq) para obtener más información. Tenga en cuenta que estos cambios se implementarán gradualmente durante el mes de junio.


* Adobe Journey Optimizer ahora admite solicitudes de eliminación/acceso de privacidad, así como solicitudes de administración del ciclo de vida de datos. [Más información](../privacy/requests.md)
* Ahora puede cambiar el tamaño de las columnas en el inventario de recorridos.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* Las **políticas de combinación** ahora son de disponibilidad general (GA): las políticas de combinación que Journey utiliza ahora son visibles y homogéneas en todo el recorrido. [Más información](../building-journeys/journey-properties.md#merge-policies)



#### Campañas

* Al crear una campaña en Adobe Journey Optimizer, ahora puede elegir el tipo de campaña (programada o activada) en un nuevo modal. [Más información](../campaigns/create-campaign.md)

#### Canal de correo electrónico

* **Habilitar cancelación de suscripción a lista**: después de los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer admite la opción de Habilitar cancelación de suscripción a lista “después de 1 clic”. Consulte las siguientes páginas: [Administrar la exclusión de correo electrónico](../email/email-opt-out.md#unsubscribe-header) y [Configuración de correo electrónico](../email/email-settings.md#list-unsubscribe).

  **NOTA**: Para cualquier superficie de canal nueva, de forma predeterminada, se activa la opción de encabezado de cancelación de suscripción a lista. Para las superficies existentes, de forma predeterminada, la opción de URL de cancelación de suscripción con un clic en la configuración de la superficie de canal no está marcada. Si anteriormente utilizaba una URL de exclusión con un clic en el cuerpo del correo electrónico, esta configuración sigue siendo válida. Si la opción de URL de cancelación de suscripción con un clic está marcada en la configuración de la superficie de canal, Adobe Journey Optimizer utilizará la URL de cancelación de suscripción con un clic generada de forma predeterminada en la configuración de la superficie de canal.

#### Canal de SMS

* Ahora puede añadir códigos cortos únicos para cada zona protegida con una sola configuración de API, lo que hace que el proceso sea más eficiente y optimizado. [Más información](../sms/sms-configuration.md)

* Después de la creación, el campo **Token de API** en la página **Detalles de credenciales de API** está ahora enmascarada.

<!--* You can now modify existing SMS configurations.-->

#### Canal en la aplicación

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Ahora puede utilizar el complemento Edge Delivery para obtener la información necesaria para comprender y solucionar problemas de las implementaciones entrantes. [Más información sobre la vista de Edge Delivery](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Canal de correo directo

* El canal de correo directo ya está disponible para todos los clientes. [Más información](../direct-mail/get-started-direct-mail.md)

