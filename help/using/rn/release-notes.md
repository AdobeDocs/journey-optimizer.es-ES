---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 26%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Versión de julio de 2022 {#july-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Nuevo flujo de mensajería en línea</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer proporciona un nuevo flujo para la creación de mensajes en Recorrido. La mensajería en línea ahorrará a los usuarios un tiempo considerable y optimizará el proceso de flujo de trabajo para crear y enviar un correo electrónico, una notificación push o un SMS en Journey Optimizer. Al eliminar los mensajes como un paso independiente y, en su lugar, hacerlos editables en línea como parte de una acción en el lienzo del Recorrido, los usuarios deberán hacer clic en menos botones y navegar por menos pantallas para diseñar y editar su contenido.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Para obtener más información, consulte la <a href="../messages/get-started-content.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Control de acceso basado en atributos (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede identificar campos de esquema con etiquetas que definen ámbitos organizativos o de uso de datos. Los administradores pueden utilizar la interfaz Permisos para definir políticas de acceso que cubran los campos de esquema XDM y administrar mejor el acceso dado a usuarios o grupos de usuarios (usuarios internos, externos o de terceros), y administrar el acceso a tipos de datos específicos (es decir, datos personales confidenciales/SPD).</p>
<p>El uso del control de acceso basado en atributos está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte la <a href="../administration/attribute-based-access.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trabajos de toma de decisiones por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede ejecutar trabajos de toma de decisiones por lotes desde la interfaz de usuario, de modo que no necesite un desarrollador para ejecutar trabajos de api por lotes y pueda reducir el tiempo necesario para el marketing. Esta nueva interfaz le permite crear trabajos y administrar trabajos actuales o anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/batch-delivery.md">documentación detallada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizar automáticamente la oferta de mejor rendimiento en sus decisiones (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos de optimización personalizados en Administración de decisiones. Este nuevo tipo de modelo le permite optimizar y personalizar ofertas en función de segmentos y ofrecer rendimiento.</p>
<p>El uso de modelos de IA de optimización personalizados está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/ranking/personalized-optimization-model.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.
-->

**Mensajes**

* Los mensajes preestablecidos ya están **superficies de canal**. [Más información](../configuration/channel-surfaces.md)

**Administración**

* **Edición de registro de PTR** - Ahora, al actualizar un registro PTR, el tiempo de procesamiento solo tardará 3 horas. [Más información](../configuration/ptr-records.md#processing)

* **IU de lista de permitidos** - Ahora puede utilizar la interfaz de usuario de Journey Optimizer para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos. [Más información](../configuration/allow-list.md)

* **actualización de la lógica de lista de permitidos** - Ahora la lógica de lista de permitidos se aplica en cuanto la función está habilitada, incluso si la lista está vacía. [Más información](../configuration/allow-list.md#logic)

* **Parámetros de seguimiento de URL** - Ahora puede utilizar el Editor de expresiones para configurar los parámetros de seguimiento de URL en sus superficies de correo electrónico (es decir, ajustes preestablecidos de mensajes). [Más información](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Tamaño de la audiencia** : Ahora se muestra un nuevo componente de estimación del tamaño de la audiencia en la interfaz de usuario al crear una regla de decisión, al seleccionar un segmento o una regla para establecer la idoneidad de una oferta o al añadir un segmento o una regla al ámbito de decisión.